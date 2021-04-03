---
description: Os Aplicativos Web Progressivos (Chromium) são executados de forma nativa no Windows 10.  Aqui está tudo o que você precisa saber como desenvolvedor da Web.
title: Aplicativos Web Progressivos no Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Borda, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 2850c983c1dae34362a43be9cd33abbfd0df77cf
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474884"
---
# <a name="progressive-web-apps-on-windows-overview"></a><span data-ttu-id="9550b-105">Visão geral progressiva dos Aplicativos Web no Windows</span><span class="sxs-lookup"><span data-stu-id="9550b-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="9550b-106">[Os Aplicativos Web][MDNApps] Progressivos \(PWAs\) fornecem acesso a tecnologias da Web abertas para interoperabilidade entre plataformas e fornecem aos usuários uma experiência nativa, como o aplicativo, personalizada para seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9550b-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="9550b-107">PWAs são sites que são [progressivamente aprimorados][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.</span><span class="sxs-lookup"><span data-stu-id="9550b-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="9550b-108">As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.</span><span class="sxs-lookup"><span data-stu-id="9550b-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a><span data-ttu-id="9550b-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span><span class="sxs-lookup"><span data-stu-id="9550b-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span></span>
        <span data-ttu-id="9550b-110">Dos resultados da pesquisa da Web e dos armazenamentos de aplicativos de suporte</span><span class="sxs-lookup"><span data-stu-id="9550b-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::
        ### <a name="installablemdnpwaadvantagesinstallable"></a><span data-ttu-id="9550b-111">[Installable][MDNPwaAdvantagesInstallable]</span><span class="sxs-lookup"><span data-stu-id="9550b-111">[Installable][MDNPwaAdvantagesInstallable]</span></span>
        <span data-ttu-id="9550b-112">Fixar e iniciar na tela inicial, Menu Iniciar, Barra de Tarefas e assim por diante</span><span class="sxs-lookup"><span data-stu-id="9550b-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a><span data-ttu-id="9550b-113">[Reajagável][MDNPwaAdvantagesReEngageable]</span><span class="sxs-lookup"><span data-stu-id="9550b-113">[Re-engageable][MDNPwaAdvantagesReEngageable]</span></span>
        <span data-ttu-id="9550b-114">Enviar notificações por push, mesmo quando o aplicativo não estiver ativo</span><span class="sxs-lookup"><span data-stu-id="9550b-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a><span data-ttu-id="9550b-115">[Network Independent][MDNPwaAdvantagesNetworkIndependent]</span><span class="sxs-lookup"><span data-stu-id="9550b-115">[Network Independent][MDNPwaAdvantagesNetworkIndependent]</span></span>
        <span data-ttu-id="9550b-116">Funciona offline e em condições de baixa rede</span><span class="sxs-lookup"><span data-stu-id="9550b-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a><span data-ttu-id="9550b-117">[Progressiva][MDNPwaAdvantagesProgressive]</span><span class="sxs-lookup"><span data-stu-id="9550b-117">[Progressive][MDNPwaAdvantagesProgressive]</span></span>
        <span data-ttu-id="9550b-118">A experiência é ampliada (ou para baixo) com recursos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9550b-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::
        ### <a name="safemdnpwaadvantagessafe"></a><span data-ttu-id="9550b-119">[Seguro][MDNPwaAdvantagesSafe]</span><span class="sxs-lookup"><span data-stu-id="9550b-119">[Safe][MDNPwaAdvantagesSafe]</span></span>
        <span data-ttu-id="9550b-120">Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário</span><span class="sxs-lookup"><span data-stu-id="9550b-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a><span data-ttu-id="9550b-121">[Responsivo][MDNPwaAdvantagesResponsive]</span><span class="sxs-lookup"><span data-stu-id="9550b-121">[Responsive][MDNPwaAdvantagesResponsive]</span></span>
        <span data-ttu-id="9550b-122">Adapta-se ao tamanho da tela ou orientação e ao método de entrada do usuário</span><span class="sxs-lookup"><span data-stu-id="9550b-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::
        ### <a name="linkablemdnpwaadvantageslinkable"></a><span data-ttu-id="9550b-123">[Linkable][MDNPwaAdvantagesLinkable]</span><span class="sxs-lookup"><span data-stu-id="9550b-123">[Linkable][MDNPwaAdvantagesLinkable]</span></span>
        <span data-ttu-id="9550b-124">Compartilhar e iniciar de um hiperlink padrão</span><span class="sxs-lookup"><span data-stu-id="9550b-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="9550b-125">Crie \(ou convert\) seu site existente em um PWA para aprimorar seu envolvimento com seus usuários.</span><span class="sxs-lookup"><span data-stu-id="9550b-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="9550b-126">Os aprimoramentos incluem notificações por push, integração com aplicativos e suporte offline.</span><span class="sxs-lookup"><span data-stu-id="9550b-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="9550b-127">Continue a criar sua audiência na Web aberta para que os usuários descubram seu PWA por meio da pesquisa e do compartilhamento de links.</span><span class="sxs-lookup"><span data-stu-id="9550b-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="9550b-128">O melhor de tudo é que seu aplicativo é atualizado usando o código do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="9550b-128">Best of all, your app is updated in using your web server code.</span></span>  

