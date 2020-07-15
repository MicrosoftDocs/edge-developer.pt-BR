---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: aaaad1f622887ed1c941a9cf12ee4c753b352286
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878880"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

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

