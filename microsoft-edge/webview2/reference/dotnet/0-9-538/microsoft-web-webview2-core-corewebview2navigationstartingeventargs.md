---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: cd692de6aaa3dc694fb2fe149411e5fd64de1ee2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878866"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

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

