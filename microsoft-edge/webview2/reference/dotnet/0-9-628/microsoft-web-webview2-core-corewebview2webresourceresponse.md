---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011459"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Uma resposta HTTP usada com o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Conteúdo](#content) | Conteúdo da resposta HTTP como Stream.
[Cabeçalhos](#headers) | Cabeçalhos de resposta HTTP substituídos.
[ReasonPhrase](#reasonphrase) | A frase de motivo da resposta HTTP.
[StatusCode](#statuscode) | O código de status de resposta HTTP.

## Parte

#### Conteúdo 

Conteúdo da resposta HTTP como Stream.

> [conteúdo](#content) do fluxo público

Stream deve ter todos os dados de conteúdo disponíveis no momento em que o adiamento do evento WebResourceRequested da resposta é concluído. Stream deve ser ágil ou ser criado a partir de um thread de segundo plano para evitar o impacto de desempenho no thread da interface do usuário. NULL significa sem dados de conteúdo. Semântica de IStream se aplica (retorna S_OK para ler chamadas até que todos os dados sejam esgotados).

#### Cabeçalhos 

Cabeçalhos de resposta HTTP substituídos.

> cabeçalhos [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers) públicos

#### ReasonPhrase 

A frase de motivo da resposta HTTP.

> Cadeia de caracteres pública [ReasonPhrase](#reasonphrase)

#### StatusCode 

O código de status de resposta HTTP.

> [StatusCode](#statuscode) público público

