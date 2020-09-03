---
description: Depuração remota do conteúdo ao vivo em um dispositivo Android de um computador com Windows ou macOS.
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f1ed7c698f588bb4e438d1b85a0cd0d1aba42647
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993496"
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

# Introdução à depuração remota de dispositivos Android  

Depurador remoto conteúdo dinâmico em um dispositivo Android a partir de seu computador com Windows ou macOS.  A página do tutorial a seguir ensina a concluir as ações a seguir.  

*   Configurar seu dispositivo Android para depuração remota e descobri-lo a partir de seu computador de desenvolvimento.  
*   Inspecione e depure conteúdo dinâmico em seu dispositivo Android a partir de seu computador de desenvolvimento.  
*   O conteúdo do screencast do seu dispositivo Android para uma instância do DevTools em seu computador de desenvolvimento.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> A depuração remota do aplicativo Microsoft Edge em dispositivos iOS não é suportada no momento.  O guia a seguir é especialmente focalizado em depuração remota do Microsoft Edge em dispositivos Android.
> Se você tiver um dispositivo macOS, siga o [Guia de depuração do Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar remotamente o Microsoft Edge em um dispositivo IOS usando o Safari.  Para obter mais informações sobre a ferramenta Web Inspector no Safari, consulte [ferramentas de desenvolvimento da Web do Safari][AppleDeveloperSafariTools].  

## Etapa 1: Descubra seu dispositivo Android  

O fluxo de trabalho abaixo funciona para a maioria dos usuários.  Para obter mais ajuda, consulte o guia de [solução de problemas: devtools não está detectando a seção de dispositivos Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Abra a tela **Opções do desenvolvedor** no seu Android.  Para obter mais informações, consulte [Configurar opções do desenvolvedor no dispositivo][AndroidDeveloperStudioDevOptions].  
1.  Selecione **habilitar a depuração USB**.  
1.  Na máquina de desenvolvimento, abra o Microsoft Edge.  
1.  Navegue até a `edge://inspect` página no Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="A página edge://inspect no Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Figura 1.  A `edge://inspect` página no Microsoft Edge  
    :::image-end:::  
    
1.  Conecte seu dispositivo Android diretamente ao seu computador de desenvolvimento usando um cabo USB.  Na primeira vez que tentar se conectar, você geralmente verá prompt sobre DevTools detectando um dispositivo desconhecido.  Aceite o prompt **Allow USB Debugging** Permission em seu dispositivo Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="O prompt permitir a depuração USB em um dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Figura 2.  O prompt **permitir a depuração USB** em um dispositivo Android  
    :::image-end:::  
    
1.  Se você vir o nome do modelo do seu dispositivo Android, o Microsoft Edge estabelecerá a conexão com êxito com o seu dispositivo.  Vá para a seção [etapa 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### Solução de problemas: o DevTools não está detectando o dispositivo Android  

Use as dicas a seguir para ajudá-lo a solucionar os problemas de configuração correto para o seu hardware.  

*   Se você estiver usando um hub USB, tente conectar o dispositivo Android diretamente ao seu computador de desenvolvimento.  
*   Tente desconectar o cabo USB entre seu dispositivo Android e seu computador de desenvolvimento e Conecte novamente o cabo USB.  Concluir a tarefa enquanto as telas do seu computador de desenvolvimento e Android estiverem desbloqueadas.  
*   Verifique se o cabo USB funciona.  Você deve ser capaz de inspecionar arquivos em seu dispositivo Android a partir de seu computador de desenvolvimento.  

Use as dicas a seguir para ajudá-lo a verificar se o seu software está configurado corretamente.  

*   Se a sua máquina de desenvolvimento estiver executando o Windows, tente instalar manualmente os drivers USB do seu dispositivo Android.  Para obter mais informações, consulte [instalar drivers USB OEM][AndroidDeveloperToolsOemUsb].  
*   Algumas combinações de dispositivos Windows e Android \ (especialmente a Samsung \) exigem configurações adicionais.  Para obter mais informações, consulte os [dispositivos devtools não detectam o dispositivo quando conectado][Stackoverflow21925992].  

Use as dicas a seguir para ajudá-lo a solucionar problemas para não ver o prompt **permitir a depuração USB** em seu dispositivo Android.  

*   Desconecte e, em seguida, reconecte o cabo USB enquanto o DevTools estiver em foco na máquina de desenvolvimento e o seu tela inicial Android estiver sendo exibido.  
    
    > [!NOTE]
    > Você pode não ver o prompt se as telas do seu computador de desenvolvimento ou Android estiverem bloqueadas.  

*   Atualização das configurações de exibição do seu dispositivo Android e do seu computador de desenvolvimento para que cada nunca entre em suspensão.  
*   Definindo o modo USB para Android para PTP.  Para obter mais informações, consulte [o Galaxy S4 não mostra a caixa de diálogo autorizar a depuração de USB][StackexchangeAndroid101933].  
*   Selecione **revogar autorizações de depuração USB** na tela **Opções do desenvolvedor** em seu dispositivo Android para redefini-lo para um estado novo.  

Se você encontrar uma solução que não seja mencionada nesta página ou em [dispositivos devtools não detectará o dispositivo quando conectado][Stackoverflow21925992] ao estouro de pilha, adicione a solução à pergunta de estouro de pilha.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Etapa 2: depurar o conteúdo do seu dispositivo Android a partir de seu computador de desenvolvimento  

1.  Abra o Microsoft Edge em seu dispositivo Android.  
1.  Na `edge://inspect` página, você vê o nome do modelo do seu dispositivo Android, seguido do número de série do dispositivo.  Abaixo disso, você deve ver a versão do Microsoft Edge em execução no dispositivo, com o número de versão entre parênteses.  Cada guia aberta do Microsoft Edge Obtém uma seção exclusiva.  Você pode interagir com essa guia em uma seção.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Um dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Figura 3.  Um dispositivo remoto conectado  
    :::image-end:::  
    
1.  Na **guia abrir com a** caixa de texto URL, insira uma URL e, em seguida, selecione **abrir**.  A página é aberta em uma nova guia em seu dispositivo Android.  
1.  Selecione **inspecionar** ao lado da URL que você acabou de abrir.  Uma nova instância de DevTools é aberta.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### Mais ações: focalizar, recarregar ou fechar uma guia  

Selecione a **guia foco**, **recarregar**ou **Fechar** ao lado da guia que você deseja focalizar, recarregar ou fechar.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Os botões para enfocar, recarregar ou fechar uma guia" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Figura 4.  Os botões para enfocar, recarregar ou fechar uma guia  
:::image-end:::  

### Inspecionar elementos  

Vá para o painel **elementos** da sua instância do devtools e passe o mouse sobre um elemento para realçá-lo na viewport do seu dispositivo Android.  

Você também pode selecionar um elemento na tela do seu dispositivo Android para selecioná-lo no painel de **elementos** .  Selecione **selecionar elemento** ![ selecione ][ImageSelectElementIcon] o ícone do elemento na sua instância do devtools e selecione o elemento na tela do seu dispositivo Android.  

> [!NOTE]
> **Selecione o elemento** está desabilitado após a primeira seleção, portanto, você deve reativá-lo toda vez que quiser usar o recurso.  

### Screencast sua tela do Android para o seu computador de desenvolvimento  

Selecione **alternar** ![ o ícone de botão de alternância do screencast ][ImageToggleScreencastIcon] para exibir o conteúdo do seu dispositivo Android em sua instância do devtools.  

Você pode interagir com o screencast da seguinte maneira.  

*   Os cliques são convertidos em toques, disparando eventos de toque apropriados no dispositivo.  
*   Os pressionamentos de teclas do computador são enviados para o dispositivo.  
*   Para simular um gesto de pinçagem, mantenha pressionado `Shift` enquanto arrasta.  
*   Para rolar, use a trackpad ou a roda do mouse, ou Fling com o ponteiro do mouse.

> [!NOTE]
> Use as dicas a seguir para ajudá-lo a screencasts.  
> 
> *   Screencasts exibem apenas o conteúdo da página.  Partes transparentes do screencast representam interfaces de dispositivos, como a barra de endereços do Microsoft Edge, a barra de status do Android ou o teclado Android.  
> *   Os screencasts afetam negativamente as tarifas de quadro.  Desabilite o screencast enquanto estiver medindo rolagens ou animações para obter uma imagem mais precisa do desempenho da página.  
> *   Se a tela do seu dispositivo Android for bloqueada, o conteúdo do screencast desaparecerá.  Desbloqueie a tela do seu dispositivo Android para continuar o screencast automaticamente.  

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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
