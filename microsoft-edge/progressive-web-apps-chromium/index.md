---
description: Os aplicativos Web progressivos (Chromium) são executados nativamente no Windows 10.  Aqui está tudo o que você precisa saber como desenvolvedor da Web.
title: Aplicativos Web progressivos no Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: a9fa08a9c84ee5da8eab3c9c3edeea34439b6557
ms.sourcegitcommit: be76feed0d616a96c77ea2748a9f0d6c0c06284b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/07/2020
ms.locfileid: "11103929"
---
# <span data-ttu-id="73bf0-105">Aplicativos Web progressivos no Windows</span><span class="sxs-lookup"><span data-stu-id="73bf0-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="73bf0-106">[Aplicativos Web progressivos][MDNApps] \ (PWAs \) fornecem acesso a tecnologias da Web abertas para interoperabilidade entre plataformas e oferecer aos usuários uma experiência nativa e semelhante a um aplicativo personalizada para seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="73bf0-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="73bf0-107">PWAs são sites [aprimorados progressivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.</span><span class="sxs-lookup"><span data-stu-id="73bf0-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="73bf0-108">As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.</span><span class="sxs-lookup"><span data-stu-id="73bf0-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [<span data-ttu-id="73bf0-109">Detectáveis</span><span class="sxs-lookup"><span data-stu-id="73bf0-109">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="73bf0-110">Nos resultados da pesquisa na Web e nos repositórios de aplicativos de suporte</span><span class="sxs-lookup"><span data-stu-id="73bf0-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [<span data-ttu-id="73bf0-111">Instaláveis</span><span class="sxs-lookup"><span data-stu-id="73bf0-111">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="73bf0-112">Fixar e iniciar na tela inicial, no menu Iniciar, na barra de tarefas e assim por diante</span><span class="sxs-lookup"><span data-stu-id="73bf0-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [<span data-ttu-id="73bf0-113">Recontratar</span><span class="sxs-lookup"><span data-stu-id="73bf0-113">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="73bf0-114">Enviar notificações por push, mesmo quando o aplicativo não estiver ativo</span><span class="sxs-lookup"><span data-stu-id="73bf0-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [<span data-ttu-id="73bf0-115">Independente de rede</span><span class="sxs-lookup"><span data-stu-id="73bf0-115">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="73bf0-116">O Works offline e em condições de rede baixa</span><span class="sxs-lookup"><span data-stu-id="73bf0-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [<span data-ttu-id="73bf0-117">Progressivas</span><span class="sxs-lookup"><span data-stu-id="73bf0-117">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="73bf0-118">A experiência pode ser dimensionada para cima (ou para baixo) com recursos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="73bf0-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [<span data-ttu-id="73bf0-119">Desligar</span><span class="sxs-lookup"><span data-stu-id="73bf0-119">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="73bf0-120">Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário</span><span class="sxs-lookup"><span data-stu-id="73bf0-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [<span data-ttu-id="73bf0-121">Responsivo</span><span class="sxs-lookup"><span data-stu-id="73bf0-121">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="73bf0-122">Adapta-se ao tamanho da tela ou orientação e método de entrada do usuário</span><span class="sxs-lookup"><span data-stu-id="73bf0-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [<span data-ttu-id="73bf0-123">Vinculável</span><span class="sxs-lookup"><span data-stu-id="73bf0-123">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="73bf0-124">Compartilhar e iniciar a partir de um hiperlink padrão</span><span class="sxs-lookup"><span data-stu-id="73bf0-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="73bf0-125">Construa \ (ou converta \) seu site existente em um PWA para aprimorar seu envolvimento com os usuários.</span><span class="sxs-lookup"><span data-stu-id="73bf0-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="73bf0-126">Melhorias incluem notificações por push, integração do tipo de aplicativo e suporte offline.</span><span class="sxs-lookup"><span data-stu-id="73bf0-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="73bf0-127">Continue a criar seu público-alvo na Web em aberto para que os usuários descubram o PWA por meio de pesquisa e compartilhamento de links.</span><span class="sxs-lookup"><span data-stu-id="73bf0-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="73bf0-128">O melhor de tudo é que seu aplicativo é atualizado para usar seu código de servidor Web.</span><span class="sxs-lookup"><span data-stu-id="73bf0-128">Best of all, your app is updated in using your web server code.</span></span>  

