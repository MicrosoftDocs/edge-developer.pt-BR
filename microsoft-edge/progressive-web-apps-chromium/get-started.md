---
description: Este guia fornece uma visão geral das noções básicas e ferramentas do PWA para a criação de Aplicativos Web Progressivos (Chromium) no Windows.
title: Começar com o Progressive Web Apps (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Borda, Windows, PWABuilder, manifesto da Web, serviço de trabalho, push
ms.openlocfilehash: 6a40742c1065dbc3b8aaeeeb469ab9154629a47a
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474905"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a><span data-ttu-id="e8ad6-104">Começar com o Progressive Web Apps (Chromium)</span><span class="sxs-lookup"><span data-stu-id="e8ad6-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="e8ad6-105">Os Aplicativos Web Progressivos \(PWAs\) são aplicativos Web que são [progressivamente aprimorados.][WikiProgressiveEnhancement]</span><span class="sxs-lookup"><span data-stu-id="e8ad6-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="e8ad6-106">Os aprimoramentos progressivos incluem recursos parecidos com aplicativos, como instalação, suporte offline e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="e8ad6-107">Você também pode empacotá-lo para lojas de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="e8ad6-108">Os possíveis armazenamentos de aplicativos incluem a Microsoft Store, Google Play, Mac App Store e muito mais.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="e8ad6-109">A Microsoft Store é a loja de aplicativos comerciais criada no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="e8ad6-110">O guia a seguir fornece uma visão geral das noções básicas do PWA criando um aplicativo Web simples e estendendo-o como um PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="e8ad6-111">O projeto concluído funciona em navegadores modernos.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="e8ad6-112">Você pode usar [o PWABuilder][PwaBuilder] para criar um novo PWA, aprimorar o PWA existente ou empacotar seu PWA para lojas de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="e8ad6-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e8ad6-113">Prerequisites</span></span>  

*   <span data-ttu-id="e8ad6-114">Use [Visual Studio Código][VisualstudioCodeMain] para editar o código-fonte do PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="e8ad6-115">Use [Node.js][NodejsMain] como seu servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <a name="create-a-basic-web-app"></a><span data-ttu-id="e8ad6-116">Criar um aplicativo Web básico</span><span class="sxs-lookup"><span data-stu-id="e8ad6-116">Create a basic web app</span></span>  

<span data-ttu-id="e8ad6-117">Para criar um aplicativo Web vazio, siga as etapas em [Node Express App Generator][ExpressjsApplicationGenerator]e nomee seu aplicativo `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="e8ad6-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="e8ad6-118">No prompt, execute os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="e8ad6-119">Os comandos criam um aplicativo Web vazio e instalam qualquer dependência.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="e8ad6-120">Agora você tem um aplicativo Web simples e funcional.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="e8ad6-121">Para iniciar seu aplicativo Web, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="e8ad6-122">Agora, navegue `http://localhost:3000` para exibir seu novo aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="Executando seu novo PWA no localhost" lightbox="./media/visual-studio-nodejs-express-index.png":::
   <span data-ttu-id="e8ad6-124">Executando seu novo PWA no localhost</span><span class="sxs-lookup"><span data-stu-id="e8ad6-124">Running your new PWA on localhost</span></span>  
:::image-end:::  

## <a name="get-started-building-a-pwa"></a><span data-ttu-id="e8ad6-125">Começar a criar um PWA</span><span class="sxs-lookup"><span data-stu-id="e8ad6-125">Get started building a PWA</span></span>  

<span data-ttu-id="e8ad6-126">Agora que você tem um aplicativo Web simples, estenda-o como um PWA adicionando os três requisitos para PWAs</span><span class="sxs-lookup"><span data-stu-id="e8ad6-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="e8ad6-127">: [HTTPS](#step-1---use-https), um [Manifesto do Aplicativo Web](#step-2---create-a-web-app-manifest)e um Trabalhador de [Serviço.](#step-3---add-a-service-worker)</span><span class="sxs-lookup"><span data-stu-id="e8ad6-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <a name="step-1---use-https"></a><span data-ttu-id="e8ad6-128">Etapa 1 - Usar HTTPS</span><span class="sxs-lookup"><span data-stu-id="e8ad6-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="e8ad6-129">As partes principais da plataforma PWA, como Os Trabalhadores [do Serviço,][MDNServiceWorkerApi]exigem o uso de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="e8ad6-130">Quando o PWA for ao vivo, você deverá publicá-lo em uma URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="e8ad6-131">Para fins de depuração, o Microsoft Edge também permite `http://localhost` usar as APIs do PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="e8ad6-132">[Publique seu aplicativo Web como um site ao vivo][VisualStudioNodejsTutorialPublishAzureAppService], mas verifique se o servidor está configurado para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="e8ad6-133">Por exemplo, você pode criar uma conta gratuita [do Azure.][AzureCreateFreeAccount]</span><span class="sxs-lookup"><span data-stu-id="e8ad6-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="e8ad6-134">Hospede seu site no Serviço de Aplicativo do [Microsoft Azure][AzureWebApps] e ele é servido por https por padrão.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="e8ad6-135">O guia a seguir, use `http://localhost` para criar seu PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <a name="step-2---create-a-web-app-manifest"></a><span data-ttu-id="e8ad6-136">Etapa 2 - Criar um Manifesto do Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e8ad6-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="e8ad6-137">Um [Manifesto do Aplicativo Web][MDNWebAppManifest] é um arquivo JSON que contém metadados sobre seu aplicativo, como nome, descrição, ícones e muito mais.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="e8ad6-138">Para adicionar um manifesto de aplicativo ao aplicativo Web:</span><span class="sxs-lookup"><span data-stu-id="e8ad6-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="e8ad6-139">Em Visual Studio Código, escolha **Arquivo**  >  **Abrir Pasta** e escolha o diretório que você criou `MySamplePwa` anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="e8ad6-140">Selecione `Ctrl` + `N` para criar um novo arquivo e colar no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="e8ad6-141">Salve o arquivo como `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="e8ad6-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="e8ad6-142">Adicione uma imagem de ícone do aplicativo 512x512 chamada `icon512.png` `/MySamplePwa/public/images` para .</span><span class="sxs-lookup"><span data-stu-id="e8ad6-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="e8ad6-143">Você pode usar a [imagem de exemplo para](./media/progressive-web-app.png) fins de teste.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-143">You may use the [sample image](./media/progressive-web-app.png) for testing purposes.</span></span>  
1.  <span data-ttu-id="e8ad6-144">Em Visual Studio Código, abra e adicione o seguinte trecho de `/public/index.html` código dentro da `<head>` marca.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a><span data-ttu-id="e8ad6-145">Etapa 3 - Adicionar um Trabalhador de Serviço</span><span class="sxs-lookup"><span data-stu-id="e8ad6-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="e8ad6-146">Os funcionários de serviço são a principal tecnologia por trás de PWAs, habilitando cenários como suporte offline, cache avançado e executando tarefas em segundo plano anteriormente limitadas a aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="e8ad6-147">Os funcionários de serviço são tarefas em segundo plano que interceptam solicitações de rede do seu aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="e8ad6-148">Os funcionários de serviço tentam concluir tarefas, mesmo quando o PWA não está em execução.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="e8ad6-149">As tarefas incluem as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="e8ad6-150">Servindo recursos solicitados de um cache</span><span class="sxs-lookup"><span data-stu-id="e8ad6-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="e8ad6-151">Enviando notificações por push</span><span class="sxs-lookup"><span data-stu-id="e8ad6-151">Sending push notifications</span></span>  
*   <span data-ttu-id="e8ad6-152">Executar tarefas de busca em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e8ad6-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="e8ad6-153">Ícones de badging</span><span class="sxs-lookup"><span data-stu-id="e8ad6-153">Badging icons</span></span>  
*   <span data-ttu-id="e8ad6-154">e mais</span><span class="sxs-lookup"><span data-stu-id="e8ad6-154">and more</span></span>  
    
<span data-ttu-id="e8ad6-155">Os funcionários de serviço são definidos em um arquivo JavaScript especial.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="e8ad6-156">Para obter mais informações, navegue até [Using Service Workers][MDNUsingServiceWorkers] and Service Worker [API][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="e8ad6-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="e8ad6-157">Para criar um funcionário de serviço em seu projeto, use a receita de trabalho de serviço de rede do **PWA** [Builder][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="e8ad6-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="e8ad6-158">Navegue [até pwabuilder.com/serviceworker][PwaBuilderServiceWorker], selecione o serviço de rede de cache **primeiro** e selecione o **botão Baixar.**</span><span class="sxs-lookup"><span data-stu-id="e8ad6-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="e8ad6-159">O arquivo baixado contém os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="e8ad6-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="e8ad6-160">Copie os arquivos baixados para a `public` pasta no projeto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="e8ad6-161">Em Visual Studio Código, abra e adicione o seguinte trecho de `/public/index.html` código dentro da `<head>` marca.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="e8ad6-162">Seu aplicativo Web agora tem um trabalhador de serviço que usa a estratégia de cache primeiro.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="e8ad6-163">Você novo funcionário de serviço busca recursos do cache primeiro e da rede apenas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="e8ad6-164">Os recursos armazenados em cache incluem imagens, JavaScript, CSS e HTML.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="e8ad6-165">Use as etapas a seguir para confirmar se o seu funcionário de serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="e8ad6-166">Navegue até seu aplicativo Web usando `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="e8ad6-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="e8ad6-167">Se seu aplicativo Web não estiver disponível, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="e8ad6-168">No Microsoft Edge, selecione `F12` para abrir o Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="e8ad6-169">Selecione **Aplicativo**, em **seguida, Service Workers** para exibir os funcionários do serviço.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="e8ad6-170">Se o trabalhador do serviço não for exibido, atualize a página.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Visão geral do Microsoft Edge DevTools Service Worker" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="e8ad6-172">Visão geral do Microsoft Edge DevTools Service Worker</span><span class="sxs-lookup"><span data-stu-id="e8ad6-172">Microsoft Edge DevTools Service Worker overview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e8ad6-173">Exibir o cache do trabalhador de serviço expandindo **o Armazenamento de Cache** e selecione **pwabuilder-precache**.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="e8ad6-174">Todos os recursos armazenados em cache pelo trabalhador do serviço devem ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="e8ad6-175">Os recursos armazenados em cache pelo trabalhador do serviço incluem o ícone do aplicativo, o manifesto do aplicativo, o CSS e os arquivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache de Trabalhador de Serviço no Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="e8ad6-177">Cache de Trabalhador de Serviço no Microsoft Edge DevTools \(F12\)</span><span class="sxs-lookup"><span data-stu-id="e8ad6-177">Service Worker cache in Microsoft Edge DevTools \(F12\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e8ad6-178">Experimente o PWA como um aplicativo offline.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="e8ad6-179">No Microsoft Edge DevTools \( `F12` \), escolha **Rede** e altere o status **online** para **Offline**.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Configurando o aplicativo para o modo offline no Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="e8ad6-181">Configurando o aplicativo para o modo offline no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e8ad6-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e8ad6-182">Atualize seu aplicativo e ele deve exibir o mecanismo offline para servir os recursos do seu aplicativo a partir do cache.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/visual-studio-nodejs-express-index.png" alt-text="PWA em execução offline" lightbox="./media/visual-studio-nodejs-express-index.png":::
       <span data-ttu-id="e8ad6-184">PWA em execução offline</span><span class="sxs-lookup"><span data-stu-id="e8ad6-184">PWA running offline</span></span>  
    :::image-end:::  
    
## <a name="add-push-notifications-to-your-pwa"></a><span data-ttu-id="e8ad6-185">Adicionar notificações por push ao seu PWA</span><span class="sxs-lookup"><span data-stu-id="e8ad6-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="e8ad6-186">Você pode criar PWAs que suportam notificações por push concluindo as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="e8ad6-187">Inscrever-se em um serviço de mensagens usando a [API push][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="e8ad6-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="e8ad6-188">Exibir uma mensagem de notificação quando uma mensagem é recebida do serviço usando a [API de Notificações][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="e8ad6-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="e8ad6-189">Assim como com Os Trabalhadores do Serviço, as APIs de notificação por push são APIs baseadas em padrões.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="e8ad6-190">As APIs de notificação por push funcionam em navegadores, portanto, seu código deve funcionar em todos os lugares com suporte para PWAs.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="e8ad6-191">Para obter mais informações sobre como entregar mensagens push para diferentes navegadores em seu servidor, navegue até [Web-Push][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="e8ad6-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="e8ad6-192">As etapas a seguir foram adaptadas do Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] fornecido pelo Mozilla, que tem várias outras receitas úteis de Web Push e de trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <a name="step-1---generate-vapid-keys"></a><span data-ttu-id="e8ad6-193">Etapa 1 - Gerar chaves VAPID</span><span class="sxs-lookup"><span data-stu-id="e8ad6-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="e8ad6-194">As notificações por push exigem teclas VAPID \(Voluntary Application Server Identification\) para enviar mensagens push ao cliente PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="e8ad6-195">Há vários geradores de chaves VAPID disponíveis online \(por exemplo, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="e8ad6-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="e8ad6-196">Após a geração, você deve obter um objeto JSON contendo uma chave pública e privada.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="e8ad6-197">Salve as chaves para etapas posteriores no tutorial a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="e8ad6-198">Para obter informações sobre VAPID e WebPush, navegue até Enviar notificações de [WebPush identificadas vapid usando o Serviço de Push do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="e8ad6-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <a name="step-2---subscribe-to-push-notifications"></a><span data-ttu-id="e8ad6-199">Etapa 2 - Inscrever-se em notificações por push</span><span class="sxs-lookup"><span data-stu-id="e8ad6-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="e8ad6-200">Os funcionários do serviço lidam com eventos de push e interações de notificação</span><span class="sxs-lookup"><span data-stu-id="e8ad6-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="e8ad6-201">Para assinar as notificações por push do PWA no servidor, certifique-se de que as seguintes condições sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="e8ad6-202">Seu PWA está instalado, ativo e registrado</span><span class="sxs-lookup"><span data-stu-id="e8ad6-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="e8ad6-203">Seu código para concluir a tarefa de assinatura está no thread principal da interface do usuário do PWA</span><span class="sxs-lookup"><span data-stu-id="e8ad6-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="e8ad6-204">Você tem conectividade de rede</span><span class="sxs-lookup"><span data-stu-id="e8ad6-204">You have network connectivity</span></span>  
    
<span data-ttu-id="e8ad6-205">Antes de uma nova assinatura por push ser criada, o Microsoft Edge verifica se o usuário concedeu a permissão do PWA para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="e8ad6-206">Caso não seja, o usuário será solicitado pelo navegador a pedir permissão.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="e8ad6-207">Se a permissão for negada, a solicitação para lançar `registration.pushManager.subscribe` um , que deve ser `DOMException` manipulado.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="e8ad6-208">Para obter mais informações sobre o gerenciamento de permissões, navegue até [Notificações por Push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="e8ad6-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="e8ad6-209">Em seu `pwabuilder-sw-register.js` arquivo, adendo o seguinte trecho de código.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="e8ad6-210">Para obter mais informações, navegue até [PushManager][MDNPushManager] e [Web-Push.][NPMWebPushUsage]</span><span class="sxs-lookup"><span data-stu-id="e8ad6-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <a name="step-3---listen-for-push-notifications"></a><span data-ttu-id="e8ad6-211">Etapa 3 - Escutar notificações por push</span><span class="sxs-lookup"><span data-stu-id="e8ad6-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="e8ad6-212">Depois que uma assinatura for criada no PWA, adicione manipuladores ao trabalhador do serviço para responder a eventos de push.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="e8ad6-213">O evento Push é enviado do servidor para exibir notificações de notificação</span><span class="sxs-lookup"><span data-stu-id="e8ad6-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="e8ad6-214">As notificações de notificação do</span><span class="sxs-lookup"><span data-stu-id="e8ad6-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="e8ad6-215">Para concluir as seguintes tarefas, você deve adicionar um `click` manipulador.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-215">To complete the following tasks, you must add a `click` handler.</span></span>  

*   <span data-ttu-id="e8ad6-216">Descartar a notificação de not</span><span class="sxs-lookup"><span data-stu-id="e8ad6-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="e8ad6-217">Abrir, focalizar ou abrir e focalizar todas as janelas abertas</span><span class="sxs-lookup"><span data-stu-id="e8ad6-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="e8ad6-218">Abra e foque em uma nova janela para exibir uma página de cliente PWA</span><span class="sxs-lookup"><span data-stu-id="e8ad6-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="e8ad6-219">Em seu `pwabuilder-sw.js` arquivo, adicione os seguintes manipuladores.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <a name="step-4---try-it-out"></a><span data-ttu-id="e8ad6-220">Etapa 4 - Experimente</span><span class="sxs-lookup"><span data-stu-id="e8ad6-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="e8ad6-221">Para testar notificações por push para seu PWA, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="e8ad6-222">Navegue até seu PWA em `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="e8ad6-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="e8ad6-223">Quando o seu funcionário de serviço é ativado e tenta inscrever seu PWA para notificações por push, o Microsoft Edge solicita que você permita que seu PWA mostre notificações.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="e8ad6-224">Selecione **Permitir**.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Caixa de diálogo De permissão para habilenciar notificações" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="e8ad6-226">Caixa de diálogo De permissão para habilenciar notificações</span><span class="sxs-lookup"><span data-stu-id="e8ad6-226">Permission dialog for enabling notifications</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e8ad6-227">Simular uma notificação por push do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="e8ad6-228">Com o PWA aberto `http://localhost:3000` no navegador, selecione `F12` abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="e8ad6-229">Escolha **Application**  >  **Service Worker**  >  **Push** para enviar uma notificação por push de teste ao seu PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="e8ad6-230">Uma notificação por push deve ser exibida perto da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Push a notification from DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="e8ad6-232">Push a notification from DevTools</span><span class="sxs-lookup"><span data-stu-id="e8ad6-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="e8ad6-233">Se você não selecionar \(ou ativar\) uma notificação de notificação do sistema, o sistema a descartará automaticamente após vários segundos e enfilá-la em sua Central de Ações do Windows.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notificações no Centro de Ações do Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="e8ad6-235">Notificações no Centro de Ações do Windows</span><span class="sxs-lookup"><span data-stu-id="e8ad6-235">Notifications in Windows Action Center</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="e8ad6-236">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="e8ad6-236">Next steps</span></span>  

<span data-ttu-id="e8ad6-237">As etapas a seguir incluem tarefas adicionais para ajudá-lo a entender a criação de PWAs reais.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="e8ad6-238">Gerenciar e armazenar assinaturas por push</span><span class="sxs-lookup"><span data-stu-id="e8ad6-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="e8ad6-239">[Criptografar][NPMWebPushEncrypt] dados de carga</span><span class="sxs-lookup"><span data-stu-id="e8ad6-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="e8ad6-240">Design dinâmico</span><span class="sxs-lookup"><span data-stu-id="e8ad6-240">Responsive design</span></span>  
*   <span data-ttu-id="e8ad6-241">Vinculação profunda</span><span class="sxs-lookup"><span data-stu-id="e8ad6-241">Deep-linking</span></span>  
*   [<span data-ttu-id="e8ad6-242">Teste entre navegadores</span><span class="sxs-lookup"><span data-stu-id="e8ad6-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="e8ad6-243">Implementar práticas de validação e teste, como [Webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="e8ad6-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="e8ad6-244">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e8ad6-244">See also</span></span>  

*   [<span data-ttu-id="e8ad6-245">Aplicativos Web progressivos em documentos web do MDN</span><span class="sxs-lookup"><span data-stu-id="e8ad6-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="e8ad6-246">Aplicativos Web progressivos no web.dev</span><span class="sxs-lookup"><span data-stu-id="e8ad6-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="e8ad6-247">[Leitores de Notícias do Hacker como Aplicativos Web Progressivos][HackerNewsProgressiveWebApps] - Compara diferentes estruturas e padrões de desempenho para implementar um exemplo \(Leitor de Notícias do Hacker\) PWA.</span><span class="sxs-lookup"><span data-stu-id="e8ad6-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="e8ad6-248">PWAs de estouros de míticos</span><span class="sxs-lookup"><span data-stu-id="e8ad6-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="e8ad6-249">Um roteiro progressivo para seu Aplicativo Web Progressivo</span><span class="sxs-lookup"><span data-stu-id="e8ad6-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="e8ad6-250">POSTs offline com aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="e8ad6-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="e8ad6-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="e8ad6-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="e8ad6-252">Apostando na Web</span><span class="sxs-lookup"><span data-stu-id="e8ad6-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="e8ad6-253">Nomear Aplicativos Web Progressivos</span><span class="sxs-lookup"><span data-stu-id="e8ad6-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="e8ad6-254">Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 1)</span><span class="sxs-lookup"><span data-stu-id="e8ad6-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="e8ad6-255">Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 2)</span><span class="sxs-lookup"><span data-stu-id="e8ad6-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="e8ad6-256">Projetando e criando um aplicativo Web progressivo sem uma estrutura (Parte 3)</span><span class="sxs-lookup"><span data-stu-id="e8ad6-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

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
