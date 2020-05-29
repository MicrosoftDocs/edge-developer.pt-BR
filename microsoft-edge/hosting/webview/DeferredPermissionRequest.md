---
description: Representa uma solicitação adiada para a permissão do usuário acessar a funcionalidade do dispositivo
title: Objeto DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560978"
---
# Objeto DeferredPermissionRequest

Representa uma solicitação adiada pelo conteúdo da [WebView](../webview.md) para permissão de usuário final para acessar funcionalidade de dispositivo especializada (como geolocalização ou bloqueio de ponteiro).

```js
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```

## Métodos

### habilitar

Permite a solicitação de permissão.

```js
deferredPermissionRequest.allow();
```

#### Parâmetros

Esse método não tem parâmetros.

#### Valor de retorno

Esse método não retorna um valor.

### negar

Nega a solicitação de permissão.

```js
deferredPermissionRequest.deny();
```

#### Parâmetros

Esse método não tem parâmetros.

#### Valor de retorno

Esse método não retorna um valor.

## Propriedades

### id

Uma ID exclusiva que pode ser usada para correlacionar a DeferredPermissionRequest atual com um objeto PermissionRequest de um evento MSWebViewPermissionRequested anterior. Consulte o método **PermissionRequested. Defer** .

Essa propriedade é somente leitura.

```js
var id = deferredPermissionRequest.id;
```

##### Valor da propriedade

Tipo: **unsigned long**

### tipo

O tipo de permissão que está sendo solicitada. Pode ser um dos seguintes valores de cadeia de caracteres:

- **geolocalização: acesso**a dados de localização via Navigator. geolocalização.
- **unlimitedIndexedDBQuota**: permitir que as APIs do IndexedDB ignorem o limite de tamanho de dados armazenados usual.
- **mídia**: acesso ao microfone e à câmera via Navigator. getUserMedia.
- **pointerlock**: capacidade de bloquear e controlar o ponteiro do mouse via Element. requestPointerLock.
- **webnotifications**: capacidade de mostrar notificações da área de trabalho via janela. Forma.
- **tela**: capacidade de fazer capturas de tela por meio da API de captura de mídia.
- **immersiveview**: capacidade de controlar uma exibição VR.

Essa propriedade é somente leitura.

```js
var type = deferredPermissionRequest.type;
```

#### Valor da propriedade

Tipo: **cadeia de caracteres**

### uri

O URI (Uniform Resource Identifier) do documento que solicita permissão.

Essa propriedade é somente leitura.

```js
var uri = deferredPermissionRequest.uri;
```

##### Valor da propriedade

Tipo: **cadeia de caracteres**

## Requisitos

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong>Mínimo de cliente com suporte</strong> | Windows 10 [somente aplicativos da Windows Store] |
| <strong>Servidor mínimo com suporte</strong> |            Sem suporte             |
| <strong>Número mínimo com suporte</strong>  |            Sem suporte             |
