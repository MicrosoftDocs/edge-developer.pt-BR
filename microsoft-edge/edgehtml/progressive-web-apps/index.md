---
description: Aplicativos Web progressivos são executados nativamente no Windows 10.  Aqui está tudo o que você precisa saber como desenvolvedor da Web.
title: Aplicativos de web progressivos (EdgeHTML) no Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 87996f6be7c1963c01a476b307a31e689e3880d4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231616"
---
# Aplicativos de web progressivos (EdgeHTML) no Windows  

Com os [aplicativos Web progressivos][MDNApps] \ (ou simplesmente PWAs \), você não precisa decidir entre usar tecnologias abertas da Web para interoperabilidade entre plataformas e fornecer aos usuários uma experiência do tipo de aplicativo nativo personalizada para seus dispositivos.  Isso ocorre porque PWAs são apenas sites que são [progressivamente aprimorados][AListApartUnderstandingProgressiveEnhancement] para funcionar como aplicativos nativos em plataformas de suporte.  As qualidades de um PWA combinam o melhor dos aplicativos Web e nativos.  

:::row:::
    :::column:::
        ![Ícone detectável][ImageISearch]
        ### [Detectáveis][MDNPwaAdvantagesDiscoverable]
        Nos resultados da pesquisa na Web e nos repositórios de aplicativos de suporte
    :::column-end:::
    :::column:::
        ![Ícone instalável][ImageIPackage]
        ### [Instaláveis][MDNPwaAdvantagesInstallable]
        Fixar e iniciar na tela inicial  
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
        Dimensionamento de experiência \ (para cima ou para baixo \) com recursos de dispositivo  
    :::column-end:::
    :::column:::
        ![Ícone de segurança][ImageISecurity]
        ### [Desligar][MDNPwaAdvantagesSafe]
        Fornece um ponto de extremidade HTTPS seguro e outras proteções de usuário  
    :::column-end:::
    :::column:::
        ![Ícone responsivo][ImageIResponsive]
        ### [Responsivo][MDNPwaAdvantagesResponsive]
        Adapta-se ao tamanho/orientação de tela e método de entrada do usuário  
    :::column-end:::
    :::column:::
        ![Ícone vinculável][ImageILink]
        ### [Vinculável][MDNPwaAdvantagesLinkable]
        Compartilhar e iniciar a partir de um hiperlink padrão  
    :::column-end:::
:::row-end:::

Ao criar ou converter seu site existente em um PWA, você poderá se envolver melhor em seu público-alvo existente com notificações por push e suporte offline.  Ao mesmo tempo, você pode continuar a criar seu público-alvo na Web em aberto, pois os usuários detectam o PWA por meio de pesquisa e compartilhamento de links.  

## PWAs no Windows 10 (EdgeHTML)  

> [!NOTE]
> Com o mover para o Microsoft Edge (Chromium) do EdgeHTML, as plataformas da Web subjacentes usadas pelo PWAs não são iguais.  Edge (Chromium) PWAs são instalados e executados no navegador.  Edge (EdgeHTML) PWAs executar como aplicativos da plataforma universal do Windows (UWP) e usar a plataforma da Web EdgeHTML mais antiga.  Se você precisar ter acesso à API do Windows 10 para seu PWA, esta documentação do EdgeHTML é para você.  Se o seu objetivo for suporte a várias plataformas sem acesso à API específico do Windows, vá para a [documentação do PWA do Microsoft Edge (Chromium)][PwaChromiumIndex].  

Quando você cria um aplicativo Web progressivo para aproveitar o Windows 10, é possível distribuir o PWA por meio da [Microsoft Store][MicrosoftDeveloperStore], toda a base de instalação do Windows 10 de 600 milhões de usuários ativos mensais é o seu potencial público de aplicativos!  Os aplicativos desenvolvidos dessa maneira são executados como aplicativos da [plataforma universal do Windows][WindowsUWPGetStartedGuide] e têm acesso nativo às APIs do WinRT.  Observe que a plataforma da Web que renderiza seu código é EdgeHTML ao usar as APIs do WinRT, portanto, use a detecção de recurso antes de chamar qualquer uma das APIs específicas do Windows para garantir que o PWA ainda seja capaz de ser executado entre plataformas nas quais o PWAs do Microsoft Edge \ (Chromium \) esteja disponível.  

[Veja como começar][PwaEdgehtmlGetStarted] a converter seu aplicativo Web em um PWA \ (EdgeHTML \), testá-lo no Windows 10 e distribuí-lo na Microsoft Store.  

## Requisitos  

Para executar como um PWA, seu aplicativo Web hospedado no servidor pelo menos exige:  

*   [Https][WikiHttps].  Proteja seus usuários fornecendo uma conexão segura para comunicação de servidor/aplicativo.  Os funcionários do serviço e outras tecnologias do PWA só funcionam com recursos da Web servidos por meio de uma conexão segura \ (ou de `localhost` para fins de depuração \).  
  
