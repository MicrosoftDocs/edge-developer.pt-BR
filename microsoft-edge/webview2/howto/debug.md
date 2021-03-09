---
description: Saiba como depurar controles WebView2.
title: Começar a depurar aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: f895634d5e005bb07579d9a5f41c6a988cd78a33
ms.sourcegitcommit: 140e09e508fa97f2d124f264d7d2ff77d12d1ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "11399841"
---
# <a name="get-started-debugging-webview2-apps"></a><span data-ttu-id="0a3d6-104">Começar a depurar aplicativos WebView2</span><span class="sxs-lookup"><span data-stu-id="0a3d6-104">Get started debugging WebView2 apps</span></span>  

<span data-ttu-id="0a3d6-105">O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos e ferramentas de desenvolvimento de aplicativos nativos e web.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native app development features and tools.</span></span>  <span data-ttu-id="0a3d6-106">Ao desenvolver seu aplicativo WebView2, você deve depurar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-106">When you develop your WebView2 app, you should debug your app.</span></span>  <span data-ttu-id="0a3d6-107">Este artigo descreve as diferentes ferramentas a ser usadas para depurar sua Web e código nativo em seu aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 app.</span></span>  

## [<a name="microsoft-edge-devtools"></a><span data-ttu-id="0a3d6-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0a3d6-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="0a3d6-109">Use as Ferramentas de Desenvolvedor do [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você pode depurar para outra página da Web exibida no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="0a3d6-110">Para abrir o DevTools, de definir o foco no controle WebView e, em seguida, use uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="0a3d6-111">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-111">Select `F12`.</span></span>  
*   <span data-ttu-id="0a3d6-112">Selecione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="0a3d6-113">Abra o menu de contexto \(clique com o botão direito do mouse\) e escolha `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="0a3d6-114">Para obter mais informações, navegue até [DevTools overview][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="0a3d6-114">For more information, navigate to [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="DevTools depuração" lightbox="./media/f12.png":::
   <span data-ttu-id="0a3d6-116">DevTools depuração</span><span class="sxs-lookup"><span data-stu-id="0a3d6-116">DevTools debugging</span></span>  
:::image-end:::  

## [<a name="visual-studio"></a><span data-ttu-id="0a3d6-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a3d6-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="0a3d6-118">Visual Studio fornece várias ferramentas de depuração para web e código nativo em aplicativos WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-118">Visual Studio provides various debugging tools for web and native code in WebView2 apps.</span></span>  <span data-ttu-id="0a3d6-119">Na seção Visual Studio, o foco principal é depurar controles WebView, no entanto, os outros métodos de depuração no Visual Studio estão disponíveis como de costume.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="0a3d6-120">Use o processo a seguir para depurar código nativo e web em aplicativos win32 ou somente em complementos do Office.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-120">Use the following process to debug web and native code in Win32 apps or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0a3d6-121">Quando você depura seu aplicativo Visual Studio com o depurador nativo anexado, a seleção pode disparar o depurador nativo em vez de Ferramentas do `F12` Desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-121">When you debug your app in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="0a3d6-122">Selecione `Ctrl` + `Shift` + `I` , ou use o menu de contexto \(clique com o botão direito do mouse\) para evitar a situação.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="0a3d6-123">Antes de começar, certifique-se de que os seguintes requisitos sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="0a3d6-124">Para depurar scripts, o aplicativo deve ser lançado de dentro Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="0a3d6-125">Não é possível anexar um depurador a um processo WebView2 em execução.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="0a3d6-126">Instale Visual Studio versão 2019 16.4 Preview 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="0a3d6-127">Instalar e configurar as ferramentas de depurador de script em Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="0a3d6-128">Conclua as seguintes ações para instalar o componente de diagnóstico **JavaScript** no **desenvolvimento da área de trabalho com C++**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    
    1.  <span data-ttu-id="0a3d6-129">Na barra do Windows Explorer, digite `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="0a3d6-130">Escolha **Visual Studio Instalador para** abri-lo.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="0a3d6-131">No Visual Studio Instalador, na versão instalada, escolha o botão **Mais** e escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="0a3d6-132">Em Visual Studio, em **Cargas de Trabalho,** escolha a configuração Desenvolvimento da Área de Trabalho **em C++.**</span><span class="sxs-lookup"><span data-stu-id="0a3d6-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio de Modificação de Cargas de Trabalho" lightbox="./media/workloads.png":::
            <span data-ttu-id="0a3d6-134">Visual Studio de Modificação de Cargas de Trabalho</span><span class="sxs-lookup"><span data-stu-id="0a3d6-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="0a3d6-135">Escolha **Componentes individuais**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="0a3d6-136">Na caixa de pesquisa, digite `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="0a3d6-137">Escolha a **configuração de diagnóstico JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="0a3d6-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="0a3d6-138">Escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio guia Modificando Componentes Individuais" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="0a3d6-140">Visual Studio guia Modificando Componentes Individuais</span><span class="sxs-lookup"><span data-stu-id="0a3d6-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="0a3d6-141">Habilitar a depuração de script para aplicativos WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-141">Enable script debugging for WebView2 apps.</span></span>  
    1.  <span data-ttu-id="0a3d6-142">Em seu projeto WebView2, abra o menu de contexto \(clique com o botão direito do mouse\) e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="0a3d6-143">Em Propriedades **de Configuração,** escolha **Depuração**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="0a3d6-144">Em Tipo **de Depurador,** escolha **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio Propriedade de Configuração de Depuração" lightbox="./media/enbjs.png":::
           <span data-ttu-id="0a3d6-146">Visual Studio Propriedade **de Configuração de Depuração**</span><span class="sxs-lookup"><span data-stu-id="0a3d6-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="0a3d6-147">Conclua as seguintes ações para depurar seu aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-147">Complete the following actions to debug your WebView2 app.</span></span>  

