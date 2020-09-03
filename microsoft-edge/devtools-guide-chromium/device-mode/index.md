---
description: Use dispositivos virtuais no modo de dispositivo para Microsoft Edge para criar websites para os primeiros sites do celular.
title: Simular dispositivos móveis com o modo de dispositivo no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: eababe8112b5d888671a8955e16f0fe1c89564fb
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993013"
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

Clique em **alternar barra de ferramentas de dispositivo** \ ( ![ alternar barra ][ImageDeviceToolbarIcon] de ferramentas de dispositivo \) para abrir a interface do usuário que permite simular um visor móvel.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A barra de ferramentas do dispositivo  
:::image-end:::  

Por padrão, a barra de ferramentas do dispositivo é aberta no modo de visor responsivo.  

### Modo de visor responsivo   

Arraste as alças para redimensionar o visor para qualquer dimensão necessária.  Ou insira valores específicos nas caixas largura e altura.  Na figura a seguir, a largura é definida como `626` e a altura é definida como `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="As alças para alterar as dimensões do visor quando no modo de visor responsivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   As alças para alterar as dimensões do visor quando no modo de visor responsivo  
:::image-end:::  

#### Mostrar consultas de mídia   

Para mostrar pontos de interrupção de consulta de mídia acima do visor, clique em **mais opções** e selecione **Mostrar consultas de mídia**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas de mídia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Mostrar consultas de mídia**  
:::image-end:::  

Clique em um ponto de interrupção para alterar a largura do visor para que o ponto de interrupção seja disparado.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Clique em um ponto de interrupção para alterar a largura do visor" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Clique em um ponto de interrupção para alterar a largura do visor  
:::image-end:::  

#### Definir o tipo de dispositivo   

Use a lista **tipo de dispositivo** para simular um dispositivo móvel ou um dispositivo de desktop.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="A lista tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   A lista **tipo de dispositivo**  
:::image-end:::  

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

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Lista de **dispositivos**  
:::image-end:::  

#### Girar o visor para a orientação paisagem   

Clique em **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar o visor para a orientação paisagem.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Orientação paisagem" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   Orientação paisagem  
:::image-end:::  

> [!NOTE]
> O botão **girar** desaparecerá se a **barra de ferramentas** do seu dispositivo for estreita.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A **barra de ferramentas do dispositivo**  
:::image-end:::  

Consulte também [definir orientação](#set-orientation).  

#### Mostrar quadro de dispositivo   

Ao simular as dimensões de um dispositivo móvel específico, como um iPhone 6, abra **mais opções** e selecione **Mostrar quadro de dispositivo** para mostrar a estrutura do dispositivo físico em torno do visor.  

> [!NOTE]
> Se você não vir um quadro de dispositivo para um dispositivo específico, provavelmente significa que o DevTools não tem arte para essa opção específica.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar quadro de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Mostrar quadro de dispositivo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="O quadro do dispositivo para o iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         O quadro do dispositivo para o iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Adicionar um dispositivo móvel personalizado   

Para adicionar um dispositivo personalizado:  

1.  Clique na lista de **dispositivos** e, em seguida, selecione **Editar**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Selecione Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Selecione **Editar**  
    :::image-end:::  
    
1.  Clique em **Adicionar dispositivo personalizado**.  
1.  Insira um nome, uma largura e uma altura para o dispositivo.  A [taxa de pixels de dispositivo][MDNWindowDevicePixelRatio], a [cadeia de caracteres do agente do usuário][MDNUserAgent]e os campos do tipo de [dispositivo](#set-the-device-type) são opcionais.  O campo tipo de dispositivo é a lista definida como **celular** por padrão.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Criar um dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Criar dispositivo personalizado  
    :::image-end:::  

### Mostrar réguas   

Clique em **mais opções** e selecione **Mostrar réguas** para ver as réguas acima e à esquerda do visor.  A unidade de dimensionamento das réguas é pixels.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Mostrar réguas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **Mostrar réguas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Réguas acima e à esquerda da viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Réguas acima e à esquerda da viewport  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Aplicar zoom ao visor   

Use a lista **zoom** para ampliar ou reduzir.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Acelerar a rede e a CPU   

Para acelerar a rede e a CPU, selecione celular de **nível intermediário** ou **móvel de baixo** nível na lista **acelerador** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Lista de aceleração" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Lista de **aceleração**  
:::image-end:::  

O **Mobile de nível intermediário** simula a rede 3G rápida e acelera a CPU para que seja 4 vezes mais lento do que o normal.  O **celular low-end** simula a 3G lenta e acelera a CPU 6 vezes mais lenta do que o normal.  Lembre-se de que a limitação é relativa à funcionalidade normal do laptop ou da área de trabalho.  

> [!NOTE]
> A lista de **aceleração** fica oculta se a **barra de ferramentas** do seu dispositivo for estreita.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A **barra de ferramentas do dispositivo**  
:::image-end:::  

### Acelerar apenas a CPU   

Para controlar apenas a CPU e não a rede, vá para o painel **desempenho** , clique em **configurações de captura** \ (configurações de ![ captura ][ImageCaptureIcon] \) e selecione **4x** lentidão ou **lentidão 6x** na lista **CPU** .  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Lista da CPU" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   Lista **da CPU**  
:::image-end:::  

### Acelerar somente a rede   

Para limitar apenas a rede e não a CPU, vá até **Network** o painel de rede **e selecione 3G** ou a **3G lento** na lista **aceleração** .  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Lista de aceleração" lightbox="../media/device-mode-network-throttle.msft.png":::
   Lista de **aceleração**  
:::image-end:::  

Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**, digite `3G` e selecione Habilitar a aceleração **3G rápida** ou **habilitar a limitação 3G lenta**.  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="O menu de comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   O **menu de comando**  
:::image-end:::  

Você também pode definir a limitação de rede no painel **desempenho** .  Clique em **configurações de captura** \ ( ![ capturar configurações ][ImageCaptureIcon] \) e, em seguida, selecione 3G **rápido** ou **3G lento** na lista **rede** .  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Definir a limitação de rede no painel desempenho" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   Definir a limitação de rede no painel **desempenho**  
:::image-end:::  

## Substituir geolocalização   

Para abrir a interface do usuário que substitui a localização geográfica, clique em **Personalizar e controle devtools** \ ( `...` \) e selecione **mais**  >  **sensores**de ferramentas.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **Sensores**  
:::image-end:::  

Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **Mostrar sensores**  
:::image-end:::  

Selecione uma das predefinições **na lista geolocalização** ou selecione **local personalizado** para inserir suas próprias coordenadas ou selecione **localização indisponível** para testar como a sua página se comporta quando a localização geográfica está em um estado de erro.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Geolocalização" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **Geolocalização**  
:::image-end:::  

## Definir orientação   

:::row:::
   :::column span="":::
      Para abrir a interface do usuário de orientação, clique em **Personalizar e controle devtools** `...` e selecione **mais**  >  **sensores**de ferramentas.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Ou pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o menu de comando, digite `Sensors` e selecione **Mostrar sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Selecione uma das predefinições na lista **orientação** ou selecione **orientação personalizada** para definir seus próprios valores Alfa, beta e gama.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Orientação" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **Orientação**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "comece a usar dispositivos Android de depuração remota | Documentos da Microsoft "  

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
