---
description: Como usar Elementos para Microsoft Edge (Chromium) de Visual Studio Code
title: Elementos para Microsoft Edge (Chromium) de Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398452"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="51fce-104">Microsoft Edge DevTools para Visual Studio Code extensão</span><span class="sxs-lookup"><span data-stu-id="51fce-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="51fce-105">Usar</span><span class="sxs-lookup"><span data-stu-id="51fce-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="51fce-106">esta extensão para acessar no Microsoft Edge DevTools [dentro Microsoft Visual Studio Código][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="51fce-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="51fce-107">Você tem acesso às ferramentas **Elementos** e **Rede** no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="51fce-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="51fce-108">Você pode iniciar ou anexar a uma instância de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="51fce-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="51fce-109">Depois de se conectar, você pode exibir a estrutura HTML do tempo de execução, alterar o layout, corrigir problemas de estilo e inspecionar o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="51fce-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="51fce-110">Ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="51fce-110">Elements tool</span></span>  

<span data-ttu-id="51fce-111">Por padrão, a extensão inicia uma instância do navegador em uma janela exclusiva e fornece a funcionalidade **Elements** do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="51fce-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools para Visual Studio Code em execução com uma janela completa do navegador" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="51fce-113">Microsoft Edge DevTools para Visual Studio Code em execução com uma janela completa do navegador</span><span class="sxs-lookup"><span data-stu-id="51fce-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="51fce-114">Nas configurações de extensão, você pode habilitar mais funcionalidades como **Modo Sem Cabeça** e **Rede.**</span><span class="sxs-lookup"><span data-stu-id="51fce-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Habilitando (ou desabilitando) o modo sem cabeça e a inspeção de rede nas configurações de extensão" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="51fce-116">Habilitando \(ou desabilitando\) modo sem cabeça e inspeção de rede nas configurações de extensão</span><span class="sxs-lookup"><span data-stu-id="51fce-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="51fce-117">Modo Sem Cabeça</span><span class="sxs-lookup"><span data-stu-id="51fce-117">Headless Mode</span></span>  

