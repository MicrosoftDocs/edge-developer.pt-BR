---
description: Aplicativos Web progressivos são executados nativamente no Windows 10.  Aqui está tudo o que você precisa saber como desenvolvedor da Web.
title: Aplicativos Web progressivos no Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 482f498e246ee265424f7b80ff3cd67f78501ee2
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583032"
---
# <span data-ttu-id="dec7e-105">Aplicativos Web progressivos no Windows</span><span class="sxs-lookup"><span data-stu-id="dec7e-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="dec7e-106">Com os [aplicativos Web progressivos][MDNApps] \ (ou simplesmente PWAs \), você não precisa decidir entre usar tecnologias abertas da Web para interoperabilidade entre plataformas e fornecer aos seus usuários uma experiência de aplicativo nativo personalizada para seus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dec7e-106">With [Progressive Web Apps][MDNApps] \(or simply PWAs\), you do not have to decide between using open web technologies for cross-platform interoperability and providing your users with a native app-like experience customized for their devices.</span></span>  <span data-ttu-id="dec7e-107">PWAs são apenas sites que são [progressivamente aprimorados][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.</span><span class="sxs-lookup"><span data-stu-id="dec7e-107">PWAs are just websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="dec7e-108">As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.</span><span class="sxs-lookup"><span data-stu-id="dec7e-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        ![Ícone detectável][ImageISearch]
        ### [<span data-ttu-id="dec7e-110">Detectáveis</span><span class="sxs-lookup"><span data-stu-id="dec7e-110">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="dec7e-111">Nos resultados da pesquisa na Web e nos repositórios de aplicativos de suporte</span><span class="sxs-lookup"><span data-stu-id="dec7e-111">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        ![Ícone instalável][ImageIPackage]
        ### [<span data-ttu-id="dec7e-113">Instaláveis</span><span class="sxs-lookup"><span data-stu-id="dec7e-113">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="dec7e-114">Fixar e iniciar na tela inicial, no menu Iniciar, na barra de tarefas e assim por diante</span><span class="sxs-lookup"><span data-stu-id="dec7e-114">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        ![Ícone recontratar][ImageIPushNotification]
        ### [<span data-ttu-id="dec7e-116">Recontratar</span><span class="sxs-lookup"><span data-stu-id="dec7e-116">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="dec7e-117">Enviar notificações por push, mesmo quando o aplicativo não estiver ativo</span><span class="sxs-lookup"><span data-stu-id="dec7e-117">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
    :::column:::
        ![Ícone independente de rede][ImageIOffline]
        ### [<span data-ttu-id="dec7e-119">Independente de rede</span><span class="sxs-lookup"><span data-stu-id="dec7e-119">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="dec7e-120">O Works offline e em condições de rede baixa</span><span class="sxs-lookup"><span data-stu-id="dec7e-120">Works offline and in low-network conditions</span></span>
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Ícone progressivo][ImageIProgressive]
        ### [<span data-ttu-id="dec7e-122">Progressivas</span><span class="sxs-lookup"><span data-stu-id="dec7e-122">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="dec7e-123">A experiência pode ser dimensionada para cima (ou para baixo) com recursos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="dec7e-123">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        ![Ícone de segurança][ImageISecurity]
        ### [<span data-ttu-id="dec7e-125">Desligar</span><span class="sxs-lookup"><span data-stu-id="dec7e-125">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="dec7e-126">Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário</span><span class="sxs-lookup"><span data-stu-id="dec7e-126">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
    :::column:::
        ![Ícone responsivo][ImageIResponsive]
        ### [<span data-ttu-id="dec7e-128">Responsivo</span><span class="sxs-lookup"><span data-stu-id="dec7e-128">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="dec7e-129">Adapta-se ao tamanho da tela ou orientação e método de entrada do usuário</span><span class="sxs-lookup"><span data-stu-id="dec7e-129">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        ![Ícone vinculável][ImageILink]
        ### [<span data-ttu-id="dec7e-131">Vinculável</span><span class="sxs-lookup"><span data-stu-id="dec7e-131">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="dec7e-132">Compartilhar e iniciar a partir de um hiperlink padrão</span><span class="sxs-lookup"><span data-stu-id="dec7e-132">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="dec7e-133">Ao criar ou converter seu site existente em um PWA, você se envolve melhor com seu público-alvo existente usando notificações por push, integração do tipo de aplicativo e suporte offline.</span><span class="sxs-lookup"><span data-stu-id="dec7e-133">By building or converting your existing site to a PWA, you engage better with your existing audience using push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="dec7e-134">Ao mesmo tempo, você deve continuar a criar seu público-alvo na Web em aberto, pois os usuários detectam o PWA por meio de pesquisa e compartilhamento de links.</span><span class="sxs-lookup"><span data-stu-id="dec7e-134">At the same time, you should continue to build your audience on the open web, as users discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="dec7e-135">O melhor de tudo é que você pode atualizar seu aplicativo simplesmente atualizando o código do servidor Web.</span><span class="sxs-lookup"><span data-stu-id="dec7e-135">Best of all, you may update your app by simply updating your web server code.</span></span>  

