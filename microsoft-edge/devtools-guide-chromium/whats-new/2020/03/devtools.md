---
title: O que há de novo no DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f1b5d147aac1b8b527cc7365f9f91a2a7974863e
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942219"
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

# <span data-ttu-id="d2cee-103">O que há de novo no DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="d2cee-103">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="d2cee-104">Após o cronograma atualizado do Chromium, estamos ajustando o nosso cronograma para futuras versões do Microsoft Edge e cancelando o lançamento do Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="d2cee-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="d2cee-105">Confira nossa [postagem no blog][WindowsBlogStableRelease] para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d2cee-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="d2cee-106">Estes são os novos recursos disponíveis no DevTools no Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="d2cee-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="d2cee-107">Anúncios da equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d2cee-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="d2cee-108">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe do Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="d2cee-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="d2cee-109">Dê uma olhada neles para experimentar os novos recursos do DevTools, as extensões de código do VS e muito mais.</span><span class="sxs-lookup"><span data-stu-id="d2cee-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="d2cee-110">Para ficar atualizado sobre todos os recursos mais recentes e mais recentes em suas ferramentas de desenvolvedor, baixe os [canais de visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="d2cee-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="d2cee-111">Depurar remotamente o Microsoft Edge em dispositivos Windows 10</span><span class="sxs-lookup"><span data-stu-id="d2cee-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="d2cee-112">O aplicativo [ferramentas remotas para Microsoft Edge \ (beta \)][RemoteTools] agora está disponível na [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="d2cee-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="d2cee-113">Ao usar este aplicativo, que estende o [Windows Device portal][WindowsUwpDebugTestPerfDevicePortal], você pode se conectar da instância do Microsoft Edge em execução na sua máquina de desenvolvimento a um dispositivo Windows 10 remoto, ver uma lista de destinos \ (todas as guias no Microsoft Edge e [PWAs][PprgressiveWebAppsChromiumIndex] abertas no dispositivo Windows 10 \) e usar o devtools em seu computador de desenvolvimento em relação a um destino em execução no dispositivo Windows 10 remoto.</span><span class="sxs-lookup"><span data-stu-id="d2cee-113">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="O aplicativo Remote Tools para Microsoft Edge (beta) disponível na Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="d2cee-115">Figura 1: o aplicativo [ferramentas remotas para o Microsoft Edge (beta)][RemoteTools] disponível na [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="d2cee-115">Figure 1:  The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-116">[Leia nosso guia para configurar seu dispositivo Windows 10 e seu computador de desenvolvimento para depuração remota][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="d2cee-116">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="d2cee-117">Informe-nos sobre sua experiência de depuração remota em [tweet][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-117">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="d2cee-118">Novas maneiras de acessar as configurações</span><span class="sxs-lookup"><span data-stu-id="d2cee-118">New ways to access Settings</span></span>  

