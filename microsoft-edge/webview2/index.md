---
description: Hospedar conteúdo da Web em seus aplicativos do Win32, .NET e UWP com o controle WebView2 do Microsoft Edge
title: Controle WebView2 do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, HTML de borda, Windows Forms, WinForms, WPF, .NET, WinUI, reunião do projeto
ms.openlocfilehash: d3294ce72237a323113ed9f7c8f31e37af43f5e6
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013741"
---
# <span data-ttu-id="9a8bc-104">Introdução ao Microsoft Edge WebView2 (visualização)</span><span class="sxs-lookup"><span data-stu-id="9a8bc-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="9a8bc-105">O controle WebView2 do Microsoft Edge permite que você incorpore tecnologias da Web \ (HTML, CSS e JavaScript \) em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="9a8bc-106">O controle WebView2 usa o [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="9a8bc-107">Com o WebView2, você pode inserir código da Web em diferentes partes do seu aplicativo nativo ou criar todo o aplicativo nativo em um único WebView.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="9a8bc-108">Para saber mais sobre como começar a criar um aplicativo do WebView2, consulte [introdução](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="9a8bc-108">For information on how to start building a WebView2 application, see [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="O que é o WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="9a8bc-110">O que é o WebView</span><span class="sxs-lookup"><span data-stu-id="9a8bc-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9a8bc-111">A visualização do WebView2 foi desenvolvida para o início do protótipo e para coletar comentários para ajudar a moldar a API.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help shape the API.</span></span>  <span data-ttu-id="9a8bc-112">Você não deve usar a visualização em seus aplicativos de produção porque pode haver alterações significativas.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-112">You should not use the preview in your production apps because there may be breaking changes.</span></span>  <span data-ttu-id="9a8bc-113">Para obter mais informações, consulte [Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="9a8bc-113">For more information, see [Webview2Releasenotes].</span></span>  

## <span data-ttu-id="9a8bc-114">Abordagem do aplicativo híbrido</span><span class="sxs-lookup"><span data-stu-id="9a8bc-114">Hybrid application approach</span></span>  

<span data-ttu-id="9a8bc-115">Geralmente, os desenvolvedores precisam decidir entre a criação de um aplicativo Web ou um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-115">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="9a8bc-116">As dobradiças de decisão sobre a compensação entre o alcance e a potência.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-116">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="9a8bc-117">Os aplicativos da Web permitem um amplo alcance.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-117">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="9a8bc-118">Como um desenvolvedor da Web, você pode reutilizar a maioria, se não todo o seu código, em todas as plataformas diferentes.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-118">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="9a8bc-119">No entanto, os aplicativos nativos utilizam os recursos de toda a plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-119">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="9a8bc-121">Web Native</span><span class="sxs-lookup"><span data-stu-id="9a8bc-121">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="9a8bc-122">Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-122">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="9a8bc-123">Os desenvolvedores de aplicativos híbridos se beneficiam do Ubiquity e da força da plataforma da Web, e da capacidade e dos recursos completos da plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-123">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="9a8bc-124">Benefícios do WebView2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-124">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos da WebView" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="9a8bc-126">Motivos da WebView</span><span class="sxs-lookup"><span data-stu-id="9a8bc-126">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-127">Ecossistema da Web \ & conjunto de qualificações</span><span class="sxs-lookup"><span data-stu-id="9a8bc-127">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="9a8bc-128">Use toda a plataforma da Web, bibliotecas, ferramentas e talento existentes dentro do ecossistema da Web.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-129">Inovação rápida</span><span class="sxs-lookup"><span data-stu-id="9a8bc-129">Rapid innovation</span></span>**  
      <span data-ttu-id="9a8bc-130">O desenvolvimento na Web permite implantação e iteração mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-130">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-131">Suporte do Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="9a8bc-131">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="9a8bc-132">Suporte para uma experiência de usuário consistente em todo o Windows 7, 8 e 10.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-132">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-133">Recursos nativos</span><span class="sxs-lookup"><span data-stu-id="9a8bc-133">Native capabilities</span></span>**  
      <span data-ttu-id="9a8bc-134">Acesse o conjunto completo de APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-135">Compartilhamento de código</span><span class="sxs-lookup"><span data-stu-id="9a8bc-135">Code-sharing</span></span>**  
      <span data-ttu-id="9a8bc-136">Adicionar código da Web à sua codebase permite maior reutilização em várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-136">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-137">Suporte da Microsoft</span><span class="sxs-lookup"><span data-stu-id="9a8bc-137">Microsoft support</span></span>**  
      <span data-ttu-id="9a8bc-138">A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado como GA.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-138">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-139">Distribuição para o meio-verde</span><span class="sxs-lookup"><span data-stu-id="9a8bc-139">Evergreen distribution</span></span>**  
      <span data-ttu-id="9a8bc-140">Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e correções de segurança.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="9a8bc-141">**Corrigido** \ (em breve \)</span><span class="sxs-lookup"><span data-stu-id="9a8bc-141">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="9a8bc-142">Escolha para empacotar os bits Chromium em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-142">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="9a8bc-143">Adoção incremental</span><span class="sxs-lookup"><span data-stu-id="9a8bc-143">Incremental adoption</span></span>**  
      <span data-ttu-id="9a8bc-144">Adicione componentes Web por parte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-144">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="9a8bc-145">Introdução</span><span class="sxs-lookup"><span data-stu-id="9a8bc-145">Getting started</span></span>  

