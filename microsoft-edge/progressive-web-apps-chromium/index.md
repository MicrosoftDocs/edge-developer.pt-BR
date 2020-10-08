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
# Aplicativos Web progressivos no Windows  

[Aplicativos Web progressivos][MDNApps] \ (PWAs \) fornecem acesso a tecnologias da Web abertas para interoperabilidade entre plataformas e oferecer aos usuários uma experiência nativa e semelhante a um aplicativo personalizada para seus dispositivos.  PWAs são sites [aprimorados progressivamente][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.  As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [Detectáveis][MDNPwaAdvantagesDiscoverable]
        Nos resultados da pesquisa na Web e nos repositórios de aplicativos de suporte
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [Instaláveis][MDNPwaAdvantagesInstallable]
        Fixar e iniciar na tela inicial, no menu Iniciar, na barra de tarefas e assim por diante
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [Recontratar][MDNPwaAdvantagesReEngageable]
        Enviar notificações por push, mesmo quando o aplicativo não estiver ativo
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [Independente de rede][MDNPwaAdvantagesNetworkIndependent]
        O Works offline e em condições de rede baixa
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [Progressivas][MDNPwaAdvantagesProgressive]
        A experiência pode ser dimensionada para cima (ou para baixo) com recursos de dispositivo
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [Desligar][MDNPwaAdvantagesSafe]
        Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [Responsivo][MDNPwaAdvantagesResponsive]
        Adapta-se ao tamanho da tela ou orientação e método de entrada do usuário
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [Vinculável][MDNPwaAdvantagesLinkable]
        Compartilhar e iniciar a partir de um hiperlink padrão
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Construa \ (ou converta \) seu site existente em um PWA para aprimorar seu envolvimento com os usuários.  Melhorias incluem notificações por push, integração do tipo de aplicativo e suporte offline.  Continue a criar seu público-alvo na Web em aberto para que os usuários descubram o PWA por meio de pesquisa e compartilhamento de links.  O melhor de tudo é que seu aplicativo é atualizado para usar seu código de servidor Web.  

## PWAs no Microsoft Edge (Chromium)  

Quando você cria um aplicativo Web progressivo direcionado a APIs da Web Standard, seu aplicativo pode ser implantado entre plataformas e dispositivos e aproveitando as funcionalidades específicas do dispositivo, conforme disponível.  PWAs no Microsoft Edge \ (Chromium \) adicione as seguintes vantagens ao seu site.  

*   Seu aplicativo é baseado em uma plataforma da Web baseada em padrões.  
*   Permite que os usuários instalem o aplicativo diretamente do navegador.  
*   Permite que os usuários instalem seu aplicativo sem uma implantação ou registro baseado na loja.  
    
Os PWAs da área de trabalho são compatíveis com qualquer uma das plataformas que o Microsoft Edge \ (Chromium \) está disponível. O Microsoft Edge \ (Chromium \) está disponível no Windows 7, no Windows 10 e no macOS.  Os benefícios a seguir estão incluídos.  

*   Os aplicativos podem ser instalados diretamente no navegador usando o ícone de **instalação** na barra de navegação.  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Instalar submenu e ícone do aplicativo" lightbox="./media/install_pwa_icon.png":::
       Instalar submenu e ícone do aplicativo  
    :::image-end:::  
    
*   Os aplicativos também podem ser instalados, executados e gerenciados no menu **configurações**de  >  **aplicativos**  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Instalar submenu e ícone do aplicativo" lightbox="./media/app_menus.png":::
       Itens de menu do aplicativo em configurações  
    :::image-end:::  
    
*   As notificações da Web são integradas ao sistema de notificação do Windows  
*   Repositório de cookies compartilhados com o perfil do navegador que instalou o aplicativo  
*   Acesso a outros recursos do navegador usando o menu de **configuração e mais** \ ( `...` \), incluindo validação de certificado, permissões de site, proteção de rastreamento e extensões de navegador  
*   Acesso total ao [Microsoft Edge devtools][DevtoolsProgressiveWebApps] para depurar seu aplicativo  
    
> [!IMPORTANT]
> Para personalizar o PWAs especificamente para o Windows 10 que faz solicitações de API do WinRT usando JavaScript, navegue até [a documentação específica para os recursos do PWA do EdgeHTML][PwaEdgehtmlIndex].  Saiba mais sobre como testar o PWA no Windows 10 e distribuí-lo na Microsoft Store.  

> [!NOTE]
> Para obter mais informações sobre benefícios do PWA, recursos futuros e demonstrações curtas, navegue até [Build 2020 PWA Session][BuildVideo]. 

## Requisitos  

Para ser executado como um PWA, seu aplicativo Web hospedado no servidor deve incluir os requisitos mínimos a seguir.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Protege seus usuários fornecendo uma conexão segura para comunicação do servidor ou do aplicativo.  Os funcionários do serviço e outras tecnologias do PWA só funcionam com recursos da Web servidos por meio de uma conexão segura \ (ou de `localhost` para fins de depuração \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Profissionais de Serviço][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Usa threads de trabalho de serviço para atuar como proxies de rede entre o aplicativo cliente e servidor.  Threads de trabalho do serviço fornecem suporte offline, cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de desempenho de carregamento de página.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Manifesto do aplicativo Web][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Fornece um arquivo de metadados baseado em JSON que descreve as principais informações sobre o seu aplicativo Web, para que o Windows 10 e outras plataformas de host forneçam aos seus usuários do PWA uma experiência que permite a instalação e a aparência do aplicativo nativo.  As informações de chave incluem ícones, idioma e ponto de entrada de URL. 
   :::column-end:::
:::row-end:::  

Para ser um grande PWA, seu aplicativo também deve atender aos seguintes requisitos.  

:::row:::
   :::column span="1":::
      [Compatibilidade entre navegadores][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Certifique-se de que o PWA funcione [testando][MicrosoftDeveloperEdgeToolsRemote] em diferentes navegadores e ambientes.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Design dinâmico][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Emprega layouts fluidos e imagens flexíveis.  O design responsivo inclui os seguintes elementos que adaptam a sua experiência ao dispositivo do usuário.  
      
      *   [Grade][MDNCssGridLayout] CSS  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   [Grade][MDNCssGridLayout] e [flexbox][MDNCssFlexibleBoxLayout] CSS  
      *   [consultas de mídia][MDNMediaQueries]  
      *   [imagens responsivas][MDNResponsiveImages]  
      
      Usa [ferramentas de emulação de dispositivo][DevToolsGuide|::ref1::|] do seu navegador para testar localmente ou criar uma [sessão de depuração remota][DevToolsProtocolClientsEdgeDevToolsPreview] para testar diretamente um dispositivo de destino.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Vinculação profunda][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Roteia cada página do seu site para uma URL exclusiva, para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Práticas de validação e teste][Webhint]  
   :::column-end:::
   :::column span="2":::
      Usa ferramentas de qualidade de código como o [webhint][Webhint] subbotão para otimizar a eficiência, a robustez, a segurança e a acessibilidade do seu aplicativo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Lista de verificação do Chromium PWA][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Verifica o PWA em relação à lista de verificação do PWA da linha de base do Google.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Para transformar o PWA em um aplicativo da [Microsoft Store][MicrosoftDeveloperStore] , navegue até [Web Apps progressivos (EdgeHTML) na Microsoft Store][PwaEdgehtmlMicrosoftStore].  
  
## Consulte também  

*   [Myth de PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Um roteiro progressivo para seu aplicativo Web progressivo][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Postagens offline com Web Apps progressivos][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [&DO PWA P A][AaronGustafsonNotebookPwaQa]  
*   [Aposta na Web][JoretegBlogBettingWeb]  
*   [Nomeando aplicativos Web progressivos][Fberriman20170626NamingProgressiveWebApps]  
*   [Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