## <span data-ttu-id="dec7e-136">PWAs no Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="dec7e-136">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="dec7e-137">Quando você cria um aplicativo Web progressivo direcionado a APIs da Web Standard, seu aplicativo pode ser implantado entre plataformas e dispositivos e aproveitando os recursos específicos do dispositivo como disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dec7e-137">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device specific capabilities as available.</span></span>  <span data-ttu-id="dec7e-138">O PWAs no Microsoft Edge \ (Chromium \) são completamente baseados em padrões de uma perspectiva de plataforma da Web e permitem que os usuários instalem o aplicativo diretamente no navegador sem a necessidade de implantação ou registro baseados na loja.</span><span class="sxs-lookup"><span data-stu-id="dec7e-138">PWAs in Microsoft Edge \(Chromium\) are completely standards-based from a web platform perspective and enable users to install the app directly from within the browser without the need for Store-based deployment or registration.</span></span>  <span data-ttu-id="dec7e-139">A área de trabalho PWAs são compatíveis com qualquer uma das plataformas o Microsoft Edge \ (Chromium \) está disponível, incluindo Windows 7, Windows 10 e macOS.</span><span class="sxs-lookup"><span data-stu-id="dec7e-139">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available, including Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="dec7e-140">Outros benefícios incluem:</span><span class="sxs-lookup"><span data-stu-id="dec7e-140">Other benefits include:</span></span>  

*   <span data-ttu-id="dec7e-141">Os aplicativos podem ser instalados diretamente no navegador pelo ícone de **instalação** na barra de navegação.</span><span class="sxs-lookup"><span data-stu-id="dec7e-141">Applications may be installed directly from within the browser via the **Install** icon in the navigation bar.</span></span>  
    
    ![Instalar submenu e ícone do aplicativo][ImageInstallPwa]  
    
*   <span data-ttu-id="dec7e-143">Os aplicativos também podem ser instalados, executados e gerenciados no menu **configurações**de  >  **aplicativos**</span><span class="sxs-lookup"><span data-stu-id="dec7e-143">Applications may also be installed, run and managed from the **Settings** > **Apps** menu</span></span>  
    
    ![Itens de menu do aplicativo em configurações][ImageAppMenus]  

