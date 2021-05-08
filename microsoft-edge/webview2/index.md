---
description: Hospedar conteúdo da Web em seus aplicativos Win32, .NET, UWP com o controle Microsoft Edge WebView2
title: Controle WebView2 do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, html de borda, Windows Forms, WinForms, WPF, .NET, WinUI, Project Reunion
ms.openlocfilehash: 154c18a3cc9236a8abd286918d72e1a1968fea38
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535717"
---
# <a name="introduction-to-microsoft-edge-webview2"></a>Introdução ao Microsoft Edge WebView2  

O controle WebView2 do Microsoft Edge permite inserir tecnologias web \(HTML, CSS e JavaScript\) em seus aplicativos nativos.  O controle WebView2 usa [o Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.  Com WebView2, você pode inserir código da Web em diferentes partes do aplicativo nativo.  Crie todo o aplicativo nativo em uma única instância do WebView.  Para obter informações sobre como começar a criar um aplicativo WebView2, navegue até [Começar](#get-started).  

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

<!--  
:::image type="complex" source="./media/WebView2/webview-reasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webview-reasons.png":::
   WebView reasons  
:::image-end:::    
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **Ecossistema da Web \& skillset**  
      Utilize toda a plataforma Web, bibliotecas, ferramentas e talentos existentes no ecossistema da Web.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **Inovação rápida**  
      O desenvolvimento da Web permite a implantação e a iteração mais rápidas.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **Suporte para Windows 7, 8 e 10**  
      Suporte para uma experiência de usuário consistente no Windows 7, Windows 8 e Windows 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **Recursos nativos**  
      Acesse o conjunto completo de APIs nativas.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **Compartilhamento de código**  
      Adicionar código da Web à sua base de código permite reutilização maior em várias plataformas.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **Suporte da Microsoft**  
      A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado em Disponibilidade Geral \(GA\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **Distribuição evergreen**  
      Conte com uma versão atualizada do Chromium com atualizações regulares de plataforma e patches de segurança.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **Corrigidos**  
      \(em breve\) Escolha para empacotar os bits do Chromium em seu aplicativo.  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **Adoção incremental**  
      Adicione componentes da Web peça por parte ao seu aplicativo.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Introdução  

Para criar e testar seu aplicativo usando o controle WebView2, você precisa ter <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->o [SDK WebView2][NugetPackagesMicrosoftWebWebView2] instalado.  Selecione uma das opções a seguir para começar.  

*   [Começar com Win32 C/C++][Webview2GetStartedWin32]  
*   [Começar com o WPF][Webview2GetStartedWpf]  
*   [Começar com WinForms][Webview2GetStartedWinforms]  
*   [Começar com WinUI3][Webview2GetStartedWinui]  
    
O repositório de Exemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK WebView2 e padrões de uso da API.  À medida que mais recursos são adicionados ao SDK WebView2, os aplicativos de exemplo serão atualizados.  

## <a name="supported-platforms"></a>Plataformas compatíveis  

Uma versão Disponibilidade Geral \(GA\) ou Visualização está disponível nos seguintes ambientes de programação.  

*   Win32 C/C++ \(GA\)  
*   .NET Framework 4,5 ou posterior  
*   .NET Core 3.1 ou posterior  
*   .NET 5  
*   [WinUI 3.0][UwpToolkitsWinui3] \(Preview\)  
    
Você pode executar aplicativos WebView2 nas seguintes versões do Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \*\*  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server 2012 R2  
*   Windows Server 2008 R2 \*\*  
    
> [!IMPORTANT]
> \*\* O suporte a WebView2 para Windows 7 e Windows Server 2008 R2 tem o mesmo ciclo de suporte do Microsoft Edge.  Para obter mais informações, navegue [até Sistemas Operacionais com][DeployedgeMicrosoftEdgeSupportedOS]suporte do Microsoft Edge.  

## <a name="next-steps"></a>Próximas etapas  

Para obter mais informações sobre como criar e implantar aplicativos WebView2, revise a documentação conceitual e os guias de como usar.  

### <a name="concepts"></a>Conceitos  

*   [Compreender versões do SDK webView2][Webview2ConceptsVersioning]  
*   [Distribuição de aplicativos usando WebView2][Webview2ConceptsDistribution]  
*   [Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros][Webview2ConceptsSecurity]  
*   [Gerenciar Pasta de Dados do Usuário em aplicativos WebView2][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To guias  

*   [Como depurar com WebView2][Webview2HowToDebug]  
*   [Automatizar e testar o WebView2 com o Microsoft Edge Driver][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Práticas recomendadas para desenvolver aplicativos WebView2 seguros | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Gerenciar a pasta de dados do usuário | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Entenda as versões do SDK do WebView2 | Microsoft Docs"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Começar com WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Começar a trabalhar com o WebView2 em aplicativos do Windows Forms (Visualização) | Microsoft Docs"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Começar a trabalhar com WebView2 no WinUI3 (Visualização) | Microsoft Docs"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Começar com WebView2 no WPF (Visualização) | Microsoft Docs"  
[Webview2HowToDebug]: ./how-to/debug.md "Como depurar com webView2 | Microsoft Docs"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatizar e testar o WebView2 com o Microsoft Edge Driver | Microsoft Docs"  
[Webview2ReleaseNotes]: ./release-notes.md "Notas de versão do SDK WebView2 | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (Julho de 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Sistemas operacionais com suporte do Microsoft Edge | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | Galeria NuGet"  