## <a name="pwas-on-microsoft-edge-chromium"></a><span data-ttu-id="9550b-129">PWAs no Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="9550b-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="9550b-130">Quando você cria um Aplicativo Web Progressivo destinado a APIs padrão da Web, seu aplicativo pode ser implantado em plataformas e dispositivos e tirar proveito dos recursos específicos do dispositivo conforme disponível.</span><span class="sxs-lookup"><span data-stu-id="9550b-130">When you build a Progressive Web App targeting web standard APIs, your app may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="9550b-131">PWAs no Microsoft Edge \(Chromium\) adicione as seguintes vantagens ao seu site.</span><span class="sxs-lookup"><span data-stu-id="9550b-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="9550b-132">Seu aplicativo é criado em uma plataforma Web baseada em padrões.</span><span class="sxs-lookup"><span data-stu-id="9550b-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="9550b-133">Permite que os usuários instalem seu aplicativo diretamente do navegador.</span><span class="sxs-lookup"><span data-stu-id="9550b-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="9550b-134">Permite que os usuários instalem seu aplicativo sem uma implantação ou registro baseado na Loja.</span><span class="sxs-lookup"><span data-stu-id="9550b-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="9550b-135">PWAs da área de trabalho têm suporte em qualquer uma das plataformas em que o Microsoft Edge \(Chromium\) está disponível.</span><span class="sxs-lookup"><span data-stu-id="9550b-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="9550b-136">O Microsoft Edge \(Chromium\) está disponível no Windows 7, Windows 10 e macOS.</span><span class="sxs-lookup"><span data-stu-id="9550b-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="9550b-137">Os seguintes benefícios estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="9550b-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="9550b-138">Os aplicativos podem ser instalados diretamente de dentro do navegador usando o ícone **Instalar** na barra de navegação.</span><span class="sxs-lookup"><span data-stu-id="9550b-138">Apps may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Instalar o ícone e o flyout do aplicativo" lightbox="./media/install-progressive-web-app-icon.png":::
       <span data-ttu-id="9550b-140">Instalar o ícone e o flyout do aplicativo</span><span class="sxs-lookup"><span data-stu-id="9550b-140">Install app flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="9550b-141">Os aplicativos também podem ser instalados, executados e gerenciados no menu **Configurações**  >  **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="9550b-141">Apps may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="Itens de menu do aplicativo em configurações" lightbox="./media/app-menus.png":::
       <span data-ttu-id="9550b-143">Itens de menu do aplicativo em configurações</span><span class="sxs-lookup"><span data-stu-id="9550b-143">App menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="9550b-144">As notificações da Web são integradas ao sistema de notificação do Windows</span><span class="sxs-lookup"><span data-stu-id="9550b-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="9550b-145">Armazenamento de cookies compartilhado com o perfil do navegador que instalou o aplicativo</span><span class="sxs-lookup"><span data-stu-id="9550b-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="9550b-146">Acesso a outros recursos do navegador usando o menu **Configuração** e mais \( \) incluindo validação de certificado, permissões de site, proteção de controle e `...` extensões do navegador</span><span class="sxs-lookup"><span data-stu-id="9550b-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="9550b-147">Acesso total ao [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para depuração de seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="9550b-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!NOTE]
