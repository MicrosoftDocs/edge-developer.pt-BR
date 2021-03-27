---
description: Conteúdo ao vivo de depuração remota em um dispositivo Android de um computador Windows ou macOS.
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d69fd4832991826c76f47daea399bdd89e981bb4
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461210"
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
# <a name="get-started-with-remote-debugging-android-devices"></a><span data-ttu-id="838a4-104">Introdução à depuração remota de dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="838a4-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="838a4-105">Conteúdo ao vivo de depuração remota em um dispositivo Android do computador Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="838a4-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="838a4-106">A página de tutorial a seguir ensina como concluir as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="838a4-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="838a4-107">Configurar seu dispositivo Android para depuração remota e descubra-o no computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="838a4-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="838a4-108">Inspecionar e depurar conteúdo ao vivo em seu dispositivo Android da máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="838a4-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="838a4-109">Conteúdo de screencast do dispositivo Android para uma instância do DevTools em sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="838a4-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="838a4-110">Não há suporte para depuração remota do aplicativo Microsoft Edge em dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="838a4-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="838a4-111">O guia a seguir é especificamente focado na depuração remota do Microsoft Edge em dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="838a4-112">Se você tiver um dispositivo macOS, siga o guia de [Depuração do Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar remotamente o Microsoft Edge em um dispositivo iOS usando o Safari.</span><span class="sxs-lookup"><span data-stu-id="838a4-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="838a4-113">Para obter mais informações sobre a ferramenta Inspetor da Web no Safari, navegue até [Safari Web Development Tools][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="838a4-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <a name="step-1-discover-your-android-device"></a><span data-ttu-id="838a4-114">Etapa 1: Descobrir seu dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="838a4-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="838a4-115">O fluxo de trabalho abaixo funciona para a maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="838a4-115">The workflow below works for most users.</span></span>  <span data-ttu-id="838a4-116">Para obter mais ajuda, navegue até [Solução de Problemas: o DevTools não está detectando a seção dispositivo Android.](#troubleshooting-devtools-is-not-detecting-the-android-device)</span><span class="sxs-lookup"><span data-stu-id="838a4-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="838a4-117">Abra a **tela Opções do** Desenvolvedor em seu Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="838a4-118">Para obter mais informações, navegue até [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="838a4-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="838a4-119">Escolha **Habilitar Depuração USB**.</span><span class="sxs-lookup"><span data-stu-id="838a4-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="838a4-120">Em sua máquina de desenvolvimento, abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="838a4-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="838a4-121">Navegue até `edge://inspect` a página no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="838a4-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="A edge://inspect no Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="838a4-123">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="838a4-123">Figure 1.</span></span>  <span data-ttu-id="838a4-124">A `edge://inspect` página no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="838a4-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="838a4-125">Conecte seu dispositivo Android diretamente à máquina de desenvolvimento usando um cabo USB.</span><span class="sxs-lookup"><span data-stu-id="838a4-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="838a4-126">Na primeira vez que você tentar se conectar, um prompt deve ser exibido sobre o DevTools detectar um dispositivo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="838a4-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="838a4-127">Aceite o **prompt de permissão Permitir Depuração USB** em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="O prompt de permissão Permitir Depuração USB em um dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="838a4-129">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="838a4-129">Figure 2.</span></span>  <span data-ttu-id="838a4-130">O prompt de permissão Permitir **Depuração USB** em um dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="838a4-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="838a4-131">Se o nome do modelo do dispositivo Android for exibido, o Microsoft Edge estabeleceu com êxito a conexão com seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="838a4-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="838a4-132">Continue até a [seção Etapa 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)</span><span class="sxs-lookup"><span data-stu-id="838a4-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a><span data-ttu-id="838a4-133">Solução de problemas: o DevTools não está detectando o dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="838a4-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="838a4-134">Use as dicas a seguir para ajudá-lo a solucionar problemas das configurações corretas para o hardware.</span><span class="sxs-lookup"><span data-stu-id="838a4-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="838a4-135">Se você estiver usando um hub USB, tente conectar seu dispositivo Android diretamente à máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="838a4-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="838a4-136">Tente desconectar o cabo USB entre o dispositivo Android e a máquina de desenvolvimento e, em seguida, conecte novamente o cabo USB.</span><span class="sxs-lookup"><span data-stu-id="838a4-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="838a4-137">Conclua a tarefa enquanto as telas do computador de desenvolvimento e Android estão desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="838a4-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="838a4-138">Certifique-se de que o cabo USB funcione.</span><span class="sxs-lookup"><span data-stu-id="838a4-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="838a4-139">Você deve ser capaz de inspecionar arquivos em seu dispositivo Android de sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="838a4-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="838a4-140">Use as dicas a seguir para ajudá-lo a verificar se o software está definido corretamente.</span><span class="sxs-lookup"><span data-stu-id="838a4-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="838a4-141">Se o computador de desenvolvimento estiver executando o Windows, tente instalar manualmente os drivers USB para seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="838a4-142">Para obter mais informações, navegue até [Instalar drivers USB OEM][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="838a4-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="838a4-143">Algumas combinações de dispositivos Windows e Android \(especialmente a Samsung\) exigem configurações adicionais.</span><span class="sxs-lookup"><span data-stu-id="838a4-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="838a4-144">Para obter mais informações, navegue até [Dispositivos DevTools não detecta dispositivo quando conectado][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="838a4-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="838a4-145">Use as dicas a seguir para ajudá-lo a solucionar problemas se o prompt **Permitir Depuração USB** não for exibido em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="838a4-146">Desconectando e, em seguida, conectando o cabo USB enquanto o DevTools está em foco no seu computador de desenvolvimento e sua tela inicial do Android está sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="838a4-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="838a4-147">O prompt será exibido se as telas do computador de desenvolvimento ou Android estão bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="838a4-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="838a4-148">Atualizando as configurações de exibição para seu dispositivo Android e máquina de desenvolvimento para que cada um nunca vá para o sono.</span><span class="sxs-lookup"><span data-stu-id="838a4-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="838a4-149">Definindo o modo USB para Android como PTP.</span><span class="sxs-lookup"><span data-stu-id="838a4-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="838a4-150">Para obter mais informações, navegue até o Galaxy S4 não mostra a caixa de diálogo [Autorizar depuração USB][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="838a4-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="838a4-151">Escolha \*\*\*\* **Revogar Autorizações de Depuração USB** na tela Opções do Desenvolvedor em seu dispositivo Android para redefini-la para um estado novo.</span><span class="sxs-lookup"><span data-stu-id="838a4-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="838a4-152">Se você encontrar uma solução que não seja mencionada nesta página ou em [Dispositivos DevTools][Stackoverflow21925992] não detectar dispositivo quando conectado ao Stack Overflow, adicione sua solução à pergunta Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="838a4-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="838a4-153">.</span><span class="sxs-lookup"><span data-stu-id="838a4-153">.</span></span>  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a><span data-ttu-id="838a4-154">Etapa 2: Depurar conteúdo em seu dispositivo Android da máquina de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="838a4-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="838a4-155">Abra o Microsoft Edge em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="838a4-156">Navegue `edge://inspect` até , o nome do modelo do dispositivo Android é exibido, seguido pelo número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="838a4-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="838a4-157">Abaixo disso, a versão do Microsoft Edge em execução no dispositivo deve ser exibida, com o número da versão entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="838a4-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="838a4-158">Cada guia abrir o Microsoft Edge obtém uma seção exclusiva.</span><span class="sxs-lookup"><span data-stu-id="838a4-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="838a4-159">Você pode interagir com essa guia de uma seção.</span><span class="sxs-lookup"><span data-stu-id="838a4-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Um dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="838a4-161">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="838a4-161">Figure 3.</span></span>  <span data-ttu-id="838a4-162">Um dispositivo remoto conectado</span><span class="sxs-lookup"><span data-stu-id="838a4-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="838a4-163">Na guia **Abrir com a caixa de texto url,** insira uma URL e escolha **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="838a4-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="838a4-164">A página abre em uma nova guia em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="838a4-165">Escolha **inspecionar** ao lado da URL que você acabou de abrir.</span><span class="sxs-lookup"><span data-stu-id="838a4-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="838a4-166">Uma nova instância do DevTools é aberta.</span><span class="sxs-lookup"><span data-stu-id="838a4-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a><span data-ttu-id="838a4-167">Mais ações: foco, atualização ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="838a4-167">More actions: focus, refresh, or close a tab</span></span>  

