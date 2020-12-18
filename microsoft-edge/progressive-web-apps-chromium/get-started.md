---
description: Este guia fornece uma visão geral das ferramentas e noções básicas do PWA para criar aplicativos Web progressivos (Chromium) no Windows.
title: Introdução aos aplicativos Web progressivos (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, PWABuilder, Web manifest, trabalho de serviço, push
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231220"
---
# Introdução aos aplicativos Web progressivos (Chromium)  

Aplicativos Web progressivos \ (PWAs \) são aplicativos Web que são [aprimorados progressivamente][WikiProgressiveEnhancement].  Os aprimoramentos progressivos incluem recursos semelhantes a aplicativos, como instalação, suporte offline e notificações por push.  Você também pode empacotar seu PWA para repositórios de aplicativos.  Possíveis repositórios de aplicativos incluem a Microsoft Store, Google Play, Mac App Store e muito mais.  A Microsoft Store é a loja de aplicativos comerciais interna do Windows 10.  

O guia a seguir fornece uma visão geral das noções básicas do PWA ao criar um aplicativo Web simples e prorroga-lo como PWA.  O projeto concluído funciona em navegadores modernos.  

> [!TIP]
> Você pode usar o [PWABuilder][PwaBuilder] para criar um novo PWA, aprimorar o PWA existente ou empacotar seu PWA para repositórios de aplicativos.  

## Pré-requisitos  

*   Use o [código do Visual Studio][VisualstudioCodeMain] para editar o código-fonte do PWA.  
*   Use [Node.js][NodejsMain] como seu servidor Web local.  
    
## Criar um aplicativo Web básico  

Para criar um aplicativo Web vazio, siga as etapas no [aplicativo nó Express app Generator][ExpressjsApplicationGenerator]e nomeie seu aplicativo `MySamplePwa` .  

No prompt, execute os comandos a seguir.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Os comandos criam um aplicativo Web vazio e instalam as dependências.  

Agora você tem um aplicativo Web funcional simples.  Para iniciar seu aplicativo Web, execute o seguinte comando.  

```shell
npm start
```  

Agora, navegue até `http://localhost:3000` para exibir seu novo aplicativo Web.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Executando seu novo PWA no localhost" lightbox="./media/vs-nodejs-express-index.png":::
   Executando seu novo PWA no localhost
:::image-end:::

## Começar a criar um PWA  

Agora que você tem um aplicativo Web simples, estenda-o como um PWA adicionando os três requisitos para PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), um [manifesto do aplicativo Web](#step-2---create-a-web-app-manifest)e um [trabalho de serviço](#step-3---add-a-service-worker).  

### Etapa 1: usar HTTPS  

As principais partes da plataforma PWA, como [funcionários de serviço][MDNServiceWorkerApi], exigem o uso de HTTPS.  Quando o seu PWA ficar ao vivo, você deverá publicá-lo em uma URL HTTPS.  

Para fins de depuração, o Microsoft Edge também permite `http://localhost` usar as APIs do PWA.  

[Publicar seu aplicativo Web como um site ativo][VisualStudioNodejsTutorialPublishAzureAppService], mas verifique se o servidor está configurado para https.  Por exemplo, você pode criar uma [conta do Azure grátis][AzureCreateFreeAccount].  Hospede seu site no [serviço de aplicativo do Microsoft Azure][AzureWebApps] e ele é servido por HTTPS por padrão.  

O guia a seguir, use `http://localhost` para criar seu PWA.  

### Etapa 2-criar um manifesto do aplicativo Web  

Um [manifesto do aplicativo Web][MDNWebAppManifest] é um arquivo JSON que contém metadados sobre o seu aplicativo, como nome, descrição, ícones e muito mais.  

Para adicionar um manifesto do aplicativo ao aplicativo Web:  

1.  No código do Visual Studio, escolha **arquivo**  >  **abrir pasta** e escolha o `MySamplePwa` diretório que você criou anteriormente.  
1.  Selecione `Ctrl` + `N` para criar um novo arquivo e cole no trecho de código a seguir.  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  Salve o arquivo como `/MySamplePwa/public/manifest.json` .  
1.  Adicione uma imagem do ícone do aplicativo 512x512 chamado `icon512.png` to `/MySamplePwa/public/images` .  Você pode usar a [imagem de exemplo][ImagePwa] para fins de teste.  
1.  No código do Visual Studio, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Etapa 3: adicionar um trabalhador de serviço  

Os funcionários de serviço são a tecnologia principal por trás do PWAs, permitindo cenários como suporte offline, cache avançado e executar tarefas em segundo plano anteriormente limitadas a aplicativos nativos.  

Os funcionários de serviço são tarefas em segundo plano que interceptam solicitações de rede de seu aplicativo Web.  Os funcionários do serviço tentam concluir as tarefas, mesmo quando o seu PWA não está em execução.  As tarefas incluem as ações a seguir.  

*   Servindo os recursos solicitados de um cache  
*   Enviar notificações por push  
*   Executar tarefas de busca em segundo plano  
*   Ícones de selos  
*   e muito mais  
    
Os funcionários do serviço são definidos em um arquivo JavaScript especial.  Para obter mais informações, navegue para [usando trabalhadores do serviço][MDNUsingServiceWorkers] e a [API do serviço de trabalho][MDNServiceWorkerApi].  

Para criar um trabalho de serviço em seu projeto, use a primeira receita do trabalho do serviço de **rede cache** do [PWA Builder][PwaBuilderServiceWorker].  

1.  Navegue até [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], selecione o trabalho do primeiro serviço de **rede em cache** e selecione o botão **baixar** .  O arquivo baixado contém os seguintes arquivos:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Copie os arquivos baixados para a `public` pasta no seu projeto de aplicativo Web.  
1.  No código do Visual Studio, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Seu aplicativo Web agora tem um trabalho de serviço que usa a primeira estratégia cache.  O novo trabalho de serviço busca recursos do cache primeiro e da rede apenas conforme necessário.  Os recursos armazenados em cache incluem imagens, JavaScript, CSS e HTML.

Use as etapas a seguir para confirmar a execução do trabalho do serviço.  

1.  Navegue até seu aplicativo Web usando `http://localhost:3000` .  Se o seu aplicativo Web não estiver disponível, execute o seguinte comando.   
    
    ```shell
    npm start
    ```
    
1.  No Microsoft Edge, selecione `F12` para abrir o Microsoft Edge devtools.  Selecione **aplicativo**e, em seguida, selecione os **funcionários** do serviço para exibir os funcionários do serviço.  Se o trabalhador do serviço não for exibido, atualize a página.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Visão geral do trabalhador do serviço Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       Visão geral do trabalhador do serviço Microsoft Edge DevTools
    :::image-end:::
    
1.  Exiba o cache do serviço de trabalho expandindo o **armazenamento de cache** e selecione **pwabuilder-cache**.  Todos os recursos armazenados em cache pelo trabalhador do serviço devem ser exibidos.  Os recursos armazenados em cache pelo trabalhador do serviço incluem o ícone do aplicativo, manifesto do aplicativo, CSS e arquivos JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache do trabalho do serviço no Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Cache do trabalho do serviço no Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Experimente o seu PWA como um aplicativo offline.  No Microsoft Edge DevTools \ ( `F12` \), escolha **rede** e altere o status **online** para **offline**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Configurando o aplicativo para o modo offline no Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Configurando o aplicativo para o modo offline no Microsoft Edge DevTools
    :::image-end:::
    
1.  Atualize seu aplicativo e ele deve exibir o mecanismo offline para servir os recursos de seu aplicativo a partir do cache.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA em execução offline" lightbox="./media/vs-nodejs-express-index.png":::
       PWA em execução offline
    :::image-end:::
    
## Adicionar notificações por push ao seu PWA  

Você pode criar PWAs que dão suporte a notificações por push completando as seguintes tarefas.  

1.  Assinar um serviço de mensagens usando a [API de envio][MDNPushApi]  
1.  Exibir uma mensagem de notificação do sistema quando uma mensagem é recebida do serviço usando a [API de notificações][MDNNotificationsApi]  
    
Assim como acontece com trabalhadores de serviço, as APIs de notificação por push são APIs baseadas em padrões.  As APIs de notificação por push funcionam entre navegadores, portanto, o código deve funcionar em qualquer lugar no qual o PWAs for compatível.  Para obter mais informações sobre como enviar mensagens push para navegadores diferentes em seu servidor, navegue até [Internet-Push][NPMWebPush].  

As etapas a seguir foram adaptadas da demonstração avançada push no [livro do serviço de trabalho][ServiceWorkerCookbookPushRichDemo] do entanto, que tem uma série de outras receitas úteis de trabalho de serviço e envio da Web.  

### Etapa 1-gerar chaves VAPID  

As notificações por push exigem chaves VAPID \ (identificação do servidor de aplicativos voluntários \) para enviar mensagens de envio para o cliente PWA.  Há vários geradores de chave VAPID disponíveis online \ (por exemplo, [vapidkeys.com][VapidkeysMain]\).  Após a geração, você deve obter um objeto JSON que contém uma chave pública e privada.  Salve as chaves para etapas posteriores do tutorial a seguir.  Para obter informações sobre o VAPID e o webpush, navegue para [Enviar VAPID notificações webpush identificadas usando o serviço de envio do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Etapa 2-assinar notificações por push  

Os funcionários de serviço lidam com eventos de push e interações de notificação do sistema no seu PWA.  Para assinar o PWA para notificações por push de servidor, verifique se as seguintes condições foram atendidas.  

*   Seu PWA está instalado, ativo e cadastrado  
*   Seu código para concluir a tarefa de assinatura está no thread da interface do usuário principal do PWA  
*   Você tem conectividade de rede  
    
Antes da criação de uma nova assinatura de envio, o Microsoft Edge verifica se o usuário concedeu permissão ao PWA para receber notificações.  Caso contrário, o usuário será solicitado a confirmar a permissão do navegador.  Se a permissão for negada, a solicitação para `registration.pushManager.subscribe` lançar uma `DOMException` , que deve ser manipulada.  Para saber mais sobre o gerenciamento de permissões, navegue até [notificações por push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Em seu `pwabuilder-sw-register.js` arquivo, acrescente o trecho de código a seguir.  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
                });
            });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

