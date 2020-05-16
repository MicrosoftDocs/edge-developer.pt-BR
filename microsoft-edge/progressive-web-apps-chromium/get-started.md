---
description: Este guia fornece uma visão geral das ferramentas e noções básicas do PWA para a criação de aplicativos Web progressivos no Windows.
title: Introdução aos aplicativos Web progressivos (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, PWABuilder, Web manifest, trabalho de serviço, push
ms.openlocfilehash: 6c5fa5d6af8494f33e11a545d5dde1264604c787
ms.sourcegitcommit: 136642396bb8094a535e203067ee429e60d31d25
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "10659206"
---
# <span data-ttu-id="63e7b-104">Introdução aos aplicativos Web progressivos (Chromium)</span><span class="sxs-lookup"><span data-stu-id="63e7b-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="63e7b-105">Aplicativos Web progressivos \ (PWAs \) são aplicativos Web que são [aprimorados progressivamente][WikiProgressiveEnhancement] com recursos semelhantes a aplicativos, como instalação, suporte offline e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="63e7b-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement] with app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="63e7b-106">Você também pode empacotar o PWA para repositórios de aplicativos, incluindo a Microsoft Store e o Google Play, a Mac App Store e muito mais.</span><span class="sxs-lookup"><span data-stu-id="63e7b-106">You may also packaged your PWA for app stores, including the Microsoft Store as well as Google Play, Mac App Store and more.</span></span>  <span data-ttu-id="63e7b-107">A Microsoft Store é a loja de aplicativos comerciais interna do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63e7b-107">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="63e7b-108">O guia a seguir fornece uma visão geral das noções básicas do PWA ao criar um aplicativo Web simples e prorroga-lo como PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-108">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="63e7b-109">O projeto concluído funciona em navegadores modernos.</span><span class="sxs-lookup"><span data-stu-id="63e7b-109">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="63e7b-110">Você pode usar o [PWABuilder][PwaBuilder] para criar um novo PWA, aprimorar o PWA existente ou empacotar seu PWA para repositórios de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="63e7b-110">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="63e7b-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="63e7b-111">Prerequisites</span></span>  

*   <span data-ttu-id="63e7b-112">Use o [código vs][VisualstudioCodeMain] para editar o código-fonte do PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-112">Use [VS Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="63e7b-113">Use [node. js][NodejsMain] como seu servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="63e7b-113">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="63e7b-114">Configurar um aplicativo Web básico</span><span class="sxs-lookup"><span data-stu-id="63e7b-114">Set up a basic web app</span></span>  

<span data-ttu-id="63e7b-115">Para criar um aplicativo Web vazio, siga as etapas no [aplicativo nó Express app Generator][ExpressjsApplicationGenerator]e nomeie seu aplicativo `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="63e7b-115">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="63e7b-116">No prompt, execute os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e7b-116">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="63e7b-117">Os comandos criam um aplicativo Web vazio e instalam as dependências.</span><span class="sxs-lookup"><span data-stu-id="63e7b-117">The commands creates an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="63e7b-118">Agora você tem um aplicativo Web funcional simples.</span><span class="sxs-lookup"><span data-stu-id="63e7b-118">Now you have a simple, functional web app.</span></span>  <span data-ttu-id="63e7b-119">Para iniciá-lo, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="63e7b-119">To start it, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="63e7b-120">Agora, navegue até `http://localhost:3000` para exibir seu novo aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="63e7b-120">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Executando seu novo PWA no localhost":::
   <span data-ttu-id="63e7b-122">Executando seu novo PWA no localhost</span><span class="sxs-lookup"><span data-stu-id="63e7b-122">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="63e7b-123">Começar a criar um PWA</span><span class="sxs-lookup"><span data-stu-id="63e7b-123">Get started building a PWA</span></span>  

<span data-ttu-id="63e7b-124">Agora que você tem um aplicativo Web simples, estenda-o como um PWA adicionando os 3 requisitos para PWAs</span><span class="sxs-lookup"><span data-stu-id="63e7b-124">Now that you have a simple web app, extend it as a PWA by adding the 3 requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="63e7b-125">: [Https](#step-1---use-https), um [manifesto do aplicativo Web](#step-2---create-a-web-app-manifest)e um [trabalho de serviço](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="63e7b-125">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="63e7b-126">Etapa 1: usar HTTPS</span><span class="sxs-lookup"><span data-stu-id="63e7b-126">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="63e7b-127">As principais partes da plataforma PWA, como [funcionários de serviço][MDNServiceWorkerApi], exigem o uso de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="63e7b-127">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="63e7b-128">Quando o seu PWA ficar ao vivo, você deverá publicá-lo em uma URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="63e7b-128">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="63e7b-129">Para fins de depuração, o Microsoft Edge também permite `http://localhost` usar as APIs do PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-129">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="63e7b-130">Se você [publicar seu aplicativo Web como um site do vivo][VisualStudioNodejsTutorialPublishAzureAppService] \ (por exemplo, configurando uma [conta gratuita do Azure][AzureCreateFreeAccount]\), você deve garantir que seu servidor esteja configurado para https.</span><span class="sxs-lookup"><span data-stu-id="63e7b-130">If you [publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="63e7b-131">Se você usar o [serviço de aplicativo do Microsoft Azure][AzureWebApps] para hospedar seu site, ele será servido via HTTPS por padrão.</span><span class="sxs-lookup"><span data-stu-id="63e7b-131">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="63e7b-132">O guia a seguir, use `http://localhost` para criar seu PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-132">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="63e7b-133">Etapa 2-criar um manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="63e7b-133">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="63e7b-134">Um [manifesto do aplicativo Web][MDNWebAppManifest] é um arquivo JSON que contém metadados sobre o seu aplicativo, como nome, descrição, ícones e muito mais.</span><span class="sxs-lookup"><span data-stu-id="63e7b-134">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="63e7b-135">Para adicionar um manifesto do aplicativo ao aplicativo Web:</span><span class="sxs-lookup"><span data-stu-id="63e7b-135">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="63e7b-136">Em vs Code, vá para **arquivo**  >  **abrir pasta** e escolha o `MySamplePwa` diretório que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="63e7b-136">In VS Code, go **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="63e7b-137">Pressione `Ctrl` + `N` para criar um novo arquivo e cole no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e7b-137">Press `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="63e7b-138">Salve o arquivo como `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="63e7b-138">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="63e7b-139">Adicione uma imagem do ícone do aplicativo 512x512 chamado `icon512.png` to `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="63e7b-139">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="63e7b-140">Você pode usar a [imagem de exemplo][ImagePwa] para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="63e7b-140">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="63e7b-141">Em VS Code, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.</span><span class="sxs-lookup"><span data-stu-id="63e7b-141">In VS Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="63e7b-142">Etapa 3: adicionar um trabalhador de serviço</span><span class="sxs-lookup"><span data-stu-id="63e7b-142">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="63e7b-143">Os funcionários de serviço são a tecnologia principal por trás do PWAs, permitindo cenários como suporte offline, cache avançado e executar tarefas em segundo plano anteriormente limitadas a aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="63e7b-143">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="63e7b-144">Os funcionários de serviço são tarefas em segundo plano que interceptam solicitações de rede de seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="63e7b-144">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="63e7b-145">Elas executam tarefas, mesmo quando o PWA não está em execução, como servir recursos solicitados de um cache, enviar notificações por push, executar tarefas de busca em segundo plano, ícones do selos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="63e7b-145">They perform tasks, even when your PWA is not running, such as serving requested resources from a cache, sending push notifications, running background fetch tasks, badging icons, and so on.</span></span>  <span data-ttu-id="63e7b-146">Os funcionários do serviço são definidos em um arquivo JavaScript especial.</span><span class="sxs-lookup"><span data-stu-id="63e7b-146">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="63e7b-147">Para obter mais informações, consulte [usando trabalhadores do serviço][MDNUsingServiceWorkers] e a [API do serviço de trabalho][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="63e7b-147">For more information, see [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="63e7b-148">Para criar um trabalho de serviço em seu projeto, use a primeira receita do trabalho do serviço de **rede cache** do [PWA Builder][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="63e7b-148">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="63e7b-149">Navegue até [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], selecione o trabalho do primeiro serviço de **rede em cache** e selecione o botão **baixar** .</span><span class="sxs-lookup"><span data-stu-id="63e7b-149">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="63e7b-150">O arquivo baixado contém os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="63e7b-150">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="63e7b-151">Copie os arquivos baixados para a `public` pasta no seu projeto de aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="63e7b-151">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="63e7b-152">No código VS, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.</span><span class="sxs-lookup"><span data-stu-id="63e7b-152">In VS Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="63e7b-153">Seu aplicativo Web agora tem um trabalho de serviço que usa a primeira estratégia de cache, que busca recursos como imagens, JS, CSS e HTML do cache primeiro, e retorna à rede conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="63e7b-153">Your web app now has a service worker that uses the cache-first strategy, which fetches resources like images, JS, CSS, and HTML from the cache first, and falls back to the network as needed.</span></span>  

<span data-ttu-id="63e7b-154">Use as etapas a seguir para confirmar a execução do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="63e7b-154">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="63e7b-155">Navegue até seu aplicativo Web usando `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="63e7b-155">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="63e7b-156">Se o seu aplicativo Web não estiver disponível, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="63e7b-156">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="63e7b-157">No Microsoft Edge, selecione `F12` para abrir o Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="63e7b-157">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="63e7b-158">Selecione **aplicativo**e, em seguida, selecione os **funcionários** do serviço para exibir os funcionários do serviço.</span><span class="sxs-lookup"><span data-stu-id="63e7b-158">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="63e7b-159">Se você não vir o trabalhador do serviço, talvez seja necessário atualizar a página.</span><span class="sxs-lookup"><span data-stu-id="63e7b-159">If you do not see the service worker, you may need to refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Visão geral do trabalhador do serviço Microsoft Edge DevTools":::
       <span data-ttu-id="63e7b-161">Visão geral do trabalhador do serviço Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63e7b-161">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="63e7b-162">Exiba o cache do serviço de trabalho expandindo o **armazenamento de cache** e selecione **pwabuilder-cache**.</span><span class="sxs-lookup"><span data-stu-id="63e7b-162">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="63e7b-163">Você deve ver todos os recursos armazenados em cache pelo trabalhador do serviço, como o ícone do aplicativo, manifesto do aplicativo, arquivos CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63e7b-163">You should see all the resources cached by the service worker, such as the app icon, app manifest, CSS and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache do trabalho do serviço no Microsoft Edge DevTools":::
       <span data-ttu-id="63e7b-165">Cache do trabalho do serviço no Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="63e7b-165">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="63e7b-166">Experimente o seu PWA como um aplicativo offline.</span><span class="sxs-lookup"><span data-stu-id="63e7b-166">Try your PWA as an offline app.</span></span>  <span data-ttu-id="63e7b-167">No Microsoft Edge DevTools \ ( `F12` \), escolha **rede** e altere o status **online** para **offline**.</span><span class="sxs-lookup"><span data-stu-id="63e7b-167">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Configurando o aplicativo para o modo offline no Microsoft Edge DevTools":::
       <span data-ttu-id="63e7b-169">Configurando o aplicativo para o modo offline no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="63e7b-169">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="63e7b-170">Atualize o aplicativo e veja se ele está funcionando offline, servindo os recursos do seu aplicativo do cache.</span><span class="sxs-lookup"><span data-stu-id="63e7b-170">Refresh your app and you should see it working offline by serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA em execução offline":::
       <span data-ttu-id="63e7b-172">PWA em execução offline</span><span class="sxs-lookup"><span data-stu-id="63e7b-172">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="63e7b-173">Adicionar notificações por push ao seu PWA</span><span class="sxs-lookup"><span data-stu-id="63e7b-173">Add push notifications to your PWA</span></span>  

<span data-ttu-id="63e7b-174">Você pode criar PWAs que dão suporte a notificações por push completando as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="63e7b-174">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="63e7b-175">Assinar um serviço de mensagens usando a [API de envio][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="63e7b-175">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="63e7b-176">Exibir mensagens do sistema quando uma mensagem é recebida do serviço usando a [API de notificações][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="63e7b-176">Display a toast messages when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  

<span data-ttu-id="63e7b-177">Da mesma forma que com os profissionais do serviço, são APIs baseadas em padrões que funcionam entre navegadores, portanto, você só precisa escrever o código uma vez para que ele funcione em qualquer lugar com suporte para o PWAs.</span><span class="sxs-lookup"><span data-stu-id="63e7b-177">As with Service Workers, these are standards-based APIs that work across browsers, so you only have to write the code once for it to work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="63e7b-178">Para obter mais informações sobre como enviar mensagens push para navegadores diferentes em seu servidor, use a biblioteca de fonte aberta do [Push Web][NPMWebPush] .</span><span class="sxs-lookup"><span data-stu-id="63e7b-178">For more information on delivering push messages to different browsers on your server, use the [Web-Push][NPMWebPush] open-source library.</span></span>  

<span data-ttu-id="63e7b-179">As etapas a seguir foram adaptadas da demonstração avançada push no [livro do serviço de trabalho][ServiceWorkerCookbookPushRichDemo] do entanto, que tem uma série de outras receitas úteis de trabalho de serviço e envio da Web.</span><span class="sxs-lookup"><span data-stu-id="63e7b-179">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="63e7b-180">Etapa 1-gerar chaves VAPID</span><span class="sxs-lookup"><span data-stu-id="63e7b-180">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="63e7b-181">As notificações por push exigem chaves VAPID \ (identificação do servidor de aplicativos voluntários \) para enviar mensagens de envio para o cliente PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-181">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="63e7b-182">Há vários geradores de chave VAPID disponíveis online \ (por exemplo, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="63e7b-182">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="63e7b-183">Após a geração, você deve obter um objeto JSON que contém uma chave pública e privada.</span><span class="sxs-lookup"><span data-stu-id="63e7b-183">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="63e7b-184">Salve as chaves para etapas subsequentes no tutorial a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e7b-184">Save the keys for subsequent steps in the following tutorial.</span></span>  <span data-ttu-id="63e7b-185">Para obter informações sobre como o VAPID e o webpush funcionam, consulte [enviando notificações webpush identificadas pelo serviço de envio do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="63e7b-185">For information on how VAPID and WebPush works, see [Sending VAPID identified WebPush Notifications via Mozilla's Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="63e7b-186">Etapa 2-assinar notificações por push</span><span class="sxs-lookup"><span data-stu-id="63e7b-186">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="63e7b-187">Os funcionários de serviço lidam com eventos de push e interações de notificação do sistema no seu PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-187">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="63e7b-188">Para assinar o PWA para notificações por push de servidor, verifique se as seguintes condições foram atendidas.</span><span class="sxs-lookup"><span data-stu-id="63e7b-188">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="63e7b-189">Seu PWA está instalado, ativo e cadastrado</span><span class="sxs-lookup"><span data-stu-id="63e7b-189">Your PWA is installed, active and registered</span></span>  
*   <span data-ttu-id="63e7b-190">Seu código que executa a tarefa de assinatura está no thread da interface do usuário principal do PWA</span><span class="sxs-lookup"><span data-stu-id="63e7b-190">Your code that performs the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="63e7b-191">Você tem conectividade de rede</span><span class="sxs-lookup"><span data-stu-id="63e7b-191">You have network connectivity</span></span>  

<span data-ttu-id="63e7b-192">Antes da criação de uma nova assinatura de envio, o Microsoft Edge verifica se o usuário concedeu permissão ao PWA para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="63e7b-192">Before a new push subscription is created, Microsoft Edge checks if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="63e7b-193">Caso contrário, o usuário será solicitado a confirmar a permissão do navegador.</span><span class="sxs-lookup"><span data-stu-id="63e7b-193">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="63e7b-194">Se a permissão for negada, a solicitação para `registration.pushManager.subscribe` lançar uma `DOMException` , que deve ser manipulada.</span><span class="sxs-lookup"><span data-stu-id="63e7b-194">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="63e7b-195">Para saber mais sobre o gerenciamento de permissões, consulte [notificações por push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="63e7b-195">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="63e7b-196">Em seu `pwabuilder-sw-register.js` arquivo, acrescente o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e7b-196">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="63e7b-197">Para obter mais informações, consulte o [pushmanager][MDNPushManager] e [a Web-Push][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="63e7b-197">For more information, see [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="63e7b-198">Etapa 3-ouvir as notificações por push</span><span class="sxs-lookup"><span data-stu-id="63e7b-198">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="63e7b-199">Agora que uma assinatura está configurada no PWA, adicione manipuladores ao trabalhador do serviço para responder a eventos Push \ (enviado do servidor \) para exibir notificações do sistema com os dados de uma mensagem recebida.</span><span class="sxs-lookup"><span data-stu-id="63e7b-199">Now that a subscription is set up in your PWA, add handlers to the service worker to respond to push events \(sent from the server\) to display toast notifications with the data of a received message.</span></span>  <span data-ttu-id="63e7b-200">Você deve adicionar um manipulador de clique para executar qualquer uma das seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="63e7b-200">You must add a click handler to perform the any of the following tasks.</span></span>  
*   <span data-ttu-id="63e7b-201">ignorar a notificação do sistema</span><span class="sxs-lookup"><span data-stu-id="63e7b-201">dismiss the toast notification</span></span>  
*   <span data-ttu-id="63e7b-202">abrir, focalizar ou abrir e focalizar qualquer janelas abertas</span><span class="sxs-lookup"><span data-stu-id="63e7b-202">open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="63e7b-203">abrir e focalizar uma nova janela para exibir uma página do cliente PWA</span><span class="sxs-lookup"><span data-stu-id="63e7b-203">open and focus a new window to display a PWA client page</span></span>  

<span data-ttu-id="63e7b-204">Em seu `pwabuilder-sw.js` arquivo, adicione os manipuladores a seguir.</span><span class="sxs-lookup"><span data-stu-id="63e7b-204">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <span data-ttu-id="63e7b-205">Etapa 4-experimentar</span><span class="sxs-lookup"><span data-stu-id="63e7b-205">Step 4 - Try it out</span></span>  

<span data-ttu-id="63e7b-206">Execute as etapas a seguir para testar as notificações por push no PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-206">Perform the following steps to test push notifications in your PWA.</span></span>  

1.  <span data-ttu-id="63e7b-207">Navegue até o seu PWA em `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="63e7b-207">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="63e7b-208">Quando o trabalhador do serviço é ativado e tenta assinar notificações por push pelo PWA, o Microsoft Edge solicita que o seu PWA mostre notificações.</span><span class="sxs-lookup"><span data-stu-id="63e7b-208">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="63e7b-209">Selecione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="63e7b-209">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Caixa de diálogo de permissão para habilitar notificações":::
       <span data-ttu-id="63e7b-211">Caixa de diálogo de permissão para habilitar notificações</span><span class="sxs-lookup"><span data-stu-id="63e7b-211">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
    
1.  <span data-ttu-id="63e7b-212">Simule uma notificação por push do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="63e7b-212">Simulate a server-side push notification.</span></span>  <span data-ttu-id="63e7b-213">Com o seu PWA aberto em `http://localhost:3000` no navegador, selecione `F12` para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="63e7b-213">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="63e7b-214">Escolha **Application**  >  **Service Worker**  >  **envio** de trabalhador de serviço de aplicativo para enviar uma notificação por push de teste ao seu PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-214">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  <span data-ttu-id="63e7b-215">Você verá uma notificação por push exibida próxima à barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="63e7b-215">You should see a push notification appear near the taskbar.</span></span>  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Enviar uma notificação por push de DevTools":::
       <span data-ttu-id="63e7b-217">Enviar uma notificação por push de DevTools</span><span class="sxs-lookup"><span data-stu-id="63e7b-217">Push a notification from DevTools</span></span>
    :::image-end:::
     
    <span data-ttu-id="63e7b-218">Se você não selecionar \ (ou ativar \) uma notificação do sistema, ela será ignorada após vários segundos e será colocada em fila na central de ações do Windows.</span><span class="sxs-lookup"><span data-stu-id="63e7b-218">If you do not select \(or activate\) a toast notification, it is dismissed after several seconds and queues up in your Windows Action Center.</span></span>  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificações na central de ações do Windows":::
       <span data-ttu-id="63e7b-220">Notificações na central de ações do Windows</span><span class="sxs-lookup"><span data-stu-id="63e7b-220">Notifications in Windows Action Center</span></span>
    :::image-end:::
    
    
## <span data-ttu-id="63e7b-221">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="63e7b-221">Next steps</span></span>  

<span data-ttu-id="63e7b-222">Veja a seguir uma lista de tarefas adicionais a serem aprendidas ao criar PWAs do mundo real:</span><span class="sxs-lookup"><span data-stu-id="63e7b-222">The following is a list of additional tasks to learn when building real-world PWAs:</span></span>  

*  <span data-ttu-id="63e7b-223">Gerenciar e armazenar assinaturas push</span><span class="sxs-lookup"><span data-stu-id="63e7b-223">Manage and store push subscriptions</span></span>  
*  <span data-ttu-id="63e7b-224">[Criptografar][NPMWebPushEncrypt] dados de carga</span><span class="sxs-lookup"><span data-stu-id="63e7b-224">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*  <span data-ttu-id="63e7b-225">Design dinâmico</span><span class="sxs-lookup"><span data-stu-id="63e7b-225">Responsive design</span></span>  
*  <span data-ttu-id="63e7b-226">Vinculação profunda</span><span class="sxs-lookup"><span data-stu-id="63e7b-226">Deep-linking</span></span>  
*  [<span data-ttu-id="63e7b-227">Teste entre navegadores</span><span class="sxs-lookup"><span data-stu-id="63e7b-227">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*  <span data-ttu-id="63e7b-228">Implementar práticas recomendadas, como [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="63e7b-228">Implement best practices such as [Webhint][Webhint]</span></span>  

## <span data-ttu-id="63e7b-229">Consulte também</span><span class="sxs-lookup"><span data-stu-id="63e7b-229">See also</span></span>  

*   <span data-ttu-id="63e7b-230">[Aplicativos Web progressivos em MDN Web docs][MDNProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="63e7b-230">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps].</span></span>  
*   <span data-ttu-id="63e7b-231">[Aplicativos Web progressivos em Web. dev][WebDevProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="63e7b-231">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps].</span></span>  
*   <span data-ttu-id="63e7b-232">[Leitores de notícias de hackers como Web Apps progressivos][HackerNewsProgressiveWebApps] – compara estruturas e padrões de desempenho diferentes para implementar uma amostra \ (leitor de notícias de hackers \) PWA.</span><span class="sxs-lookup"><span data-stu-id="63e7b-232">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publicar no serviço de aplicativo do Azure-criar um aplicativo node. js e Express no Visual Studio | Documentos da Microsoft"  

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

[NodejsMain]: https://nodejs.org "Node. js"  

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
