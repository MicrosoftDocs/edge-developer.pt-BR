---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 14b88f83e9635c94e205df05f6764e059f0def78
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011447"
---
# interface ICoreWebView2WebResourceRequestedEventArgs 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Solicitação de recurso da Web.
[get_ResourceContext](#get_resourcecontext) | O contexto de solicitação de recurso da Web.
[get_Response](#get_response) | Um espaço reservado para o objeto de resposta de recurso da Web.
[GetDeferral](#getdeferral) | Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.
[put_Response](#put_response) | Defina a propriedade Response.

## Parte

#### get_Request 

Solicitação de recurso da Web.

> Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * * Request)

O objeto de solicitação pode não ter alguns cabeçalhos que são adicionados pela pilha de rede mais tarde.

#### get_ResourceContext 

O contexto de solicitação de recurso da Web.

> [get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT * contexto)

#### get_Response 

Um espaço reservado para o objeto de resposta de recurso da Web.

> público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * resposta)

Se esse objeto estiver definido, a solicitação de recurso da Web será concluída com essa resposta.

#### GetDeferral 

Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.

> público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * adiamento)

Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação em um momento posterior.

#### put_Response 

Defina a propriedade Response.

> público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) *)

Um objeto de resposta de recurso da Web vazio pode ser criado com CreateWebResourceResponse e, em seguida, modificado para construir a resposta.

