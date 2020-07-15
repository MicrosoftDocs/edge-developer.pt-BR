---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2f9fb899746922206ff3f6cbfd129d69389fd60e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879307"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Solicitação](#request) | A solicitação HTTP.
[ResourceContext](#resourcecontext) | Os contextos de solicitação de recurso da Web.
[Resposta](#response) | A resposta HTTP.
[GetDeferral](#getdeferral) | Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.

## Parte

#### Solicitação 

A solicitação HTTP.

> [solicitação](#request) de HttpRequestMessage pública

#### ResourceContext 

Os contextos de solicitação de recurso da Web.

> [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)

#### Resposta 

A resposta HTTP.

> [resposta](#response) HttpResponseMessage pública

#### GetDeferral 

Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.

> Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()

Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação de rede em um momento posterior.

