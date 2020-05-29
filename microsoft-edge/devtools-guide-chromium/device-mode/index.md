---
title: Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607423"
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





# Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools   

  

Use o modo de dispositivo para aproximar a aparência e a execução de sua página em um dispositivo móvel.  

O modo de dispositivo é o nome para a coleção flexível de recursos no Microsoft Edge DevTools que ajudam você a simular dispositivos móveis.  Esses recursos incluem:  

*   [Simulando um visor móvel](#simulate-a-mobile-viewport)  
*   [Otimizando a rede](#throttle-the-network-only)  
*   [Otimizando a CPU](#throttle-the-cpu-only)  
*   [Simulação de localização geográfica](#override-geolocation)  
*   [Definir orientação](#set-orientation)  

## Limitações   

Pense no modo de dispositivo como uma [aproximação de primeira ordem][WikiApproximation] de como a sua página se parece e se sente em um dispositivo móvel.  Com o modo de dispositivo, você não executa o código em um dispositivo móvel.  Você simula a experiência do usuário móvel do laptop ou da área de trabalho.  

Há alguns aspectos dos dispositivos móveis que o DevTools nunca poderá simular.  Por exemplo, a arquitetura de CPUs móveis é muito diferente da arquitetura de CPUs para laptop ou desktop.  Quando estiver em dúvida, a melhor opção é realmente executar sua página em um dispositivo móvel.  Use [depuração remota] [DevToolsRemoteDebugging] para exibir, alterar, depurar e criar o perfil do código de uma página do laptop ou da área de trabalho, enquanto ela é executada em um dispositivo móvel.  

## Simular um visor móvel   

Clique na **barra de ferramentas Alternar** dispositivo ![ alternar barra ][ImageDeviceToolbarIcon] de ferramentas para abrir a interface do usuário que permite simular um visor móvel.  

> ##### Figura 1  
> A barra de ferramentas do dispositivo  
> ![A barra de ferramentas do dispositivo][ImageDeviceToolbar]  

Por padrão, a barra de ferramentas do dispositivo é aberta no modo de visor responsivo.  

### Modo de visor responsivo   

Arraste as alças para redimensionar o visor para qualquer dimensão necessária.  Ou insira valores específicos nas caixas largura e altura.  Na [Figura 2](#figure-2), a largura é definida como `626` e a altura é definida como `516` .  

> ##### Figura 2  
> As alças para alterar as dimensões do visor quando no modo de visor responsivo  
> ![As alças para alterar as dimensões do visor quando no modo de visor responsivo][ImageResponsiveHandles]  

#### Mostrar consultas de mídia   

Para mostrar pontos de interrupção de consulta de mídia acima do visor, clique em **mais opções** e selecione **Mostrar consultas de mídia**.  

> ##### Figura 3  
> Mostrar consultas de mídia  
> ![Mostrar consultas de mídia][ImageShowMediaQueries]  

Clique em um ponto de interrupção para alterar a largura do visor para que o ponto de interrupção seja disparado.  

> ##### Figura 4  
> Clique em um ponto de interrupção para alterar a largura do visor  
> ![Clique em um ponto de interrupção para alterar a largura do visor][ImageBreakpoint]  

#### Definir o tipo de dispositivo   

Use a lista **tipo de dispositivo** para simular um dispositivo móvel ou um dispositivo de desktop.  

> ##### Figura 5  
> A lista **tipo de dispositivo**  
> ![A lista tipo de dispositivo][ImageDeviceType]  

A tabela a seguir descreve as diferenças entre as opções.  **Método de renderização** refere-se ao Microsoft Edge renderiza a página como um visor móvel ou da área de trabalho.  **Ícone do cursor** refere-se ao tipo de cursor que você vê quando passa o mouse sobre a página.  Os **eventos acionados** referem-se à página `touch` ou `click` eventos quando você interage com a página.  

| Opção | Método de renderização | Ícone de cursor | Eventos acionados |  
|:--- |:--- |:--- |:--- |  
| Dispositivos móveis | Dispositivos móveis | Circle | touch |  
| Celular \ (sem toque \) | Dispositivos móveis | Normal |  clique em  |  
| Desktop | Desktop | Normal |  clique em  |  
| Área de trabalho \ (Touch \) | Desktop | Circle | touch |  

> [!NOTE]
> Se você não vir a lista **tipo de dispositivo** , clique em **mais opções** e selecione **Adicionar tipo de dispositivo**.  

### Modo visor do dispositivo móvel   

Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na lista de **dispositivos** .  

> ##### Figura 6  
> Lista de dispositivos  
> ![Lista de dispositivos][ImageDeviceList]  

#### Girar o visor para a orientação paisagem   

Clique em **girar** ![ rotação ][ImageRotateIcon] para girar o visor para a orientação paisagem.  

> ##### Figura 7  
> Orientação paisagem  
> ![Orientação paisagem][ImageLandscape]  

> [!NOTE]
> O botão **girar** desaparecerá se a **barra de ferramentas** do seu dispositivo for estreita.  

> ##### Figura 8  
> A barra de ferramentas do dispositivo  
> ![A barra de ferramentas do dispositivo][ImageDeviceToolbar2]  

Consulte também [definir orientação](#set-orientation).  

#### Mostrar quadro de dispositivo   

Ao simular as dimensões de um dispositivo móvel específico, como um iPhone 6, abra **mais opções** e selecione **Mostrar quadro de dispositivo** para mostrar a estrutura do dispositivo físico em torno do visor.  

> [!NOTE]
> Se você não vir um quadro de dispositivo para um dispositivo específico, provavelmente significa que o DevTools não tem arte para essa opção específica.  

> ##### Figura 9  
> Mostrar quadro de dispositivo  
> ![Mostrar quadro de dispositivo][ImageShowDeviceFrame]  

> ##### Figura 10  
> O quadro do dispositivo para o iPhone 6  
> ![O quadro do dispositivo para o iPhone 6][ImageIphoneFrame]  

#### Adicionar um dispositivo móvel personalizado   

Para adicionar um dispositivo personalizado:  

1.  Clique na lista de **dispositivos** e, em seguida, selecione **Editar**.  

> ##### Figura 11  
> Selecionar **Editar** 
> ![ selecionando editar][ImageEdit]  

1.  Clique em **Adicionar dispositivo personalizado**.  

1.  Insira um nome, uma largura e uma altura para o dispositivo.  A [taxa de pixels de dispositivo][MDNWindowDevicePixelRatio], a [cadeia de caracteres do agente do usuário][MDNUserAgent]e os campos do tipo de [dispositivo](#set-the-device-type) são opcionais.  O campo tipo de dispositivo é a lista definida como **celular** por padrão.  

> ##### Figura 12  
> Criando um dispositivo personalizado  
> ![Criando um dispositivo personalizado][ImageAddCustomDevice]  

### Mostrar réguas   

Clique em **mais opções** e selecione **Mostrar réguas** para ver as réguas acima e à esquerda do visor.  A unidade de dimensionamento das réguas é pixels.  

> ##### Figura 13  
> Mostrar réguas  
> ![Mostrar réguas][ImageShowRulers]  

> ##### Figura 14  
> Réguas acima e à esquerda da viewport  
> ![Réguas acima e à esquerda da viewport][ImageRulers]  

### Aplicar zoom ao visor   

Use a lista **zoom** para ampliar ou reduzir.  

> ##### Figura 15  
> Zoom  
> ![Zoom][ImageZoomViewport]  

## Acelerar a rede e a CPU   

Para acelerar a rede e a CPU, selecione celular de **nível intermediário** ou **móvel de baixo** nível na lista **acelerador** .  

> ##### Figura 16  
> Lista de aceleração  
> ![Lista de aceleração][ImageThrottling]  

O **Mobile de nível intermediário** simula a rede 3G rápida e acelera a CPU para que seja 4 vezes mais lento do que o normal.  O **celular low-end** simula a 3G lenta e acelera a CPU 6 vezes mais lenta do que o normal.  Lembre-se de que a limitação é relativa à funcionalidade normal do laptop ou da área de trabalho.  

> [!NOTE]
> A lista de **aceleração** ficará oculta se a **barra de ferramentas** do seu dispositivo for estreita.  

> ##### Figura 17  
> A barra de ferramentas do dispositivo  
> ![A barra de ferramentas do dispositivo][ImageDeviceToolbar3]  

### Acelerar apenas a CPU   

Para controlar apenas a CPU e não a rede, vá para o **painel desempenho** , clique em capturar configurações de captura de **configurações** e ![ ][ImageCaptureIcon] selecione **4x** lentidão ou **lentidão 6x** na lista **CPU** .  

> ##### Figura 18  
> Lista da CPU  
> ![Lista da CPU][ImageCPU]  

### Acelerar somente a rede   

Para limitar apenas a rede e não a CPU, vá até **Network** o painel de rede **e selecione 3G** ou a **3G lento** na lista **aceleração** .  

> ##### Figura 19  
> Lista de aceleração  
> ![Lista de aceleração][ImageNetwork]  

Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `3G` e selecione Habilitar a aceleração **3G rápida** ou **habilitar a limitação 3G lenta**.  

> ##### Figura 20  
> O menu de comando  
> ![O menu de comando][ImageCommandMenu]  

Você também pode definir a limitação de rede no painel **desempenho** .  Clique em **capturar** ![ configurações de captura ][ImageCaptureIcon] e, em seguida, selecione 3G **rápido** ou **3G lento** na lista **rede** .  

> ##### Figura 21  
> Definindo a limitação de rede no painel desempenho  
> ![Definindo a limitação de rede no painel desempenho][ImageNetwork2]  

## Substituir geolocalização   

Para abrir a interface do usuário que substitui a localização geográfica, clique em **Personalizar e controle devtools** `...` e selecione **mais**  >  **sensores**de ferramentas.  

> ##### Figura 22  
> Sensores  
> ![Sensores][ImageSensors]  

Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.  

> ##### Figura 23  
> Mostrar sensores  
> ![Mostrar sensores][ImageShowSensors]  

Selecione uma das predefinições **na lista geolocalização** ou selecione **local personalizado** para inserir suas próprias coordenadas ou selecione **localização indisponível** para testar como a sua página se comporta quando a localização geográfica está em um estado de erro.  

> ##### Figura 24  
> Geolocalização  
> ![Geolocalização][ImageGeolocation]  

## Definir orientação   

Para abrir a interface do usuário de orientação, clique em **Personalizar e controle devtools** `...` e selecione **mais**  >  **sensores**de ferramentas.  

> ##### Figura 25  
> Sensores  
> ![Sensores][ImageSensors2]  

Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.  

> ##### Figura 26  
> Mostrar sensores  
> ![Mostrar sensores][ImageShowSensors2]  

Selecione uma das predefinições na lista **orientação** ou selecione **orientação personalizada** para definir seus próprios valores Alfa, beta e gama.  

> ##### Figura 27  
> Orientação  
> ![Orientação][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figura 1: a barra de ferramentas do dispositivo"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Figura 2: identificadores para alterar as dimensões do visor quando no modo de visor responsivo"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Figura 3: mostrar consultas de mídia"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Figura 4: clique em um ponto de interrupção para alterar a largura do visor"  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Figura 5: lista do tipo de dispositivo"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Figura 6: lista de dispositivos"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Figura 7: orientação paisagem"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figura 8: a barra de ferramentas do dispositivo"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Figura 9: mostrar quadro de dispositivo"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Figura 10: o quadro do dispositivo para o iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Figura 11: selecionando editar"  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Figura 12: Criando um dispositivo personalizado"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Figura 13: Mostrar réguas"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Figura 14: réguas acima e à esquerda da viewport"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Figura 15: zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Figura 16: a lista de aceleração"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figura 17: a barra de ferramentas do dispositivo"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Figura 18: lista da CPU"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Figura 19: a lista de aceleração"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Figura 20: o menu de comando"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Figura 21: definindo a limitação de rede no painel desempenho"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figura 22: sensores"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figura 23: mostrar sensores"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Figura 24: geolocalização"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figura 25: sensores"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figura 26: mostrar sensores"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Figura 27: orientação"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/devtools-Guide-Chromium/Remote-Debugging/index "introdução à depuração remota de dispositivos Android"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordem de aproximação-primeira ordem-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
