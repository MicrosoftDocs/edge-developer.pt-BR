---
description: Os Aplicativos Web Progressivos (Chromium) são executados na Windows 10.  Aqui está tudo o que você precisa saber como desenvolvedor da Web.
title: Aplicativos Web progressivos no Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Borda, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f1f5370af0710927f66c8231274fe307cb3ee2a4
ms.sourcegitcommit: 7f7922dbb6af87ecac1378d18359125770c5b8e5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536806"
---
# <a name="progressive-web-apps-on-windows-overview"></a>Visão geral progressiva dos Aplicativos Web Windows Web  

[Os Aplicativos Web][MDNApps] Progressivos \(PWAs\) fornecem acesso a tecnologias da Web abertas para interoperabilidade entre plataformas e fornecem aos usuários uma experiência nativa, como o aplicativo, personalizada para seus dispositivos.  PWAs são sites que são [progressivamente aprimorados][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.  As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a>[Discoverable][MDNPwaAdvantagesDiscoverable]  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a>[Installable][MDNPwaAdvantagesInstallable]  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a>[Reajagável][MDNPwaAdvantagesReEngageable]  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Dos resultados da pesquisa da Web e dos armazenamentos de aplicativos de suporte  
    :::column-end:::
    :::column:::
        Fixar e iniciar na tela inicial, Menu Iniciar, Barra de Tarefas e assim por diante  
    :::column-end:::
    :::column:::
        Enviar notificações por push, mesmo quando o aplicativo não estiver ativo  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a>[Network Independent][MDNPwaAdvantagesNetworkIndependent]  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a>[Progressiva][MDNPwaAdvantagesProgressive]  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a>[Cofre][MDNPwaAdvantagesSafe]  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Funciona offline e em condições de baixa rede  
    :::column-end:::
    :::column:::
        A experiência é ampliada (ou para baixo) com recursos de dispositivo  
    :::column-end:::
    :::column:::
        Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a>[Responsivo][MDNPwaAdvantagesResponsive]  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a>[Linkable][MDNPwaAdvantagesLinkable]  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Adapta-se ao tamanho da tela ou orientação e ao método de entrada do usuário  
    :::column-end:::
    :::column:::
        Compartilhar e iniciar de um hiperlink padrão  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

Crie \(ou convert\) seu site existente em um PWA para aprimorar seu envolvimento com seus usuários.  Os aprimoramentos incluem notificações por push, integração com aplicativos e suporte offline.  Continue a criar sua audiência na Web aberta para que os usuários descubram sua PWA por meio da pesquisa e do compartilhamento de links.  O melhor de tudo é que seu aplicativo é atualizado usando o código do servidor Web.  

## <a name="pwas-on-microsoft-edge-chromium"></a>PWAs no Microsoft Edge (Chromium)  

Quando você cria um Aplicativo Web Progressivo destinado a APIs padrão da Web, seu aplicativo pode ser implantado em plataformas e dispositivos e tirar proveito dos recursos específicos do dispositivo conforme disponível.  PWAs no Microsoft Edge \(Chromium\) adicione as seguintes vantagens ao seu site.  

*   Seu aplicativo é criado em uma plataforma Web baseada em padrões.  
*   Permite que os usuários instalem seu aplicativo diretamente do navegador.  
*   Permite que os usuários instalem seu aplicativo sem uma implantação ou registro baseado na Store.  
    
PWAs da área de trabalho têm suporte em qualquer uma das plataformas Microsoft Edge \(Chromium\) está disponível. Microsoft Edge \(Chromium\) está disponível no Windows 7, Windows 10 e macOS.  Os seguintes benefícios estão incluídos.  

*   Os aplicativos podem ser instalados diretamente de dentro do navegador usando o ícone **Instalar** na barra de navegação.  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Instalar o ícone e o flyout do aplicativo" lightbox="./media/install-progressive-web-app-icon.png":::
       Instalar o ícone e o flyout do aplicativo  
    :::image-end:::  
    
*   Os aplicativos também podem ser instalados, executados e gerenciados no menu **Configurações**  >  **Apps**  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="Itens de menu do aplicativo em configurações" lightbox="./media/app-menus.png":::
       Itens de menu do aplicativo em configurações  
    :::image-end:::  
    
*   As notificações da Web são integradas ao sistema de Windows de notificação  
*   Armazenamento de cookies compartilhado com o perfil do navegador que instalou o aplicativo  
*   Acesso a outros recursos do navegador usando o menu **Configuração** e mais \( \) incluindo validação de certificado, permissões de site, proteção de controle e `...` extensões do navegador  
*   Acesso total ao [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] para depuração do aplicativo  
    
> [!NOTE]
> Para obter mais informações sobre PWA benefícios, recursos futuros e demonstrações curtas, navegue até [Build 2020 PWA sessão][BuildVideo]. 

## <a name="requirements"></a>Requisitos  

Para ser executado como um PWA, seu aplicativo Web hospedado pelo servidor deve incluir os requisitos mínimos a seguir.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Protege seus usuários fornecendo uma conexão segura para comunicação de servidor ou aplicativo.  Os Trabalhadores do Serviço e outras tecnologias PWA funcionam apenas com recursos web servidos por meio de uma conexão segura \(ou de para `localhost` fins de depuração\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Profissionais de Serviço][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Usa threads de Trabalho de Serviço para atuar como proxies de rede entre seu servidor e aplicativo cliente.  Os threads do Service Worker fornecem suporte offline, cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de desempenho de carga de página.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Manifesto do Aplicativo Web][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Fornece um arquivo de metadados baseado em JSON que descreve as principais informações sobre seu aplicativo Web, para que o Windows 10 e outras plataformas host forneçam aos usuários do PWA uma experiência de aplicativo nativa e instalável.  As informações principais incluem ícones, idioma e ponto de entrada de URL. 
   :::column-end:::
:::row-end:::  

Para ser uma ótima PWA, seu aplicativo também deve atender aos seguintes requisitos.  

:::row:::
   :::column span="1":::
      [Compatibilidade entre navegadores][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Verifique se o PWA funciona [testando em][MicrosoftDeveloperEdgeToolsRemote] diferentes navegadores e ambientes.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Design dinâmico][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Emprega layouts fluidos e imagens flexíveis.  O design responsivo inclui os elementos a seguir que adaptam seu UX ao dispositivo do usuário.  
      
      *   Grade [][MDNCssGridLayout] CSS  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   Grade [][MDNCssGridLayout] CSS e [flexbox][MDNCssFlexibleBoxLayout]  
      *   [consultas de mídia][MDNMediaQueries]  
      *   [imagens responsivas][MDNResponsiveImages]  
          
      Usa [ferramentas de emulação][DevToolsGuideDeviceModeTestingOtherBrowsers] de dispositivo do navegador para testar localmente [][DevtoolsRemoteDebuggingWindows] ou criar uma sessão de depuração remota em Windows ou [Android][DevtoolsRemoteDebuggingIndex] para testar diretamente em um dispositivo de destino.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Vinculação profunda][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Encaminha cada página do seu site para uma URL exclusiva para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Práticas de validação e teste][Webhint]  
   :::column-end:::
   :::column span="2":::
      Usa ferramentas de qualidade de código como o [linter Webhint][Webhint] para otimizar a eficiência, robustez, segurança e acessibilidade do seu aplicativo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Chromium PWA Lista de Verificação][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Verifica sua PWA na lista de verificação da linha de base do Google PWA.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Para transformar seu PWA em um aplicativo [Microsoft Store,][MicrosoftDeveloperStore] navegue até [Progressive Web Apps no Microsoft Store][PwaChromiumMicrosoftStore].  
  
## <a name="see-also"></a>Consulte também  

*   [PWAs de estouros de míticos][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Um roteiro progressivo para seu Aplicativo Web Progressivo][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [POSTs offline com aplicativos Web progressivos][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA P&A][AaronGustafsonNotebookPwaQa]  
*   [Apostando na Web][JoretegBlogBettingWeb]  
*   [Nomear Aplicativos Web Progressivos][Fberriman20170626NamingProgressiveWebApps]  
*   [Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 1)][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 2)][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 3)][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introdução com a Depuração Remota Windows 10 Dispositivos | Microsoft Docs"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Emular e testar outros navegadores | Microsoft Docs"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Depurar aplicativos Web progressivos | Microsoft Docs"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Publique seu Aplicativo Web Progressivo no Microsoft Store | Microsoft Docs"

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows Visão geral Notification Services push (WNS) | Microsoft Docs"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Projetando para Xbox e TV | Microsoft Docs"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considerações da interface do usuário para dispositivos UWP | Microsoft Docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "O que é um aplicativo UWP (Plataforma de Windows Universal) ? | Microsoft Docs"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Dar suporte ao aplicativo com tarefas em segundo plano | Microsoft Docs"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publicar Windows aplicativos e jogos | Microsoft Docs"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Abrir uma conta de desenvolvedor | Microsoft Docs"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Saudando aplicativos Web progressivos para Microsoft Edge e Windows 10 - Windows Blogs"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de sincronização em segundo plano - Microsoft Edge status da plataforma"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifesto do Aplicativo Web - status Microsoft Edge plataforma"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Teste instantâneo"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Realidade Misturada para desenvolvedores"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Baixar Novo Microsoft Edge Navegador"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Ativar ou desativar a assistência de foco em Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Alterar as configurações de notificação Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA P&A"  

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
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Cofre - Vantagens progressivas do aplicativo Web"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imagens responsivas | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de Trabalho de Serviço | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do Aplicativo Web | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "PWA vídeo"  

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
