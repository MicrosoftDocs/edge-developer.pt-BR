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
ms.openlocfilehash: 90740bac07ebfd74f89e2524e6955621e1b09b05
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882804"
---
# Aplicativos Web progressivos no Windows  

Com os [aplicativos Web progressivos][MDNApps] \ (ou simplesmente PWAs \), você não precisa decidir entre usar tecnologias abertas da Web para interoperabilidade entre plataformas e fornecer aos seus usuários uma experiência de aplicativo nativo personalizada para seus dispositivos.  PWAs são apenas sites que são [progressivamente aprimorados][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.  As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.  

:::row:::
    :::column:::
        ![Ícone detectável][ImageISearch]
        ### [Detectáveis][MDNPwaAdvantagesDiscoverable]
        Nos resultados da pesquisa na Web e nos repositórios de aplicativos de suporte
    :::column-end:::
    :::column:::
        ![Ícone instalável][ImageIPackage]
        ### [Instaláveis][MDNPwaAdvantagesInstallable]
        Fixar e iniciar na tela inicial, no menu Iniciar, na barra de tarefas e assim por diante
    :::column-end:::
    :::column:::
        ![Ícone recontratar][ImageIPushNotification]
        ### [Recontratar][MDNPwaAdvantagesReEngageable]
        Enviar notificações por push, mesmo quando o aplicativo não estiver ativo
    :::column-end:::
    :::column:::
        ![Ícone independente de rede][ImageIOffline]
        ### [Independente de rede][MDNPwaAdvantagesNetworkIndependent]
        O Works offline e em condições de rede baixa
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Ícone progressivo][ImageIProgressive]
        ### [Progressivas][MDNPwaAdvantagesProgressive]
        A experiência pode ser dimensionada para cima (ou para baixo) com recursos de dispositivo
    :::column-end:::
    :::column:::
        ![Ícone de segurança][ImageISecurity]
        ### [Desligar][MDNPwaAdvantagesSafe]
        Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário
    :::column-end:::
    :::column:::
        ![Ícone responsivo][ImageIResponsive]
        ### [Responsivo][MDNPwaAdvantagesResponsive]
        Adapta-se ao tamanho da tela ou orientação e método de entrada do usuário
    :::column-end:::
    :::column:::
        ![Ícone vinculável][ImageILink]
        ### [Vinculável][MDNPwaAdvantagesLinkable]
        Compartilhar e iniciar a partir de um hiperlink padrão
    :::column-end:::
:::row-end:::

Ao criar ou converter seu site existente em um PWA, você se envolve melhor com seu público-alvo existente usando notificações por push, integração do tipo de aplicativo e suporte offline.  Ao mesmo tempo, você deve continuar a criar seu público-alvo na Web em aberto, pois os usuários detectam o PWA por meio de pesquisa e compartilhamento de links.  O melhor de tudo é que você pode atualizar seu aplicativo simplesmente atualizando o código do servidor Web.  

## PWAs no Microsoft Edge (Chromium)  

Quando você cria um aplicativo Web progressivo direcionado a APIs da Web Standard, seu aplicativo pode ser implantado entre plataformas e dispositivos e aproveitando os recursos específicos do dispositivo como disponíveis.  O PWAs no Microsoft Edge \ (Chromium \) são completamente baseados em padrões de uma perspectiva de plataforma da Web e permitem que os usuários instalem o aplicativo diretamente no navegador sem a necessidade de implantação ou registro baseados na loja.  A área de trabalho PWAs são compatíveis com qualquer uma das plataformas o Microsoft Edge \ (Chromium \) está disponível, incluindo Windows 7, Windows 10 e macOS.  Outros benefícios incluem:  

*   Os aplicativos podem ser instalados diretamente no navegador pelo ícone de **instalação** na barra de navegação.  
    
    ![Instalar submenu e ícone do aplicativo][ImageInstallPwa]  
    
*   Os aplicativos também podem ser instalados, executados e gerenciados no menu **configurações**de  >  **aplicativos**  
    
    ![Itens de menu do aplicativo em configurações][ImageAppMenus]  

