---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011442"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Cabeçalhos de solicitação HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Contém](#contains) | Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.
[GetHeader](#getheader) | Obtém o valor do cabeçalho que corresponde ao nome.
[Getheaders](#getheaders) | Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.
[GetIterator](#getiterator) | Obtém um iterador sobre a coleção de cabeçalhos de solicitação.
[RemoveHeader](#removeheader) | Remove o cabeçalho que corresponde ao nome.
[SetHeader](#setheader) | Adiciona ou atualiza o cabeçalho que corresponde ao nome.

Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting. Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.

## Parte

#### Contém 

Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.

> Public bool [contém](#contains)(nome da cadeia de caracteres)

#### GetHeader 

Obtém o valor do cabeçalho que corresponde ao nome.

> Cadeia de caracteres pública [GetHeader](#getheader)(nome da cadeia de caracteres)

#### Getheaders 

Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.

> [CoreWebView2HttpHeadersCollectionIterator público](#getheaders)(nome da cadeia de caracteres)

#### GetIterator 

Obtém um iterador sobre a coleção de cabeçalhos de solicitação.

> Public CoreWebView2HttpHeadersCollectionIterator [Getiteration](#getiterator)()

#### RemoveHeader 

Remove o cabeçalho que corresponde ao nome.

> public void [RemoveHeader](#removeheader)(nome da cadeia de caracteres)

#### SetHeader 

Adiciona ou atualiza o cabeçalho que corresponde ao nome.

> valor de [cadeia de caracteres void público](#setheader)(nome da cadeia de caracteres, valor da cadeia de caracteres)

