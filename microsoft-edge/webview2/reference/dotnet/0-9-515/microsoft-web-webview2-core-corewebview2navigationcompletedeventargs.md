---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885076"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

