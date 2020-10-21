---
description: Seu trabalho não termina com a garantia de que o seu site seja ótimo no Microsoft Edge e no Android.  Apesar de o modo de dispositivo poder simular uma faixa de outros dispositivos como iPhones, recomendamos que você consulte as soluções para emulação fornecidas por outros navegadores.
title: Emular e Testar Outros Navegadores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1a7cc1c7e0a49760f30afdc16921824372b3a1aa
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124940"
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

# Emular e testar outros navegadores  

Seu trabalho não termina com a garantia de que o seu site seja ótimo no Microsoft Edge e no Android.  Apesar de o modo de dispositivo poder simular uma faixa de outros dispositivos como iPhones, recomendamos que você consulte as soluções para emulação fornecidas por outros navegadores.  

### Resumo  

*   Quando você não tiver um dispositivo em particular ou se quiser fazer uma verificação de ponto em algo, a melhor opção é emular o dispositivo diretamente dentro do navegador.  
*   Emuladores e emuladores de dispositivo permitem a imitação do seu site de desenvolvimento em uma variedade de dispositivos da sua estação de trabalho.  
*   Os emuladores baseados em nuvem permitem automatizar os testes de unidade do seu site em diferentes plataformas.  

## Emuladores de navegador  

Os emuladores de navegador são ótimos para testar a capacidade de resposta de um site, mas cada um não emula diferenças na API, suporte a CSS e certos comportamentos que você vê em um navegador móvel.  Teste seu site em navegadores executados em dispositivos reais para ter certeza de que tudo se comporta conforme o esperado.  

### Modo de exibição de design responsivo do Firefox  

O Firefox tem um [modo de exibição de design responsivo][MDNResponsiveDesignMode] que incentiva você a parar de pensar em termos de dispositivos específicos e explorar como o design muda em tamanhos de tela comuns ou em seu próprio tamanho arrastando as bordas.  

### Emulação de EdgeHTML  

Para emular telefones Windows, use a [emulação interna][DevToolsEdgeHtmlEmulation]do Microsoft Edge \ (EdgeHTML \).  

Use a [emulação do IE 11][Ie11DevToolsEmulation] para simular como a sua página pode ser exibida em versões mais antigas do Internet Explorer.  

## Emuladores de dispositivo e simuladores  

Os simuladores de dispositivo e emuladores simulam não apenas o ambiente do navegador, mas o dispositivo inteiro.  Cada um é útil para testar itens que exigem integração com o sistema operacional, por exemplo, entrada de formulário com teclados virtuais.  

### Emulador Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

No momento, não há nenhuma maneira de instalar o Microsoft Edge em um emulador Android.  No entanto, você pode usar o navegador Android, o Shell de conteúdo do Chromium e o Firefox para Android, que são revisados mais adiante neste guia.  Chromium o Shell de conteúdo executa o mesmo mecanismo de renderização Chromium como o Microsoft Edge, mas vem sem qualquer recurso específico do navegador.  

O emulador Android vem com o SDK do Android que você precisa baixar como parte do [Android Studio][AndroidStudioDownload].  Em seguida, siga as instruções para [configurar um dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e [iniciar o emulador][AndroidStudioRunAppsAndroidEmulator].  
Depois que o emulador for inicializado, clique no ícone do navegador e teste o site no navegador de ações antigo para Android.  

#### Shell de conteúdo do Chromium no Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Para instalar o Shell de conteúdo Chromium para Android, deixe seu emulador em execução e execute o comando a seguir.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Agora você pode testar seu site com o Shell de conteúdo do Chromium.  

#### Firefox no Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Semelhante ao Shell de conteúdo Chromium, você pode obter um APK para instalar o Firefox no emulador.  

[Baixe o arquivo. apk correto][MozillaFirefoxDownload].  

Para instalar o arquivo em um emulador aberto ou dispositivo Android conectado, execute o comando a seguir.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### simulador do iOS  

O simulador do iOS para Mac OS X vem com o Xcode, que você [instala a partir da App Store][MacAppStoreXcode].  

Quando terminar, aprenda a trabalhar com o simulador por meio da [documentação do desenvolvedor da Apple][AppleSimulatorHelp].  

> [!NOTE]
> Para evitar ter que abrir o Xcode sempre que você quiser usar o simulador do iOS, abra-o, clique com o botão direito do mouse no ícone do simulador do iOS em seu Dock e escolha **manter no Dock**.  Agora, basta clicar nesse ícone sempre que precisar.  

###  Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   VM moderna do IE  
:::image-end:::  

O Microsoft Edge \ (EdgeHTML \) máquinas virtuais \ (VMs \) permitem que você acesse versões diferentes do EdgeHTML e do IE em seu computador via VirtualBox \ (ou VMWare \).  Escolha uma [máquina virtual na página de download][MicrosoftDeveloperEdgeVms].  

## Emuladores e simuladores baseados em nuvem  

Se você não conseguir usar os emuladores e não tiver acesso a dispositivos reais, os emuladores baseados em nuvem serão a melhor coisa melhor.  Uma grande vantagem dos emuladores baseados em nuvem em dispositivos reais e emuladores locais é que você pode automatizar testes de unidade para o seu site em diferentes plataformas.  

*   [BrowserStack (comercial)][|::ref1::|] é a maneira mais fácil de usar para testes manuais.  Selecione um sistema operacional, selecione a versão do navegador e o tipo de dispositivo, selecione uma URL para navegar e ele gira uma máquina virtual hospedada com a qual você pode interagir.  Você também pode executar vários emuladores na mesma tela, permitindo que você teste a aparência do seu aplicativo em vários dispositivos ao mesmo tempo.  
*   O [SauceLabs (comercial)][SauceLabs] permite que você execute testes de unidade dentro de um emulador, que podem ser muito úteis para o script de um fluxo por meio de seu site e para observar a gravação de vídeo disso posteriormente em vários dispositivos.  Você também pode fazer testes manuais com o seu site.  
*   O [dispositivo em qualquer lugar (comercial)][AppExperience] não usa emuladores, mas dispositivos reais que você pode controlar remotamente.  Isso é muito útil no evento em que você precisa reproduzir um problema em um dispositivo específico e não consegue ver o erro usando qualquer uma das opções nos guias anteriores.  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor The Google | Ferramentas, desempenho, animação, UX \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
