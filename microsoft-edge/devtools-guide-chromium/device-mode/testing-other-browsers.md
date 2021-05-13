---
description: Seu trabalho não termina com a garantia de que seu site seja executado em Microsoft Edge e Android.  Mesmo que o Modo de Dispositivo seja capaz de simular um intervalo de outros dispositivos, como iPhones, recomendamos que você confira soluções para emulação fornecidas por outros navegadores.
title: Emular e testar outros navegadores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f2ca56c2e15f578a970e6ceb84b1554bfda53862
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564277"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="emulate-and-test-other-browsers"></a><span data-ttu-id="b1ad0-105">Emular e testar outros navegadores</span><span class="sxs-lookup"><span data-stu-id="b1ad0-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="b1ad0-106">Seu trabalho não termina com a garantia de que seu site seja executado em Microsoft Edge e Android.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="b1ad0-107">Mesmo que o Modo de Dispositivo seja capaz de simular um intervalo de outros dispositivos, como iPhones, recomendamos que você confira soluções para emulação fornecidas por outros navegadores.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <a name="summary"></a><span data-ttu-id="b1ad0-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b1ad0-108">Summary</span></span>  

*   <span data-ttu-id="b1ad0-109">Quando você não tem um dispositivo específico ou deseja fazer uma verificação de ponto em algo, a melhor opção é emular o dispositivo dentro do navegador.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="b1ad0-110">Os emuladores de dispositivos e simuladores permitem que você mime seu site de desenvolvimento em um intervalo de dispositivos de sua estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="b1ad0-111">Os emuladores baseados em nuvem permitem automatizar testes de unidade para seu site em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <a name="browser-emulators"></a><span data-ttu-id="b1ad0-112">Emuladores de navegador</span><span class="sxs-lookup"><span data-stu-id="b1ad0-112">Browser emulators</span></span>  

<span data-ttu-id="b1ad0-113">Os emuladores de navegador são ótimos para testar a capacidade de resposta de um site, mas cada um deles não emula diferenças na API, no suporte CSS e em determinados comportamentos exibidos em um navegador móvel.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that is displayed on a mobile browser.</span></span>  <span data-ttu-id="b1ad0-114">Teste seu site em navegadores em execução em dispositivos reais para ter certeza de que tudo se comporta conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <a name="firefox-responsive-design-view"></a><span data-ttu-id="b1ad0-115">Exibição de design responsivo do Firefox</span><span class="sxs-lookup"><span data-stu-id="b1ad0-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="b1ad0-116">O Firefox tem uma exibição de [design][MDNResponsiveDesignMode] responsivo que incentiva você a parar de pensar em termos de dispositivos específicos e, em vez disso, explorar como seu design muda em tamanhos de tela comuns ou seu próprio tamanho arrastando as bordas.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <a name="edgehtml-emulation"></a><span data-ttu-id="b1ad0-117">Emulação edgeHTML</span><span class="sxs-lookup"><span data-stu-id="b1ad0-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="b1ad0-118">Para emular Windows Telefones, use a emulação Microsoft Edge \(EdgeHTML\) [embutida][ArchiveMicrosoftEdgeDevtoolsEmulation].</span><span class="sxs-lookup"><span data-stu-id="b1ad0-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][ArchiveMicrosoftEdgeDevtoolsEmulation].</span></span>  

<span data-ttu-id="b1ad0-119">Use [a Emulação do IE 11][Ie11DevToolsEmulation] para simular a aparência da sua página em versões mais antigas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <a name="device-emulators-and-simulators"></a><span data-ttu-id="b1ad0-120">Emuladores de dispositivos e simuladores</span><span class="sxs-lookup"><span data-stu-id="b1ad0-120">Device emulators and simulators</span></span>  

