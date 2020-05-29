---
title: O que há de novo no DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 17dab9120535ae11ea5a5456552d47dbd7f9e236
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684717"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  







# <span data-ttu-id="98b4b-103">O que há de novo no DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="98b4b-103">What's New In DevTools (Microsoft Edge 83)</span></span>   

  

<span data-ttu-id="98b4b-104">Após o cronograma atualizado do Chromium, estamos ajustando o nosso cronograma para futuras versões do Microsoft Edge e cancelando o lançamento do Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="98b4b-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="98b4b-105">Confira nossa [postagem no blog][WindowsBlogStableRelease] para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="98b4b-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>

<span data-ttu-id="98b4b-106">Estes são os novos recursos disponíveis no DevTools no Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="98b4b-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>

## <span data-ttu-id="98b4b-107">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="98b4b-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="98b4b-108">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="98b4b-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="98b4b-109">Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.</span><span class="sxs-lookup"><span data-stu-id="98b4b-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="98b4b-110">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="98b4b-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="98b4b-111">Depurar remotamente o Microsoft Edge em dispositivos Windows 10</span><span class="sxs-lookup"><span data-stu-id="98b4b-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="98b4b-112">O aplicativo [ferramentas remotas para Microsoft Edge \ (beta \)][RemoteTools] agora está disponível na [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="98b4b-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="98b4b-113">Ao usar este aplicativo, que estende o [Windows Device portal][WindowsDevicePortal], você pode se conectar da instância do Microsoft Edge em execução na sua máquina de desenvolvimento a um dispositivo Windows 10 remoto, ver uma lista de destinos \ (todas as guias no Microsoft Edge e [PWAs][PWADoc] abertas no dispositivo Windows 10 \) e usar o devtools em seu computador de desenvolvimento em relação a um destino em execução no dispositivo Windows 10 remoto.</span><span class="sxs-lookup"><span data-stu-id="98b4b-113">Using this app, which extends the [Windows Device Portal][WindowsDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PWADoc] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

