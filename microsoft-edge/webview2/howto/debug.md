---
description: Saiba como depurar controles WebView2.
title: Introdução à depuração de aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 4f94fe880f66f8aeb387d2db4a8bfaab20699466
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230695"
---
# <span data-ttu-id="0cf09-104">Introdução à depuração de aplicativos WebView2</span><span class="sxs-lookup"><span data-stu-id="0cf09-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="0cf09-105">O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos e ferramentas de desenvolvimento de aplicativo Web e nativo.</span><span class="sxs-lookup"><span data-stu-id="0cf09-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="0cf09-106">Ao desenvolver seu aplicativo WebView2, você deve depurar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0cf09-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="0cf09-107">Este artigo descreve as diferentes ferramentas a serem usadas para depurar o código nativo e Web em seu aplicativo do WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="0cf09-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0cf09-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="0cf09-109">Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que você pode depurar para outra página da Web exibida no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0cf09-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="0cf09-110">Para abrir o DevTools, defina o foco no controle WebView e use uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cf09-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="0cf09-111">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-111">Select `F12`.</span></span>  
*   <span data-ttu-id="0cf09-112">Selecione `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="0cf09-113">Abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="0cf09-114">Para obter mais informações, consulte [visão geral de devtools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="0cf09-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Depuração DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="0cf09-116">Depuração DevTools</span><span class="sxs-lookup"><span data-stu-id="0cf09-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="0cf09-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="0cf09-118">O Visual Studio fornece várias ferramentas de depuração para o código nativo e Web em aplicativos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="0cf09-119">Na seção do Visual Studio, o foco principal é a depuração de controles WebView, mas os outros métodos de depuração no Visual Studio estão disponíveis normalmente.</span><span class="sxs-lookup"><span data-stu-id="0cf09-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="0cf09-120">Use o processo a seguir para depurar o código nativo e Web somente em aplicativos Win32 ou em suplementos do Office.</span><span class="sxs-lookup"><span data-stu-id="0cf09-120">Use the following process to debug web and native code in Win32 applications or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0cf09-121">Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="0cf09-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="0cf09-122">Selecione `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar a situação.</span><span class="sxs-lookup"><span data-stu-id="0cf09-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="0cf09-123">Antes de começar, certifique-se de que os seguintes requisitos sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="0cf09-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="0cf09-124">Para depurar scripts, o aplicativo deve ser iniciado no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0cf09-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="0cf09-125">Não é possível anexar um depurador a um processo de WebView2 em execução.</span><span class="sxs-lookup"><span data-stu-id="0cf09-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="0cf09-126">Instale o Visual Studio 2019 versão 16,4 Preview 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0cf09-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="0cf09-127">Instale e configure as ferramentas do depurador de scripts no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0cf09-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="0cf09-128">Conclua as seguintes ações para instalar o componente de **diagnóstico JavaScript** no **desenvolvimento de área de trabalho com C++**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    
    1.  <span data-ttu-id="0cf09-129">Na barra do Windows Explorer, digite `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="0cf09-130">Escolha **instalador do Visual Studio** para abri-lo.</span><span class="sxs-lookup"><span data-stu-id="0cf09-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="0cf09-131">No instalador do Visual Studio, na versão instalada, escolha o botão **mais** e, em seguida, escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="0cf09-132">No Visual Studio, em **cargas**de trabalho, escolha a configuração **desenvolvimento de área de trabalho em C++** .</span><span class="sxs-lookup"><span data-stu-id="0cf09-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Tela modificando cargas de trabalho do Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="0cf09-134">Tela modificando cargas de trabalho do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="0cf09-135">Escolha **componentes individuais**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="0cf09-136">Na caixa de pesquisa, digite `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="0cf09-137">Escolha a configuração **diagnóstico de JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="0cf09-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="0cf09-138">Escolha **Modificar**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio modificando a guia componentes individuais" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="0cf09-140">Visual Studio modificando a guia componentes individuais</span><span class="sxs-lookup"><span data-stu-id="0cf09-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="0cf09-141">Habilite a depuração de script para aplicativos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="0cf09-142">No projeto do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="0cf09-143">Em **Propriedades de configuração**, escolha **depuração**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="0cf09-144">Em **tipo de depurador**, escolha **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propriedade de configuração de depuração do Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="0cf09-146">Propriedade de configuração de **depuração** do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="0cf09-147">Conclua as seguintes ações para depurar seu aplicativo WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="0cf09-148">Para definir um ponto de interrupção no código-fonte, passe o mouse à esquerda do número da linha e escolha definir um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="0cf09-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="0cf09-149">O adaptador de depuração JS/TS não executa o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="0cf09-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="0cf09-150">Você deve abrir exatamente o mesmo caminho associado à sua WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Adicionar ponto de interrupção do Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="0cf09-152">Adicionar ponto de interrupção do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0cf09-153">Para executar o depurador, escolha o tamanho do bit da plataforma e escolha o botão de reprodução verde ao lado de **depurador local do Windows**.</span><span class="sxs-lookup"><span data-stu-id="0cf09-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="0cf09-154">O aplicativo é executado e o depurador se conecta ao primeiro processo WebView2 criado.</span><span class="sxs-lookup"><span data-stu-id="0cf09-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Depurador local do Windows do Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="0cf09-156">**Depurador local do Windows** do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0cf09-157">No **console de depuração**, localize a saída do depurador.</span><span class="sxs-lookup"><span data-stu-id="0cf09-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Console de depuração do Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="0cf09-159">Console de **depuração** do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<span data-ttu-id="0cf09-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0cf09-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="0cf09-161">Use o código do Microsoft Visual Studio para depurar scripts executados em controles WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="0cf09-162">No código do Visual Studio, conclua as seguintes ações para depurar seu código.</span><span class="sxs-lookup"><span data-stu-id="0cf09-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="0cf09-163">Seu projeto precisa ter um `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="0cf09-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="0cf09-164">Se o seu projeto não tiver um `launch.json` arquivo, copie o trecho de código a seguir e crie um novo `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="0cf09-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
    
