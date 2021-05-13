---
description: Conteúdo ao vivo de depuração remota em um dispositivo Android de um computador Windows ou macOS.
title: Introdução à depuração remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d5a5ea8faef40925fb0fb986eb984ac9ae4f051b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565103"
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
# <a name="get-started-with-remote-debugging-android-devices"></a>Introdução à depuração remota de dispositivos Android  

Conteúdo ao vivo de depuração remota em um dispositivo Android do computador Windows ou macOS.  A página de tutorial a seguir ensina como concluir as seguintes ações.  

*   Configurar seu dispositivo Android para depuração remota e descubra-o no computador de desenvolvimento.  
*   Inspecionar e depurar conteúdo ao vivo em seu dispositivo Android da máquina de desenvolvimento.  
*   Conteúdo de screencast do dispositivo Android para uma instância do DevTools em sua máquina de desenvolvimento.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> A depuração remota do Microsoft Edge aplicativo em dispositivos iOS não é suportada no momento.  O guia a seguir é especificamente focado na depuração remota Microsoft Edge em dispositivos Android.
> Se você tiver um dispositivo macOS, siga o guia de [Depuração do Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar remotamente Microsoft Edge em um dispositivo iOS usando o Safari.  Para obter mais informações sobre a ferramenta Inspetor da Web no Safari, navegue até [Safari Web Development Tools][AppleDeveloperSafariTools].  

## <a name="step-1-discover-your-android-device"></a>Etapa 1: Descobrir seu dispositivo Android  

O fluxo de trabalho abaixo funciona para a maioria dos usuários.  Para obter mais ajuda, navegue até [Solução de Problemas: o DevTools não está detectando a seção dispositivo Android.](#troubleshooting-devtools-is-not-detecting-the-android-device)  

1.  Abra a **tela Opções do** Desenvolvedor em seu Android.  Para obter mais informações, navegue até [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].  
1.  Escolha **Habilitar Depuração USB**.  
1.  Em sua máquina de desenvolvimento, abra Microsoft Edge.  
1.  Navegue até `edge://inspect` a página Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="A edge://inspect de Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Figura 1.  A `edge://inspect` página em Microsoft Edge  
    :::image-end:::  
    
1.  Conexão seu dispositivo Android diretamente para sua máquina de desenvolvimento usando um cabo USB.  Na primeira vez que você tentar se conectar, um prompt deve ser exibido sobre o DevTools detectar um dispositivo desconhecido.  Aceite o **prompt de permissão Permitir Depuração USB** em seu dispositivo Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="O prompt de permissão Permitir Depuração USB em um dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Figura 2.  O prompt de permissão Permitir **Depuração USB** em um dispositivo Android  
    :::image-end:::  
    
1.  Se o nome do modelo do dispositivo Android for exibido, Microsoft Edge estabeleceu com êxito a conexão com seu dispositivo.  Continue até a [seção Etapa 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a>Solução de problemas: o DevTools não está detectando o dispositivo Android  

Use as dicas a seguir para ajudá-lo a solucionar problemas das configurações corretas para o hardware.  

*   Se você estiver usando um hub USB, tente conectar seu dispositivo Android diretamente à máquina de desenvolvimento.  
*   Tente desconectar o cabo USB entre o dispositivo Android e a máquina de desenvolvimento e, em seguida, conecte novamente o cabo USB.  Conclua a tarefa enquanto as telas do computador de desenvolvimento e Android estão desbloqueadas.  
*   Certifique-se de que o cabo USB funcione.  Você deve ser capaz de inspecionar arquivos em seu dispositivo Android de sua máquina de desenvolvimento.  

Use as dicas a seguir para ajudá-lo a verificar se o software está definido corretamente.  

*   Se a máquina de desenvolvimento estiver executando Windows, tente instalar manualmente os drivers USB para seu dispositivo Android.  Para obter mais informações, navegue até [Instalar drivers USB OEM][AndroidDeveloperToolsOemUsb].  
*   Algumas combinações de Windows e dispositivos Android \(especialmente a Samsung\) exigem configurações adicionais.  Para obter mais informações, navegue até [Dispositivos DevTools não detecta dispositivo quando conectado][Stackoverflow21925992].  

Use as dicas a seguir para ajudá-lo a solucionar problemas se o prompt **Permitir Depuração USB** não for exibido em seu dispositivo Android.  

*   Desconectando e, em seguida, conectando o cabo USB enquanto o DevTools está em foco no seu computador de desenvolvimento e sua tela inicial do Android está sendo exibido.  
    
    > [!NOTE]
    > O prompt será exibido se as telas do computador de desenvolvimento ou Android estão bloqueadas.  

*   Atualizando as configurações de exibição para seu dispositivo Android e máquina de desenvolvimento para que cada um nunca vá para o sono.  
*   Definindo o modo USB para Android como PTP.  Para obter mais informações, navegue até o Galaxy S4 não mostra a caixa de diálogo [Autorizar depuração USB][StackexchangeAndroid101933].  
*   Escolha **** **Revogar Autorizações de Depuração USB** na tela Opções do Desenvolvedor em seu dispositivo Android para redefini-la para um estado novo.  

Se você encontrar uma solução que não seja mencionada nesta página ou em [Dispositivos DevTools][Stackoverflow21925992] não detectar dispositivo quando conectado ao Stack Overflow, adicione sua solução à pergunta Stack Overflow<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->.  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a>Etapa 2: Depurar conteúdo em seu dispositivo Android da máquina de desenvolvimento  

1.  Abra Microsoft Edge em seu dispositivo Android.  
1.  Navegue `edge://inspect` até , o nome do modelo do dispositivo Android é exibido, seguido pelo número de série do dispositivo.  Abaixo disso, a versão do Microsoft Edge em execução no dispositivo deve ser exibida, com o número da versão entre parênteses.  Cada guia Microsoft Edge obtém uma seção exclusiva.  Você pode interagir com essa guia de uma seção.  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Um dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Figura 3.  Um dispositivo remoto conectado  
    :::image-end:::  
    
1.  Na guia **Abrir com a caixa de texto url,** insira uma URL e escolha **Abrir**.  A página abre em uma nova guia em seu dispositivo Android.  
1.  Escolha **inspecionar** ao lado da URL que você acabou de abrir.  Uma nova instância do DevTools é aberta.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a>Mais ações: foco, atualização ou fechar uma guia  

Escolha **a guia foco,** **recarregue**ou **feche** ao lado da guia que você deseja focalizar, atualizar ou fechar.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Os botões para focalizar, atualizar ou fechar uma guia" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Figura 4.  Os botões para focalizar, atualizar ou fechar uma guia  
:::image-end:::  

### <a name="inspect-elements"></a>Inspecionar elementos  

Navegue até **a ferramenta Elements** da sua instância do DevTools e passe o mouse em um elemento para realça-lo no viewport do seu dispositivo Android.  

Você também pode selecionar um elemento na tela do dispositivo Android para selecioná-lo na **ferramenta Elementos.**  Escolha **Selecionar Elemento** \( Selecione Elemento \) ícone em sua instância do ![ DevTools e selecione o elemento na tela ](../media/select-element-icon.msft.png) do dispositivo Android.  

> [!NOTE]
> **Select Element** é desabilitado após a primeira seleção, portanto, você deve reabilitar sempre que quiser usar o recurso.  

### <a name="screencast-your-android-screen-to-your-development-machine"></a>Screencast your Android screen to your development machine  

Escolha **Toggle Screencast** \( Toggle Screencast \) icon para exibir o conteúdo do seu dispositivo Android em sua instância ![ do ](../media/toggle-screencast-icon.msft.png) DevTools.  

Você pode interagir com o screencast das seguintes maneiras.  

*   As escolha são traduzidas em toques, disparando eventos de toque apropriados no dispositivo.  
*   Teclas de teclas em seu computador são enviadas para o dispositivo.  
*   Para simular um gesto de pinça, segure `Shift` enquanto arrasta.  
*   Para rolar, use o trackpad ou a roda do mouse ou arremesse com o ponteiro do mouse.

> [!NOTE]
> Use as dicas a seguir para ajudá-lo a screencast.  
> 
> *   Os screencasts exibem apenas o conteúdo da página.  Partes transparentes do screencast representam interfaces de dispositivo, como a barra Microsoft Edge de endereços, a barra de status do Android ou o teclado Android.  
> *   Screencasts afetam negativamente as taxas de quadros.  Desabilite o screencasting durante a medição de rolagem ou animações para obter uma imagem mais precisa do desempenho da sua página.  
> *   Se a tela do dispositivo Android for travada, o conteúdo do screencast desaparecerá.  Desbloqueie a tela do dispositivo Android para retomar automaticamente a screencast.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opções de desenvolvedor no dispositivo | Desenvolvedor Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar drivers USB OEM | Desenvolvedores Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Ferramentas de Desenvolvimento web do Safari | Desenvolvedor apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://general.support.brightcove.com/developer/debugging-mobile-devices.html "Depuração em dispositivos móveis | Suporte brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb - Pilha de Entusiastas do Android Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Dispositivos DevTools não detectam dispositivos quando conectados - Estouro de Pilha"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
