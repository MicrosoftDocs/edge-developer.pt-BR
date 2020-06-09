---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Controle WebView2 do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, controle de navegador, HTML de borda, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: 1b140d9f644c7a864cac4966bb4cfdd400feeb0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697739"
---
# <span data-ttu-id="68f9e-104">Introdução ao Microsoft Edge WebView2 (visualização)</span><span class="sxs-lookup"><span data-stu-id="68f9e-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="68f9e-105">O controle WebView2 do Microsoft Edge permite que você incorpore tecnologias da Web \ (HTML, CSS e JavaScript \) em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="68f9e-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="68f9e-106">O controle WebView2 usa o [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com) como o mecanismo de renderização para exibir o conteúdo da Web em aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="68f9e-106">The WebView2 control uses [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com) as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="68f9e-107">Com o WebView2, você pode inserir código da Web em diferentes partes do seu aplicativo nativo ou criar todo o aplicativo nativo em um único WebView.</span><span class="sxs-lookup"><span data-stu-id="68f9e-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="68f9e-108">Para saber mais sobre como começar a criar um aplicativo do WebView2, consulte [introdução](./index.md#getting-started).</span><span class="sxs-lookup"><span data-stu-id="68f9e-108">For information on how to start building a WebView2 application, see [Get Started](./index.md#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="O que é o WebView":::
   <span data-ttu-id="68f9e-110">O que é o WebView</span><span class="sxs-lookup"><span data-stu-id="68f9e-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="68f9e-111">A visualização do WebView2 foi desenvolvida para o início do protótipo e para coletar comentários e para ajudar a moldar a API.</span><span class="sxs-lookup"><span data-stu-id="68f9e-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help to shape the API.</span></span>  <span data-ttu-id="68f9e-112">A equipe do Microsoft Edge WebView não recomenda que você use a visualização em seus aplicativos de produção, pois pode haver [alterações significativas](./releasenotes.md).</span><span class="sxs-lookup"><span data-stu-id="68f9e-112">The Microsoft Edge WebView team does not recommend that you use the preview in your production apps because there may be [breaking changes](./releasenotes.md).</span></span>  

## <span data-ttu-id="68f9e-113">Abordagem do aplicativo híbrido</span><span class="sxs-lookup"><span data-stu-id="68f9e-113">Hybrid application approach</span></span>  

