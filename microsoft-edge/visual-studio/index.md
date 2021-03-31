---
description: Microsoft Edge (Chromium) e Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs, visual studio, depurador
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387271"
---
# <a name="visual-studio"></a><span data-ttu-id="67ef8-104">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-104">Visual Studio</span></span>  

<span data-ttu-id="67ef8-105">O Microsoft [Visual Studio][MicrosoftVisualstudioVs] é um ambiente de desenvolvimento integrado \(IDE\).</span><span class="sxs-lookup"><span data-stu-id="67ef8-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] is an integrated development environment \(IDE\).</span></span>   <span data-ttu-id="67ef8-106">Use-o para editar, depurar, criar e publicar seus aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="67ef8-106">Use it to edit, debug, build, and publish your web apps.</span></span>  <span data-ttu-id="67ef8-107">É um programa rico em recursos que pode ser usado para muitos aspectos do desenvolvimento da Web.</span><span class="sxs-lookup"><span data-stu-id="67ef8-107">It is a feature-rich program that may be used for many aspects of your web development.</span></span>  <span data-ttu-id="67ef8-108">Além do editor padrão e do depurador que a maioria das IDEs fornece, Visual Studio inclui os seguintes recursos para facilitar seu processo de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="67ef8-108">Over and above the standard editor and debugger that most IDEs provide, Visual Studio includes the following features to ease your development process.</span></span>  

*   <span data-ttu-id="67ef8-109">compiladores</span><span class="sxs-lookup"><span data-stu-id="67ef8-109">compilers</span></span>  
*   <span data-ttu-id="67ef8-110">ferramentas de conclusão de código</span><span class="sxs-lookup"><span data-stu-id="67ef8-110">code completion tools</span></span>  
*   <span data-ttu-id="67ef8-111">designers gráficos</span><span class="sxs-lookup"><span data-stu-id="67ef8-111">graphical designers</span></span>  
*   <span data-ttu-id="67ef8-112">muitos mais</span><span class="sxs-lookup"><span data-stu-id="67ef8-112">many more</span></span>  
    
<span data-ttu-id="67ef8-113">Se você ainda não estiver usando Visual Studio, navegue até [Baixar][MicrosoftVisualstudioDownloads] Visual Studio para baixá-lo.</span><span class="sxs-lookup"><span data-stu-id="67ef8-113">If you are not already using Visual Studio, navigate to [Download Visual Studio][MicrosoftVisualstudioDownloads] to download it.</span></span>  

<span data-ttu-id="67ef8-114">Atualmente, o Visual Studio 2019 oferece suporte à depuração do JavaScript no Microsoft Edge para o ASP.NET Framework e ASP.NET Principais aplicativos.</span><span class="sxs-lookup"><span data-stu-id="67ef8-114">Currently, Visual Studio 2019 supports debugging JavaScript in Microsoft Edge for your ASP.NET Framework and ASP.NET Core apps.</span></span>  <span data-ttu-id="67ef8-115">Conclua as etapas a seguir para usar Visual Studio para depurar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67ef8-115">Complete the following steps to use Visual Studio to debug Microsoft Edge.</span></span>  

## <a name="launch-microsoft-edge"></a><span data-ttu-id="67ef8-116">Iniciar o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67ef8-116">Launch Microsoft Edge</span></span>  

<span data-ttu-id="67ef8-117">Visual Studio o fluxo de trabalho a seguir usando um único botão.</span><span class="sxs-lookup"><span data-stu-id="67ef8-117">Visual Studio completes the following workflow using a single button.</span></span>  

1.  <span data-ttu-id="67ef8-118">Cria seu aplicativo ASP.NET e ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="67ef8-118">Builds your ASP.NET and ASP.NET Core app.</span></span>  
1.  <span data-ttu-id="67ef8-119">Inicia seu servidor Web.</span><span class="sxs-lookup"><span data-stu-id="67ef8-119">Starts your web server.</span></span>  
1.  <span data-ttu-id="67ef8-120">Inicia o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67ef8-120">Launches Microsoft Edge.</span></span>  
1.  <span data-ttu-id="67ef8-121">Conecta o Visual Studio depurador.</span><span class="sxs-lookup"><span data-stu-id="67ef8-121">Connects the Visual Studio debugger.</span></span>  
    