> ##### <span data-ttu-id="98b4b-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="98b4b-114">Figure 1</span></span>  
> <span data-ttu-id="98b4b-115">O aplicativo [Remote Tools para Microsoft Edge (beta)][RemoteTools] disponível na [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="98b4b-115">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
> ![O aplicativo Remote Tools para Microsoft Edge (beta) disponível na Microsoft Store][ImageRemoteTools]  

<span data-ttu-id="98b4b-117">[Leia nosso guia para configurar seu dispositivo Windows 10 e seu computador de desenvolvimento para depuração remota][RemoteDebuggingWin10].</span><span class="sxs-lookup"><span data-stu-id="98b4b-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][RemoteDebuggingWin10].</span></span>  <span data-ttu-id="98b4b-118">Informe-nos sobre sua experiência de depuração remota em [tweet][PostTweetEdgeDevTools] ou clique no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

### <span data-ttu-id="98b4b-119">Novas maneiras de acessar as configurações</span><span class="sxs-lookup"><span data-stu-id="98b4b-119">New ways to access Settings</span></span> 

<span data-ttu-id="98b4b-120">Há toneladas de configurações para o DevTools que você pode personalizar para fazer com que a aparência DevTools e funcione da maneira que você precisa.</span><span class="sxs-lookup"><span data-stu-id="98b4b-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="98b4b-121">No Microsoft Edge 83, agora é muito mais fácil acessar [as configurações][OverviewSettings] no devtools.</span><span class="sxs-lookup"><span data-stu-id="98b4b-121">In Microsoft Edge 83, accessing [Settings][OverviewSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="98b4b-122">Abra configurações com o ícone de engrenagem ao lado de alertas do console e o menu principal.</span><span class="sxs-lookup"><span data-stu-id="98b4b-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>

> ##### <span data-ttu-id="98b4b-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="98b4b-123">Figure 2</span></span> 
> <span data-ttu-id="98b4b-124">O ícone de engrenagem abre as configurações na DevTools ![ o ícone de engrenagem abre as configurações no devtools][ImageSettingsGearIcon]</span><span class="sxs-lookup"><span data-stu-id="98b4b-124">The gear icon opens Settings in the DevTools ![The gear icon opens Settings in the DevTools][ImageSettingsGearIcon]</span></span>  

<span data-ttu-id="98b4b-125">Você também pode abrir [as configurações][OverviewSettings] no **menu principal** em **mais ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="98b4b-125">You are also able to open [Settings][OverviewSettings] from the **Main Menu** under **More tools**.</span></span>

> ##### <span data-ttu-id="98b4b-126">Figura 3</span><span class="sxs-lookup"><span data-stu-id="98b4b-126">Figure 3</span></span> 
> <span data-ttu-id="98b4b-127">Menu principal > mais ferramentas do menu principal do > configurações ![ > mais ferramentas > configurações][ImageSettingsMainMenu]</span><span class="sxs-lookup"><span data-stu-id="98b4b-127">Main Menu > More tools > Settings ![Main Menu > More tools > Settings][ImageSettingsMainMenu]</span></span>  

<span data-ttu-id="98b4b-128">Chromium problema [#1050855][crbug1050855]</span><span class="sxs-lookup"><span data-stu-id="98b4b-128">Chromium issue [#1050855][crbug1050855]</span></span>

### <span data-ttu-id="98b4b-129">Novo e aprimorado infobars</span><span class="sxs-lookup"><span data-stu-id="98b4b-129">New and improved infobars</span></span>

<span data-ttu-id="98b4b-130">As barras de notificação informativas \ (infobars \) no DevTools agora têm uma aparência aprimorada e mais funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="98b4b-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="98b4b-131">No Microsoft Edge 83, o infobars é mais fácil de ler e oferecer botões para que você possa executar a ação relevante imediatamente.</span><span class="sxs-lookup"><span data-stu-id="98b4b-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>

> ##### <span data-ttu-id="98b4b-132">Figura 4</span><span class="sxs-lookup"><span data-stu-id="98b4b-132">Figure 4</span></span>
> <span data-ttu-id="98b4b-133">Barra de a e para impressão de um arquivo do minified no Microsoft Edge 83 ![ , para imprimir um arquivo minified no Microsoft edge 83][ImageInfobar]</span><span class="sxs-lookup"><span data-stu-id="98b4b-133">Infobar for pretty-printing a minified file in Microsoft Edge 83 ![Infobar for pretty-printing a minified file in Microsoft Edge 83][ImageInfobar]</span></span>  

<span data-ttu-id="98b4b-134">Chromium problema [#1056348][crbug1056348]</span><span class="sxs-lookup"><span data-stu-id="98b4b-134">Chromium issue [#1056348][crbug1056348]</span></span>

### <span data-ttu-id="98b4b-135">Navegar pelo seletor de cores com o teclado</span><span class="sxs-lookup"><span data-stu-id="98b4b-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="98b4b-136">O [seletor de cores][ColorPicker] é uma GUI no [painel elementos][ElementsDoc] para alteração `color` e `background-color` declarações.</span><span class="sxs-lookup"><span data-stu-id="98b4b-136">The [Color Picker][ColorPicker] is a GUI in the [Elements panel][ElementsDoc] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="98b4b-137">Em versões anteriores do Microsoft Edge, você não pôde navegar na seção **sombras** do [seletor de cores][ColorPicker] com o teclado.</span><span class="sxs-lookup"><span data-stu-id="98b4b-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][ColorPicker] with the keyboard.</span></span>  

> ##### <span data-ttu-id="98b4b-138">Figura 5</span><span class="sxs-lookup"><span data-stu-id="98b4b-138">Figure 5</span></span>  
> <span data-ttu-id="98b4b-139">Agora você pode usar o teclado para mover o seletor na seção **sombras** do [seletor de cores][ColorPicker]</span><span class="sxs-lookup"><span data-stu-id="98b4b-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][ColorPicker]</span></span>  
> ![Agora você pode usar o teclado para mover o seletor na seção sombras do seletor de cores][ImageColorPicker]  

<span data-ttu-id="98b4b-141">No Microsoft Edge 83, agora você pode usar o teclado para mover o seletor na seção **sombras** do seletor de cores.</span><span class="sxs-lookup"><span data-stu-id="98b4b-141">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="98b4b-142">Chromium problema [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="98b4b-142">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="98b4b-143">A guia Propriedades agora é preenchida após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="98b4b-143">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="98b4b-144">No Microsoft Edge 81 e versões anteriores, a **guia Propriedades** no [painel elementos][ElementsDoc] foi interrompida pelas atualizações de página.</span><span class="sxs-lookup"><span data-stu-id="98b4b-144">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][ElementsDoc] was broken by page refreshes.</span></span>  <span data-ttu-id="98b4b-145">Quando você atualiza a página, a **guia Propriedades** não preenche as propriedades do elemento atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="98b4b-145">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

> ##### <span data-ttu-id="98b4b-146">Figura 6</span><span class="sxs-lookup"><span data-stu-id="98b4b-146">Figure 6</span></span>  
> <span data-ttu-id="98b4b-147">No Microsoft Edge 81 e versões anteriores, a **guia Propriedades** estava em branco após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="98b4b-147">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
> ![No Microsoft Edge 81 e versões anteriores, a guia Propriedades estava em branco após uma atualização de página][ImagePropertiesIn81]  

<span data-ttu-id="98b4b-149">No Microsoft Edge 83, agora você pode ver as propriedades do elemento atualmente selecionado após uma atualização de página na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="98b4b-149">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

> ##### <span data-ttu-id="98b4b-150">Figura 7</span><span class="sxs-lookup"><span data-stu-id="98b4b-150">Figure 7</span></span>  
> <span data-ttu-id="98b4b-151">No Microsoft Edge 83, a **guia Propriedades** exibe as propriedades do elemento atualmente selecionado após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="98b4b-151">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
> ![No Microsoft Edge 83, a guia Propriedades exibe as propriedades do elemento atualmente selecionado após uma atualização de página][ImagePropertiesIn82]  

<span data-ttu-id="98b4b-153">Chromium problema [#1050999][crbug1050999]</span><span class="sxs-lookup"><span data-stu-id="98b4b-153">Chromium issue [#1050999][crbug1050999]</span></span>  

### <span data-ttu-id="98b4b-154">Use as teclas de direção para rolar a ferramenta alterações</span><span class="sxs-lookup"><span data-stu-id="98b4b-154">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="98b4b-155">A **ferramenta alterações** acompanha todas as alterações feitas em CSS ou JavaScript no devtools.</span><span class="sxs-lookup"><span data-stu-id="98b4b-155">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="98b4b-156">Você pode usar a ferramenta de **alterações** para ver rapidamente todas as suas alterações e retomar os retornos do seu editor/IDE.</span><span class="sxs-lookup"><span data-stu-id="98b4b-156">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="98b4b-157">Para abrir a **ferramenta alterações** , pressione `Ctrl` + `Shift` + `P` a devtools para abrir o [menu de comandos][DevToolsCommandMenuIndex] e digite `changes` .</span><span class="sxs-lookup"><span data-stu-id="98b4b-157">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="98b4b-158">Selecione e execute o comando **Mostrar alterações** para abrir a **ferramenta mudanças** na gaveta do devtools.</span><span class="sxs-lookup"><span data-stu-id="98b4b-158">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="98b4b-159">Quando você faz uma alteração em um arquivo minified, a **ferramenta alterações** permite que você role horizontalmente para ver todo o código do minified.</span><span class="sxs-lookup"><span data-stu-id="98b4b-159">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="98b4b-160">A partir do Microsoft Edge 83, agora você pode rolar horizontalmente usando as teclas de direção do teclado.</span><span class="sxs-lookup"><span data-stu-id="98b4b-160">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

> ##### <span data-ttu-id="98b4b-161">Figura 8</span><span class="sxs-lookup"><span data-stu-id="98b4b-161">Figure 8</span></span>  
> <span data-ttu-id="98b4b-162">No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver as alterações feitas em seu código minified na **ferramenta alterações**</span><span class="sxs-lookup"><span data-stu-id="98b4b-162">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
> ![No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver o código minified na ferramenta alterações][ImageChanges]  

<span data-ttu-id="98b4b-164">Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-164">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="98b4b-165">Chromium problema [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="98b4b-165">Chromium issue [#963183][crbug963183]</span></span>  

## <span data-ttu-id="98b4b-166">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="98b4b-166">Announcements from the Chromium project</span></span>  

<span data-ttu-id="98b4b-167">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 83 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="98b4b-167">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="98b4b-168">Emular deficiências de visão</span><span class="sxs-lookup"><span data-stu-id="98b4b-168">Emulate vision deficiencies</span></span>   

<span data-ttu-id="98b4b-169">Abra a [guia renderização][RenderingDoc] e use o novo recurso de **deficiências de visão de emulação** para ter uma ideia melhor de como as pessoas com diferentes tipos de deficiência visual apresentam o seu site.</span><span class="sxs-lookup"><span data-stu-id="98b4b-169">Open the [Rendering tab][RenderingDoc] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

> ##### <span data-ttu-id="98b4b-170">Figura 9</span><span class="sxs-lookup"><span data-stu-id="98b4b-170">Figure 9</span></span>  
> <span data-ttu-id="98b4b-171">Emulando a visão desfocada</span><span class="sxs-lookup"><span data-stu-id="98b4b-171">Emulating blurred vision</span></span>  
> ![Emulando a visão desfocada][ImageEmulatingBlurredVision]  

<span data-ttu-id="98b4b-173">O DevTools é capaz de emular a visão borrada e os seguintes [tipos de deficiências de visão de cor][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="98b4b-173">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="98b4b-174">Deficiência de visão colorida</span><span class="sxs-lookup"><span data-stu-id="98b4b-174">Color Vision Deficiency</span></span> | <span data-ttu-id="98b4b-175">Detalhes</span><span class="sxs-lookup"><span data-stu-id="98b4b-175">Details</span></span> |  
|:--- |:--- | 
| <span data-ttu-id="98b4b-176">Protanopia</span><span class="sxs-lookup"><span data-stu-id="98b4b-176">Protanopia</span></span> | <span data-ttu-id="98b4b-177">A incapacidade de perceber qualquer luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="98b4b-177">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="98b4b-178">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="98b4b-178">Deuteranopia</span></span> | <span data-ttu-id="98b4b-179">A incapacidade de perceber qualquer luz verde.</span><span class="sxs-lookup"><span data-stu-id="98b4b-179">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="98b4b-180">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="98b4b-180">Tritanopia</span></span> | <span data-ttu-id="98b4b-181">A incapacidade de perceber qualquer luz azul.</span><span class="sxs-lookup"><span data-stu-id="98b4b-181">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="98b4b-182">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="98b4b-182">Achromatopsia</span></span> | <span data-ttu-id="98b4b-183">A incapacidade de perceber qualquer cor, exceto para tonalidades de cinza \ (extremamente raro \).</span><span class="sxs-lookup"><span data-stu-id="98b4b-183">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> | 

<span data-ttu-id="98b4b-184">Existem versões menos extremas dessas deficiências de visão de cor e, na verdade, são mais comuns.</span><span class="sxs-lookup"><span data-stu-id="98b4b-184">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>
<span data-ttu-id="98b4b-185">Por exemplo, protanomaly é uma sensibilidade reduzida à luz vermelha (em oposição ao protanopia, que é a incapacidade completa de perceber a luz vermelha).</span><span class="sxs-lookup"><span data-stu-id="98b4b-185">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="98b4b-186">No entanto, essas deficiências de visão omaly não são tão claramente definidas: todas as pessoas com tal deficiência visual são diferentes e podem ver coisas de forma diferente (sendo capaz de perceber mais/menos das cores relevantes).</span><span class="sxs-lookup"><span data-stu-id="98b4b-186">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>

<span data-ttu-id="98b4b-187">Ao projetar para as simulações mais extremas no DevTools, os seus aplicativos Web são garantidos para pessoas com o protanomaly, o deuteranomaly, o tritanomaly e o achromatomaly também.</span><span class="sxs-lookup"><span data-stu-id="98b4b-187">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>

<span data-ttu-id="98b4b-188">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-188">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="98b4b-189">Chromium problema [#1003700][crbug1003700]</span><span class="sxs-lookup"><span data-stu-id="98b4b-189">Chromium issue [#1003700][crbug1003700]</span></span>  

### <span data-ttu-id="98b4b-190">Emular localidades</span><span class="sxs-lookup"><span data-stu-id="98b4b-190">Emulate locales</span></span> 

<span data-ttu-id="98b4b-191">Emular localidades definindo um local no local dos **sensores**  >  **Location**.</span><span class="sxs-lookup"><span data-stu-id="98b4b-191">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="98b4b-192">[Abrir o **menu de comando** ][DevToolsCommandMenuIndex] e digitar `Sensors` para acessar a guia **sensores** . Depois de executar essas ações, o DevTools modifica a localidade padrão atual, afetando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="98b4b-192">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab. After performing these actions, DevTools modifies the current default locale, affecting the following:</span></span>

- `Intl.*` <span data-ttu-id="98b4b-193">APIs, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="98b4b-193">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`
- <span data-ttu-id="98b4b-194">outras APIs JavaScript com reconhecimento de localidade, como `String.prototype.localeCompare` e `*.prototype.toLocaleString` , por exemplo:`123_456..toLocaleString()`</span><span class="sxs-lookup"><span data-stu-id="98b4b-194">other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example: `123_456..toLocaleString()`</span></span>
- <span data-ttu-id="98b4b-195">APIs DOM, como `navigator.language` e</span><span class="sxs-lookup"><span data-stu-id="98b4b-195">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`
- <span data-ttu-id="98b4b-196">o [`Accept-Language`][MDNAcceptLanguage] cabeçalho da solicitação http</span><span class="sxs-lookup"><span data-stu-id="98b4b-196">the [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>

> ##### <span data-ttu-id="98b4b-197">Figura 10</span><span class="sxs-lookup"><span data-stu-id="98b4b-197">Figure 10</span></span>  
> <span data-ttu-id="98b4b-198">Emulando uma localidade</span><span class="sxs-lookup"><span data-stu-id="98b4b-198">Emulating a locale</span></span>  
> ![Emulando uma localidade][ImageEmulatingLocales]  

<span data-ttu-id="98b4b-200">Para experimentar uma demonstração, consulte [exemplo de código dependente de localidade][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="98b4b-200">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="98b4b-201">Chromium problema [#1051822][crbug1051822]</span><span class="sxs-lookup"><span data-stu-id="98b4b-201">Chromium issue [#1051822][crbug1051822]</span></span>

### <span data-ttu-id="98b4b-202">Depuração da política de incorporação de várias origens \ (COEP \) depuração</span><span class="sxs-lookup"><span data-stu-id="98b4b-202">Cross-Origin Embedder Policy \(COEP\) debugging</span></span>   

<span data-ttu-id="98b4b-203">O painel rede agora fornece informações de depuração da [política de incorporação de várias origens][COEP] .</span><span class="sxs-lookup"><span data-stu-id="98b4b-203">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="98b4b-204">A coluna **status** agora fornece uma explicação rápida do motivo pelo qual uma solicitação foi bloqueada, bem como um link para exibir os cabeçalhos dessa solicitação para a depuração adicional:</span><span class="sxs-lookup"><span data-stu-id="98b4b-204">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

> ##### <span data-ttu-id="98b4b-205">Figura 11</span><span class="sxs-lookup"><span data-stu-id="98b4b-205">Figure 11</span></span>  
> <span data-ttu-id="98b4b-206">Solicitações bloqueadas na coluna **status**</span><span class="sxs-lookup"><span data-stu-id="98b4b-206">Blocked requests in the **Status** column</span></span>  
> ![Solicitações bloqueadas na coluna status][ImageNetworkStatus]  

<span data-ttu-id="98b4b-208">A seção de **cabeçalhos de resposta** da guia **cabeçalhos** fornece mais orientações sobre como resolver os problemas:</span><span class="sxs-lookup"><span data-stu-id="98b4b-208">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

> ##### <span data-ttu-id="98b4b-209">Figura 12</span><span class="sxs-lookup"><span data-stu-id="98b4b-209">Figure 12</span></span>  
> <span data-ttu-id="98b4b-210">Mais diretrizes na seção cabeçalhos de resposta</span><span class="sxs-lookup"><span data-stu-id="98b4b-210">More guidance in the Response Headers section</span></span>  
> ![Mais diretrizes na seção cabeçalhos de resposta][ImageNetworkGuidance]  

<span data-ttu-id="98b4b-212">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-212">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="98b4b-213">Chromium problema [#1051466][crbug1051466]</span><span class="sxs-lookup"><span data-stu-id="98b4b-213">Chromium issue [#1051466][crbug1051466]</span></span>  

### <span data-ttu-id="98b4b-214">Exibir solicitações de rede que definem um caminho de cookie específico</span><span class="sxs-lookup"><span data-stu-id="98b4b-214">View network requests that set a specific cookie path</span></span> 

<span data-ttu-id="98b4b-215">Use a nova `cookie-path` palavra-chave Filter no painel **rede** para se concentrar nas solicitações de rede que definem um [caminho de cookie][MDNCookiePath]específico.</span><span class="sxs-lookup"><span data-stu-id="98b4b-215">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>

<span data-ttu-id="98b4b-216">Verifique as [solicitações de filtro por Propriedades][NetworkProperties] para descobrir mais palavras-chave como `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="98b4b-216">Check out [Filter requests by properties][NetworkProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="98b4b-217">**Encaixar à esquerda** no menu de comando</span><span class="sxs-lookup"><span data-stu-id="98b4b-217">**Dock to left** from the Command Menu</span></span>   

<span data-ttu-id="98b4b-218">Abra o [menu de comando][DevToolsCommandMenuIndex] e execute o `Dock to left` comando para mover devtools para a esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="98b4b-218">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

> ##### <span data-ttu-id="98b4b-219">Figura 13</span><span class="sxs-lookup"><span data-stu-id="98b4b-219">Figure 13</span></span>  
> <span data-ttu-id="98b4b-220">DevTools encaixado à esquerda da viewport</span><span class="sxs-lookup"><span data-stu-id="98b4b-220">DevTools docked to the left of the viewport</span></span>  
> ![DevTools encaixado à esquerda da viewport][ImageDockToLeft]  

> [!NOTE]
> <span data-ttu-id="98b4b-222">O recurso **Dock to Left** está disponível desde o Microsoft Edge 75, mas anteriormente era acessível apenas a partir do [**menu principal**][MainMenuDoc].</span><span class="sxs-lookup"><span data-stu-id="98b4b-222">The **Dock to left** feature has been available since Microsoft Edge 75 but it was previously only accessible from the [**Main Menu**][MainMenuDoc].</span></span>  <span data-ttu-id="98b4b-223">O novo recurso no Microsoft Edge 83 é que agora você pode acessar esse recurso no menu de comando.</span><span class="sxs-lookup"><span data-stu-id="98b4b-223">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="98b4b-224">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-224">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="98b4b-225">Chromium problema [#1011679][crbug1011679]</span><span class="sxs-lookup"><span data-stu-id="98b4b-225">Chromium issue [#1011679][crbug1011679]</span></span>  

### <span data-ttu-id="98b4b-226">O painel **auditorias** agora é o painel **Lighthouse**</span><span class="sxs-lookup"><span data-stu-id="98b4b-226">The **Audits** panel is now the **Lighthouse** panel</span></span>   

<span data-ttu-id="98b4b-227">A equipe do DevTools freqüentemente tem comentários dos desenvolvedores da Web que, enquanto era possível executar o [Lighthouse][GithubGoogleChromeLighthouse] do devtools, quando eles tentavam não puderam localizar o painel "Lighthouse", portanto, o painel **auditorias** agora é o painel **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="98b4b-227">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

> ##### <span data-ttu-id="98b4b-228">Figura 14</span><span class="sxs-lookup"><span data-stu-id="98b4b-228">Figure 14</span></span>  
> <span data-ttu-id="98b4b-229">O painel Lighthouse</span><span class="sxs-lookup"><span data-stu-id="98b4b-229">The Lighthouse panel</span></span>  
> ![O painel Lighthouse][ImageLighthouse]  

> [!NOTE]
> <span data-ttu-id="98b4b-231">O painel **Lighthouse** fornece links para conteúdo hospedado em websites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="98b4b-231">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="98b4b-232">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e todos os dados que eles podem coletar.</span><span class="sxs-lookup"><span data-stu-id="98b4b-232">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="98b4b-233">Excluir todas as substituições locais em uma pasta</span><span class="sxs-lookup"><span data-stu-id="98b4b-233">Delete all Local Overrides in a folder</span></span>   

<span data-ttu-id="98b4b-234">Depois de configurar **substituições locais** , você pode clicar com o botão direito do mouse em uma pasta e selecionar a opção novo **excluir tudo substitui** para excluir todas as substituições locais nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="98b4b-234">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

> ##### <span data-ttu-id="98b4b-235">Figura 15</span><span class="sxs-lookup"><span data-stu-id="98b4b-235">Figure 15</span></span>  
> <span data-ttu-id="98b4b-236">Excluir todas as substituições</span><span class="sxs-lookup"><span data-stu-id="98b4b-236">Delete all overrides</span></span>  
> ![Excluir todas as substituições][ImageDeleteOverrides]  

<span data-ttu-id="98b4b-238">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-238">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="98b4b-239">Chromium problema [#1016501][crbug1016501]</span><span class="sxs-lookup"><span data-stu-id="98b4b-239">Chromium issue [#1016501][crbug1016501]</span></span>  

### <span data-ttu-id="98b4b-240">Interface do usuário de tarefas longa atualizada</span><span class="sxs-lookup"><span data-stu-id="98b4b-240">Updated Long tasks UI</span></span>   

<span data-ttu-id="98b4b-241">Uma **tarefa longa** é o código JavaScript que monopolizes o thread principal há muito tempo, fazendo com que uma página da Web congele.</span><span class="sxs-lookup"><span data-stu-id="98b4b-241">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="98b4b-242">Você foi capaz de [Visualizar tarefas longas no painel de desempenho][LongTasksInPerformancePanel] durante um período de tempo, mas no Microsoft Edge 83 a interface do usuário de visualização de tarefa longa no painel desempenho foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="98b4b-242">You have been able to [visualize Long Tasks in the Performance panel][LongTasksInPerformancePanel] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="98b4b-243">A parte de tarefa longa de uma tarefa está agora colorida com um plano de fundo vermelho listrado.</span><span class="sxs-lookup"><span data-stu-id="98b4b-243">The Long Task portion of a task is now colored with a striped red background.</span></span>  

> ##### <span data-ttu-id="98b4b-244">Figura 16</span><span class="sxs-lookup"><span data-stu-id="98b4b-244">Figure 16</span></span>  
> <span data-ttu-id="98b4b-245">A nova interface do usuário de tarefa longa</span><span class="sxs-lookup"><span data-stu-id="98b4b-245">The new Long Task UI</span></span>  
> ![A nova interface do usuário de tarefa longa][ImageLongTask]  

<span data-ttu-id="98b4b-247">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone de [comentários](#feedback) !</span><span class="sxs-lookup"><span data-stu-id="98b4b-247">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="98b4b-248">Chromium problema [#1054447][crbug1054447]</span><span class="sxs-lookup"><span data-stu-id="98b4b-248">Chromium issue [#1054447][crbug1054447]</span></span>  

### <span data-ttu-id="98b4b-249">Suporte a ícones mascaráveis no painel manifesto</span><span class="sxs-lookup"><span data-stu-id="98b4b-249">Maskable icon support in the Manifest pane</span></span>   

<span data-ttu-id="98b4b-250">O Android Oreo introduziu ícones adaptáveis, que exibem ícones do aplicativo em uma variedade de formas em diferentes modelos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98b4b-250">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="98b4b-251">**Ícones Mascaráveis** são um novo formato de ícone que dão suporte a ícones adaptáveis, que permitem que você verifique se o ícone do [PWA][PWADoc] tem uma boa aparência em dispositivos que dão suporte ao padrão de ícones mascaráveis.</span><span class="sxs-lookup"><span data-stu-id="98b4b-251">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PWADoc] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="98b4b-252">Habilite a caixa de seleção **Mostrar apenas a área de segurança mínima para ícones mascaráveis** no painel **manifesto** para verificar se o ícone mascarable tem uma boa aparência em dispositivos Android do Oreo.</span><span class="sxs-lookup"><span data-stu-id="98b4b-252">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

> ##### <span data-ttu-id="98b4b-253">Figura 17</span><span class="sxs-lookup"><span data-stu-id="98b4b-253">Figure 17</span></span>  
> <span data-ttu-id="98b4b-254">A caixa de seleção "mostrar apenas a área de segurança mínima para ícones mascaráveis"</span><span class="sxs-lookup"><span data-stu-id="98b4b-254">The "Show only the minimum safe area for maskable icons" checkbox</span></span>  
> ![A caixa de seleção "mostrar apenas a área de segurança mínima para ícones mascaráveis"][ImageMaskableIcons]  

> [!NOTE]
> <span data-ttu-id="98b4b-256">Este recurso foi iniciado no Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="98b4b-256">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="98b4b-257">As atualizações abordadas aqui no Microsoft Edge 83 não foram abordadas nas novidades do [devtools (Microsoft edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="98b4b-257">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="98b4b-258">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="98b4b-258">Feedback</span></span>   

  

<span data-ttu-id="98b4b-259">Para discutir os novos recursos e alterações nesta postagem, ou qualquer outro item relacionado ao DevTools:</span><span class="sxs-lookup"><span data-stu-id="98b4b-259">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="98b4b-260">Envie seus comentários usando o ícone de **comentários** no devtools</span><span class="sxs-lookup"><span data-stu-id="98b4b-260">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="98b4b-261">Tweet em [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="98b4b-261">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="98b4b-262">Enviar uma sugestão para [a Web que][TheWebWeWant] queremos</span><span class="sxs-lookup"><span data-stu-id="98b4b-262">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="98b4b-263">Arquivos com erros neste documento no repositório [Edge-Developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="98b4b-263">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

> ##### <span data-ttu-id="98b4b-264">Figura 18</span><span class="sxs-lookup"><span data-stu-id="98b4b-264">Figure 18</span></span>  
> <span data-ttu-id="98b4b-265">O ícone de **comentários** no Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="98b4b-265">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![O ícone \* \* feedback \* \* na Microsoft Edge DevTools][ImageFeedbackIcon]  

## <span data-ttu-id="98b4b-267">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="98b4b-267">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="98b4b-268">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="98b4b-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="98b4b-269">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="98b4b-269">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- <<../../_shared/devtools-feedback.md>>

<<../../_shared/canary.md>>

<<../../_shared/discover.md>> -->

  

<!-- image links -->  

[ImageRemoteTools]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/remote-tools.msft.png "Figura 1: o aplicativo ferramentas remotas para o Microsoft Edge (beta) disponível na Microsoft Store"  
[ImageSettingsGearIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings.msft.png "Figura 2: o ícone de engrenagem abre as configurações na DevTools"
[ImageSettingsMainMenu]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings2.msft.png "Figura 3: menu principal > mais ferramentas > configurações"
[ImageInfobar]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/infobar.msft.png "Figura 4: barra de formatação para imprimir um arquivo minified no Microsoft Edge 83"
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/color-picker.msft.png "Figura 5: agora você pode usar o teclado para mover o seletor na seção sombras do seletor de cores"  
[ImagePropertiesIn81]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-81.msft.png "Figura 6: no Microsoft Edge 81 e versões anteriores, a guia Propriedades estava em branco após uma atualização de página"  
[ImagePropertiesIn82]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-82.msft.png "Figura 7: no Microsoft Edge 83, a guia Propriedades exibe as propriedades do elemento atualmente selecionado após uma atualização de página"  
[ImageChanges]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/changes.msft.png "Figura 8: no Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver o código minified na ferramenta alterações"  
[ImageEmulatingBlurredVision]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/vision.msft.png "Figura 9: emulando a visão desfocada"  
[ImageEmulatingLocales]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/locale.msft.png "Figura 10: emulando uma localidade"
[ImageNetworkStatus]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/status.msft.png "Figura 11: solicitações bloqueadas na coluna status"  
[ImageNetworkGuidance]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/guidance.msft.png "Figura 12: mais diretrizes na seção de cabeçalhos de resposta"  
[ImageDockToLeft]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/dock-to-left.msft.png "Figura 13: DevTools encaixado à esquerda da viewport"  
[ImageLighthouse]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/lighthouse.msft.png "Figura 14: painel de Lighthouse"  
[ImageDeleteOverrides]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/overrides.msft.png "Figura 15: excluir todas as substituições"  
[ImageLongTask]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/long-task.msft.png "Figura 16: a nova interface do usuário longa da tarefa"  
[ImageMaskableIcons]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/maskable-icons.msft.png "Figura 17: a caixa de seleção Mostrar apenas a área de segurança mínima para ícones mascaráveis"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/feedback-icon.msft.png "Figura 18: o ícone de comentários no Microsoft Edge DevTools"  

[ImageLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/breakpoint.msft.png
[ImageLogpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/logpoint.msft.png

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Novo problema-MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canais de visualização do Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "A Web que queremos"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "O que há de novo no DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar as cores com o seletor de cores"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Alterar o posicionamento a partir do menu principal"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Exibir atividade de thread principal"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização"  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introdução à depuração remota de dispositivos Windows 10"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Pontos de interrupção de linha do código"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Visão geral do Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Ferramentas remotas para Microsoft Edge (beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Atualização em lançamentos de canais estáveis para o Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Tipos de cegueira para cor"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemplo de código dependente de localidade"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Problema 963183: DevTools não são compatíveis com a WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Problema 1003700: adicionar suporte a DevTools para simulação de deficiência visual de cor"  
[crbug1011679]: https://crbug.com/1011679 "Problema 1011679: apresentar ' Dock to Left ' usando o menu de comandos"  
[crbug1016501]: https://crbug.com/1016501 "Problema 1016501: solicitação de recurso: botão para excluir todas as substituições locais"  
[crbug1050999]: https://crbug.com/1050999 "Problema 1050999: guia Propriedades"  
[crbug1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Problema 1054447: atualizar as métricas de desempenho na linha do tempo do DevTools"  
[crbug1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: adicionar a interface do usuário para emular a localidade"
[crbug1041830]: https://crbug.com/1041830 "Problema 1041830: aprimorar as cores dos pontos de interrupção"
[crbug1050855]: https://crbug.com/1050855 "Problema 1050855: o modo de exibição de configurações é difícil de descobrir"
[crbug1056348]: https://crbug.com/1056348 "Problema 1056348: atualização do componente da barra de atualizações"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP e COEP explicou-política do Opener entre origens"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP e COEP explicou-política de incorporação de várias origens"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Repositório do GitHub Lighthouse"  

> [!NOTE]
> <span data-ttu-id="98b4b-324">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="98b4b-324">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="98b4b-325">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/03/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="98b4b-325">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="98b4b-327">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="98b4b-327">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