<span data-ttu-id="68f9e-114">Geralmente, os desenvolvedores precisam escolher entre a criação de um aplicativo Web ou um aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="68f9e-114">Developers often have to choose between building a web application or a native application.</span></span>  <span data-ttu-id="68f9e-115">As dobradiças de decisão sobre a compensação entre o alcance e a potência.</span><span class="sxs-lookup"><span data-stu-id="68f9e-115">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="68f9e-116">Os aplicativos da Web permitem um amplo alcance.</span><span class="sxs-lookup"><span data-stu-id="68f9e-116">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="68f9e-117">Como um desenvolvedor da Web, você pode reutilizar a maioria, se não todo o seu código, em todas as plataformas diferentes.</span><span class="sxs-lookup"><span data-stu-id="68f9e-117">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="68f9e-118">No entanto, os aplicativos nativos utilizam os recursos de toda a plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="68f9e-118">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native":::
   <span data-ttu-id="68f9e-120">Web Native</span><span class="sxs-lookup"><span data-stu-id="68f9e-120">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="68f9e-121">Os aplicativos híbridos permitem que os desenvolvedores aproveitem o melhor dos dois mundos.</span><span class="sxs-lookup"><span data-stu-id="68f9e-121">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="68f9e-122">Os desenvolvedores de aplicativos híbridos se beneficiam do Ubiquity e da força da plataforma da Web, e da capacidade e dos recursos completos da plataforma nativa.</span><span class="sxs-lookup"><span data-stu-id="68f9e-122">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="68f9e-123">Benefícios do WebView2</span><span class="sxs-lookup"><span data-stu-id="68f9e-123">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos da WebView":::
   <span data-ttu-id="68f9e-125">Motivos da WebView</span><span class="sxs-lookup"><span data-stu-id="68f9e-125">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-126">Ecossistema da Web \ & conjunto de qualificações</span><span class="sxs-lookup"><span data-stu-id="68f9e-126">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="68f9e-127">Use toda a plataforma da Web, bibliotecas, ferramentas e talento existentes dentro do ecossistema da Web.</span><span class="sxs-lookup"><span data-stu-id="68f9e-127">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-128">Inovação rápida</span><span class="sxs-lookup"><span data-stu-id="68f9e-128">Rapid innovation</span></span>**  
      <span data-ttu-id="68f9e-129">O desenvolvimento na Web permite implantação e iteração mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="68f9e-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-130">Suporte do Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="68f9e-130">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="68f9e-131">Suporte para uma experiência de usuário consistente em todo o Windows 7, 8 e 10.</span><span class="sxs-lookup"><span data-stu-id="68f9e-131">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-132">Recursos nativos</span><span class="sxs-lookup"><span data-stu-id="68f9e-132">Native capabilities</span></span>**  
      <span data-ttu-id="68f9e-133">Acesse o conjunto completo de APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="68f9e-133">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-134">Compartilhamento de código</span><span class="sxs-lookup"><span data-stu-id="68f9e-134">Code-sharing</span></span>**  
      <span data-ttu-id="68f9e-135">Adicionar código da Web à sua codebase permite maior reutilização em várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="68f9e-135">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-136">Suporte da Microsoft</span><span class="sxs-lookup"><span data-stu-id="68f9e-136">Microsoft support</span></span>**  
      <span data-ttu-id="68f9e-137">A Microsoft oferece suporte e adiciona novas solicitações de recursos quando o WebView2 é lançado como GA.</span><span class="sxs-lookup"><span data-stu-id="68f9e-137">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-138">Distribuição para o meio-verde</span><span class="sxs-lookup"><span data-stu-id="68f9e-138">Evergreen distribution</span></span>**  
      <span data-ttu-id="68f9e-139">Conte com uma versão atualizada do Chromium com atualizações de plataforma regulares e correções de segurança.</span><span class="sxs-lookup"><span data-stu-id="68f9e-139">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="68f9e-140">**Corrigido** \ (em breve \)</span><span class="sxs-lookup"><span data-stu-id="68f9e-140">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="68f9e-141">Escolha para empacotar os bits Chromium em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68f9e-141">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="68f9e-142">Adoção incremental</span><span class="sxs-lookup"><span data-stu-id="68f9e-142">Incremental adoption</span></span>**  
      <span data-ttu-id="68f9e-143">Adicione componentes Web por parte do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68f9e-143">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="68f9e-144">Introdução</span><span class="sxs-lookup"><span data-stu-id="68f9e-144">Getting started</span></span>  