Para obter mais informações, navegue até o [pushmanager][MDNPushManager] e [com a Web-Push][NPMWebPushUsage].  

### Etapa 3-ouvir as notificações por push  

Após a criação de uma assinatura no PWA, adicione manipuladores ao trabalhador do serviço para responder a eventos de envio.  O evento Push é enviado do servidor para exibir notificações do sistema.  Notificações do sistema exibem dados de uma mensagem recebida.  Para concluir as tarefas a seguir, você deve adicionar um manipulador de clique.  

*   Ignorar a notificação do sistema  
*   Abrir, focalizar ou abrir e focalizar qualquer janelas abertas  
*   Abrir e focalizar uma nova janela para exibir uma página do cliente PWA  
    
Em seu `pwabuilder-sw.js` arquivo, adicione os manipuladores a seguir.  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### Etapa 4-experimentar  

Para testar as notificações por push do seu PWA, conclua as etapas a seguir.  

1.  Navegue até o seu PWA em `http://localhost:3000` .  Quando o trabalhador do serviço é ativado e tenta assinar notificações por push pelo PWA, o Microsoft Edge solicita que o seu PWA mostre notificações.  Selecione **permitir**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Caixa de diálogo de permissão para habilitar notificações" lightbox="./media/notification-permission.png":::
       Caixa de diálogo de permissão para habilitar notificações
    :::image-end:::
    