1.  <span data-ttu-id="0a3d6-148">Para definir um ponto de interrupção no código-fonte, passe o mouse para a esquerda do número de linha e escolha definir um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="0a3d6-149">O adaptador de depuração JS/TS não executa o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="0a3d6-150">Você deve abrir exatamente o mesmo caminho associado ao seu WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio adicionar ponto de interrupção" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="0a3d6-152">Visual Studio adicionar ponto de interrupção</span><span class="sxs-lookup"><span data-stu-id="0a3d6-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a3d6-153">Para executar o depurador, escolha o tamanho do bit da plataforma e, em seguida, escolha o botão de reprodução verde ao lado de **Depurador local do Windows**.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="0a3d6-154">O aplicativo é executado e o depurador se conecta ao primeiro processo WebView2 criado.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-154">The app runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Depurador local do Windows" lightbox="./media/run.png"::: 
       <span data-ttu-id="0a3d6-156">Visual Studio **Depurador local do Windows**</span><span class="sxs-lookup"><span data-stu-id="0a3d6-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0a3d6-157">No **Console de Depuração,** encontre a saída do depurador.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio Console de Depuração" lightbox="./media/console.png"::: 
       <span data-ttu-id="0a3d6-159">Visual Studio Console **de Depuração**</span><span class="sxs-lookup"><span data-stu-id="0a3d6-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a><span data-ttu-id="0a3d6-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0a3d6-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="0a3d6-161">Use o Código Visual Studio Microsoft para depurar scripts executados em controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="0a3d6-162">Em Visual Studio Código, conclua as seguintes ações para depurar seu código.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="0a3d6-163">Seu projeto é necessário para ter um `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="0a3d6-164">Se seu projeto não tiver um arquivo, copie o trecho de código a seguir `launch.json` e crie um novo `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="0a3d6-165">Visual Studio mapeamento de caminho de origem do código agora requer a URL, portanto, seu aplicativo agora recebe um parâmetro de linha de comando quando ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-165">Visual Studio Code source path mapping now requires the URL, so your app now receives a command-line parameter when it starts.</span></span>  <span data-ttu-id="0a3d6-166">Você pode ignorar com segurança o `url` parâmetro, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-166">You may safely ignore the `url` parameter if needed.</span></span>  
    