*   As notificações da Web são integradas ao sistema de notificação do Windows
*   Repositório de cookies compartilhados com o perfil do navegador que instalou o aplicativo
*   Acesso a outros recursos do navegador por meio do `...` menu, incluindo a validação do certificado, as permissões de site, a proteção de rastreamento e as extensões do navegador
*   Acesso total ao [Microsoft Edge devtools][DevtoolsProgressiveWebApps] para depurar seu aplicativo  

> [!IMPORTANT]
> Para personalizar o PWAs especificamente para o Windows 10 que faz solicitações de API do WinRT usando JavaScript, consulte a [documentação específica para os recursos do PWA do EdgeHTML][PwaEdgehtmlIndex].  Saiba mais sobre como testar o PWA no Windows 10 e distribuí-lo na Microsoft Store.  

> [!NOTE]
> Confira a [sessão Build 2020 PWA][BuildVideo] para obter uma visão geral dos benefícios do PWA, recursos futuros e demonstrações curtas. 

## Requisitos  

Para ser executado como um PWA, seu aplicativo Web hospedado no servidor deve incluir os requisitos mínimos a seguir.  

| Requisito | Detalhes | 
|:--- |:--- |  
| [HTTPS][WikiHttps] | Proteja seus usuários fornecendo uma conexão segura para comunicação do servidor ou do aplicativo.  Os funcionários do serviço e outras tecnologias do PWA só funcionam com recursos da Web servidos por meio de uma conexão segura \ (ou de `localhost` para fins de depuração \).  |  
| [Profissionais de Serviço][MDNServiceWorkerApi] | Use threads de trabalho do serviço para atuar como proxies de rede entre o aplicativo cliente e servidor para fornecer suporte offline, armazenamento em cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de perf de carregamento de página.  |  
| [Manifesto do aplicativo Web][MDNWebAppManifest] | Forneça um arquivo de metadados baseado em JSON que descreve as principais informações sobre o seu aplicativo Web \ (como ícones, idioma e ponto de entrada de URL \), para que o Windows 10 e outras plataformas de host possam fornecer aos usuários do PWA uma experiência instalável e parecida com o aplicativo nativo.  |  

Para ser um grande PWA, seu aplicativo também deve atender aos seguintes requisitos.  

| Requisito | Detalhes | 
|:--- |:--- |  
| [Compatibilidade entre navegadores][MDNCrossBrowserTesting] | Certifique-se de que o PWA funcione [testando][MicrosoftDeveloperEdgeToolsRemote] em diferentes navegadores e ambientes.  |  
| [Design dinâmico][WikiResponsiveWebDesign] | Empregue layouts fluidos e imagens flexíveis com [grade][MDNCssGridLayout]CSS, [flexbox][MDNCssFlexibleBoxLayout], [grade][MDNCssGridLayout] CSS e [flexbox][MDNCssFlexibleBoxLayout] , [consultas de mídia][MDNMediaQueries]e [imagens responsivas][MDNResponsiveImages] para adaptar sua experiência ao dispositivo do usuário.  Use [ferramentas de emulação de dispositivo][DevToolsGuide|::ref1::|] do seu navegador para testar localmente ou configure uma [sessão de depuração remota][DevToolsProtocolClientsEdgeDevToolsPreview] para testar diretamente um dispositivo de destino.  |  
| [Vinculação profunda][WikiDeepLinking] | Encaminhar cada página do seu site para um URL exclusivo para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.  |  
| [Práticas recomendadas][Webhint] | Use ferramentas de qualidade de código como o [webhint][Webhint] para otimizar a eficiência, a robustez, a segurança e a acessibilidade do seu aplicativo.  |  
| [Lista de verificação do Chromium PWA][WebDevGoodPwaChecklist] | Verifique seu PWA em relação à lista de verificação do Google Baseline PWA.  |  

Se você quiser transformar o PWA em um aplicativo da [Microsoft Store][MicrosoftDeveloperStore] , vá para a documentação dos [aplicativos Web progressivos (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .  
  

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

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "O que faz um bom aplicativo Web progressivo? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculação profunda-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Design da Web responsivo-Wikipédia"  
