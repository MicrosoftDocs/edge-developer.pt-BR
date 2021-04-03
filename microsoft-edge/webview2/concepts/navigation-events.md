---
description: Navegação
title: Navegação | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: e87994d6205f81e01385a131e17091d0c8b001d5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470841"
---
# <a name="navigation-events"></a>Eventos de navegação  

:::row:::
   :::column span="1":::
      Plataformas com suporte:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

Os eventos de navegação são executados quando ações assíncronas específicas ocorrem no conteúdo exibido em uma instância do WebView2.  Por exemplo, quando um usuário webView2 navega para um novo site, o conteúdo nativo escuta a alteração usando o `NavigationStarting` evento.  Quando a ação de navegação for concluída, `NavigationCompleted` será executado.  Para obter um bom exemplo de eventos de navegação, navegue até [WebView2 guia de início.][Webview2IndexGettingStarted]  

<!--todo:  Move the relevant information out of the getting started guide to better focus the content and leave the most concise elements in the getting started guide.  -->   

A sequência normal de eventos de navegação `NavigationStarting` `SourceChanged` é , , `ContentLoading` `HistoryChanged` e, em `NavigationCompleted` seguida.  Os eventos a seguir descrevem o estado de WebView2 durante cada navegação.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Eventos de navegação do Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
         Eventos de navegação do Microsoft Edge WebView2  
      :::image-end:::  
      
      > [!NOTE]
      > A figura representa eventos de navegação com a mesma `NavigationId` propriedade no argumento de evento respectivo.  
   :::column-end:::
   :::column span="2":::
      | Sequence | Nome do evento | Detalhes |  
      |:--- |:--- |:--- |  
      | 1 | `NavigationStarting`  |  WebView2 começa a navegar e a navegação resulta em uma solicitação de rede.  O host pode não permitir a solicitação durante o evento.  |  
      | 2 | `SourceChanged`  |  A origem do WebView2 muda para uma nova URL.  O evento pode resultar de uma ação de navegação que não causa uma solicitação de rede, como uma navegação de fragmento.  |  
      | 3 | `ContentLoading`  |  O WebView começa a carregar conteúdo para a nova página.  |  
      | 4 | `HistoryChanged`  |  A navegação faz com que o histórico de WebView2 seja atualizado.  |  
      | 5 | `NavigationCompleted`  |  WebView2 conclui o carregamento de conteúdo na nova página.  |  
   :::column-end:::
:::row-end:::

Rastrear eventos de navegação para cada novo documento usando a ID de navegação \( `NavigationId` event\).  O `NavigationId` evento do WebView muda sempre que uma navegação bem-sucedida para um novo documento é concluída.  

 Eventos de navegação com instâncias diferentes `NavigationId` de evento podem se sobrepor.  Por exemplo, ao iniciar um evento de navegação, você deve aguardar o evento `NavigationStarting` relacionado.  Se você, em seguida, iniciar outra navegação, verá o evento para a primeira navegação seguida pelo evento para a segunda navegação, seguido pelo evento para a primeira navegação e, em seguida, todo o restante dos eventos de navegação apropriados para a segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegação.  
 
 Em casos de erro, pode haver ou não um evento, dependendo se a navegação `ContentLoading` é continuada para uma página de erro.  
 
 Se ocorrer um redirecionamento HTTP, haverá vários eventos em uma linha, onde argumentos de evento posteriores têm a propriedade definida, no entanto, o evento `NavigationStarting` `IsRedirect` permanece o `NavigationId` mesmo.  
 
 Os mesmos eventos de navegação de documento, como navegar para um fragmento, não resultam no evento e `NavigationStarting` não incrementam o `NavigationId` evento.  

Para monitorar ou cancelar eventos de navegação dentro de subframes em uma instância webView2, use os eventos e que agem da mesma forma que os eventos equivalentes de contraparte não `FrameNavigationStarting` `FrameNavigationCompleted` quadro.  

## <a name="see-also"></a>Consulte também  

*   Para começar a usar o WebView2, navegue até Guias de Guia [de Iniciação da WebView2.][Webview2IndexGettingStarted]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples no][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
