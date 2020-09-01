---
title: Emular e Testar Outros Navegadores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d5eb33ea4cd1224930e91898d2c711310202cfc0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984974"
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





# <span data-ttu-id="67655-103">Emular e testar outros navegadores</span><span class="sxs-lookup"><span data-stu-id="67655-103">Emulate and test other browsers</span></span>   




<span data-ttu-id="67655-104">Seu trabalho não termina com a garantia de que o seu site seja ótimo no Microsoft Edge e no Android.</span><span class="sxs-lookup"><span data-stu-id="67655-104">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="67655-105">Apesar de o modo de dispositivo poder simular uma faixa de outros dispositivos como iPhones, recomendamos que você consulte as soluções para emulação fornecidas por outros navegadores.</span><span class="sxs-lookup"><span data-stu-id="67655-105">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <span data-ttu-id="67655-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="67655-106">Summary</span></span>  

*   <span data-ttu-id="67655-107">Quando você não tiver um dispositivo em particular ou se quiser fazer uma verificação de ponto em algo, a melhor opção é emular o dispositivo diretamente dentro do navegador.</span><span class="sxs-lookup"><span data-stu-id="67655-107">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="67655-108">Emuladores e emuladores de dispositivo permitem a imitação do seu site de desenvolvimento em uma variedade de dispositivos da sua estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="67655-108">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="67655-109">Os emuladores baseados em nuvem permitem automatizar os testes de unidade do seu site em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="67655-109">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <span data-ttu-id="67655-110">Emuladores de navegador</span><span class="sxs-lookup"><span data-stu-id="67655-110">Browser emulators</span></span>  

<span data-ttu-id="67655-111">Os emuladores de navegador são ótimos para testar a capacidade de resposta de um site, mas cada um não emula diferenças na API, suporte a CSS e certos comportamentos que você vê em um navegador móvel.</span><span class="sxs-lookup"><span data-stu-id="67655-111">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that you see on a mobile browser.</span></span>  <span data-ttu-id="67655-112">Teste seu site em navegadores executados em dispositivos reais para ter certeza de que tudo se comporta conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="67655-112">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <span data-ttu-id="67655-113">Modo de exibição de design responsivo do Firefox</span><span class="sxs-lookup"><span data-stu-id="67655-113">Firefox Responsive Design View</span></span>  

<span data-ttu-id="67655-114">O Firefox tem um [modo de exibição de design responsivo][MDNResponsiveDesignMode] que incentiva você a parar de pensar em termos de dispositivos específicos e explorar como o design muda em tamanhos de tela comuns ou em seu próprio tamanho arrastando as bordas.</span><span class="sxs-lookup"><span data-stu-id="67655-114">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <span data-ttu-id="67655-115">Emulação de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="67655-115">EdgeHTML emulation</span></span>  

<span data-ttu-id="67655-116">Para emular telefones Windows, use a [emulação interna][DevToolsEdgeHtmlEmulation]do Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="67655-116">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="67655-117">Use a [emulação do IE 11][Ie11DevToolsEmulation] para simular como a sua página pode ser exibida em versões mais antigas do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="67655-117">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <span data-ttu-id="67655-118">Emuladores de dispositivo e simuladores</span><span class="sxs-lookup"><span data-stu-id="67655-118">Device emulators and simulators</span></span>  

