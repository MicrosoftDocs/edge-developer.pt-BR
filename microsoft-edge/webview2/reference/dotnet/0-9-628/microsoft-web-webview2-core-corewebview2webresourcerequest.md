---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011463"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Uma solicitação HTTP usada com o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Conteúdo](#content) | O corpo da mensagem de solicitação HTTP como Stream.
[Cabeçalhos](#headers) | Os cabeçalhos de solicitação HTTP mutável.
[Método](#method) | O método de solicitação HTTP.
[Uri](#uri) | O URI da solicitação.

## Parte

#### Conteúdo 

O corpo da mensagem de solicitação HTTP como Stream.

> [conteúdo](#content) do fluxo público

PUBLICAR dados seria aqui. Se um fluxo for definido, o que substituirá o corpo da mensagem, o fluxo deverá ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested desta resposta estiver concluído. Stream deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto no desempenho do thread da interface do usuário. NULL significa sem dados de conteúdo. Semântica de IStream se aplica (retorna S_OK para ler chamadas até que todos os dados sejam esgotados).

#### Cabeçalhos 

Os cabeçalhos de solicitação HTTP mutável.

> cabeçalhos [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers) públicos

#### Método 

O método de solicitação HTTP.

> [método](#method) de cadeia de caracteres pública

#### Uri 

O URI da solicitação.

> [URI](#uri) da cadeia de caracteres pública

