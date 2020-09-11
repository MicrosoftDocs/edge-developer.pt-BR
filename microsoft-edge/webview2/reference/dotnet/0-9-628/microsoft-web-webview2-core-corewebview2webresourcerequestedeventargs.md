---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011462"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Solicitação](#request) | Solicitação de recurso da Web.
[ResourceContext](#resourcecontext) | O contexto de solicitação de recurso da Web.
[Resposta](#response) | Um espaço reservado para o objeto de resposta de recurso da Web.
[GetDeferral](#getdeferral) | Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.

## Parte

#### Solicitação 

Solicitação de recurso da Web.

> [solicitação](#request) de [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) pública

O objeto de solicitação pode não ter alguns cabeçalhos que são adicionados pela pilha de rede mais tarde.

#### ResourceContext 

O contexto de solicitação de recurso da Web.

> [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) público [ResourceContext](#resourcecontext)

#### Resposta 

Um espaço reservado para o objeto de resposta de recurso da Web.

> resposta [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response) pública

Se esse objeto estiver definido, a solicitação de recurso da Web será concluída com essa resposta. Um objeto de resposta de recurso da Web vazio pode ser criado com CreateWebResourceResponse e, em seguida, modificado para construir a resposta.

#### GetDeferral 

Obtenha um objeto CoreWebView2Deferral e coloque o evento em um estado adiado.

> Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [getadiamento](#getdeferral)()

Você pode usar o objeto CoreWebView2Deferral para concluir a solicitação em um momento posterior.

