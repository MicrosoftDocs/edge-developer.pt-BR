---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011506"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Cabeçalhos de resposta HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Acrescenta uma linha de cabeçalho com nome e valor.
[Contém](#contains) | Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.
[GetHeader](#getheader) | Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.
[Getheaders](#getheaders) | Obtém os valores de cabeçalho correspondentes ao nome.
[GetIterator](#getiterator) | Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.

Usado para construir um WebResourceResponse para o evento WebResourceRequested.

## Parte

#### AppendHeader 

Acrescenta uma linha de cabeçalho com nome e valor.

> public void [AppendHeader](#appendheader)(nome da cadeia de caracteres, valor da cadeia de caracteres)

#### Contém 

Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.

> Public bool [contém](#contains)(nome da cadeia de caracteres)

#### GetHeader 

Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.

> Cadeia de caracteres pública [GetHeader](#getheader)(nome da cadeia de caracteres)

#### Getheaders 

Obtém os valores de cabeçalho correspondentes ao nome.

> [CoreWebView2HttpHeadersCollectionIterator público](#getheaders)(nome da cadeia de caracteres)

#### GetIterator 

Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.

> Public CoreWebView2HttpHeadersCollectionIterator [Getiteration](#getiterator)()

