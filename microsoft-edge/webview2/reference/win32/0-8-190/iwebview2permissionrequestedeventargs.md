---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 9d16f1c72a3921b220bd0046e78ed0c6b32a718a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652571"
---
# interface IWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento PermissionRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | A origem do conteúdo da Web que solicita a permissão.
[get_PermissionType](#get_permissiontype) | O tipo da permissão que é solicitada.
[get_IsUserInitiated](#get_isuserinitiated) | Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.
[get_State](#get_state) | O status de uma solicitação de permissão, ou seja,
[put_State](#put_state) | Defina a propriedade State.
[GetDeferral](#getdeferral) | Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .

## Parte

#### get_Uri 

A origem do conteúdo da Web que solicita a permissão.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### get_PermissionType 

O tipo da permissão que é solicitada.

> [get_PermissionType](#get_permissiontype)público HRESULT (WEBVIEW2_PERMISSION_TYPE * valor)

#### get_IsUserInitiated 

Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.

> [get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool * IsUserInitiated)

Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.

#### get_State 

O status de uma solicitação de permissão, ou seja,

> [get_State](#get_state)público HRESULT (WEBVIEW2_PERMISSION_STATE * valor)

se a solicitação é concedida. O valor padrão é WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Defina a propriedade State.

> público HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE valor)

#### GetDeferral 

Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .

> público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * adiamento)

O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.

