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
# <a name="introduction-to-microsoft-edge-webview2"></a><span data-ttu-id="9d9a2-104">Introdução ao Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="9d9a2-105">O Microsoft Edge webView2 permite inserir tecnologias web \(HTML, CSS e JavaScript\) em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-105">The Microsoft Edge WebView2 control allows you to embed web technologies \(HTML, CSS, and JavaScript\) in your native apps.</span></span>  <span data-ttu-id="9d9a2-106">O controle WebView2 usa [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native apps.</span></span>  <span data-ttu-id="9d9a2-107">Com WebView2, você pode inserir código da Web em diferentes partes do aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-107">With WebView2, you may embed web code in different parts of your native app.</span></span>  <span data-ttu-id="9d9a2-108">Crie todo o aplicativo nativo em uma única instância do WebView.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-108">Build all of the native app within a single WebView instance.</span></span>  <span data-ttu-id="9d9a2-109">Para obter informações sobre como começar a criar um aplicativo WebView2, navegue até [Introdução](#get-started).</span><span class="sxs-lookup"><span data-stu-id="9d9a2-109">For information on how to start building a WebView2 app, navigate to [Get Started](#get-started).</span></span>  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="O que é WebView?" lightbox="./media/WebView2/what-webview.png":::
   <span data-ttu-id="9d9a2-111">O que é WebView?</span><span class="sxs-lookup"><span data-stu-id="9d9a2-111">What is WebView?</span></span>  
:::image-end:::    

## <a name="hybrid-app-approach"></a><span data-ttu-id="9d9a2-112">Abordagem de aplicativo híbrido</span><span class="sxs-lookup"><span data-stu-id="9d9a2-112">Hybrid app approach</span></span>  

<span data-ttu-id="9d9a2-113">Os desenvolvedores geralmente devem decidir entre a criação de um aplicativo Web ou um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-113">Developers must often decide between building a web app or a native app.</span></span>  <span data-ttu-id="9d9a2-114">A decisão depende da troca entre o alcance e a energia.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-114">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="9d9a2-115">Os aplicativos Web permitem um amplo alcance.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-115">Web apps allow for a broad reach.</span></span>  <span data-ttu-id="9d9a2-116">Como desenvolvedor da Web, você pode reutilizar a maior parte do código em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-116">As a Web developer, you may reuse most of your code across different platforms.</span></span>  <span data-ttu-id="9d9a2-117">Para acessar todos os recursos de uma plataforma nativa, use um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-117">To access the all capabilities of a native platform, use a native app.</span></span>  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Nativo da Web" lightbox="./media/WebView2/web-native.png":::
   <span data-ttu-id="9d9a2-119">Nativo da Web</span><span class="sxs-lookup"><span data-stu-id="9d9a2-119">Web native</span></span>  
:::image-end:::    

<span data-ttu-id="9d9a2-120">Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-120">Hybrid apps allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="9d9a2-121">Os desenvolvedores de aplicativos híbridos se beneficiam das seguintes vantagens.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-121">Hybrid app developers benefit from the following advantages.</span></span>  

*   <span data-ttu-id="9d9a2-122">A ubiquidade e a força da plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-122">The ubiquity and strength of the web platform.</span></span>  
*   <span data-ttu-id="9d9a2-123">O poder e os recursos completos da plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-123">The power and full capabilities of the native platform.</span></span>  
    