*   [Trabalhadores do serviço][MDNServiceWorkerApi].  Use threads de trabalho do serviço para atuar como proxies de rede entre o aplicativo cliente e servidor para fornecer suporte offline, armazenamento em cache de recursos, notificações por push, sincronização de dados em segundo plano e otimizações de perf de carregamento de página.  

*   [Manifesto do aplicativo Web][MDNWebAppManifest].  Forneça um arquivo de metadados baseado em JSON que descreve as principais informações sobre o seu aplicativo Web \ (como ícones, idioma e ponto de entrada de URL \) para que o Windows 10 e outras plataformas de host possam fornecer aos usuários do PWA uma experiência instalável e parecida com o aplicativo nativo.  Associar seu site a um manifesto do aplicativo Web faz com que ele seja qualificado para [inclusão automática na Microsoft Store][PwaEdgehtmlMicrosoftStoreImportingBing] por meio do serviço de indexação do Bing.  

Para ser um grande PWA, seu aplicativo também precisa de:  

*   [Compatibilidade com vários navegadores][MDNCrossBrowserTesting].  Certifique-se de que o PWA funcione [testando][MicrosoftDeveloperEdgeToolsRemote] em diferentes navegadores e ambientes.  No Windows 10, certifique-se de testar seu aplicativo no navegador Microsoft Edge e também na experiência completa do PWA: como um aplicativo autônomo do Windows 10 instalado \ (da plataforma do mecanismo EdgeHTML \).  
  
