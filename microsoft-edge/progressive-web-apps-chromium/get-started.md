---
description: Este guia fornece uma visão geral das ferramentas e noções básicas do PWA para a criação de aplicativos Web progressivos no Windows.
title: Introdução aos aplicativos Web progressivos (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, PWABuilder, Web manifest, trabalho de serviço, push
ms.openlocfilehash: a9a0cad2d771e52b783053e36f0f23dec5d8e70c
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894707"
---
# Introdução aos aplicativos Web progressivos (Chromium)  

Aplicativos Web progressivos \ (PWAs \) são aplicativos Web que são [aprimorados progressivamente][WikiProgressiveEnhancement] com recursos semelhantes a aplicativos, como instalação, suporte offline e notificações por push.  Você também pode empacotar o PWA para repositórios de aplicativos, incluindo a Microsoft Store e o Google Play, a Mac App Store e muito mais.  A Microsoft Store é a loja de aplicativos comerciais interna do Windows 10.  

O guia a seguir fornece uma visão geral das noções básicas do PWA ao criar um aplicativo Web simples e prorroga-lo como PWA.  O projeto concluído funciona em navegadores modernos.  

> [!TIP]
> Você pode usar o [PWABuilder][PwaBuilder] para criar um novo PWA, aprimorar o PWA existente ou empacotar seu PWA para repositórios de aplicativos.  

## Pré-requisitos  

*   Use o [código vs][VisualstudioCodeMain] para editar o código-fonte do PWA.  
*   Use [Node.js][NodejsMain] como seu servidor Web local.  

## Configurar um aplicativo Web básico  

Para criar um aplicativo Web vazio, siga as etapas no [aplicativo nó Express app Generator][ExpressjsApplicationGenerator]e nomeie seu aplicativo `MySamplePwa` .  

No prompt, execute os comandos a seguir.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Os comandos criam um aplicativo Web vazio e instalam as dependências.  

Agora você tem um aplicativo Web funcional simples.  Para iniciá-lo, execute o seguinte comando.  

```shell
npm start
```  

Agora, navegue até `http://localhost:3000` para exibir seu novo aplicativo Web.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Executando seu novo PWA no localhost":::
   Executando seu novo PWA no localhost
:::image-end:::

## Começar a criar um PWA  

Agora que você tem um aplicativo Web simples, estenda-o como um PWA adicionando os 3 requisitos para PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [Https](#step-1---use-https), um [manifesto do aplicativo Web](#step-2---create-a-web-app-manifest)e um [trabalho de serviço](#step-3---add-a-service-worker).  

### Etapa 1: usar HTTPS  

As principais partes da plataforma PWA, como [funcionários de serviço][MDNServiceWorkerApi], exigem o uso de HTTPS.  Quando o seu PWA ficar ao vivo, você deverá publicá-lo em uma URL HTTPS.  

Para fins de depuração, o Microsoft Edge também permite `http://localhost` usar as APIs do PWA.  

Se você [publicar seu aplicativo Web como um site do vivo][VisualStudioNodejsTutorialPublishAzureAppService] \ (por exemplo, configurando uma [conta gratuita do Azure][AzureCreateFreeAccount]\), você deve garantir que seu servidor esteja configurado para https.  Se você usar o [serviço de aplicativo do Microsoft Azure][AzureWebApps] para hospedar seu site, ele será servido via HTTPS por padrão.  

O guia a seguir, use `http://localhost` para criar seu PWA.  

### Etapa 2-criar um manifesto do aplicativo Web  

Um [manifesto do aplicativo Web][MDNWebAppManifest] é um arquivo JSON que contém metadados sobre o seu aplicativo, como nome, descrição, ícones e muito mais.  

Para adicionar um manifesto do aplicativo ao aplicativo Web:  

1.  Em vs Code, vá para **arquivo**  >  **abrir pasta** e escolha o `MySamplePwa` diretório que você criou anteriormente.  
1.  Pressione `Ctrl` + `N` para criar um novo arquivo e cole no trecho de código a seguir.  
    
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
1.  Em VS Code, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Etapa 3: adicionar um trabalhador de serviço  

Os funcionários de serviço são a tecnologia principal por trás do PWAs, permitindo cenários como suporte offline, cache avançado e executar tarefas em segundo plano anteriormente limitadas a aplicativos nativos.  

Os funcionários de serviço são tarefas em segundo plano que interceptam solicitações de rede de seu aplicativo Web.  Elas executam tarefas, mesmo quando o PWA não está em execução, como servir recursos solicitados de um cache, enviar notificações por push, executar tarefas de busca em segundo plano, ícones do selos e assim por diante.  Os funcionários do serviço são definidos em um arquivo JavaScript especial.  Para obter mais informações, consulte [usando trabalhadores do serviço][MDNUsingServiceWorkers] e a [API do serviço de trabalho][MDNServiceWorkerApi].  

Para criar um trabalho de serviço em seu projeto, use a primeira receita do trabalho do serviço de **rede cache** do [PWA Builder][PwaBuilderServiceWorker].  

1.  Navegue até [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], selecione o trabalho do primeiro serviço de **rede em cache** e selecione o botão **baixar** .  O arquivo baixado contém os seguintes arquivos:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  Copie os arquivos baixados para a `public` pasta no seu projeto de aplicativo Web.  
    
1.  No código VS, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Seu aplicativo Web agora tem um trabalho de serviço que usa a primeira estratégia de cache, que busca recursos como imagens, JS, CSS e HTML do cache primeiro, e retorna à rede conforme necessário.  

Use as etapas a seguir para confirmar a execução do trabalho do serviço.  

1.  Navegue até seu aplicativo Web usando `http://localhost:3000` .  Se o seu aplicativo Web não estiver disponível, execute o seguinte comando.   
    
    ```shell
    npm start
    ```
    
1.  No Microsoft Edge, selecione `F12` para abrir o Microsoft Edge devtools.  Selecione **aplicativo**e, em seguida, selecione os **funcionários** do serviço para exibir os funcionários do serviço.  Se você não vir o trabalhador do serviço, talvez seja necessário atualizar a página.  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Visão geral do trabalhador do serviço Microsoft Edge DevTools":::
       Visão geral do trabalhador do serviço Microsoft Edge DevTools
    :::image-end:::
    
1.  Exiba o cache do serviço de trabalho expandindo o **armazenamento de cache** e selecione **pwabuilder-cache**.  Você deve ver todos os recursos armazenados em cache pelo trabalhador do serviço, como o ícone do aplicativo, manifesto do aplicativo, arquivos CSS e JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache do trabalho do serviço no Microsoft Edge DevTools":::
       Cache do trabalho do serviço no Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Experimente o seu PWA como um aplicativo offline.  No Microsoft Edge DevTools \ ( `F12` \), escolha **rede** e altere o status **online** para **offline**.  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Configurando o aplicativo para o modo offline no Microsoft Edge DevTools":::
       Configurando o aplicativo para o modo offline no Microsoft Edge DevTools
    :::image-end:::
    
1.  Atualize o aplicativo e veja se ele está funcionando offline, servindo os recursos do seu aplicativo do cache.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA em execução offline":::
       PWA em execução offline
    :::image-end:::
    
## Adicionar notificações por push ao seu PWA  

Você pode criar PWAs que dão suporte a notificações por push completando as seguintes tarefas.  

1.  Assinar um serviço de mensagens usando a [API de envio][MDNPushApi]  
1.  Exibir mensagens do sistema quando uma mensagem é recebida do serviço usando a [API de notificações][MDNNotificationsApi]  

Da mesma forma que com os profissionais do serviço, são APIs baseadas em padrões que funcionam entre navegadores, portanto, você só precisa escrever o código uma vez para que ele funcione em qualquer lugar com suporte para o PWAs.  Para obter mais informações sobre como enviar mensagens push para navegadores diferentes em seu servidor, use a biblioteca de fonte aberta do [Push Web][NPMWebPush] .  

As etapas a seguir foram adaptadas da demonstração avançada push no [livro do serviço de trabalho][ServiceWorkerCookbookPushRichDemo] do entanto, que tem uma série de outras receitas úteis de trabalho de serviço e envio da Web.  

### Etapa 1-gerar chaves VAPID  

As notificações por push exigem chaves VAPID \ (identificação do servidor de aplicativos voluntários \) para enviar mensagens de envio para o cliente PWA.  Há vários geradores de chave VAPID disponíveis online \ (por exemplo, [vapidkeys.com][VapidkeysMain]\).  Após a geração, você deve obter um objeto JSON que contém uma chave pública e privada.  Salve as chaves para etapas subsequentes no tutorial a seguir.  Para obter informações sobre como o VAPID e o webpush funcionam, consulte [enviando notificações webpush identificadas pelo serviço de envio do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Etapa 2-assinar notificações por push  

Os funcionários de serviço lidam com eventos de push e interações de notificação do sistema no seu PWA.  Para assinar o PWA para notificações por push de servidor, verifique se as seguintes condições foram atendidas.  

*   Seu PWA está instalado, ativo e cadastrado  
*   Seu código que executa a tarefa de assinatura está no thread da interface do usuário principal do PWA  
*   Você tem conectividade de rede  

Antes da criação de uma nova assinatura de envio, o Microsoft Edge verifica se o usuário concedeu permissão ao PWA para receber notificações.  Caso contrário, o usuário será solicitado a confirmar a permissão do navegador.  Se a permissão for negada, a solicitação para `registration.pushManager.subscribe` lançar uma `DOMException` , que deve ser manipulada.  Para saber mais sobre o gerenciamento de permissões, consulte [notificações por push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

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

Para obter mais informações, consulte o [pushmanager][MDNPushManager] e [a Web-Push][NPMWebPushUsage].  

### Etapa 3-ouvir as notificações por push  

Agora que uma assinatura está configurada no PWA, adicione manipuladores ao trabalhador do serviço para responder a eventos Push \ (enviado do servidor \) para exibir notificações do sistema com os dados de uma mensagem recebida.  Você deve adicionar um manipulador de clique para executar qualquer uma das seguintes tarefas.  
*   ignorar a notificação do sistema  
*   abrir, focalizar ou abrir e focalizar qualquer janelas abertas  
*   abrir e focalizar uma nova janela para exibir uma página do cliente PWA  

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
    
    // This looks to see if the current notification is already open and focuses it.
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

Execute as etapas a seguir para testar as notificações por push no PWA.  

1.  Navegue até o seu PWA em `http://localhost:3000` .  Quando o trabalhador do serviço é ativado e tenta assinar notificações por push pelo PWA, o Microsoft Edge solicita que o seu PWA mostre notificações.  Selecione **permitir**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Caixa de diálogo de permissão para habilitar notificações":::
       Caixa de diálogo de permissão para habilitar notificações
    :::image-end:::
    
    
1.  Simule uma notificação por push do lado do servidor.  Com o seu PWA aberto em `http://localhost:3000` no navegador, selecione `F12` para abrir o devtools.  Escolha **Application**  >  **Service Worker**  >  **envio** de trabalhador de serviço de aplicativo para enviar uma notificação por push de teste ao seu PWA.  Você verá uma notificação por push exibida próxima à barra de tarefas.  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Enviar uma notificação por push de DevTools":::
       Enviar uma notificação por push de DevTools
    :::image-end:::
     
    Se você não selecionar \ (ou ativar \) uma notificação do sistema, ela será ignorada após vários segundos e será colocada em fila na central de ações do Windows.  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificações na central de ações do Windows":::
       Notificações na central de ações do Windows
    :::image-end:::
    
    
## Próximas etapas  

Veja a seguir uma lista de tarefas adicionais a serem aprendidas ao criar PWAs do mundo real:  

*  Gerenciar e armazenar assinaturas push  
*  [Criptografar][NPMWebPushEncrypt] dados de carga  
*  Design dinâmico  
*  Vinculação profunda  
*  [Teste entre navegadores][BrowserStackTestEdgeBrowser]  
*  Implementar práticas recomendadas, como [webhint][Webhint]  

## Consulte também  

*   [Aplicativos Web progressivos em MDN Web docs][MDNProgressiveWebApps].  
*   [Aplicativos Web progressivos em Web. dev][WebDevProgressiveWebApps].  
*   [Leitores de notícias de hackers como Web Apps progressivos][HackerNewsProgressiveWebApps] – compara estruturas e padrões de desempenho diferentes para implementar uma amostra \ (leitor de notícias de hackers \) PWA.  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Implantar um aplicativo Node.js no Azure com código VS | Documentos da Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Criar conta gratuita do Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicativos Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificações da Web no Microsoft Edge | Blogs do Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Código do Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste gratuito do navegador Microsoft Edge no Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Gerador de aplicativos expressos | Expresso" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Leitores de notícias de hackers como Web Apps progressivos"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificações | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicativos Web progressivos \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabalhadores de serviço | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do aplicativo Web | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Enviar notificações webpush identificadas pela VAPID por meio do serviço de envio do Mozilla | Serviços do Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "por push na Web | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "criptografar (userpublickey, userauth, Payload, contentEncoding)-envio pela Web | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso-Push-Web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicativos Web progressivos"  

[PwaBuilder]: https://www.pwabuilder.com "Construtor do PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Trabalhador do serviço | Construtor do PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Demonstração avançada push | Cookbook do inworkr"  

[VapidkeysMain]: https://vapidkeys.com "Gerador de chave de VAPID seguro | VapidKeys" 

[Webhint]: https://sonarwhal.com "webhint, o mecanismo de dicas para práticas recomendadas da Web"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicativos Web progressivos | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Aperfeiçoamento progressivo | Wikipédia"  