<span data-ttu-id="d2cee-119">Há toneladas de configurações para o DevTools que você pode personalizar para fazer com que a aparência DevTools e funcione da maneira que você precisa.</span><span class="sxs-lookup"><span data-stu-id="d2cee-119">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="d2cee-120">No Microsoft Edge 83, agora é muito mais fácil acessar [as configurações][DevtoolsCustomizeIndexSettings] no devtools.</span><span class="sxs-lookup"><span data-stu-id="d2cee-120">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="d2cee-121">Abra configurações com o ícone de engrenagem ao lado de alertas do console e o menu principal.</span><span class="sxs-lookup"><span data-stu-id="d2cee-121">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="O ícone de engrenagem abre as configurações na DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="d2cee-123">Figura 2: o ícone de engrenagem abre **as configurações** na devtools</span><span class="sxs-lookup"><span data-stu-id="d2cee-123">Figure 2:  The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-124">Você também pode abrir [as configurações][DevtoolsCustomizeIndexSettings] no **menu principal** em **mais ferramentas**.</span><span class="sxs-lookup"><span data-stu-id="d2cee-124">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu principal > mais ferramentas > configurações" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="d2cee-126">Figura 3: **menu principal**  >  **mais**  >  **configurações** de ferramentas</span><span class="sxs-lookup"><span data-stu-id="d2cee-126">Figure 3:  **Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-127">Chromium problema [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="d2cee-127">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="d2cee-128">Novo e aprimorado infobars</span><span class="sxs-lookup"><span data-stu-id="d2cee-128">New and improved infobars</span></span>

<span data-ttu-id="d2cee-129">As barras de notificação informativas \ (infobars \) no DevTools agora têm uma aparência aprimorada e mais funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="d2cee-129">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="d2cee-130">No Microsoft Edge 83, o infobars é mais fácil de ler e oferecer botões para que você possa executar a ação relevante imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d2cee-130">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barra de formatação para imprimir um arquivo minified no Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="d2cee-132">Figura 4: barra de formatação para imprimir um arquivo minified no Microsoft Edge versão 83</span><span class="sxs-lookup"><span data-stu-id="d2cee-132">Figure 4:  Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-133">Chromium problema [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="d2cee-133">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="d2cee-134">Navegar pelo seletor de cores com o teclado</span><span class="sxs-lookup"><span data-stu-id="d2cee-134">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="d2cee-135">O [seletor de cores][DevtoolsCssReferenceColorPicker] é uma GUI no [painel elementos][DevtoolsCssIndex] para alteração `color` e `background-color` declarações.</span><span class="sxs-lookup"><span data-stu-id="d2cee-135">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="d2cee-136">Em versões anteriores do Microsoft Edge, você não pôde navegar na seção **sombras** do [seletor de cores][DevtoolsCssReferenceColorPicker] com o teclado.</span><span class="sxs-lookup"><span data-stu-id="d2cee-136">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Agora você pode usar o teclado para mover o seletor na seção sombras do seletor de cores" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="d2cee-138">Figura 5: agora você pode usar o teclado para mover o seletor na seção **sombras** do [seletor de cores][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="d2cee-138">Figure 5:  You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-139">No Microsoft Edge 83, agora você pode usar o teclado para mover o seletor na seção **sombras** do seletor de cores.</span><span class="sxs-lookup"><span data-stu-id="d2cee-139">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="d2cee-140">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="d2cee-140">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="d2cee-141">A guia Propriedades agora é preenchida após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="d2cee-141">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="d2cee-142">No Microsoft Edge 81 e versões anteriores, a **guia Propriedades** no [painel elementos][DevtoolsCssIndex] foi interrompida pelas atualizações de página.</span><span class="sxs-lookup"><span data-stu-id="d2cee-142">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="d2cee-143">Quando você atualiza a página, a **guia Propriedades** não preenche as propriedades do elemento atualmente selecionado.</span><span class="sxs-lookup"><span data-stu-id="d2cee-143">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="No Microsoft Edge 81 e versões anteriores, a guia Propriedades estava em branco após uma atualização de página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="d2cee-145">Figura 6: no Microsoft Edge 81 e versões anteriores, a **guia Propriedades** estava em branco após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="d2cee-145">Figure 6:  In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-146">No Microsoft Edge 83, agora você pode ver as propriedades do elemento atualmente selecionado após uma atualização de página na **guia Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="d2cee-146">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="No Microsoft Edge 83, a guia Propriedades exibe as propriedades do elemento atualmente selecionado após uma atualização de página" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="d2cee-148">Figura 7: no Microsoft Edge 83, a **guia Propriedades** exibe as propriedades do elemento atualmente selecionado após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="d2cee-148">Figure 7:  In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-149">Chromium problema [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="d2cee-149">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="d2cee-150">Use as teclas de direção para rolar a ferramenta alterações</span><span class="sxs-lookup"><span data-stu-id="d2cee-150">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="d2cee-151">A **ferramenta alterações** acompanha todas as alterações feitas em CSS ou JavaScript no devtools.</span><span class="sxs-lookup"><span data-stu-id="d2cee-151">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="d2cee-152">Você pode usar a ferramenta de **alterações** para ver rapidamente todas as suas alterações e retomar os retornos do seu editor/IDE.</span><span class="sxs-lookup"><span data-stu-id="d2cee-152">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="d2cee-153">Para abrir a **ferramenta alterações** , pressione `Ctrl` + `Shift` + `P` a devtools para abrir o [menu de comandos][DevToolsCommandMenuIndex] e digite `changes` .</span><span class="sxs-lookup"><span data-stu-id="d2cee-153">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="d2cee-154">Selecione e execute o comando **Mostrar alterações** para abrir a **ferramenta mudanças** na gaveta do devtools.</span><span class="sxs-lookup"><span data-stu-id="d2cee-154">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="d2cee-155">Quando você faz uma alteração em um arquivo minified, a **ferramenta alterações** permite que você role horizontalmente para ver todo o código do minified.</span><span class="sxs-lookup"><span data-stu-id="d2cee-155">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="d2cee-156">A partir do Microsoft Edge 83, agora você pode rolar horizontalmente usando as teclas de direção do teclado.</span><span class="sxs-lookup"><span data-stu-id="d2cee-156">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver o código minified na ferramenta alterações" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="d2cee-158">Figura 8: no Microsoft Edge 83, você pode rolar horizontalmente com as teclas de direção para ver as alterações feitas em seu código minified na **ferramenta alterações**</span><span class="sxs-lookup"><span data-stu-id="d2cee-158">Figure 8:  In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-159">Se você usar leitores de tela ou o teclado para navegar pelo DevTools, envie-nos seus comentários em [tweeting][PostTweetEdgeDevTools] ou clique no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-159">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="d2cee-160">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="d2cee-160">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="d2cee-161">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="d2cee-161">Announcements from the Chromium project</span></span>  

<span data-ttu-id="d2cee-162">As seções a seguir anunciarão recursos adicionais disponíveis no Microsoft Edge 83 que contribuíram para o projeto de código-fonte aberto Chromium.</span><span class="sxs-lookup"><span data-stu-id="d2cee-162">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="d2cee-163">Emular deficiências de visão</span><span class="sxs-lookup"><span data-stu-id="d2cee-163">Emulate vision deficiencies</span></span>  

<span data-ttu-id="d2cee-164">Abra a [guia renderização][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] e use o novo recurso de **deficiências de visão de emulação** para ter uma ideia melhor de como as pessoas com diferentes tipos de deficiência visual apresentam o seu site.</span><span class="sxs-lookup"><span data-stu-id="d2cee-164">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulando a visão desfocada" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="d2cee-166">Figura 9: emulando a visão desfocada</span><span class="sxs-lookup"><span data-stu-id="d2cee-166">Figure 9:  Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-167">O DevTools é capaz de emular a visão borrada e os seguintes [tipos de deficiências de visão de cor][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="d2cee-167">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="d2cee-168">Deficiência de visão colorida</span><span class="sxs-lookup"><span data-stu-id="d2cee-168">Color Vision Deficiency</span></span> | <span data-ttu-id="d2cee-169">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d2cee-169">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="d2cee-170">Protanopia</span><span class="sxs-lookup"><span data-stu-id="d2cee-170">Protanopia</span></span> | <span data-ttu-id="d2cee-171">A incapacidade de perceber qualquer luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="d2cee-171">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="d2cee-172">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="d2cee-172">Deuteranopia</span></span> | <span data-ttu-id="d2cee-173">A incapacidade de perceber qualquer luz verde.</span><span class="sxs-lookup"><span data-stu-id="d2cee-173">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="d2cee-174">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="d2cee-174">Tritanopia</span></span> | <span data-ttu-id="d2cee-175">A incapacidade de perceber qualquer luz azul.</span><span class="sxs-lookup"><span data-stu-id="d2cee-175">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="d2cee-176">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="d2cee-176">Achromatopsia</span></span> | <span data-ttu-id="d2cee-177">A incapacidade de perceber qualquer cor, exceto para tonalidades de cinza \ (extremamente raro \).</span><span class="sxs-lookup"><span data-stu-id="d2cee-177">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="d2cee-178">Existem versões menos extremas dessas deficiências de visão de cor e, na verdade, são mais comuns.</span><span class="sxs-lookup"><span data-stu-id="d2cee-178">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="d2cee-179">Por exemplo, protanomaly é uma sensibilidade reduzida à luz vermelha (em oposição ao protanopia, que é a incapacidade completa de perceber a luz vermelha).</span><span class="sxs-lookup"><span data-stu-id="d2cee-179">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="d2cee-180">No entanto, essas deficiências de visão omaly não são tão claramente definidas: todas as pessoas com tal deficiência visual são diferentes e podem ver coisas de forma diferente (sendo capaz de perceber mais/menos das cores relevantes).</span><span class="sxs-lookup"><span data-stu-id="d2cee-180">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="d2cee-181">Ao projetar para as simulações mais extremas no DevTools, os seus aplicativos Web são garantidos para pessoas com o protanomaly, o deuteranomaly, o tritanomaly e o achromatomaly também.</span><span class="sxs-lookup"><span data-stu-id="d2cee-181">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="d2cee-182">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-182">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="d2cee-183">Chromium problema [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="d2cee-183">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="d2cee-184">Emular localidades</span><span class="sxs-lookup"><span data-stu-id="d2cee-184">Emulate locales</span></span>  

<span data-ttu-id="d2cee-185">Emular localidades definindo um local no local dos **sensores**  >  **Location**.</span><span class="sxs-lookup"><span data-stu-id="d2cee-185">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="d2cee-186">[Abrir o **menu de comando** ][DevToolsCommandMenuIndex] e digitar `Sensors` para acessar a guia **sensores** .  Depois de executar essas ações, o DevTools modifica a localidade padrão atual, afetando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2cee-186">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="d2cee-187">APIs, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2cee-187">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="d2cee-188">Outras APIs JavaScript com reconhecimento de localidade, como `String.prototype.localeCompare` e `*.prototype.toLocaleString` , por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2cee-188">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="d2cee-189">APIs DOM, como `navigator.language` e</span><span class="sxs-lookup"><span data-stu-id="d2cee-189">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="d2cee-190">O [`Accept-Language`][MDNAcceptLanguage] cabeçalho da solicitação http</span><span class="sxs-lookup"><span data-stu-id="d2cee-190">The [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="d2cee-191">Atualizações `navigator.language` e `navigator.languages` não são visíveis imediatamente, mas somente após a próxima atualização da navegação ou da página.</span><span class="sxs-lookup"><span data-stu-id="d2cee-191">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="d2cee-192">As alterações feitas no `Accept-Language` cabeçalho http só se refletem nas solicitações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d2cee-192">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulando uma localidade" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="d2cee-194">Figura 10: emulando uma localidade</span><span class="sxs-lookup"><span data-stu-id="d2cee-194">Figure 10:  Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-195">Para experimentar uma demonstração, consulte [exemplo de código dependente de localidade][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="d2cee-195">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="d2cee-196">Chromium problema [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="d2cee-196">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="d2cee-197">Depuração de política de incorporação de várias origens (COEP)</span><span class="sxs-lookup"><span data-stu-id="d2cee-197">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="d2cee-198">O painel rede agora fornece informações de depuração da [política de incorporação de várias origens][COEP] .</span><span class="sxs-lookup"><span data-stu-id="d2cee-198">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="d2cee-199">A coluna **status** agora fornece uma explicação rápida do motivo pelo qual uma solicitação foi bloqueada, bem como um link para exibir os cabeçalhos dessa solicitação para a depuração adicional:</span><span class="sxs-lookup"><span data-stu-id="d2cee-199">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitações bloqueadas na coluna \* \* status \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="d2cee-201">Figura 11: solicitações bloqueadas na coluna status</span><span class="sxs-lookup"><span data-stu-id="d2cee-201">Figure 11:  Blocked requests in the Status column</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-202">A seção de **cabeçalhos de resposta** da guia **cabeçalhos** fornece mais orientações sobre como resolver os problemas:</span><span class="sxs-lookup"><span data-stu-id="d2cee-202">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Mais diretrizes na seção cabeçalhos de resposta" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="d2cee-204">Figura 12: mais diretrizes na seção de cabeçalhos de resposta</span><span class="sxs-lookup"><span data-stu-id="d2cee-204">Figure 12:  More guidance in the Response Headers section</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-205">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-205">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="d2cee-206">Chromium problema [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="d2cee-206">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="d2cee-207">Novos ícones para pontos de interrupção, pontos de interrupção condicionais e logpoints</span><span class="sxs-lookup"><span data-stu-id="d2cee-207">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="d2cee-208">O painel fontes tem novos ícones para pontos de interrupção, pontos de interrupção condicionais e logpoints:</span><span class="sxs-lookup"><span data-stu-id="d2cee-208">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="d2cee-209">Pontos de interrupção \ (</span><span class="sxs-lookup"><span data-stu-id="d2cee-209">Breakpoints \(</span></span>![Interrupção](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="d2cee-211">\) são representados por círculos vermelhos.</span><span class="sxs-lookup"><span data-stu-id="d2cee-211">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="d2cee-212">Pontos de interrupção condicionais \ (</span><span class="sxs-lookup"><span data-stu-id="d2cee-212">Conditional Breakpoints \(</span></span>![Ponto de interrupção condicional](../../media/2020/03/conditional.msft.png)<span data-ttu-id="d2cee-214">\) são representados por círculos semi-brancos semivermelhos.</span><span class="sxs-lookup"><span data-stu-id="d2cee-214">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="d2cee-215">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="d2cee-215">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="d2cee-217">\) são representados por círculos vermelhos com ícones de console.</span><span class="sxs-lookup"><span data-stu-id="d2cee-217">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="d2cee-218">A motivação para os novos ícones era deixar a interface do usuário mais consistente com outras ferramentas de depuração de GUI \ (que normalmente são pontos de interrupção de cor vermelhas \) e para facilitar a distinção entre os três recursos em um relance.</span><span class="sxs-lookup"><span data-stu-id="d2cee-218">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="d2cee-219">Chromium problema [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="d2cee-219">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="d2cee-220">Exibir solicitações de rede que definem um caminho de cookie específico</span><span class="sxs-lookup"><span data-stu-id="d2cee-220">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="d2cee-221">Use a nova `cookie-path` palavra-chave Filter no painel **rede** para se concentrar nas solicitações de rede que definem um [caminho de cookie][MDNCookiePath]específico.</span><span class="sxs-lookup"><span data-stu-id="d2cee-221">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="d2cee-222">Verifique as [solicitações de filtro por Propriedades][DevtoolsNetworkReferenceFilterRequestsProperties] para descobrir mais palavras-chave como `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="d2cee-222">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="d2cee-223">Encaixar à esquerda no menu de comando</span><span class="sxs-lookup"><span data-stu-id="d2cee-223">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="d2cee-224">Abra o [menu de comando][DevToolsCommandMenuIndex] e execute o `Dock to left` comando para mover devtools para a esquerda do visor.</span><span class="sxs-lookup"><span data-stu-id="d2cee-224">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools encaixado à esquerda da viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="d2cee-226">Figura 13: DevTools encaixado à esquerda da viewport</span><span class="sxs-lookup"><span data-stu-id="d2cee-226">Figure 13:  DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="d2cee-227">O recurso **Dock to Left** está disponível desde o Microsoft Edge 75, mas anteriormente era acessível apenas a partir do [**menu principal**][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="d2cee-227">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [**Main Menu**][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="d2cee-228">O novo recurso no Microsoft Edge 83 é que agora você pode acessar esse recurso no menu de comando.</span><span class="sxs-lookup"><span data-stu-id="d2cee-228">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="d2cee-229">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-229">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="d2cee-230">Chromium problema [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="d2cee-230">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="d2cee-231">O painel auditorias agora é o painel Lighthouse</span><span class="sxs-lookup"><span data-stu-id="d2cee-231">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="d2cee-232">A equipe do DevTools freqüentemente tem comentários dos desenvolvedores da Web que, enquanto era possível executar o [Lighthouse][GithubGoogleChromeLighthouse] do devtools, quando eles tentavam não puderam localizar o painel "Lighthouse", portanto, o painel **auditorias** agora é o painel **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="d2cee-232">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="O painel Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="d2cee-234">Figura 14: painel de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="d2cee-234">Figure 14:  The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="d2cee-235">O painel **Lighthouse** fornece links para conteúdo hospedado em websites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="d2cee-235">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="d2cee-236">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e todos os dados que eles podem coletar.</span><span class="sxs-lookup"><span data-stu-id="d2cee-236">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="d2cee-237">Excluir todas as substituições locais em uma pasta</span><span class="sxs-lookup"><span data-stu-id="d2cee-237">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="d2cee-238">Depois de configurar **substituições locais** , você pode clicar com o botão direito do mouse em uma pasta e selecionar a opção novo **excluir tudo substitui** para excluir todas as substituições locais nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="d2cee-238">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Excluir todas as substituições" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="d2cee-240">Figura 15: excluir todas as substituições</span><span class="sxs-lookup"><span data-stu-id="d2cee-240">Figure 15:  Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-241">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-241">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="d2cee-242">Chromium problema [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="d2cee-242">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="d2cee-243">Interface do usuário de tarefas longa atualizada</span><span class="sxs-lookup"><span data-stu-id="d2cee-243">Updated Long tasks UI</span></span>  

<span data-ttu-id="d2cee-244">Uma **tarefa longa** é o código JavaScript que monopolizes o thread principal há muito tempo, fazendo com que uma página da Web congele.</span><span class="sxs-lookup"><span data-stu-id="d2cee-244">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="d2cee-245">Você foi capaz de [Visualizar tarefas longas no painel de desempenho][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] durante um período de tempo, mas no Microsoft Edge 83 a interface do usuário de visualização de tarefa longa no painel desempenho foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="d2cee-245">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="d2cee-246">A parte de tarefa longa de uma tarefa está agora colorida com um plano de fundo vermelho listrado.</span><span class="sxs-lookup"><span data-stu-id="d2cee-246">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="A nova interface do usuário de tarefa longa" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="d2cee-248">Figura 16: a nova interface do usuário longa da tarefa</span><span class="sxs-lookup"><span data-stu-id="d2cee-248">Figure 16:  The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="d2cee-249">Envie seus comentários aplicando um [tweet][PostTweetEdgeDevTools] ou clicando no ícone [enviar comentários](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="d2cee-249">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="d2cee-250">Chromium problema [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="d2cee-250">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="d2cee-251">Suporte a ícones mascaráveis no painel manifesto</span><span class="sxs-lookup"><span data-stu-id="d2cee-251">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="d2cee-252">O Android Oreo introduziu ícones adaptáveis, que exibem ícones do aplicativo em uma variedade de formas em diferentes modelos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2cee-252">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="d2cee-253">**Ícones Mascaráveis** são um novo formato de ícone que dão suporte a ícones adaptáveis, que permitem que você verifique se o ícone do [PWA][PprgressiveWebAppsChromiumIndex] tem uma boa aparência em dispositivos que dão suporte ao padrão de ícones mascaráveis.</span><span class="sxs-lookup"><span data-stu-id="d2cee-253">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="d2cee-254">Habilite a caixa de seleção **Mostrar apenas a área de segurança mínima para ícones mascaráveis** no painel **manifesto** para verificar se o ícone mascarable tem uma boa aparência em dispositivos Android do Oreo.</span><span class="sxs-lookup"><span data-stu-id="d2cee-254">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="A caixa de seleção Mostrar apenas a área de segurança mínima para ícones mascaráveis" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="d2cee-256">Figura 17: a caixa de seleção **Mostrar apenas a área de segurança mínima para ícones mascaráveis**</span><span class="sxs-lookup"><span data-stu-id="d2cee-256">Figure 17:  The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="d2cee-257">Este recurso foi iniciado no Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="d2cee-257">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="d2cee-258">As atualizações abordadas aqui no Microsoft Edge 83 não foram abordadas nas novidades do [devtools (Microsoft edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="d2cee-258">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="d2cee-259">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d2cee-259">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="d2cee-260">Se você estiver no Windows ou no macOS, considere o uso dos [canais da visualização do Microsoft Edge][MicrosoftEdgePreviewChannels] como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="d2cee-260">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="d2cee-261">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="d2cee-261">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="d2cee-262">Como entrar em contato com o Microsoft Edge DevTools equipe</span><span class="sxs-lookup"><span data-stu-id="d2cee-262">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Novo problema-MicrosoftDocs/Edge-Developer-GitHub"  
[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de visualização do Microsoft Edge"  
[TheWebWeWant]: https://webwewant.fyi "A Web que queremos"  

[WhatsNew81]: ../01/devtools.md "O que há de novo no DevTools (Microsoft Edge 81) | Documentos da Microsoft"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Alterar as cores com o seletor de cores | Documentos da Microsoft"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Alterar o posicionamento no menu principal | Documentos da Microsoft"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Exibir atividade principal do thread | Documentos da Microsoft"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analisar o desempenho de renderização com a guia renderização | Documentos da Microsoft"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicativos Web progressivos no Windows | Documentos da Microsoft"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introdução à depuração remota de dispositivos Windows 10 | Documentos da Microsoft"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Pontos de interrupção de linha de código-como pausar um código com pontos de interrupção no Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitações por Propriedades-referência de análise de rede | Documentos da Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configurações-personalizar o Microsoft Edge DevTools | Documentos da Microsoft"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Visão geral do Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Ferramentas remotas para Microsoft Edge (beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Atualização em lançamentos de canais estáveis para o Microsoft Edge"

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de cegueira para cor"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemplo de código dependente de localidade"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools não são compatíveis com a WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: adicionar suporte a DevTools para simulação de deficiência visual de cor"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: apresentar ' Dock to Left ' usando o menu de comandos"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: solicitação de recurso: botão para excluir todas as substituições locais"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: guia Propriedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: suporte para a depuração COOP/COEP no DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: atualizar as métricas de desempenho na linha do tempo do DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: adicionar a interface do usuário para emular a localidade"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: aprimorar as cores dos pontos de interrupção"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: o modo de exibição de configurações é difícil de descobrir"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: atualização do componente da barra de atualizações"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP e COEP explicou-política do Opener entre origens"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP e COEP explicou-política de incorporação de várias origens"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Repositório do GitHub Lighthouse"  

> [!NOTE]
> <span data-ttu-id="d2cee-303">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d2cee-303">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d2cee-304">A página original é encontrada [aqui](https://developers.google.com/web/updates/2020/03/devtools/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d2cee-304">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d2cee-306">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d2cee-306">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
