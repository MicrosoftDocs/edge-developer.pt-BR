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
# <span data-ttu-id="63b56-104">Introdução aos aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="63b56-104">Get started with Progressive Web Apps</span></span>  

<span data-ttu-id="63b56-105">Aplicativos Web progressivos \ (PWAs \) são simplesmente aplicativos Web que são [aprimorados progressivamente][WikiProgressiveEnhancement] com recursos de semelhantes a aplicativos nativos em plataformas de suporte e mecanismos de navegador, como instalação do lançamento-da-tela inicial, suporte offline e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="63b56-105">Progressive Web Apps \(PWAs\) are simply web apps that are [progressively enhanced][WikiProgressiveEnhancement] with native app-like features on supporting platforms and browser engines, such as launch-from-homescreen installation, offline support, and push notifications.</span></span>  <span data-ttu-id="63b56-106">No Windows 10 com o mecanismo \ (EdgeHTML \) do Microsoft Edge, PWAs Desfrute da vantagem adicional de ser executado independentemente da janela do navegador como aplicativos da [plataforma universal do Windows][WindowsUwpGetStartedWhat] .</span><span class="sxs-lookup"><span data-stu-id="63b56-106">On Windows 10 with the Microsoft Edge \(EdgeHTML\) engine, PWAs enjoy the added advantage of running independently of the browser window as [Universal Windows Platform][WindowsUwpGetStartedWhat] apps.</span></span>  

<span data-ttu-id="63b56-107">Este guia fornece uma visão geral das noções básicas do PWA criando um `localhost` aplicativo Web simples como um PWA usando o Microsoft Visual Studio e alguns utilitários do PWA Builder.</span><span class="sxs-lookup"><span data-stu-id="63b56-107">This guide gives you an overview of PWA basics by building a simple `localhost` web app as a PWA using Microsoft Visual Studio and some PWA Builder utilities.</span></span>  <span data-ttu-id="63b56-108">O produto concluído funciona da mesma forma em qualquer navegador que ofereça suporte a PWAs.</span><span class="sxs-lookup"><span data-stu-id="63b56-108">The finished product works similarly across any browser that supports PWAs.</span></span>  