<span data-ttu-id="67ef8-122">O fluxo de trabalho simplificado permite depurar JavaScript executado no Microsoft Edge diretamente do seu IDE.</span><span class="sxs-lookup"><span data-stu-id="67ef8-122">The simplified workflow allows you to debug JavaScript that run in Microsoft Edge directly from your IDE.</span></span>  

### <a name="create-a-new-aspnet-core-web-app"></a><span data-ttu-id="67ef8-123">Criar um novo ASP.NET Web Core</span><span class="sxs-lookup"><span data-stu-id="67ef8-123">Create a new ASP.NET Core web app</span></span>  

<span data-ttu-id="67ef8-124">Abra Visual Studio 2019 e escolha **Criar um novo projeto.**</span><span class="sxs-lookup"><span data-stu-id="67ef8-124">Open Visual Studio 2019 and choose **Create a new project**.</span></span>  <span data-ttu-id="67ef8-125">Na próxima tela, escolha ASP.NET **Aplicativo Web Principal**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-125">On the next screen, choose **ASP.NET Core Web app** > **Next**.</span></span>  

:::image type="complex" source="./media/create-new-project.png" alt-text="Criar um novo ASP.NET Core Web" lightbox="./media/create-new-project.png":::
   <span data-ttu-id="67ef8-127">Criar um novo ASP.NET Core Web</span><span class="sxs-lookup"><span data-stu-id="67ef8-127">Create a new ASP.NET Core Web app</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-128">Forneça um **nome de projeto** para seu novo projeto e escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-128">Provide a **Project name** for your new project and choose **Create**.</span></span>  <span data-ttu-id="67ef8-129">Para os fins do exemplo,  escolha React.jscomo o modelo e escolha **Criar**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-129">For the purposes of the example, choose **React.js** as the template, and choose **Create**.</span></span>  <span data-ttu-id="67ef8-130">O **React.js** especifica como integrar o React.js com um ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="67ef8-130">The **React.js** template specifies how to integrate React.js with an ASP.NET Core app.</span></span>  

### <a name="launch-microsoft-edge-from-visual-studio"></a><span data-ttu-id="67ef8-131">Iniciar o Microsoft Edge do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-131">Launch Microsoft Edge from Visual Studio</span></span>  

