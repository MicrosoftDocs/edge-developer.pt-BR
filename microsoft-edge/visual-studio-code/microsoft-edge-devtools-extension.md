---
description: Como usar os elementos do Microsoft Edge (Chromium) a partir do código do Visual Studio
title: Elementos para Microsoft Edge (Chromium) do código do Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, elementos
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135472"
---
# <span data-ttu-id="c76f2-104">Extensão de código do Microsoft Edge DevTools para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c76f2-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="c76f2-105">Usar</span><span class="sxs-lookup"><span data-stu-id="c76f2-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="c76f2-106">Esta extensão para acessar o Microsoft Edge DevTools dentro do [código do Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="c76f2-106">this extension to access in Microsoft Edge DevTools inside [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="c76f2-107">Você tem acesso aos **elementos** e às ferramentas de **rede** no Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="c76f2-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="c76f2-108">Você pode iniciar ou anexar uma instância do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c76f2-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="c76f2-109">Depois de se conectar, você pode exibir a estrutura HTML do tempo de execução, alterar o layout, corrigir os problemas de estilo e inspecionar o tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="c76f2-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <span data-ttu-id="c76f2-110">Ferramenta elementos</span><span class="sxs-lookup"><span data-stu-id="c76f2-110">Elements tool</span></span>  

<span data-ttu-id="c76f2-111">Por padrão, a extensão inicia uma instância de navegador em uma janela exclusiva e oferece a funcionalidade de **elementos** do Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="c76f2-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="c76f2-113">Microsoft Edge DevTools para o código do Visual Studio em execução com uma janela de navegador completa</span><span class="sxs-lookup"><span data-stu-id="c76f2-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="c76f2-114">Nas configurações de extensão, você pode habilitar mais funcionalidade, como **modo sem periféricos** e **rede**.</span><span class="sxs-lookup"><span data-stu-id="c76f2-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Ativar (ou desativar) o modo sem periféricos e a inspeção de rede nas configurações de extensão" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="c76f2-116">Habilitando \ (ou desativando \) o modo sem periféricos e a inspeção de rede nas configurações de extensão</span><span class="sxs-lookup"><span data-stu-id="c76f2-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <span data-ttu-id="c76f2-117">Modo sem periféricos</span><span class="sxs-lookup"><span data-stu-id="c76f2-117">Headless Mode</span></span>  

<span data-ttu-id="c76f2-118">No modo sem periféricos, essa extensão não inicia uma instância completa do navegador para depurar.</span><span class="sxs-lookup"><span data-stu-id="c76f2-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="c76f2-119">Ele executa uma instância em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c76f2-119">It runs an instance in the background.</span></span>  <span data-ttu-id="c76f2-120">Talvez você precise ficar dentro do editor e interagir com o navegador integrado.</span><span class="sxs-lookup"><span data-stu-id="c76f2-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="c76f2-121">Um ícone adicional do navegador não é exibido na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c76f2-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools para o código do Visual Studio em execução com uma sem periféricos" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="c76f2-123">Microsoft Edge DevTools para o código do Visual Studio em execução com um navegador sem periféricos</span><span class="sxs-lookup"><span data-stu-id="c76f2-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c76f2-124">No macOS, você deve ativar o modo sem periféricos como modo preferencial.</span><span class="sxs-lookup"><span data-stu-id="c76f2-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="c76f2-125">Usar o modo sem periféricos deve resolver um problema em que, se a janela não estiver visível, a janela do navegador informa que é `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="c76f2-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <span data-ttu-id="c76f2-126">Ferramenta de rede</span><span class="sxs-lookup"><span data-stu-id="c76f2-126">Network tool</span></span>  