<span data-ttu-id="68f9e-145">Para compilar e testar seu aplicativo usando o controle WebView2, você precisa ter o [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download) e o [SDK do WebView2](https://aka.ms/webviewnuget) instalado.</span><span class="sxs-lookup"><span data-stu-id="68f9e-145">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download) and the [WebView2 SDK](https://aka.ms/webviewnuget) installed.</span></span>  <span data-ttu-id="68f9e-146">Selecione uma das seguintes opções para começar.</span><span class="sxs-lookup"><span data-stu-id="68f9e-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="68f9e-147">Introdução ao Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="68f9e-147">Getting Started with Win32 C/C++</span></span>](./gettingstarted/win32.md)  
*   [<span data-ttu-id="68f9e-148">Introdução ao WPF</span><span class="sxs-lookup"><span data-stu-id="68f9e-148">Getting Started with WPF</span></span>](./gettingstarted/wpf.md)  
*   [<span data-ttu-id="68f9e-149">Introdução ao WinForms</span><span class="sxs-lookup"><span data-stu-id="68f9e-149">Getting Started with WinForms</span></span>](./gettingstarted/winforms.md)  

<span data-ttu-id="68f9e-150">O repositório de [exemplos WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contém exemplos que demonstram todos os recursos de SDKs do WebView2 e padrões de uso de APIs.</span><span class="sxs-lookup"><span data-stu-id="68f9e-150">The [WebView2 Samples](https://github.com/MicrosoftEdge/WebView2Samples) repository contains samples that demonstrate all of the WebView2 SDKs features and API usage patterns.</span></span> <span data-ttu-id="68f9e-151">Conforme mais recursos forem adicionados ao SDK do WebView2, os aplicativos de exemplo serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="68f9e-151">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>   

## <span data-ttu-id="68f9e-152">Plataformas compatíveis</span><span class="sxs-lookup"><span data-stu-id="68f9e-152">Supported platforms</span></span>  

<span data-ttu-id="68f9e-153">Uma visualização do desenvolvedor está disponível nos seguintes ambientes de programação:</span><span class="sxs-lookup"><span data-stu-id="68f9e-153">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="68f9e-154">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="68f9e-154">Win32 C/C++</span></span>  
*   <span data-ttu-id="68f9e-155">.NET Framework 4.6.2 ou posterior</span><span class="sxs-lookup"><span data-stu-id="68f9e-155">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="68f9e-156">.NET Core 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="68f9e-156">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="68f9e-157">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="68f9e-157">WinUI 3.0</span></span>](/uwp/toolkits/winui3/)  

<span data-ttu-id="68f9e-158">Você poderá executar aplicativos do WebView2 nas seguintes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="68f9e-158">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="68f9e-159">Windows 10</span><span class="sxs-lookup"><span data-stu-id="68f9e-159">Windows 10</span></span>  
*   <span data-ttu-id="68f9e-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="68f9e-160">Windows 8.1</span></span>  
*   <span data-ttu-id="68f9e-161">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68f9e-161">Windows 8</span></span>  
*   <span data-ttu-id="68f9e-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68f9e-162">Windows 7</span></span>  
*   <span data-ttu-id="68f9e-163">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="68f9e-163">Windows Server 2016</span></span>  
*   <span data-ttu-id="68f9e-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68f9e-164">Windows Server 2012</span></span>  
*   <span data-ttu-id="68f9e-165">2012R2 do Windows Server</span><span class="sxs-lookup"><span data-stu-id="68f9e-165">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="68f9e-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68f9e-166">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="68f9e-167">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="68f9e-167">Next steps</span></span>  

<span data-ttu-id="68f9e-168">Para obter informações mais detalhadas sobre como criar e implantar aplicativos do WebView2, faça checkout dos guias de instruções e documentação conceitual.</span><span class="sxs-lookup"><span data-stu-id="68f9e-168">For more detailed information on how to build and deploy WebView2 applications, checkout the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="68f9e-169">Conceitos</span><span class="sxs-lookup"><span data-stu-id="68f9e-169">Concepts</span></span>  

*   [<span data-ttu-id="68f9e-170">WebView2 SDK e controle de versão do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="68f9e-170">WebView2 SDK and Microsoft Edge versioning</span></span>](./concepts/versioning.md)
*   [<span data-ttu-id="68f9e-171">Distribuir aplicativos do WebView2</span><span class="sxs-lookup"><span data-stu-id="68f9e-171">Distributing WebView2 applications</span></span>](./concepts/distribution.md)  
 
#### <span data-ttu-id="68f9e-172">Guias de instruções</span><span class="sxs-lookup"><span data-stu-id="68f9e-172">How-To guides</span></span>  

*   [<span data-ttu-id="68f9e-173">Depuração de WebView2 com o DevTools e depuração de script do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="68f9e-173">Debugging WebView2 with DevTools and Visual Studio script debugging</span></span>](./howto/debug.md)  
*   [<span data-ttu-id="68f9e-174">Automatizando e Depurando o WebView2 com o Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="68f9e-174">Automating and debugging WebView2 with Microsoft EdgeDriver</span></span>](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## <span data-ttu-id="68f9e-175">Entrar em contato com a equipe do WebView2</span><span class="sxs-lookup"><span data-stu-id="68f9e-175">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="68f9e-176">Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.</span><span class="sxs-lookup"><span data-stu-id="68f9e-176">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="68f9e-177">Acesse o [repositório de comentários](https://aka.ms/webviewfeedback) da WebView para enviar solicitações de recursos ou relatórios de erros.</span><span class="sxs-lookup"><span data-stu-id="68f9e-177">Visit the WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  <span data-ttu-id="68f9e-178">Também é um bom lugar para procurar problemas conhecidos.</span><span class="sxs-lookup"><span data-stu-id="68f9e-178">It is also a good place to search for known issues.</span></span>  

> [!NOTE]
> <span data-ttu-id="68f9e-179">Durante a visualização do desenvolvedor, a equipe do Microsoft Edge WebView também coleta dados para ajudar a criar um WebView melhor.</span><span class="sxs-lookup"><span data-stu-id="68f9e-179">During developer preview, the Microsoft Edge WebView team also collects data to help build a better WebView.</span></span>  <span data-ttu-id="68f9e-180">Os usuários podem desativar a coleta de dados do WebView ao navegar `edge://settings/privacy` no navegador Microsoft Edge e desativar a coleta de dados do navegador.</span><span class="sxs-lookup"><span data-stu-id="68f9e-180">Users may turn off WebView data collection by navigating to `edge://settings/privacy` in the Microsoft Edge browser and turning off browser data collection.</span></span>  
