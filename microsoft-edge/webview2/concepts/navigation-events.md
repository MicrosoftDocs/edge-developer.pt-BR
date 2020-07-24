---
description: Navegação
title: Navegação
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895539"
---
# Eventos de navegação  

A sequência normal de eventos de navegação é `NavigationStarting` , `SourceChanged` ,, `ContentLoading` `HistoryChanged` e `NavigationCompleted` .  Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.  

| Ordena | Nome do evento | Detalhes |  
|:--- |:--- |:--- |  
| um | `NavigationStarting`  |  O WebView2 começa a navegar e a navegação resulta em uma solicitação de rede.  O host pode impedir a solicitação durante o evento.  |  
| 2 | `SourceChanged`  |  A fonte de WebView2 muda para uma nova URL.  O evento pode resultar de uma navegação que não causa uma solicitação de rede, como uma navegação de fragmento.  |  
| 3D | `HistoryChanged`  |  O histórico de atualizações do WebView2 como resultado da navegação.  |  
| 4 | `ContentLoading`  |  O WebView começa a carregar o conteúdo da nova página.  |  
| 5 | `NavigationCompleted`  |  O WebView2 conclui o carregamento do conteúdo na nova página.  |  

Acompanhe `navigations` cada novo documento usando a identificação de navegação \ ( `NavigationId` \).  O `NavigationId` do WebView muda a cada vez que há uma navegação com êxito para um novo documento.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Os eventos de navegação do Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Os eventos de navegação do Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> A figura anterior representa eventos de navegação com a mesma `NavigationId` propriedade no argumento de evento respectiva.  

 `Navigations` eventos com diferentes instâncias de `NavigationId` evento podem sobrepor-se.  Por exemplo, quando você inicia uma navegação, é preciso aguardar o `NavigationStarting` evento relacionado.  Se, em seguida, você iniciar outra navegação, verá o `NavigationStarting` evento para a primeira navegação acompanhada pelo `NavigationStarting` evento para a segunda navegação, seguida do `NavigationCompleted` evento para a primeira navegação e todos os demais eventos de navegação apropriados para a segunda navegação.  
 
 Em casos de erro, pode ou não ser um `ContentLoading` evento, dependendo se a navegação é continuada para uma página de erro.  
 
 No caso de um redirecionamento HTTP, há vários `NavigationStarting` eventos em uma linha, onde os args de eventos subsequentes têm a `IsRedirect` propriedade definida, no entanto, o `NavigationId` restante é o mesmo.  
 
 O mesmo documento `navigations` , como navegar para um fragmento, não resulta no `NavigationStarting` evento e não aumenta o `NavigationId` .  

Para monitorar ou cancelar `navigations` subquadros dentro do WebView, use os `FrameNavigationStarting` eventos e os `FrameNavigationCompleted` eventos que atuam exatamente como os eventos equivalentes sem quadro correspondente.  

<!-- links -->  