1.  Simule uma notificação por push do lado do servidor.  Com o seu PWA aberto em `http://localhost:3000` no navegador, selecione `F12` para abrir o devtools.  Escolha ****  >  ****  >  **envio** de trabalhador de serviço de aplicativo para enviar uma notificação por push de teste ao seu PWA.  
    
    :::row:::
       :::column span="":::
          Uma notificação por push deve ser exibida perto da barra de tarefas.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Enviar uma notificação por push de DevTools" lightbox="./media/devtools-push.png":::
             Enviar uma notificação por push de DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Se você não selecionar \ (ou ativar \) uma notificação do sistema, o sistema a descartará automaticamente após vários segundos e a enfileirará na sua central de ações do Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificações na central de ações do Windows" lightbox="./media/windows-action-center.png":::
             Notificações na central de ações do Windows :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## Próximas etapas  

As etapas a seguir incluem tarefas adicionais para ajudá-lo a entender a criação de PWAss do mundo real.  

*   Gerenciar e armazenar assinaturas push  
*   [Criptografar][NPMWebPushEncrypt] dados de carga  
*   Design dinâmico  
*   Vinculação profunda  
*   [Teste entre navegadores][BrowserStackTestEdgeBrowser]  
*   Implementar práticas de validação e teste, como [webhint][Webhint]  
    
## Consulte também  

*   [Aplicativos Web progressivos em documentos da Web do MDN][MDNProgressiveWebApps]  
*   [Aplicativos Web progressivos em Web. dev][WebDevProgressiveWebApps]  
*   [Leitores de notícias de hackers como Web Apps progressivos][HackerNewsProgressiveWebApps] – compara estruturas e padrões de desempenho diferentes para implementar uma amostra \ (leitor de notícias de hackers \) PWA.  
*   [Myth de PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Um roteiro progressivo para seu aplicativo Web progressivo][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Postagens offline com Web Apps progressivos][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [&DO PWA P A][AaronGustafsonNotebookPwaQa]  
*   [Aposta na Web][JoretegBlogBettingWeb]  
*   [Nomeando aplicativos Web progressivos][Fberriman20170626NamingProgressiveWebApps]  
*   [Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implantar um aplicativo Node.js no Azure com código do Visual Studio | Documentos da Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Criar conta gratuita do Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicativos Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificações da Web no Microsoft Edge | Blogs do Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "&DO PWA P A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste gratuito do navegador Microsoft Edge no Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Um roteiro progressivo para seu aplicativo Web progressivo"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Myth de PWAs – o novo Edge Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Gerador de aplicativos expressos | Expresso" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Nomeando aplicativos Web progressivos"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Leitores de notícias de hackers como Web Apps progressivos"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Aposta na Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificações | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicativos Web progressivos \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabalhadores de serviço | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do aplicativo Web | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Postagens offline com Web Apps progressivos"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Enviar notificações webpush identificadas pela VAPID por meio do serviço de envio do Mozilla | Serviços do Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "por push na Web | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "criptografar (userpublickey, userauth, Payload, contentEncoding)-envio pela Web | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso-Push-Web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicativos Web progressivos"  

[PwaBuilder]: https://www.pwabuilder.com "Construtor do PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Trabalhador do serviço | Construtor do PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Demonstração avançada push | Cookbook do inworkr"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 3)"  

[VapidkeysMain]: https://vapidkeys.com "Gerador de chave de VAPID seguro | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicativos Web progressivos | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Aperfeiçoamento progressivo | Wikipédia"  
