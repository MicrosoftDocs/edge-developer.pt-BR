---
description: Este guia fornece uma visão geral das ferramentas e noções básicas do PWA para a criação de aplicativos Web progressivos no Windows.
title: Introdução aos aplicativos Web progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, PWABuilder, Web manifest, trabalho de serviço, push
ms.openlocfilehash: 4d7b571b83048f9ce271f451a7537027bb92eebc
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583781"
---
# Introdução aos aplicativos Web progressivos  

Aplicativos Web progressivos \ (PWAs \) são simplesmente aplicativos Web que são [aprimorados progressivamente][WikiProgressiveEnhancement] com recursos de semelhantes a aplicativos nativos em plataformas de suporte e mecanismos de navegador, como instalação do lançamento-da-tela inicial, suporte offline e notificações por push.  No Windows 10 com o mecanismo \ (EdgeHTML \) do Microsoft Edge, PWAs Desfrute da vantagem adicional de ser executado independentemente da janela do navegador como aplicativos da [plataforma universal do Windows][WindowsUwpGetStartedWhat] .  

Este guia fornece uma visão geral das noções básicas do PWA criando um `localhost` aplicativo Web simples como um PWA usando o Microsoft Visual Studio e alguns utilitários do PWA Builder.  O produto concluído funciona da mesma forma em qualquer navegador que ofereça suporte a PWAs.  

> [!TIP]
> Para uma maneira rápida de converter um site existente em um PWA e empacotá-lo para o Windows 10 e outras plataformas de aplicativos, examine o [construtor do PWA][PwaBuilder].  

## Pré-requisitos  

Você pode criar PWAs com qualquer IDE de desenvolvimento na Web.  Os pré-requisitos a seguir são apenas pré-requisitos para este guia, que o orientam pelo suporte de ferramentas do PWA no ecossistema do desenvolvedor do Windows.  

*   Baixe o \ (grátis \) [comunidade do Visual Studio 2017][VisualStudioDownloads].  Você também pode usar as edições Professional, Enterprise ou [Preview][VisualStudioPreview] .  No instalador do Visual Studio, escolha as seguintes cargas de trabalho.  
    
    *   **Desenvolvimento da plataforma universal do Windows**  
    *   **Desenvolvimento de Node. js**  

## Configurar um aplicativo Web básico  

Para simplificar, use o nó do Visual Studio [. js e][VisualStudioNodeJsTutorial] o modelo de aplicativo expresso para criar `localhost` um aplicativo Web que sirva uma `index.html` página.  Imagine isso como um espaço reservado para o aplicativo Web com todos os recursos atraentes que você está desenvolvendo como PWA.  

1.  Inicie o Visual Studio e inicie um novo projeto.  
    *   **Arquivo**  >  **Novo**  >  **Projeto...**  
    *   `Ctrl`+`Shift`+`N`  
