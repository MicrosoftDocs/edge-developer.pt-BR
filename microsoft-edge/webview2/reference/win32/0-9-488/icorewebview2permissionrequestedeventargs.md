---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 88f5008dbc9a4ebfccfe96299899a2474ecc6d95
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880406"
---
# 0.9.515-ICoreWebView2PermissionRequestedEventArgs de interface 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

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

> [get_PermissionKind](#get_permissionkind)público HRESULT (COREWEBVIEW2_PERMISSION_KIND * valor)

#### get_State 

O status de uma solicitação de permissão, ou seja,

> [get_State](#get_state)público HRESULT (COREWEBVIEW2_PERMISSION_STATE * valor)

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

> público HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE valor)

