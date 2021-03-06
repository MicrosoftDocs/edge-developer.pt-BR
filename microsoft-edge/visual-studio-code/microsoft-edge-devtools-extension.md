---
description: Como usar elementos para o Microsoft Edge (Chromium) Visual Studio Code
title: Elementos do Microsoft Edge (Chromium) do Visual Studio Code
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
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="e307b-104">Microsoft Edge DevTools para Visual Studio de código</span><span class="sxs-lookup"><span data-stu-id="e307b-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="e307b-105">Usar</span><span class="sxs-lookup"><span data-stu-id="e307b-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="e307b-106">essa extensão para acessar no Microsoft Edge DevTools dentro [do Microsoft Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="e307b-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="e307b-107">Você tem acesso às ferramentas **Elementos** e **Rede** no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e307b-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="e307b-108">Você pode iniciar ou anexar a uma instância do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e307b-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="e307b-109">Depois de se conectar, você pode exibir a estrutura HTML do tempo de execução, alterar o layout, corrigir problemas de estilo e inspecionar o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="e307b-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="e307b-110">Ferramenta Elements</span><span class="sxs-lookup"><span data-stu-id="e307b-110">Elements tool</span></span>  

<span data-ttu-id="e307b-111">Por padrão, a extensão inicia uma instância do navegador em uma janela exclusiva e fornece a funcionalidade **Elements** do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e307b-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools for Visual Studio Code em execução com uma janela completa do navegador" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="e307b-113">Microsoft Edge DevTools for Visual Studio Code em execução com uma janela completa do navegador</span><span class="sxs-lookup"><span data-stu-id="e307b-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="e307b-114">Nas configurações de extensão, você pode habilitar mais funcionalidades como **Modo Sem Cabeça** e **Rede.**</span><span class="sxs-lookup"><span data-stu-id="e307b-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Habilitando (ou desabilitando) o modo sem cabeça e a inspeção de rede nas configurações de extensão" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="e307b-116">Habilitando \(ou desabilitando\) modo sem cabeça e inspeção de rede nas configurações de extensão</span><span class="sxs-lookup"><span data-stu-id="e307b-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="e307b-117">Modo Sem Cabeça</span><span class="sxs-lookup"><span data-stu-id="e307b-117">Headless Mode</span></span>  

<span data-ttu-id="e307b-118">No modo sem cabeça, essa extensão não inicia uma instância completa do navegador para depurar.</span><span class="sxs-lookup"><span data-stu-id="e307b-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="e307b-119">Ele executa uma instância em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e307b-119">It runs an instance in the background.</span></span>  <span data-ttu-id="e307b-120">Talvez seja preciso ficar dentro do editor e interagir com o navegador incorporado.</span><span class="sxs-lookup"><span data-stu-id="e307b-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="e307b-121">Um ícone extra do navegador não será exibido na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e307b-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools for Visual Studio Code em execução com um sem cabeça" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="e307b-123">Microsoft Edge DevTools for Visual Studio Code em execução com um navegador sem cabeça</span><span class="sxs-lookup"><span data-stu-id="e307b-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e307b-124">No macOS, você deve ativar o modo sem cabeça como seu modo preferencial.</span><span class="sxs-lookup"><span data-stu-id="e307b-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="e307b-125">O uso do modo sem cabeça deve resolver um problema em que, se a janela não estiver visível, a janela do navegador relata que ela é `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="e307b-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="e307b-126">Ferramenta Rede</span><span class="sxs-lookup"><span data-stu-id="e307b-126">Network tool</span></span>  

<span data-ttu-id="e307b-127">Se você também quiser inspecionar o tráfego de rede do seu aplicativo, abra as configurações e acione a **guia** Rede.</span><span class="sxs-lookup"><span data-stu-id="e307b-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspeção de rede no Microsoft Edge DevTools para Visual Studio Código" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="e307b-129">Inspeção de rede no Microsoft Edge DevTools para Visual Studio Código</span><span class="sxs-lookup"><span data-stu-id="e307b-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="e307b-130">Iniciando o Microsoft Edge na extensão</span><span class="sxs-lookup"><span data-stu-id="e307b-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="e307b-131">Navegue até Ferramentas do Microsoft Edge na **Barra de Atividades.**</span><span class="sxs-lookup"><span data-stu-id="e307b-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="e307b-132">Ao lado de onde ele diz **Microsoft Edge Tools: Targets,** há um sinal de a mais que abre o navegador para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e307b-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="e307b-133">Se você escolher a **opção about:blank,** deverá navegar até seu aplicativo Web no navegador para que ele apareça no painel **Elementos** em Visual Studio Código.</span><span class="sxs-lookup"><span data-stu-id="e307b-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="e307b-134">Iniciando o Microsoft Edge no ponto de exibição Depuração</span><span class="sxs-lookup"><span data-stu-id="e307b-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="e307b-135">Se você estiver acostumado a usar o exibição Depurar no código Visual Studio, acesse o Microsoft Edge DevTools a partir dele.</span><span class="sxs-lookup"><span data-stu-id="e307b-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="e307b-136">Em Visual Studio Código, navegue até o exibição Depurar</span><span class="sxs-lookup"><span data-stu-id="e307b-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="e307b-137">Selecione `Ctrl` + `Shift` + `D` no Windows/Linux \( `Command` + `Shift` + `D` no macOS\).</span><span class="sxs-lookup"><span data-stu-id="e307b-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="e307b-138">Se você não tiver configurações no Visual Studio Code, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="e307b-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="e307b-139">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e307b-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="e307b-140">Escolha o **botão Reproduzir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="e307b-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="e307b-141">No menu suspenso, escolha **Borda** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="e307b-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="e307b-142">Um `launch.json` arquivo deve ser exibido que contém a seguinte configuração.</span><span class="sxs-lookup"><span data-stu-id="e307b-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
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
> <span data-ttu-id="e307b-143">Depois de carregar a configuração correta, conclua a ação a seguir.</span><span class="sxs-lookup"><span data-stu-id="e307b-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="e307b-144">Para iniciar a **ferramenta Elementos** Visual Studio Código, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="e307b-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="e307b-145">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e307b-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="e307b-146">Escolha o **botão Reproduzir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="e307b-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="e307b-147">Agora, você pode fazer as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="e307b-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="e307b-148">Acesse uma screencast do navegador.</span><span class="sxs-lookup"><span data-stu-id="e307b-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="e307b-149">Inspecione o DOM e o estilo dos componentes em sua página.</span><span class="sxs-lookup"><span data-stu-id="e307b-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="e307b-150">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e307b-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="e307b-151">Para abrir um navegador e anexar a instância Visual Studio Código, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e307b-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="e307b-152">Para abrir uma instância do Microsoft Edge \(Chromium\), copie e execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="e307b-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="e307b-153">Depois que a instância é lançada, copie e colar o seguinte trecho de código em seu `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="e307b-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
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
    
1.  <span data-ttu-id="e307b-154">Em Visual Studio Código, abra o menu suspenso **Depurador** e escolha Anexar ao **Microsoft Edge e abra as ferramentas de desenvolvedor.**</span><span class="sxs-lookup"><span data-stu-id="e307b-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="e307b-155">Para iniciar a **ferramenta Elementos** Visual Studio Código, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="e307b-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="e307b-156">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="e307b-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="e307b-157">Escolha o **botão Reproduzir** \(verde\).</span><span class="sxs-lookup"><span data-stu-id="e307b-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="e307b-158">Agora, você pode fazer as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="e307b-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="e307b-159">Acesse uma screencast do navegador.</span><span class="sxs-lookup"><span data-stu-id="e307b-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="e307b-160">Inspecione o DOM e o estilo dos componentes em sua página.</span><span class="sxs-lookup"><span data-stu-id="e307b-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="e307b-161">Entrar em contato com a equipe de extensão do Microsoft Edge DevTools Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e307b-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="e307b-162">Envie seus comentários [arquivando um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] no [repositório do GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="e307b-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="e307b-163">Se você quiser ajudar a fazer</span><span class="sxs-lookup"><span data-stu-id="e307b-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="e307b-164">essa extensão é melhor, suas contribuições são bem-vindas.</span><span class="sxs-lookup"><span data-stu-id="e307b-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="e307b-165">Encontre tudo o que você precisa para começar no [repositório do GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="e307b-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Código"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Código"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo Problema - microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code"  
