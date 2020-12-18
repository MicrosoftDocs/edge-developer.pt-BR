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
# <span data-ttu-id="9f603-104">Introdução aos aplicativos Web progressivos (Chromium)</span><span class="sxs-lookup"><span data-stu-id="9f603-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="9f603-105">Aplicativos Web progressivos \ (PWAs \) são aplicativos Web que são [aprimorados progressivamente][WikiProgressiveEnhancement].</span><span class="sxs-lookup"><span data-stu-id="9f603-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="9f603-106">Os aprimoramentos progressivos incluem recursos semelhantes a aplicativos, como instalação, suporte offline e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="9f603-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="9f603-107">Você também pode empacotar seu PWA para repositórios de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9f603-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="9f603-108">Possíveis repositórios de aplicativos incluem a Microsoft Store, Google Play, Mac App Store e muito mais.</span><span class="sxs-lookup"><span data-stu-id="9f603-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="9f603-109">A Microsoft Store é a loja de aplicativos comerciais interna do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9f603-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="9f603-110">O guia a seguir fornece uma visão geral das noções básicas do PWA ao criar um aplicativo Web simples e prorroga-lo como PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="9f603-111">O projeto concluído funciona em navegadores modernos.</span><span class="sxs-lookup"><span data-stu-id="9f603-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="9f603-112">Você pode usar o [PWABuilder][PwaBuilder] para criar um novo PWA, aprimorar o PWA existente ou empacotar seu PWA para repositórios de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9f603-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="9f603-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9f603-113">Prerequisites</span></span>  

*   <span data-ttu-id="9f603-114">Use o [código do Visual Studio][VisualstudioCodeMain] para editar o código-fonte do PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="9f603-115">Use [Node.js][NodejsMain] como seu servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="9f603-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <span data-ttu-id="9f603-116">Criar um aplicativo Web básico</span><span class="sxs-lookup"><span data-stu-id="9f603-116">Create a basic web app</span></span>  

<span data-ttu-id="9f603-117">Para criar um aplicativo Web vazio, siga as etapas no [aplicativo nó Express app Generator][ExpressjsApplicationGenerator]e nomeie seu aplicativo `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="9f603-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="9f603-118">No prompt, execute os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="9f603-119">Os comandos criam um aplicativo Web vazio e instalam as dependências.</span><span class="sxs-lookup"><span data-stu-id="9f603-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="9f603-120">Agora você tem um aplicativo Web funcional simples.</span><span class="sxs-lookup"><span data-stu-id="9f603-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="9f603-121">Para iniciar seu aplicativo Web, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="9f603-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="9f603-122">Agora, navegue até `http://localhost:3000` para exibir seu novo aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9f603-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Executando seu novo PWA no localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="9f603-124">Executando seu novo PWA no localhost</span><span class="sxs-lookup"><span data-stu-id="9f603-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="9f603-125">Começar a criar um PWA</span><span class="sxs-lookup"><span data-stu-id="9f603-125">Get started building a PWA</span></span>  