*   [Design responsivo][WikiResponsiveWebDesign].  Empregue layouts fluidos e imagens flexíveis com [grade][MDNCssGridLayout] CSS e/ou [flexbox][MDNCssFlexibleBoxLayout], [consultas de mídia][MDNMediaQueries]e [[MDNResponsiveImages] de imagens responsivas para adaptar seu UX ao dispositivo do usuário.  Use [ferramentas de emulação][DevToolsGuideEmulation] de dispositivo do seu navegador para testar localmente ou configure uma [sessão de depuração remota][DevToolsProtocolClientsEdgeDevToolsPreview] para testar diretamente um dispositivo de destino.  No Windows 10, PWAs \ (EdgeHTML \) também podem ser [adaptados para fatores formados][WindowsUWPDesignDevicesIndex] além da área de trabalho, telefone e Tablet, incluindo: [Xbox e TV][WindowsUWPDesignDevicesDesigningTv], [Surface Hub][MicrosoftDeveloperWindowsSurfaceHub]e dispositivos [Windows Mixed Reality][MicrosoftDeveloperWindowsMixedReality] .  
  
*   [Vinculação profunda][WikiDeepLinking].  Encaminhar cada página do seu site para um URL exclusivo para que os usuários existentes possam ajudá-lo a envolver um público ainda mais amplo por meio do compartilhamento de mídia social.  

*   [Práticas recomendadas][Webhint].  Use ferramentas de qualidade de código como o [webhint][Webhint] para otimizar a eficiência, a robustez, a segurança e a acessibilidade do seu aplicativo.  

Para enviar seu aplicativo Web progressivo para a [Microsoft Store][MicrosoftDeveloperStore], você deve ter:  

*   Uma [conta de desenvolvedor da Microsoft][WindowsUWPPublishDeveloperAccount]  
*   Etapas concluídas [para publicar um aplicativo do Windows][WindowsUWPPublishIndex]  

Nos próximos meses, a PWAs existente nos [critérios específicos][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] de reunião na Web são indexadas automaticamente pelo mecanismo de pesquisa do Bing na Microsoft Store \ (em que os desenvolvedores podem gerenciá-los diretamente para a sua audiência \) do Windows 10.  

Confira [o PWAs (EdgeHTML) na Microsoft Store][PwaEdgehtmlMicrosoftStore] para obter mais detalhes.  

## Disponibilidade atual  

Suporte ao mecanismo de navegador para chamadas de aplicativos Web progressivos para vários componentes arquitetônicos, o mais significativo sendo a infraestrutura de rede subjacente à [API de busca][MDNFetchApi].  O suporte do PWA no mecanismo EdgeHTML foi concluído na versão do Windows 10 1809.  Outros aprimoramentos nos padrões da Web desde que esse tempo não sejam incorporados ao mecanismo EdgeHTML, portanto, certifique-se de executar testes de compatibilidade e usar a detecção de recursos para fallbacks, caso o recurso que seu PWA precisa não seja compatível com a plataforma EdgeHTML.  

Para o próximo lançamento do Microsoft Edge \ (Chromium \) no 2020, a plataforma do navegador tem suporte completo para esses recursos que trabalham entre dispositivos nos quais o navegador Chromium é compatível.  

Para o EdgeHTML e o Windows, este é o status atual das tecnologias do PWA baseadas em padrões:  

| Tecnologia | Finalidade | Disponibilidade | Observações de uso |  
|:--- |:--- |:--- |:--- |  
| [Manifesto de aplicativo Web][MDNWebAppManifest] | Fornece metadados do aplicativo para o sistema operacional host para habilitar a promoção de instalação e da loja de aplicativos.  Obrigatório para PWAs na Microsoft Store.  | [Em desenvolvimento][MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest] | Por enquanto, você pode usar o [construtor do PWA][|::ref1::|] para gerar um manifesto JSON compatível com W3C e empacotar o aplicativo para várias plataformas do sistema operacional.  Para Windows, o construtor do PWA traduz o manifesto JSON para o `.appxmanifest` formato \ (XML \) exigido pelos aplicativos do Windows 10.  |  
| [API de busca][MDNFetchApi] | Fornece redes assíncronas \ (solicitações, respostas \) para recursos de página |[EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /Build 14393 + | A sintaxe da [API do serviço de trabalho][MDNServiceWorkerApi] é baseada em APIs de rede com base em busca.  Você também pode usar a [API FETCH][MDNFetchApi] mais geralmente como uma alternativa moderna para `XMLHttpRequest` .  |  
| [API de trabalho do serviço][MDNServiceWorkerApi] | Fornece um proxy de rede/modelo de aplicativo Web compatível com offline, no qual scripts orientados por eventos são executados independentemente das páginas da Web  | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Suporte experimental \ (atrás `Enable Service Workers` do sinalizador \) fornecido no EdgeHTML 16.  Ativado por padrão em EdgeHTML de 17 + Builds.  |  
| [API do cache][MDNCache] | Fornece um mecanismo de armazenamento para pares de solicitação/resposta de rede | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Consulte observação sobre a [API de trabalho do serviço][MDNServiceWorkerApi] acima.  |  
| [API push][MDNPushApi] | Permite que um trabalhador de serviço assine notificações por push |[EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 +| Consulte observação sobre a [API de trabalho do serviço][MDNServiceWorkerApi] acima.  Os aplicativos do Windows 10 (incluindo PWAs \) exigem que o [serviço de notificação por push do Windows \ (WNS \)][WindowsUWPControlsPatternTilesNotificationsWns] forneçam notificações por push, que dão suporte à [API de push][MDNPushApi]W3C.  |  
| [API de notificações][MDNNotificationsApi] | Permite que um trabalhador de serviço exiba uma notificação do sistema para o usuário após a mensagem de chat | [EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /Build 14393 + | As notificações da Web no EdgeHTML são totalmente integradas à [central de ações][MicrosoftSupportWindowsNotificationSettings]do Windows 10, em que os usuários podem gerenciar as notificações do aplicativo e definir as [horas de silêncio][MicrosoftSupportWindowsFocusAssist].  |  
| [API de sincronização em segundo plano][MDNSyncManager] | Fornece uma API para notificar um trabalhador de serviço que o usuário voltou a ficar online e para agendar eventos periódicos para sincronizar dados locais com o servidor | [Em desenvolvimento][MicrosoftDeveloperEdgePlatformStatusBackgroundSync] | Por enquanto, você pode usar a [API BackgroundTask do WinRT][WindowsUWPLaunchResumeBackgroundTasks] nativa para implementar tarefas em segundo plano para o seu PWA quando ele é executado como um aplicativo do Windows 10.  |  

Aqui está o status atual do suporte do Microsoft Store para PWAs no Windows 10:  

| Método de envio da loja | Status | Detalhes |  
|:--- |:--- |:--- |  
| Manual \ (desenvolvedor iniciado \) | Disponível | Confira [o PWAs (EdgeHTML) na Microsoft Store][PwaEdgehtmlMicrosoftStore] para começar.  |  
| Automática \ (indexado automaticamente com o Bing \) | Em breve | [No momento, estamos conduzindo][WindowsBlogsWelcomingPWAsEdgeWindows] o processo de integração do PWA com um subconjunto limitado de parceiros de aplicativo.  Nos próximos meses, a Microsoft bem-vindo bem-vindo ao PWAs na Web, a Microsoft Store.  Confira [importação automática do PWA com o Bing][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] para saber mais sobre os requisitos da Microsoft Store para listagens do PWA geradas automaticamente.  |  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview-DevTools de protocolo dos clientes | Documentos da Microsoft"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Emulação | Documentos da Microsoft"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Novidades do EdgeHTML 17 | Documentos da Microsoft"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "O que há de novo no EdgeHTML 14 | Documentos da Microsoft"  
[PwaChromiumIndex]: ../../progressive-web-apps-chromium/index.md "Aplicativos Web progressivos (Chromium) no Windows | Documentos da Microsoft"  
[PwaEdgehtmlGetStarted]: ../progressive-web-apps/get-started.md "Introdução aos aplicativos Web progressivos (EdgeHTML) | Documentos da Microsoft"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Aplicativos Web progressivos na Microsoft Store | Documentos da Microsoft"
[PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Critérios para envio automático-aplicativos Web progressivos na Microsoft Store | Documentos da Microsoft"  
[PwaEdgehtmlMicrosoftStoreImportingBing]: ./microsoft-store.md#automatic-pwa-importing-with-bing "Importação automática do PWA com o Bing-Web Apps progressivos (EdgeHTML) na Microsoft Store | Documentos da Microsoft"  


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
[]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Imagens responsivas MDNResponsiveImages | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do aplicativo Web | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Vinculação profunda-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Design da Web responsivo-Wikipédia"  
