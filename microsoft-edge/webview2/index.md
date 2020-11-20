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
# <span data-ttu-id="11f2f-104">Introdução ao Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-104">Introduction to Microsoft Edge WebView2</span></span>  

<span data-ttu-id="11f2f-105">O controle WebView2 do Microsoft Edge permite que você incorpore tecnologias da Web \ (HTML, CSS e JavaScript \) em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="11f2f-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="11f2f-106">O controle WebView2 usa o [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="11f2f-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="11f2f-107">Com o WebView2, você pode inserir código da Web em diferentes partes do seu aplicativo nativo ou criar todo o aplicativo nativo em um único WebView.</span><span class="sxs-lookup"><span data-stu-id="11f2f-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="11f2f-108">Para obter informações sobre como começar a criar um aplicativo do WebView2, navegue até [introdução](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="11f2f-108">For information on how to start building a WebView2 application, navigate to [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="O que é o WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="11f2f-110">O que é o WebView</span><span class="sxs-lookup"><span data-stu-id="11f2f-110">What is WebView</span></span>  
:::image-end:::  

## <span data-ttu-id="11f2f-111">Abordagem do aplicativo híbrido</span><span class="sxs-lookup"><span data-stu-id="11f2f-111">Hybrid application approach</span></span>  

<span data-ttu-id="11f2f-112">Geralmente, os desenvolvedores precisam decidir entre a criação de um aplicativo Web ou um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="11f2f-112">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="11f2f-113">As dobradiças de decisão sobre a compensação entre o alcance e a potência.</span><span class="sxs-lookup"><span data-stu-id="11f2f-113">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="11f2f-114">Os aplicativos da Web permitem um amplo alcance.</span><span class="sxs-lookup"><span data-stu-id="11f2f-114">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="11f2f-115">Como um desenvolvedor da Web, você pode reutilizar a maioria, se não todo o seu código, em todas as plataformas diferentes.</span><span class="sxs-lookup"><span data-stu-id="11f2f-115">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="11f2f-116">No entanto, os aplicativos nativos utilizam os recursos de toda a plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="11f2f-116">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="11f2f-118">Web Native</span><span class="sxs-lookup"><span data-stu-id="11f2f-118">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="11f2f-119">Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.</span><span class="sxs-lookup"><span data-stu-id="11f2f-119">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="11f2f-120">Os desenvolvedores de aplicativos híbridos se beneficiam do Ubiquity e da força da plataforma da Web, e da capacidade e dos recursos completos da plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="11f2f-120">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="11f2f-121">Benefícios do WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-121">WebView2 benefits</span></span>  

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos da WebView" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="11f2f-123">Motivos da WebView</span><span class="sxs-lookup"><span data-stu-id="11f2f-123">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-124">Ecossistema da Web \ & conjunto de qualificações</span><span class="sxs-lookup"><span data-stu-id="11f2f-124">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="11f2f-125">Use toda a plataforma da Web, bibliotecas, ferramentas e talento existentes dentro do ecossistema da Web.</span><span class="sxs-lookup"><span data-stu-id="11f2f-125">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-126">Inovação rápida</span><span class="sxs-lookup"><span data-stu-id="11f2f-126">Rapid innovation</span></span>**  
      <span data-ttu-id="11f2f-127">O desenvolvimento na Web permite implantação e iteração mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="11f2f-127">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-128">Suporte do Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="11f2f-128">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="11f2f-129">Suporte para uma experiência de usuário consistente em todo o Windows 7, 8 e 10.</span><span class="sxs-lookup"><span data-stu-id="11f2f-129">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-130">Recursos nativos</span><span class="sxs-lookup"><span data-stu-id="11f2f-130">Native capabilities</span></span>**  
      <span data-ttu-id="11f2f-131">Acesse o conjunto completo de APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="11f2f-131">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-132">Compartilhamento de código</span><span class="sxs-lookup"><span data-stu-id="11f2f-132">Code-sharing</span></span>**  
      <span data-ttu-id="11f2f-133">Adicionar código da Web à sua codebase permite maior reutilização em várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="11f2f-133">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-134">Suporte da Microsoft</span><span class="sxs-lookup"><span data-stu-id="11f2f-134">Microsoft support</span></span>**  
      <span data-ttu-id="11f2f-135">A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado como GA.</span><span class="sxs-lookup"><span data-stu-id="11f2f-135">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-136">Distribuição para o meio-verde</span><span class="sxs-lookup"><span data-stu-id="11f2f-136">Evergreen distribution</span></span>**  
      <span data-ttu-id="11f2f-137">Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e correções de segurança.</span><span class="sxs-lookup"><span data-stu-id="11f2f-137">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="11f2f-138">**Corrigido** \ (em breve \)</span><span class="sxs-lookup"><span data-stu-id="11f2f-138">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="11f2f-139">Escolha para empacotar os bits Chromium em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11f2f-139">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="11f2f-140">Adoção incremental</span><span class="sxs-lookup"><span data-stu-id="11f2f-140">Incremental adoption</span></span>**  
      <span data-ttu-id="11f2f-141">Adicione componentes Web por parte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11f2f-141">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="11f2f-142">Introdução</span><span class="sxs-lookup"><span data-stu-id="11f2f-142">Getting started</span></span>  