> <span data-ttu-id="9550b-148">Para obter mais informações sobre benefícios do PWA, recursos futuros e demonstrações curtas, navegue até [Build 2020 PWA session][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="9550b-148">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <a name="requirements"></a><span data-ttu-id="9550b-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9550b-149">Requirements</span></span>  

<span data-ttu-id="9550b-150">Para ser executado como um PWA, seu aplicativo Web hospedado pelo servidor deve incluir os requisitos mínimos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9550b-150">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-151">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9550b-151">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-152">Protege seus usuários fornecendo uma conexão segura para comunicação de servidor ou aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9550b-152">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="9550b-153">Os Trabalhadores do Serviço e outras tecnologias do PWA só funcionam com recursos web servidos por meio de uma conexão segura \(ou de para `localhost` fins de depuração\).</span><span class="sxs-lookup"><span data-stu-id="9550b-153">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-154">Profissionais de Serviço</span><span class="sxs-lookup"><span data-stu-id="9550b-154">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-155">Usa threads de Trabalho de Serviço para atuar como proxies de rede entre seu servidor e aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="9550b-155">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="9550b-156">Os threads do Service Worker fornecem suporte offline, cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de desempenho de carga de página.</span><span class="sxs-lookup"><span data-stu-id="9550b-156">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-157">Manifesto do Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="9550b-157">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-158">Fornece um arquivo de metadados baseado em JSON que descreve as principais informações sobre seu aplicativo Web, de modo que o Windows 10 e outras plataformas host forneçam aos usuários do PWA uma experiência de aplicativo nativa e instalável.</span><span class="sxs-lookup"><span data-stu-id="9550b-158">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="9550b-159">As informações principais incluem ícones, idioma e ponto de entrada de URL.</span><span class="sxs-lookup"><span data-stu-id="9550b-159">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="9550b-160">Para ser um ótimo PWA, seu aplicativo também deve atender aos seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="9550b-160">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-161">Compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="9550b-161">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-162">Verifique se o PWA funciona [testando em][MicrosoftDeveloperEdgeToolsRemote] diferentes navegadores e ambientes.</span><span class="sxs-lookup"><span data-stu-id="9550b-162">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-163">Design dinâmico</span><span class="sxs-lookup"><span data-stu-id="9550b-163">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-164">Emprega layouts fluidos e imagens flexíveis.</span><span class="sxs-lookup"><span data-stu-id="9550b-164">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="9550b-165">O design responsivo inclui os elementos a seguir que adaptam seu UX ao dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="9550b-165">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="9550b-166">Grade [][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="9550b-166">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="9550b-167">flexbox</span><span class="sxs-lookup"><span data-stu-id="9550b-167">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="9550b-168">Grade [][MDNCssGridLayout] CSS e [flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="9550b-168">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="9550b-169">consultas de mídia</span><span class="sxs-lookup"><span data-stu-id="9550b-169">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="9550b-170">imagens responsivas</span><span class="sxs-lookup"><span data-stu-id="9550b-170">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="9550b-171">Usa [ferramentas de emulação][DevToolsGuideDeviceModeTestingOtherBrowsers] de dispositivo do navegador para testar localmente ou criar uma sessão de depuração remota no [Windows][DevtoolsRemoteDebuggingWindows] ou [Android][DevtoolsRemoteDebuggingIndex] para testar diretamente em um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="9550b-171">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-172">Vinculação profunda</span><span class="sxs-lookup"><span data-stu-id="9550b-172">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-173">Encaminha cada página do seu site para uma URL exclusiva para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.</span><span class="sxs-lookup"><span data-stu-id="9550b-173">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-174">Práticas de validação e teste</span><span class="sxs-lookup"><span data-stu-id="9550b-174">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-175">Usa ferramentas de qualidade de código como o [linter Webhint][Webhint] para otimizar a eficiência, robustez, segurança e acessibilidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9550b-175">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="9550b-176">Lista de verificação do Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="9550b-176">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="9550b-177">Verifica seu PWA na lista de verificação do PWA da linha de base do Google.</span><span class="sxs-lookup"><span data-stu-id="9550b-177">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="9550b-178">Para transformar o PWA em um aplicativo da [Microsoft Store,][MicrosoftDeveloperStore] navegue até [Progressive Web Apps (EdgeHTML) na Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="9550b-178">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] app, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9550b-179">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9550b-179">See also</span></span>  

*   [<span data-ttu-id="9550b-180">PWAs de estouros de míticos</span><span class="sxs-lookup"><span data-stu-id="9550b-180">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="9550b-181">Um roteiro progressivo para seu Aplicativo Web Progressivo</span><span class="sxs-lookup"><span data-stu-id="9550b-181">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="9550b-182">POSTs offline com aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="9550b-182">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="9550b-183">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="9550b-183">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="9550b-184">Apostando na Web</span><span class="sxs-lookup"><span data-stu-id="9550b-184">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="9550b-185">Nomear Aplicativos Web Progressivos</span><span class="sxs-lookup"><span data-stu-id="9550b-185">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="9550b-186">Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 1)</span><span class="sxs-lookup"><span data-stu-id="9550b-186">Designing And Building A Progressive Web App Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [<span data-ttu-id="9550b-187">Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 2)</span><span class="sxs-lookup"><span data-stu-id="9550b-187">Designing And Building A Progressive Web App Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [<span data-ttu-id="9550b-188">Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 3)</span><span class="sxs-lookup"><span data-stu-id="9550b-188">Designing And Building A Progressive Web App Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Começar com a depuração remota de dispositivos Windows 10 | Microsoft Docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emular e testar outros navegadores | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Depurar aplicativos Web progressivos | Microsoft Docs"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Publique seu Aplicativo Web Progressivo na Microsoft Store | Microsoft Docs"

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Visão geral do Windows Push Notification Services (WNS) | Microsoft Docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Projetando para Xbox e TV | Microsoft Docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considerações da interface do usuário para dispositivos UWP | Microsoft Docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "O que é um aplicativo UWP (Plataforma Universal do Windows) | Microsoft Docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Dar suporte ao aplicativo com tarefas em segundo plano | Microsoft Docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publicar aplicativos e jogos do Windows | Microsoft Docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Abrir uma conta de desenvolvedor | Microsoft Docs"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Saudando aplicativos Web progressivos para o Microsoft Edge e o Windows 10 - Blogs do Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de sincronização em segundo plano - Status da plataforma do Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifesto do Aplicativo Web - Status da Plataforma do Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Teste instantâneo"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Realidade Misturada para desenvolvedores"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar Novo Navegador do Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Ativar ou desativar a assistência de foco no Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Alterar configurações de notificação no Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Noções básicas sobre aprimoramento progressivo - uma lista separada"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "aplicativos | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Testes entre navegadores | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Layout de caixa flexível css | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Layout de Grade CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar api | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Consultas de mídia | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Api de notificações | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Discoverable - Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Installable - Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Linkable - Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Independente da rede - Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Reativar - Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Responsivo - Vantagens progressivas do aplicativo Web"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Seguro - Vantagens progressivas do aplicativo Web"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imagens responsivas | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de Trabalho de Serviço | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do Aplicativo Web | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Vídeo do PWA"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Um roteiro progressivo para seu Aplicativo Web Progressivo"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs de estouros de míticos – a nova edição de borda"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Nomear Aplicativos Web Progressivos"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Apostando na Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "POSTs offline com aplicativos Web progressivos"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 1)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 2)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "O que torna um bom Aplicativo Web Progressivo? | web.dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculação profunda - Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS - Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Design da Web responsivo - Wikipédia"  
