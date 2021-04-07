---
description: Este guia fornece uma visão geral das noções básicas e ferramentas do PWA para a criação de Aplicativos Web Progressivos (Chromium) no Windows.
title: Começar com o Progressive Web Apps (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Borda, Windows, PWABuilder, manifesto da Web, serviço de trabalho, push
ms.openlocfilehash: 3023c38790185ca6989f4a487928abc79b1d5a2c
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480192"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a>Começar com o Progressive Web Apps (Chromium)  

Os Aplicativos Web Progressivos \(PWAs\) são aplicativos Web que são [progressivamente aprimorados.][WikiProgressiveEnhancement]  Os aprimoramentos progressivos incluem recursos parecidos com aplicativos, como instalação, suporte offline e notificações por push.  Você também pode empacotá-lo para lojas de aplicativos.  Os possíveis armazenamentos de aplicativos incluem a Microsoft Store, Google Play, Mac App Store e muito mais.  A Microsoft Store é a loja de aplicativos comerciais criada no Windows 10.  

O guia a seguir fornece uma visão geral das noções básicas do PWA criando um aplicativo Web simples e estendendo-o como um PWA.  O projeto concluído funciona em navegadores modernos.  

> [!TIP]
> Você pode usar [o PWABuilder][PwaBuilder] para criar um novo PWA, aprimorar o PWA existente ou empacotar seu PWA para lojas de aplicativos.  

## <a name="prerequisites"></a>Pré-requisitos  

*   Use [Visual Studio Código][VisualstudioCodeMain] para editar o código-fonte do PWA.  
*   Use [Node.js][NodejsMain] como seu servidor Web local.  
    
## <a name="create-a-basic-web-app"></a>Criar um aplicativo Web básico  

Para criar um aplicativo Web vazio, siga as etapas em [Node Express App Generator][ExpressjsApplicationGenerator]e nomee seu aplicativo `MySamplePwa` .  

No prompt, execute os comandos a seguir.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Os comandos criam um aplicativo Web vazio e instalam qualquer dependência.  

Agora você tem um aplicativo Web simples e funcional.  Para iniciar seu aplicativo Web, execute o seguinte comando.  

```shell
npm start
```  

Agora, navegue `http://localhost:3000` para exibir seu novo aplicativo Web.  

:::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="Executando seu novo PWA no localhost" lightbox="./media/visual-studio-nodejs-express-index.png":::
   Executando seu novo PWA no localhost  
:::image-end:::  

## <a name="get-started-building-a-pwa"></a>Começar a criar um PWA  

Agora que você tem um aplicativo Web simples, estenda-o como um PWA adicionando os três requisitos para PWAs<!--[3 requirements for PWAs][ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]-->: [HTTPS](#step-1---use-https), um [Manifesto do Aplicativo Web](#step-2---create-a-web-app-manifest)e um Trabalhador de [Serviço.](#step-3---add-a-service-worker)  

### <a name="step-1---use-https"></a>Etapa 1 - Usar HTTPS  

As partes principais da plataforma PWA, como Os Trabalhadores [do Serviço,][MDNServiceWorkerApi]exigem o uso de HTTPS.  Quando o PWA for ao vivo, você deverá publicá-lo em uma URL HTTPS.  

Para fins de depuração, o Microsoft Edge também permite `http://localhost` usar as APIs do PWA.  

[Publique seu aplicativo Web como um site ao vivo][VisualStudioNodejsTutorialPublishAzureAppService], mas verifique se o servidor está configurado para HTTPS.  Por exemplo, você pode criar uma conta gratuita [do Azure.][AzureCreateFreeAccount]  Hospede seu site no Serviço de Aplicativo do [Microsoft Azure][AzureWebApps] e ele é servido por https por padrão.  

O guia a seguir, use `http://localhost` para criar seu PWA.  

### <a name="step-2---create-a-web-app-manifest"></a>Etapa 2 - Criar um Manifesto do Aplicativo Web  

Um [Manifesto do Aplicativo Web][MDNWebAppManifest] é um arquivo JSON que contém metadados sobre seu aplicativo, como nome, descrição, ícones e muito mais.  

Para adicionar um manifesto de aplicativo ao aplicativo Web:  

1.  Em Visual Studio Código, escolha **Arquivo**  >  **Abrir Pasta** e escolha o diretório que você criou `MySamplePwa` anteriormente.  
1.  Selecione `Ctrl` + `N` para criar um novo arquivo e colar no trecho de código a seguir.  
    
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
1.  Adicione uma imagem de ícone do aplicativo 512x512 chamada `icon512.png` `/MySamplePwa/public/images` para .  Você pode usar a [imagem de exemplo para](./media/progressive-web-app.png) fins de teste.  
1.  Em Visual Studio Código, abra e adicione o seguinte trecho de `/public/index.html` código dentro da `<head>` marca.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a>Etapa 3 - Adicionar um Trabalhador de Serviço  

Os funcionários de serviço são a principal tecnologia por trás de PWAs, habilitando cenários como suporte offline, cache avançado e executando tarefas em segundo plano anteriormente limitadas a aplicativos nativos.  

Os funcionários de serviço são tarefas em segundo plano que interceptam solicitações de rede do seu aplicativo Web.  Os funcionários de serviço tentam concluir tarefas, mesmo quando o PWA não está em execução.  As tarefas incluem as seguintes ações.  

*   Servindo recursos solicitados de um cache  
*   Enviando notificações por push  
*   Executar tarefas de busca em segundo plano  
*   Ícones de badging  
*   e mais  
    
Os funcionários de serviço são definidos em um arquivo JavaScript especial.  Para obter mais informações, navegue até [Using Service Workers][MDNUsingServiceWorkers] and Service Worker [API][MDNServiceWorkerApi].  

Para criar um funcionário de serviço em seu projeto, use a receita de trabalho de serviço de rede do **PWA** [Builder][PwaBuilderServiceWorker].  

1.  Navegue [até pwabuilder.com/serviceworker][PwaBuilderServiceWorker], selecione o serviço de rede de cache **primeiro** e selecione o **botão Baixar.**  O arquivo baixado contém os seguintes arquivos:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Copie os arquivos baixados para a `public` pasta no projeto do aplicativo Web.  
1.  Em Visual Studio Código, abra e adicione o seguinte trecho de `/public/index.html` código dentro da `<head>` marca.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Seu aplicativo Web agora tem um trabalhador de serviço que usa a estratégia de cache primeiro.  Você novo funcionário de serviço busca recursos do cache primeiro e da rede apenas conforme necessário.  Os recursos armazenados em cache incluem imagens, JavaScript, CSS e HTML.

Use as etapas a seguir para confirmar se o seu funcionário de serviço é executado.  

1.  Navegue até seu aplicativo Web usando `http://localhost:3000` .  Se seu aplicativo Web não estiver disponível, execute o seguinte comando.   
    
    ```shell
    npm start
    ```
    
1.  No Microsoft Edge, selecione `F12` para abrir o Microsoft Edge DevTools.  Selecione **Aplicativo**, em **seguida, Service Workers** para exibir os funcionários do serviço.  Se o trabalhador do serviço não for exibido, atualize a página.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Visão geral do Microsoft Edge DevTools Service Worker" lightbox="./media/devtools-sw-overview.png":::
       Visão geral do Microsoft Edge DevTools Service Worker  
    :::image-end:::  
    
1.  Exibir o cache do trabalhador de serviço expandindo **o Armazenamento de Cache** e selecione **pwabuilder-precache**.  Todos os recursos armazenados em cache pelo trabalhador do serviço devem ser exibidos.  Os recursos armazenados em cache pelo trabalhador do serviço incluem o ícone do aplicativo, o manifesto do aplicativo, o CSS e os arquivos JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache de Trabalhador de Serviço no Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Cache de Trabalhador de Serviço no Microsoft Edge DevTools \(F12\)  
    :::image-end:::  
    
1.  Experimente o PWA como um aplicativo offline.  No Microsoft Edge DevTools \( `F12` \), escolha **Rede** e altere o status **online** para **Offline**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Configurando o aplicativo para o modo offline no Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Configurando o aplicativo para o modo offline no Microsoft Edge DevTools  
    :::image-end:::  
    
1.  Atualize seu aplicativo e ele deve exibir o mecanismo offline para servir os recursos do seu aplicativo a partir do cache.  
    
    :::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="PWA em execução offline" lightbox="./media/visual-studio-nodejs-express-index.png":::
       PWA em execução offline  
    :::image-end:::  
    
## <a name="add-push-notifications-to-your-pwa"></a>Adicionar notificações por push ao seu PWA  

Você pode criar PWAs que suportam notificações por push concluindo as seguintes tarefas.  

1.  Inscrever-se em um serviço de mensagens usando a [API push][MDNPushApi]  
1.  Exibir uma mensagem de notificação quando uma mensagem é recebida do serviço usando a [API de Notificações][MDNNotificationsApi]  
    
Assim como com Os Trabalhadores do Serviço, as APIs de notificação por push são APIs baseadas em padrões.  As APIs de notificação por push funcionam em navegadores, portanto, seu código deve funcionar em todos os lugares com suporte para PWAs.  Para obter mais informações sobre como entregar mensagens push para diferentes navegadores em seu servidor, navegue até [Web-Push][NPMWebPush].  

As etapas a seguir foram adaptadas do Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] fornecido pelo Mozilla, que tem várias outras receitas úteis de Web Push e de trabalho de serviço.  

### <a name="step-1---generate-vapid-keys"></a>Etapa 1 - Gerar chaves VAPID  

As notificações por push exigem teclas VAPID \(Voluntary Application Server Identification\) para enviar mensagens push ao cliente PWA.  Há vários geradores de chaves VAPID disponíveis online \(por exemplo, [vapidkeys.com][VapidkeysMain]\).  Após a geração, você deve obter um objeto JSON contendo uma chave pública e privada.  Salve as chaves para etapas posteriores no tutorial a seguir.  Para obter informações sobre VAPID e WebPush, navegue até Enviar notificações de [WebPush identificadas vapid usando o Serviço de Push do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### <a name="step-2---subscribe-to-push-notifications"></a>Etapa 2 - Inscrever-se em notificações por push  

Os funcionários do serviço lidam com eventos de push e interações de notificação  Para assinar as notificações por push do PWA no servidor, certifique-se de que as seguintes condições sejam atendidas.  

*   Seu PWA está instalado, ativo e registrado  
*   Seu código para concluir a tarefa de assinatura está no thread principal da interface do usuário do PWA  
*   Você tem conectividade de rede  
    
Antes de uma nova assinatura por push ser criada, o Microsoft Edge verifica se o usuário concedeu a permissão do PWA para receber notificações.  Caso não seja, o usuário será solicitado pelo navegador a pedir permissão.  Se a permissão for negada, a solicitação para lançar `registration.pushManager.subscribe` um , que deve ser `DOMException` manipulado.  Para obter mais informações sobre o gerenciamento de permissões, navegue até [Notificações por Push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Em seu `pwabuilder-sw-register.js` arquivo, adendo o seguinte trecho de código.  

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

Para obter mais informações, navegue até [PushManager][MDNPushManager] e [Web-Push.][NPMWebPushUsage]  

### <a name="step-3---listen-for-push-notifications"></a>Etapa 3 - Escutar notificações por push  

Depois que uma assinatura for criada no PWA, adicione manipuladores ao trabalhador do serviço para responder a eventos de push.  O evento Push é enviado do servidor para exibir notificações de notificação  As notificações de notificação do  Para concluir as seguintes tarefas, você deve adicionar um `click` manipulador.  

*   Descartar a notificação de not  
*   Abrir, focalizar ou abrir e focalizar todas as janelas abertas  
*   Abra e foque em uma nova janela para exibir uma página de cliente PWA  
    
Em seu `pwabuilder-sw.js` arquivo, adicione os seguintes manipuladores.  

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

### <a name="step-4---try-it-out"></a>Etapa 4 - Experimente  

Para testar notificações por push para seu PWA, conclua as etapas a seguir.  

1.  Navegue até seu PWA em `http://localhost:3000` .  Quando o seu funcionário de serviço é ativado e tenta inscrever seu PWA para notificações por push, o Microsoft Edge solicita que você permita que seu PWA mostre notificações.  Selecione **Permitir**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Caixa de diálogo De permissão para habilenciar notificações" lightbox="./media/notification-permission.png":::
       Caixa de diálogo De permissão para habilenciar notificações  
    :::image-end:::  
    
1.  Simular uma notificação por push do lado do servidor.  Com o PWA aberto `http://localhost:3000` no navegador, selecione `F12` abrir o DevTools.  Escolha **Application**  >  **Service Worker**  >  **Push** para enviar uma notificação por push de teste ao seu PWA.  
    
    :::row:::
       :::column span="":::
          Uma notificação por push deve ser exibida perto da barra de tarefas.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Push a notification from DevTools" lightbox="./media/devtools-push.png":::
             Push a notification from DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Se você não selecionar \(ou ativar\) uma notificação de notificação do sistema, o sistema a descartará automaticamente após vários segundos e enfilá-la em sua Central de Ações do Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificações no Centro de Ações do Windows" lightbox="./media/windows-action-center.png":::
             Notificações no Centro de Ações do Windows  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a>Próximas etapas  

As etapas a seguir incluem tarefas adicionais para ajudá-lo a entender a criação de PWAs reais.  

*   Gerenciar e armazenar assinaturas por push  
*   [Criptografar][NPMWebPushEncrypt] dados de carga  
*   Design dinâmico  
*   Vinculação profunda  
*   [Teste entre navegadores][BrowserStackTestEdgeBrowser]  
*   Implementar práticas de validação e teste, como [Webhint][Webhint]  
    
## <a name="see-also"></a>Ver também  

*   [Aplicativos Web progressivos em documentos web do MDN][MDNProgressiveWebApps]  
*   [Aplicativos Web progressivos no web.dev][WebDevProgressiveWebApps]  
*   [Leitores de Notícias do Hacker como Aplicativos Web Progressivos][HackerNewsProgressiveWebApps] - Compara diferentes estruturas e padrões de desempenho para implementar um exemplo \(Leitor de Notícias do Hacker\) PWA.  
*   [PWAs de estouros de míticos][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Um roteiro progressivo para seu Aplicativo Web Progressivo][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [POSTs offline com aplicativos Web progressivos][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Apostando na Web][JoretegBlogBettingWeb]  
*   [Nomear Aplicativos Web Progressivos][Fberriman20170626NamingProgressiveWebApps]  
*   [Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  

<!-- links -->  

<!--[ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]: /archive/microsoft-edge/legacy/developer/progressive-web-apps/index#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implantar um Node.js no Azure com Visual Studio código | Microsoft Docs"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Criar contas gratuitas do Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicativos Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificações da Web no Microsoft Edge | Windows Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste gratuito do Navegador do Microsoft Edge no Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Um roteiro progressivo para seu Aplicativo Web Progressivo"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs de estouros de míticos – a nova edição de borda"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Gerador de aplicativos express | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Nomear Aplicativos Web Progressivos"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Leitores de Notícias do Hacker como Aplicativos Web Progressivos"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Apostando na Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Api de notificações | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicativos Web progressivos \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de Trabalho de Serviço | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usando o serviço de | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do Aplicativo Web | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "POSTs offline com aplicativos Web progressivos"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Enviando notificações de WebPush identificadas pelo VAPID por meio do Serviço de Push do Mozilla | Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) - web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso - web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicativos Web Progressivos"  

[PwaBuilder]: https://www.pwabuilder.com "Construtor do PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Serviço de | Construtor do PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 3)"  

[VapidkeysMain]: https://vapidkeys.com "Proteger o gerador de teclas VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicativos Web progressivos | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Melhoria progressiva | Wikipédia"  