<span data-ttu-id="67655-119">Os simuladores de dispositivo e emuladores simulam não apenas o ambiente do navegador, mas o dispositivo inteiro.</span><span class="sxs-lookup"><span data-stu-id="67655-119">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="67655-120">Cada um é útil para testar itens que exigem integração com o sistema operacional, por exemplo, entrada de formulário com teclados virtuais.</span><span class="sxs-lookup"><span data-stu-id="67655-120">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <span data-ttu-id="67655-121">Emulador Android</span><span class="sxs-lookup"><span data-stu-id="67655-121">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="67655-122">No momento, não há nenhuma maneira de instalar o Microsoft Edge em um emulador Android.</span><span class="sxs-lookup"><span data-stu-id="67655-122">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="67655-123">No entanto, você pode usar o navegador Android, o Shell de conteúdo do Chromium e o Firefox para Android, que são revisados mais adiante neste guia.</span><span class="sxs-lookup"><span data-stu-id="67655-123">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="67655-124">Chromium o Shell de conteúdo executa o mesmo mecanismo de renderização Chromium como o Microsoft Edge, mas vem sem qualquer recurso específico do navegador.</span><span class="sxs-lookup"><span data-stu-id="67655-124">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="67655-125">O emulador Android vem com o SDK do Android que você precisa baixar como parte do [Android Studio][AndroidStudioDownload].</span><span class="sxs-lookup"><span data-stu-id="67655-125">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="67655-126">Em seguida, siga as instruções para [configurar um dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e [iniciar o emulador][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="67655-126">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="67655-127">Depois que o emulador for inicializado, clique no ícone do navegador e teste o site no navegador de ações antigo para Android.</span><span class="sxs-lookup"><span data-stu-id="67655-127">Once your emulator is booted, click on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <span data-ttu-id="67655-128">Shell de conteúdo do Chromium no Android</span><span class="sxs-lookup"><span data-stu-id="67655-128">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="67655-129">Para instalar o Shell de conteúdo Chromium para Android, deixe seu emulador em execução e execute o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="67655-129">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="67655-130">Agora você pode testar seu site com o Shell de conteúdo do Chromium.</span><span class="sxs-lookup"><span data-stu-id="67655-130">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <span data-ttu-id="67655-131">Firefox no Android</span><span class="sxs-lookup"><span data-stu-id="67655-131">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="67655-132">Semelhante ao Shell de conteúdo Chromium, você pode obter um APK para instalar o Firefox no emulador.</span><span class="sxs-lookup"><span data-stu-id="67655-132">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="67655-133">[Baixe o arquivo. apk correto][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="67655-133">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="67655-134">Para instalar o arquivo em um emulador aberto ou dispositivo Android conectado, execute o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="67655-134">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <span data-ttu-id="67655-135">simulador do iOS</span><span class="sxs-lookup"><span data-stu-id="67655-135">iOS simulator</span></span>  

<span data-ttu-id="67655-136">O simulador do iOS para Mac OS X vem com o Xcode, que você [instala a partir da App Store][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="67655-136">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="67655-137">Quando terminar, aprenda a trabalhar com o simulador por meio da [documentação do desenvolvedor da Apple][AppleSimulatorHelp].</span><span class="sxs-lookup"><span data-stu-id="67655-137">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="67655-138">Para evitar ter que abrir o Xcode sempre que você quiser usar o simulador do iOS, abra-o, clique com o botão direito do mouse no ícone do simulador do iOS em seu Dock e selecione **manter no Dock**.</span><span class="sxs-lookup"><span data-stu-id="67655-138">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, then right-click the iOS Simulator icon in your dock and select **Keep in Dock**.</span></span>  <span data-ttu-id="67655-139">Agora, basta clicar nesse ícone sempre que precisar.</span><span class="sxs-lookup"><span data-stu-id="67655-139">Now just click this icon whenever you need it.</span></span>  

###  <span data-ttu-id="67655-140">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="67655-140">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM moderna do IE" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="67655-142">VM moderna do IE</span><span class="sxs-lookup"><span data-stu-id="67655-142">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="67655-143">O Microsoft Edge \ (EdgeHTML \) máquinas virtuais \ (VMs \) permitem que você acesse versões diferentes do EdgeHTML e do IE em seu computador via VirtualBox \ (ou VMWare \).</span><span class="sxs-lookup"><span data-stu-id="67655-143">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="67655-144">Escolha uma [máquina virtual na página de download][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="67655-144">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <span data-ttu-id="67655-145">Emuladores e simuladores baseados em nuvem</span><span class="sxs-lookup"><span data-stu-id="67655-145">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="67655-146">Se você não conseguir usar os emuladores e não tiver acesso a dispositivos reais, os emuladores baseados em nuvem serão a melhor coisa melhor.</span><span class="sxs-lookup"><span data-stu-id="67655-146">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="67655-147">Uma grande vantagem dos emuladores baseados em nuvem em dispositivos reais e emuladores locais é que você pode automatizar testes de unidade para o seu site em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="67655-147">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="67655-148">[BrowserStack (comercial)][|::ref1::|] é a maneira mais fácil de usar para testes manuais.</span><span class="sxs-lookup"><span data-stu-id="67655-148">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="67655-149">Selecione um sistema operacional, selecione a versão do navegador e o tipo de dispositivo, selecione uma URL para navegar e ele gira uma máquina virtual hospedada com a qual você pode interagir.</span><span class="sxs-lookup"><span data-stu-id="67655-149">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="67655-150">Você também pode executar vários emuladores na mesma tela, permitindo que você teste a aparência do seu aplicativo em vários dispositivos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="67655-150">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="67655-151">O [SauceLabs (comercial)][SauceLabs] permite que você execute testes de unidade dentro de um emulador, que podem ser muito úteis para o script de um fluxo por meio de seu site e para observar a gravação de vídeo disso posteriormente em vários dispositivos.</span><span class="sxs-lookup"><span data-stu-id="67655-151">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="67655-152">Você também pode fazer testes manuais com o seu site.</span><span class="sxs-lookup"><span data-stu-id="67655-152">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="67655-153">O [dispositivo em qualquer lugar (comercial)][AppExperience] não usa emuladores, mas dispositivos reais que você pode controlar remotamente.</span><span class="sxs-lookup"><span data-stu-id="67655-153">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="67655-154">Isso é muito útil no evento em que você precisa reproduzir um problema em um dispositivo específico e não consegue ver o erro usando qualquer uma das opções nos guias anteriores.</span><span class="sxs-lookup"><span data-stu-id="67655-154">This is very useful in the event where you need to reproduce a problem on a specific device and are not able to see the bug using any of the options in the previous guides.</span></span>  

<!--  
 


-->  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML)-emulação | Documentos da Microsoft"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emular navegadores, tamanhos de tela e locais de GPS | Documentos da Microsoft"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Baixar máquinas virtuais"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Criar e gerenciar dispositivos virtuais | Desenvolvedores Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Baixar o Android Studio e ferramentas SDK | Desenvolvedores Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Executar aplicativos no emulador Android | Desenvolvedores Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Experiência do aplicativo"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Ajuda do simulador-atual | Apple"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode na Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Modo de design responsivo | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Baixar o navegador Firefox"  
[SauceLabs]: https://saucelabs.com "Molho Labs"  

> [!NOTE]
> <span data-ttu-id="67655-168">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="67655-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="67655-169">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor The Google | Ferramentas, desempenho, animação, UX \).</span><span class="sxs-lookup"><span data-stu-id="67655-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="67655-171">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="67655-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
