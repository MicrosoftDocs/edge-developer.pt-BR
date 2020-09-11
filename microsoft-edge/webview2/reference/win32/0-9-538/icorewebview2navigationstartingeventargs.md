---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 8bf2cf37ef76256987a52fd5491e5c995244dd65
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011297"
---
# 0.9.579-ICoreWebView2NavigationStartingEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