1.  Em **JavaScript**, selecione **aplicativo Basic node. js Express 4**.  Defina o nome e o local e escolha **OK**.  
    
    ![Selecionando o modelo de projeto do node. js Express 4 no Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  Depois que seu novo projeto for carregado, escolha **Compilar** \ ( `Ctrl` + `Shift` + `B` \) e **Iniciar Depuração** \ ( `F5` \).  Verifique se o `index.html` arquivo é carregado quando você navega `http://localhost:1337` .  
    
    ![Executando seu novo site em localhost][ImageVsNodejsExpressIndex]  

## Transformar seu aplicativo em um PWA  

Agora, é hora de conectar os [requisitos][PwaEdgehtmlIndexRequirements] básicos do PWA para seu aplicativo Web: um *manifesto do aplicativo Web*, *https* e *serviços de trabalho*.  

### Manifesto do aplicativo Web  

Um [manifesto do aplicativo Web][MDNWebAppManifest] é um arquivo de metadados JSON que descreve seu aplicativo, incluindo o nome, o autor, a URL da página de entrada e um ou mais ícones.  Como ele segue um [esquema baseado em padrões][W3cWebAppManifest], você deve apenas fornecer um único manifesto de aplicativo Web para o PWA que você está instalando em qualquer plataforma, sistema operacional e combinação de dispositivos que suporte PWAs.  No ecossistema do Windows, seu manifesto do aplicativo Web se sinaliza ao indexador da Web do Bing que o PWA é um candidato para a inclusão automática na [Microsoft Store][PwaEdgehtmlMicrosoftStore], onde poderá alcançar cerca de 700 milhões usuários mensais ativos como um aplicativo do Windows 10.  

Se esse for um site existente, você poderá gerar um manifesto do aplicativo Web usando o [construtor do PWA][PwaBuilder].  Como ainda é um projeto não publicado, copie um manifesto de exemplo.  

1.  No *Gerenciador de soluções*do Visual Studio, clique com o botão direito do mouse na pasta *pública* e selecione **Adicionar**  >  **novo arquivo...** especificando `manifest.json` como o nome do item.  
1.  No `manifest.json` arquivo, copie o código a seguir.  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    Em um PWA real, a próxima etapa é personalizar o *nome*, *start_url*, *short_name*, *Descrição*e *ícones* \ (os ícones são abordados na próxima etapa \).  
    
    Para saber mais sobre os diferentes valores de membro e objetivos associados, consulte a referência de [manifesto do aplicativo Web][MDNWebAppManifest] .  
    
1.  Em seguida, preencha a `icons` matriz vazia com caminhos de imagem reais usando o gerador de imagem de aplicativo do PWA Builder.  
    
    1.  Usando um navegador da Web, Baixe esta [amostra 512x512 de imagem do PWA][ImagePwa].  
    1.  Vá para o gerador de [imagem do aplicativo][PwaBuilderAppImageGenerator]do PWA Builder e selecione a `pwa.png` imagem que você acabou de salvar como a **imagem de entrada** e, em seguida, escolha o botão **baixar** .  
    1.  **Abra** e **Extraia** o arquivo zip.  
    1.  No Gerenciador de soluções do Visual Studio, clique com o botão direito do mouse na `public` pasta e **abra pasta no explorador de arquivos**.  Crie uma **nova pasta** chamada `images` .  
    1.  Copie todas as pastas da plataforma \ ( `android` , `chrome` , `windows10` , etc. \) do zip extraído para a `images` pasta e feche a janela do explorador de arquivos.  Adicione as pastas ao seu projeto do Visual Studio \ (no Gerenciador de soluções, clique com o botão direito do mouse em `images` pasta e selecione **Adicionar**  >  **pasta existente..** . para cada uma das pastas \).  
    1.  Abra \ (com o Visual Studio ou qualquer editor \) do `icons.json` arquivo zip extraído e copie a `"icons": [...]` matriz para o `manifest.json` arquivo do seu projeto.  

1.  Agora você deve associar seu manifesto do aplicativo Web ao seu aplicativo.  Abra o `layout.pug` arquivo \ (na `views` pasta \) para edição e adicione essa linha logo após o link de folha de estilos.  \ (É simplesmente a abreviação do modelo [Pug][PugAttributes] do nó para `<link rel='manifest' href='/manifest.json'>` \).  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
Com tudo isso em vigor, seu aplicativo Web agora está servindo um manifesto e ícones de aplicativos prontos para tela inicial!  Tente executar seu aplicativo \ ( `F5` \) e carregar o manifesto.  

![Manifesto do aplicativo Web carregando do localhost][ImageVsNodejsExpressManifest]  

E um de seus ícones.  

![O logotipo do aplicativo Square71x71Logo está sendo carregado do localhost][ImageVsNodejsExpressIcon]  

Se você publicar o aplicativo em tempo real \ (com um `start_url` \ real \), o mecanismo de pesquisa do Bing agora o identifica como um candidato para [empacotamento e envio automáticos para a Microsoft Store][PwaEdgehtmlMicrosoftStore] como um aplicativo instalável do Windows 10.  Verifique se o arquivo manifest. JSON inclui os [sinais de qualidade para aplicativos Web progressivos][WindowsBlogsPwaEdge] para os quais o Bing verifica incluindo os itens a seguir.   

*   `name`  
*   `description`  
*   Pelo menos um ícone 512px quadrado ou maior \ (para garantir uma fonte de resolução suficiente para a geração automática da tela inicial do seu aplicativo, a listagem da loja, a imagem do bloco e assim por diante \).  

Além disso, use [https](#https), [trabalhos de serviço](#service-workers)e cumpra [as políticas da Microsoft Store][LegalWindowsAgrementsMicrosoftStorePolicies].  

### HTTPS  

[Os funcionários do serviço][MDNServiceWorkerApi] e outras tecnologias importantes do PWA que trabalham com trabalhadores de serviço \ (como as APIs de [cache][MDNCache], [Push][MDNPushApi]e [sincronização em segundo plano][MDNSyncManager] ) funcionam apenas em conexões seguras, o que significa [https][WikiHttps] para sites ativos ou `localhost` para fins de depuração.  

Se você [publicar este aplicativo Web como um site do Live][VisualStudioNodejsTutorialPublishAzureAppService] \ (por exemplo, configurando uma [conta gratuita do Azure][AzureCreateFreeAccount]\), você deve garantir que seu servidor esteja configurado para https.  Se você usar o [serviço de aplicativo do Microsoft Azure][AzureWebApps] para hospedar seu site, ele será servido via HTTPS por padrão.  

Para este guia, continue `http://localhost` a usar como um espaço reservado para um site ao vivo servido `https://` .  

### Trabalhadores do serviço  

Trabalhadores de serviço é a principal tecnologia por trás do PWAs. Os funcionários de serviço atuam como um proxy entre seu PWA e a rede para permitir que seu site funcione como um aplicativo nativo instalado que atende a cenários offline, responde a notificações por push do servidor e executa tarefas em segundo plano.  Os funcionários de serviço também abrem novas estratégias de desempenho.  Você não precisa implementar um aplicativo Web completo para usar o cache do serviço de trabalho para o desempenho de carregamento de página ajustado para seu site.  

Os funcionários de serviço são threads em segundo plano acionados por eventos que são executados a partir de arquivos JavaScript fornecidos juntamente com os scripts regulares que alimentam o aplicativo Web.  Como os funcionários do serviço não são executados no thread da interface do usuário principal, os funcionários do serviço não têm acesso ao DOM, embora o [thread de interface do usuário][MDNWorkerPrototypePostMessage] e um [thread de trabalho][MDNDedicatedWorkerGlobalScopePostMessage] sejam capazes de se comunicar usando `postMessage()` `onmessage` manipuladores de eventos.  

Você associa um trabalhador de serviço ao seu aplicativo registrando-o na origem da URL do seu site \ (ou um caminho especificado dentro dele \).  Depois de registrado, o arquivo de trabalho do serviço é baixado, instalado e ativado no computador do usuário.  Para saber mais, o MDN Web docs tem um guia abrangente sobre o [uso de trabalhadores de serviço][MDNUsingServiceWorkers] e uma referência de API de trabalho de [serviço][MDNServiceWorkerApi] detalhada.  

Para este tutorial, use o script de trabalho do serviço de página offline no [criador do PWA][PwaBuilderServiceWorker].  Comece Personalizando o script com mais funcionalidade de acordo com os requisitos de desempenho, a largura de banda da rede e assim por diante.  Examine o [Cookbook do serviço do serviço][ServiceWorkerCookbook] fornecido pelo Mozilla para obter uma série de ideias úteis de armazenamento em cache de trabalho de serviço.  

1.  Abra [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] e selecione o trabalhador do serviço de **página offline** \ (padrão \) e clique no botão **baixar trabalho do serviço** .  
1.  Abrir a pasta baixar e copiar os dois arquivos a seguir  

    *   ServiceWorker1\pwabuilder-sw-register.js  
    *   ServiceWorker1\pwabuilder-sw.js  
    
    Salve os arquivos na `public` pasta do seu projeto do Visual Studio Web App.  \ (Do Visual Studio, use `Ctrl` + `O` para abrir o explorador de arquivos para o seu projeto e navegue até a `public` pasta \).  
    
    Vale a pena rever o código em ambos os arquivos para obter a essência de como registrar um trabalhador de serviço que armazena em cache uma página designada \ ( `offline.html` \) e a atende quando uma busca de rede falha.  Em seguida, crie uma `offline.html` página simples como um espaço reservado para a funcionalidade offline do seu aplicativo.  
    
1.  No Gerenciador de soluções, abra o `views/layout.pug` arquivo e adicione a seguinte linha abaixo de suas marcas de link.  
    
    ```html
    script(src='/pwabuilder-sw-register.js')
    ```  
    
    Seu site carrega e executa o script de registro do trabalho do serviço.  
    
1.  No Gerenciador de soluções, clique com o botão direito do mouse na `public` pasta e selecione **Adicionar**  >  **novo arquivo..**..  Nomeie- `offline.html` o e adicione um `<title>` conteúdo de corpo e, por exemplo, o código a seguir.  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    Nesse ponto, sua `public` pasta deve ter três arquivos novos.  
    
    ![Arquivos adicionados à pasta pública da solução][ImageVsNodejsExpressPublic]  
    
1.  No Gerenciador de soluções, abra o `routes\index.js` arquivo e adicione o seguinte código logo antes do comando final \ ( `module.exports = router;` \).  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    Isso instrui seu aplicativo a servir o `offline.html` arquivo \ (quando seu operador de serviço o busca no cache offline \).  
    
1.  Teste seu PWA!  Compilar \ ( `Ctrl` + `Shift` + `B` \) e executar \ ( `F5` \) seu aplicativo Web para iniciar o Microsoft Edge e abrir a `localhost` página.  Em seguida, conclua as etapas a seguir.  
    
    1.  Abra o **console** do Edge devtools \ ( `Ctrl` + `Shift` + `J` \) e verifique se o trabalhador do serviço foi registrado.  
    1.  No painel **depurador** , expanda o controle **serviços de funcionários** e clique em sua origem.  Na **visão geral do trabalho do serviço**, verifique se o trabalhador do seu serviço está ativado e em execução.  
        
        ![Visão geral do trabalhador do serviço Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  Expanda o controle de **cache** e verifique se a `offline.html` página está armazenada em cache.  
        
        ![Cache de trabalho do serviço Edge DevTools][ImageDevtoolsSwCache]  
        
1.  Tempo para experimentar o PWA como um aplicativo offline!  No Visual Studio, **pare a depuração** \ ( `Shift` + `F5` \) em seu aplicativo Web, abra o Microsoft Edge \ (ou atualize \) no endereço localhost do seu website.  Ele agora deve carregar a `offline.html` página \ (Obrigado ao seu trabalhador de serviço e cache offline \)!  
    
    ![offline. html de http://localhost:1337 carregado no Microsoft Edge][ImageOfflineHtml]  

## Adicionar notificações por push  

Torne seu PWA mais parecido com o aplicativo adicionando suporte do lado do cliente para notificações por push usando a [API de envio][MDNPushApi] para assinar um serviço de mensagens e a [API de notificações][MDNNotificationsApi] para exibir uma mensagem em notificação do sistema ao receber uma mensagem.  Da mesma forma que com os profissionais do serviço, são APIs baseadas em padrões que funcionam entre navegadores, portanto, você só precisa escrever o código uma vez para que ele funcione em qualquer lugar PWAs tem suporte.  No lado do servidor, use a biblioteca de código-fonte aberto [por push da Web][NPMWebPush] para manipular as diferenças envolvidas no envio de mensagens de push para vários navegadores.  

O procedimento a seguir é adaptado da demonstração avançada push no [manual do serviço de trabalho][ServiceWorkerCookbookPushRichDemo] que é fornecida pelo Mozilla, o que vale a pena fazer uma série de outras receitas de trabalho por push e serviço da Web úteis.  

### Etapa 1-instalar a NPM Web-Push library  

No Gerenciador de soluções do Visual Studio, clique com o botão direito do mouse em seu projeto e **abra janela interativa do node. js..**..  Digite o código a seguir.  

```javascript
.npm install web-push
```  

Isso faz com que a biblioteca de [envio por push da Web][NPMWebPush] seja instalada.  Em seguida, abra o `index.js` arquivo e adicione a seguinte linha à parte superior do seu arquivo após as outras instruções de requisito.  

```javascript
var webpush = require('web-push');
```  

### Etapa 2-gerar chaves VAPID para o seu servidor  

Em seguida, você deve gerar as chaves VAPID \ (identificação do servidor de aplicativos voluntária \) para que seu servidor envie mensagens de envio para o cliente PWA.  Você só precisa fazer isso uma vez \ (ou seja, seu servidor requer apenas um único par de teclas VAPID \).  Na janela interativa node. js, digite o código a seguir.  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

A saída deve resultar em um objeto JSON que contém uma chave pública e privada, que você copia para a lógica do servidor.  

No seu `index.js` arquivo, logo antes da linha final \ ( `module.exports = router` \), adicione o código a seguir.  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

Copie os `publicKey` `privateKey` valores e que você acabou de gerar.  Sinta-se à vontade para personalizar o `mailto` endereço também \ (ainda não é necessário para executar este exemplo \).  

O [blog de engenharia de serviços do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] tem um ótimo explicador em VAPID e webpush se você estiver interessado nos detalhes de como ele funciona nos bastidores.  

### Etapa 3-manipular solicitações do servidor relacionados a Push  

Agora, configure rotas para manipular solicitações relacionadas a Push do cliente PWA, incluindo a veiculação da chave pública VAPID e o registro do cliente para receber envios.  

Em um cenário real, uma notificação por Push provavelmente provém de um evento na lógica do servidor.  Para simplificar as coisas aqui, você deve adicionar um botão de **notificação por push** à nossa página inicial do PWA para gerar envios do nosso servidor e um `/sendNotification` ponto de extremidade \ (rota do servidor \) para lidar com essas solicitações.  

Em seu `index.js` arquivo, acrescente as seguintes rotas logo após o código de inicialização do VAPID que você adicionou na [etapa 2] [#step-2---gerar-VAPID-Keys-para-seu-servidor].  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

Com o código do lado do servidor estabelecido, coloque as notificações por push no cliente do PWA.  

### Etapa 4-assinar notificações por push  

Como parte da função dos proxies de rede do PWA, os funcionários de serviço lidam com eventos de push e interações de notificação do sistema.  No entanto, como se trata de primeiro configurar \ (ou registrar \) um trabalhador de serviço, a assinatura do PWA para notificações por push de servidor acontece no thread da interface do usuário principal do PWA e requer conectividade de rede.  Assinar as notificações por push requer um registro de trabalho do serviço ativo, portanto, você deve primeiro verificar se o trabalhador do serviço está instalado e ativo antes de tentar assiná-lo para notificações por push.  

Antes de criar uma nova assinatura push, o Microsoft Edge verifica se o usuário concedeu permissão ao PWA para receber notificações.  Caso contrário, o usuário será solicitado a confirmar a permissão do navegador.  Se a permissão for negada, a solicitação para `registration.pushManager.subscribe` lançar a `DOMException` ; portanto, você deverá tratá-la.  Para saber mais sobre o gerenciamento de permissões, consulte [notificações por push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

Em seu `pwabuilder-sw-register.js` arquivo, acrescente o código a seguir.  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
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

Examine a documentação do MDN na interface do [pushmanager][MDNPushManager] e documentos do NPM na biblioteca de [envio pela Web][NPMWebPushUsage] para obter mais detalhes sobre como as APIs funcionam e várias opções relacionadas.  

### Etapa 5-configurar manipuladores de eventos push e notificationclick  

Com a configuração da assinatura push, o restante do trabalho acontece no trabalho do serviço.  Primeiro, você deve configurar um manipulador para eventos Push enviados pelo servidor e responder com uma notificação do sistema \ (se a permissão foi concedida \) exibindo a carga de dados de envio.  Em seguida, adicione um manipulador de clique para o sistema de notificação para ignorar a notificação e classificar por uma lista de janelas abertas no momento para abrir, enfocar ou abrir e focalizar a página do cliente PWA pretendida.  

Em seu `pwabuilder-sw.js` arquivo, acrescente os manipuladores a seguir.  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
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

### Etapa 6-Experimente  

Tempo para testar as notificações por push no seu PWA!  

1.  Execute \ ( `F5` \) o PWA no navegador.  Como você modificou o código de trabalho do serviço \ ( `pwabuilder-sw.js` \), deve abrir o depurador devtools \ ( `F12` \) para o painel de **visão geral do trabalhador do serviço** e **cancelar o registro** do trabalhador do serviço e recarregar \ ( `F5` \) a página para registrá-la novamente \ (ou clicar em **Atualizar**\).  Em um cenário de produção, o navegador verifica regularmente se há atualizações do trabalho do serviço e instala as atualizações em segundo plano.  Você deve forçá-lo aqui para obter resultados imediatos.  
    
    À medida que o trabalhador do serviço é ativado e tenta assinar as notificações por push do PWA, você deve ver uma caixa de diálogo de permissão na parte inferior da página.  
    
    ![Caixa de diálogo de permissão para habilitar notificações][ImageNotificationPermission]  
    
    Escolha **Sim** para habilitar as notificações do sistema para o seu PWA.  
    
1.  No painel Visão geral do trabalhador do serviço, tente escolher o botão de **ação** .  Será exibida uma notificação do sistema com a carga \ (codificada "\ (embutida" Test Push Message of DevTools "\).  
    
    ![Enviar uma notificação por push de DevTools][ImageDevtoolsPush]  
    
1.  Em seguida, tente escolher o botão **enviar notificação** na home page do seu PWA.  Desta vez, um sistema de notificação com a carga do seu servidor será exibido.  
    
    ![Enviar uma notificação por push do servidor PWA][ImagePwaPush]  
    
    Se você não clicar em \ (ou ativar \) uma notificação do sistema, ela será ignorada após vários segundos e será colocada na fila na central de ações do Windows.  
    
    ![Notificações na central de ações do Windows][ImageWindowsActionCenter]  
    
    Você tem noções básicas das notificações por push do PWA.  Em um aplicativo real, as próximas etapas são implementadas de forma a gerenciar e armazenar assinaturas push e de [criptografar][NPMWebPushEncrypt] corretamente os dados de carga enviados pela conexão.  
    
## Aprofundamento  

Este guia demonstrou a Anatomia básica de um aplicativo Web progressivo e das ferramentas de desenvolvimento do Microsoft PWA, incluindo o Visual Studio, o construtor do PWA e o Edge DevTools.  

É claro que há muito mais que vai para [fazer um grande PWA][PwaEdgehtmlIndexRequirements] além do que você lê aqui, incluindo design responsivo, vinculação profunda, [teste entre navegadores][BrowserStackTestEdgeBrowser] e outras [práticas recomendadas][Webhint] \ (não para mencionar a funcionalidade do seu aplicativo! \), mas espero que este guia tenha uma introdução sólida de noções básicas do PWA e algumas ideias sobre como começar.  Se você tiver outras dúvidas sobre o desenvolvimento do PWA com o Windows ou com o Visual Studio, deixe um comentário!  

Revise os outros guias do PWA para aprender a aumentar o envolvimento do cliente e oferecer uma experiência de aplicativo integrada mais uniforme e integrada ao sistema operacional.  

*   [Ajuste do Windows][PwaEdgehtmlWindowsFeatures]. Usando a detecção simples de recursos, você pode aprimorar progressivamente seus clientes do PWA para Windows 10 por meio de APIs do Windows Runtime (WinRT \) nativas, como aquelas para personalizar as notificações do bloco do menu **Iniciar** do Windows e a barra de tarefas, e \ (mediante permissão \) trabalhando com recursos do usuário, como fotos, música e calendário.  
*   [PWAs na Microsoft Store][PwaEdgehtmlMicrosoftStore].  Saiba mais sobre as vantagens da distribuição da App Store e como enviar seu PWA.  

## Consulte também  

*   [Aplicativos Web progressivos em MDN Web docs][MDNProgressiveWebApps] – excelente guia sobre aplicativos Web progressivos.  
*   [Aplicativos Web progressivos no Web. dev][WebDevProgressiveWebApps] – excelente guia sobre aplicativos Web progressivos.  
*   [Aplicativos Web progressivos tem][ProgressiveWebApps] -tem exemplos reais de PWAs.  
*   [Leitores de notícias de hackers como Web Apps progressivos][HackerNewsProgressiveWebApps] – compara estruturas e padrões de desempenho diferentes para implementar uma amostra \ (leitor de notícias de hackers \) PWA.  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requisitos-aplicativos Web progressivos \ (EdgeHTML \) no Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Aplicativos Web progressivos \ (EdgeHTML \) na Microsoft Store"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps-edgehtml/windows-features.md "Personalize seu PWA \ (EdgeHTML \) para Windows"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Políticas da Microsoft Store | Documentos da Microsoft"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Tutorial: criar um aplicativo node. js e expressa no Visual Studio | Documentos da Microsoft"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publicar no serviço de aplicativo do Azure-criar um aplicativo node. js e Express no Visual Studio | Documentos da Microsoft"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "O que é um aplicativo da plataforma universal do Windows \ (UWP \)?  | Documentos da Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Criar conta gratuita do Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Aplicativos Web | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Boas-vindas de aplicativos Web progressivos para Microsoft Edge e Windows 10 | Blogs do Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notificações da Web no Microsoft Edge | Blogs do Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Downloads | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Serviços de & de software para desenvolvedores gratuitos | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visualização do Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Teste gratuito do navegador Microsoft Edge no Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Leitores de notícias de hackers como Web Apps progressivos"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. CreateMessage \ (\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API de notificações | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Aplicativos Web progressivos \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "Pushmanager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Usar trabalhadores de serviço | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifesto do aplicativo Web | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. prototype. CreateMessage \ (\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Enviar notificações webpush identificadas pela VAPID por meio do serviço de envio do Mozilla | Serviços do Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "por push na Web | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "criptografar (userpublickey, userauth, Payload, contentEncoding)-envio pela Web | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Uso-Push-Web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Aplicativos Web progressivos"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Atributos | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Construtor do PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Gerador de imagens de aplicativos"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Trabalhador do serviço | Construtor do PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "Cookbook do inworkr"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Demonstração avançada push | Cookbook do inworkr"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Manifesto do aplicativo Web | W3C"  

[Webhint]: https://sonarwhal.com "webhint, o mecanismo de dicas para práticas recomendadas da Web" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usar funcionários da Web" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Aplicativos Web progressivos | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Wikipédia"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Aperfeiçoamento progressivo | Wikipédia"  
