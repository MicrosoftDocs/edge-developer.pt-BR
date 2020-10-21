---
description: Depuração remota do conteúdo ao vivo em um dispositivo Android de um computador com Windows ou macOS.
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c6bdb48460fb8f6ff26cbb02872e33cb50dd6e12
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125360"
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

# <span data-ttu-id="7b3d4-104">Introdução à depuração remota de dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="7b3d4-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="7b3d4-105">Depurador remoto conteúdo dinâmico em um dispositivo Android a partir de seu computador com Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="7b3d4-106">A página do tutorial a seguir ensina a concluir as ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="7b3d4-107">Configurar seu dispositivo Android para depuração remota e descobri-lo a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="7b3d4-108">Inspecione e depure conteúdo dinâmico em seu dispositivo Android a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="7b3d4-109">O conteúdo do screencast do seu dispositivo Android para uma instância do DevTools em seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="7b3d4-110">A depuração remota do aplicativo Microsoft Edge em dispositivos iOS não é suportada no momento.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="7b3d4-111">O guia a seguir é especialmente focalizado em depuração remota do Microsoft Edge em dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="7b3d4-112">Se você tiver um dispositivo macOS, siga o [Guia de depuração do Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar remotamente o Microsoft Edge em um dispositivo IOS usando o Safari.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="7b3d4-113">Para obter mais informações sobre a ferramenta Web Inspector no Safari, navegue até [ferramentas de desenvolvimento da Web do Safari][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="7b3d4-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <span data-ttu-id="7b3d4-114">Etapa 1: Descubra seu dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="7b3d4-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="7b3d4-115">O fluxo de trabalho abaixo funciona para a maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-115">The workflow below works for most users.</span></span>  <span data-ttu-id="7b3d4-116">Para obter mais ajuda, navegue até [solução de problemas: o devtools não está detectando a seção de dispositivos Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="7b3d4-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="7b3d4-117">Abra a tela **Opções do desenvolvedor** no seu Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="7b3d4-118">Para obter mais informações, navegue para [configurar as opções do desenvolvedor no dispositivo][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="7b3d4-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="7b3d4-119">Escolha **Habilitar depuração USB**.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="7b3d4-120">Na máquina de desenvolvimento, abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="7b3d4-121">Navegue até a `edge://inspect` página no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="7b3d4-123">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-123">Figure 1.</span></span>  <span data-ttu-id="7b3d4-124">A `edge://inspect` página no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7b3d4-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b3d4-125">Conecte seu dispositivo Android diretamente ao seu computador de desenvolvimento usando um cabo USB.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="7b3d4-126">Na primeira vez que você tenta se conectar, um aviso deve ser exibido sobre DevTools detectar um dispositivo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="7b3d4-127">Aceite o prompt **Allow USB Debugging** Permission em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="7b3d4-129">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-129">Figure 2.</span></span>  <span data-ttu-id="7b3d4-130">O prompt **permitir a depuração USB** em um dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="7b3d4-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b3d4-131">Se o nome do modelo do seu dispositivo Android for exibido, o Microsoft Edge estabelecerá a conexão com êxito com o seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="7b3d4-132">Vá para a seção [etapa 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .</span><span class="sxs-lookup"><span data-stu-id="7b3d4-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="7b3d4-133">Solução de problemas: o DevTools não está detectando o dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="7b3d4-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="7b3d4-134">Use as dicas a seguir para ajudá-lo a solucionar os problemas de configuração correto para o seu hardware.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="7b3d4-135">Se você estiver usando um hub USB, tente conectar o dispositivo Android diretamente ao seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="7b3d4-136">Tente desconectar o cabo USB entre seu dispositivo Android e seu computador de desenvolvimento e Conecte novamente o cabo USB.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="7b3d4-137">Concluir a tarefa enquanto as telas do seu computador de desenvolvimento e Android estiverem desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="7b3d4-138">Verifique se o cabo USB funciona.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="7b3d4-139">Você deve ser capaz de inspecionar arquivos em seu dispositivo Android a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="7b3d4-140">Use as dicas a seguir para ajudá-lo a verificar se o seu software está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="7b3d4-141">Se a sua máquina de desenvolvimento estiver executando o Windows, tente instalar manualmente os drivers USB do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="7b3d4-142">Para obter mais informações, navegue até [instalar drivers USB OEM][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="7b3d4-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="7b3d4-143">Algumas combinações de dispositivos Windows e Android \ (especialmente a Samsung \) exigem configurações adicionais.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="7b3d4-144">Para obter mais informações, acesse [devtools dispositivos não detectam o dispositivo quando conectado][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="7b3d4-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="7b3d4-145">Use as dicas a seguir para ajudá-lo a solucionar problemas se o prompt de **permissão de depuração USB** não for exibido em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="7b3d4-146">Desconecte e, em seguida, reconecte o cabo USB enquanto o DevTools estiver em foco na máquina de desenvolvimento e o seu tela inicial Android estiver sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7b3d4-147">O aviso será exibido se as telas do seu computador de desenvolvimento ou Android estiverem bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="7b3d4-148">Atualização das configurações de exibição do seu dispositivo Android e do seu computador de desenvolvimento para que cada nunca entre em suspensão.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="7b3d4-149">Definindo o modo USB para Android para PTP.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="7b3d4-150">Para obter mais informações, navegue até [Galaxy S4 não mostra a caixa de diálogo autorizar a depuração de USB][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="7b3d4-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="7b3d4-151">Escolha **revogar autorizações de depuração USB** na tela de **Opções do desenvolvedor** em seu dispositivo Android para redefini-lo para um estado novo.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="7b3d4-152">Se você encontrar uma solução que não seja mencionada nesta página ou em [dispositivos devtools não detectará o dispositivo quando conectado][Stackoverflow21925992] ao estouro de pilha, adicione a solução à pergunta de estouro de pilha.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="7b3d4-153">!</span><span class="sxs-lookup"><span data-stu-id="7b3d4-153">!</span></span>  

