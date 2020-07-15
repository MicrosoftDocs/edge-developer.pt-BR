---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: c2ac2e499e6bbd49f411a001e061af72fda524b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877879"
---
# 0.9.430-ICoreWebView2NavigationStartingEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

Args de evento para o evento NavigationStarting.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | O URI da navegação solicitada.
[get_IsUserInitiated](#get_isuserinitiated) | Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.
[get_IsRedirected](#get_isredirected) | Verdadeiro quando a navegação é redirecionada.
[get_RequestHeaders](#get_requestheaders) | Os cabeçalhos da solicitação HTTP para a navegação.
[get_Cancel](#get_cancel) | O host pode definir esse sinalizador para cancelar a navegação.
[put_Cancel](#put_cancel) | Defina a propriedade cancelamento.
[get_NavigationId](#get_navigationid) | A ID da navegação.

## Parte

#### get_Uri 

O URI da navegação solicitada.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### get_IsUserInitiated 

Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.

> [get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool * IsUserInitiated)

#### get_IsRedirected 

Verdadeiro quando a navegação é redirecionada.

> [get_IsRedirected](#get_isredirected)público HRESULT (bool * isredirected)

#### get_RequestHeaders 

Os cabeçalhos da solicitação HTTP para a navegação.

> Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) * * RequestHeaders)

Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.

#### get_Cancel 

O host pode definir esse sinalizador para cancelar a navegação.

> público HRESULT [get_Cancel](#get_cancel)(bool * Cancel)

Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto. Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo. Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.

#### put_Cancel 

Defina a propriedade cancelamento.

> público HRESULT [put_Cancel](#put_cancel)(bool Cancel)

#### get_NavigationId 

A ID da navegação.

> [get_NavigationId](#get_navigationid)público HRESULT (UINT64 * navigation_id)

