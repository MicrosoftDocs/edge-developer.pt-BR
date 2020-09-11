---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 18048222a9d6bf4d3ad80346a41e4ef5950ca0e6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011586"
---
# interface ICoreWebView2PermissionRequestedEventArgs 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento PermissionRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_IsUserInitiated](#get_isuserinitiated) | Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.
[get_PermissionKind](#get_permissionkind) | O tipo da permissão que é solicitada.
[get_State](#get_state) | O status de uma solicitação de permissão, ou seja,
[get_Uri](#get_uri) | A origem do conteúdo da Web que solicita a permissão.
[GetDeferral](#getdeferral) | Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .
[put_State](#put_state) | Defina a propriedade State.

## Parte

#### get_IsUserInitiated 

Verdadeiro quando a solicitação de permissão foi iniciada por meio de um gesto do usuário.

> [get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool * IsUserInitiated)

Observe que a inicialização por meio de um gesto do usuário não significa que o usuário pretendia acessar o recurso associado.

#### get_PermissionKind 

O tipo da permissão que é solicitada.

> público HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND * PermissionKind)

#### get_State 

O status de uma solicitação de permissão, ou seja,

> público HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE * estado)

se a solicitação é concedida. O valor padrão é COREWEBVIEW2_PERMISSION_STATE_DEFAULT.

#### get_Uri 

A origem do conteúdo da Web que solicita a permissão.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### GetDeferral 

Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .

> público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * adiamento)

O desenvolvedor pode usar o objeto de adiamento para dar a decisão de permissão em um momento posterior.

#### put_State 

Defina a propriedade State.

> [put_State](#put_state)público HRESULT (COREWEBVIEW2_PERMISSION_STATE estado)