<span data-ttu-id="9f603-126">Agora que você tem um aplicativo Web simples, estenda-o como um PWA adicionando os três requisitos para PWAs</span><span class="sxs-lookup"><span data-stu-id="9f603-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="9f603-127">: [Https](#step-1---use-https), um [manifesto do aplicativo Web](#step-2---create-a-web-app-manifest)e um [trabalho de serviço](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="9f603-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="9f603-128">Etapa 1: usar HTTPS</span><span class="sxs-lookup"><span data-stu-id="9f603-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="9f603-129">As principais partes da plataforma PWA, como [funcionários de serviço][MDNServiceWorkerApi], exigem o uso de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9f603-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="9f603-130">Quando o seu PWA ficar ao vivo, você deverá publicá-lo em uma URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9f603-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="9f603-131">Para fins de depuração, o Microsoft Edge também permite `http://localhost` usar as APIs do PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="9f603-132">[Publicar seu aplicativo Web como um site ativo][VisualStudioNodejsTutorialPublishAzureAppService], mas verifique se o servidor está configurado para https.</span><span class="sxs-lookup"><span data-stu-id="9f603-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="9f603-133">Por exemplo, você pode criar uma [conta do Azure grátis][AzureCreateFreeAccount].</span><span class="sxs-lookup"><span data-stu-id="9f603-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="9f603-134">Hospede seu site no [serviço de aplicativo do Microsoft Azure][AzureWebApps] e ele é servido por HTTPS por padrão.</span><span class="sxs-lookup"><span data-stu-id="9f603-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="9f603-135">O guia a seguir, use `http://localhost` para criar seu PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="9f603-136">Etapa 2-criar um manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="9f603-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="9f603-137">Um [manifesto do aplicativo Web][MDNWebAppManifest] é um arquivo JSON que contém metadados sobre o seu aplicativo, como nome, descrição, ícones e muito mais.</span><span class="sxs-lookup"><span data-stu-id="9f603-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="9f603-138">Para adicionar um manifesto do aplicativo ao aplicativo Web:</span><span class="sxs-lookup"><span data-stu-id="9f603-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="9f603-139">No código do Visual Studio, escolha **arquivo**  >  **abrir pasta** e escolha o `MySamplePwa` diretório que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9f603-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="9f603-140">Selecione `Ctrl` + `N` para criar um novo arquivo e cole no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="9f603-141">Salve o arquivo como `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="9f603-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="9f603-142">Adicione uma imagem do ícone do aplicativo 512x512 chamado `icon512.png` to `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="9f603-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="9f603-143">Você pode usar a [imagem de exemplo][ImagePwa] para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="9f603-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="9f603-144">No código do Visual Studio, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.</span><span class="sxs-lookup"><span data-stu-id="9f603-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="9f603-145">Etapa 3: adicionar um trabalhador de serviço</span><span class="sxs-lookup"><span data-stu-id="9f603-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="9f603-146">Os funcionários de serviço são a tecnologia principal por trás do PWAs, permitindo cenários como suporte offline, cache avançado e executar tarefas em segundo plano anteriormente limitadas a aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="9f603-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="9f603-147">Os funcionários de serviço são tarefas em segundo plano que interceptam solicitações de rede de seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9f603-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="9f603-148">Os funcionários do serviço tentam concluir as tarefas, mesmo quando o seu PWA não está em execução.</span><span class="sxs-lookup"><span data-stu-id="9f603-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="9f603-149">As tarefas incluem as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="9f603-150">Servindo os recursos solicitados de um cache</span><span class="sxs-lookup"><span data-stu-id="9f603-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="9f603-151">Enviar notificações por push</span><span class="sxs-lookup"><span data-stu-id="9f603-151">Sending push notifications</span></span>  
*   <span data-ttu-id="9f603-152">Executar tarefas de busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9f603-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="9f603-153">Ícones de selos</span><span class="sxs-lookup"><span data-stu-id="9f603-153">Badging icons</span></span>  
*   <span data-ttu-id="9f603-154">e muito mais</span><span class="sxs-lookup"><span data-stu-id="9f603-154">and more</span></span>  
    
<span data-ttu-id="9f603-155">Os funcionários do serviço são definidos em um arquivo JavaScript especial.</span><span class="sxs-lookup"><span data-stu-id="9f603-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="9f603-156">Para obter mais informações, navegue para [usando trabalhadores do serviço][MDNUsingServiceWorkers] e a [API do serviço de trabalho][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="9f603-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="9f603-157">Para criar um trabalho de serviço em seu projeto, use a primeira receita do trabalho do serviço de **rede cache** do [PWA Builder][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="9f603-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="9f603-158">Navegue até [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], selecione o trabalho do primeiro serviço de **rede em cache** e selecione o botão **baixar** .</span><span class="sxs-lookup"><span data-stu-id="9f603-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="9f603-159">O arquivo baixado contém os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="9f603-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="9f603-160">Copie os arquivos baixados para a `public` pasta no seu projeto de aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="9f603-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="9f603-161">No código do Visual Studio, abra `/public/index.html` e adicione o trecho de código a seguir dentro da `<head>` marca.</span><span class="sxs-lookup"><span data-stu-id="9f603-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="9f603-162">Seu aplicativo Web agora tem um trabalho de serviço que usa a primeira estratégia cache.</span><span class="sxs-lookup"><span data-stu-id="9f603-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="9f603-163">O novo trabalho de serviço busca recursos do cache primeiro e da rede apenas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="9f603-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="9f603-164">Os recursos armazenados em cache incluem imagens, JavaScript, CSS e HTML.</span><span class="sxs-lookup"><span data-stu-id="9f603-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="9f603-165">Use as etapas a seguir para confirmar a execução do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="9f603-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="9f603-166">Navegue até seu aplicativo Web usando `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="9f603-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="9f603-167">Se o seu aplicativo Web não estiver disponível, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="9f603-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="9f603-168">No Microsoft Edge, selecione `F12` para abrir o Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="9f603-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="9f603-169">Selecione **aplicativo**e, em seguida, selecione os **funcionários** do serviço para exibir os funcionários do serviço.</span><span class="sxs-lookup"><span data-stu-id="9f603-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="9f603-170">Se o trabalhador do serviço não for exibido, atualize a página.</span><span class="sxs-lookup"><span data-stu-id="9f603-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Visão geral do trabalhador do serviço Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="9f603-172">Visão geral do trabalhador do serviço Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9f603-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9f603-173">Exiba o cache do serviço de trabalho expandindo o **armazenamento de cache** e selecione **pwabuilder-cache**.</span><span class="sxs-lookup"><span data-stu-id="9f603-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="9f603-174">Todos os recursos armazenados em cache pelo trabalhador do serviço devem ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="9f603-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="9f603-175">Os recursos armazenados em cache pelo trabalhador do serviço incluem o ícone do aplicativo, manifesto do aplicativo, CSS e arquivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9f603-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache do trabalho do serviço no Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="9f603-177">Cache do trabalho do serviço no Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="9f603-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9f603-178">Experimente o seu PWA como um aplicativo offline.</span><span class="sxs-lookup"><span data-stu-id="9f603-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="9f603-179">No Microsoft Edge DevTools \ ( `F12` \), escolha **rede** e altere o status **online** para **offline**.</span><span class="sxs-lookup"><span data-stu-id="9f603-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Configurando o aplicativo para o modo offline no Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="9f603-181">Configurando o aplicativo para o modo offline no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9f603-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9f603-182">Atualize seu aplicativo e ele deve exibir o mecanismo offline para servir os recursos de seu aplicativo a partir do cache.</span><span class="sxs-lookup"><span data-stu-id="9f603-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA em execução offline" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="9f603-184">PWA em execução offline</span><span class="sxs-lookup"><span data-stu-id="9f603-184">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="9f603-185">Adicionar notificações por push ao seu PWA</span><span class="sxs-lookup"><span data-stu-id="9f603-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="9f603-186">Você pode criar PWAs que dão suporte a notificações por push completando as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="9f603-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="9f603-187">Assinar um serviço de mensagens usando a [API de envio][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="9f603-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="9f603-188">Exibir uma mensagem de notificação do sistema quando uma mensagem é recebida do serviço usando a [API de notificações][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="9f603-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="9f603-189">Assim como acontece com trabalhadores de serviço, as APIs de notificação por push são APIs baseadas em padrões.</span><span class="sxs-lookup"><span data-stu-id="9f603-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="9f603-190">As APIs de notificação por push funcionam entre navegadores, portanto, o código deve funcionar em qualquer lugar no qual o PWAs for compatível.</span><span class="sxs-lookup"><span data-stu-id="9f603-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="9f603-191">Para obter mais informações sobre como enviar mensagens push para navegadores diferentes em seu servidor, navegue até [Internet-Push][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="9f603-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="9f603-192">As etapas a seguir foram adaptadas da demonstração avançada push no [livro do serviço de trabalho][ServiceWorkerCookbookPushRichDemo] do entanto, que tem uma série de outras receitas úteis de trabalho de serviço e envio da Web.</span><span class="sxs-lookup"><span data-stu-id="9f603-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="9f603-193">Etapa 1-gerar chaves VAPID</span><span class="sxs-lookup"><span data-stu-id="9f603-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="9f603-194">As notificações por push exigem chaves VAPID \ (identificação do servidor de aplicativos voluntários \) para enviar mensagens de envio para o cliente PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="9f603-195">Há vários geradores de chave VAPID disponíveis online \ (por exemplo, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="9f603-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="9f603-196">Após a geração, você deve obter um objeto JSON que contém uma chave pública e privada.</span><span class="sxs-lookup"><span data-stu-id="9f603-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="9f603-197">Salve as chaves para etapas posteriores do tutorial a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="9f603-198">Para obter informações sobre o VAPID e o webpush, navegue para [Enviar VAPID notificações webpush identificadas usando o serviço de envio do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="9f603-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="9f603-199">Etapa 2-assinar notificações por push</span><span class="sxs-lookup"><span data-stu-id="9f603-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="9f603-200">Os funcionários de serviço lidam com eventos de push e interações de notificação do sistema no seu PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="9f603-201">Para assinar o PWA para notificações por push de servidor, verifique se as seguintes condições foram atendidas.</span><span class="sxs-lookup"><span data-stu-id="9f603-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="9f603-202">Seu PWA está instalado, ativo e cadastrado</span><span class="sxs-lookup"><span data-stu-id="9f603-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="9f603-203">Seu código para concluir a tarefa de assinatura está no thread da interface do usuário principal do PWA</span><span class="sxs-lookup"><span data-stu-id="9f603-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="9f603-204">Você tem conectividade de rede</span><span class="sxs-lookup"><span data-stu-id="9f603-204">You have network connectivity</span></span>  
    
<span data-ttu-id="9f603-205">Antes da criação de uma nova assinatura de envio, o Microsoft Edge verifica se o usuário concedeu permissão ao PWA para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="9f603-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="9f603-206">Caso contrário, o usuário será solicitado a confirmar a permissão do navegador.</span><span class="sxs-lookup"><span data-stu-id="9f603-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="9f603-207">Se a permissão for negada, a solicitação para `registration.pushManager.subscribe` lançar uma `DOMException` , que deve ser manipulada.</span><span class="sxs-lookup"><span data-stu-id="9f603-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="9f603-208">Para saber mais sobre o gerenciamento de permissões, navegue até [notificações por push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="9f603-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="9f603-209">Em seu `pwabuilder-sw-register.js` arquivo, acrescente o trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="9f603-210">Para obter mais informações, navegue até o [pushmanager][MDNPushManager] e [com a Web-Push][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="9f603-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="9f603-211">Etapa 3-ouvir as notificações por push</span><span class="sxs-lookup"><span data-stu-id="9f603-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="9f603-212">Após a criação de uma assinatura no PWA, adicione manipuladores ao trabalhador do serviço para responder a eventos de envio.</span><span class="sxs-lookup"><span data-stu-id="9f603-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="9f603-213">O evento Push é enviado do servidor para exibir notificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="9f603-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="9f603-214">Notificações do sistema exibem dados de uma mensagem recebida.</span><span class="sxs-lookup"><span data-stu-id="9f603-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="9f603-215">Para concluir as tarefas a seguir, você deve adicionar um manipulador de clique.</span><span class="sxs-lookup"><span data-stu-id="9f603-215">To complete the following tasks, you must add a click handler.</span></span>  

*   <span data-ttu-id="9f603-216">Ignorar a notificação do sistema</span><span class="sxs-lookup"><span data-stu-id="9f603-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="9f603-217">Abrir, focalizar ou abrir e focalizar qualquer janelas abertas</span><span class="sxs-lookup"><span data-stu-id="9f603-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="9f603-218">Abrir e focalizar uma nova janela para exibir uma página do cliente PWA</span><span class="sxs-lookup"><span data-stu-id="9f603-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="9f603-219">Em seu `pwabuilder-sw.js` arquivo, adicione os manipuladores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <span data-ttu-id="9f603-220">Etapa 4-experimentar</span><span class="sxs-lookup"><span data-stu-id="9f603-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="9f603-221">Para testar as notificações por push do seu PWA, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f603-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="9f603-222">Navegue até o seu PWA em `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="9f603-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="9f603-223">Quando o trabalhador do serviço é ativado e tenta assinar notificações por push pelo PWA, o Microsoft Edge solicita que o seu PWA mostre notificações.</span><span class="sxs-lookup"><span data-stu-id="9f603-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="9f603-224">Selecione **permitir**.</span><span class="sxs-lookup"><span data-stu-id="9f603-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Caixa de diálogo de permissão para habilitar notificações" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="9f603-226">Caixa de diálogo de permissão para habilitar notificações</span><span class="sxs-lookup"><span data-stu-id="9f603-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="9f603-227">Simule uma notificação por push do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="9f603-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="9f603-228">Com o seu PWA aberto em `http://localhost:3000` no navegador, selecione `F12` para abrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="9f603-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="9f603-229">Escolha \*\*\*\*  >  \*\*\*\*  >  **envio** de trabalhador de serviço de aplicativo para enviar uma notificação por push de teste ao seu PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="9f603-230">Uma notificação por push deve ser exibida perto da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9f603-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Enviar uma notificação por push de DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="9f603-232">Enviar uma notificação por push de DevTools</span><span class="sxs-lookup"><span data-stu-id="9f603-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="9f603-233">Se você não selecionar \ (ou ativar \) uma notificação do sistema, o sistema a descartará automaticamente após vários segundos e a enfileirará na sua central de ações do Windows.</span><span class="sxs-lookup"><span data-stu-id="9f603-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificações na central de ações do Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="9f603-235">Notificações na central de ações do Windows</span><span class="sxs-lookup"><span data-stu-id="9f603-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="9f603-236">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="9f603-236">Next steps</span></span>  

<span data-ttu-id="9f603-237">As etapas a seguir incluem tarefas adicionais para ajudá-lo a entender a criação de PWAss do mundo real.</span><span class="sxs-lookup"><span data-stu-id="9f603-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="9f603-238">Gerenciar e armazenar assinaturas push</span><span class="sxs-lookup"><span data-stu-id="9f603-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="9f603-239">[Criptografar][NPMWebPushEncrypt] dados de carga</span><span class="sxs-lookup"><span data-stu-id="9f603-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="9f603-240">Design dinâmico</span><span class="sxs-lookup"><span data-stu-id="9f603-240">Responsive design</span></span>  
*   <span data-ttu-id="9f603-241">Vinculação profunda</span><span class="sxs-lookup"><span data-stu-id="9f603-241">Deep-linking</span></span>  
*   [<span data-ttu-id="9f603-242">Teste entre navegadores</span><span class="sxs-lookup"><span data-stu-id="9f603-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="9f603-243">Implementar práticas de validação e teste, como [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="9f603-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <span data-ttu-id="9f603-244">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9f603-244">See also</span></span>  

*   [<span data-ttu-id="9f603-245">Aplicativos Web progressivos em documentos da Web do MDN</span><span class="sxs-lookup"><span data-stu-id="9f603-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="9f603-246">Aplicativos Web progressivos em Web. dev</span><span class="sxs-lookup"><span data-stu-id="9f603-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="9f603-247">[Leitores de notícias de hackers como Web Apps progressivos][HackerNewsProgressiveWebApps] – compara estruturas e padrões de desempenho diferentes para implementar uma amostra \ (leitor de notícias de hackers \) PWA.</span><span class="sxs-lookup"><span data-stu-id="9f603-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="9f603-248">Myth de PWAs</span><span class="sxs-lookup"><span data-stu-id="9f603-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="9f603-249">Um roteiro progressivo para seu aplicativo Web progressivo</span><span class="sxs-lookup"><span data-stu-id="9f603-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="9f603-250">Postagens offline com Web Apps progressivos</span><span class="sxs-lookup"><span data-stu-id="9f603-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="9f603-251">&DO PWA P A</span><span class="sxs-lookup"><span data-stu-id="9f603-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="9f603-252">Aposta na Web</span><span class="sxs-lookup"><span data-stu-id="9f603-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="9f603-253">Nomeando aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="9f603-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="9f603-254">Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 1)</span><span class="sxs-lookup"><span data-stu-id="9f603-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="9f603-255">Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 2)</span><span class="sxs-lookup"><span data-stu-id="9f603-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="9f603-256">Criando e criando um aplicativo Web progressivo sem uma estrutura (parte 3)</span><span class="sxs-lookup"><span data-stu-id="9f603-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