<span data-ttu-id="67ef8-132">Depois de criar seu projeto, abra `ClientApp/src/components/Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="67ef8-132">After you create your project, open `ClientApp/src/components/Counter.js`.</span></span>  <span data-ttu-id="67ef8-133">Agora, para usar Visual Studio para depurar JavaScript, escolha a lista suspenso ao lado do botão **verde Reproduzir** e **do IIS Express**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-133">Now, to use Visual Studio to debug JavaScript, choose the dropdown next to the green **Play** button and **IIS Express**.</span></span>  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="O menu suspenso ao lado do botão verde Reproduzir e do IIS Express" lightbox="./media/vs-dropdown.png":::
   <span data-ttu-id="67ef8-135">O menu suspenso ao lado do botão **verde Reproduzir** e **do IIS Express**</span><span class="sxs-lookup"><span data-stu-id="67ef8-135">The dropdown next to the green **Play** button and **IIS Express**</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-136">Escolha **Depuração de Script**  >  **Habilitada**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-136">Choose **Script Debugging** > **Enabled**.</span></span>  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Ativar a depuração de scripts Visual Studio" lightbox="./media/enable-script-debugging.png":::
   <span data-ttu-id="67ef8-138">Ativar a depuração de scripts Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-138">Turn on script debugging in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-139">Na mesma lista suspenso, escolha Navegador da **Web** > o canal de visualização do Microsoft Edge que você deseja Visual Studio iniciar, como o Microsoft Edge Canary, Dev ou Beta.</span><span class="sxs-lookup"><span data-stu-id="67ef8-139">In the same dropdown, choose **Web Browser** > the preview channel of Microsoft Edge that you want Visual Studio to launch, such as Microsoft Edge Canary, Dev, or Beta.</span></span>  <span data-ttu-id="67ef8-140">Se você ainda não estiver usando um dos canais de visualização do Microsoft Edge, navegue até [Baixar canais do Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para baixar um.</span><span class="sxs-lookup"><span data-stu-id="67ef8-140">If you are not already using one of the Microsoft Edge preview channels, navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] to download one.</span></span>  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Escolha o canal de visualização do Microsoft Edge que você Visual Studio iniciar" lightbox="./media/set-web-browser.png":::
   <span data-ttu-id="67ef8-142">Escolha o canal de visualização do Microsoft Edge que você Visual Studio iniciar</span><span class="sxs-lookup"><span data-stu-id="67ef8-142">Choose the preview channel of Microsoft Edge that you want Visual Studio to launch</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="67ef8-143">Se você escolher o Microsoft Edge \(EdgeHTML\), Visual Studio o iniciará em vez do Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="67ef8-143">If you choose Microsoft Edge \(EdgeHTML\), Visual Studio launches it instead of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="67ef8-144">[Instale um][MicrosoftedgeinsiderDownload] dos canais de visualização do Microsoft Edge ou verifique se a versão do Microsoft Edge instalada em seu computador é o Microsoft Edge \(Chromium\) e não o Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="67ef8-144">[Install the one of the preview channels of Microsoft Edge][MicrosoftedgeinsiderDownload] or ensure that the version of Microsoft Edge installed on your machine is Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  

<span data-ttu-id="67ef8-145">Agora que Visual Studio está configurado corretamente, escolha o botão **verde Reproduzir.**</span><span class="sxs-lookup"><span data-stu-id="67ef8-145">Now that Visual Studio is correctly configured, choose the green **Play** button.</span></span>  <span data-ttu-id="67ef8-146">Visual Studio criar seu aplicativo, iniciar o servidor Web, iniciar o Microsoft Edge e navegar até ou qualquer `https://localhost:44362/` porta especificada em `launchSettings.json` .</span><span class="sxs-lookup"><span data-stu-id="67ef8-146">Visual Studio builds your app, start the web server, launch Microsoft Edge, and navigate to `https://localhost:44362/` or whatever port is specified in `launchSettings.json`.</span></span>  

:::image type="complex" source="./media/edge-launch.png" alt-text="O Microsoft Edge é lançado a partir Visual Studio" lightbox="./media/edge-launch.png":::
   <span data-ttu-id="67ef8-148">O Microsoft Edge é lançado a partir Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-148">Microsoft Edge launches from Visual Studio</span></span>  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a><span data-ttu-id="67ef8-149">Depurar JavaScript em execução no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67ef8-149">Debug JavaScript running in Microsoft Edge</span></span>  

<span data-ttu-id="67ef8-150">Alternar de volta para Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67ef8-150">Switch back to Visual Studio.</span></span>  <span data-ttu-id="67ef8-151">Em `Counter.js` , para definir um ponto de interrupção na Linha 13, escolha a canalização ao lado da linha.</span><span class="sxs-lookup"><span data-stu-id="67ef8-151">In `Counter.js`, to set a breakpoint on Line 13, choose the gutter next to the line.</span></span>  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Escolha a canalização ao lado da Linha 13 no Counter.js para definir um ponto de interrupção no Visual Studio" lightbox="./media/set-breakpoint.png":::
   <span data-ttu-id="67ef8-153">Escolha a canalização ao lado da Linha 13 para definir um ponto de interrupção `Counter.js` no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-153">Choose the gutter next to Line 13 in `Counter.js` to set a breakpoint in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-154">Agora, volte para a instância do Microsoft Edge que Visual Studio lançada.</span><span class="sxs-lookup"><span data-stu-id="67ef8-154">Now switch back to the instance of Microsoft Edge that Visual Studio launched.</span></span>  <span data-ttu-id="67ef8-155">Escolha no **Contador** no NavMenu à esquerda da página da Web.</span><span class="sxs-lookup"><span data-stu-id="67ef8-155">Choose on **Counter** in the NavMenu on the left of the webpage.</span></span>  <span data-ttu-id="67ef8-156">Agora escolha **Increment**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-156">Now choose **Increment**.</span></span>  

