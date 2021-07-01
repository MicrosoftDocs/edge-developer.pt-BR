---
description: Hospedar conteúdo da Web em seus aplicativos Win32, .NET, UWP com o controle Microsoft Edge WebView2
title: Microsoft Edge Controle WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, html de borda, formulários Windows, WinForms, WPF, .NET, WinUI, Project Reunião
ms.openlocfilehash: 64c835d0122a1c72e610efed2c060f7921a8e2b5
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627982"
---
# <a name="introduction-to-microsoft-edge-webview2"></a>Introdução ao Microsoft Edge WebView2  

O Microsoft Edge webView2 permite inserir tecnologias web \(HTML, CSS e JavaScript\) em seus aplicativos nativos.  O controle WebView2 usa [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.  Com WebView2, você pode inserir código da Web em diferentes partes do aplicativo nativo.  Crie todo o aplicativo nativo em uma única instância do WebView.  Para obter informações sobre como começar a criar um aplicativo WebView2, navegue até [Introdução](#get-started).  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="O que é WebView?" lightbox="./media/WebView2/what-webview.png":::
   O que é WebView?  
:::image-end:::    

## <a name="hybrid-app-approach"></a>Abordagem de aplicativo híbrido  

Os desenvolvedores geralmente devem decidir entre a criação de um aplicativo Web ou um aplicativo nativo.  A decisão depende da troca entre o alcance e a energia.  Os aplicativos Web permitem um amplo alcance.  Como desenvolvedor da Web, você pode reutilizar a maior parte do código em diferentes plataformas.  Para acessar todos os recursos de uma plataforma nativa, use um aplicativo nativo.  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Nativo da Web" lightbox="./media/WebView2/web-native.png":::
   Nativo da Web  
:::image-end:::    

Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.  Os desenvolvedores de aplicativos híbridos se beneficiam das seguintes vantagens.  

*   A ubiquidade e a força da plataforma Web.  
*   O poder e os recursos completos da plataforma nativa.  
    
## <a name="webview2-benefits"></a>Benefícios do WebView2   

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="web-ecosystem--skillset"></a>Web ecosystem & skillset  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a>Inovação rápida  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a>Windows suporte a 7, 8 e 10  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Utilize toda a plataforma Web, bibliotecas, ferramentas e talentos existentes no ecossistema da Web.  
   :::column-end:::
   :::column span="1":::
      O desenvolvimento da Web permite a implantação e a iteração mais rápidas.  
   :::column-end:::
   :::column span="1":::
      Suporte para uma experiência de usuário consistente entre Windows 7, Windows 8 e Windows 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="native-capabilities"></a>Recursos nativos  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a>Compartilhamento de código  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a>Suporte da Microsoft  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Acesse o conjunto completo de APIs nativas.  
   :::column-end:::
   :::column span="1":::
      Adicionar código da Web à sua base de código permite reutilização maior em várias plataformas.  
   :::column-end:::
   :::column span="1":::
      A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado em Disponibilidade Geral \(GA\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="evergreen-distribution"></a>Distribuição evergreen  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a>Corrigidos  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a>Adoção incremental  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e patches de segurança.  
   :::column-end:::
   :::column span="1":::
      \(em breve\) Escolha empacotar os Chromium bits em seu aplicativo.  
   :::column-end:::
   :::column span="1":::
      Adicione componentes da Web peça por parte ao seu aplicativo.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Introdução  

Para criar e testar seu aplicativo usando o controle WebView2, você precisa ter <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->o [SDK WebView2][NugetPackagesMicrosoftWebWebView2] instalado.  Selecione uma das opções a seguir para começar.  

*   [Introdução com Win32 C/C++][Webview2GetStartedWin32]  
*   [Introdução com WPF][Webview2GetStartedWpf]  
*   [Introdução com WinForms][Webview2GetStartedWinforms]  
*   [Introdução com WinUI3][Webview2GetStartedWinui]  
    
O repositório de Exemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK WebView2 e padrões de uso da API.  À medida que mais recursos são adicionados ao SDK WebView2, os aplicativos de exemplo serão atualizados.  

## <a name="supported-platforms"></a>Plataformas compatíveis  

Uma versão Disponibilidade Geral \(GA\) ou Visualização está disponível nos seguintes ambientes de programação.  

*   Win32 C/C++ \(GA\)  
*   .NET Framework 4,5 ou posterior  
*   .NET Core 3.1 ou posterior  
*   .NET 5  
*   [WinUI 3.0][UwpToolkitsWinui3] \(Preview\)  
    
Você pode executar aplicativos WebView2 nas seguintes versões Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \*\*  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server 2012 R2  
*   Windows Server 2008 R2 \*\*  
    
> [!IMPORTANT]
> \*\* O suporte a WebView2 para Windows 7 e Windows Server 2008 R2 tem o mesmo ciclo de suporte que Microsoft Edge.  Para obter mais informações, navegue [até Microsoft Edge sistemas operacionais com suporte.][DeployedgeMicrosoftEdgeSupportedOS]  

## <a name="next-steps"></a>Próximas etapas  

Para obter mais informações sobre como criar e implantar aplicativos WebView2, revise a documentação conceitual e os guias de como usar.  

### <a name="concepts"></a>Conceitos  

*   [Compreender versões do SDK webView2][Webview2ConceptsVersioning]  
*   [Distribuição de aplicativos usando WebView2][Webview2ConceptsDistribution]  
*   [Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros][Webview2ConceptsSecurity]  
*   [Gerenciar Pasta de Dados do Usuário em aplicativos WebView2][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To guias  

*   [Como depurar com WebView2][Webview2HowToDebug]  
*   [Automatizando e testando o WebView2 com Microsoft Edge Driver][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Práticas recomendadas para desenvolver aplicativos WebView2 seguros | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Gerenciar a pasta de dados do usuário | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Entenda as versões do SDK do WebView2 | Microsoft Docs"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Começar com WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Começar com o WebView2 em Windows aplicativos de formulários (Visualização) | Microsoft Docs"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Começar a trabalhar com WebView2 no WinUI3 (Visualização) | Microsoft Docs"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Começar com WebView2 no WPF (Visualização) | Microsoft Docs"  
[Webview2HowToDebug]: ./how-to/debug.md "Como depurar com webView2 | Microsoft Docs"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatizar e testar o WebView2 com Microsoft Edge driver | Microsoft Docs"  
[Webview2ReleaseNotes]: ./release-notes.md "Notas de versão do SDK WebView2 | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows Biblioteca da Interface do Usuário 3 Visualização 2 (julho de 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge sistemas operacionais com suporte | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Galeria"  