## <span data-ttu-id="7b3d4-154">Etapa 2: depurar o conteúdo do seu dispositivo Android a partir de seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="7b3d4-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="7b3d4-155">Abra o Microsoft Edge em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="7b3d4-156">Navegue até `edge://inspect` , o nome do modelo do seu dispositivo Android é exibido, seguido do número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="7b3d4-157">Abaixo disso, a versão do Microsoft Edge em execução no dispositivo deve ser exibida, com o número de versão entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="7b3d4-158">Cada guia aberta do Microsoft Edge Obtém uma seção exclusiva.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="7b3d4-159">Você pode interagir com essa guia em uma seção.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="7b3d4-161">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-161">Figure 3.</span></span>  <span data-ttu-id="7b3d4-162">Um dispositivo remoto conectado</span><span class="sxs-lookup"><span data-stu-id="7b3d4-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b3d4-163">Na **guia abrir com a** caixa de texto URL, insira uma URL e, em seguida, escolha **abrir**.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="7b3d4-164">A página é aberta em uma nova guia em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="7b3d4-165">Escolha **inspecionar** ao lado da URL que você acabou de abrir.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="7b3d4-166">Uma nova instância de DevTools é aberta.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="7b3d4-167">Mais ações: focalizar, recarregar ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="7b3d4-167">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="7b3d4-168">Escolha a **guia foco**, **recarregar**ou **Fechar** ao lado da guia que você deseja focalizar, recarregar ou fechar.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="7b3d4-170">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-170">Figure 4.</span></span>  <span data-ttu-id="7b3d4-171">Os botões para enfocar, recarregar ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="7b3d4-171">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="7b3d4-172">Inspecionar elementos</span><span class="sxs-lookup"><span data-stu-id="7b3d4-172">Inspect elements</span></span>  

<span data-ttu-id="7b3d4-173">Vá para o painel **elementos** da sua instância do devtools e passe o mouse sobre um elemento para realçá-lo na viewport do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-173">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="7b3d4-174">Você também pode selecionar um elemento na tela do seu dispositivo Android para selecioná-lo no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="7b3d4-174">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="7b3d4-175">Escolha **selecionar elemento** \ ( ![ selecione ][ImageSelectElementIcon] o elemento \) ícone na sua instância do devtools e selecione o elemento na tela do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-175">Choose **Select Element** \(![Select Element][ImageSelectElementIcon]\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="7b3d4-176">**Selecione o elemento** está desabilitado após a primeira seleção, portanto, você deve reativá-lo toda vez que quiser usar o recurso.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="7b3d4-177">Screencast sua tela do Android para o seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="7b3d4-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="7b3d4-178">Escolha **alternar o screencast** \ ( ![ alternar screencast ][ImageToggleScreencastIcon] \) ícone para exibir o conteúdo do seu dispositivo Android na sua instância do devtools.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-178">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="7b3d4-179">Você pode interagir com o screencast da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="7b3d4-180">Os cliques são convertidos em toques, disparando eventos de toque apropriados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-180">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="7b3d4-181">Os pressionamentos de teclas do computador são enviados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="7b3d4-182">Para simular um gesto de pinçagem, mantenha pressionado `Shift` enquanto arrasta.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="7b3d4-183">Para rolar, use a trackpad ou a roda do mouse, ou Fling com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="7b3d4-184">Use as dicas a seguir para ajudá-lo a screencasts.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="7b3d4-185">Screencasts exibem apenas o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-185">Screencasts only display page content.</span></span>  <span data-ttu-id="7b3d4-186">Partes transparentes do screencast representam interfaces de dispositivos, como a barra de endereços do Microsoft Edge, a barra de status do Android ou o teclado Android.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="7b3d4-187">Os screencasts afetam negativamente as tarifas de quadro.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="7b3d4-188">Desabilite o screencast enquanto estiver medindo rolagens ou animações para obter uma imagem mais precisa do desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="7b3d4-189">Se a tela do seu dispositivo Android for bloqueada, o conteúdo do screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="7b3d4-190">Desbloqueie a tela do seu dispositivo Android para continuar o screencast automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <span data-ttu-id="7b3d4-191">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7b3d4-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opções do desenvolvedor no dispositivo | Desenvolvedor de Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar drivers USB OEM | Desenvolvedores Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Ferramentas de desenvolvimento da Web do Safari | Desenvolvedor da Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Depuração em dispositivos móveis | Suporte Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB-troca de pilha de entusiastas Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Os dispositivos DevTools não detectam o dispositivo quando o estouro na pilha está conectado"  

> [!NOTE]
> <span data-ttu-id="7b3d4-198">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="7b3d4-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7b3d4-199">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7b3d4-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7b3d4-201">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7b3d4-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