## <a name="webview2-benefits"></a><span data-ttu-id="9d9a2-124">Benefícios do WebView2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-124">WebView2 benefits</span></span>   

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
      ### <a name="web-ecosystem--skillset"></a><span data-ttu-id="9d9a2-125">Web ecosystem & skillset</span><span class="sxs-lookup"><span data-stu-id="9d9a2-125">Web ecosystem & skillset</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a><span data-ttu-id="9d9a2-126">Inovação rápida</span><span class="sxs-lookup"><span data-stu-id="9d9a2-126">Rapid innovation</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a><span data-ttu-id="9d9a2-127">Windows suporte a 7, 8 e 10</span><span class="sxs-lookup"><span data-stu-id="9d9a2-127">Windows 7, 8, and 10 support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-128">Utilize toda a plataforma Web, bibliotecas, ferramentas e talentos existentes no ecossistema da Web.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-129">O desenvolvimento da Web permite a implantação e a iteração mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-130">Suporte para uma experiência de usuário consistente entre Windows 7, Windows 8 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-130">Support for a consistent user experience across Windows 7, Windows 8, and Windows 10.</span></span>  
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
      ### <a name="native-capabilities"></a><span data-ttu-id="9d9a2-131">Recursos nativos</span><span class="sxs-lookup"><span data-stu-id="9d9a2-131">Native capabilities</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a><span data-ttu-id="9d9a2-132">Compartilhamento de código</span><span class="sxs-lookup"><span data-stu-id="9d9a2-132">Code-sharing</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a><span data-ttu-id="9d9a2-133">Suporte da Microsoft</span><span class="sxs-lookup"><span data-stu-id="9d9a2-133">Microsoft support</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-134">Acesse o conjunto completo de APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-135">Adicionar código da Web à sua base de código permite reutilização maior em várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-135">Add web code to your codebase allows for increased reuse across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-136">A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado em Disponibilidade Geral \(GA\).</span><span class="sxs-lookup"><span data-stu-id="9d9a2-136">Microsoft provides support and adds new feature requests when WebView2 releases at Generally Availability \(GA\).</span></span>  
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
      ### <a name="evergreen-distribution"></a><span data-ttu-id="9d9a2-137">Distribuição evergreen</span><span class="sxs-lookup"><span data-stu-id="9d9a2-137">Evergreen distribution</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a><span data-ttu-id="9d9a2-138">Corrigidos</span><span class="sxs-lookup"><span data-stu-id="9d9a2-138">Fixed</span></span>  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a><span data-ttu-id="9d9a2-139">Adoção incremental</span><span class="sxs-lookup"><span data-stu-id="9d9a2-139">Incremental adoption</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-140">Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e patches de segurança.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-141">\(em breve\) Escolha empacotar os Chromium bits em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-141">\(coming soon\)  Choose to package the Chromium bits in your app.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9d9a2-142">Adicione componentes da Web peça por parte ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-142">Add web components piece by piece to your app.</span></span>  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a><span data-ttu-id="9d9a2-143">Introdução</span><span class="sxs-lookup"><span data-stu-id="9d9a2-143">Get started</span></span>  

