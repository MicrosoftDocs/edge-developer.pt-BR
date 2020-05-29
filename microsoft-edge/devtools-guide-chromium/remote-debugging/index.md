---
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611816"
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




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# <span data-ttu-id="2c7e5-103">Introdução à depuração remota de dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="2c7e5-103">Get Started with Remote Debugging Android Devices</span></span>   



<span data-ttu-id="2c7e5-104">Depurador remoto conteúdo dinâmico em um dispositivo Android a partir de seu computador com Windows ou macOS.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="2c7e5-105">Este tutorial ensina a:</span><span class="sxs-lookup"><span data-stu-id="2c7e5-105">This tutorial teaches you how to:</span></span>  

*   <span data-ttu-id="2c7e5-106">Configurar seu dispositivo Android para depuração remota e descobri-lo a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="2c7e5-107">Inspecione e depure conteúdo dinâmico em seu dispositivo Android a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="2c7e5-108">O conteúdo do screencast do seu dispositivo Android para uma instância do DevTools em seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## <span data-ttu-id="2c7e5-109">Etapa 1: Descubra seu dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="2c7e5-109">Step 1: Discover your Android device</span></span>   

<span data-ttu-id="2c7e5-110">O fluxo de trabalho abaixo funciona para a maioria dos usuários.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-110">The workflow below works for most users.</span></span>  <span data-ttu-id="2c7e5-111">Consulte [solução de problemas: o devtools não está detectando o dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) para obter mais ajuda.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="2c7e5-112">Abra a tela **Opções do desenvolvedor** no seu Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="2c7e5-113">Consulte [Configurar opções do desenvolvedor no dispositivo](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="2c7e5-113">See [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="2c7e5-114">Selecione **habilitar a depuração USB**.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="2c7e5-115">Na máquina de desenvolvimento, abra o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="2c7e5-116">[Abra o devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="2c7e5-116">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="2c7e5-117">No devtools, selecione o **menu principal** `...` e, em seguida, selecione **mais ferramentas**de  >  **dispositivos remotos**.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-117">In DevTools, select the **Main Menu** `...` then select **More tools** > **Remote devices**.</span></span>  
    
    > ##### <span data-ttu-id="2c7e5-118">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2c7e5-118">Figure 1</span></span>  
    > <span data-ttu-id="2c7e5-119">Abrindo a guia **dispositivos remotos** por meio do **menu principal**</span><span class="sxs-lookup"><span data-stu-id="2c7e5-119">Opening the **Remote Devices** tab via the **Main Menu**</span></span>  
    > <span data-ttu-id="2c7e5-120">! [Abrindo a guia dispositivos remotos por meio do menu principal] [ImageOpenRemoteDevices]</span><span class="sxs-lookup"><span data-stu-id="2c7e5-120">![Opening the Remote Devices tab via the Main Menu][ImageOpenRemoteDevices]</span></span>  

1.  <span data-ttu-id="2c7e5-121">No DevTools, abra a guia **configurações** .</span><span class="sxs-lookup"><span data-stu-id="2c7e5-121">In DevTools, open the **Settings** tab.</span></span>  

1.  <span data-ttu-id="2c7e5-122">Verifique se a caixa de seleção **descobrir dispositivos USB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-122">Make sure that the **Discover USB devices** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="2c7e5-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2c7e5-123">Figure 2</span></span>  
    > <span data-ttu-id="2c7e5-124">A caixa de seleção **descobrir dispositivos USB** está habilitada</span><span class="sxs-lookup"><span data-stu-id="2c7e5-124">The **Discover USB Devices** checkbox is enabled</span></span>  
    > <span data-ttu-id="2c7e5-125">! [A caixa de seleção descobrir dispositivos USB está habilitada] [ImageDiscoverUSBDevices]</span><span class="sxs-lookup"><span data-stu-id="2c7e5-125">![The Discover USB Devices checkbox is enabled][ImageDiscoverUSBDevices]</span></span>  

