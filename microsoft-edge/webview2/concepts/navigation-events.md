---
description: Navegação
title: Navegação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314794"
---
# Eventos de navegação  

A sequência normal de eventos de navegação `NavigationStarting` `SourceChanged` é , `ContentLoading` `HistoryChanged` e, em seguida `NavigationCompleted` .  Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.  

| Sequence | Nome do evento | Detalhes |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 começa a navegar e os resultados de navegação em uma solicitação de rede.  O host é capaz de não permitir a solicitação durante o evento.  |  
| 2 | `SourceChanged`  |  A origem de WebView2 muda para uma nova URL.  O evento pode resultar de uma navegação que não causa uma solicitação de rede, como uma navegação de fragmento.  |  
| 3 | `HistoryChanged`  |  O histórico de atualizações de WebView2 como resultado da navegação.  |  
| 4 | `ContentLoading`  |  WebView2 começa a carregar conteúdo para a nova página.  |  
| 5 | `NavigationCompleted`  |  WebView2 conclui o carregamento de conteúdo na nova página.  |  

Acompanhe `navigations` cada novo documento usando a ID de navegação \( `NavigationId` \).  O `NavigationId` WebView muda sempre que há uma navegação bem-sucedida para um novo documento.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Os eventos de navegação do Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Eventos de navegação do Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> A figura anterior representa eventos de navegação com a mesma `NavigationId` propriedade no respectivo arg de evento.  

 `Navigations` com instâncias diferentes de `NavigationId` evento podem se sobrepor.  Por exemplo, quando você inicia uma navegação, precisa aguardar o evento `NavigationStarting` relacionado.  Se você iniciar outra navegação, deverá ver o evento da primeira navegação seguido do evento para a segunda navegação, seguido do evento para a primeira navegação e, em seguida, todos os outros eventos de navegação apropriados para a segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegação.  
 
 Em casos de erro, pode haver ou não um evento, dependendo se a `ContentLoading` navegação continua para uma página de erro.  
 
 No caso de um redirecionamento HTTP, há vários eventos em uma linha, onde os args de evento subsequentes têm a propriedade definida, no entanto, os `NavigationStarting` `IsRedirect` mesmos permanecem os `NavigationId` mesmos.  
 
 Mesmo documento , como navegar para `navigations` um fragmento, não resultam no evento e não `NavigationStarting` incrementam o `NavigationId` .  

Para monitorar ou cancelar dentro de subframes no WebView, use os eventos que atuam exatamente como os eventos equivalentes que não são `navigations` `FrameNavigationStarting` de `FrameNavigationCompleted` quadro.  

<!-- links -->  
