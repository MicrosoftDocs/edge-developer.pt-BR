---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2a18fe9f8f79a109047d029affab8d84a6ef845c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652364"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