1.  <span data-ttu-id="2c7e5-126">Conecte seu dispositivo Android diretamente ao seu computador de desenvolvimento usando um cabo USB.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-126">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="2c7e5-127">Na primeira vez que você fizer isso, você normalmente verá que o DevTools detectou um dispositivo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-127">The first time you do this, you usually see that DevTools has detected an unknown device.</span></span>  <span data-ttu-id="2c7e5-128">Se você vir um ponto verde e o texto **conectado** abaixo do nome do modelo do seu dispositivo Android, o devtools estabelecerá a conexão com êxito com o seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-128">If you see a green dot and the text **Connected** below the model name of your Android device, then DevTools has successfully established the connection to your device.</span></span>  <span data-ttu-id="2c7e5-129">Vá para a [etapa 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="2c7e5-129">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  <span data-ttu-id="2c7e5-130">Se o seu dispositivo estiver aparecendo como **desconhecido**, aceite o prompt **Allow USB Debugging** Permission em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-130">If your device is showing up as **Unknown**, accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  

### <span data-ttu-id="2c7e5-131">Solução de problemas: o DevTools não está detectando o dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="2c7e5-131">Troubleshooting: DevTools is not detecting the Android device</span></span>   

<span data-ttu-id="2c7e5-132">Verifique se o seu hardware está configurado corretamente:</span><span class="sxs-lookup"><span data-stu-id="2c7e5-132">Make sure that your hardware is set up correctly:</span></span>  

*   <span data-ttu-id="2c7e5-133">Se você estiver usando um hub USB, tente conectar o dispositivo Android diretamente ao seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-133">If you are using a USB hub, try connecting your Android device directly to your development machine instead.</span></span>  
*   <span data-ttu-id="2c7e5-134">Tente desconectar o cabo USB entre seu dispositivo Android e seu computador de desenvolvimento e conecte-o novamente.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-134">Try unplugging the USB cable between your Android device and development machine, and then plugging it back in.</span></span>  <span data-ttu-id="2c7e5-135">Faça isso enquanto as telas do seu computador de desenvolvimento e Android estiverem desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-135">Do it while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="2c7e5-136">Verifique se o cabo USB funciona.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-136">Make sure that your USB cable works.</span></span>  <span data-ttu-id="2c7e5-137">Você deve ser capaz de inspecionar arquivos em seu dispositivo Android a partir de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-137">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="2c7e5-138">Verifique se o seu software está configurado corretamente:</span><span class="sxs-lookup"><span data-stu-id="2c7e5-138">Make sure that your software is set up correctly:</span></span>  

*   <span data-ttu-id="2c7e5-139">Se a sua máquina de desenvolvimento estiver executando o Windows, tente instalar manualmente os drivers USB do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-139">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="2c7e5-140">Consulte [instalar drivers USB OEM][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="2c7e5-140">See [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
    
*   <span data-ttu-id="2c7e5-141">Algumas combinações de dispositivos Windows e Android (especialmente a Samsung) exigem configuração adicional.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-141">Some combinations of Windows and Android devices (especially Samsung) require extra set up.</span></span>  <span data-ttu-id="2c7e5-142">Consulte [os dispositivos DevTools não detectam o dispositivo quando conectado] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="2c7e5-142">See [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  
    
<span data-ttu-id="2c7e5-143">Se você não vir o prompt **permitir a depuração USB** em seu dispositivo Android, tente:</span><span class="sxs-lookup"><span data-stu-id="2c7e5-143">If you do not see the **Allow USB Debugging** prompt on your Android device try:</span></span>  