<span data-ttu-id="51fce-118">No modo sem cabeça, essa extensão não inicia uma instância completa do navegador para depurar.</span><span class="sxs-lookup"><span data-stu-id="51fce-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="51fce-119">Ele executa uma instância em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="51fce-119">It runs an instance in the background.</span></span>  <span data-ttu-id="51fce-120">Talvez seja preciso ficar dentro do editor e interagir com o navegador incorporado.</span><span class="sxs-lookup"><span data-stu-id="51fce-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="51fce-121">Um ícone extra do navegador não será exibido na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="51fce-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para Visual Studio Code executando com um sem cabeça" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="51fce-123">Microsoft Edge DevTools para Visual Studio Code em execução com um navegador sem cabeça</span><span class="sxs-lookup"><span data-stu-id="51fce-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="51fce-124">No macOS, você deve ativar o modo sem cabeça como seu modo preferencial.</span><span class="sxs-lookup"><span data-stu-id="51fce-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="51fce-125">O uso do modo sem cabeça deve resolver um problema em que, se a janela não estiver visível, a janela do navegador relata que ela é `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="51fce-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="51fce-126">Ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="51fce-126">Network tool</span></span>  

<span data-ttu-id="51fce-127">Se você também quiser inspecionar o tráfego de rede do seu aplicativo, abra as configurações e acione a **guia** Rede.</span><span class="sxs-lookup"><span data-stu-id="51fce-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspeção de rede Microsoft Edge DevTools para Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="51fce-129">Inspeção de rede Microsoft Edge DevTools para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="51fce-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="51fce-130">Iniciando Microsoft Edge da extensão</span><span class="sxs-lookup"><span data-stu-id="51fce-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="51fce-131">Navegue até Microsoft Edge Ferramentas na Barra **de Atividades**.</span><span class="sxs-lookup"><span data-stu-id="51fce-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="51fce-132">Ao lado de onde ele **Microsoft Edge Ferramentas: Destinos,** há um sinal de aplicação que abre o navegador para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51fce-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="51fce-133">Se você escolher a **opção about:blank,** deverá navegar até seu aplicativo Web no navegador para que ele apareça no painel **Elementos** no Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="51fce-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="51fce-134">Iniciando Microsoft Edge do exibição Depurar</span><span class="sxs-lookup"><span data-stu-id="51fce-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="51fce-135">Se você estiver acostumado a usar o exibição Depurar no Visual Studio Code, acesse Microsoft Edge DevTools a partir dele.</span><span class="sxs-lookup"><span data-stu-id="51fce-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="51fce-136">Em Visual Studio Code, navegue até o exibição Depurar</span><span class="sxs-lookup"><span data-stu-id="51fce-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="51fce-137">Selecione `Ctrl` + `Shift` + `D` em Windows/Linux \( `Command` + `Shift` + `D` no macOS\).</span><span class="sxs-lookup"><span data-stu-id="51fce-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="51fce-138">Se você não tiver configurações no Visual Studio Code, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="51fce-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="51fce-139">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="51fce-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="51fce-140">Escolha o **botão Reproduzir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="51fce-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="51fce-141">No menu suspenso, escolha **Borda** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="51fce-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="51fce-142">Um `launch.json` arquivo deve ser exibido que contém a seguinte configuração.</span><span class="sxs-lookup"><span data-stu-id="51fce-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> <span data-ttu-id="51fce-143">Depois de carregar a configuração correta, conclua a ação a seguir.</span><span class="sxs-lookup"><span data-stu-id="51fce-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="51fce-144">Para iniciar a **ferramenta Elements** Visual Studio Code, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="51fce-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="51fce-145">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="51fce-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="51fce-146">Escolha o **botão Reproduzir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="51fce-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="51fce-147">Agora, você pode fazer as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="51fce-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="51fce-148">Acesse uma screencast do navegador.</span><span class="sxs-lookup"><span data-stu-id="51fce-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="51fce-149">Inspecione o DOM e o estilo dos componentes em sua página.</span><span class="sxs-lookup"><span data-stu-id="51fce-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="51fce-150">Anexando a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="51fce-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="51fce-151">Para abrir um navegador e anexar a instância Visual Studio Code, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="51fce-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="51fce-152">Para abrir uma instância de Microsoft Edge \(Chromium\), copie e execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="51fce-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="51fce-153">Depois que a instância é lançada, copie e colar o seguinte trecho de código em seu `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="51fce-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  <span data-ttu-id="51fce-154">Em Visual Studio Code, abra o menu suspenso **Depurador** e escolha Anexar ao Microsoft Edge **e abra as ferramentas de desenvolvedor.**</span><span class="sxs-lookup"><span data-stu-id="51fce-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="51fce-155">Para iniciar a **ferramenta Elements** Visual Studio Code, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="51fce-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="51fce-156">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="51fce-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="51fce-157">Escolha o **botão Reproduzir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="51fce-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="51fce-158">Agora, você pode fazer as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="51fce-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="51fce-159">Acesse uma screencast do navegador.</span><span class="sxs-lookup"><span data-stu-id="51fce-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="51fce-160">Inspecione o DOM e o estilo dos componentes em sua página.</span><span class="sxs-lookup"><span data-stu-id="51fce-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="51fce-161">Entrar em contato com o Microsoft Edge DevTools para Visual Studio Code de extensão</span><span class="sxs-lookup"><span data-stu-id="51fce-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="51fce-162">Envie seus comentários [arquivando um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] GitHub [o repo][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="51fce-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="51fce-163">Se você quiser ajudar a fazer</span><span class="sxs-lookup"><span data-stu-id="51fce-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="51fce-164">essa extensão é melhor, suas contribuições são bem-vindas.</span><span class="sxs-lookup"><span data-stu-id="51fce-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="51fce-165">Encontre tudo o que você precisa para começar no GitHub [do repo][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="51fce-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo Problema - microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Ferramentas para Visual Studio Code"  
