---
description: Aprimore progressivamente seu PWA para Windows com recursos nativos do aplicativo
title: Personalizar o PWA para Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicativos Web progressivos, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 5bad708db5b13517fd1887214a5e1d5457796ee2
ms.sourcegitcommit: e07de36ee9fbe20422ffc2c62b98839851e1b02b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2020
ms.locfileid: "10604008"
---
# <span data-ttu-id="78208-104">Personalizar o PWA (EdgeHTML) para Windows</span><span class="sxs-lookup"><span data-stu-id="78208-104">Tailor your PWA (EdgeHTML) for Windows</span></span>  

<span data-ttu-id="78208-105">O PWAs instalado no Windows 10 aproveita [todas as vantagens][PwaIndexWindows10] de executar como aplicativos da [plataforma universal do Windows \ (UWP \)][WindowsUWPGetStartedGuide] , incluindo a proteção por meio da proteção de segurança do aplicativo Windows e acesso total a APIs do [Windows Runtime \ (WinRT \))][UwpApiIndex] , incluindo as para:</span><span class="sxs-lookup"><span data-stu-id="78208-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span></span>  

*   <span data-ttu-id="78208-106">Controlando recursos de dispositivo \ (como câmera, microfone, GPS \)</span><span class="sxs-lookup"><span data-stu-id="78208-106">Controlling device features \(such as camera, microphone, GPS\)</span></span>  
*   <span data-ttu-id="78208-107">Acessando recursos do usuário \ (como calendário, contatos, documentos, música \)</span><span class="sxs-lookup"><span data-stu-id="78208-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span></span>  
*   <span data-ttu-id="78208-108">Iniciar/navegar pelo aplicativo por meio de comandos de voz da Cortana</span><span class="sxs-lookup"><span data-stu-id="78208-108">Launching / navigating your app through Cortana voice commands</span></span>  
*   <span data-ttu-id="78208-109">Integração com o sistema operacional Windows \ (por meio da central de ações do Windows, da barra de tarefas da área de trabalho e dos menus de contexto \)</span><span class="sxs-lookup"><span data-stu-id="78208-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span></span>  

<span data-ttu-id="78208-110">... e essas são apenas algumas das possibilidades adicionadas ao seu PWA \ (EdgeHTML \) no Windows!</span><span class="sxs-lookup"><span data-stu-id="78208-110">... and these are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows!</span></span>  

<span data-ttu-id="78208-111">Este guia mostra como instalar, executar e aprimorar o seu PWA \ (EdgeHTML \) como um aplicativo do Windows 10 e ainda garantir a compatibilidade entre navegadores e várias plataformas.</span><span class="sxs-lookup"><span data-stu-id="78208-111">This guide shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span></span>  

## <span data-ttu-id="78208-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="78208-112">Prerequisites</span></span>  

