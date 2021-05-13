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
# <a name="emulate-and-test-other-browsers"></a>Emular e testar outros navegadores  

Seu trabalho não termina com a garantia de que seu site seja executado em Microsoft Edge e Android.  Mesmo que o Modo de Dispositivo seja capaz de simular um intervalo de outros dispositivos, como iPhones, recomendamos que você confira soluções para emulação fornecidas por outros navegadores.  

### <a name="summary"></a>Resumo  

*   Quando você não tem um dispositivo específico ou deseja fazer uma verificação de ponto em algo, a melhor opção é emular o dispositivo dentro do navegador.  
*   Os emuladores de dispositivos e simuladores permitem que você mime seu site de desenvolvimento em um intervalo de dispositivos de sua estação de trabalho.  
*   Os emuladores baseados em nuvem permitem automatizar testes de unidade para seu site em diferentes plataformas.  

## <a name="browser-emulators"></a>Emuladores de navegador  

Os emuladores de navegador são ótimos para testar a capacidade de resposta de um site, mas cada um deles não emula diferenças na API, no suporte CSS e em determinados comportamentos exibidos em um navegador móvel.  Teste seu site em navegadores em execução em dispositivos reais para ter certeza de que tudo se comporta conforme o esperado.  

### <a name="firefox-responsive-design-view"></a>Exibição de design responsivo do Firefox  

O Firefox tem uma exibição de [design][MDNResponsiveDesignMode] responsivo que incentiva você a parar de pensar em termos de dispositivos específicos e, em vez disso, explorar como seu design muda em tamanhos de tela comuns ou seu próprio tamanho arrastando as bordas.  

### <a name="edgehtml-emulation"></a>Emulação edgeHTML  

Para emular Windows Telefones, use a emulação Microsoft Edge \(EdgeHTML\) [embutida][ArchiveMicrosoftEdgeDevtoolsEmulation].  

Use [a Emulação do IE 11][Ie11DevToolsEmulation] para simular a aparência da sua página em versões mais antigas do Internet Explorer.  

## <a name="device-emulators-and-simulators"></a>Emuladores de dispositivos e simuladores  

Simuladores de dispositivo e emuladores simulam não apenas o ambiente do navegador, mas todo o dispositivo.  Cada uma delas é útil para testar coisas que exigem integração do sistema operacional, por exemplo, entrada de formulário com teclados virtuais.  

### <a name="android-emulator"></a>Emulador android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

No momento, não há como instalar o Microsoft Edge em um emulador Android.  No entanto, você pode usar o Navegador do Android, o Shell de Conteúdo Chromium e o Firefox para Android que analisaremos mais adiante neste guia.  Chromium O Shell de Conteúdo executa o mesmo Chromium de renderização do Microsoft Edge, mas vem sem nenhum dos recursos específicos do navegador.  

O emulador android vem com o SDK do Android que você precisa baixar como parte do [Android Studio.][AndroidStudioDownload]  Em seguida, siga as instruções [para configurar um dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e iniciar o [emulador][AndroidStudioRunAppsAndroidEmulator].  
Depois que o emulador for inicializado, escolha no ícone Navegador e teste seu site no navegador de ações antigo para Android.  

#### <a name="chromium-content-shell-on-android"></a>Chromium de conteúdo no Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Para instalar o shell Chromium conteúdo para Android, deixe o emulador em execução e execute o seguinte comando.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Agora você pode testar seu site com o Shell Chromium Conteúdo.  

#### <a name="firefox-on-android"></a>Firefox no Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Semelhante ao Shell de Conteúdo Chromium, você pode obter um APK para instalar o Firefox no emulador.  

[Baixe o arquivo .apk correto.][MozillaFirefoxDownload]  

Para instalar o arquivo em um emulador aberto ou dispositivo Android conectado, execute o seguinte comando.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a>Simulador do iOS  

O simulador do iOS para Mac OS X vem com Xcode, que você [instala na App Store][MacAppStoreXcode].  

Quando terminar, saiba como trabalhar com o simulador por meio da [documentação do Desenvolvedor da Apple.][AppleSimulatorHelp]  

> [!NOTE]
> Para evitar ter que abrir o Xcode sempre que quiser usar o Simulador do iOS, abra-o, passe o mouse no ícone do Simulador do iOS em seu dock, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Manter no Encaixe**.  Agora basta escolher o ícone sempre que precisar dele.  

###  <a name="microsoft-edge-edgehtml"></a>Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM moderna do IE" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   VM moderna do IE  
:::image-end:::  

Microsoft Edge \(EdgeHTML\) As Máquinas Virtuais \(VMs\) permitem que você acesse diferentes versões de EdgeHTML e IE em seu computador por meio de VirtualBox \(ou VMWare\).  Escolha uma [máquina virtual na página de download.][MicrosoftDeveloperEdgeVms]  

## <a name="cloud-based-emulators-and-simulators"></a>Emuladores e simuladores baseados em nuvem  

Se você não for capaz de usar os emuladores e não tiver acesso a dispositivos reais, em seguida, os emuladores baseados em nuvem são a próxima melhor coisa.  Uma grande vantagem dos emuladores baseados em nuvem em dispositivos reais e emuladores locais é que você é capaz de automatizar testes de unidade para seu site em diferentes plataformas.  

*   [BrowserStack (comercial)][|::ref1::|] é o mais fácil de usar para testes manuais.  Você seleciona um sistema operacional, seleciona a versão do navegador e o tipo de dispositivo, seleciona uma URL para navegar e ela gira uma máquina virtual hospedada com a qual você pode interagir.  Você também pode executar vários emuladores na mesma tela, permitindo que você teste a aparência do seu aplicativo em vários dispositivos ao mesmo tempo.  
*   [O SauceLabs (comercial)][SauceLabs] permite que você execute testes de unidade dentro de um emulador, o que pode ser realmente útil para rotear um fluxo pelo seu site e assistir à gravação em vídeo disso depois em vários dispositivos.  Você também pode fazer testes manuais com seu site.  
*   [Device Anywhere (comercial)][AppExperience] não usa emuladores, mas dispositivos reais que você pode controlar remotamente.  Isso é muito útil no caso em que você precisa reproduzir um problema em um dispositivo específico e pode não exibir o bug usando qualquer uma das opções nos guias anteriores.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

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
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) é encontrada aqui e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Paulo Bakaus][PaulBakaus] \(Open Web Developer Advocate no Google | Ferramentas, Desempenho, Animação, UX\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
