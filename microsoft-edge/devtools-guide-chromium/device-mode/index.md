---
description: Use dispositivos virtuais no Microsoft Edge para criar sites do primeiro celular.
title: Emular dispositivos móveis no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, emulação, dispositivo, simulação, celular
ms.openlocfilehash: 8b636a20fcb1c55630009031ec8bf300624d03d7
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125101"
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

# Emular dispositivos móveis no Microsoft Edge DevTools  

Use a **emulação de dispositivo** para aproximar a aparência da página e responder em um dispositivo móvel.  O Microsoft Edge DevTools fornece um conjunto de recursos para ajudá-lo a emular dispositivos móveis.  A coleção inclui os recursos a seguir.  

*   [Simular um visor móvel](#simulate-a-mobile-viewport)  
*   [Acelerar a rede](#throttle-the-network-only)  
*   [Acelerar a CPU](#throttle-the-cpu-only)  
*   [Simular geolocalização](#override-geolocation)  
*   [Definir orientação](#set-orientation)  
*   [Definir a cadeia de caracteres do agente do usuário](#set-user-agent-string)  

## Limitações  

**Emulação de dispositivo** é uma [aproximação de primeira ordem][WikiApproximation] da aparência da sua página em um dispositivo móvel.  A **emulação de dispositivo** não executa realmente o código em um dispositivo móvel.  Em vez disso, você simula a experiência do usuário móvel do laptop ou da área de trabalho.  

Alguns aspectos de dispositivos móveis nunca são emulados no DevTools.  Por exemplo, a arquitetura de CPUs móveis é diferente da arquitetura de CPUs para laptop ou desktop.  Quando estiver em dúvida, a melhor opção é realmente executar sua página em um dispositivo móvel.  Use [depuração remota] [DevToolsRemoteDebugging] para interagir com o código de uma página de seu computador enquanto sua página realmente é executada em um dispositivo móvel.  Você pode exibir, alterar, depurar, criar perfil ou todos os quatro enquanto interage com o código.  Seu computador pode ser um notebook ou computador de mesa.  

## Simular um visor móvel  

Escolha **alternar emulação de dispositivo**  \ ( ![ alternar barra de ferramentas de dispositivo ][ImageDeviceToolbarIcon] \) ou escolha **Personalizar e controlar devtools** \ ( `...` \) > **emulação de dispositivo** para abrir a interface do usuário que permite simular um visor móvel.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    A barra de ferramentas do dispositivo  
:::image-end:::  

Por padrão, a barra de ferramentas do dispositivo é aberta no modo de visor responsivo.  

### Modo de visor responsivo  

Para testar rapidamente a aparência da sua página em vários tamanhos de tela, arraste as alças para redimensionar o visor para suas dimensões obrigatórias.  Você também pode inserir valores específicos nas caixas largura e altura.  Na figura a seguir, a largura é definida como `626` e a altura é definida como `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    As alças para alterar as dimensões do visor quando no modo de visor responsivo  
:::image-end:::  

#### Mostrar consultas de mídia  

Se você definiu consultas de mídia em sua página, vá para as dimensões do visor em que essas consultas de mídia entram em vigor mostrando pontos de interrupção de consulta de mídia acima do visor.  Escolha **mais opções**  >  **Mostrar consultas de mídia**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Mostrar consultas de mídia**  
:::image-end:::  

Escolha um ponto de interrupção para alterar a largura do visor para que a consulta de mídia seja disparada.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Escolher um ponto de interrupção para alterar a largura do visor  
:::image-end:::  

#### Definir o tipo de dispositivo  

Use a lista **tipo de dispositivo** para simular um dispositivo móvel ou um dispositivo de desktop.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   A lista **tipo de dispositivo**  
:::image-end:::  

A tabela a seguir descreve as diferenças entre as opções de tipo de dispositivo disponíveis.  A coluna método de renderização refere-se ao Microsoft Edge renderiza a página como um visor móvel ou da área de trabalho.  A coluna do ícone do cursor refere-se ao tipo de cursor que você vê quando passa o mouse sobre a página.  A coluna eventos disparados se refere a um gatilho de página `touch` ou `click` eventos quando você interage com a página.  

| Opção | Método de renderização | Ícone de cursor | Eventos disparados |  
|:--- |:--- |:--- |:--- |  
| Dispositivos móveis | Dispositivos móveis | Circle | touch |  
| Celular \ (sem toque \) | Dispositivos móveis | Normal |  clique em  |  
| Desktop | Desktop | Normal |  clique em  |  
| Área de trabalho \ (Touch \) | Desktop | Circle | touch |  

> [!NOTE]
> Se a lista **tipo de dispositivo** não for exibida, escolha **mais opções**  >  **Adicionar tipo de dispositivo**.  

### Modo visor do dispositivo móvel  

Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na lista de **dispositivos** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Lista de **dispositivos**  
:::image-end:::  

#### Girar o visor para a orientação paisagem  

Teste sua página da Web na orientação paisagem.  

*   Para girar o visor para a orientação paisagem, escolha **girar** \ ( ![ girar ][ImageRotateIcon] \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Página exibida na orientação paisagem  
    :::image-end:::  
    
> [!NOTE]
> O botão **girar** desaparecerá se a **barra de ferramentas** do seu dispositivo for estreita.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A **barra de ferramentas do dispositivo**  
:::image-end:::  

Para obter mais informações, vá para [definir orientação](#set-orientation).  

#### Mostrar quadro de dispositivo  

Exiba o quadro do dispositivo físico ao lado do visor ao simular as dimensões de um dispositivo móvel específico, como um iPhone 6.  

1.  Abrir **mais opções**.  
1.  Escolha **Mostrar quadro de dispositivo**.  

> [!NOTE]
> Se você não vir um quadro de dispositivo para um dispositivo específico, isso significa que o DevTools não tem arte para essa opção.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Mostrar quadro de dispositivo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         O quadro do dispositivo para o iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Adicionar um dispositivo móvel personalizado  

Se a opção de dispositivo móvel necessária não estiver incluída na lista padrão, você poderá adicionar um dispositivo personalizado.  Para adicionar um dispositivo personalizado, conclua as etapas a seguir.  

1.  Escolha a lista de **dispositivos** > **Editar**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Escolha **Editar**  
    :::image-end:::  
    
1.  Escolha **Adicionar dispositivo personalizado**.  
1.  Em **dispositivos emulados**, insira um nome de dispositivo, a largura da tela e a altura da tela do dispositivo personalizado.  A [taxa de pixels de dispositivo][MDNWindowDevicePixelRatio], a [cadeia de caracteres do agente do usuário][MDNUserAgent]e os campos do tipo de [dispositivo](#set-the-device-type) são opcionais.  O campo tipo de dispositivo é definido como padrão para **celular**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Criar um dispositivo personalizado  
    :::image-end:::  
    
### Mostrar réguas  

Se precisar medir as dimensões da tela, você pode usar réguas para medir o tamanho da tela em pixels.  Escolha **mais opções**  >  **Mostrar réguas** para exibir réguas acima e à esquerda do visor.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Item de menu para exibir réguas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Réguas acima e à esquerda da viewport  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Aplicar zoom ao visor  

Para testar a aparência da sua página em vários níveis de zoom, use a lista de **zoom** para ampliar ou reduzir.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Acelerar a rede e a CPU  

Os dispositivos móveis geralmente têm restrições de rede e CPU.  Certifique-se de testar a rapidez com que sua página é carregada e como ela responde em velocidades de CPU e de Internet diferentes.  

Acelera a rede e a CPU.  

1.  Escolha lista de **aceleração** e altere a predefinição para móvel médio ou **celular de baixo** **nível** .  
    *   O **celular de nível intermediário** simula `fast 3G` e acelera a CPU.  É quatro vezes mais lento do que o normal.  
    *   O **celular low-end** simula `slow 3G` e acelera a CPU.  É seis vezes mais lento do que o normal.  
    
Toda a limitação se baseia na funcionalidade normal do laptop ou da área de trabalho.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   A lista de **aceleração** na barra de ferramentas do dispositivo  
:::image-end:::  

> [!NOTE]
> Se a **lista de aceleração** estiver oculta, a **barra de ferramentas** do seu dispositivo é estreita demais.  Para acessar a **lista de aceleração**, aumente a largura da **barra de ferramentas do dispositivo**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A **barra de ferramentas do dispositivo**  
:::image-end:::  

### Acelerar apenas a CPU  

Para acelerar apenas a CPU e não a rede, conclua as etapas a seguir.

1.  Escolha o painel **desempenho** e escolha **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureIcon] \).
1.  Escolha a **CPU**  >  **4x lentidão** ou **lentidão 6x**.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Lista **CPU** no painel **desempenho**  
    :::image-end:::  
    
### Acelerar somente a rede  

Para controlar apenas a rede, conclua as etapas a seguir.

1.  Escolha o painel **rede** .
1.  Escolha **online**  >  **Fast 3G** ou **3G lento**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-network-throttle.msft.png":::
       A lista de **aceleração** no painel de rede  
    :::image-end:::  
    
    Ou selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) para abrir o **menu de comando**, digite `3G` e escolha **habilitar a limitação de 3G rápido** ou **habilitar a limitação 3G lenta**.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       O **menu de comando**  
    :::image-end:::  
    
Você também pode definir a limitação de rede no painel **desempenho** .  

1.  Escolha **configurações de captura** \ ( ![ configurações de captura ][ImageCaptureIcon] \) e escolha a lista de **redes** e altere a predefinição para 3G **rápido** ou **3G lento**.  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Definir a limitação de rede no painel **desempenho**  
    :::image-end:::  
    
## Substituir geolocalização  

:::row:::
   :::column span="":::
      Se sua página depende de informações de localização geográfica de um dispositivo móvel para renderização apropriada, forneça geolocalidades diferentes usando a interface do usuário de substituição de localização geográfica.  

      1.  Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais**  >  **sensores**de ferramentas.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** de localização geográfica  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abrir o menu de comandos.  
          *   Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \).  
      1. Digite `Sensors` e escolha **Mostrar sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores** de localização geográfica  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

No painel **sensores** , você pode selecionar um dos locais predefinidos incluídos no devtools usando o menu suspenso **Location** .  Para inserir um local personalizado, escolha **outros...** e insira as coordenadas do seu local personalizado.  Para testar sua página em um estado de erro quando as informações de localização não estiverem disponíveis, escolha **local indisponível**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    Painel de **sensores** com um local predefinido selecionado.  
:::image-end:::

## Definir orientação  

:::row:::
   :::column span="":::
      Se sua página depende de informações de orientação de um dispositivo móvel para renderização apropriada, abra a interface do usuário de orientação.  

      1.  Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais**  >  **sensores**de ferramentas.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** para orientação  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abrir o menu de comandos.  
          *   Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \).  
      1. Digite `Sensors` e escolha **Mostrar sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores** para orientação  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

No painel **sensores** , você pode selecionar uma orientação predefinida no menu suspenso **orientação** .  Para inserir sua própria orientação, escolha **orientação personalizada**e insira seus próprios valores [alfa][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta]e [gama][MDNDeviceOrientaitonGamma] .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    Opções de **orientação** no painel **sensores**  
:::image-end:::  

## Definir cadeia de caracteres do agente do usuário  

:::row:::
   :::column span="":::
      Se sua página depende da cadeia de caracteres do agente do usuário de um dispositivo móvel para renderizar corretamente, use o painel de **condições de rede** para fornecer diferentes cadeias de agente do usuário.  
      
      1.  Escolha **Personalizar e controle devtools** \ ( `...` \) > **mais ferramentas**  >  **condições de rede**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         Entrada de **condições de rede** no menu **mais ferramentas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abrir o menu de comandos.  
          *   Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \).  
      1. Digite `Network conditions` e escolha **Mostrar condições de rede**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Mostrar condições de rede**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Ao lado de **agente do usuário**, desmarque a caixa de seleção **selecionar automaticamente** .  Em seguida, escolha **personalizado...** para selecionar em uma lista de cadeias de caracteres de agente do usuário predefinidas.  Para inserir sua cadeia de caracteres de agente do usuário, insira a cadeia de caracteres em **digite um agente de usuário personalizado**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="A barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Definir a cadeia de caracteres do agente do usuário como Microsoft Edge no macOS  
:::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "comece a usar dispositivos Android de depuração remota | Documentos da Microsoft "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuário | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. alfa | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. gama | MDN"  

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