<span data-ttu-id="b1ad0-121">Simuladores de dispositivo e emuladores simulam não apenas o ambiente do navegador, mas todo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="b1ad0-122">Cada uma delas é útil para testar coisas que exigem integração do sistema operacional, por exemplo, entrada de formulário com teclados virtuais.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <a name="android-emulator"></a><span data-ttu-id="b1ad0-123">Emulador android</span><span class="sxs-lookup"><span data-stu-id="b1ad0-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="b1ad0-124">No momento, não há como instalar o Microsoft Edge em um emulador Android.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="b1ad0-125">No entanto, você pode usar o Navegador do Android, o Shell de Conteúdo Chromium e o Firefox para Android que analisaremos mais adiante neste guia.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="b1ad0-126">Chromium O Shell de Conteúdo executa o mesmo Chromium de renderização do Microsoft Edge, mas vem sem nenhum dos recursos específicos do navegador.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="b1ad0-127">O emulador android vem com o SDK do Android que você precisa baixar como parte do [Android Studio.][AndroidStudioDownload]</span><span class="sxs-lookup"><span data-stu-id="b1ad0-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="b1ad0-128">Em seguida, siga as instruções [para configurar um dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e iniciar o [emulador][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="b1ad0-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="b1ad0-129">Depois que o emulador for inicializado, escolha no ícone Navegador e teste seu site no navegador de ações antigo para Android.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-129">Once your emulator is booted, choose on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <a name="chromium-content-shell-on-android"></a><span data-ttu-id="b1ad0-130">Chromium de conteúdo no Android</span><span class="sxs-lookup"><span data-stu-id="b1ad0-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="b1ad0-131">Para instalar o shell Chromium conteúdo para Android, deixe o emulador em execução e execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="b1ad0-132">Agora você pode testar seu site com o Shell Chromium Conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <a name="firefox-on-android"></a><span data-ttu-id="b1ad0-133">Firefox no Android</span><span class="sxs-lookup"><span data-stu-id="b1ad0-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="b1ad0-134">Semelhante ao Shell de Conteúdo Chromium, você pode obter um APK para instalar o Firefox no emulador.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="b1ad0-135">[Baixe o arquivo .apk correto.][MozillaFirefoxDownload]</span><span class="sxs-lookup"><span data-stu-id="b1ad0-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="b1ad0-136">Para instalar o arquivo em um emulador aberto ou dispositivo Android conectado, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a><span data-ttu-id="b1ad0-137">Simulador do iOS</span><span class="sxs-lookup"><span data-stu-id="b1ad0-137">iOS simulator</span></span>  

<span data-ttu-id="b1ad0-138">O simulador do iOS para Mac OS X vem com Xcode, que você [instala na App Store][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="b1ad0-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="b1ad0-139">Quando terminar, saiba como trabalhar com o simulador por meio da [documentação do Desenvolvedor da Apple.][AppleSimulatorHelp]</span><span class="sxs-lookup"><span data-stu-id="b1ad0-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="b1ad0-140">Para evitar ter que abrir o Xcode sempre que quiser usar o Simulador do iOS, abra-o, passe o mouse no ícone do Simulador do iOS em seu dock, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Manter no Encaixe**.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, hover on the iOS Simulator icon in your dock, open the contextual menu \(right-click\), and choose **Keep in Dock**.</span></span>  <span data-ttu-id="b1ad0-141">Agora basta escolher o ícone sempre que precisar dele.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-141">Now just choose the icon whenever you need it.</span></span>  

###  <a name="microsoft-edge-edgehtml"></a><span data-ttu-id="b1ad0-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="b1ad0-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM moderna do IE" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="b1ad0-144">VM moderna do IE</span><span class="sxs-lookup"><span data-stu-id="b1ad0-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="b1ad0-145">Microsoft Edge \(EdgeHTML\) As Máquinas Virtuais \(VMs\) permitem que você acesse diferentes versões de EdgeHTML e IE em seu computador por meio de VirtualBox \(ou VMWare\).</span><span class="sxs-lookup"><span data-stu-id="b1ad0-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="b1ad0-146">Escolha uma [máquina virtual na página de download.][MicrosoftDeveloperEdgeVms]</span><span class="sxs-lookup"><span data-stu-id="b1ad0-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <a name="cloud-based-emulators-and-simulators"></a><span data-ttu-id="b1ad0-147">Emuladores e simuladores baseados em nuvem</span><span class="sxs-lookup"><span data-stu-id="b1ad0-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="b1ad0-148">Se você não for capaz de usar os emuladores e não tiver acesso a dispositivos reais, em seguida, os emuladores baseados em nuvem são a próxima melhor coisa.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="b1ad0-149">Uma grande vantagem dos emuladores baseados em nuvem em dispositivos reais e emuladores locais é que você é capaz de automatizar testes de unidade para seu site em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="b1ad0-150">[BrowserStack (comercial)][|::ref1::|] é o mais fácil de usar para testes manuais.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="b1ad0-151">Você seleciona um sistema operacional, seleciona a versão do navegador e o tipo de dispositivo, seleciona uma URL para navegar e ela gira uma máquina virtual hospedada com a qual você pode interagir.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="b1ad0-152">Você também pode executar vários emuladores na mesma tela, permitindo que você teste a aparência do seu aplicativo em vários dispositivos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="b1ad0-153">[O SauceLabs (comercial)][SauceLabs] permite que você execute testes de unidade dentro de um emulador, o que pode ser realmente útil para rotear um fluxo pelo seu site e assistir à gravação em vídeo disso depois em vários dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="b1ad0-154">Você também pode fazer testes manuais com seu site.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="b1ad0-155">[Device Anywhere (comercial)][AppExperience] não usa emuladores, mas dispositivos reais que você pode controlar remotamente.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="b1ad0-156">Isso é muito útil no caso em que você precisa reproduzir um problema em um dispositivo específico e pode não exibir o bug usando qualquer uma das opções nos guias anteriores.</span><span class="sxs-lookup"><span data-stu-id="b1ad0-156">This is very useful in the event where you need to reproduce a problem on a specific device and may not display the bug using any of the options in the previous guides.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b1ad0-157">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b1ad0-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[ArchiveMicrosoftEdgeDevtoolsEmulation]: /archive/microsoft-edge/legacy/developer/devtools-guide/emulation "Emulação | Microsoft Docs"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emular navegadores, tamanhos de tela e localizações GPS | Microsoft Docs"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Baixar máquinas virtuais"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Criar e gerenciar dispositivos virtuais | Desenvolvedores Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Baixar ferramentas do Android Studio e SDK | Desenvolvedores Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Executar aplicativos no | Desenvolvedores Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Experiência do aplicativo"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Ajuda do Simulador - atual | Apple"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode na Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Modo de Design Responsivo | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Baixar o Navegador firefox"  
[SauceLabs]: https://saucelabs.com "Laboratórios de Disco"  

> [!NOTE]
> <span data-ttu-id="b1ad0-171">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b1ad0-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b1ad0-172">A página original [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) é encontrada aqui e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Paulo Bakaus][PaulBakaus] \(Open Web Developer Advocate no Google | Ferramentas, Desempenho, Animação, UX\).</span><span class="sxs-lookup"><span data-stu-id="b1ad0-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b1ad0-174">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b1ad0-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
