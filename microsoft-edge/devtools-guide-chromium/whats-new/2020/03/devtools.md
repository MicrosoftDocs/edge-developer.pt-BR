---
description: Emular deficiências de visão de cor, Doca para a esquerda no Menu de Comando e muito mais.
title: Novidades no DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e5fa4b066e47b0779fcdf2b3e814c598e9615ccf
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564949"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a><span data-ttu-id="eb55d-104">Novidades no DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="eb55d-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="eb55d-105">Seguindo o cronograma Chromium, estamos ajustando nossa agenda para os próximos lançamentos Microsoft Edge e cancelando a versão Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="eb55d-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="eb55d-106">Confira nossa [postagem de blog][WindowsBlogStableRelease] para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="eb55d-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="eb55d-107">Aqui estão os novos recursos disponíveis no DevTools no Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="eb55d-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="eb55d-108">Comunicados da equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eb55d-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="eb55d-109">As seções a seguir são uma lista de comunicados que você pode ter perdido da equipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb55d-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="eb55d-110">Confira os comunicados para experimentar novos recursos no DevTools, Microsoft Visual Studio Extensões de Código e muito mais.</span><span class="sxs-lookup"><span data-stu-id="eb55d-110">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="eb55d-111">Para ficar atualizado sobre todos os recursos mais recentes e maiores em suas ferramentas de desenvolvedor, baixe os canais Microsoft Edge [de][MicrosoftEdgePreviewChannels] visualização e [siga-nos no Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="eb55d-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a><span data-ttu-id="eb55d-112">Depuração remota Microsoft Edge em Windows 10 Dispositivos</span><span class="sxs-lookup"><span data-stu-id="eb55d-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="eb55d-113">O [aplicativo Ferramentas Remotas Microsoft Edge \(Beta\)][RemoteTools] agora está disponível [no][MicrosoftStore]Microsoft Store .</span><span class="sxs-lookup"><span data-stu-id="eb55d-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="eb55d-114">Usando este aplicativo, que estende o Portal de Dispositivos do [Windows][WindowsUwpDebugTestPerfDevicePortal], você pode se conectar da instância do Microsoft Edge em execução em sua máquina de desenvolvimento a um dispositivo Windows 10 remoto, exibir uma lista de destinos \(todas as guias no Microsoft Edge e [PWAs][ProgressiveWebAppsChromiumIndex] abertas no dispositivo Windows 10\) e usar o DevTools em sua máquina de desenvolvimento em um destino em execução no dispositivo Windows 10 remoto.</span><span class="sxs-lookup"><span data-stu-id="eb55d-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, display a list of targets \(all tabs in Microsoft Edge and [PWAs][ProgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="O aplicativo Ferramentas Remotas Microsoft Edge (Beta) disponível no Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="eb55d-116">O [aplicativo Ferramentas Remotas Microsoft Edge (Beta)][RemoteTools] disponível no [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="eb55d-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-117">Leia nosso guia para configurar seu dispositivo Windows 10 e sua máquina de desenvolvimento [para depuração remota.][DevtoolsRemoteDebuggingWindows]</span><span class="sxs-lookup"><span data-stu-id="eb55d-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="eb55d-118">Deixe-nos saber sobre sua experiência de depuração remota [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <a name="new-ways-to-access-settings"></a><span data-ttu-id="eb55d-119">Novas maneiras de acessar Configurações</span><span class="sxs-lookup"><span data-stu-id="eb55d-119">New ways to access Settings</span></span>  

<span data-ttu-id="eb55d-120">Há várias configurações para o DevTools que você pode personalizar para fazer com que o DevTools pareça, sinta e trabalhe da maneira que você precisa.</span><span class="sxs-lookup"><span data-stu-id="eb55d-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="eb55d-121">No Microsoft Edge 83, acessar [Configurações][DevtoolsCustomizeIndexSettings] no DevTools agora é muito mais fácil.</span><span class="sxs-lookup"><span data-stu-id="eb55d-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span>  <span data-ttu-id="eb55d-122">Abra Configurações com o ícone de engrenagem ao lado de Alertas de Console e o menu principal.</span><span class="sxs-lookup"><span data-stu-id="eb55d-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="O ícone de engrenagem abre Configurações no DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="eb55d-124">O ícone de engrenagem **abre Configurações** no DevTools</span><span class="sxs-lookup"><span data-stu-id="eb55d-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-125">Você também pode abrir o [Configurações][DevtoolsCustomizeIndexSettings] menu **principal** em **Mais ferramentas.**</span><span class="sxs-lookup"><span data-stu-id="eb55d-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menu Principal > mais ferramentas > Configurações" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="eb55d-127">**Menu Principal**  >  **Mais ferramentas**  >  **Configurações**</span><span class="sxs-lookup"><span data-stu-id="eb55d-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-128">Chromium problema [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="eb55d-128">Chromium issue [#1050855][CR1050855]</span></span>

### <a name="new-and-improved-infobars"></a><span data-ttu-id="eb55d-129">Infobars novos e aprimorados</span><span class="sxs-lookup"><span data-stu-id="eb55d-129">New and improved infobars</span></span>

<span data-ttu-id="eb55d-130">As barras de notificação informacional \(infobars\) no DevTools agora têm uma aparência aprimorada e mais funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="eb55d-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="eb55d-131">No Microsoft Edge 83, as barras de informações são mais fáceis de ler e fornecer botões para que você possa tomar a ação relevante imediatamente.</span><span class="sxs-lookup"><span data-stu-id="eb55d-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barra de informações para imprimir bastante um arquivo minificado no Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="eb55d-133">Barra de informações para impressão de um arquivo minificado na Microsoft Edge Versão 83</span><span class="sxs-lookup"><span data-stu-id="eb55d-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-134">Chromium problema [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="eb55d-134">Chromium issue [#1056348][CR1056348]</span></span>

### <a name="navigate-the-color-picker-with-your-keyboard"></a><span data-ttu-id="eb55d-135">Navegue pelo Se picker de cores com o teclado</span><span class="sxs-lookup"><span data-stu-id="eb55d-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="eb55d-136">O [Selador de][DevtoolsCssReferenceColorPicker] Cores é uma GUI no painel [Elementos][DevtoolsCssIndex] para alterações `color` e `background-color` declarações.</span><span class="sxs-lookup"><span data-stu-id="eb55d-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="eb55d-137">Nas versões anteriores Microsoft Edge, você não era capaz de navegar na seção **Sombreamentos** do [Selador][DevtoolsCssReferenceColorPicker] de Cores com o teclado.</span><span class="sxs-lookup"><span data-stu-id="eb55d-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Agora você pode usar o teclado para mover o seletor na seção Sombreamentos do Seletor de Cores" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="eb55d-139">Agora você pode usar o teclado para mover o seletor na seção **Sombreamentos** do [Seletor de Cores][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="eb55d-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-140">No Microsoft Edge 83, agora você pode usar o teclado para mover o seletor na seção **Sombreamentos** do Seletor de Cores.</span><span class="sxs-lookup"><span data-stu-id="eb55d-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="eb55d-141">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="eb55d-141">Chromium issue [#963183][CR963183]</span></span>  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a><span data-ttu-id="eb55d-142">A guia Propriedades agora é preenchida após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="eb55d-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="eb55d-143">No Microsoft Edge 81 e anteriormente, a **guia Propriedades** no painel [Elementos][DevtoolsCssIndex] foi interrompida por atções de página.</span><span class="sxs-lookup"><span data-stu-id="eb55d-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="eb55d-144">Quando você atualizeu a página, a **guia Propriedades** não preencheu as propriedades do elemento selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="eb55d-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="No Microsoft Edge 81 e anterior, a guia Propriedades estava em branco após uma atualização de página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="eb55d-146">No Microsoft Edge 81 e anterior, a **guia Propriedades** estava em branco após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="eb55d-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-147">No Microsoft Edge 83, agora você pode exibir as propriedades do elemento selecionado no momento após uma atualização de página na **guia Propriedades.**</span><span class="sxs-lookup"><span data-stu-id="eb55d-147">In Microsoft Edge 83, you are now able to display the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="No Microsoft Edge 83, a guia Propriedades exibe as propriedades do elemento selecionado no momento após uma atualização de página" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="eb55d-149">No Microsoft Edge 83, a guia **Propriedades** exibe as propriedades do elemento selecionado no momento após uma atualização de página</span><span class="sxs-lookup"><span data-stu-id="eb55d-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-150">Chromium problema [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="eb55d-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a><span data-ttu-id="eb55d-151">Use as teclas de seta para rolar na ferramenta Alterações</span><span class="sxs-lookup"><span data-stu-id="eb55d-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="eb55d-152">A **ferramenta Changes** rastreia todas as alterações feitas em CSS ou JavaScript no DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb55d-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="eb55d-153">Você pode usar a ferramenta **Alterações para** exibir rapidamente todas as alterações e levá-los de volta ao seu editor/IDE.</span><span class="sxs-lookup"><span data-stu-id="eb55d-153">You are able to use the **Changes tool** to quickly display all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="eb55d-154">Para abrir a **ferramenta Alterações,** selecione `Ctrl` + `Shift` + `P` no DevTools para abrir o [Menu de Comando][DevtoolsCommandMenuIndex] e digite `changes` .</span><span class="sxs-lookup"><span data-stu-id="eb55d-154">To open the **Changes tool**, select `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevtoolsCommandMenuIndex] and type `changes`.</span></span>  <span data-ttu-id="eb55d-155">escolha e execute o **comando Mostrar Alterações** para abrir a ferramenta **Alterações** na gaveta DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb55d-155">choose and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="eb55d-156">Quando você fez uma alteração em um arquivo minificado, a ferramenta **Changes** permite que você role horizontalmente para exibir todo o código minificado.</span><span class="sxs-lookup"><span data-stu-id="eb55d-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to display all of your minified code.</span></span>  <span data-ttu-id="eb55d-157">A partir Microsoft Edge 83, agora você pode rolar horizontalmente usando as teclas de seta no teclado.</span><span class="sxs-lookup"><span data-stu-id="eb55d-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de seta para exibir seu código minificado na ferramenta Alterações" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="eb55d-159">No Microsoft Edge 83, você pode rolar horizontalmente com as teclas de seta para exibir as alterações feitas no código minificado na **ferramenta Alterações**</span><span class="sxs-lookup"><span data-stu-id="eb55d-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to display the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-160">Se você usar leitores de tela ou o teclado para navegar [][PostTweetEdgeDevTools] ao redor do DevTools, envie seus comentários tuitando para nós ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="eb55d-161">Chromium problema [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="eb55d-161">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="eb55d-162">Anúncios do projeto Chromium</span><span class="sxs-lookup"><span data-stu-id="eb55d-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="eb55d-163">As seções a seguir anunciam recursos adicionais disponíveis no Microsoft Edge 83 que foram contribuídos para o projeto de Chromium de código aberto.</span><span class="sxs-lookup"><span data-stu-id="eb55d-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <a name="emulate-vision-deficiencies"></a><span data-ttu-id="eb55d-164">Emular deficiências visuais</span><span class="sxs-lookup"><span data-stu-id="eb55d-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="eb55d-165">Abra a [guia Renderização][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTool] e use o novo recurso **emular** deficiências de visão para ter uma ideia melhor de como as pessoas com diferentes tipos de deficiências de visão experimentam seu site.</span><span class="sxs-lookup"><span data-stu-id="eb55d-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTool] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emulando a visão desfocado" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="eb55d-167">Emulando a visão desfocado</span><span class="sxs-lookup"><span data-stu-id="eb55d-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-168">O DevTools é capaz de emular a visão desfocado e os seguintes tipos de deficiências de visão [de cor.][ColorBlindnessTypes]</span><span class="sxs-lookup"><span data-stu-id="eb55d-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="eb55d-169">Deficiência de visão de cor</span><span class="sxs-lookup"><span data-stu-id="eb55d-169">Color Vision Deficiency</span></span> | <span data-ttu-id="eb55d-170">Detalhes</span><span class="sxs-lookup"><span data-stu-id="eb55d-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="eb55d-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="eb55d-171">Protanopia</span></span> | <span data-ttu-id="eb55d-172">A incapacidade de perceber qualquer luz vermelha.</span><span class="sxs-lookup"><span data-stu-id="eb55d-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="eb55d-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="eb55d-173">Deuteranopia</span></span> | <span data-ttu-id="eb55d-174">A incapacidade de perceber qualquer luz verde.</span><span class="sxs-lookup"><span data-stu-id="eb55d-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="eb55d-175">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="eb55d-175">Tritanopia</span></span> | <span data-ttu-id="eb55d-176">A incapacidade de perceber qualquer luz azul.</span><span class="sxs-lookup"><span data-stu-id="eb55d-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="eb55d-177">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="eb55d-177">Achromatopsia</span></span> | <span data-ttu-id="eb55d-178">A incapacidade de perceber qualquer cor, exceto os tons de cinza \(extremamente raro\).</span><span class="sxs-lookup"><span data-stu-id="eb55d-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="eb55d-179">Existem versões menos extremas dessas deficiências de visão de cor e, na verdade, são mais comuns.</span><span class="sxs-lookup"><span data-stu-id="eb55d-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="eb55d-180">Por exemplo, protanomaly é uma sensibilidade reduzida à luz vermelha (em vez de protanopia, que é a incapacidade completa de perceber a luz vermelha).</span><span class="sxs-lookup"><span data-stu-id="eb55d-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="eb55d-181">No entanto, essas deficiências de visão **omaly** não são definidas claramente: cada pessoa com essa deficiência de visão é diferente e pode ver as coisas de forma diferente \(ser capaz de perceber mais/menos das cores relevantes\).</span><span class="sxs-lookup"><span data-stu-id="eb55d-181">However, these **-omaly** vision deficiencies are not as clearly defined:  every person with such a vision deficiency is different and may see things differently \(being able to perceive more/less of the relevant colors\).</span></span>  

<span data-ttu-id="eb55d-182">Ao projetar para as simulações mais extremas no DevTools, seus aplicativos Web garantem estar acessíveis a pessoas com protanomaly, deuteranomaly, tritanomaly e achromatomaly também.</span><span class="sxs-lookup"><span data-stu-id="eb55d-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="eb55d-183">Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="eb55d-184">Chromium problema [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="eb55d-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <a name="emulate-locales"></a><span data-ttu-id="eb55d-185">Emular localidades</span><span class="sxs-lookup"><span data-stu-id="eb55d-185">Emulate locales</span></span>  

<span data-ttu-id="eb55d-186">Emular localidades definindo um local em **Sensor**  >  **Location**.</span><span class="sxs-lookup"><span data-stu-id="eb55d-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="eb55d-187">[Abra o **Menu de Comando** ][DevtoolsCommandMenuIndex] e digite para acessar a guia `Sensors` **Sensores.**  Depois de executar essas ações, o DevTools modifica a localidade padrão atual, afetando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb55d-187">[Open the **Command Menu**][DevtoolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="eb55d-188">APIs, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="eb55d-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="eb55d-189">Outras APIs JavaScript com conhecimento de localidade, `String.prototype.localeCompare` como e , por `*.prototype.toLocaleString` exemplo:</span><span class="sxs-lookup"><span data-stu-id="eb55d-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="eb55d-190">APIs DOM como `navigator.language` e</span><span class="sxs-lookup"><span data-stu-id="eb55d-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="eb55d-191">O [cabeçalho de solicitação][MDNAcceptLanguage] HTTP de idioma aceito</span><span class="sxs-lookup"><span data-stu-id="eb55d-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="eb55d-192">As atualizações `navigator.language` para e não ficam `navigator.languages` visíveis imediatamente, mas somente após a próxima atualização de página ou navegação.</span><span class="sxs-lookup"><span data-stu-id="eb55d-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="eb55d-193">As alterações no `Accept-Language` cabeçalho HTTP só são refletidas para solicitações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="eb55d-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emulando uma localidade" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="eb55d-195">Emulando uma localidade</span><span class="sxs-lookup"><span data-stu-id="eb55d-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-196">Para experimentar uma demonstração, navegue até [Locale-dependent code example][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="eb55d-196">To try a demo, navigate to [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="eb55d-197">Chromium problema [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="eb55d-197">Chromium issue [#1051822][CR1051822]</span></span>

### <a name="cross-origin-embedder-policy-coep-debugging"></a><span data-ttu-id="eb55d-198">Depuração de CoEP (Política de Embedder entre Origens)</span><span class="sxs-lookup"><span data-stu-id="eb55d-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="eb55d-199">O painel Rede agora fornece informações de depuração de Política de [Embedder][COEP] entre Origens.</span><span class="sxs-lookup"><span data-stu-id="eb55d-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="eb55d-200">A **coluna Status** agora fornece uma explicação rápida do motivo pelo qual uma solicitação foi bloqueada, bem como um link para exibir os headers dessa solicitação para depuração posterior:</span><span class="sxs-lookup"><span data-stu-id="eb55d-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitações bloqueadas na coluna **Status**" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="eb55d-202">Solicitações bloqueadas na **coluna Status**</span><span class="sxs-lookup"><span data-stu-id="eb55d-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-203">A **seção Headers de** Resposta da guia **Headers** fornece mais orientações sobre como resolver os problemas:</span><span class="sxs-lookup"><span data-stu-id="eb55d-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Mais orientações na seção Headers de Resposta" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="eb55d-205">Mais orientações na seção **Headers de** Resposta</span><span class="sxs-lookup"><span data-stu-id="eb55d-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-206">Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="eb55d-207">Chromium problema [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="eb55d-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="eb55d-208">Novos ícones para pontos de interrupção, pontos de interrupção condicional e logpoints</span><span class="sxs-lookup"><span data-stu-id="eb55d-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="eb55d-209">O painel Fontes tem novos ícones para pontos de interrupção, pontos de interrupção condicionais e pontos de log:</span><span class="sxs-lookup"><span data-stu-id="eb55d-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="eb55d-210">Pontos de interrupção \(</span><span class="sxs-lookup"><span data-stu-id="eb55d-210">Breakpoints \(</span></span>![Ponto de interrupção](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="eb55d-212">\) são representados por círculos vermelhos.</span><span class="sxs-lookup"><span data-stu-id="eb55d-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="eb55d-213">Pontos de interrupção condicionais \(</span><span class="sxs-lookup"><span data-stu-id="eb55d-213">Conditional Breakpoints \(</span></span>![Ponto de interrupção condicional](../../media/2020/03/conditional.msft.png)<span data-ttu-id="eb55d-215">\) são representados por círculos meio-brancos vermelhos.</span><span class="sxs-lookup"><span data-stu-id="eb55d-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="eb55d-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="eb55d-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="eb55d-218">\) são representados por círculos vermelhos com ícones de Console.</span><span class="sxs-lookup"><span data-stu-id="eb55d-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="eb55d-219">A motivação para os novos ícones era tornar a interface do usuário mais consistente com outras ferramentas de depuração de GUI \(que normalmente são pontos de interrupção de cor vermelho\) e facilitar a distinção entre os três recursos rapidamente.</span><span class="sxs-lookup"><span data-stu-id="eb55d-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="eb55d-220">Chromium problema [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="eb55d-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a><span data-ttu-id="eb55d-221">Exibir solicitações de rede que configuram um caminho de cookie específico</span><span class="sxs-lookup"><span data-stu-id="eb55d-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="eb55d-222">Use a nova `cookie-path` palavra-chave de filtro na **ferramenta Rede** para se concentrar nas solicitações de rede que definiram um caminho de [cookie específico.][MDNCookiePath]</span><span class="sxs-lookup"><span data-stu-id="eb55d-222">Use the new `cookie-path` filter keyword in the **Network** tool to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="eb55d-223">Confira [Solicitações de filtro por propriedades][DevtoolsNetworkReferenceFilterRequestsProperties] para descobrir mais palavras-chave como `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="eb55d-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <a name="dock-to-left-from-the-command-menu"></a><span data-ttu-id="eb55d-224">Doca para a esquerda no Menu de Comando</span><span class="sxs-lookup"><span data-stu-id="eb55d-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="eb55d-225">Abra o [Menu de Comando][DevtoolsCommandMenuIndex] e execute o comando para mover `Dock to left` DevTools para a esquerda do seu viewport.</span><span class="sxs-lookup"><span data-stu-id="eb55d-225">Open the [Command Menu][DevtoolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools encaixado à esquerda do viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="eb55d-227">DevTools encaixado à esquerda do viewport</span><span class="sxs-lookup"><span data-stu-id="eb55d-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="eb55d-228">O **recurso Dock para a** esquerda está disponível desde o Microsoft Edge 75, mas antes só era acessível no Menu [Principal][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="eb55d-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="eb55d-229">O novo recurso no Microsoft Edge 83 é que agora você pode acessar esse recurso no Menu de Comando.</span><span class="sxs-lookup"><span data-stu-id="eb55d-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="eb55d-230">Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="eb55d-231">Chromium problema [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="eb55d-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a><span data-ttu-id="eb55d-232">O painel Auditorias agora é o painel do Farol</span><span class="sxs-lookup"><span data-stu-id="eb55d-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="eb55d-233">A equipe do DevTools frequentemente recebia comentários dos desenvolvedores da Web que, embora fosse possível executar [o Farol][GithubGoogleChromeLighthouse] do DevTools, ao experimentá-lo, eles não conseguiam encontrar o painel "Farol", portanto, o painel **Auditorias** agora é o painel **do Farol.**</span><span class="sxs-lookup"><span data-stu-id="eb55d-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="O painel do Farol" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="eb55d-235">O painel do Farol</span><span class="sxs-lookup"><span data-stu-id="eb55d-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="eb55d-236">O **painel do Farol** fornece links para conteúdo hospedado em sites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="eb55d-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="eb55d-237">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e os dados que eles podem coletar.</span><span class="sxs-lookup"><span data-stu-id="eb55d-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <a name="delete-all-local-overrides-in-a-folder"></a><span data-ttu-id="eb55d-238">Excluir todas as Substituições Locais em uma pasta</span><span class="sxs-lookup"><span data-stu-id="eb55d-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="eb55d-239">Depois de \*\*\*\* configurar Substituições Locais, você pode passar o mouse em um diretório, abrir o menu contextual \(clique com o botão direito do mouse\) e escolha a nova opção **Excluir** todas as substituições locais para excluir todas as Substituições Locais nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="eb55d-239">After setting up **Local Overrides** you may hover on a directory, open the contextual menu \(right-click\), and choose the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Excluir todas as substituições" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="eb55d-241">Excluir todas as substituições</span><span class="sxs-lookup"><span data-stu-id="eb55d-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-242">Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="eb55d-243">Chromium problema [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="eb55d-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <a name="updated-long-tasks-ui"></a><span data-ttu-id="eb55d-244">Interface do usuário de tarefas longas atualizadas</span><span class="sxs-lookup"><span data-stu-id="eb55d-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="eb55d-245">Uma **Tarefa Longa** é um código JavaScript que monopoliza o thread principal por muito tempo, fazendo com que uma página da Web seja paralisada.</span><span class="sxs-lookup"><span data-stu-id="eb55d-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="eb55d-246">Você foi capaz [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] de visualizar tarefas longas no painel Desempenho há algum tempo, mas, no Microsoft Edge 83, a interface do usuário de visualização de Tarefas Longas no painel Desempenho foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="eb55d-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="eb55d-247">A parte Tarefa Longa de uma tarefa agora é colorida com um plano de fundo vermelho listrado.</span><span class="sxs-lookup"><span data-stu-id="eb55d-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="A nova interface do usuário de tarefa longa" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="eb55d-249">A nova interface do usuário de tarefa longa</span><span class="sxs-lookup"><span data-stu-id="eb55d-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="eb55d-250">Envie seus comentários [tuitando][PostTweetEdgeDevTools] ou clicando no ícone [Enviar Comentários!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="eb55d-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="eb55d-251">Chromium problema [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="eb55d-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <a name="maskable-icon-support-in-the-manifest-pane"></a><span data-ttu-id="eb55d-252">Suporte a ícones mascaradas no painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="eb55d-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="eb55d-253">O Android Oreo introduziu ícones adaptáveis, que exibem ícones de aplicativo em uma variedade de formas em diferentes modelos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb55d-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="eb55d-254">**Ícones que podem ser mascarados** são um novo formato de ícone que suporta ícones adaptáveis, o que permite garantir que seu [ícone PWA][ProgressiveWebAppsChromiumIndex] se pareça bem em dispositivos que suportam o padrão de ícones mascarados.</span><span class="sxs-lookup"><span data-stu-id="eb55d-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][ProgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="eb55d-255">Habilita a nova Caixa de seleção Mostrar apenas \*\*\*\* a área segura mínima para **ícones mascarados** no painel Manifesto para verificar se o ícone mascaral tem boa aparência em dispositivos Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="eb55d-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Mostrar apenas a área segura mínima para a caixa de seleção ícones mascaradas" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="eb55d-257">A caixa de seleção Mostrar apenas a área segura mínima para **ícones mascarados**</span><span class="sxs-lookup"><span data-stu-id="eb55d-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="eb55d-258">Esse recurso foi lançado no Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="eb55d-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="eb55d-259">As atualizações abordadas aqui no Microsoft Edge 83 não foram abordadas em [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="eb55d-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="eb55d-260">Baixar os canais de visualização do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="eb55d-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="eb55d-261">Se você estiver no Windows ou macOS, considere usar os canais [Microsoft Edge de][MicrosoftEdgePreviewChannels] visualização como seu navegador de desenvolvimento padrão.</span><span class="sxs-lookup"><span data-stu-id="eb55d-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="eb55d-262">Os canais de visualização fornecem acesso aos recursos mais recentes do DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb55d-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="eb55d-263">Como entrar em contato com a equipe do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eb55d-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Novidades no DevTools (Microsoft Edge 81) | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../../../command-menu/index.md "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssIndex]: ../../../css/index.md "Introdução Com exibição e alteração de css | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: ../../../css/reference.md#change-colors-with-the-color-picker "Alterar cores com o selador de cores | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: ../../../customize/index.md#settings "Configurações - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: ../../../customize/placement.md#change-placement-from-the-main-menu "Alterar o posicionamento do menu principal | Microsoft Docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTool]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analisar o desempenho de renderização com a ferramenta rendering | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: ../../../evaluate-performance/reference.md#view-main-thread-activity "Exibir a atividade de thread principal | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLineCode]: ../../../javascript/breakpoints.md#line-of-code-breakpoints "Pontos de interrupção de linha de código - Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: ../../../network/reference.md#filter-requests-by-properties "Filtrar solicitações por propriedades - Referência de análise de rede | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: ../../../remote-debugging/windows.md "Introdução com a Depuração Remota Windows 10 Dispositivos | Microsoft Docs"  

[ProgressiveWebAppsChromiumIndex]: ../../../../progressive-web-apps-chromium/index.md "Aplicativos Web progressivos no Windows | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Windows Visão geral do Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Ferramentas remotas para Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canais de Visualização do Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Atualização em versões de canal estável para Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[Devtools%20Docs%20Feedback] "Novo Problema - MicrosoftDocs/edge-developer - GitHub"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Postar um Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools conta do Twitter"  
[TheWebWeWantMain]: https://webwewant.fyi "A Web Que Queremos"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de Color Blindness"  
<!-- this link must be http, not https -->  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemplo de código dependente de localidade"  

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools não são compatíveis com WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: Adicionar suporte ao DevTools para simulação de deficiência de visão colorida"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: Introduzir 'Encaixe para a Esquerda' usando o Menu de Comando"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: Solicitação de Recurso: Botão para excluir todas as substituições locais"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: Guia Propriedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: Suporte à depuração DE COOP/COEP no DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: Atualizar métricas de desempenho na Linha do Tempo do DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: adicionar interface do usuário para emular localidade"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: Melhorar as cores para pontos de interrupção"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: Configurações de exibição é difícil de descobrir"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: Atualização do componente infobar"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP e COEP explicados - Política de abridor entre origens"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP e COEP explicados - Política de embedder entre origens"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "| GitHub"  

> [!NOTE]
> <span data-ttu-id="eb55d-305">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb55d-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="eb55d-306">A página original é [encontrada](https://developer.chrome.com/blog/new-in-devtools-83) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="eb55d-306">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-83) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="eb55d-308">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb55d-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