<span data-ttu-id="9d9a2-144">Para criar e testar seu aplicativo usando o controle WebView2, você precisa ter</span><span class="sxs-lookup"><span data-stu-id="9d9a2-144">To build and test your app using the WebView2 control, you need to have</span></span> <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  --><span data-ttu-id="9d9a2-145">o [SDK WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-145">the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="9d9a2-146">Selecione uma das opções a seguir para começar.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="9d9a2-147">Introdução com Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="9d9a2-147">Get Started with Win32 C/C++</span></span>][Webview2GetStartedWin32]  
*   [<span data-ttu-id="9d9a2-148">Introdução com WPF</span><span class="sxs-lookup"><span data-stu-id="9d9a2-148">Get Started with WPF</span></span>][Webview2GetStartedWpf]  
*   [<span data-ttu-id="9d9a2-149">Introdução com WinForms</span><span class="sxs-lookup"><span data-stu-id="9d9a2-149">Get Started with WinForms</span></span>][Webview2GetStartedWinforms]  
*   [<span data-ttu-id="9d9a2-150">Introdução com WinUI3</span><span class="sxs-lookup"><span data-stu-id="9d9a2-150">Get Started with WinUI3</span></span>][Webview2GetStartedWinui]  
    
<span data-ttu-id="9d9a2-151">O repositório de Exemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK WebView2 e padrões de uso da API.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-151">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="9d9a2-152">À medida que mais recursos são adicionados ao SDK WebView2, os aplicativos de exemplo serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-152">As more features are added to the WebView2 SDK, the sample apps will be updated.</span></span>  

## <a name="supported-platforms"></a><span data-ttu-id="9d9a2-153">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="9d9a2-153">Supported platforms</span></span>  

<span data-ttu-id="9d9a2-154">Uma versão Disponibilidade Geral \(GA\) ou Visualização está disponível nos seguintes ambientes de programação.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-154">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="9d9a2-155">Win32 C/C++ \(GA\)</span><span class="sxs-lookup"><span data-stu-id="9d9a2-155">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="9d9a2-156">.NET Framework 4,5 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d9a2-156">.NET Framework 4.5 or later</span></span>  
*   <span data-ttu-id="9d9a2-157">.NET Core 3.1 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d9a2-157">.NET Core 3.1 or later</span></span>  
*   <span data-ttu-id="9d9a2-158">.NET 5</span><span class="sxs-lookup"><span data-stu-id="9d9a2-158">.NET 5</span></span>  
*   <span data-ttu-id="9d9a2-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span><span class="sxs-lookup"><span data-stu-id="9d9a2-159">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  
    
<span data-ttu-id="9d9a2-160">Você pode executar aplicativos WebView2 nas seguintes versões Windows.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-160">You may run WebView2 apps on the following versions of Windows.</span></span>  

*   <span data-ttu-id="9d9a2-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9d9a2-161">Windows 10</span></span>  
*   <span data-ttu-id="9d9a2-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9d9a2-162">Windows 8.1</span></span>  
*   <span data-ttu-id="9d9a2-163">Windows 7 \*\*</span><span class="sxs-lookup"><span data-stu-id="9d9a2-163">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="9d9a2-164">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="9d9a2-164">Windows Server 2019</span></span>  
*   <span data-ttu-id="9d9a2-165">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d9a2-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="9d9a2-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d9a2-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="9d9a2-167">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-167">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="9d9a2-168">Windows Server 2008 R2 \*\*</span><span class="sxs-lookup"><span data-stu-id="9d9a2-168">Windows Server 2008 R2 \*\*</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="9d9a2-169">\*\* O suporte a WebView2 para Windows 7 e Windows Server 2008 R2 tem o mesmo ciclo de suporte que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-169">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="9d9a2-170">Para obter mais informações, navegue [até Microsoft Edge sistemas operacionais com suporte.][DeployedgeMicrosoftEdgeSupportedOS]</span><span class="sxs-lookup"><span data-stu-id="9d9a2-170">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="9d9a2-171">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9d9a2-171">Next steps</span></span>  

<span data-ttu-id="9d9a2-172">Para obter mais informações sobre como criar e implantar aplicativos WebView2, revise a documentação conceitual e os guias de como usar.</span><span class="sxs-lookup"><span data-stu-id="9d9a2-172">For more information on how to build and deploy WebView2 apps, review the conceptual documentation and how-to guides.</span></span>  

### <a name="concepts"></a><span data-ttu-id="9d9a2-173">Conceitos</span><span class="sxs-lookup"><span data-stu-id="9d9a2-173">Concepts</span></span>  

*   [<span data-ttu-id="9d9a2-174">Compreender versões do SDK webView2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-174">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]  
*   [<span data-ttu-id="9d9a2-175">Distribuição de aplicativos usando WebView2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-175">Distribution of apps using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="9d9a2-176">Práticas recomendadas para o desenvolvimento de aplicativos WebView2 seguros</span><span class="sxs-lookup"><span data-stu-id="9d9a2-176">Best practices for developing secure WebView2 apps</span></span>][Webview2ConceptsSecurity]  
*   [<span data-ttu-id="9d9a2-177">Gerenciar Pasta de Dados do Usuário em aplicativos WebView2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-177">Manage User Data Folder in WebView2 apps</span></span>][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a><span data-ttu-id="9d9a2-178">How-To guias</span><span class="sxs-lookup"><span data-stu-id="9d9a2-178">How-To guides</span></span>  

*   [<span data-ttu-id="9d9a2-179">Como depurar com WebView2</span><span class="sxs-lookup"><span data-stu-id="9d9a2-179">How to Debug with WebView2</span></span>][Webview2HowToDebug]  
*   [<span data-ttu-id="9d9a2-180">Automatizando e testando o WebView2 com Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="9d9a2-180">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="9d9a2-181">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="9d9a2-181">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
