---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2282b36d3b7dfcca83f84ed50a976d4e6622ce07
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010121"
---
# classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