> [!TIP]
> <span data-ttu-id="63b56-109">Para uma maneira rápida de converter um site existente em um PWA e empacotá-lo para o Windows 10 e outras plataformas de aplicativos, examine o [construtor do PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="63b56-109">For a quick way to convert an existing site to a PWA and package it for Windows 10 and other app platforms, review [PWA Builder][PwaBuilder].</span></span>  

## <span data-ttu-id="63b56-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="63b56-110">Prerequisites</span></span>  

<span data-ttu-id="63b56-111">Você pode criar PWAs com qualquer IDE de desenvolvimento na Web.</span><span class="sxs-lookup"><span data-stu-id="63b56-111">You may build PWAs with any web development IDE.</span></span>  <span data-ttu-id="63b56-112">Os pré-requisitos a seguir são apenas pré-requisitos para este guia, que o orientam pelo suporte de ferramentas do PWA no ecossistema do desenvolvedor do Windows.</span><span class="sxs-lookup"><span data-stu-id="63b56-112">The following are only prerequisites for this guide, which walks you through PWA tooling support in the Windows developer ecosystem.</span></span>  

*   <span data-ttu-id="63b56-113">Baixe o \ (grátis \) [comunidade do Visual Studio 2017][VisualStudioDownloads].</span><span class="sxs-lookup"><span data-stu-id="63b56-113">Download the \(free\) [Visual Studio Community 2017][VisualStudioDownloads].</span></span>  <span data-ttu-id="63b56-114">Você também pode usar as edições Professional, Enterprise ou [Preview][VisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="63b56-114">You may also use the Professional, Enterprise, or [Preview][VisualStudioPreview] editions.</span></span>  <span data-ttu-id="63b56-115">No instalador do Visual Studio, escolha as seguintes cargas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="63b56-115">From the Visual Studio Installer, choose the following Workloads.</span></span>  
    
    *   **<span data-ttu-id="63b56-116">Desenvolvimento da plataforma universal do Windows</span><span class="sxs-lookup"><span data-stu-id="63b56-116">Universal Windows Platform development</span></span>**  
    *   **<span data-ttu-id="63b56-117">Desenvolvimento de Node. js</span><span class="sxs-lookup"><span data-stu-id="63b56-117">Node.js development</span></span>**  

## <span data-ttu-id="63b56-118">Configurar um aplicativo Web básico</span><span class="sxs-lookup"><span data-stu-id="63b56-118">Set up a basic web app</span></span>  

<span data-ttu-id="63b56-119">Para simplificar, use o nó do Visual Studio [. js e][VisualStudioNodeJsTutorial] o modelo de aplicativo expresso para criar `localhost` um aplicativo Web que sirva uma `index.html` página.</span><span class="sxs-lookup"><span data-stu-id="63b56-119">For the sake of simplicity, use the Visual Studio [Node.js and Express app][VisualStudioNodeJsTutorial] template to create `localhost` web app that serves up an `index.html` page.</span></span>  <span data-ttu-id="63b56-120">Imagine isso como um espaço reservado para o aplicativo Web com todos os recursos atraentes que você está desenvolvendo como PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-120">Imagine this as a placeholder for the compelling, full-featured web app that you are developing as a PWA.</span></span>  

1.  <span data-ttu-id="63b56-121">Inicie o Visual Studio e inicie um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="63b56-121">Launch Visual Studio, and start a new project.</span></span>  
    *   <span data-ttu-id="63b56-122">**Arquivo**  >  **Novo**  >  **Projeto...**</span><span class="sxs-lookup"><span data-stu-id="63b56-122">**File** > **New** > **Project...**</span></span>  
    *   `Ctrl`+`Shift`+`N`  
1.  <span data-ttu-id="63b56-123">Em **JavaScript**, selecione **aplicativo Basic node. js Express 4**.</span><span class="sxs-lookup"><span data-stu-id="63b56-123">Under **JavaScript**, select **Basic Node.js Express 4 Application**.</span></span>  <span data-ttu-id="63b56-124">Defina o nome e o local e escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="63b56-124">Set the name and location and choose **OK**.</span></span>  
    
    ![Selecionando o modelo de projeto do node. js Express 4 no Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  <span data-ttu-id="63b56-126">Depois que seu novo projeto for carregado, escolha **Compilar** \ ( `Ctrl` + `Shift` + `B` \) e **Iniciar Depuração** \ ( `F5` \).</span><span class="sxs-lookup"><span data-stu-id="63b56-126">Once your new project loads, choose **Build** \(`Ctrl`+`Shift`+`B`\) and **Start Debugging** \(`F5`\).</span></span>  <span data-ttu-id="63b56-127">Verifique se o `index.html` arquivo é carregado quando você navega `http://localhost:1337` .</span><span class="sxs-lookup"><span data-stu-id="63b56-127">Verify that your `index.html` file loads when you browse to `http://localhost:1337`.</span></span>  
    
    ![Executando seu novo site em localhost][ImageVsNodejsExpressIndex]  

## <span data-ttu-id="63b56-129">Transformar seu aplicativo em um PWA</span><span class="sxs-lookup"><span data-stu-id="63b56-129">Turn your app into a PWA</span></span>  

<span data-ttu-id="63b56-130">Agora, é hora de conectar os [requisitos][PwaEdgehtmlIndexRequirements] básicos do PWA para seu aplicativo Web: um *manifesto do aplicativo Web*, *https* e *serviços de trabalho*.</span><span class="sxs-lookup"><span data-stu-id="63b56-130">Now it is time to wire up the basic [PWA requirements][PwaEdgehtmlIndexRequirements] for your web app: a *Web App Manifest*, *HTTPS* and *Service Workers*.</span></span>  

### <span data-ttu-id="63b56-131">Manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="63b56-131">Web App Manifest</span></span>  

<span data-ttu-id="63b56-132">Um [manifesto do aplicativo Web][MDNWebAppManifest] é um arquivo de metadados JSON que descreve seu aplicativo, incluindo o nome, o autor, a URL da página de entrada e um ou mais ícones.</span><span class="sxs-lookup"><span data-stu-id="63b56-132">A [Web App Manifest][MDNWebAppManifest] is a JSON metadata file describing your app, including the name, author, entry page URL, and one or more icons.</span></span>  <span data-ttu-id="63b56-133">Como ele segue um [esquema baseado em padrões][W3cWebAppManifest], você deve apenas fornecer um único manifesto de aplicativo Web para o PWA que você está instalando em qualquer plataforma, sistema operacional e combinação de dispositivos que suporte PWAs.</span><span class="sxs-lookup"><span data-stu-id="63b56-133">Because it follows a [standards-based schema][W3cWebAppManifest], you must only supply a single web app manifest for the PWA that you are installing on any platform, OS, and device combination that supports PWAs.</span></span>  <span data-ttu-id="63b56-134">No ecossistema do Windows, seu manifesto do aplicativo Web se sinaliza ao indexador da Web do Bing que o PWA é um candidato para a inclusão automática na [Microsoft Store][PwaEdgehtmlMicrosoftStore], onde poderá alcançar cerca de 700 milhões usuários mensais ativos como um aplicativo do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63b56-134">In the Windows ecosystem, your web app manifest signals to the Bing web indexer that your PWA is a candidate for automatic inclusion in the [Microsoft Store][PwaEdgehtmlMicrosoftStore], where it may reach nearly 700 million active monthly users as a Windows 10 app.</span></span>  

<span data-ttu-id="63b56-135">Se esse for um site existente, você poderá gerar um manifesto do aplicativo Web usando o [construtor do PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="63b56-135">If this were an existing live site, you may generate a web app manifest using [PWA Builder][PwaBuilder].</span></span>  <span data-ttu-id="63b56-136">Como ainda é um projeto não publicado, copie um manifesto de exemplo.</span><span class="sxs-lookup"><span data-stu-id="63b56-136">Since it is still an unpublished project, copy a sample manifest.</span></span>  

1.  <span data-ttu-id="63b56-137">No *Gerenciador de soluções*do Visual Studio, clique com o botão direito do mouse na pasta *pública* e selecione **Adicionar**  >  **novo arquivo...** especificando `manifest.json` como o nome do item.</span><span class="sxs-lookup"><span data-stu-id="63b56-137">In the Visual Studio *Solution Explorer*, right-click the *public* folder and select **Add** > **New File...**, specifying `manifest.json` as the item name.</span></span>  
1.  <span data-ttu-id="63b56-138">No `manifest.json` arquivo, copie o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-138">In the `manifest.json` file, copy the following code.</span></span>  

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
    
    <span data-ttu-id="63b56-139">Em um PWA real, a próxima etapa é personalizar o *nome*, *start_url*, *short_name*, *Descrição*e *ícones* \ (os ícones são abordados na próxima etapa \).</span><span class="sxs-lookup"><span data-stu-id="63b56-139">In a real PWA, the next step is to customize *name*, *start_url*, *short_name*, *description*, and *icons* \(icons are covered in the next step\).</span></span>  
    
    <span data-ttu-id="63b56-140">Para saber mais sobre os diferentes valores de membro e objetivos associados, consulte a referência de [manifesto do aplicativo Web][MDNWebAppManifest] .</span><span class="sxs-lookup"><span data-stu-id="63b56-140">To learn more about the different member values and associated purposes, see the [Web App Manifest][MDNWebAppManifest] reference.</span></span>  
    
1.  <span data-ttu-id="63b56-141">Em seguida, preencha a `icons` matriz vazia com caminhos de imagem reais usando o gerador de imagem de aplicativo do PWA Builder.</span><span class="sxs-lookup"><span data-stu-id="63b56-141">Next, fill in the empty `icons` array with actual image paths by using the PWA Builder App Image Generator.</span></span>  
    
    1.  <span data-ttu-id="63b56-142">Usando um navegador da Web, Baixe esta [amostra 512x512 de imagem do PWA][ImagePwa].</span><span class="sxs-lookup"><span data-stu-id="63b56-142">Using a web browser, download this [sample 512x512 PWA image][ImagePwa].</span></span>  
    1.  <span data-ttu-id="63b56-143">Vá para o gerador de [imagem do aplicativo][PwaBuilderAppImageGenerator]do PWA Builder e selecione a `pwa.png` imagem que você acabou de salvar como a **imagem de entrada** e, em seguida, escolha o botão **baixar** .</span><span class="sxs-lookup"><span data-stu-id="63b56-143">Go to the PWA Builder [App Image Generator][PwaBuilderAppImageGenerator], and select the `pwa.png` image you just saved as the **Input Image** and then choose the **Download** button.</span></span>  
    1.  <span data-ttu-id="63b56-144">**Abra** e **Extraia** o arquivo zip.</span><span class="sxs-lookup"><span data-stu-id="63b56-144">**Open** and **Extract** the zip file.</span></span>  
    1.  <span data-ttu-id="63b56-145">No Gerenciador de soluções do Visual Studio, clique com o botão direito do mouse na `public` pasta e **abra pasta no explorador de arquivos**.</span><span class="sxs-lookup"><span data-stu-id="63b56-145">In the Visual Studio Solution Explorer, right-click the `public` folder and **Open Folder in File Explorer**.</span></span>  <span data-ttu-id="63b56-146">Crie uma **nova pasta** chamada `images` .</span><span class="sxs-lookup"><span data-stu-id="63b56-146">Create a **New folder** named `images`.</span></span>  
    1.  <span data-ttu-id="63b56-147">Copie todas as pastas da plataforma \ ( `android` , `chrome` , `windows10` , etc. \) do zip extraído para a `images` pasta e feche a janela do explorador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="63b56-147">Copy all of the platform folders \(`android`, `chrome`, `windows10`, and so on\) from your extracted zip to the `images` folder and close the file explorer window.</span></span>  <span data-ttu-id="63b56-148">Adicione as pastas ao seu projeto do Visual Studio \ (no Gerenciador de soluções, clique com o botão direito do mouse em `images` pasta e selecione **Adicionar**  >  **pasta existente..** . para cada uma das pastas \).</span><span class="sxs-lookup"><span data-stu-id="63b56-148">Add the folders to your Visual Studio project \(in Solution Explorer, right-click `images` folder and select **Add** > **Existing folder...** for each of the folders\).</span></span>  
    1.  <span data-ttu-id="63b56-149">Abra \ (com o Visual Studio ou qualquer editor \) do `icons.json` arquivo zip extraído e copie a `"icons": [...]` matriz para o `manifest.json` arquivo do seu projeto.</span><span class="sxs-lookup"><span data-stu-id="63b56-149">Open \(with Visual Studio or any editor\) the `icons.json` file from the extracted zip and copy the `"icons": [...]` array into the `manifest.json` file of your project.</span></span>  

1.  <span data-ttu-id="63b56-150">Agora você deve associar seu manifesto do aplicativo Web ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63b56-150">Now you must associate your web app manifest with your app.</span></span>  <span data-ttu-id="63b56-151">Abra o `layout.pug` arquivo \ (na `views` pasta \) para edição e adicione essa linha logo após o link de folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="63b56-151">Open the `layout.pug` file \(in `views` folder\) for editing, and add this line right after the stylesheet link.</span></span>  <span data-ttu-id="63b56-152">\ (É simplesmente a abreviação do modelo [Pug][PugAttributes] do nó para `<link rel='manifest' href='/manifest.json'>` \).</span><span class="sxs-lookup"><span data-stu-id="63b56-152">\(It is simply the Node [pug][PugAttributes] template shorthand for `<link rel='manifest' href='/manifest.json'>`\).</span></span>  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
<span data-ttu-id="63b56-153">Com tudo isso em vigor, seu aplicativo Web agora está servindo um manifesto e ícones de aplicativos prontos para tela inicial!</span><span class="sxs-lookup"><span data-stu-id="63b56-153">With all that in place, your web app is now serving up a manifest and homescreen-ready app icons!</span></span>  <span data-ttu-id="63b56-154">Tente executar seu aplicativo \ ( `F5` \) e carregar o manifesto.</span><span class="sxs-lookup"><span data-stu-id="63b56-154">Try running your app \(`F5`\) and loading up the manifest.</span></span>  

![Manifesto do aplicativo Web carregando do localhost][ImageVsNodejsExpressManifest]  

<span data-ttu-id="63b56-156">E um de seus ícones.</span><span class="sxs-lookup"><span data-stu-id="63b56-156">And one of your icons.</span></span>  

![O logotipo do aplicativo Square71x71Logo está sendo carregado do localhost][ImageVsNodejsExpressIcon]  

<span data-ttu-id="63b56-158">Se você publicar o aplicativo em tempo real \ (com um `start_url` \ real \), o mecanismo de pesquisa do Bing agora o identifica como um candidato para [empacotamento e envio automáticos para a Microsoft Store][PwaEdgehtmlMicrosoftStore] como um aplicativo instalável do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63b56-158">If you publish the app live \(with an actual `start_url`\), the Bing search engine now identifies it as a candidate for [automatic packaging and submission to the Microsoft Store][PwaEdgehtmlMicrosoftStore] as an installable Windows 10 app.</span></span>  <span data-ttu-id="63b56-159">Verifique se o arquivo manifest. JSON inclui os [sinais de qualidade para aplicativos Web progressivos][WindowsBlogsPwaEdge] para os quais o Bing verifica incluindo os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-159">Ensure that your manifest.json file includes the [Quality signals for Progressive Web Apps][WindowsBlogsPwaEdge] for which Bing scans including the following items.</span></span>   

*   `name`  
*   `description`  
*   <span data-ttu-id="63b56-160">Pelo menos um ícone 512px quadrado ou maior \ (para garantir uma fonte de resolução suficiente para a geração automática da tela inicial do seu aplicativo, a listagem da loja, a imagem do bloco e assim por diante \).</span><span class="sxs-lookup"><span data-stu-id="63b56-160">At least one icon 512px square or larger \(to ensure an image source of sufficient resolution for auto-generating the splash screen of your app, store listing, tile image, and so on\).</span></span>  

<span data-ttu-id="63b56-161">Além disso, use [https](#https), [trabalhos de serviço](#service-workers)e cumpra [as políticas da Microsoft Store][LegalWindowsAgrementsMicrosoftStorePolicies].</span><span class="sxs-lookup"><span data-stu-id="63b56-161">In addition, use [HTTPS](#https), [service workers](#service-workers), and comply with [Microsoft Store Policies][LegalWindowsAgrementsMicrosoftStorePolicies].</span></span>  

### <span data-ttu-id="63b56-162">HTTPS</span><span class="sxs-lookup"><span data-stu-id="63b56-162">HTTPS</span></span>  

<span data-ttu-id="63b56-163">[Os funcionários do serviço][MDNServiceWorkerApi] e outras tecnologias importantes do PWA que trabalham com trabalhadores de serviço \ (como as APIs de [cache][MDNCache], [Push][MDNPushApi]e [sincronização em segundo plano][MDNSyncManager] ) funcionam apenas em conexões seguras, o que significa [https][WikiHttps] para sites ativos ou `localhost` para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="63b56-163">[Service Workers][MDNServiceWorkerApi] and other key PWA technologies that work with service workers \(such as the [Cache][MDNCache], [Push][MDNPushApi], and [Background Sync][MDNSyncManager] APIs\) only work across secure connections, which means [HTTPS][WikiHttps] for live sites or `localhost` for debugging purposes.</span></span>  

<span data-ttu-id="63b56-164">Se você [publicar este aplicativo Web como um site do Live][VisualStudioNodejsTutorialPublishAzureAppService] \ (por exemplo, configurando uma [conta gratuita do Azure][AzureCreateFreeAccount]\), você deve garantir que seu servidor esteja configurado para https.</span><span class="sxs-lookup"><span data-stu-id="63b56-164">If you [publish this web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="63b56-165">Se você usar o [serviço de aplicativo do Microsoft Azure][AzureWebApps] para hospedar seu site, ele será servido via HTTPS por padrão.</span><span class="sxs-lookup"><span data-stu-id="63b56-165">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="63b56-166">Para este guia, continue `http://localhost` a usar como um espaço reservado para um site ao vivo servido `https://` .</span><span class="sxs-lookup"><span data-stu-id="63b56-166">For this guide, continue using `http://localhost` as a placeholder for a live site served over `https://`.</span></span>  

### <span data-ttu-id="63b56-167">Trabalhadores do serviço</span><span class="sxs-lookup"><span data-stu-id="63b56-167">Service Workers</span></span>  

<span data-ttu-id="63b56-168">Trabalhadores de serviço é a principal tecnologia por trás do PWAs.</span><span class="sxs-lookup"><span data-stu-id="63b56-168">Service Workers is the key technology behind PWAs.</span></span> <span data-ttu-id="63b56-169">Os funcionários de serviço atuam como um proxy entre seu PWA e a rede para permitir que seu site funcione como um aplicativo nativo instalado que atende a cenários offline, responde a notificações por push do servidor e executa tarefas em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="63b56-169">Service Workers act as a proxy between your PWA and the network to enable your website to function as an installed native app that serves up offline scenarios, responds to server push notifications, and runs background tasks.</span></span>  <span data-ttu-id="63b56-170">Os funcionários de serviço também abrem novas estratégias de desempenho.</span><span class="sxs-lookup"><span data-stu-id="63b56-170">Service workers also open up new performance strategies.</span></span>  <span data-ttu-id="63b56-171">Você não precisa implementar um aplicativo Web completo para usar o cache do serviço de trabalho para o desempenho de carregamento de página ajustado para seu site.</span><span class="sxs-lookup"><span data-stu-id="63b56-171">You are not required to implement a full web app to use the service worker cache for fine-tuned page load performance for your website.</span></span>  

<span data-ttu-id="63b56-172">Os funcionários de serviço são threads em segundo plano acionados por eventos que são executados a partir de arquivos JavaScript fornecidos juntamente com os scripts regulares que alimentam o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="63b56-172">Service workers are event-driven background threads that run from JavaScript files served up alongside the regular scripts that power your web app.</span></span>  <span data-ttu-id="63b56-173">Como os funcionários do serviço não são executados no thread da interface do usuário principal, os funcionários do serviço não têm acesso ao DOM, embora o [thread de interface do usuário][MDNWorkerPrototypePostMessage] e um [thread de trabalho][MDNDedicatedWorkerGlobalScopePostMessage] sejam capazes de se comunicar usando `postMessage()` `onmessage` manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="63b56-173">Because Service workers do not run on the main UI thread, service workers do not have DOM access, though the [UI thread][MDNWorkerPrototypePostMessage] and a [worker thread][MDNDedicatedWorkerGlobalScopePostMessage] is able to communicate using `postMessage()` and `onmessage` event handlers.</span></span>  

<span data-ttu-id="63b56-174">Você associa um trabalhador de serviço ao seu aplicativo registrando-o na origem da URL do seu site \ (ou um caminho especificado dentro dele \).</span><span class="sxs-lookup"><span data-stu-id="63b56-174">You associate a service worker with your app by registering it to the URL origin of your site \(or a specified path within it\).</span></span>  <span data-ttu-id="63b56-175">Depois de registrado, o arquivo de trabalho do serviço é baixado, instalado e ativado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="63b56-175">Once registered, the service worker file is then downloaded, installed, and activated on the user machine.</span></span>  <span data-ttu-id="63b56-176">Para saber mais, o MDN Web docs tem um guia abrangente sobre o [uso de trabalhadores de serviço][MDNUsingServiceWorkers] e uma referência de API de trabalho de [serviço][MDNServiceWorkerApi] detalhada.</span><span class="sxs-lookup"><span data-stu-id="63b56-176">For more, MDN web docs has a comprehensive guide on [Using Service Workers][MDNUsingServiceWorkers] and a detailed [Service Worker API][MDNServiceWorkerApi] reference.</span></span>  

<span data-ttu-id="63b56-177">Para este tutorial, use o script de trabalho do serviço de página offline no [criador do PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="63b56-177">For this tutorial, use the Offline page service worker script on [PWA Builder][PwaBuilderServiceWorker].</span></span>  <span data-ttu-id="63b56-178">Comece Personalizando o script com mais funcionalidade de acordo com os requisitos de desempenho, a largura de banda da rede e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="63b56-178">Start by customizing the script with more functionality according to your performance requirements, network bandwidth, and so on.</span></span>  <span data-ttu-id="63b56-179">Examine o [Cookbook do serviço do serviço][ServiceWorkerCookbook] fornecido pelo Mozilla para obter uma série de ideias úteis de armazenamento em cache de trabalho de serviço.</span><span class="sxs-lookup"><span data-stu-id="63b56-179">Review the [Service Worker Cookbook][ServiceWorkerCookbook]  provided by Mozilla for a number of useful service worker caching ideas.</span></span>  

1.  <span data-ttu-id="63b56-180">Abra [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] e selecione o trabalhador do serviço de **página offline** \ (padrão \) e clique no botão **baixar trabalho do serviço** .</span><span class="sxs-lookup"><span data-stu-id="63b56-180">Open [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] and select the \(default\) **Offline page** service worker and click the **Download service worker** button.</span></span>  
1.  <span data-ttu-id="63b56-181">Abrir a pasta baixar e copiar os dois arquivos a seguir</span><span class="sxs-lookup"><span data-stu-id="63b56-181">Open the download folder and copy the following two files</span></span>  

    *   <span data-ttu-id="63b56-182">ServiceWorker1\pwabuilder-sw-register.js</span><span class="sxs-lookup"><span data-stu-id="63b56-182">ServiceWorker1\pwabuilder-sw-register.js</span></span>  
    *   <span data-ttu-id="63b56-183">ServiceWorker1\pwabuilder-sw.js</span><span class="sxs-lookup"><span data-stu-id="63b56-183">ServiceWorker1\pwabuilder-sw.js</span></span>  
    
    <span data-ttu-id="63b56-184">Salve os arquivos na `public` pasta do seu projeto do Visual Studio Web App.</span><span class="sxs-lookup"><span data-stu-id="63b56-184">Save the files to the `public` folder of your Visual Studio web app project.</span></span>  <span data-ttu-id="63b56-185">\ (Do Visual Studio, use `Ctrl` + `O` para abrir o explorador de arquivos para o seu projeto e navegue até a `public` pasta \).</span><span class="sxs-lookup"><span data-stu-id="63b56-185">\(From Visual Studio, use `Ctrl`+`O` to open file explorer to your project and navigate to the `public` folder\).</span></span>  
    
    <span data-ttu-id="63b56-186">Vale a pena rever o código em ambos os arquivos para obter a essência de como registrar um trabalhador de serviço que armazena em cache uma página designada \ ( `offline.html` \) e a atende quando uma busca de rede falha.</span><span class="sxs-lookup"><span data-stu-id="63b56-186">It is worth reviewing the code in both of these files, to get the gist of how to register a service worker that caches a designated page \(`offline.html`\) and serves it when a network fetch fails.</span></span>  <span data-ttu-id="63b56-187">Em seguida, crie uma `offline.html` página simples como um espaço reservado para a funcionalidade offline do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63b56-187">Next, create a simple `offline.html` page as a placeholder for the offline functionality of your app.</span></span>  
    
1.  <span data-ttu-id="63b56-188">No Gerenciador de soluções, abra o `views/layout.pug` arquivo e adicione a seguinte linha abaixo de suas marcas de link.</span><span class="sxs-lookup"><span data-stu-id="63b56-188">In Solution Explorer, open the `views/layout.pug` file, and add the following line below your link tags.</span></span>  
    
    ```html
    script(src='/pwabuilder-sw-register.js')
    ```  
    
    <span data-ttu-id="63b56-189">Seu site carrega e executa o script de registro do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="63b56-189">Your site loads and runs your service worker registration script.</span></span>  
    
1.  <span data-ttu-id="63b56-190">No Gerenciador de soluções, clique com o botão direito do mouse na `public` pasta e selecione **Adicionar**  >  **novo arquivo..**..  Nomeie- `offline.html` o e adicione um `<title>` conteúdo de corpo e, por exemplo, o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-190">In Solution Explorer, right-click on the `public` folder and select **Add** > **New File...**.  Name it `offline.html`, and add a `<title>` and some body content, for example the following code.</span></span>  
    
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
    
    <span data-ttu-id="63b56-191">Nesse ponto, sua `public` pasta deve ter três arquivos novos.</span><span class="sxs-lookup"><span data-stu-id="63b56-191">At this point, your `public` folder should have three new files.</span></span>  
    
    ![Arquivos adicionados à pasta pública da solução][ImageVsNodejsExpressPublic]  
    
1.  <span data-ttu-id="63b56-193">No Gerenciador de soluções, abra o `routes\index.js` arquivo e adicione o seguinte código logo antes do comando final \ ( `module.exports = router;` \).</span><span class="sxs-lookup"><span data-stu-id="63b56-193">In Solution Explorer, open the `routes\index.js` file, and add the following code just before the final command \(`module.exports = router;`\).</span></span>  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    <span data-ttu-id="63b56-194">Isso instrui seu aplicativo a servir o `offline.html` arquivo \ (quando seu operador de serviço o busca no cache offline \).</span><span class="sxs-lookup"><span data-stu-id="63b56-194">This instructs your app to serve the `offline.html` file \(when your service worker fetches it for the offline cache\).</span></span>  
    
1.  <span data-ttu-id="63b56-195">Teste seu PWA!</span><span class="sxs-lookup"><span data-stu-id="63b56-195">Test out your PWA!</span></span>  <span data-ttu-id="63b56-196">Compilar \ ( `Ctrl` + `Shift` + `B` \) e executar \ ( `F5` \) seu aplicativo Web para iniciar o Microsoft Edge e abrir a `localhost` página.</span><span class="sxs-lookup"><span data-stu-id="63b56-196">Build \(`Ctrl`+`Shift`+`B`\) and Run \(`F5`\) your web app to launch Microsoft Edge and open your `localhost` page.</span></span>  <span data-ttu-id="63b56-197">Em seguida, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-197">Then complete the following steps.</span></span>  
    
    1.  <span data-ttu-id="63b56-198">Abra o **console** do Edge devtools \ ( `Ctrl` + `Shift` + `J` \) e verifique se o trabalhador do serviço foi registrado.</span><span class="sxs-lookup"><span data-stu-id="63b56-198">Open the Edge DevTools **Console** \(`Ctrl`+`Shift`+`J`\) and verify the Service worker was registered.</span></span>  
    1.  <span data-ttu-id="63b56-199">No painel **depurador** , expanda o controle **serviços de funcionários** e clique em sua origem.</span><span class="sxs-lookup"><span data-stu-id="63b56-199">In the **Debugger** panel, expand the **Service Workers** control and click on your origin.</span></span>  <span data-ttu-id="63b56-200">Na **visão geral do trabalho do serviço**, verifique se o trabalhador do seu serviço está ativado e em execução.</span><span class="sxs-lookup"><span data-stu-id="63b56-200">In the **Service Worker Overview**, verify your service worker is activated and running.</span></span>  
        
        ![Visão geral do trabalhador do serviço Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  <span data-ttu-id="63b56-202">Expanda o controle de **cache** e verifique se a `offline.html` página está armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="63b56-202">Expand the **Cache** control and verify that the `offline.html` page is cached.</span></span>  
        
        ![Cache de trabalho do serviço Edge DevTools][ImageDevtoolsSwCache]  
        
1.  <span data-ttu-id="63b56-204">Tempo para experimentar o PWA como um aplicativo offline!</span><span class="sxs-lookup"><span data-stu-id="63b56-204">Time to try your PWA as an offline app!</span></span>  <span data-ttu-id="63b56-205">No Visual Studio, **pare a depuração** \ ( `Shift` + `F5` \) em seu aplicativo Web, abra o Microsoft Edge \ (ou atualize \) no endereço localhost do seu website.</span><span class="sxs-lookup"><span data-stu-id="63b56-205">In Visual Studio, **Stop Debugging** \(`Shift`+`F5`\) your web app, then open Microsoft Edge \(or refresh\) to the localhost address of your website.</span></span>  <span data-ttu-id="63b56-206">Ele agora deve carregar a `offline.html` página \ (Obrigado ao seu trabalhador de serviço e cache offline \)!</span><span class="sxs-lookup"><span data-stu-id="63b56-206">It should now load the `offline.html` page \(thanks to your service worker and offline cache\)!</span></span>  
    
    ![offline. html de http://localhost:1337 carregado no Microsoft Edge][ImageOfflineHtml]  

## <span data-ttu-id="63b56-208">Adicionar notificações por push</span><span class="sxs-lookup"><span data-stu-id="63b56-208">Add push notifications</span></span>  

<span data-ttu-id="63b56-209">Torne seu PWA mais parecido com o aplicativo adicionando suporte do lado do cliente para notificações por push usando a [API de envio][MDNPushApi] para assinar um serviço de mensagens e a [API de notificações][MDNNotificationsApi] para exibir uma mensagem em notificação do sistema ao receber uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b56-209">Make your PWA more app-like by adding client-side support for push notifications using the [Push API][MDNPushApi] to subscribe to a messaging service and the [Notifications API][MDNNotificationsApi] to display a toast message upon receiving a message.</span></span>  <span data-ttu-id="63b56-210">Da mesma forma que com os profissionais do serviço, são APIs baseadas em padrões que funcionam entre navegadores, portanto, você só precisa escrever o código uma vez para que ele funcione em qualquer lugar PWAs tem suporte.</span><span class="sxs-lookup"><span data-stu-id="63b56-210">As with Service Workers, these are standards-based APIs that work cross-browser, so you only have to write the code once for it to work everywhere PWAs are supported.</span></span>  <span data-ttu-id="63b56-211">No lado do servidor, use a biblioteca de código-fonte aberto [por push da Web][NPMWebPush] para manipular as diferenças envolvidas no envio de mensagens de push para vários navegadores.</span><span class="sxs-lookup"><span data-stu-id="63b56-211">On the server side, use the [Web-Push][NPMWebPush] open-source library to handle the differences involved in delivering push messages to various browsers.</span></span>  

<span data-ttu-id="63b56-212">O procedimento a seguir é adaptado da demonstração avançada push no [manual do serviço de trabalho][ServiceWorkerCookbookPushRichDemo] que é fornecida pelo Mozilla, o que vale a pena fazer uma série de outras receitas de trabalho por push e serviço da Web úteis.</span><span class="sxs-lookup"><span data-stu-id="63b56-212">The following is adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which is worth checking out for a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="63b56-213">Etapa 1-instalar a NPM Web-Push library</span><span class="sxs-lookup"><span data-stu-id="63b56-213">Step 1 - Install the NPM web-push library</span></span>  

<span data-ttu-id="63b56-214">No Gerenciador de soluções do Visual Studio, clique com o botão direito do mouse em seu projeto e **abra janela interativa do node. js..**..  Digite o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-214">In Visual Studio Solution Explorer, right-click your project and **Open Node.js Interactive Window...**.  In it, type the following code.</span></span>  

```javascript
.npm install web-push
```  

<span data-ttu-id="63b56-215">Isso faz com que a biblioteca de [envio por push da Web][NPMWebPush] seja instalada.</span><span class="sxs-lookup"><span data-stu-id="63b56-215">This installs the [Web-Push][NPMWebPush] library.</span></span>  <span data-ttu-id="63b56-216">Em seguida, abra o `index.js` arquivo e adicione a seguinte linha à parte superior do seu arquivo após as outras instruções de requisito.</span><span class="sxs-lookup"><span data-stu-id="63b56-216">Then, open up your `index.js` file, and add the following line to the top of your file after the other requirement statements.</span></span>  

```javascript
var webpush = require('web-push');
```  

### <span data-ttu-id="63b56-217">Etapa 2-gerar chaves VAPID para o seu servidor</span><span class="sxs-lookup"><span data-stu-id="63b56-217">Step 2 - Generate VAPID keys for your server</span></span>  

<span data-ttu-id="63b56-218">Em seguida, você deve gerar as chaves VAPID \ (identificação do servidor de aplicativos voluntária \) para que seu servidor envie mensagens de envio para o cliente PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-218">Next you must generate VAPID \(Voluntary Application Server Identification\) keys for your server to send push messages to the PWA client.</span></span>  <span data-ttu-id="63b56-219">Você só precisa fazer isso uma vez \ (ou seja, seu servidor requer apenas um único par de teclas VAPID \).</span><span class="sxs-lookup"><span data-stu-id="63b56-219">You only have to do this once \(that is, your server only requires a single pair of VAPID keys\).</span></span>  <span data-ttu-id="63b56-220">Na janela interativa node. js, digite o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-220">In the Node.js Interactive Window, type the following code.</span></span>  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

<span data-ttu-id="63b56-221">A saída deve resultar em um objeto JSON que contém uma chave pública e privada, que você copia para a lógica do servidor.</span><span class="sxs-lookup"><span data-stu-id="63b56-221">The output should result in a JSON object containing a public and private key, which you copy into your server logic.</span></span>  

<span data-ttu-id="63b56-222">No seu `index.js` arquivo, logo antes da linha final \ ( `module.exports = router` \), adicione o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-222">In your `index.js` file, just before the final  \(`module.exports = router`\) line, add the following code.</span></span>  

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

<span data-ttu-id="63b56-223">Copie os `publicKey` `privateKey` valores e que você acabou de gerar.</span><span class="sxs-lookup"><span data-stu-id="63b56-223">Copy the `publicKey` and `privateKey` values that you just generated.</span></span>  <span data-ttu-id="63b56-224">Sinta-se à vontade para personalizar o `mailto` endereço também \ (ainda não é necessário para executar este exemplo \).</span><span class="sxs-lookup"><span data-stu-id="63b56-224">Feel free to customize the `mailto` address as well \(though it is not required in order to run this sample\).</span></span>  

<span data-ttu-id="63b56-225">O [blog de engenharia de serviços do Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] tem um ótimo explicador em VAPID e webpush se você estiver interessado nos detalhes de como ele funciona nos bastidores.</span><span class="sxs-lookup"><span data-stu-id="63b56-225">The [Mozilla Services engineering blog][MozillaServicesSendingVapidWebPushNotificationsPush] has a nice explainer on VAPID and WebPush if you are interested in the details of how it works behind the scenes.</span></span>  

### <span data-ttu-id="63b56-226">Etapa 3-manipular solicitações do servidor relacionados a Push</span><span class="sxs-lookup"><span data-stu-id="63b56-226">Step 3 - Handle push-related server requests</span></span>  

<span data-ttu-id="63b56-227">Agora, configure rotas para manipular solicitações relacionadas a Push do cliente PWA, incluindo a veiculação da chave pública VAPID e o registro do cliente para receber envios.</span><span class="sxs-lookup"><span data-stu-id="63b56-227">Now set up routes for handling push-related requests from the PWA client, including serving up the VAPID public key and registering the client to receive pushes.</span></span>  

<span data-ttu-id="63b56-228">Em um cenário real, uma notificação por Push provavelmente provém de um evento na lógica do servidor.</span><span class="sxs-lookup"><span data-stu-id="63b56-228">In a real scenario, a push notification likely originates from an event in your server logic.</span></span>  <span data-ttu-id="63b56-229">Para simplificar as coisas aqui, você deve adicionar um botão de **notificação por push** à nossa página inicial do PWA para gerar envios do nosso servidor e um `/sendNotification` ponto de extremidade \ (rota do servidor \) para lidar com essas solicitações.</span><span class="sxs-lookup"><span data-stu-id="63b56-229">To simplify things here, you must add a **Push Notification** button to our PWA homepage for generating pushes from our server, and a `/sendNotification` endpoint \(server route\)for handling those requests.</span></span>  

<span data-ttu-id="63b56-230">Em seu `index.js` arquivo, acrescente as seguintes rotas logo após o código de inicialização do VAPID que você adicionou na [etapa 2] [#step-2---gerar-VAPID-Keys-para-seu-servidor].</span><span class="sxs-lookup"><span data-stu-id="63b56-230">In your `index.js` file, append the following routes just after the VAPID initialization code you added in [Step 2][#step-2---generate-vapid-keys-for-your-server].</span></span>  

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

<span data-ttu-id="63b56-231">Com o código do lado do servidor estabelecido, coloque as notificações por push no cliente do PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-231">With the server-side code in place, plumb in push notifications on the PWA client.</span></span>  

### <span data-ttu-id="63b56-232">Etapa 4-assinar notificações por push</span><span class="sxs-lookup"><span data-stu-id="63b56-232">Step 4 - Subscribe to push notifications</span></span>  

<span data-ttu-id="63b56-233">Como parte da função dos proxies de rede do PWA, os funcionários de serviço lidam com eventos de push e interações de notificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="63b56-233">As part of their role as PWA network proxies, service workers handle push events and toast notification interactions.</span></span>  <span data-ttu-id="63b56-234">No entanto, como se trata de primeiro configurar \ (ou registrar \) um trabalhador de serviço, a assinatura do PWA para notificações por push de servidor acontece no thread da interface do usuário principal do PWA e requer conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="63b56-234">However, as it is with first setting up \(or registering\) a service worker, subscribing the PWA to server push notifications happens on the main UI thread of the PWA and requires network connectivity.</span></span>  <span data-ttu-id="63b56-235">Assinar as notificações por push requer um registro de trabalho do serviço ativo, portanto, você deve primeiro verificar se o trabalhador do serviço está instalado e ativo antes de tentar assiná-lo para notificações por push.</span><span class="sxs-lookup"><span data-stu-id="63b56-235">Subscribing to push notifications requires an active service worker registration, so you must first verify that your service worker is installed and active before trying to subscribe it to push notifications.</span></span>  

<span data-ttu-id="63b56-236">Antes de criar uma nova assinatura push, o Microsoft Edge verifica se o usuário concedeu permissão ao PWA para receber notificações.</span><span class="sxs-lookup"><span data-stu-id="63b56-236">Before a new push subscription is created, Microsoft Edge check if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="63b56-237">Caso contrário, o usuário será solicitado a confirmar a permissão do navegador.</span><span class="sxs-lookup"><span data-stu-id="63b56-237">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="63b56-238">Se a permissão for negada, a solicitação para `registration.pushManager.subscribe` lançar a `DOMException` ; portanto, você deverá tratá-la.</span><span class="sxs-lookup"><span data-stu-id="63b56-238">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, so you must handle it.</span></span>  <span data-ttu-id="63b56-239">Para saber mais sobre o gerenciamento de permissões, consulte [notificações por push no Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="63b56-239">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="63b56-240">Em seu `pwabuilder-sw-register.js` arquivo, acrescente o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-240">In your `pwabuilder-sw-register.js` file, append the following code.</span></span>  

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

<span data-ttu-id="63b56-241">Examine a documentação do MDN na interface do [pushmanager][MDNPushManager] e documentos do NPM na biblioteca de [envio pela Web][NPMWebPushUsage] para obter mais detalhes sobre como as APIs funcionam e várias opções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="63b56-241">Review the MDN documentation on the [PushManager][MDNPushManager] interface and NPM docs on the [Web-Push][NPMWebPushUsage] library for more details on how the APIs work and various related options.</span></span>  

### <span data-ttu-id="63b56-242">Etapa 5-configurar manipuladores de eventos push e notificationclick</span><span class="sxs-lookup"><span data-stu-id="63b56-242">Step 5 - Set up push and notificationclick event handlers</span></span>  

<span data-ttu-id="63b56-243">Com a configuração da assinatura push, o restante do trabalho acontece no trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="63b56-243">With our push subscription set up, the remainder of the work happens in the service worker.</span></span>  <span data-ttu-id="63b56-244">Primeiro, você deve configurar um manipulador para eventos Push enviados pelo servidor e responder com uma notificação do sistema \ (se a permissão foi concedida \) exibindo a carga de dados de envio.</span><span class="sxs-lookup"><span data-stu-id="63b56-244">First you must set up a handler for server-sent push events, and respond with a toast notification \(if permission was granted\) displaying the push data payload.</span></span>  <span data-ttu-id="63b56-245">Em seguida, adicione um manipulador de clique para o sistema de notificação para ignorar a notificação e classificar por uma lista de janelas abertas no momento para abrir, enfocar ou abrir e focalizar a página do cliente PWA pretendida.</span><span class="sxs-lookup"><span data-stu-id="63b56-245">Next you add a click handler for the toast to dismiss the notification and sort through a list of currently open windows to open, focus, or open and focus the intended PWA client page.</span></span>  

<span data-ttu-id="63b56-246">Em seu `pwabuilder-sw.js` arquivo, acrescente os manipuladores a seguir.</span><span class="sxs-lookup"><span data-stu-id="63b56-246">In your `pwabuilder-sw.js` file, append the following handlers.</span></span>  

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

### <span data-ttu-id="63b56-247">Etapa 6-Experimente</span><span class="sxs-lookup"><span data-stu-id="63b56-247">Step 6 - Try it out</span></span>  

<span data-ttu-id="63b56-248">Tempo para testar as notificações por push no seu PWA!</span><span class="sxs-lookup"><span data-stu-id="63b56-248">Time to test push notifications in your PWA!</span></span>  

1.  <span data-ttu-id="63b56-249">Execute \ ( `F5` \) o PWA no navegador.</span><span class="sxs-lookup"><span data-stu-id="63b56-249">Run \(`F5`\) your PWA in the browser.</span></span>  <span data-ttu-id="63b56-250">Como você modificou o código de trabalho do serviço \ ( `pwabuilder-sw.js` \), deve abrir o depurador devtools \ ( `F12` \) para o painel de **visão geral do trabalhador do serviço** e **cancelar o registro** do trabalhador do serviço e recarregar \ ( `F5` \) a página para registrá-la novamente \ (ou clicar em **Atualizar**\).</span><span class="sxs-lookup"><span data-stu-id="63b56-250">Because you modified the service worker code \(`pwabuilder-sw.js`\), you must open the DevTools Debugger \(`F12`\) to the **Service Worker Overview** panel and **Unregister** the service worker and reload \(`F5`\) the page to re-register it \(or you click **Update**\).</span></span>  <span data-ttu-id="63b56-251">Em um cenário de produção, o navegador verifica regularmente se há atualizações do trabalho do serviço e instala as atualizações em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="63b56-251">In a production scenario, the browser checks regularly check for service worker updates and install the updates in the background.</span></span>  <span data-ttu-id="63b56-252">Você deve forçá-lo aqui para obter resultados imediatos.</span><span class="sxs-lookup"><span data-stu-id="63b56-252">You should force it here for immediate results.</span></span>  
    
    <span data-ttu-id="63b56-253">À medida que o trabalhador do serviço é ativado e tenta assinar as notificações por push do PWA, você deve ver uma caixa de diálogo de permissão na parte inferior da página.</span><span class="sxs-lookup"><span data-stu-id="63b56-253">As your service worker activates and attempts to subscribe your PWA to push notifications, you should see a permission dialog at the bottom of the page.</span></span>  
    
    ![Caixa de diálogo de permissão para habilitar notificações][ImageNotificationPermission]  
    
    <span data-ttu-id="63b56-255">Escolha **Sim** para habilitar as notificações do sistema para o seu PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-255">Choose **Yes** to enable toast notifications for your PWA.</span></span>  
    
1.  <span data-ttu-id="63b56-256">No painel Visão geral do trabalhador do serviço, tente escolher o botão de **ação** .</span><span class="sxs-lookup"><span data-stu-id="63b56-256">From the Service Worker Overview pane, try choosing the  **Push** button.</span></span>  <span data-ttu-id="63b56-257">Será exibida uma notificação do sistema com a carga \ (codificada "\ (embutida" Test Push Message of DevTools "\).</span><span class="sxs-lookup"><span data-stu-id="63b56-257">A toast notification with the \(hard-coded "Test push message from DevTools"\) payload should appear.</span></span>  
    
    ![Enviar uma notificação por push de DevTools][ImageDevtoolsPush]  
    
1.  <span data-ttu-id="63b56-259">Em seguida, tente escolher o botão **enviar notificação** na home page do seu PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-259">Next try choosing the **Send Notification** button on the homepage of your PWA.</span></span>  <span data-ttu-id="63b56-260">Desta vez, um sistema de notificação com a carga do seu servidor será exibido.</span><span class="sxs-lookup"><span data-stu-id="63b56-260">This time a toast with the payload from your server appears.</span></span>  
    
    ![Enviar uma notificação por push do servidor PWA][ImagePwaPush]  
    
    <span data-ttu-id="63b56-262">Se você não clicar em \ (ou ativar \) uma notificação do sistema, ela será ignorada após vários segundos e será colocada na fila na central de ações do Windows.</span><span class="sxs-lookup"><span data-stu-id="63b56-262">If you do not click \(or activate\) a toast notification, it is dismissed after several seconds and queue up in your Windows Action Center.</span></span>  
    
    ![Notificações na central de ações do Windows][ImageWindowsActionCenter]  
    
    <span data-ttu-id="63b56-264">Você tem noções básicas das notificações por push do PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-264">You have the basics of PWA push notifications.</span></span>  <span data-ttu-id="63b56-265">Em um aplicativo real, as próximas etapas são implementadas de forma a gerenciar e armazenar assinaturas push e de [criptografar][NPMWebPushEncrypt] corretamente os dados de carga enviados pela conexão.</span><span class="sxs-lookup"><span data-stu-id="63b56-265">In a real app, the next steps are implemented in a way to manage and store push subscriptions and to properly [encrypt][NPMWebPushEncrypt] payload data being sent across the wire.</span></span>  
    
## <span data-ttu-id="63b56-266">Aprofundamento</span><span class="sxs-lookup"><span data-stu-id="63b56-266">Going further</span></span>  

<span data-ttu-id="63b56-267">Este guia demonstrou a Anatomia básica de um aplicativo Web progressivo e das ferramentas de desenvolvimento do Microsoft PWA, incluindo o Visual Studio, o construtor do PWA e o Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="63b56-267">This guide demonstrated the basic anatomy of a Progressive Web App and Microsoft PWA development tools including Visual Studio, PWA Builder, and Edge DevTools.</span></span>  

<span data-ttu-id="63b56-268">É claro que há muito mais que vai para [fazer um grande PWA][PwaEdgehtmlIndexRequirements] além do que você lê aqui, incluindo design responsivo, vinculação profunda, [teste entre navegadores][BrowserStackTestEdgeBrowser] e outras [práticas recomendadas][Webhint] \ (não para mencionar a funcionalidade do seu aplicativo! \), mas espero que este guia tenha uma introdução sólida de noções básicas do PWA e algumas ideias sobre como começar.</span><span class="sxs-lookup"><span data-stu-id="63b56-268">Of course, there is a lot more that goes into [making a great PWA][PwaEdgehtmlIndexRequirements] beyond what you read here, including responsive design, deep-linking, [cross-browser testing][BrowserStackTestEdgeBrowser] and other [best practices][Webhint] \(not to mention your app functionality!\), but hopefully this guide gave you a solid introduction of PWA basics and some ideas on getting started.</span></span>  <span data-ttu-id="63b56-269">Se você tiver outras dúvidas sobre o desenvolvimento do PWA com o Windows ou com o Visual Studio, deixe um comentário!</span><span class="sxs-lookup"><span data-stu-id="63b56-269">If you have further questions on PWA development with Windows or with Visual Studio, please leave a comment!</span></span>  

<span data-ttu-id="63b56-270">Revise os outros guias do PWA para aprender a aumentar o envolvimento do cliente e oferecer uma experiência de aplicativo integrada mais uniforme e integrada ao sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="63b56-270">Review the other PWA guides to learn how to increase customer engagement and provide a more seamless, OS-integrated app experience.</span></span>  

*   <span data-ttu-id="63b56-271">[Ajuste do Windows][PwaEdgehtmlWindowsFeatures].</span><span class="sxs-lookup"><span data-stu-id="63b56-271">[Windows tailoring][PwaEdgehtmlWindowsFeatures].</span></span> <span data-ttu-id="63b56-272">Usando a detecção simples de recursos, você pode aprimorar progressivamente seus clientes do PWA para Windows 10 por meio de APIs do Windows Runtime (WinRT \) nativas, como aquelas para personalizar as notificações do bloco do menu **Iniciar** do Windows e a barra de tarefas, e \ (mediante permissão \) trabalhando com recursos do usuário, como fotos, música e calendário.</span><span class="sxs-lookup"><span data-stu-id="63b56-272">Using simple feature detection, you may progressively enhance your PWA for Windows 10 customers through native Windows Runtime \(WinRT\) APIs, such as those for customizing Windows **Start** menu tile notifications and taskbar jumplists, and \(upon permission\) working with user resources, such as photos, music, and calendar.</span></span>  
*   <span data-ttu-id="63b56-273">[PWAs na Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="63b56-273">[PWAs in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  <span data-ttu-id="63b56-274">Saiba mais sobre as vantagens da distribuição da App Store e como enviar seu PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-274">Learn more about the benefits of app store distribution and how to submit your PWA.</span></span>  

## <span data-ttu-id="63b56-275">Consulte também</span><span class="sxs-lookup"><span data-stu-id="63b56-275">See also</span></span>  

*   <span data-ttu-id="63b56-276">[Aplicativos Web progressivos em MDN Web docs][MDNProgressiveWebApps] – excelente guia sobre aplicativos Web progressivos.</span><span class="sxs-lookup"><span data-stu-id="63b56-276">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="63b56-277">[Aplicativos Web progressivos no Web. dev][WebDevProgressiveWebApps] – excelente guia sobre aplicativos Web progressivos.</span><span class="sxs-lookup"><span data-stu-id="63b56-277">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="63b56-278">[Aplicativos Web progressivos tem][ProgressiveWebApps] -tem exemplos reais de PWAs.</span><span class="sxs-lookup"><span data-stu-id="63b56-278">[Progressive Web Apps rocks][ProgressiveWebApps] - Showcases real-world examples of PWAs.</span></span>  
*   <span data-ttu-id="63b56-279">[Leitores de notícias de hackers como Web Apps progressivos][HackerNewsProgressiveWebApps] – compara estruturas e padrões de desempenho diferentes para implementar uma amostra \ (leitor de notícias de hackers \) PWA.</span><span class="sxs-lookup"><span data-stu-id="63b56-279">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

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
