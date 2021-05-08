---
description: Modelo de processo
title: Modelo de processo | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 95d0c53219114c47a781317ab4b2ee2028fc586f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535612"
---
# <a name="process-model"></a>Modelo de processo  

:::row:::
   :::column span="1":::
      Plataformas com suporte:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

O WebView2 usa o mesmo modelo de processo que o navegador do Microsoft Edge.  Para obter mais informações sobre o modelo de processo do navegador, navegue até Arquitetura do Navegador - Confira o [navegador da Web moderno.][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]  

Um processo de navegador está associado aos processos de renderização e outros processos utilitários, conforme descrito neste artigo.  Além disso, se WebView2 for especificado, os processos de solicitação do aplicativo host usarão WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processo 1" lightbox="../media/process-model-1.png":::
   Processo 1  
:::image-end:::    

Um processo de navegador é associado a apenas uma pasta de dados do usuário.  Um processo de solicitação pode especificar mais de uma pasta de dados do usuário.  Um processo de solicitação que especifica mais de uma pasta de dados do usuário está associado ao mesmo número de processos do navegador.  
Por exemplo, um processo de solicitação que solicita acesso a duas pastas de dados do usuário usa dois processos de navegador.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processo 2" lightbox="../media/process-model-2.png":::
   Processo 2  
:::image-end:::    

Um processo de navegador está associado a vários processos de renderização.  Uma instância do WebView 2 cria um processo de navegador para quadros de serviço.  Um processo de navegador pode estar associado a vários quadros.  Um processo de navegador pode ser associado a instâncias diferentes do WebView2.  O número de processos de renderização varia com base nas seguintes condições.  

*   Uso do recurso de isolamento de site no navegador.  
*   O número de origens desconectadas distintas renderizadas em instâncias associadas de WebView2.  
    
O recurso de navegador de isolamento de site é descrito no conteúdo anterior. 
<!--todo:  which previous content?  -->  

Representa `CoreWebView2Environment` uma pasta de dados do usuário e um processo de navegador.  O não corresponde diretamente a nenhum conjunto de processos, pois vários processos renderer são usados por um WebView2, dependendo do isolamento do `CoreWebView2` site, conforme descrito anteriormente.  

Para reagir a falhas e travamentos nos processos do navegador e do renderador, use o `ProcessFailed` evento `CoreWebView2` de .  

Para desligar com segurança os processos de renderização e navegador associados, use o `Close` método `CoreWebView2Controller` de .  

Para abrir a janela Gerenciador de Tarefas do Navegador na janela **DevTools** de uma instância do WebView2, conclua as seguintes ações.  

*   Selecione `Shift` + `Escape` .  
*   Passe o mouse na barra de título da janela DevTools, abra o menu contextual \(clique com o botão direito do mouse\) e escolha `Browser task manager` .  
    
Todos os processos associados ao processo de navegador do WebView2 são exibidos, incluindo finalidades associadas.  

## <a name="see-also"></a>Ver também  

*   Para começar a usar o WebView2, navegue até Guias de Início da [WebView2.][Webview2IndexGetStarted]  
*   Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples no][GithubMicrosoftedgeWebview2samples] GitHub.  
*   Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitetura do Navegador - Veja o navegador da Web moderno (parte 1)"  