*   <span data-ttu-id="2c7e5-144">Desconecte e, em seguida, reconecte o cabo USB enquanto o DevTools estiver em foco na máquina de desenvolvimento e o seu tela inicial Android estiver sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-144">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  <span data-ttu-id="2c7e5-145">Em outras palavras, às vezes o prompt não aparece quando as telas do seu computador de desenvolvimento ou Android estão bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-145">In other words, sometimes the prompt does not show up when your Android or development machine screens are locked.</span></span>
*   <span data-ttu-id="2c7e5-146">Atualização das configurações de exibição do seu dispositivo Android e do seu computador de desenvolvimento, para que eles nunca entrem em suspensão.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-146">Updating the display settings for your Android device and development machine so that they never go to sleep.</span></span>  
*   <span data-ttu-id="2c7e5-147">Definindo o modo USB para Android para PTP.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-147">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="2c7e5-148">Consulte [o Galaxy S4 não mostra a caixa de diálogo autorizar a depuração de USB][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="2c7e5-148">See [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="2c7e5-149">Selecione **revogar autorizações de depuração USB** na tela **Opções do desenvolvedor** em seu dispositivo Android para redefini-lo para um estado novo.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-149">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="2c7e5-150">Se você encontrar uma solução não mencionada nesta seção ou em [DevTools dispositivos não detecta o dispositivo quando conectado] [StackOverflowDevicesNotDetected] ou adicione uma resposta a essa pergunta de estouro de pilha</span><span class="sxs-lookup"><span data-stu-id="2c7e5-150">If you find a solution that is not mentioned in this section or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] or please add an answer to that Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="2c7e5-151">!</span><span class="sxs-lookup"><span data-stu-id="2c7e5-151">!</span></span>  

## <span data-ttu-id="2c7e5-152">Etapa 2: depurar o conteúdo do seu dispositivo Android a partir de seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="2c7e5-152">Step 2: Debug content on your Android device from your development machine</span></span>   

1.  <span data-ttu-id="2c7e5-153">Abra o Microsoft Edge em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-153">Open Microsoft Edge on your Android device.</span></span>  

1.  <span data-ttu-id="2c7e5-154">Na guia **dispositivos remotos** , selecione a guia que corresponde ao nome do modelo do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-154">In the **Remote Devices** tab, select the tab that matches your Android device model name.</span></span>  
    <span data-ttu-id="2c7e5-155">Na parte superior desta página, você verá o nome do modelo do seu dispositivo Android, seguido pelo número de série.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-155">At the top of this page, you see the model name of your Android device, followed by its serial number.</span></span>  <span data-ttu-id="2c7e5-156">Abaixo disso, você deve ver a versão do Microsoft Edge em execução no dispositivo, com o número de versão entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="2c7e5-157">Cada guia aberta do Microsoft Edge obtém sua própria seção.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-157">Each open Microsoft Edge tab gets its own section.</span></span>  <span data-ttu-id="2c7e5-158">Você pode interagir com essa guia desta seção.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-158">You may interact with that tab from this section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  <span data-ttu-id="2c7e5-159">Na caixa de texto **nova guia** , insira uma URL e, em seguida, selecione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-159">In the **New tab** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="2c7e5-160">A página é aberta em uma nova guia em seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-160">The page opens in a new tab on your Android device.</span></span>  

1.  <span data-ttu-id="2c7e5-161">Selecione **inspecionar** ao lado da URL que você acabou de abrir.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-161">Select **Inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="2c7e5-162">Uma nova instância de DevTools é aberta.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-162">A new DevTools instance opens.</span></span>  <span data-ttu-id="2c7e5-163">A versão do Microsoft Edge que está sendo executada em seu dispositivo Android determina a versão do DevTools que é aberta na máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-163">The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.</span></span>  
    <span data-ttu-id="2c7e5-164">Portanto, se o seu dispositivo Android estiver executando uma versão mais antiga do Microsoft Edge, a instância do DevTools poderá parecer muito diferente da que você está acostumado.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-164">So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.</span></span>  