1.  <span data-ttu-id="0cf09-165">Para definir um ponto de interrupção no código-fonte, passe o mouse sobre a linha e selecione</span><span class="sxs-lookup"><span data-stu-id="0cf09-165">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="O ponto de interrupção é definido no código do Visual Studio" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="0cf09-167">O ponto de interrupção é definido no código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-167">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
    > [!NOTE]
    > <span data-ttu-id="0cf09-168">Como o código do Visual Studio não executa o mapeamento de origem, certifique-se de definir pontos de interrupção no mesmo arquivo que o WebView2 usa.</span><span class="sxs-lookup"><span data-stu-id="0cf09-168">Because Visual Studio Code does not perform source mapping, ensure you set breakpoints in the same file that WebView2 uses.</span></span>  <span data-ttu-id="0cf09-169">Se os caminhos não corresponderem, o código do Visual Studio não pausará o código em execução no ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="0cf09-169">If the paths do not match, Visual Studio Code does not pause the running code at the breakpoint.</span></span>  
    
1.  <span data-ttu-id="0cf09-170">Executar o código.</span><span class="sxs-lookup"><span data-stu-id="0cf09-170">Run the code.</span></span>  
    1.  <span data-ttu-id="0cf09-171">Na guia **executar** , escolha a configuração iniciar no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="0cf09-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="0cf09-172">Para iniciar a depuração do aplicativo, escolha Iniciar Depuração, que é o triângulo verde ao lado do menu suspenso configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="0cf09-172">To start debugging your application, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Guia executar código do Visual Studio" lightbox="./media/runvs.png":::
           <span data-ttu-id="0cf09-174">Guia executar código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="0cf09-175">Abra o **console de depuração** para exibir a saída de depuração e os erros.</span><span class="sxs-lookup"><span data-stu-id="0cf09-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Console de depuração de código do Visual Studio" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="0cf09-177">Console de depuração de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0cf09-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0cf09-178">**Configurações avançadas**:</span><span class="sxs-lookup"><span data-stu-id="0cf09-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="0cf09-179">Depuração WebView direcionada.</span><span class="sxs-lookup"><span data-stu-id="0cf09-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="0cf09-180">Em alguns aplicativos do WebView2, você pode usar mais de um controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-180">In some WebView2 applications, you may use more than one WebView2 control.</span></span> <span data-ttu-id="0cf09-181">Para escolher o controle WebView2 para depurar nesta situação, você pode usar a depuração de WebView2 direcionada</span><span class="sxs-lookup"><span data-stu-id="0cf09-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="0cf09-182">Abra `launch.json` e conclua as seguintes ações para usar a depuração WebView direcionada.</span><span class="sxs-lookup"><span data-stu-id="0cf09-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="0cf09-183">Confirme se o `useWebview` parâmetro está definido como `true` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="0cf09-184">Adicione o `urlFilter` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0cf09-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="0cf09-185">Quando o controle WebView2 navega para uma URL, o `urlFilter` valor do parâmetro é usado para comparar cadeias de caracteres que aparecem na URL.</span><span class="sxs-lookup"><span data-stu-id="0cf09-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="0cf09-186">Ao depurar seu aplicativo, talvez você precise percorrer o código do início do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="0cf09-186">When debugging your application, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="0cf09-187">Se você estiver renderizando páginas da Web em sites e não tiver acesso ao código-fonte, poderá usar a `?=value`  opção porque as páginas da Web ignoram parâmetros não reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="0cf09-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="0cf09-188">Depois que a primeira correspondência for encontrada na URL, o depurador será interrompido.</span><span class="sxs-lookup"><span data-stu-id="0cf09-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="0cf09-189">Você não pode depurar dois controles WebView2 ao mesmo tempo porque a porta CDP é compartilhada por todos os controles WebView2 e usa um número de porta único.</span><span class="sxs-lookup"><span data-stu-id="0cf09-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="0cf09-190">Depurar processos em execução</span><span class="sxs-lookup"><span data-stu-id="0cf09-190">Debug running processes</span></span>  
    
    <span data-ttu-id="0cf09-191">Talvez seja necessário anexar o depurador para executar os processos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="0cf09-192">Para fazer isso, `launch.json` atualize o `request` parâmetro para `attach` .</span><span class="sxs-lookup"><span data-stu-id="0cf09-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="0cf09-193">O controle WebView2 deve abrir a porta CDP para permitir a depuração do controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="0cf09-194">Seu código deve ser criado para garantir que apenas um controle WebView2 tenha uma porta CDP (protocolo de desenvolvedor Chrome) aberta antes de iniciar o depurador.</span><span class="sxs-lookup"><span data-stu-id="0cf09-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="0cf09-195">Opções de rastreamento de depuração</span><span class="sxs-lookup"><span data-stu-id="0cf09-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="0cf09-196">Adicione o `trace` parâmetro a launch.jspara habilitar o rastreamento de depuração.</span><span class="sxs-lookup"><span data-stu-id="0cf09-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="0cf09-197">Adicionar `trace` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0cf09-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Salvar a saída de depuração em um arquivo de log." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="0cf09-199">Salvar a saída de depuração em um arquivo de log</span><span class="sxs-lookup"><span data-stu-id="0cf09-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Saída detalhada" lightbox="./media/verbose.png":::
                 <span data-ttu-id="0cf09-201">Saída de depuração de código do Visual Studio com o rastreamento detalhado ativado</span><span class="sxs-lookup"><span data-stu-id="0cf09-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="0cf09-202">Depurar suplementos do Office.</span><span class="sxs-lookup"><span data-stu-id="0cf09-202">Debug Office Add-ins.</span></span>
    
    <span data-ttu-id="0cf09-203">Se você estiver Depurando suplementos do Office, abra o código-fonte do suplemento em uma instância separada do código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0cf09-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="0cf09-204">Abra o launch.jsem seu aplicativo do WebView2 e adicione o trecho de código a seguir para anexar o depurador ao suplemento do Office.</span><span class="sxs-lookup"><span data-stu-id="0cf09-204">Open launch.json in your WebView2 application and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="0cf09-205">Solucionando problemas com o depurador</span><span class="sxs-lookup"><span data-stu-id="0cf09-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="0cf09-206">Você pode encontrar os seguintes cenários ao usar o depurador.</span><span class="sxs-lookup"><span data-stu-id="0cf09-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="0cf09-207">O depurador não pára no ponto de interrupção, e você tem saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="0cf09-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="0cf09-208">Para resolver o problema, confirme se o arquivo com o ponto de interrupção é o mesmo arquivo que é usado pelo controle WebView2.</span><span class="sxs-lookup"><span data-stu-id="0cf09-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="0cf09-209">O depurador não executa o mapeamento de caminho de origem.</span><span class="sxs-lookup"><span data-stu-id="0cf09-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="0cf09-210">Você não pode anexar a um processo em execução e Obtém um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="0cf09-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="0cf09-211">Para solucionar o problema, confirme se o controle WebView2 abriu a porta CDP.</span><span class="sxs-lookup"><span data-stu-id="0cf09-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="0cf09-212">Verifique se o  `additionalBrowserArguments`  valor no registro está correto ou as opções estão corretas.</span><span class="sxs-lookup"><span data-stu-id="0cf09-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="0cf09-213">Para obter mais informações, consulte [additionalBrowserArguments para dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] e [additionalBrowserArguments para Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="0cf09-213">For more information, see [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  

## <span data-ttu-id="0cf09-214">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0cf09-214">See also</span></span>  

*   <span data-ttu-id="0cf09-215">Para começar a usar o WebView2, confira [WebView2 guias de introdução][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="0cf09-215">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="0cf09-216">Para obter um exemplo abrangente de recursos do WebView2, consulte o repositório do [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.</span><span class="sxs-lookup"><span data-stu-id="0cf09-216">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="0cf09-217">Para obter informações mais detalhadas sobre APIs do WebView2, consulte [referência de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="0cf09-217">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="0cf09-218">Para obter mais informações sobre o WebView2, consulte [recursos do WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="0cf09-218">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <span data-ttu-id="0cf09-219">Entrar em contato com a equipe do Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="0cf09-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriedade CoreWebView2EnvironmentOptions. AdditionalBrowserArguments (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-globais | Documentos da Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
