---
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: fc7450ba2b088eee8f4005216374980096cbb067
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688140"
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

# <span data-ttu-id="334ab-103">Introdução à depuração remota de dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="334ab-103">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="334ab-104">Depurador remoto conteúdo dinâmico em um dispositivo Android a partir de seu computador com Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="334ab-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="334ab-105">Esta página do tutorial ensina a concluir as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="334ab-105">This tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="334ab-106">Configurar seu dispositivo Android para depuração remota e descobri-lo a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="334ab-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="334ab-107">Inspecione e depure conteúdo dinâmico em seu dispositivo Android a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="334ab-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="334ab-108">O conteúdo do screencast do seu dispositivo Android para uma instância do DevTools em seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="334ab-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

## <span data-ttu-id="334ab-109">Etapa 1: Descubra seu dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="334ab-109">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="334ab-110">O fluxo de trabalho abaixo funciona para a maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="334ab-110">The workflow below works for most users.</span></span>  <span data-ttu-id="334ab-111">Consulte [solução de problemas: o devtools não está detectando o dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) para obter mais ajuda.</span><span class="sxs-lookup"><span data-stu-id="334ab-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="334ab-112">Abra a tela **Opções do desenvolvedor** no seu Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="334ab-113">Para obter mais informações, consulte [Configurar opções do desenvolvedor no dispositivo](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="334ab-113">For more information, see [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="334ab-114">Selecione **habilitar a depuração USB**.</span><span class="sxs-lookup"><span data-stu-id="334ab-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="334ab-115">Na máquina de desenvolvimento, abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="334ab-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="334ab-116">Navegue até a `edge://inspect` página no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="334ab-116">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="A página edge://inspect no Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="334ab-118">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="334ab-118">Figure 1.</span></span>  <span data-ttu-id="334ab-119">A `edge://inspect` página no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="334ab-119">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="334ab-120">Conecte seu dispositivo Android diretamente ao seu computador de desenvolvimento usando um cabo USB.</span><span class="sxs-lookup"><span data-stu-id="334ab-120">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="334ab-121">Na primeira vez que tentar se conectar, você geralmente verá prompt sobre DevTools detectando um dispositivo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="334ab-121">The first time you try to connect, you usually see prompt about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="334ab-122">Aceite o prompt **Allow USB Debugging** Permission em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-122">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="O prompt permitir a depuração USB em um dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="334ab-124">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="334ab-124">Figure 2.</span></span>  <span data-ttu-id="334ab-125">O prompt **permitir a depuração USB** em um dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="334ab-125">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="334ab-126">Se você vir o nome do modelo do seu dispositivo Android, o Microsoft Edge estabelecerá a conexão com êxito com o seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="334ab-126">If you see the model name of your Android device, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="334ab-127">Vá para a [etapa 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="334ab-127">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="334ab-128">Solução de problemas: o DevTools não está detectando o dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="334ab-128">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="334ab-129">Use as dicas a seguir para ajudá-lo a solucionar os problemas de configuração correto para o seu hardware.</span><span class="sxs-lookup"><span data-stu-id="334ab-129">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="334ab-130">Se você estiver usando um hub USB, tente conectar o dispositivo Android diretamente ao seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="334ab-130">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="334ab-131">Tente desconectar o cabo USB entre seu dispositivo Android e seu computador de desenvolvimento e Conecte novamente o cabo USB.</span><span class="sxs-lookup"><span data-stu-id="334ab-131">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="334ab-132">Concluir a tarefa enquanto as telas do seu computador de desenvolvimento e Android estiverem desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="334ab-132">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="334ab-133">Verifique se o cabo USB funciona.</span><span class="sxs-lookup"><span data-stu-id="334ab-133">Make sure that your USB cable works.</span></span>  <span data-ttu-id="334ab-134">Você deve ser capaz de inspecionar arquivos em seu dispositivo Android a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="334ab-134">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="334ab-135">Use as dicas a seguir para ajudá-lo a verificar se o seu software está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="334ab-135">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="334ab-136">Se a sua máquina de desenvolvimento estiver executando o Windows, tente instalar manualmente os drivers USB do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-136">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="334ab-137">Para obter mais informações, consulte [instalar drivers USB OEM][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="334ab-137">For more information, see [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
*   <span data-ttu-id="334ab-138">Algumas combinações de dispositivos Windows e Android \ (especialmente a Samsung \) exigem configurações adicionais.</span><span class="sxs-lookup"><span data-stu-id="334ab-138">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="334ab-139">Para obter mais informações, consulte [os dispositivos DevTools não detectam o dispositivo quando conectado] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="334ab-139">For more information, see [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  

<span data-ttu-id="334ab-140">Use as dicas a seguir para ajudá-lo a solucionar problemas para não ver o prompt **permitir a depuração USB** em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-140">Use the following tips to help you troubleshoot not seeing the **Allow USB Debugging** prompt on your Android device.</span></span>  

*   <span data-ttu-id="334ab-141">Desconecte e, em seguida, reconecte o cabo USB enquanto o DevTools estiver em foco na máquina de desenvolvimento e o seu tela inicial Android estiver sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="334ab-141">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="334ab-142">Você pode não ver o prompt se as telas do seu computador de desenvolvimento ou Android estiverem bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="334ab-142">You may not see the prompt if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="334ab-143">Atualização das configurações de exibição do seu dispositivo Android e do seu computador de desenvolvimento para que cada nunca entre em suspensão.</span><span class="sxs-lookup"><span data-stu-id="334ab-143">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="334ab-144">Definindo o modo USB para Android para PTP.</span><span class="sxs-lookup"><span data-stu-id="334ab-144">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="334ab-145">Para obter mais informações, consulte [o Galaxy S4 não mostra a caixa de diálogo autorizar a depuração de USB][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="334ab-145">For more information, see [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="334ab-146">Selecione **revogar autorizações de depuração USB** na tela **Opções do desenvolvedor** em seu dispositivo Android para redefini-lo para um estado novo.</span><span class="sxs-lookup"><span data-stu-id="334ab-146">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="334ab-147">Se você encontrar uma solução que não seja mencionada nesta página ou em [DevTools dispositivos não detectam o dispositivo quando conectado] [StackOverflowDevicesNotDetected] no estouro de pilha, adicione sua solução à pergunta de estouro de pilha.</span><span class="sxs-lookup"><span data-stu-id="334ab-147">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="334ab-148">!</span><span class="sxs-lookup"><span data-stu-id="334ab-148">!</span></span>  

## <span data-ttu-id="334ab-149">Etapa 2: depurar o conteúdo do seu dispositivo Android a partir de seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="334ab-149">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="334ab-150">Abra o Microsoft Edge em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-150">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="334ab-151">Na `edge://inspect` página, você vê o nome do modelo do seu dispositivo Android, seguido do número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="334ab-151">From the `edge://inspect` page, you see the model name of your Android device, followed by the device serial number.</span></span>  <span data-ttu-id="334ab-152">Abaixo disso, você deve ver a versão do Microsoft Edge em execução no dispositivo, com o número de versão entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="334ab-152">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="334ab-153">Cada guia aberta do Microsoft Edge Obtém uma seção exclusiva.</span><span class="sxs-lookup"><span data-stu-id="334ab-153">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="334ab-154">Você pode interagir com essa guia em uma seção.</span><span class="sxs-lookup"><span data-stu-id="334ab-154">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Um dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="334ab-156">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="334ab-156">Figure 3.</span></span>  <span data-ttu-id="334ab-157">Um dispositivo remoto conectado</span><span class="sxs-lookup"><span data-stu-id="334ab-157">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="334ab-158">Na **guia abrir com a** caixa de texto URL, insira uma URL e, em seguida, selecione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="334ab-158">In the **Open tab with url** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="334ab-159">A página é aberta em uma nova guia em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-159">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="334ab-160">Selecione **inspecionar** ao lado da URL que você acabou de abrir.</span><span class="sxs-lookup"><span data-stu-id="334ab-160">Select **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="334ab-161">Uma nova instância de DevTools é aberta.</span><span class="sxs-lookup"><span data-stu-id="334ab-161">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="334ab-162">Mais ações: focalizar, recarregar ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="334ab-162">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="334ab-163">Selecione a **guia foco**, **recarregar**ou **Fechar** ao lado da guia que você deseja focalizar, recarregar ou fechar.</span><span class="sxs-lookup"><span data-stu-id="334ab-163">Select **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Os botões para enfocar, recarregar ou fechar uma guia" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="334ab-165">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="334ab-165">Figure 4.</span></span>  <span data-ttu-id="334ab-166">Os botões para enfocar, recarregar ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="334ab-166">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="334ab-167">Inspecionar elementos</span><span class="sxs-lookup"><span data-stu-id="334ab-167">Inspect elements</span></span>  

<span data-ttu-id="334ab-168">Vá para o painel **elementos** da sua instância do devtools e passe o mouse sobre um elemento para realçá-lo na viewport do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="334ab-169">Você também pode selecionar um elemento na tela do seu dispositivo Android para selecioná-lo no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="334ab-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="334ab-170">Selecione **selecionar elemento** ![ selecione ][ImageSelectElementIcon] o ícone do elemento na sua instância do devtools e selecione o elemento na tela do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="334ab-171">**Selecione o elemento** está desabilitado após a primeira seleção, portanto, você deve reativá-lo toda vez que quiser usar o recurso.</span><span class="sxs-lookup"><span data-stu-id="334ab-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="334ab-172">Screencast sua tela do Android para o seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="334ab-172">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="334ab-173">Selecione **alternar** ![ o ícone de botão de alternância do screencast ][ImageToggleScreencastIcon] para exibir o conteúdo do seu dispositivo Android em sua instância do devtools.</span><span class="sxs-lookup"><span data-stu-id="334ab-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="334ab-174">Você pode interagir com o screencast da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="334ab-174">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="334ab-175">Os cliques são convertidos em toques, disparando eventos de toque apropriados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="334ab-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="334ab-176">Os pressionamentos de teclas do computador são enviados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="334ab-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="334ab-177">Para simular um gesto de pinçagem, mantenha pressionado `Shift` enquanto arrasta.</span><span class="sxs-lookup"><span data-stu-id="334ab-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="334ab-178">Para rolar, use a trackpad ou a roda do mouse, ou Fling com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="334ab-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="334ab-179">Use as dicas a seguir para ajudá-lo a screencasts.</span><span class="sxs-lookup"><span data-stu-id="334ab-179">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="334ab-180">Screencasts exibem apenas o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="334ab-180">Screencasts only display page content.</span></span>  <span data-ttu-id="334ab-181">Partes transparentes do screencast representam interfaces de dispositivos, como a barra de endereços do Microsoft Edge, a barra de status do Android ou o teclado Android.</span><span class="sxs-lookup"><span data-stu-id="334ab-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="334ab-182">Os screencasts afetam negativamente as tarifas de quadro.</span><span class="sxs-lookup"><span data-stu-id="334ab-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="334ab-183">Desabilite o screencast enquanto estiver medindo rolagens ou animações para obter uma imagem mais precisa do desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="334ab-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="334ab-184">Se a tela do seu dispositivo Android for bloqueada, o conteúdo do screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="334ab-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="334ab-185">Desbloqueie a tela do seu dispositivo Android para continuar o screencast automaticamente.</span><span class="sxs-lookup"><span data-stu-id="334ab-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
<!--[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-no-targets.msft.png "Figure 1: The edge://inspect page in Microsoft Edge"  -->  
<!--[ImageAndroidPermissionPrompt]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-android-permissions-prompt.msft.png "Figure 2: The Allow USB Debugging permission prompt on an Android device"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets.msft.png "Figure 3: A connected remote device"  -->  
<!-- [ImageReload]:  /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets-buttons.msft.png "Figure 4: The buttons for focusing, reloading, or closing a tab"  -->  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  

<!-- links -->  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Instalar drivers USB OEM | Desenvolvedores Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "os dispositivos devtools não detectam o dispositivo quando o estouro da pilha está conectado"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB-troca de pilha de entusiastas Android"  

> [!NOTE]
> <span data-ttu-id="334ab-189">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="334ab-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="334ab-190">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="334ab-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="334ab-192">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="334ab-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
