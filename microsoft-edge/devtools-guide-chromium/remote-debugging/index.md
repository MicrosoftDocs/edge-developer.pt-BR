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
# Introdução à depuração remota de dispositivos Android   



Depurador remoto conteúdo dinâmico em um dispositivo Android a partir de seu computador com Windows ou macOS.  Este tutorial ensina a:  

*   Configurar seu dispositivo Android para depuração remota e descobri-lo a partir de seu computador de desenvolvimento.  
*   Inspecione e depure conteúdo dinâmico em seu dispositivo Android a partir de seu computador de desenvolvimento.  
*   O conteúdo do screencast do seu dispositivo Android para uma instância do DevTools em seu computador de desenvolvimento.  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## Etapa 1: Descubra seu dispositivo Android   

O fluxo de trabalho abaixo funciona para a maioria dos usuários.  Consulte [solução de problemas: o devtools não está detectando o dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) para obter mais ajuda.  

1.  Abra a tela **Opções do desenvolvedor** no seu Android.  Consulte [Configurar opções do desenvolvedor no dispositivo](https://developer.android.com/studio/debug/dev-options.html).  
1.  Selecione **habilitar a depuração USB**.  
1.  Na máquina de desenvolvimento, abra o Microsoft Edge.  
1.  [Abra o devtools][DevToolsOpen].  
1.  No devtools, selecione o **menu principal** `...` e, em seguida, selecione **mais ferramentas**de  >  **dispositivos remotos**.  
    
    > ##### Figura 1  
    > Abrindo a guia **dispositivos remotos** por meio do **menu principal**  
    > ! [Abrindo a guia dispositivos remotos por meio do menu principal] [ImageOpenRemoteDevices]  

1.  No DevTools, abra a guia **configurações** .  

1.  Verifique se a caixa de seleção **descobrir dispositivos USB** está habilitada.  
    
    > ##### Figura 2  
    > A caixa de seleção **descobrir dispositivos USB** está habilitada  
    > ! [A caixa de seleção descobrir dispositivos USB está habilitada] [ImageDiscoverUSBDevices]  

1.  Conecte seu dispositivo Android diretamente ao seu computador de desenvolvimento usando um cabo USB.  Na primeira vez que você fizer isso, você normalmente verá que o DevTools detectou um dispositivo desconhecido.  Se você vir um ponto verde e o texto **conectado** abaixo do nome do modelo do seu dispositivo Android, o devtools estabelecerá a conexão com êxito com o seu dispositivo.  Vá para a [etapa 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  Se o seu dispositivo estiver aparecendo como **desconhecido**, aceite o prompt **Allow USB Debugging** Permission em seu dispositivo Android.  

### Solução de problemas: o DevTools não está detectando o dispositivo Android   

Verifique se o seu hardware está configurado corretamente:  

*   Se você estiver usando um hub USB, tente conectar o dispositivo Android diretamente ao seu computador de desenvolvimento.  
*   Tente desconectar o cabo USB entre seu dispositivo Android e seu computador de desenvolvimento e conecte-o novamente.  Faça isso enquanto as telas do seu computador de desenvolvimento e Android estiverem desbloqueadas.  
*   Verifique se o cabo USB funciona.  Você deve ser capaz de inspecionar arquivos em seu dispositivo Android a partir de seu computador de desenvolvimento.  

Verifique se o seu software está configurado corretamente:  

*   Se a sua máquina de desenvolvimento estiver executando o Windows, tente instalar manualmente os drivers USB do seu dispositivo Android.  Consulte [instalar drivers USB OEM][AndroidUSBDrivers].  
    
*   Algumas combinações de dispositivos Windows e Android (especialmente a Samsung) exigem configuração adicional.  Consulte [os dispositivos DevTools não detectam o dispositivo quando conectado] [StackOverflowDevicesNotDetected].  
    
Se você não vir o prompt **permitir a depuração USB** em seu dispositivo Android, tente:  

*   Desconecte e, em seguida, reconecte o cabo USB enquanto o DevTools estiver em foco na máquina de desenvolvimento e o seu tela inicial Android estiver sendo exibido.  Em outras palavras, às vezes o prompt não aparece quando as telas do seu computador de desenvolvimento ou Android estão bloqueadas.
*   Atualização das configurações de exibição do seu dispositivo Android e do seu computador de desenvolvimento, para que eles nunca entrem em suspensão.  
*   Definindo o modo USB para Android para PTP.  Consulte [o Galaxy S4 não mostra a caixa de diálogo autorizar a depuração de USB][StackExchangeGalaxyS4DoesNotShowDialogBox].  
*   Selecione **revogar autorizações de depuração USB** na tela **Opções do desenvolvedor** em seu dispositivo Android para redefini-lo para um estado novo.  

Se você encontrar uma solução não mencionada nesta seção ou em [DevTools dispositivos não detecta o dispositivo quando conectado] [StackOverflowDevicesNotDetected] ou adicione uma resposta a essa pergunta de estouro de pilha<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Etapa 2: depurar o conteúdo do seu dispositivo Android a partir de seu computador de desenvolvimento   

1.  Abra o Microsoft Edge em seu dispositivo Android.  

1.  Na guia **dispositivos remotos** , selecione a guia que corresponde ao nome do modelo do seu dispositivo Android.  
    Na parte superior desta página, você verá o nome do modelo do seu dispositivo Android, seguido pelo número de série.  Abaixo disso, você deve ver a versão do Microsoft Edge em execução no dispositivo, com o número de versão entre parênteses.  Cada guia aberta do Microsoft Edge obtém sua própria seção.  Você pode interagir com essa guia desta seção.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  Na caixa de texto **nova guia** , insira uma URL e, em seguida, selecione **abrir**.  A página é aberta em uma nova guia em seu dispositivo Android.  

1.  Selecione **inspecionar** ao lado da URL que você acabou de abrir.  Uma nova instância de DevTools é aberta.  A versão do Microsoft Edge que está sendo executada em seu dispositivo Android determina a versão do DevTools que é aberta na máquina de desenvolvimento.  
    Portanto, se o seu dispositivo Android estiver executando uma versão mais antiga do Microsoft Edge, a instância do DevTools poderá parecer muito diferente da que você está acostumado.  

### Mais ações: recarregar, focalizar ou fechar uma guia   

Selecione **mais opções** `...` ao lado da guia que você deseja recarregar, enfocar ou fechar.  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### Inspecionar elementos   

Vá para o painel **elementos** da sua instância do devtools e passe o mouse sobre um elemento para realçá-lo na viewport do seu dispositivo Android.  

Você também pode selecionar um elemento na tela do seu dispositivo Android para selecioná-lo no painel de **elementos** .  Selecione **selecionar** elemento ![ selecione ][ImageSelectElementIcon] o elemento na sua instância do devtools e selecione o elemento na tela do seu dispositivo Android.  

> [!NOTE]
> **Selecione o elemento** está desabilitado após a primeira seleção, portanto, você deve reativá-lo toda vez que quiser usar esse recurso.  

### Screencast sua tela do Android para o seu computador de desenvolvimento   

Selecione **alternar screencast** ![ alternar screencast ][ImageToggleScreencastIcon] para exibir o conteúdo do seu dispositivo Android na sua instância do devtools.  

Você pode interagir com o screencast de várias maneiras:  

*   Os cliques são convertidos em toques, disparando eventos de toque apropriados no dispositivo.  
*   Os pressionamentos de teclas do computador são enviados para o dispositivo.  
*   Para simular um gesto de pinçagem, mantenha pressionado `Shift` enquanto arrasta.  
*   Para rolar, use a trackpad ou a roda do mouse, ou Fling com o ponteiro do mouse.

Algumas observações sobre screencasts:  

*   Screencasts exibem apenas o conteúdo da página.  Partes transparentes do screencast representam interfaces de dispositivos, como a barra de endereços do Microsoft Edge, a barra de status do Android ou o teclado Android.  
*   Os screencasts afetam negativamente as tarifas de quadro.  Desabilite o screencast enquanto estiver medindo rolagens ou animações para obter uma imagem mais precisa do desempenho da página.  
*   Se a tela do seu dispositivo Android for bloqueada, o conteúdo do screencast desaparecerá.  Desbloqueie a tela do seu dispositivo Android para continuar o screencast automaticamente.  





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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