## <span data-ttu-id="73bf0-129">PWAs no Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="73bf0-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="73bf0-130">Quando você cria um aplicativo Web progressivo direcionado a APIs da Web Standard, seu aplicativo pode ser implantado entre plataformas e dispositivos e aproveitando as funcionalidades específicas do dispositivo, conforme disponível.</span><span class="sxs-lookup"><span data-stu-id="73bf0-130">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="73bf0-131">PWAs no Microsoft Edge \ (Chromium \) adicione as seguintes vantagens ao seu site.</span><span class="sxs-lookup"><span data-stu-id="73bf0-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="73bf0-132">Seu aplicativo é baseado em uma plataforma da Web baseada em padrões.</span><span class="sxs-lookup"><span data-stu-id="73bf0-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="73bf0-133">Permite que os usuários instalem o aplicativo diretamente do navegador.</span><span class="sxs-lookup"><span data-stu-id="73bf0-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="73bf0-134">Permite que os usuários instalem seu aplicativo sem uma implantação ou registro baseado na loja.</span><span class="sxs-lookup"><span data-stu-id="73bf0-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="73bf0-135">Os PWAs da área de trabalho são compatíveis com qualquer uma das plataformas que o Microsoft Edge \ (Chromium \) está disponível.</span><span class="sxs-lookup"><span data-stu-id="73bf0-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="73bf0-136">O Microsoft Edge \ (Chromium \) está disponível no Windows 7, no Windows 10 e no macOS.</span><span class="sxs-lookup"><span data-stu-id="73bf0-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="73bf0-137">Os benefícios a seguir estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="73bf0-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="73bf0-138">Os aplicativos podem ser instalados diretamente no navegador usando o ícone de **instalação** na barra de navegação.</span><span class="sxs-lookup"><span data-stu-id="73bf0-138">Applications may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Instalar submenu e ícone do aplicativo" lightbox="./media/install_pwa_icon.png":::
       <span data-ttu-id="73bf0-140">Instalar submenu e ícone do aplicativo</span><span class="sxs-lookup"><span data-stu-id="73bf0-140">Install application flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="73bf0-141">Os aplicativos também podem ser instalados, executados e gerenciados no menu **configurações**de  >  **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="73bf0-141">Applications may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Instalar submenu e ícone do aplicativo" lightbox="./media/app_menus.png":::
       <span data-ttu-id="73bf0-143">Itens de menu do aplicativo em configurações</span><span class="sxs-lookup"><span data-stu-id="73bf0-143">Application menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="73bf0-144">As notificações da Web são integradas ao sistema de notificação do Windows</span><span class="sxs-lookup"><span data-stu-id="73bf0-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="73bf0-145">Repositório de cookies compartilhados com o perfil do navegador que instalou o aplicativo</span><span class="sxs-lookup"><span data-stu-id="73bf0-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="73bf0-146">Acesso a outros recursos do navegador usando o menu de **configuração e mais** \ ( `...` \), incluindo validação de certificado, permissões de site, proteção de rastreamento e extensões de navegador</span><span class="sxs-lookup"><span data-stu-id="73bf0-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="73bf0-147">Acesso total ao [Microsoft Edge devtools][DevtoolsProgressiveWebApps] para depurar seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="73bf0-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="73bf0-148">Para personalizar o PWAs especificamente para o Windows 10 que faz solicitações de API do WinRT usando JavaScript, navegue até [a documentação específica para os recursos do PWA do EdgeHTML][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="73bf0-148">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, navigate to [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="73bf0-149">Saiba mais sobre como testar o PWA no Windows 10 e distribuí-lo na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="73bf0-149">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="73bf0-150">Para obter mais informações sobre benefícios do PWA, recursos futuros e demonstrações curtas, navegue até [Build 2020 PWA Session][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="73bf0-150">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <span data-ttu-id="73bf0-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73bf0-151">Requirements</span></span>  

<span data-ttu-id="73bf0-152">Para ser executado como um PWA, seu aplicativo Web hospedado no servidor deve incluir os requisitos mínimos a seguir.</span><span class="sxs-lookup"><span data-stu-id="73bf0-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-153">HTTPS</span><span class="sxs-lookup"><span data-stu-id="73bf0-153">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-154">Protege seus usuários fornecendo uma conexão segura para comunicação do servidor ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73bf0-154">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="73bf0-155">Os funcionários do serviço e outras tecnologias do PWA só funcionam com recursos da Web servidos por meio de uma conexão segura \ (ou de `localhost` para fins de depuração \).</span><span class="sxs-lookup"><span data-stu-id="73bf0-155">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-156">Profissionais de Serviço</span><span class="sxs-lookup"><span data-stu-id="73bf0-156">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-157">Usa threads de trabalho de serviço para atuar como proxies de rede entre o aplicativo cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="73bf0-157">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="73bf0-158">Threads de trabalho do serviço fornecem suporte offline, cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de desempenho de carregamento de página.</span><span class="sxs-lookup"><span data-stu-id="73bf0-158">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-159">Manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="73bf0-159">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-160">Fornece um arquivo de metadados baseado em JSON que descreve as principais informações sobre o seu aplicativo Web, para que o Windows 10 e outras plataformas de host forneçam aos seus usuários do PWA uma experiência que permite a instalação e a aparência do aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="73bf0-160">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="73bf0-161">As informações de chave incluem ícones, idioma e ponto de entrada de URL.</span><span class="sxs-lookup"><span data-stu-id="73bf0-161">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="73bf0-162">Para ser um grande PWA, seu aplicativo também deve atender aos seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="73bf0-162">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-163">Compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="73bf0-163">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-164">Certifique-se de que o PWA funcione [testando][MicrosoftDeveloperEdgeToolsRemote] em diferentes navegadores e ambientes.</span><span class="sxs-lookup"><span data-stu-id="73bf0-164">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-165">Design dinâmico</span><span class="sxs-lookup"><span data-stu-id="73bf0-165">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-166">Emprega layouts fluidos e imagens flexíveis.</span><span class="sxs-lookup"><span data-stu-id="73bf0-166">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="73bf0-167">O design responsivo inclui os seguintes elementos que adaptam a sua experiência ao dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="73bf0-167">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="73bf0-168">[Grade][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="73bf0-168">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="73bf0-169">flexbox</span><span class="sxs-lookup"><span data-stu-id="73bf0-169">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="73bf0-170">[Grade][MDNCssGridLayout] e [flexbox][MDNCssFlexibleBoxLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="73bf0-170">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="73bf0-171">consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="73bf0-171">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="73bf0-172">imagens responsivas</span><span class="sxs-lookup"><span data-stu-id="73bf0-172">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="73bf0-173">Usa [ferramentas de emulação de dispositivo][DevToolsGuide|::ref1::|] do seu navegador para testar localmente ou criar uma [sessão de depuração remota][DevToolsProtocolClientsEdgeDevToolsPreview] para testar diretamente um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="73bf0-173">Uses [device emulation tools][DevToolsGuide|::ref1::|] from your browser to locally test, or create a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-174">Vinculação profunda</span><span class="sxs-lookup"><span data-stu-id="73bf0-174">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-175">Roteia cada página do seu site para uma URL exclusiva, para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.</span><span class="sxs-lookup"><span data-stu-id="73bf0-175">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-176">Práticas de validação e teste</span><span class="sxs-lookup"><span data-stu-id="73bf0-176">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-177">Usa ferramentas de qualidade de código como o [webhint][Webhint] subbotão para otimizar a eficiência, a robustez, a segurança e a acessibilidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73bf0-177">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="73bf0-178">Lista de verificação do Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="73bf0-178">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="73bf0-179">Verifica o PWA em relação à lista de verificação do PWA da linha de base do Google.</span><span class="sxs-lookup"><span data-stu-id="73bf0-179">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="73bf0-180">Para transformar o PWA em um aplicativo da [Microsoft Store][MicrosoftDeveloperStore] , navegue até [Web Apps progressivos (EdgeHTML) na Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="73bf0-180">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <span data-ttu-id="73bf0-181">Consulte também</span><span class="sxs-lookup"><span data-stu-id="73bf0-181">See also</span></span>  

*   [<span data-ttu-id="73bf0-182">Myth de PWAs</span><span class="sxs-lookup"><span data-stu-id="73bf0-182">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="73bf0-183">Um roteiro progressivo para seu aplicativo Web progressivo</span><span class="sxs-lookup"><span data-stu-id="73bf0-183">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="73bf0-184">Postagens offline com Web Apps progressivos</span><span class="sxs-lookup"><span data-stu-id="73bf0-184">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="73bf0-185">&DO PWA P A</span><span class="sxs-lookup"><span data-stu-id="73bf0-185">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="73bf0-186">Aposta na Web</span><span class="sxs-lookup"><span data-stu-id="73bf0-186">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="73bf0-187">Nomeando aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="73bf0-187">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="73bf0-188">Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 1)</span><span class="sxs-lookup"><span data-stu-id="73bf0-188">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="73bf0-189">Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 2)</span><span class="sxs-lookup"><span data-stu-id="73bf0-189">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="73bf0-190">Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 3)</span><span class="sxs-lookup"><span data-stu-id="73bf0-190">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Visualização do Microsoft Edge DevTools - Clientes do Protocolo DevTools"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Emulação"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps.md "Depurar aplicativos Web progressivos"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "O que há de novo no EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "O que há de novo no EdgeHTML 14"  
[PwaEdgehtmlIndex]: ../progressive-web-apps-edgehtml/index.md "Aplicativos Web progressivos (EdgeHTML) no Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Aplicativos Web progressivos na Microsoft Store"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Visão geral dos serviços de notificação por push do Windows \ (WNS \)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Projetando para Xbox e TV"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considerações de interface do usuário para dispositivos UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "O que é um aplicativo da plataforma universal do Windows (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Suporte ao seu aplicativo com tarefas em segundo plano"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publicar aplicativos e jogos do Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Abrindo uma conta de desenvolvedor"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Boas-vindas de aplicativos Web progressivos para Microsoft Edge e Windows 10-Blogs do Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de sincronização em segundo plano-status da plataforma Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifesto de aplicativo Web-status da plataforma Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Teste instantâneo"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Realidade mista para desenvolvedores"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar novo navegador Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Ativar ou desativar o assistente de foco no Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Alterar as configurações de notificação no Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "&DO PWA P A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Compreendendo o aperfeiçoamento progressivo-uma lista separada"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "aplicativos | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Teste entre navegadores | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Layout de caixa flexível CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Layout de grade CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar API | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Consultas de mídia | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificações | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Vantagens do aplicativo Web progressivo"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Instalável – vantagens do aplicativo Web progressivos"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Linkable – vantagens do aplicativo Web progressivo"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Vantagens de aplicativos Web progressivos independentes de rede"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Vantagens do aplicativo Web progressivo progressivo"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Recontratar-vantagens do aplicativo Web progressivo"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Respostas-vantagens do aplicativo Web progressivos"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Vantagens do aplicativo Web progressivo seguro"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imagens responsivas | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do aplicativo Web | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Vídeo do PWA"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Um roteiro progressivo para seu aplicativo Web progressivo"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Myth de PWAs – o novo Edge Edition"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Nomeando aplicativos Web progressivos"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Aposta na Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Postagens offline com Web Apps progressivos"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "O que faz um bom aplicativo Web progressivo? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculação profunda-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Design da Web responsivo-Wikipédia"  