<span data-ttu-id="838a4-168">Escolha **a guia foco,** **recarregue**ou **feche** ao lado da guia que você deseja focalizar, atualizar ou fechar.</span><span class="sxs-lookup"><span data-stu-id="838a4-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, refresh, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Os botões para focalizar, atualizar ou fechar uma guia" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="838a4-170">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="838a4-170">Figure 4.</span></span>  <span data-ttu-id="838a4-171">Os botões para focalizar, atualizar ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="838a4-171">The buttons for focusing, refreshing, or closing a tab</span></span>  
:::image-end:::  

### <a name="inspect-elements"></a><span data-ttu-id="838a4-172">Inspecionar elementos</span><span class="sxs-lookup"><span data-stu-id="838a4-172">Inspect elements</span></span>  

<span data-ttu-id="838a4-173">Navegue até **a ferramenta Elements** da sua instância do DevTools e passe o mouse em um elemento para realça-lo no viewport do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-173">Navigate to the **Elements** tool of your DevTools instance, and hover on an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="838a4-174">Você também pode selecionar um elemento na tela do dispositivo Android para selecioná-lo na **ferramenta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="838a4-174">You may also select an element on your Android device screen to select it in the **Elements** tool.</span></span>  <span data-ttu-id="838a4-175">Escolha **Selecionar Elemento** \( Selecione Elemento \) ícone em sua instância do ![ DevTools e selecione o elemento na tela ](../media/select-element-icon.msft.png) do dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-175">Choose **Select Element** \(![Select Element](../media/select-element-icon.msft.png)\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="838a4-176">**Select Element** é desabilitado após a primeira seleção, portanto, você deve reabilitar sempre que quiser usar o recurso.</span><span class="sxs-lookup"><span data-stu-id="838a4-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <a name="screencast-your-android-screen-to-your-development-machine"></a><span data-ttu-id="838a4-177">Screencast your Android screen to your development machine</span><span class="sxs-lookup"><span data-stu-id="838a4-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="838a4-178">Escolha **Toggle Screencast** \( Toggle Screencast \) icon para exibir o conteúdo do seu dispositivo Android em sua instância ![ do ](../media/toggle-screencast-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="838a4-178">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="838a4-179">Você pode interagir com o screencast das seguintes maneiras.</span><span class="sxs-lookup"><span data-stu-id="838a4-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="838a4-180">As escolha são traduzidas em toques, disparando eventos de toque apropriados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="838a4-180">Chooses are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="838a4-181">Teclas de teclas em seu computador são enviadas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="838a4-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="838a4-182">Para simular um gesto de pinça, segure `Shift` enquanto arrasta.</span><span class="sxs-lookup"><span data-stu-id="838a4-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="838a4-183">Para rolar, use o trackpad ou a roda do mouse ou arremesse com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="838a4-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="838a4-184">Use as dicas a seguir para ajudá-lo a screencast.</span><span class="sxs-lookup"><span data-stu-id="838a4-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="838a4-185">Os screencasts exibem apenas o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="838a4-185">Screencasts only display page content.</span></span>  <span data-ttu-id="838a4-186">Partes transparentes do screencast representam interfaces de dispositivo, como a barra de endereços do Microsoft Edge, a barra de status do Android ou o teclado Android.</span><span class="sxs-lookup"><span data-stu-id="838a4-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="838a4-187">Screencasts afetam negativamente as taxas de quadros.</span><span class="sxs-lookup"><span data-stu-id="838a4-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="838a4-188">Desabilite o screencasting durante a medição de rolagem ou animações para obter uma imagem mais precisa do desempenho da sua página.</span><span class="sxs-lookup"><span data-stu-id="838a4-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="838a4-189">Se a tela do dispositivo Android for travada, o conteúdo do screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="838a4-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="838a4-190">Desbloqueie a tela do dispositivo Android para retomar automaticamente a screencast.</span><span class="sxs-lookup"><span data-stu-id="838a4-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="838a4-191">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="838a4-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opções de desenvolvedor no dispositivo | Desenvolvedor Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar drivers USB OEM | Desenvolvedores Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Ferramentas de Desenvolvimento web do Safari | Desenvolvedor apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Depuração em dispositivos móveis | Suporte brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb - Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Dispositivos DevTools não detectam dispositivos quando conectados - Estouro de Pilha"  

> [!NOTE]
> <span data-ttu-id="838a4-198">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="838a4-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="838a4-199">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="838a4-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="838a4-201">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="838a4-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
