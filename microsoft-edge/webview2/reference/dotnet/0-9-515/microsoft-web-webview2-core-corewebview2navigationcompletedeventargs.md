---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 3a15232a7fe2ddf230d0463069052c55f7abc843
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879132"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Args de evento para o evento NavigationCompleted.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[IsSuccess](#issuccess) | Verdadeiro quando a navegação é bem-sucedida.
[Navigationid](#navigationid) | A ID da navegação.
[WebErrorStatus](#weberrorstatus) | O código de erro se a navegação falhar.

## Parte

#### IsSuccess 

Verdadeiro quando a navegação é bem-sucedida.

> Public bool [IsSuccess](#issuccess)

Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.

#### Navigationid 

A ID da navegação.

> [navegação](#navigationid) de ULong do ULONG público

#### WebErrorStatus 

O código de erro se a navegação falhar.

> CoreWebView2WebErrorStatus público [WebErrorStatus](#weberrorstatus)

