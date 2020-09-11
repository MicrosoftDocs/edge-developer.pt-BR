---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011509"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Iterador para uma coleção de cabeçalhos HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[HasCurrentHeader](#hascurrentheader) | True quando o iterador não ficar fora dos cabeçalhos.
[MoveNext](#movenext) | Mover o iterador para o próximo cabeçalho HTTP na coleção.

Consulte CoreWebView2HttpRequestHeaders e CoreWebView2HttpResponseHeaders.

## Parte

#### HasCurrentHeader 

True quando o iterador não ficar fora dos cabeçalhos.

> Public bool [HasCurrentHeader](#hascurrentheader)

Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.

#### MoveNext 

Mover o iterador para o próximo cabeçalho HTTP na coleção.

> Public bool [MoveNext](#movenext)()

O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP. Após isso ocorrer, o método GetCurrentHeader falhará se chamado.

