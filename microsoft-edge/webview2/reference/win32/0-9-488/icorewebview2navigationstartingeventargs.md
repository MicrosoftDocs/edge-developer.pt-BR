---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d56f40a9780313c79f421559eaf54750828542a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697186"
---
# interface ICoreWebView2NavigationStartingEventArgs 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

Args de evento para o evento NavigationStarting.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Cancel](#get_cancel) | O host pode definir esse sinalizador para cancelar a navegação.
[get_IsRedirected](#get_isredirected) | Verdadeiro quando a navegação é redirecionada.
[get_IsUserInitiated](#get_isuserinitiated) | Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.
[get_NavigationId](#get_navigationid) | A ID da navegação.
[get_RequestHeaders](#get_requestheaders) | Os cabeçalhos da solicitação HTTP para a navegação.
[get_Uri](#get_uri) | O URI da navegação solicitada.
[put_Cancel](#put_cancel) | Defina a propriedade cancelamento.

## Parte

#### get_Cancel 

O host pode definir esse sinalizador para cancelar a navegação.

> público HRESULT [get_Cancel](#get_cancel)(bool * Cancel)

Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto. Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo. Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.

#### get_IsRedirected 

Verdadeiro quando a navegação é redirecionada.

> [get_IsRedirected](#get_isredirected)público HRESULT (bool * isredirected)

#### get_IsUserInitiated 

Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.

> [get_IsUserInitiated](#get_isuserinitiated)público HRESULT (bool * IsUserInitiated)

#### get_NavigationId 

A ID da navegação.

> [get_NavigationId](#get_navigationid)público HRESULT (UINT64 * navigation_id)

#### get_RequestHeaders 

Os cabeçalhos da solicitação HTTP para a navegação.

> Public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * * RequestHeaders)

Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.

#### get_Uri 

O URI da navegação solicitada.

> [get_Uri](#get_uri)público HRESULT (URI LPWSTR *)

#### put_Cancel 

Defina a propriedade cancelamento.

> público HRESULT [put_Cancel](#put_cancel)(bool Cancel)

