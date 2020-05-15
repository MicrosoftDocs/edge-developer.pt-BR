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
ms.openlocfilehash: 8b7ac3ab27cf5a2d9e80a77eabc488599820a02f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652776"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

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