*   <span data-ttu-id="dec7e-145">As notificações da Web são integradas ao sistema de notificação do Windows</span><span class="sxs-lookup"><span data-stu-id="dec7e-145">Web Notifications are integrated into the Windows notification system</span></span>
*   <span data-ttu-id="dec7e-146">Repositório de cookies compartilhados com o perfil do navegador que instalou o aplicativo</span><span class="sxs-lookup"><span data-stu-id="dec7e-146">Shared cookie store with the browser profile that installed the app</span></span>
*   <span data-ttu-id="dec7e-147">Acesso a outros recursos do navegador por meio do `...` menu, incluindo a validação do certificado, as permissões de site, a proteção de rastreamento e as extensões do navegador</span><span class="sxs-lookup"><span data-stu-id="dec7e-147">Access to other browser features via the `...` menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>
*   <span data-ttu-id="dec7e-148">Acesso total ao [Microsoft Edge devtools][DevtoolsProgressiveWebApps] para depurar seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="dec7e-148">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="dec7e-149">Para personalizar o PWAs especificamente para o Windows 10 que faz solicitações de API do WinRT usando JavaScript, consulte a [documentação específica para os recursos do PWA do EdgeHTML][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="dec7e-149">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, see the [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="dec7e-150">Saiba mais sobre como testar o PWA no Windows 10 e distribuí-lo na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="dec7e-150">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

## <span data-ttu-id="dec7e-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec7e-151">Requirements</span></span>  

<span data-ttu-id="dec7e-152">Para ser executado como um PWA, seu aplicativo Web hospedado no servidor deve incluir os requisitos mínimos a seguir.</span><span class="sxs-lookup"><span data-stu-id="dec7e-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

|  | <span data-ttu-id="dec7e-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec7e-153">Requirement</span></span> | <span data-ttu-id="dec7e-154">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dec7e-154">Details</span></span> | 
|:--- |:--- |:--- |  
| <span data-ttu-id="dec7e-155">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-155">X</span></span> | [<span data-ttu-id="dec7e-156">HTTPS</span><span class="sxs-lookup"><span data-stu-id="dec7e-156">HTTPS</span></span>][WikiHttps] | <span data-ttu-id="dec7e-157">Proteja seus usuários fornecendo uma conexão segura para comunicação do servidor ou do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dec7e-157">Protect your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="dec7e-158">Os funcionários do serviço e outras tecnologias do PWA só funcionam com recursos da Web servidos por meio de uma conexão segura \ (ou de `localhost` para fins de depuração \).</span><span class="sxs-lookup"><span data-stu-id="dec7e-158">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  |  
| <span data-ttu-id="dec7e-159">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-159">X</span></span> | [<span data-ttu-id="dec7e-160">Trabalhadores do serviço</span><span class="sxs-lookup"><span data-stu-id="dec7e-160">Service Workers</span></span>][MDNServiceWorkerApi] | <span data-ttu-id="dec7e-161">Use threads de trabalho do serviço para atuar como proxies de rede entre o aplicativo cliente e servidor para fornecer suporte offline, armazenamento em cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de perf de carregamento de página.</span><span class="sxs-lookup"><span data-stu-id="dec7e-161">Use Service Worker threads to act as network proxies between your server and client app in order to provide offline support, resource caching, push notifications, background data sync, and  page load perf optimizations.</span></span>  |  
| <span data-ttu-id="dec7e-162">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-162">X</span></span> | [<span data-ttu-id="dec7e-163">Manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="dec7e-163">Web App Manifest</span></span>][MDNWebAppManifest] | <span data-ttu-id="dec7e-164">Forneça um arquivo de metadados baseado em JSON que descreve as principais informações sobre o seu aplicativo Web \ (como ícones, idioma e ponto de entrada de URL \), para que o Windows 10 e outras plataformas de host possam fornecer aos usuários do PWA uma experiência instalável e parecida com o aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="dec7e-164">Provide a JSON-based metadata file describing key information about your web app \(such as icons, language, and URL entry point\), so that Windows 10 and other host platforms are able to provide your PWA users with an installable, native app-like experience.</span></span>  |  

<span data-ttu-id="dec7e-165">Para ser um grande PWA, seu aplicativo também deve atender aos seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="dec7e-165">To be a great PWA, your app must also meet the following requirements.</span></span>  

|  | <span data-ttu-id="dec7e-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec7e-166">Requirement</span></span> | <span data-ttu-id="dec7e-167">Detalhes</span><span class="sxs-lookup"><span data-stu-id="dec7e-167">Details</span></span> | 
|:--- |:--- |:--- |  
| <span data-ttu-id="dec7e-168">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-168">X</span></span> | [<span data-ttu-id="dec7e-169">Compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="dec7e-169">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting] | <span data-ttu-id="dec7e-170">Certifique-se de que o PWA funcione [testando][MicrosoftDeveloperEdgeToolsRemote] em diferentes navegadores e ambientes.</span><span class="sxs-lookup"><span data-stu-id="dec7e-170">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  |  
| <span data-ttu-id="dec7e-171">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-171">X</span></span> | [<span data-ttu-id="dec7e-172">Design dinâmico</span><span class="sxs-lookup"><span data-stu-id="dec7e-172">Responsive design</span></span>][WikiResponsiveWebDesign] | <span data-ttu-id="dec7e-173">Empregue layouts fluidos e imagens flexíveis com [grade][MDNCssGridLayout]CSS, [flexbox][MDNCssFlexibleBoxLayout], [grade][MDNCssGridLayout] CSS e [flexbox][MDNCssFlexibleBoxLayout] , [consultas de mídia][MDNMediaQueries]e [imagens responsivas][MDNResponsiveImages] para adaptar sua experiência ao dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="dec7e-173">Employ fluid layouts and flexible images with CSS [grid][MDNCssGridLayout], [flexbox][MDNCssFlexibleBoxLayout], CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout] , [media queries][MDNMediaQueries], and [responsive images][MDNResponsiveImages] to adapt your UX to your user's device.</span></span>  <span data-ttu-id="dec7e-174">Use [ferramentas de emulação de dispositivo][DevToolsGuide|::ref1::|] do seu navegador para testar localmente ou configure uma [sessão de depuração remota][DevToolsProtocolClientsEdgeDevToolsPreview] para testar diretamente um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="dec7e-174">Use [device emulation tools][DevToolsGuide|::ref1::|] from your browser to test locally, or set up a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>  |  
| <span data-ttu-id="dec7e-175">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-175">X</span></span> | [<span data-ttu-id="dec7e-176">Vinculação profunda</span><span class="sxs-lookup"><span data-stu-id="dec7e-176">Deep linking</span></span>][WikiDeepLinking] | <span data-ttu-id="dec7e-177">Encaminhar cada página do seu site para um URL exclusivo para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.</span><span class="sxs-lookup"><span data-stu-id="dec7e-177">Route each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  |  
| <span data-ttu-id="dec7e-178">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-178">X</span></span> | [<span data-ttu-id="dec7e-179">Práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="dec7e-179">Best practices</span></span>][Webhint] | <span data-ttu-id="dec7e-180">Use ferramentas de qualidade de código como o [webhint][Webhint] para otimizar a eficiência, a robustez, a segurança e a acessibilidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dec7e-180">Use code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  |  
| <span data-ttu-id="dec7e-181">X</span><span class="sxs-lookup"><span data-stu-id="dec7e-181">X</span></span> | [<span data-ttu-id="dec7e-182">Lista de verificação do Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="dec7e-182">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist] | <span data-ttu-id="dec7e-183">Verifique seu PWA em relação à lista de verificação do Google Baseline PWA.</span><span class="sxs-lookup"><span data-stu-id="dec7e-183">Check your PWA against the Google baseline PWA checklist.</span></span>  |  

<span data-ttu-id="dec7e-184">Se você quiser transformar o PWA em um aplicativo da [Microsoft Store][MicrosoftDeveloperStore] , vá para a documentação dos [aplicativos Web progressivos (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .</span><span class="sxs-lookup"><span data-stu-id="dec7e-184">If you want to turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, head to the [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] documentation.</span></span>  

## <span data-ttu-id="dec7e-185">Disponibilidade atual</span><span class="sxs-lookup"><span data-stu-id="dec7e-185">Current availability</span></span>  

<span data-ttu-id="dec7e-186">Suporte ao mecanismo de navegador para solicitações progressivas de aplicativo Web para vários componentes arquitetônicos, o mais significativo sendo a infraestrutura de rede subjacente à [API de busca][MDNFetchApi].</span><span class="sxs-lookup"><span data-stu-id="dec7e-186">Browser engine support for Progressive Web App requests for a number of architectural components, the most significant being the networking infrastructure underlying the [Fetch API][MDNFetchApi].</span></span>  

<span data-ttu-id="dec7e-187">Para o Microsoft Edge \ (Chromium \), a plataforma do navegador inclui suporte completo para esses recursos que funcionam entre dispositivos em que o Microsoft Edge \ (Chromium \) é compatível.</span><span class="sxs-lookup"><span data-stu-id="dec7e-187">For Microsoft Edge \(Chromium\), the browser platform includes full support for these features that work across devices where Microsoft Edge \(Chromium\) is supported.</span></span>  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

[ImageInstallPwa]: ./media/Install_PWA.png  
[ImageAppMenus]: ./media/App_menus.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clientes do protocolo DevTools preview do Microsoft Edge-DevTools"  
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

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "O que faz um bom aplicativo Web progressivo? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculação profunda-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Design da Web responsivo-Wikipédia"  
