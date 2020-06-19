---
description: Fornece informações sobre uma solicitação de permissão
title: Objeto PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752112"
---
# Objeto PermissionRequest  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Fornece informações sobre uma solicitação de permissão. Esse objeto está disponível na propriedade permissionRequest dos argumentos de evento do evento WebView [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) .  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## Métodos  

### habilitar  

Permite a solicitação de permissão.  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

### adiar  

Se, em vez de, permitir ou não permitir ou não permitir uma PermissionRequest, você exigir um tempo para interagir com o usuário ou fazer outra ação assíncrona, a chamada adiará () no PermissionRequest.  O PermissionRequest agora estará disponível como um DeferredPermissionRequest de getDeferredPermissionRequests e getDeferredPermissionRequestById.  Você pode correlacionar o PermissionRequest atual com o DeferredPermissionRequest correspondente por meio da propriedade ID correspondente.  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

### negar  

Nega a solicitação de permissão.  

#### Parâmetros  

Esse método não tem parâmetros.  

#### Valor de retorno  

Esse método não retorna um valor.  

## Propriedades  

### id  

Uma ID exclusiva que pode ser usada para correlacionar a PermissionRequest atual com um DeferredPermissionRequest correspondente se o método Defer for usado.  Consulte o método Defer.  

Essa propriedade é somente leitura.  

##### Valor da propriedade  

Tipo: **unsigned long**  

### Estado  

Retorna "desconhecido", "adiar", "permitir" ou "negar" para indicar o estado atual de solicitação de permissão.  A cadeia de caracteres de estado corresponderá a qualquer método Allow, Deny ou Defer chamado Last ou "Unknown" se nenhum dos métodos tiver sido chamado.  

Essa propriedade é somente leitura.  

#### Valor da propriedade  

Tipo: **cadeia de caracteres**  

### tipo  

O tipo de permissão que está sendo solicitada. Pode ser um dos seguintes valores de cadeia de caracteres:  

*   **geolocalização: acesso**a dados de localização via Navigator. geolocalização.  
*   **unlimitedIndexedDBQuota**: permitir que as APIs do IndexedDB ignorem o limite de tamanho de dados armazenados usual.  
*   **mídia**: acesso ao microfone e à câmera via Navigator. getUserMedia.  
*   **pointerlock**: capacidade de bloquear e controlar o ponteiro do mouse via Element. requestPointerLock.  
*   **webnotifications**: capacidade de mostrar notificações da área de trabalho via janela. Forma.  
*   **tela**: capacidade de fazer capturas de tela por meio da API de captura de mídia.  
*   **immersiveview**: capacidade de controlar uma exibição VR.  

Essa propriedade é somente leitura.  

#### Valor da propriedade  

Tipo: **cadeia de caracteres**  

### uri  

O URI (Uniform Resource Identifier) do documento que solicita permissão.  

Essa propriedade é somente leitura.  

#### Valor da propriedade  

Tipo: **cadeia de caracteres**  