*   <span data-ttu-id="78208-113">Um PWA existente \ (ou aplicativo Web hospedado \), um site dinâmico ou localhost.</span><span class="sxs-lookup"><span data-stu-id="78208-113">An existing PWA \(or hosted web app\), either a live or localhost site.</span></span>  <span data-ttu-id="78208-114">Este guia usa o PWA de exemplo de [introdução a Web Apps progressivos][PwaGetStarted].</span><span class="sxs-lookup"><span data-stu-id="78208-114">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span></span>  
*   <span data-ttu-id="78208-115">Baixe o \ (grátis \) [comunidade do Visual Studio 2017][MicrosoftVisualStudio|::ref1::|].</span><span class="sxs-lookup"><span data-stu-id="78208-115">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span></span>  <span data-ttu-id="78208-116">Você também pode usar as edições Professional, Enterprise ou [Preview][MicrosoftVisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="78208-116">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span></span>  <span data-ttu-id="78208-117">No instalador do Visual Studio, escolha as seguintes cargas de trabalho:</span><span class="sxs-lookup"><span data-stu-id="78208-117">From the Visual Studio Installer, choose the following Workloads:</span></span>  
    *   **<span data-ttu-id="78208-118">Desenvolvimento da plataforma universal do Windows</span><span class="sxs-lookup"><span data-stu-id="78208-118">Universal Windows Platform development</span></span>**  

## <span data-ttu-id="78208-119">Configurar e executar seu aplicativo universal do Windows</span><span class="sxs-lookup"><span data-stu-id="78208-119">Set up and run your Universal Windows app</span></span>  

<span data-ttu-id="78208-120">Um PWA \ (EdgeHTML \) instalado como um aplicativo do Windows 10 é executado independentemente do navegador, em uma janela autônoma \ ( `WWAHost.exe` process \).</span><span class="sxs-lookup"><span data-stu-id="78208-120">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span></span>  <span data-ttu-id="78208-121">Habilitar isso simplesmente requer um wrapper de aplicativo leve que contém seu aplicativo Web hospedado, que você pode configurar rapidamente usando o modelo de projeto do Visual Studio `Progressive Web App (Universal Windows)` .</span><span class="sxs-lookup"><span data-stu-id="78208-121">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span></span>  <span data-ttu-id="78208-122">\ (Toda a lógica do aplicativo, incluindo o envio de solicitações nativas da API do Windows Runtime, ainda acontece no código do seu aplicativo Web original. \)</span><span class="sxs-lookup"><span data-stu-id="78208-122">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span></span>  

<span data-ttu-id="78208-123">Configurar seu ambiente de desenvolvimento de aplicativos do Windows no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="78208-123">Set up your Windows app development environment in Visual Studio.</span></span>  

1.  <span data-ttu-id="78208-124">Em suas configurações do Windows, ative o [modo de desenvolvedor][WindowsUWPGetStartedEnable].</span><span class="sxs-lookup"><span data-stu-id="78208-124">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span></span>  <span data-ttu-id="78208-125">\ (Digite `developer mode` o Searchbar do Windows para localizá-lo. \)</span><span class="sxs-lookup"><span data-stu-id="78208-125">\(Type `developer mode` in the Windows searchbar to find it.\)</span></span>  
1.  <span data-ttu-id="78208-126">Inicie o Visual Studio e **crie um novo projeto...**</span><span class="sxs-lookup"><span data-stu-id="78208-126">Launch Visual Studio and **Create a new project...**</span></span>  
1.  <span data-ttu-id="78208-127">Selecione o modelo de **projeto de pacotes de aplicativos do Windows** em C#.</span><span class="sxs-lookup"><span data-stu-id="78208-127">Select the C# **Windows Application Packaging Project** template.</span></span>  <span data-ttu-id="78208-128">Se você estiver usando uma versão anterior do Visual Studio, localize o modelo equivalente em **aplicativo Web hospedado (Universal Windows)** ou em **aplicativo Web progressivo (universal do Windows)**.</span><span class="sxs-lookup"><span data-stu-id="78208-128">If you are using a previous version of Visual Studio, find the equivalent template under **Hosted Web App (Universal Windows)** or **Progressive Web App (Universal Windows)**.</span></span>  
1.  <span data-ttu-id="78208-129">Selecione o Windows 10 `Target version` \ (versão mais recente \) e `Minimum version` \ (Build 10586 ou superior) padrão e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="78208-129">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and click **OK**.</span></span>  

    ![Caixa de diálogo de seleção do Visual Studio para compilações de destino do projeto UWP](media/vs-target-min-version.png)  

    <span data-ttu-id="78208-131">Seu novo projeto é carregado com o Package. appxmanifest designer aberto.</span><span class="sxs-lookup"><span data-stu-id="78208-131">Your new project loads with the package.appxmanifest designer open.</span></span>  <span data-ttu-id="78208-132">Isso é onde você configura os detalhes do seu aplicativo, incluindo identidade do pacote, dependências do pacote, recursos necessários, elementos visuais e pontos de extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="78208-132">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span></span>  <span data-ttu-id="78208-133">Esta é uma versão do manifesto do pacote do aplicativo, que é facilmente configurável, usada durante o desenvolvimento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-133">This is an easily configurable, temporary version of the app package manifest used during app development.</span></span>  
    <span data-ttu-id="78208-134">Quando você cria seu projeto de aplicativo, o [Visual Studio gera um arquivo AppxManifest. xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] a partir desses metadados, que é usado para instalar e executar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-134">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span></span>  <span data-ttu-id="78208-135">Sempre que atualizar o `package.appxmanifest` arquivo, certifique-se de recriar o projeto para que ambos sejam refletidos em seu `AppxManifest.xml` tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="78208-135">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span></span>  

1.  <span data-ttu-id="78208-136">No painel de **aplicativos** do designer de manifesto, insira a URL do seu PWA como o `Start page` .</span><span class="sxs-lookup"><span data-stu-id="78208-136">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="78208-137">Os funcionários de serviço têm suporte para todas as URLs HTTPS \ (Secure, Remote \) especificadas como a `StartPage` .</span><span class="sxs-lookup"><span data-stu-id="78208-137">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span></span>  <span data-ttu-id="78208-138">Os funcionários de serviço não são suportados por padrão para aplicativos Web que especificam uma página inicial local.</span><span class="sxs-lookup"><span data-stu-id="78208-138">Service workers are not supported by default for web apps that specify a local start page.</span></span>  <span data-ttu-id="78208-139">Para habilitar o suporte do trabalho do serviço para estes casos, adicione uma entrada [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) explícita ao manifesto, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="78208-139">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span></span> `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Painel de aplicativos do Package. appxmanifest designer](media/vs-manifest-application.png)  
    
    <span data-ttu-id="78208-141">Você também pode modificar a `Display name` e como quiser `Description` .</span><span class="sxs-lookup"><span data-stu-id="78208-141">You are able to also modify the `Display name` and `Description` as you like.</span></span>  
1.  <span data-ttu-id="78208-142">Salve este arquivo \ (ou outra imagem 512x512 da sua escolha \) na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="78208-142">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span></span>  
    <span data-ttu-id="78208-143">Em seguida, no painel **recursos visuais** do designer de manifesto, clique no `Source` botão campo **..** ., selecione-o como seu arquivo de origem e clique em **gerar**.</span><span class="sxs-lookup"><span data-stu-id="78208-143">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span></span>  <span data-ttu-id="78208-144">\ (Em seguida, clique em **OK** para substituir as imagens de espaço reservado padrão \).</span><span class="sxs-lookup"><span data-stu-id="78208-144">\(Then click **OK** to overwrite the default placeholder images\).</span></span>  
    
    ![Painel ativos visuais do designer do pacote. appxmanifest](media/vs-manifest-visual-assets.png)  
    
    <span data-ttu-id="78208-146">Isso gera os ativos visuais básicos para instalar, executar, iniciar e distribuir seu aplicativo na loja.</span><span class="sxs-lookup"><span data-stu-id="78208-146">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span></span>  
    <span data-ttu-id="78208-147">Se você vir algum erro vermelho \ ( `X` \) indicando imagens ausentes, é possível clicar nos botões **...** para selecionar manualmente um arquivo das imagens geradas.</span><span class="sxs-lookup"><span data-stu-id="78208-147">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span></span>  
1.  <span data-ttu-id="78208-148">No painel URIs de **conteúdo** do designer de manifesto, substitua `http://example.com` o local do seu PWA \ (de exemplo `Rule`  =  `include` `WinRT Access`  =  `All` ).</span><span class="sxs-lookup"><span data-stu-id="78208-148">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span></span>  
    <span data-ttu-id="78208-149">Isso concede à sua permissão do PWA para enviar solicitações de API nativas do tempo de execução do Windows \ (WinRT \) durante a execução como um aplicativo do Windows 10, que é abordado um pouco mais tarde.</span><span class="sxs-lookup"><span data-stu-id="78208-149">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span></span>   <span data-ttu-id="78208-150">Se o PWA real não exigir acesso ao WinRT, você poderá mudar o `WinRT Access` valor para `None` .</span><span class="sxs-lookup"><span data-stu-id="78208-150">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span></span>  <span data-ttu-id="78208-151">De qualquer forma, certifique-se de subfator a `http://example.com` cadeia de caracteres padrão com o URI do seu PWA ou seu aplicativo não pode carregar corretamente no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="78208-151">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span></span>  
    <span data-ttu-id="78208-152">Você está pronto para executar e depurar o PWA como um aplicativo do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="78208-152">You are ready to run and debug your PWA as a Windows 10 app.</span></span>  <span data-ttu-id="78208-153">Se você estiver usando um site localhost para percorrer este guia, verifique se ele está em execução.</span><span class="sxs-lookup"><span data-stu-id="78208-153">If you are using a localhost site to step through this guide, make sure it is running.</span></span>  <span data-ttu-id="78208-154">Siga</span><span class="sxs-lookup"><span data-stu-id="78208-154">Then,</span></span>  
1.  <span data-ttu-id="78208-155">Compilar \ ( `Ctrl` + `Shift` + `F5` \) e executar \ ( `F5` \) seu projeto do PWA.</span><span class="sxs-lookup"><span data-stu-id="78208-155">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span></span>  <span data-ttu-id="78208-156">Seu site agora deve ser iniciado em uma janela de aplicativo autônomo.</span><span class="sxs-lookup"><span data-stu-id="78208-156">Your website should now launch in a standalone app window.</span></span>  <span data-ttu-id="78208-157">Não somente é um aplicativo Web hospedado; Ele está sendo executado como um aplicativo Web progressivo instalado no Windows 10!</span><span class="sxs-lookup"><span data-stu-id="78208-157">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span></span>  

    ![PWA em execução em uma janela do WWAHost. exe](media/wwahost.png)  

## <span data-ttu-id="78208-159">Depurar o PWA \ (EdgeHTML \) como um aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="78208-159">Debug your PWA \(EdgeHTML\) as a Windows app</span></span>  

<span data-ttu-id="78208-160">Como um PWA \ (EdgeHTML \) é simplesmente um aplicativo Web hospedado aprimorado progressivamente, você pode depurar o código do lado do servidor da mesma forma que qualquer aplicativo Web, usando o IDE e o fluxo de trabalho usuais.</span><span class="sxs-lookup"><span data-stu-id="78208-160">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span></span>  <span data-ttu-id="78208-161">As alterações que você implantar ao vivo serão refletidas no seu PWA instalado na próxima vez que você iniciá-lo \ (não é necessário implantar novamente seu pacote de aplicativo universal do Windows \).</span><span class="sxs-lookup"><span data-stu-id="78208-161">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span></span>

<span data-ttu-id="78208-162">Para a depuração do lado do cliente em seu aplicativo do Windows 10, você deve ter o `Microsoft Edge DevTools Preview` aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-162">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span></span>  <span data-ttu-id="78208-163">Este aplicativo autônomo inclui toda a funcionalidade do [Microsoft Edge do Microsoft Edge devtools][DevToolsGuide] \ (incluindo as [Ferramentas do PWA][DevToolsGuideServiceWorkers]), além de suporte de [depuração remota][DevToolsProtocol01ClientsEdgePreview] básica e um [seletor de destino de depuração][DevToolsGuideMicrosoftStoreApp] para anexar a qualquer instância em execução do mecanismo EdgeHTML, incluindo suplementos do Office, Cortana, webviews de aplicativos e, é claro, PWAs executados no Windows.</span><span class="sxs-lookup"><span data-stu-id="78208-163">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span></span>  

<span data-ttu-id="78208-164">Veja como configurar a depuração para seu PWA \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="78208-164">Here is how to set up debugging for your PWA \(EdgeHTML\).</span></span>  

1.  <span data-ttu-id="78208-165">Instale o aplicativo [Microsoft Edge devtools Preview][MicrosoftStoreEdgeDevtoolsPreview] da Microsoft Store se ainda não o tiver.</span><span class="sxs-lookup"><span data-stu-id="78208-165">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span></span>  
1.  <span data-ttu-id="78208-166">Com o site do PWA em funcionamento, inicie o aplicativo DevTools.</span><span class="sxs-lookup"><span data-stu-id="78208-166">With your PWA site up and running, launch the DevTools app.</span></span>  
1.  <span data-ttu-id="78208-167">No Visual Studio, inicie o aplicativo do Windows 10 com `Start Without Debugging` o `Ctrl` + `F5` comando ().</span><span class="sxs-lookup"><span data-stu-id="78208-167">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span></span>  <span data-ttu-id="78208-168">\ (O aplicativo DevTools não é anexado corretamente se o depurador do Visual Studio estiver ativo. \)</span><span class="sxs-lookup"><span data-stu-id="78208-168">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span></span>  
1.  <span data-ttu-id="78208-169">No aplicativo DevTools, clique no botão **Atualizar** no seletor de destino de depuração local.</span><span class="sxs-lookup"><span data-stu-id="78208-169">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span></span>  <span data-ttu-id="78208-170">Seu site do PWA \ (EdgeHTML \) agora deve estar listado.</span><span class="sxs-lookup"><span data-stu-id="78208-170">Your PWA \(EdgeHTML\) site should now be listed.</span></span>  <span data-ttu-id="78208-171">\ (Se ele também estiver sendo executado em uma janela do navegador, será a última instância desse site na lista. \)</span><span class="sxs-lookup"><span data-stu-id="78208-171">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span></span>  
1.  <span data-ttu-id="78208-172">Clique em sua lista de sites do PWA \ (EdgeHTML \) para abrir uma nova guia de instância do DevTools e iniciar a depuração.</span><span class="sxs-lookup"><span data-stu-id="78208-172">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span></span>  
    
    ![Seletor de destinos de depuração local no aplicativo Microsoft Edge DevTools](media/devtools-local.png)  
    
1.  <span data-ttu-id="78208-174">Você pode verificar se o DevTools está anexado ao seu aplicativo executando-executando-como-Windows-aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-174">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span></span>  <span data-ttu-id="78208-175">No **console**do devtools, digite:</span><span class="sxs-lookup"><span data-stu-id="78208-175">In the DevTools **Console**, type:</span></span>  
    
    ```shell
    window.Windows
    ```  
    
    <span data-ttu-id="78208-176">Isso retorna o `Windows Runtime` objeto global que contém todos os [namespaces do WinRT de nível superior](#find-windows-runtime-winrt-apis).</span><span class="sxs-lookup"><span data-stu-id="78208-176">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span></span>  <span data-ttu-id="78208-177">Esse é o seu EntryPoint \ (EdgeHTML \) do PWA para a [plataforma universal do Windows][WindowsUWPIndex]e só está exposto a aplicativos Web que são executados como aplicativos do Windows 10 (sendo executados fora do navegador, em um `WWAHost.exe` processo).</span><span class="sxs-lookup"><span data-stu-id="78208-177">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span></span>  
    
## <span data-ttu-id="78208-178">Encontrar APIs do Windows Runtime \ (WinRT \)</span><span class="sxs-lookup"><span data-stu-id="78208-178">Find Windows Runtime \(WinRT\) APIs</span></span>  

<span data-ttu-id="78208-179">Como um aplicativo instalado do Windows, seu [PWA \ (EdgeHTML \) tem acesso completo a APIs nativas do Windows Runtime][WindowsRuntime]; Identifique o que você precisa usar, obtenha as permissões necessárias e empregue a detecção de recursos para enviar essa solicitação de API em ambientes compatíveis.</span><span class="sxs-lookup"><span data-stu-id="78208-179">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span></span>  <span data-ttu-id="78208-180">Siga este processo para adicionar um aperfeiçoamento progressivo para usuários da área de trabalho do Windows do seu PWA.</span><span class="sxs-lookup"><span data-stu-id="78208-180">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span></span>  

<span data-ttu-id="78208-181">Há várias maneiras de identificar as APIs da plataforma universal do Windows necessárias para o seu PWA do Windows, incluindo a pesquisa de uma ampla [documentação UWP no centro de desenvolvimento do Windows] [UWP/API/], o download e a execução de [exemplos de código UWP](#uwp-code-samples) com o Visual Studio e a navegação em trechos de código para tarefas comuns do PWAs no Windows.</span><span class="sxs-lookup"><span data-stu-id="78208-181">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span></span>

<span data-ttu-id="78208-182">Há várias maneiras de identificar as APIs da plataforma universal do Windows necessárias para o seu Windows PWA, incluindo a pesquisa de uma abrangente [documentos UWP no centro de desenvolvimento do Windows] [UWP/API/], o download e a execução de [exemplos de código UWP](#uwp-code-samples) com o Visual Studio e a navegação em trechos de código para tarefas comuns do [PWAs no Windows 10 10 (EdgeHTML)][PwaIndexWindows10].</span><span class="sxs-lookup"><span data-stu-id="78208-182">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span></span>  

<span data-ttu-id="78208-183">Em geral, as APIs do WinRT funcionam em JavaScript da mesma forma que no C#, portanto, você pode seguir a documentação geral da [plataforma universal do Windows][WindowsUWPIndex] e a [referência de API][UwpApiIndex] para uso.</span><span class="sxs-lookup"><span data-stu-id="78208-183">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span></span>  <span data-ttu-id="78208-184">No entanto, observe as seguintes diferenças:</span><span class="sxs-lookup"><span data-stu-id="78208-184">However, please note the following differences:</span></span>  

*   <span data-ttu-id="78208-185">Os recursos do WinRT em JavaScript usam diferentes convenções de uso de [maiúsculas][ScriptingJsinrtUsingWinRTCasingConventions]</span><span class="sxs-lookup"><span data-stu-id="78208-185">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span></span>  
*   <span data-ttu-id="78208-186">[Os eventos são representados como identificadores de cadeia de caracteres][ScriptingJsinrtHandlingWinRTEvents] passados para `addEventListener` / `removeEventListener` métodos de classe</span><span class="sxs-lookup"><span data-stu-id="78208-186">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span></span>  
*   <span data-ttu-id="78208-187">[Métodos assíncronos][ScriptingJsinrtUsingWinRT] usam o modelo JavaScript Promise</span><span class="sxs-lookup"><span data-stu-id="78208-187">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span></span>  
*   <span data-ttu-id="78208-188">APIs no `Windows.UI.Xaml` namespace não são compatíveis com aplicativos JavaScript, que em vez disso usam a pilha de renderização da Web do mecanismo [EdgeHTML][DevGuideWhatsNew] \ (HTML, CSS \)</span><span class="sxs-lookup"><span data-stu-id="78208-188">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span></span>  

<span data-ttu-id="78208-189">Para obter mais detalhes, consulte [usando o Windows Runtime em JavaScript][WindowRuntimeUsingJavascript].</span><span class="sxs-lookup"><span data-stu-id="78208-189">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span></span>  

### <span data-ttu-id="78208-190">Exemplos de código UWP</span><span class="sxs-lookup"><span data-stu-id="78208-190">UWP code samples</span></span>  

<span data-ttu-id="78208-191">Confira o repositório de [exemplos de código da plataforma universal do Windows \ (UWP \)][MicrosoftDeveloperWindowsSamples] para procurar exemplos de JavaScript para cenários comuns de aplicativos do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="78208-191">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span></span>  <span data-ttu-id="78208-192">Embora as versões do JS dessas amostras usem a biblioteca [WinJS][GithubWinjsWinjs] para estruturar o modelo de exemplo, WinJS não é necessário para enviar as solicitações de API do WinRT demonstradas nestes exemplos.</span><span class="sxs-lookup"><span data-stu-id="78208-192">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span></span>  

> [!NOTE]
> <span data-ttu-id="78208-193">Se precisar escutar o [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] evento do aplicativo, você poderá fazer isso usando a seguinte API do WinRT nativo:</span><span class="sxs-lookup"><span data-stu-id="78208-193">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span></span>  
> 
> **<span data-ttu-id="78208-194">Use este</span><span class="sxs-lookup"><span data-stu-id="78208-194">Use this</span></span>**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> <span data-ttu-id="78208-195">... em oposição a esse tipo de solicitação de WinJS usado nos exemplos:</span><span class="sxs-lookup"><span data-stu-id="78208-195">... as opposed this type of WinJS request used in the samples:</span></span>  
> 
> **<span data-ttu-id="78208-196">Não é isso</span><span class="sxs-lookup"><span data-stu-id="78208-196">Not this</span></span>**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## <span data-ttu-id="78208-197">Enviar solicitações de API do WinRT do seu PWA (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="78208-197">Send WinRT API requests from your PWA (EdgeHTML)</span></span>  

<span data-ttu-id="78208-198">Neste ponto, finja que você deseja adicionar um menu de contexto personalizado para usuários do Windows do nosso PWA \ (EdgeHTML \) e identificar as APIs necessárias no namespace [Windows. UI. popups][UwpApiWindowsUiPopups] .</span><span class="sxs-lookup"><span data-stu-id="78208-198">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span></span>  

<span data-ttu-id="78208-199">Para enviar quaisquer solicitações de APIs do WinRT de nosso PWA \ (EdgeHTML \), primeiro você precisa [estabelecer as permissões necessárias](#set-application-content-uri-rules-acurs) \ (ou, regras de URI de conteúdo do aplicativo \) no seu arquivo de manifesto do pacote de aplicativos do Windows \ ( `.appxmanifest` \).</span><span class="sxs-lookup"><span data-stu-id="78208-199">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span></span>  

<span data-ttu-id="78208-200">Se qualquer uma dessas solicitações de API envolver o acesso aos recursos do usuário, como imagens ou músicas, ou a recursos do dispositivo, como a câmera ou o microfone, você também precisará adicionar [declarações de funcionalidade do aplicativo](#app-capability-declarations) ao manifesto do pacote do aplicativo para que o Windows solicite a permissão do usuário.</span><span class="sxs-lookup"><span data-stu-id="78208-200">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span></span>  <span data-ttu-id="78208-201">Se, posteriormente, você publicar seu PWA \ (EdgeHTML \) na Microsoft Store, essas [permissões de aplicativo][MicrosoftSupportWindowsAppPermissions] necessárias também serão observadas na listagem da loja.</span><span class="sxs-lookup"><span data-stu-id="78208-201">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span></span>  

#### <span data-ttu-id="78208-202">Definir regras de URI de conteúdo do aplicativo (ACURs)</span><span class="sxs-lookup"><span data-stu-id="78208-202">Set Application Content URI Rules (ACURs)</span></span>  

<span data-ttu-id="78208-203">Por meio do ACURs, também conhecido como uma lista de permissão de URL, você pode fornecer às URLs do seu PWA \ (EdgeHTML \) acesso direto às APIs do Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="78208-203">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span></span>  <span data-ttu-id="78208-204">No nível do sistema operacional Windows, os limites de política corretos são definidos para permitir que o código hospedado em seu servidor Web envie diretamente solicitações de API de plataforma.</span><span class="sxs-lookup"><span data-stu-id="78208-204">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span></span>  <span data-ttu-id="78208-205">Você define esses limites no arquivo de manifesto do pacote do aplicativo quando especifica as URLs do PWA como `ApplicationContentUriRules` .</span><span class="sxs-lookup"><span data-stu-id="78208-205">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span></span>  

<span data-ttu-id="78208-206">Suas regras devem incluir a página inicial do aplicativo e quaisquer outras páginas que você queira incluir como páginas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-206">Your rules should include the start page for your app and any other pages you want included as app pages.</span></span>  <span data-ttu-id="78208-207">Se o usuário navegar para uma URL que não está incluída nas regras, o Windows abrirá a URL de destino no navegador Microsoft Edge, em vez de sua janela autônoma \ (EdgeHTML \) do PWA \ ( `WWAHost.exe` processo \).</span><span class="sxs-lookup"><span data-stu-id="78208-207">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span></span>  <span data-ttu-id="78208-208">Você também pode excluir URLs específicas.</span><span class="sxs-lookup"><span data-stu-id="78208-208">You may also exclude specific URLs.</span></span>  

<span data-ttu-id="78208-209">Há várias maneiras de especificar uma URL `Match` em suas regras:</span><span class="sxs-lookup"><span data-stu-id="78208-209">There are several ways to specify a URL `Match` in your rules:</span></span>  

*   <span data-ttu-id="78208-210">Um nome de host exato</span><span class="sxs-lookup"><span data-stu-id="78208-210">An exact hostname</span></span>  
*   <span data-ttu-id="78208-211">Um nome de host para o qual um URI com qualquer subdomínio desse nome de host é incluído ou excluído</span><span class="sxs-lookup"><span data-stu-id="78208-211">A hostname for which a URI with any subdomain of that hostname is included or excluded</span></span>  
*   <span data-ttu-id="78208-212">Um URI exato</span><span class="sxs-lookup"><span data-stu-id="78208-212">An exact URI</span></span>  
*   <span data-ttu-id="78208-213">Um URI exato contendo uma propriedade de consulta</span><span class="sxs-lookup"><span data-stu-id="78208-213">An exact URI containing a query property</span></span>  
*   <span data-ttu-id="78208-214">Um caminho parcial e um curinga para indicar uma extensão de arquivo específica para uma regra de inclusão</span><span class="sxs-lookup"><span data-stu-id="78208-214">A partial path and a wildcard to indicate a particular file extension for an include rule</span></span>  
*   <span data-ttu-id="78208-215">Caminhos relativos para regras de exclusão</span><span class="sxs-lookup"><span data-stu-id="78208-215">Relative paths for exclude rules</span></span>  

<span data-ttu-id="78208-216">Aqui estão alguns exemplos de ACURs em um `.appxmanifest` arquivo:</span><span class="sxs-lookup"><span data-stu-id="78208-216">Here are a few examples of ACURs in a `.appxmanifest` file:</span></span>  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

<span data-ttu-id="78208-217">As URLs definidas no ACURs para seu aplicativo podem receber permissão para o tempo de execução do Windows por meio do `WindowsRuntimeAccess` atributo, que aceita os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="78208-217">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span></span>  

*   `all`<span data-ttu-id="78208-218">: O código JavaScript remoto tem acesso a todas as APIs do WinRT e a componentes de pacotes locais.</span><span class="sxs-lookup"><span data-stu-id="78208-218">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span></span>  <span data-ttu-id="78208-219">O namespace [Windows \ (WinRT \))][UwpApiIndex] é injetado e está presente no mecanismo de script.</span><span class="sxs-lookup"><span data-stu-id="78208-219">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span></span>  
*   `allowForWeb`<span data-ttu-id="78208-220">: O acesso ao código JavaScript remoto está limitado a componentes de pacotes locais, incluindo componentes C++/C # personalizados.</span><span class="sxs-lookup"><span data-stu-id="78208-220">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span></span>  
*   `none`<span data-ttu-id="78208-221">Assume.</span><span class="sxs-lookup"><span data-stu-id="78208-221">: Default.</span></span>  <span data-ttu-id="78208-222">A URL especificada não tem acesso a plataforma.</span><span class="sxs-lookup"><span data-stu-id="78208-222">The specified URL has no platform access.</span></span>  

<span data-ttu-id="78208-223">Neste tutorial, você já definiu a única ACUR de que precisa \ (etapa 6 da configuração anterior [e executar a seção do aplicativo](#set-up-and-run-your-universal-windows-app) \) para o aplicativo de uma única página.</span><span class="sxs-lookup"><span data-stu-id="78208-223">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span></span>  <span data-ttu-id="78208-224">Você pode confirmar isso no painel URIs de **conteúdo** do designer do Visual Studio `package.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="78208-224">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span></span>  

![Painel URI do conteúdo do designer de appxmanifest do Visual Studio](media/vs-appxmanifest-editor-acurs.png)  

<span data-ttu-id="78208-226">Você também pode exibir o XML bruto do seu manifesto clicando com o botão direito do mouse `package.appxmanifest` no arquivo no Gerenciador de soluções do Visual Studio e selecionando **Exibir código** \ ( `F7` \).</span><span class="sxs-lookup"><span data-stu-id="78208-226">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span></span>  <span data-ttu-id="78208-227">Para alternar de volta para o modo de exibição de designer, selecione **View Designer** \ ( `Shift` + `F7` \).</span><span class="sxs-lookup"><span data-stu-id="78208-227">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span></span>  

#### <span data-ttu-id="78208-228">Declarações de funcionalidades do app</span><span class="sxs-lookup"><span data-stu-id="78208-228">App capability declarations</span></span>  

<span data-ttu-id="78208-229">Se seu aplicativo precisar de acesso programático a recursos do usuário, como imagens ou músicas, ou para dispositivos como uma câmera ou um microfone, você deve incluir as [declarações de funcionalidade do aplicativo][WindowsUwpPackagingAppCapabilities] correspondente em seu arquivo de manifesto do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-229">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span></span>  <span data-ttu-id="78208-230">Há três categorias de declaração de recurso de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="78208-230">There are three app capability declaration categories:</span></span>  

*   <span data-ttu-id="78208-231">[As funcionalidades de uso geral][WindowsUwpPackagingAppCapabilitiesGeneralUse] que se aplicam à maioria dos cenários de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="78208-231">[General-use capabilities][WindowsUwpPackagingAppCapabilitiesGeneralUse] that apply to most common app scenarios.</span></span>  
*   <span data-ttu-id="78208-232">[As funcionalidades do dispositivo][WindowsUwpPackagingAppCapabilitiesDevice] que permitem que seu aplicativo acesse dispositivos periféricos e internos.</span><span class="sxs-lookup"><span data-stu-id="78208-232">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span></span>  
*   <span data-ttu-id="78208-233">[Recursos de uso especial][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] que dão suporte a cenários empresariais e exigem uma conta da empresa da Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="78208-233">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span></span>  <span data-ttu-id="78208-234">Para saber mais sobre contas empresariais, consulte [Tipos de conta, locais e taxas][WindowsUwpPublishAccountTypesLocationsFees].</span><span class="sxs-lookup"><span data-stu-id="78208-234">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span></span>

<span data-ttu-id="78208-235">Sua página do aplicativo Microsoft Store lista todas as funcionalidades declaradas no manifesto do pacote do aplicativo, portanto, certifique-se de especificar apenas as funcionalidades que o seu aplicativo realmente usa.</span><span class="sxs-lookup"><span data-stu-id="78208-235">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span></span>

<span data-ttu-id="78208-236">Alguns recursos fornecem acesso aos recursos confidenciais dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="78208-236">Some capabilities provide apps access to sensitive resources.</span></span>  <span data-ttu-id="78208-237">Esses recursos são considerados confidenciais porque cada um pode acessar os dados pessoais do usuário ou custar dinheiro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="78208-237">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span></span>  <span data-ttu-id="78208-238">As configurações de privacidade, gerenciadas pelo aplicativo [configurações][BingResultsWindows10Settings] do Windows 10, permitem que o usuário controle dinamicamente o acesso a recursos confidenciais.</span><span class="sxs-lookup"><span data-stu-id="78208-238">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span></span>  <span data-ttu-id="78208-239">Portanto, é importante que seu aplicativo não assuma que um recurso confidencial sempre está disponível.</span><span class="sxs-lookup"><span data-stu-id="78208-239">Thus, it is important that your app does not assume a sensitive resource is always available.</span></span>  <span data-ttu-id="78208-240">Para obter mais informações sobre como acessar recursos confidenciais, consulte [Diretrizes para aplicativos com reconhecimento de privacidade][WindowsUwp|::ref2::|Index].</span><span class="sxs-lookup"><span data-stu-id="78208-240">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwp|::ref2::|Index].</span></span>  

<span data-ttu-id="78208-241">Você solicita acesso declarando funcionalidades no manifesto do pacote para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78208-241">You request access by declaring capabilities in the package manifest for your app.</span></span>  <span data-ttu-id="78208-242">No Visual Studio, você pode fazer isso a partir do painel de **recursos** do designer Package. appxmanifest.</span><span class="sxs-lookup"><span data-stu-id="78208-242">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span></span>  

![Painel de funcionalidades do designer do Visual Studio appxmanifest](media/vs-appxmanifest-editor-capabilities.png)  

<span data-ttu-id="78208-244">Neste tutorial, somente a funcionalidade padrão da Internet \ (cliente \) é necessária, portanto, não é necessária nenhuma ação adicional.</span><span class="sxs-lookup"><span data-stu-id="78208-244">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span></span>  

### <span data-ttu-id="78208-245">Usar a detecção de recursos para invocar o WinRT</span><span class="sxs-lookup"><span data-stu-id="78208-245">Use feature detection to invoke WinRT</span></span>  

<span data-ttu-id="78208-246">Para garantir uma experiência de linha de base de qualidade para o seu público do PWA em todas as plataformas, você aprimora progressivamente a experiência do PWA no Windows usando a detecção de recursos do WinRT.</span><span class="sxs-lookup"><span data-stu-id="78208-246">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span></span>  <span data-ttu-id="78208-247">Dessa forma, você pode ter certeza de que seu código específico do Windows é executado apenas em um contexto em que as APIs do WinRT estão disponíveis e são aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="78208-247">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span></span>  

<span data-ttu-id="78208-248">A detecção de recursos pode ser tão simples quanto procurar o `Windows` objeto \ (o ponto de entrada para o [namespace do WinRT][UwpApiIndex]\) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="78208-248">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span></span>  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="78208-249">No entanto, Considerando que nem todas as APIs do Windows estão disponíveis em todos os [tipos de dispositivo do Windows 10][UwpExtensionSdkDeviceFamiliesOverview], geralmente é útil usar a detecção de recursos mais específica para qualificar ainda mais o namespace da solicitação de API que você está enviando:</span><span class="sxs-lookup"><span data-stu-id="78208-249">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span></span>  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="78208-250">Com esse plano de fundo, você está pronto para adicionar um código do WinRT para implementar um menu de contexto personalizado.</span><span class="sxs-lookup"><span data-stu-id="78208-250">With that background, you are ready to add some WinRT code to implement a custom context menu.</span></span>  <span data-ttu-id="78208-251">Se você estiver usando o PWA de exemplo de [introdução com Web Apps progressivos][PwaGetStarted]:</span><span class="sxs-lookup"><span data-stu-id="78208-251">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span></span>

1.  <span data-ttu-id="78208-252">Abra o Visual Studio para seu projeto de site do PWA.</span><span class="sxs-lookup"><span data-stu-id="78208-252">Open Visual Studio to your PWA site project.</span></span>

1.  <span data-ttu-id="78208-253">No Gerenciador de soluções, abra o `views\layout.pug` arquivo e adicione a seguinte linha, logo abaixo da `script` referência para seu trabalhador do serviço:</span><span class="sxs-lookup"><span data-stu-id="78208-253">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span></span>
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  <span data-ttu-id="78208-254">No Gerenciador de soluções, clique com o botão direito do mouse na `javascripts` pasta e **adicione**  >  **novo arquivo..**..</span><span class="sxs-lookup"><span data-stu-id="78208-254">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span></span>

1.  <span data-ttu-id="78208-255">Nomeie seu arquivo: `site.js` e copie no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="78208-255">Name your file: `site.js`, and copy in the following code:</span></span>
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```

1.  <span data-ttu-id="78208-256">Compare o comportamento do menu de contexto quando você executa o PWA no navegador \ ( `F5` do projeto de site do PWA \) em vez de dentro da janela de aplicativo do Windows \ ( `F5` do seu projeto de aplicativo universal do Windows \).</span><span class="sxs-lookup"><span data-stu-id="78208-256">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span></span>  <span data-ttu-id="78208-257">No navegador, clicar com o botão direito do mouse oferece o menu de contexto padrão do Microsoft Edge, enquanto `WWAHost.exe` , no processo, o menu personalizado agora é exibido.</span><span class="sxs-lookup"><span data-stu-id="78208-257">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span></span>  

    | <span data-ttu-id="78208-258">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="78208-258">Microsoft Edge</span></span> | <span data-ttu-id="78208-259">Aplicativo do Windows 10</span><span class="sxs-lookup"><span data-stu-id="78208-259">Windows 10 app</span></span> |  
    |:--- |:---- |  
    | ![Menu de contexto padrão do navegador](media/browser-context-menu.png) | ![Menu de contexto personalizado do aplicativo](media/app-context-menu.png) |  

<span data-ttu-id="78208-262">Espero que agora você tenha uma base sólida para melhorar progressivamente seu PWAs no Windows.</span><span class="sxs-lookup"><span data-stu-id="78208-262">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span></span>  <span data-ttu-id="78208-263">Se você tiver dúvidas ou algo não estiver claro, envie um comentário!</span><span class="sxs-lookup"><span data-stu-id="78208-263">If you run into questions or anything is unclear, please send a comment!</span></span>  

## <span data-ttu-id="78208-264">Aprofundamento</span><span class="sxs-lookup"><span data-stu-id="78208-264">Going further</span></span>

<span data-ttu-id="78208-265">O [centro de desenvolvimento do Windows][MicrosoftDeveloperWindowsApps] é a referência completa para todos os estágios do prédio do aplicativo Windows, desde a [introdução][MicrosoftDeveloperWindowsAppsGetStarted]até o [design][MicrosoftDeveloperWindowsAppsDesign], o [desenvolvimento][MicrosoftDeveloperWindowsAppsDevelop]e a [publicação][MicrosoftDeveloperStorePublishApps] na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="78208-265">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span></span>  

<span data-ttu-id="78208-266">Para obter uma visão geral da plataforma universal do Windows \ (UWP \) e como se concentrar em famílias de dispositivos Windows 10 diferentes, consulte [Intro para a plataforma universal do Windows][WindowsUWPGetStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="78208-266">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span></span>  

<span data-ttu-id="78208-267">E quando estiver pronto, veja como \ (e por quê! \) [enviar seu PWA para a Microsoft Store](./microsoft-store.md).</span><span class="sxs-lookup"><span data-stu-id="78208-267">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span></span>  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Introdução aos aplicativos Web progressivos"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs no Windows 10 (EdgeHTML)-aplicativos Web progressivos no Windows"  
[DevToolsGuide]: ../devtools-guide.md "Ferramentas de desenvolvedor do Microsoft Edge (EdgeHTML)"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Aplicativo da Microsoft Store-ferramentas para desenvolvedores do Microsoft Edge (EdgeHTML)"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Trabalhadores do serviço"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clientes do protocolo DevTools preview do Microsoft Edge-DevTools"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Novidades do EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Tempo de execução do Windows (WinRT) para JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Usar o tempo de execução do Windows em JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Manipulando eventos do Windows Runtime em JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Usando métodos assíncronos do tempo de execução do Windows"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Convenções de maiúsculas e minúsculas com recursos do Windows Runtime-usando o Windows Runtime em JavaScript"  
[UwpApiIndex]: /uwp/api/index "Namespaces UWP do Windows"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Namespace Windows. UI. popups"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "Evento WebUIApplication. Activated"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Visão geral das famílias de dispositivos"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "Como o Visual Studio gera um manifesto do pacote do aplicativo"  
[WindowsUWPIndex]: /windows/uwp/index "Documentação da plataforma universal do Windows"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "O que é um aplicativo da plataforma universal do Windows (UWP)?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar seu dispositivo para desenvolvimento"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Segurança"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Tipos de conta, localizações e taxas"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Recursos restritos"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Recursos do dispositivo"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Recursos de uso geral"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "Declarações de funcionalidade do aplicativo"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "configurações do Windows 10-Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Publicar aplicativos e jogos do Windows"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Documentação da plataforma universal do Windows"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Projetar e codificar aplicativos do Windows"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Desenvolver aplicativos UWP"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Comece a usar os aplicativos do Windows 10"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Exemplos de código"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools Preview"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "Permissões de aplicativo"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Fará"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Visualização do Visual Studio"  