<span data-ttu-id="9a8bc-146">Para compilar e testar seu aplicativo usando o controle WebView2, você precisa ter o [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] e o [SDK do WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-146">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="9a8bc-147">Selecione uma das seguintes opções para começar.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-147">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="9a8bc-148">Introdução ao Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="9a8bc-148">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="9a8bc-149">Introdução ao WPF</span><span class="sxs-lookup"><span data-stu-id="9a8bc-149">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="9a8bc-150">Introdução ao WinForms</span><span class="sxs-lookup"><span data-stu-id="9a8bc-150">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="9a8bc-151">Introdução ao WinUI3</span><span class="sxs-lookup"><span data-stu-id="9a8bc-151">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="9a8bc-152">O repositório de [exemplos WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK do WebView2 e os padrões de uso da API.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-152">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="9a8bc-153">Conforme mais recursos forem adicionados ao SDK do WebView2, os aplicativos de exemplo serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-153">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="9a8bc-154">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="9a8bc-154">Supported platforms</span></span>  

<span data-ttu-id="9a8bc-155">Uma visualização do desenvolvedor está disponível nos seguintes ambientes de programação:</span><span class="sxs-lookup"><span data-stu-id="9a8bc-155">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="9a8bc-156">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="9a8bc-156">Win32 C/C++</span></span>  
*   <span data-ttu-id="9a8bc-157">.NET Framework 4.6.2 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9a8bc-157">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="9a8bc-158">.NET Core 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9a8bc-158">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="9a8bc-159">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="9a8bc-159">WinUI 3.0</span></span>][UwpToolkitsWinui3]  

<span data-ttu-id="9a8bc-160">Você poderá executar aplicativos do WebView2 nas seguintes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-160">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="9a8bc-161">Windows 10</span><span class="sxs-lookup"><span data-stu-id="9a8bc-161">Windows 10</span></span>  
*   <span data-ttu-id="9a8bc-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9a8bc-162">Windows 8.1</span></span>  
*   <span data-ttu-id="9a8bc-163">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9a8bc-163">Windows 8</span></span>  
*   <span data-ttu-id="9a8bc-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a8bc-164">Windows 7</span></span>  
*   <span data-ttu-id="9a8bc-165">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="9a8bc-165">Windows Server 2019</span></span>  
*   <span data-ttu-id="9a8bc-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9a8bc-166">Windows Server 2016</span></span>  
*   <span data-ttu-id="9a8bc-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9a8bc-167">Windows Server 2012</span></span>  
*   <span data-ttu-id="9a8bc-168">2012R2 do Windows Server</span><span class="sxs-lookup"><span data-stu-id="9a8bc-168">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="9a8bc-169">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-169">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="9a8bc-170">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9a8bc-170">Next steps</span></span>  

<span data-ttu-id="9a8bc-171">Para obter mais informações sobre como criar e implantar aplicativos do WebView2, confira a documentação conceitual e os guias de instruções.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-171">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="9a8bc-172">Conceitos</span><span class="sxs-lookup"><span data-stu-id="9a8bc-172">Concepts</span></span>  

*   [<span data-ttu-id="9a8bc-173">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-173">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="9a8bc-174">Distribuição de aplicativos usando o WebView2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-174">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="9a8bc-175">Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-175">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="9a8bc-176">Gerenciar a pasta dados do usuário em aplicativos do WebView2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-176">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="9a8bc-177">Guias de instruções</span><span class="sxs-lookup"><span data-stu-id="9a8bc-177">How-To guides</span></span>  

*   [<span data-ttu-id="9a8bc-178">Como depurar com WebView2</span><span class="sxs-lookup"><span data-stu-id="9a8bc-178">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="9a8bc-179">Automatizando e testando o WebView2 com o Microsoft Edge driver</span><span class="sxs-lookup"><span data-stu-id="9a8bc-179">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="9a8bc-180">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="9a8bc-180">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

> [!NOTE]
> <span data-ttu-id="9a8bc-181">Durante a visualização, os dados coletados ajudam a criar um produto melhor.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-181">During the preview, the collected data helps build a better product.</span></span>  <span data-ttu-id="9a8bc-182">Para desativar a coleta de dados WebView2, acesse `edge://settings/privacy` e desative a coleta de dados do navegador.</span><span class="sxs-lookup"><span data-stu-id="9a8bc-182">To turn off WebView2 data collection, go to `edge://settings/privacy` and turn off browser data collection.</span></span>  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2 | Documentos da Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Gerenciando a pasta dados do usuário | Documentos da Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Compreenda as versões do SDK do WebView2 | Documentos da Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Introdução ao WebView2 (visualização do desenvolvedor) | Documentos da Microsoft"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introdução ao WebView2 em aplicativos do Windows Forms (visualização) | Documentos da Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Introdução ao WebView2 no WinUI3 (visualização) | Documentos da Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introdução ao WebView2 no WPF (visualização) | Documentos da Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Como depurar com WebView2 | Documentos da Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizando e testando o WebView2 com o Microsoft Edge driver | Documentos da Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de versão do WEBVIEW2RELEASENOTES para WebView2 SDK | Documentos da Microsoft"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Windows UI library 3 Preview 2 (julho de 2020) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galeria do NuGet"  
