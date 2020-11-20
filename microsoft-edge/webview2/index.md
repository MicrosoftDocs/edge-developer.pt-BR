---
description: Hospedar conteúdo da Web em seus aplicativos do Win32, .NET e UWP com o controle WebView2 do Microsoft Edge
title: Controle WebView2 do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, HTML de borda, Windows Forms, WinForms, WPF, .NET, WinUI, reunião do projeto
ms.openlocfilehash: 9e5cc3a26f07a11c9fd5c21d62ecafc3ed5103f4
ms.sourcegitcommit: c619168deea44cdec8ebc80ef9ddf1d91d5f726d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/19/2020
ms.locfileid: "11182180"
---
# Introdução ao Microsoft Edge WebView2  

O controle WebView2 do Microsoft Edge permite que você incorpore tecnologias da Web \ (HTML, CSS e JavaScript \) em seus aplicativos nativos.  O controle WebView2 usa o [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.  Com o WebView2, você pode inserir código da Web em diferentes partes do seu aplicativo nativo ou criar todo o aplicativo nativo em um único WebView.  Para obter informações sobre como começar a criar um aplicativo do WebView2, navegue até [introdução](#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="O que é o WebView" lightbox="./media/WebView2/whatwebview.png":::
   O que é o WebView  
:::image-end:::  

## Abordagem do aplicativo híbrido  

Geralmente, os desenvolvedores precisam decidir entre a criação de um aplicativo Web ou um aplicativo nativo.  As dobradiças de decisão sobre a compensação entre o alcance e a potência.  Os aplicativos da Web permitem um amplo alcance.  Como um desenvolvedor da Web, você pode reutilizar a maioria, se não todo o seu código, em todas as plataformas diferentes.  No entanto, os aplicativos nativos utilizam os recursos de toda a plataforma nativa.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   Web Native  
:::image-end:::  

Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.  Os desenvolvedores de aplicativos híbridos se beneficiam do Ubiquity e da força da plataforma da Web, e da capacidade e dos recursos completos da plataforma nativa.  

## Benefícios do WebView2  

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos da WebView" lightbox="./media/WebView2/webviewreasons.png":::
   Motivos da WebView  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Ecossistema da Web \ & conjunto de qualificações**  
      Use toda a plataforma da Web, bibliotecas, ferramentas e talento existentes dentro do ecossistema da Web.  
   :::column-end:::
   :::column span="1":::
      **Inovação rápida**  
      O desenvolvimento na Web permite implantação e iteração mais rápidas.  
   :::column-end:::
   :::column span="1":::
      **Suporte do Windows 7, 8, 10**  
      Suporte para uma experiência de usuário consistente em todo o Windows 7, 8 e 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Recursos nativos**  
      Acesse o conjunto completo de APIs nativas.  
   :::column-end:::
   :::column span="1":::
      **Compartilhamento de código**  
      Adicionar código da Web à sua codebase permite maior reutilização em várias plataformas.  
   :::column-end:::
   :::column span="1":::
      **Suporte da Microsoft**  
      A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado como GA.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Distribuição para o meio-verde**  
      Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e correções de segurança.  
   :::column-end:::
   :::column span="1":::
      **Corrigido** \ (em breve \)  
      Escolha para empacotar os bits Chromium em seu aplicativo.  
   :::column-end:::
   :::column span="1":::
      **Adoção incremental**  
      Adicione componentes Web por parte do seu aplicativo.  
   :::column-end:::
:::row-end:::  

## Introdução  

Para compilar e testar seu aplicativo usando o controle WebView2, você precisa ter o [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] e o [SDK do WebView2][NugetPackagesMicrosoftWebWebView2] instalado.  Selecione uma das seguintes opções para começar.  

*   [Introdução ao Win32 C/C++][Webview2GettingstartedWin32]  
*   [Introdução ao WPF][Webview2GettingstartedWpf]  
*   [Introdução ao WinForms][Webview2GettingstartedWinforms]  
*   [Introdução ao WinUI3][Webview2GettingstartedWinui]  

O repositório de [exemplos WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK do WebView2 e os padrões de uso da API.  Conforme mais recursos forem adicionados ao SDK do WebView2, os aplicativos de exemplo serão atualizados.  

## Plataformas compatíveis  

Uma disponibilidade geral \ (GA \) ou versão de visualização está disponível nos seguintes ambientes de programação:  

*   Win32 C/C++ \ (GA \)  
*   .NET Framework 4.6.2 ou posterior \ (visualização \)  
*   .NET Core 3,0 ou posterior \ (visualização \)  
*   [WinUI 3,0][UwpToolkitsWinui3] \ (visualização \)  

Você poderá executar aplicativos do WebView2 nas seguintes versões do Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \ * \ *  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server 2012 R2  
*   Windows Server 2008 R2 \ * \ *  

> [!IMPORTANT]
> \ * \ * O suporte do WebView2 para Windows 7 e Windows Server 2008 R2 tem o mesmo ciclo de suporte que o Microsoft Edge.  Para obter mais informações, navegue até [sistemas operacionais compatíveis com o Microsoft Edge][DeployedgeMicrosoftEdgeSupportedOS].  

## Próximas etapas  

Para obter mais informações sobre como criar e implantar aplicativos do WebView2, confira a documentação conceitual e os guias de instruções.  

#### Conceitos  

*   [Entender as versões do SDK do WebView2][Webview2ConceptsVersioning]
*   [Distribuição de aplicativos usando o WebView2][Webview2ConceptsDistribution]  
*   [Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2][Webview2ConceptsSecurity]
*   [Gerenciar a pasta dados do usuário em aplicativos do WebView2][Webview2ConceptsUserdatafolder]
 
#### Guias de How-To  

*   [Como depurar com WebView2][Webview2HowtoDebug]  
*   [Automatizando e testando o WebView2 com o Microsoft Edge driver][Webview2HowtoWebdriver]  

## Entrar em contato com a equipe do Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2 | Documentos da Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Gerenciando a pasta dados do usuário | Documentos da Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Compreenda as versões do SDK do WebView2 | Documentos da Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Introdução ao WebView2 | Documentos da Microsoft"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introdução ao WebView2 em aplicativos do Windows Forms (visualização) | Documentos da Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Introdução ao WebView2 no WinUI3 (visualização) | Documentos da Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introdução ao WebView2 no WPF (visualização) | Documentos da Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Como depurar com WebView2 | Documentos da Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizando e testando o WebView2 com o Microsoft Edge driver | Documentos da Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI library 3 Preview 2 (julho de 2020) | Documentos da Microsoft"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Sistemas operacionais com suporte do Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galeria do NuGet"  