:::image type="complex" source="./media/edge-counter.png" alt-text="A página Contador em nosso ASP.NET Web Principal" lightbox="./media/edge-counter.png":::
   <span data-ttu-id="67ef8-158">A página Contador em nosso ASP.NET Web Principal</span><span class="sxs-lookup"><span data-stu-id="67ef8-158">The Counter page in our ASP.NET Core web app</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-159">O depurador JavaScript no Visual Studio atinge o ponto de interrupção definido em `Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="67ef8-159">The JavaScript debugger in Visual Studio hits the breakpoint you set in `Counter.js`.</span></span>  <span data-ttu-id="67ef8-160">Visual Studio agora pausa o tempo de execução do JavaScript em execução no Microsoft Edge e você pode passar pelo script linha por linha.</span><span class="sxs-lookup"><span data-stu-id="67ef8-160">Visual Studio now pauses the runtime of the JavaScript running in Microsoft Edge and you may step through the script line-by-line.</span></span>  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio o JavaScript em execução no Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   <span data-ttu-id="67ef8-162">Visual Studio o JavaScript em execução no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67ef8-162">Visual Studio pauses JavaScript running in Microsoft Edge</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-163">O exemplo foi apenas uma pequena demonstração da funcionalidade disponível no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67ef8-163">The example was just a minor demonstration of the functionality available in Visual Studio.</span></span>  <span data-ttu-id="67ef8-164">Para obter mais informações sobre a funcionalidade no Visual Studio 2019, navegue [até Visual Studio documentação][VisualStudioWindowsIndex].</span><span class="sxs-lookup"><span data-stu-id="67ef8-164">For more information about the functionality in Visual Studio 2019, navigate to [Visual Studio documentation][VisualStudioWindowsIndex].</span></span>  

## <a name="attach-to-microsoft-edge"></a><span data-ttu-id="67ef8-165">Anexar ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="67ef8-165">Attach to Microsoft Edge</span></span>  

<span data-ttu-id="67ef8-166">Anteriormente, você precisava iniciar o Microsoft Edge Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67ef8-166">Previously, you had to launch Microsoft Edge from Visual Studio.</span></span>  <span data-ttu-id="67ef8-167">Agora, você pode anexar o Visual Studio depurador a uma instância já em execução do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67ef8-167">Now, you are able to attach the Visual Studio debugger to an already running instance of Microsoft Edge.</span></span>  

<span data-ttu-id="67ef8-168">Primeiro, verifique se não há instâncias em execução do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67ef8-168">First, ensure that there are no running instances of Microsoft Edge.</span></span>  <span data-ttu-id="67ef8-169">Agora, na linha de comando, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="67ef8-169">Now, from your command line, run the following command.</span></span>  

```console
start msedge –remote-debugging-port=9222
```  