<span data-ttu-id="c76f2-127">Se você também quiser inspecionar o tráfego de rede do seu aplicativo, abra as configurações e ative a guia **rede** .</span><span class="sxs-lookup"><span data-stu-id="c76f2-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspeção de rede no Microsoft Edge DevTools para código do Visual Studio" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="c76f2-129">Inspeção de rede no Microsoft Edge DevTools para código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c76f2-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <span data-ttu-id="c76f2-130">Iniciando o Microsoft Edge da extensão</span><span class="sxs-lookup"><span data-stu-id="c76f2-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="c76f2-131">Navegue até ferramentas do Microsoft Edge na **barra de atividades**.</span><span class="sxs-lookup"><span data-stu-id="c76f2-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="c76f2-132">Ao lado de onde diz as **Ferramentas do Microsoft Edge: destinos,** há um sinal de adição que abre o navegador do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c76f2-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="c76f2-133">Se você escolher a opção **about: Blank** , navegue até o seu aplicativo Web no navegador para que ele apareça no painel **elementos** do código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c76f2-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <span data-ttu-id="c76f2-134">Iniciando o Microsoft Edge a partir do modo de exibição de depuração</span><span class="sxs-lookup"><span data-stu-id="c76f2-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="c76f2-135">Se você estiver acostumado a usar o modo de exibição de depuração no código do Visual Studio, acesse o Microsoft Edge DevTools dele.</span><span class="sxs-lookup"><span data-stu-id="c76f2-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="c76f2-136">No código do Visual Studio, navegue até o modo de exibição de depuração</span><span class="sxs-lookup"><span data-stu-id="c76f2-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="c76f2-137">Selecione `Ctrl` + `Shift` + `D` no Windows/Linux \ ( `Command` + `Shift` + `D` no MacOS \).</span><span class="sxs-lookup"><span data-stu-id="c76f2-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="c76f2-138">Se você não tiver nenhuma configuração no código do Visual Studio, execute uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="c76f2-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="c76f2-139">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="c76f2-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="c76f2-140">Escolha o botão **reproduzir** \ (verde \).</span><span class="sxs-lookup"><span data-stu-id="c76f2-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="c76f2-141">Na lista suspensa, escolha **borda** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="c76f2-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="c76f2-142">`launch.json`Deve ser exibido um arquivo que contenha a configuração a seguir.</span><span class="sxs-lookup"><span data-stu-id="c76f2-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
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
> <span data-ttu-id="c76f2-143">Depois de carregar a configuração correta, conclua a ação a seguir.</span><span class="sxs-lookup"><span data-stu-id="c76f2-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="c76f2-144">Para iniciar a ferramenta **elementos** a partir do código do Visual Studio, conclua uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c76f2-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="c76f2-145">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="c76f2-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="c76f2-146">Escolha o botão **reproduzir** \ (verde \).</span><span class="sxs-lookup"><span data-stu-id="c76f2-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="c76f2-147">Agora, você pode executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="c76f2-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="c76f2-148">Acesse o screencast do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="c76f2-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="c76f2-149">Inspecione o DOM e o estilo dos componentes na página.</span><span class="sxs-lookup"><span data-stu-id="c76f2-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <span data-ttu-id="c76f2-150">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c76f2-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="c76f2-151">Para abrir um navegador e anexar a instância ao código do Visual Studio, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c76f2-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="c76f2-152">Para abrir uma instância do Microsoft Edge \ (Chromium \), copie e execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="c76f2-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="c76f2-153">Depois que a instância iniciar, copie e cole o trecho de código a seguir no seu `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="c76f2-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
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
    
1.  <span data-ttu-id="c76f2-154">No código do Visual Studio, abra o menu suspenso **depurador** e escolha **anexar ao Microsoft Edge e abra as ferramentas de desenvolvedor**.</span><span class="sxs-lookup"><span data-stu-id="c76f2-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="c76f2-155">Para iniciar a ferramenta **elementos** a partir do código do Visual Studio, conclua uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="c76f2-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="c76f2-156">Selecione `F5` .</span><span class="sxs-lookup"><span data-stu-id="c76f2-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="c76f2-157">Escolha o botão **reproduzir** \ (verde \).</span><span class="sxs-lookup"><span data-stu-id="c76f2-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="c76f2-158">Agora, você pode executar as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="c76f2-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="c76f2-159">Acesse o screencast do seu navegador.</span><span class="sxs-lookup"><span data-stu-id="c76f2-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="c76f2-160">Inspecione o DOM e o estilo dos componentes na página.</span><span class="sxs-lookup"><span data-stu-id="c76f2-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <span data-ttu-id="c76f2-161">Entrar em contato com o Microsoft Edge DevTools para a equipe de extensão de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c76f2-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="c76f2-162">Envie seus comentários por meio do [arquivamento de um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] no [repositório GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="c76f2-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="c76f2-163">Se você quiser ajudar a fazer</span><span class="sxs-lookup"><span data-stu-id="c76f2-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="c76f2-164">Esta extensão melhor, suas contribuições são bem-vindos.</span><span class="sxs-lookup"><span data-stu-id="c76f2-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="c76f2-165">Encontre tudo o que você precisa para começar a usar o [repositório do GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="c76f2-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo problema-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Ferramentas do Microsoft Edge para código VS"  