<span data-ttu-id="11f2f-143">Para compilar e testar seu aplicativo usando o controle WebView2, você precisa ter o [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] e o [SDK do WebView2][NugetPackagesMicrosoftWebWebView2] instalado.</span><span class="sxs-lookup"><span data-stu-id="11f2f-143">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="11f2f-144">Selecione uma das seguintes opções para começar.</span><span class="sxs-lookup"><span data-stu-id="11f2f-144">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="11f2f-145">Introdução ao Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="11f2f-145">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="11f2f-146">Introdução ao WPF</span><span class="sxs-lookup"><span data-stu-id="11f2f-146">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="11f2f-147">Introdução ao WinForms</span><span class="sxs-lookup"><span data-stu-id="11f2f-147">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="11f2f-148">Introdução ao WinUI3</span><span class="sxs-lookup"><span data-stu-id="11f2f-148">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="11f2f-149">O repositório de [exemplos WebView2][GithubMicrosoftedgeWebview2samples] contém exemplos que demonstram todos os recursos do SDK do WebView2 e os padrões de uso da API.</span><span class="sxs-lookup"><span data-stu-id="11f2f-149">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="11f2f-150">Conforme mais recursos forem adicionados ao SDK do WebView2, os aplicativos de exemplo serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="11f2f-150">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="11f2f-151">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="11f2f-151">Supported platforms</span></span>  

<span data-ttu-id="11f2f-152">Uma disponibilidade geral \ (GA \) ou versão de visualização está disponível nos seguintes ambientes de programação:</span><span class="sxs-lookup"><span data-stu-id="11f2f-152">A General Availability \(GA\) or Preview version is available on the following programming environments.</span></span>  

*   <span data-ttu-id="11f2f-153">Win32 C/C++ \ (GA \)</span><span class="sxs-lookup"><span data-stu-id="11f2f-153">Win32 C/C++ \(GA\)</span></span>  
*   <span data-ttu-id="11f2f-154">.NET Framework 4.6.2 ou posterior \ (visualização \)</span><span class="sxs-lookup"><span data-stu-id="11f2f-154">.NET Framework 4.6.2 or later \(Preview\)</span></span>  
*   <span data-ttu-id="11f2f-155">.NET Core 3,0 ou posterior \ (visualização \)</span><span class="sxs-lookup"><span data-stu-id="11f2f-155">.NET Core 3.0 or later \(Preview\)</span></span>  
*   <span data-ttu-id="11f2f-156">[WinUI 3,0][UwpToolkitsWinui3] \ (visualização \)</span><span class="sxs-lookup"><span data-stu-id="11f2f-156">[WinUI 3.0][UwpToolkitsWinui3] \(Preview\)</span></span>  

<span data-ttu-id="11f2f-157">Você poderá executar aplicativos do WebView2 nas seguintes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="11f2f-157">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="11f2f-158">Windows 10</span><span class="sxs-lookup"><span data-stu-id="11f2f-158">Windows 10</span></span>  
*   <span data-ttu-id="11f2f-159">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="11f2f-159">Windows 8.1</span></span>  
*   <span data-ttu-id="11f2f-160">Windows 7 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="11f2f-160">Windows 7 \*\*</span></span>  
*   <span data-ttu-id="11f2f-161">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="11f2f-161">Windows Server 2019</span></span>  
*   <span data-ttu-id="11f2f-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="11f2f-162">Windows Server 2016</span></span>  
*   <span data-ttu-id="11f2f-163">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11f2f-163">Windows Server 2012</span></span>  
*   <span data-ttu-id="11f2f-164">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="11f2f-164">Windows Server 2012 R2</span></span>  
*   <span data-ttu-id="11f2f-165">Windows Server 2008 R2 \ \* \ \*</span><span class="sxs-lookup"><span data-stu-id="11f2f-165">Windows Server 2008 R2 \*\*</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="11f2f-166">\ \* \ \* O suporte do WebView2 para Windows 7 e Windows Server 2008 R2 tem o mesmo ciclo de suporte que o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="11f2f-166">\*\* WebView2 support for Windows 7 and Windows Server 2008 R2 has the same support cycle as Microsoft Edge.</span></span>  <span data-ttu-id="11f2f-167">Para obter mais informações, navegue até [sistemas operacionais compatíveis com o Microsoft Edge][DeployedgeMicrosoftEdgeSupportedOS].</span><span class="sxs-lookup"><span data-stu-id="11f2f-167">For more information, navigate to [Microsoft Edge supported Operating Systems][DeployedgeMicrosoftEdgeSupportedOS].</span></span>  

## <span data-ttu-id="11f2f-168">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="11f2f-168">Next steps</span></span>  

<span data-ttu-id="11f2f-169">Para obter mais informações sobre como criar e implantar aplicativos do WebView2, confira a documentação conceitual e os guias de instruções.</span><span class="sxs-lookup"><span data-stu-id="11f2f-169">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="11f2f-170">Conceitos</span><span class="sxs-lookup"><span data-stu-id="11f2f-170">Concepts</span></span>  

*   [<span data-ttu-id="11f2f-171">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-171">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="11f2f-172">Distribuição de aplicativos usando o WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-172">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="11f2f-173">Práticas recomendadas para o desenvolvimento de aplicativos seguros do WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-173">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="11f2f-174">Gerenciar a pasta dados do usuário em aplicativos do WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-174">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="11f2f-175">Guias de How-To</span><span class="sxs-lookup"><span data-stu-id="11f2f-175">How-To guides</span></span>  

*   [<span data-ttu-id="11f2f-176">Como depurar com WebView2</span><span class="sxs-lookup"><span data-stu-id="11f2f-176">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="11f2f-177">Automatizando e testando o WebView2 com o Microsoft Edge driver</span><span class="sxs-lookup"><span data-stu-id="11f2f-177">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="11f2f-178">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="11f2f-178">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