### <span data-ttu-id="2c7e5-165">Mais ações: recarregar, focalizar ou fechar uma guia</span><span class="sxs-lookup"><span data-stu-id="2c7e5-165">More actions: reload, focus, or close a tab</span></span>   

<span data-ttu-id="2c7e5-166">Selecione **mais opções** `...` ao lado da guia que você deseja recarregar, enfocar ou fechar.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-166">Select **More Options** `...` next to the tab that you want to reload, focus, or close.</span></span>  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### <span data-ttu-id="2c7e5-167">Inspecionar elementos</span><span class="sxs-lookup"><span data-stu-id="2c7e5-167">Inspect elements</span></span>   

<span data-ttu-id="2c7e5-168">Vá para o painel **elementos** da sua instância do devtools e passe o mouse sobre um elemento para realçá-lo na viewport do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="2c7e5-169">Você também pode selecionar um elemento na tela do seu dispositivo Android para selecioná-lo no painel de **elementos** .</span><span class="sxs-lookup"><span data-stu-id="2c7e5-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="2c7e5-170">Selecione **selecionar** elemento ![ selecione ][ImageSelectElementIcon] o elemento na sua instância do devtools e selecione o elemento na tela do seu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="2c7e5-171">**Selecione o elemento** está desabilitado após a primeira seleção, portanto, você deve reativá-lo toda vez que quiser usar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use this feature.</span></span>  

### <span data-ttu-id="2c7e5-172">Screencast sua tela do Android para o seu computador de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="2c7e5-172">Screencast your Android screen to your development machine</span></span>   

<span data-ttu-id="2c7e5-173">Selecione **alternar screencast** ![ alternar screencast ][ImageToggleScreencastIcon] para exibir o conteúdo do seu dispositivo Android na sua instância do devtools.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="2c7e5-174">Você pode interagir com o screencast de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="2c7e5-174">You are able to interact with the screencast in multiple ways:</span></span>  

*   <span data-ttu-id="2c7e5-175">Os cliques são convertidos em toques, disparando eventos de toque apropriados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="2c7e5-176">Os pressionamentos de teclas do computador são enviados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="2c7e5-177">Para simular um gesto de pinçagem, mantenha pressionado `Shift` enquanto arrasta.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="2c7e5-178">Para rolar, use a trackpad ou a roda do mouse, ou Fling com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

<span data-ttu-id="2c7e5-179">Algumas observações sobre screencasts:</span><span class="sxs-lookup"><span data-stu-id="2c7e5-179">Some notes on screencasts:</span></span>  

*   <span data-ttu-id="2c7e5-180">Screencasts exibem apenas o conteúdo da página.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-180">Screencasts only display page content.</span></span>  <span data-ttu-id="2c7e5-181">Partes transparentes do screencast representam interfaces de dispositivos, como a barra de endereços do Microsoft Edge, a barra de status do Android ou o teclado Android.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
*   <span data-ttu-id="2c7e5-182">Os screencasts afetam negativamente as tarifas de quadro.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="2c7e5-183">Desabilite o screencast enquanto estiver medindo rolagens ou animações para obter uma imagem mais precisa do desempenho da página.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
*   <span data-ttu-id="2c7e5-184">Se a tela do seu dispositivo Android for bloqueada, o conteúdo do screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="2c7e5-185">Desbloqueie a tela do seu dispositivo Android para continuar o screencast automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-more-Tools-Remote-Devices.msft.png "Figura 1: abrindo a guia dispositivos remotos por meio do menu principal"  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.msft.png "Figura 2: a caixa de seleção descobrir dispositivos USB está habilitada"  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Instalar drivers USB OEM | Desenvolvedores Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "os dispositivos devtools não detectam o dispositivo quando o estouro da pilha está conectado"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB-troca de pilha de entusiastas Android"  

> [!NOTE]
> <span data-ttu-id="2c7e5-192">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="2c7e5-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2c7e5-193">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2c7e5-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2c7e5-195">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c7e5-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
