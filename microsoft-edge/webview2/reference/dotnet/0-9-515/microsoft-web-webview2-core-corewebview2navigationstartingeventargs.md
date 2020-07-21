---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886371"
---
# classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

Args de evento para o evento NavigationStarting.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Cancelar](#cancel) | O host pode definir esse sinalizador para cancelar a navegação.
[Redirecionado](#isredirected) | Verdadeiro quando a navegação é redirecionada.
[IsUserInitiated](#isuserinitiated) | Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.
[Navigationid](#navigationid) | A ID da navegação.
[RequestHeaders](#requestheaders) | Os cabeçalhos da solicitação HTTP para a navegação.
[Uri](#uri) | O URI da navegação solicitada.

## Parte

#### Cancelar 

O host pode definir esse sinalizador para cancelar a navegação.

> [cancelamento](#cancel) de booleano público

Se definido, será como se a navegação nunca ocorreu e o conteúdo da página atual estará intacto. Por motivos de desempenho, obter solicitações HTTP pode acontecer, enquanto o host está respondendo. Isso significa que os cookies podem ser definidos e usados como parte de uma solicitação de navegação.

#### Redirecionado 

Verdadeiro quando a navegação é redirecionada.

> Public bool [Isredirected](#isredirected)

#### IsUserInitiated 

Verdadeiro quando a navegação foi iniciada por meio de um gesto do usuário em oposição à navegação programática.

> Public bool [IsUserInitiated](#isuserinitiated)

#### Navigationid 

A ID da navegação.

> [navegação](#navigationid) de ULong do ULONG público

#### RequestHeaders 

Os cabeçalhos da solicitação HTTP para a navegação.

> HttpRequestHeaders público [RequestHeaders](#requestheaders)

Observe que você não pode modificar os cabeçalhos de solicitação HTTP em um evento NavigationStarting.

#### Uri 

O URI da navegação solicitada.

> [URI](#uri) da cadeia de caracteres pública