1.  <span data-ttu-id="0a3d6-167">Para definir um ponto de interrupção no código-fonte, passe o mouse na linha e selecione</span><span class="sxs-lookup"><span data-stu-id="0a3d6-167">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="O ponto de interrupção é definido Visual Studio Código" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="0a3d6-169">O ponto de interrupção é definido Visual Studio Código</span><span class="sxs-lookup"><span data-stu-id="0a3d6-169">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="0a3d6-170">Execute o código.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-170">Run the code.</span></span>  
    1.  <span data-ttu-id="0a3d6-171">Na guia **Executar,** escolha a configuração de início no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="0a3d6-172">Para começar a depurar seu aplicativo, escolha Iniciar Depuração, que é o triângulo verde ao lado da configuração de início listada.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-172">To start debugging your app, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio guia Executar Código" lightbox="./media/runvs.png":::
           <span data-ttu-id="0a3d6-174">Visual Studio guia Executar Código</span><span class="sxs-lookup"><span data-stu-id="0a3d6-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="0a3d6-175">Abra **o Console de Depuração** para exibir a saída e os erros de depuração.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio Depuração de Código" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="0a3d6-177">Visual Studio Depuração de Código</span><span class="sxs-lookup"><span data-stu-id="0a3d6-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0a3d6-178">**Configurações Avançadas**:</span><span class="sxs-lookup"><span data-stu-id="0a3d6-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="0a3d6-179">Depuração de Webview direcionada.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="0a3d6-180">Em alguns aplicativos WebView2, você pode usar mais de um controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-180">In some WebView2 apps, you may use more than one WebView2 control.</span></span> <span data-ttu-id="0a3d6-181">Para escolher o controle WebView2 para depurar nessa situação, você pode usar a depuração de webview2 direcionada</span><span class="sxs-lookup"><span data-stu-id="0a3d6-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="0a3d6-182">Abra `launch.json` e conclua as seguintes ações para usar a depuração de Webview direcionada.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="0a3d6-183">Confirme se o `useWebview` parâmetro está definido como `true` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="0a3d6-184">Adicione o `urlFilter` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="0a3d6-185">Quando o controle WebView2 navega para uma URL, o valor do parâmetro é usado para comparar cadeias de caracteres que `urlFilter` aparecem na URL.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="0a3d6-186">Ao depurar seu aplicativo, talvez seja necessário passar pelo código desde o início do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-186">When debugging your app, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="0a3d6-187">Se você estiver renderizando páginas da Web em sites e não tiver acesso ao código-fonte, poderá usar a opção, pois as páginas da Web ignoram parâmetros não `?=value`  reconhecedos.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="0a3d6-188">Depois que a primeira combinação for encontrada na URL, o depurador será interrompido.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="0a3d6-189">Não é possível depurar dois controles WebView2 ao mesmo tempo porque a porta CDP é compartilhada por todos os controles WebView2 e usa um único número de porta.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="0a3d6-190">Depurar processos em execução</span><span class="sxs-lookup"><span data-stu-id="0a3d6-190">Debug running processes</span></span>  
    
    <span data-ttu-id="0a3d6-191">Talvez seja necessário anexar o depurador a processos WebView2 em execução.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="0a3d6-192">Para fazer isso, em `launch.json` , `request` atualize o parâmetro para `attach` .</span><span class="sxs-lookup"><span data-stu-id="0a3d6-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="0a3d6-193">Seu controle WebView2 deve abrir a porta CDP para permitir a depuração do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="0a3d6-194">Seu código deve ser criado para garantir que apenas um controle WebView2 tenha uma porta CDP (Chrome Developer Protocol) aberta, antes de iniciar o depurador.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="0a3d6-195">Opções de rastreamento de depuração</span><span class="sxs-lookup"><span data-stu-id="0a3d6-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="0a3d6-196">Adicione o `trace` parâmetro launch.jspara habilitar o rastreamento de depuração.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="0a3d6-197">Adicionar `trace` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Salve a saída de depuração em um arquivo de log." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="0a3d6-199">Salvar a saída de depuração em um arquivo de log</span><span class="sxs-lookup"><span data-stu-id="0a3d6-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Saída detalhada" lightbox="./media/verbose.png":::
                 <span data-ttu-id="0a3d6-201">Visual Studio Saída de Depuração de Código com rastreamento detalhado ligado</span><span class="sxs-lookup"><span data-stu-id="0a3d6-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="0a3d6-202">Depurar Os Complementos do Office.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-202">Debug Office Add-ins.</span></span>  
    
    <span data-ttu-id="0a3d6-203">Se você estiver depurando os Complementos do Office, abra o código-fonte do add-in em uma instância separada de Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="0a3d6-204">Abra launch.jsem seu aplicativo WebView2 e adicione o seguinte trecho de código para anexar o depurador ao complemento do Office.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-204">Open launch.json in your WebView2 app and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="0a3d6-205">Solução de problemas do depurador</span><span class="sxs-lookup"><span data-stu-id="0a3d6-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="0a3d6-206">Você pode encontrar os seguintes cenários ao usar o depurador.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="0a3d6-207">O depurador não para no ponto de interrupção e você tem saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="0a3d6-208">Para resolver o problema, confirme se o arquivo com o ponto de interrupção é o mesmo arquivo usado pelo controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="0a3d6-209">O depurador não executa o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="0a3d6-210">Você não pode anexar a um processo em execução e obter um erro de tempo de tempo.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="0a3d6-211">Para resolver o problema, confirme se o controle WebView2 abriu a porta CDP.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="0a3d6-212">Verifique se  `additionalBrowserArguments`  o valor no Registro está correto ou se as opções estão corretas.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="0a3d6-213">Para obter mais informações, navegue até [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] e [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="0a3d6-213">For more information, navigate to [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  

## <a name="see-also"></a><span data-ttu-id="0a3d6-214">Veja também</span><span class="sxs-lookup"><span data-stu-id="0a3d6-214">See also</span></span>  

*   <span data-ttu-id="0a3d6-215">Para começar a usar WebView2, navegue até [WebView2 Guia de Iniciação.][Webview2MainGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="0a3d6-215">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="0a3d6-216">Para um exemplo abrangente de recursos WebView2, navegue até o repositório [WebView2Samples][GithubMicrosoftedgeWebview2samples] no GitHub.</span><span class="sxs-lookup"><span data-stu-id="0a3d6-216">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="0a3d6-217">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="0a3d6-217">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="0a3d6-218">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="0a3d6-218">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="0a3d6-219">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="0a3d6-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriedade CoreWebView2EnvironmentOptions.AdditionalBrowserArguments (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment - Globals | Microsoft Docs"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referência da API do Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Introdução - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
