---
description: Hospedar conteúdo da Web em seus aplicativos Win32, .NET, UWP com o controle Microsoft Edge WebView2
title: Controle WebView2 do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, html de borda, Windows Forms, WinForms, WPF, .NET, WinUI, Project Reunion
ms.openlocfilehash: ec22edbc838f57c2f9c591a0f48298d61dce484c
ms.sourcegitcommit: b51df5036642060525e03cd744b7d35726326abe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526070"
---
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="dd617-104">Introdução ao Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="dd617-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="dd617-105">O controle WebView2 do Microsoft Edge permite inserir tecnologias web \(HTML, CSS e JavaScript\) em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="dd617-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="dd617-106">O controle WebView2 usa [o Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="dd617-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="dd617-107">Com WebView2, você pode inserir código da Web em diferentes partes do aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="dd617-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="dd617-108">Crie todo o aplicativo nativo em uma única instância do WebView.</span><span class="sxs-lookup"><span data-stu-id="dd617-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="dd617-109">Para obter informações sobre como começar a criar um aplicativo WebView2, navegue até [Começar](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="dd617-109">For information on how to start building a WebView2 app, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="O que é WebView?" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="dd617-111">O que é WebView?</span><span class="sxs-lookup"><span data-stu-id="dd617-111">What is WebView?</span></span>  
:::image-end:::  

## <a name="hybrid-app-approach"></a><span data-ttu-id="dd617-112">Abordagem de aplicativo híbrido</span><span class="sxs-lookup"><span data-stu-id="dd617-112">Hybrid app approach</span></span>  

<span data-ttu-id="dd617-113">Os desenvolvedores geralmente devem decidir entre a criação de um aplicativo Web ou um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="dd617-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="dd617-114">A decisão depende da troca entre o alcance e a energia.</span><span class="sxs-lookup"><span data-stu-id="dd617-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="dd617-115">Os aplicativos Web permitem um amplo alcance.</span><span class="sxs-lookup"><span data-stu-id="dd617-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="dd617-116">Como desenvolvedor da Web, você pode reutilizar a maior parte do código em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="dd617-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="dd617-117">Para acessar todos os recursos de uma plataforma nativa, use um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="dd617-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Nativo da Web" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="dd617-119">Nativo da Web</span><span class="sxs-lookup"><span data-stu-id="dd617-119">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="dd617-120">Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.</span><span class="sxs-lookup"><span data-stu-id="dd617-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="dd617-121">Os desenvolvedores de aplicativos híbridos se beneficiam das seguintes vantagens.</span><span class="sxs-lookup"><span data-stu-id="dd617-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="dd617-122">A ubiquidade e a força da plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="dd617-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="dd617-123">O poder e os recursos completos da plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="dd617-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="dd617-124">Benefícios do WebView2</span><span class="sxs-lookup"><span data-stu-id="dd617-124">WebView2 benefits</span></span>   

<!--  
:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="WebView reasons" lightbox="./media/WebView2/webviewreasons.png":::
   WebView reasons  
:::image-end:::  
-->  

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset.msft.png":::  
      **<span data-ttu-id="dd617-125">Ecossistema da Web \& skillset</span><span class="sxs-lookup"><span data-stu-id="dd617-125">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="dd617-126">Utilize toda a plataforma Web, bibliotecas, ferramentas e talentos existentes no ecossistema da Web.</span><span class="sxs-lookup"><span data-stu-id="dd617-126">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation.msft.png":::  
      **<span data-ttu-id="dd617-127">Inovação rápida</span><span class="sxs-lookup"><span data-stu-id="dd617-127">Rapid innovation</span></span>**  
      <span data-ttu-id="dd617-128">O desenvolvimento da Web permite a implantação e a iteração mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="dd617-128">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support.msft.png":::  
      **<span data-ttu-id="dd617-129">Suporte para Windows 7, 8 e 10</span><span class="sxs-lookup"><span data-stu-id="dd617-129">Windows 7, 8, and 10 support</span></span>**  
      <span data-ttu-id="dd617-130">Suporte para uma experiência de usuário consistente no Windows 7, Windows 8 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="dd617-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities.msft.png":::  
      **<span data-ttu-id="dd617-131">Recursos nativos</span><span class="sxs-lookup"><span data-stu-id="dd617-131">Native capabilities</span></span>**  
      <span data-ttu-id="dd617-132">Acesse o conjunto completo de APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="dd617-132">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing.msft.png":::  
      **<span data-ttu-id="dd617-133">Compartilhamento de código</span><span class="sxs-lookup"><span data-stu-id="dd617-133">Code-sharing</span></span>**  
      <span data-ttu-id="dd617-134">Adicionar código da Web à sua base de código permite reutilização maior em várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="dd617-134">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support.msft.png":::  
      **<span data-ttu-id="dd617-135">Suporte da Microsoft</span><span class="sxs-lookup"><span data-stu-id="dd617-135">Microsoft support</span></span>**  
      <span data-ttu-id="dd617-136">A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado em Disponibilidade Geral \(GA\).</span><span class="sxs-lookup"><span data-stu-id="dd617-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen.msft.png":::  
      **<span data-ttu-id="dd617-137">Distribuição evergreen</span><span class="sxs-lookup"><span data-stu-id="dd617-137">Evergreen distribution</span></span>**  
      <span data-ttu-id="dd617-138">Conte com uma versão atualizada do Chromium com atualizações regulares de plataforma e patches de segurança.</span><span class="sxs-lookup"><span data-stu-id="dd617-138">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed.msft.png":::  
      **<span data-ttu-id="dd617-139">Corrigidos</span><span class="sxs-lookup"><span data-stu-id="dd617-139">Fixed</span></span>**  
      <span data-ttu-id="dd617-140">\(em breve\) Escolha para empacotar os bits do Chromium em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dd617-140">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption.msft.png":::  
      **<span data-ttu-id="dd617-141">Adoção incremental</span><span class="sxs-lookup"><span data-stu-id="dd617-141">Incremental adoption</span></span>**  
      <span data-ttu-id="dd617-142">Adicione componentes da Web peça por parte ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dd617-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="getting-started"></a><span data-ttu-id="dd617-143">Começando</span><span class="sxs-lookup"><span data-stu-id="dd617-143">Getting started</span></span>  

<span data-ttu-id="dd617-144">Para criar e testar seu aplicativo usando o controle WebView2, você precisa ter</span><span class="sxs-lookup"><span data-stu-id="dd617-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="dd617-145">o [SDK WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="dd617-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="dd617-146">Selecione uma das opções a seguir para começar.</span><span class="sxs-lookup"><span data-stu-id="dd617-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="dd617-147">Iniciando com Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="dd617-147">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="dd617-148">Iniciando com o WPF</span><span class="sxs-lookup"><span data-stu-id="dd617-148">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="dd617-149">Iniciando com WinForms</span><span class="sxs-lookup"><span data-stu-id="dd617-149">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="dd617-150">Iniciando com WinUI3</span><span class="sxs-lookup"><span data-stu-id="dd617-150">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="dd617-151">O repositório de Exemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK WebView2 e padrões de uso da API.</span><span class="sxs-lookup"><span data-stu-id="dd617-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="dd617-152">À medida que mais recursos são adicionados ao SDK WebView2, os aplicativos de exemplo serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="dd617-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="dd617-153">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="dd617-153">Supported platforms</span></span>  

<span data-ttu-id="dd617-154">Uma versão Disponibilidade Geral \(GA\) ou Visualização está disponível nos seguintes ambientes de programação.</span><span class="sxs-lookup"><span data-stu-id="dd617-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="dd617-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="dd617-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="dd617-156">.NET Framework 4,5 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dd617-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="dd617-157">.NET Core 3.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dd617-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="dd617-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="dd617-158">.NET 5</span></span>  
*   <span data-ttu-id="dd617-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="dd617-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="dd617-160">Você pode executar aplicativos WebView2 nas seguintes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="dd617-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="dd617-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="dd617-161">Windows 10</span></span>  
*   <span data-ttu-id="dd617-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dd617-162">Windows 8.1</span></span>  
*   <span data-ttu-id="dd617-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="dd617-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="dd617-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="dd617-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="dd617-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dd617-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="dd617-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd617-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="dd617-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dd617-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="dd617-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="dd617-168">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="dd617-169">\*\* O suporte a WebView2 para Windows 7 e Windows Server 2008 R2 tem o mesmo ciclo de suporte do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd617-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="dd617-170">Para obter mais informações, navegue [até Sistemas Operacionais com][DeployedgeMicrosoftEdgeSupportedOS]suporte do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd617-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="dd617-171">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="dd617-171">Next steps</span></span>  

<span data-ttu-id="dd617-172">Para obter mais informações sobre como criar e implantar aplicativos WebView2, revise a documentação conceitual e os guias de como usar.</span><span class="sxs-lookup"><span data-stu-id="dd617-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

#### <a name="concepts"></a><span data-ttu-id="dd617-173">Conceitos</span><span class="sxs-lookup"><span data-stu-id="dd617-173">Concepts</span></span>  

*   [<span data-ttu-id="dd617-174">Compreender versões do SDK webView2</span><span class="sxs-lookup"><span data-stu-id="dd617-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="dd617-175">Distribuição de aplicativos usando WebView2</span><span class="sxs-lookup"><span data-stu-id="dd617-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="dd617-176">Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros</span><span class="sxs-lookup"><span data-stu-id="dd617-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="dd617-177">Gerenciar Pasta de Dados do Usuário em aplicativos WebView2</span><span class="sxs-lookup"><span data-stu-id="dd617-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserdatafolder]  
 
#### <a name="how-to-guides"></a><span data-ttu-id="dd617-178">How-To guias</span><span class="sxs-lookup"><span data-stu-id="dd617-178">How-To guides</span></span>  

*   [<span data-ttu-id="dd617-179">Como depurar com WebView2</span><span class="sxs-lookup"><span data-stu-id="dd617-179">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="dd617-180">Automatizar e testar o WebView2 com o Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="dd617-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="dd617-181">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="dd617-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Práticas recomendadas para desenvolver aplicativos WebView2 seguros | Microsoft Docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Gerenciando a pasta de dados do usuário | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Entenda as versões do SDK do WebView2 | Microsoft Docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Como começar com o WebView2 | Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Como começar com o WebView2 em aplicativos do Windows Forms (Visualização) | Microsoft Docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Como começar com WebView2 no WinUI3 (Visualização) | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Como começar com o WebView2 no WPF (Visualização) | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Como depurar com webView2 | Microsoft Docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizar e testar o WebView2 com o Microsoft Edge Driver | Microsoft Docs"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de versão do SDK WebView2 | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows UI Library 3 Preview 2 (Julho de 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Sistemas operacionais com suporte do Microsoft Edge | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | Galeria NuGet"  