<span data-ttu-id="67ef8-170">No Visual Studio, abra o menu **Depurar** e escolha **Anexar ao Processo** ou selecione `Ctrl` + `Alt` + `P` .</span><span class="sxs-lookup"><span data-stu-id="67ef8-170">From Visual Studio, open the **Debug** menu and choose **Attach to Process** or select `Ctrl`+`Alt`+`P`.</span></span>  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Escolha Anexar ao processo no Visual Studio" lightbox="./media/attach-to-process.png":::
   <span data-ttu-id="67ef8-172">Escolha **Anexar ao processo** no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-172">Choose **Attach to Process** in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-173">Na caixa **de diálogo Anexar ao Processo,** de definir **Tipo** de conexão como Websocket de protocolo do **Chrome devtools (sem autenticação)**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-173">From the **Attach to Process** dialog, set **Connection type** to **Chrome devtools protocol websocket (no authentication)**.</span></span>  <span data-ttu-id="67ef8-174">Na caixa **de texto Conectar destino,** digite `http://localhost:9222/` e selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="67ef8-174">In the **Connecting target** textbox, type `http://localhost:9222/` and select `Enter`.</span></span>  <span data-ttu-id="67ef8-175">Revise a lista de guias abertas que você tem no Microsoft Edge listada na caixa **de diálogo Anexar ao Processo.**</span><span class="sxs-lookup"><span data-stu-id="67ef8-175">Review the list of open tabs you have in Microsoft Edge listed out in the **Attach to Process** dialog.</span></span>  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configure a caixa de diálogo Anexar ao Processo Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   <span data-ttu-id="67ef8-177">Configure a **caixa de diálogo Anexar ao Processo** Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-177">Configure the **Attach to Process** dialog in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="67ef8-178">Escolha **Selecionar...** > caixa de seleção ao lado de **JavaScript (Microsoft Edge – Chromium)**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-178">Choose **Select...** > the checkbox next to **JavaScript (Microsoft Edge – Chromium)**.</span></span>  <span data-ttu-id="67ef8-179">Para adicionar guias, navegue até novas guias e feche guias  e exibe as alterações refletidas na caixa de diálogo Anexar ao Processo, escolha o **botão Atualizar.**</span><span class="sxs-lookup"><span data-stu-id="67ef8-179">To add tabs, navigate to new tabs, and close tabs and display the changes reflected in the **Attach to Process** dialog, choose the **Refresh** button.</span></span>  <span data-ttu-id="67ef8-180">Escolha a guia que você deseja depurar e escolha **Anexar**.</span><span class="sxs-lookup"><span data-stu-id="67ef8-180">Choose the tab you want to debug and choose **Attach**.</span></span>  

<span data-ttu-id="67ef8-181">O Visual Studio depurador agora está anexado ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="67ef8-181">The Visual Studio debugger is now attached to Microsoft Edge.</span></span>  <span data-ttu-id="67ef8-182">Você pode pausar a execução do JavaScript, definir pontos de interrupção e revisar instruções diretamente na janela `console.log()` Depurar Saída em Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67ef8-182">You may pause the running of JavaScript, set breakpoints, and review `console.log()` statements directly in the Debug Output window in Visual Studio.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a><span data-ttu-id="67ef8-183">Entrar em contato com a equipe Visual Studio Microsoft</span><span class="sxs-lookup"><span data-stu-id="67ef8-183">Getting in touch with the Microsoft Visual Studio team</span></span>  

<span data-ttu-id="67ef8-184">As equipes do Microsoft Visual Studio e do Microsoft Edge querem saber mais sobre como você trabalha com JavaScript no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="67ef8-184">The Microsoft Visual Studio and Microsoft Edge teams wants to learn more about how you work with JavaScript in Visual Studio.</span></span>  <span data-ttu-id="67ef8-185">Para enviar seus comentários, escolha o **ícone Enviar Comentários** no Visual Studio ou tweet @VisualStudio e [@EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span><span class="sxs-lookup"><span data-stu-id="67ef8-185">To send your feedback, choose the **Send Feedback** icon in Visual Studio or tweet [@VisualStudio and @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span></span>  

:::image type="complex" source="./media/feedback-icon.png" alt-text="O ícone Enviar Comentários no Visual Studio" lightbox="./media/feedback-icon.png":::
   <span data-ttu-id="67ef8-187">O **ícone Enviar Comentários** no Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67ef8-187">The **Send Feedback** icon in Visual Studio</span></span>  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentação | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Baixar Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet para @VisualStudio e @EdgeDevTools | Twitter"  
