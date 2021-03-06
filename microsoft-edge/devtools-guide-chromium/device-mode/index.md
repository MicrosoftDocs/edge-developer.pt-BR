---
description: Use dispositivos virtuais no Microsoft Edge para criar sites móveis primeiro.
title: Emular dispositivos móveis no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, emulação, dispositivo, simulação, celular
ms.openlocfilehash: 1a83dece95acba386385bfea035a9e2c91639240
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398781"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a>Emular dispositivos móveis no Microsoft Edge DevTools  

Use **a emulação de dispositivo** para aproximar a aparência e a resposta da sua página em um dispositivo móvel.  O Microsoft Edge DevTools fornece uma coleção de recursos para ajudá-lo a emular dispositivos móveis.  A coleção inclui os seguintes recursos.  

*   [Simular um viewport móvel](#simulate-a-mobile-viewport)  
*   [Acelerar a rede](#throttle-the-network-only)  
*   [Acelerar a CPU](#throttle-the-cpu-only)  
*   [Simular localização geográfica](#override-geolocation)  
*   [Definir orientação](#set-orientation)  
*   [Definir a cadeia de caracteres do agente do usuário](#set-user-agent-string)  

## <a name="limitations"></a>Limitações  

**A emulação de dispositivo** [é][WikiApproximation] uma aproximação de primeira ordem da aparência da sua página em um dispositivo móvel.  **A emulação de dispositivo** não realmente executar seu código em um dispositivo móvel.  Em vez disso, você simula a experiência do usuário móvel do laptop ou da área de trabalho.  

Alguns aspectos de dispositivos móveis nunca são emulados no DevTools.  Por exemplo, a arquitetura das CPUs móveis é diferente da arquitetura de CPUs de laptop ou desktop.  Quando estiver em dúvida, sua melhor opção é realmente executar sua página em um dispositivo móvel.  Use [Depuração Remota][DevToolsRemoteDebugging] para interagir com o código de uma página do computador enquanto sua página é realmente executado em um dispositivo móvel.  Você pode exibir, alterar, depurar, perfil ou todos os quatro enquanto interage com o código.  Seu computador pode ser um bloco de anotações ou computador da área de trabalho.  

## <a name="simulate-a-mobile-viewport"></a>Simular um viewport móvel  

Escolha **Alternar** a emulação de dispositivo \( Toggle Device Toolbar \) ou escolha Personalizar e controlar ![ ][ImageDeviceToolbarIcon] **DevTools** \( `...` \) emulação **** de dispositivo > para abrir a interface do usuário que permite simular um modo de exibição móvel.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    A barra de ferramentas de dispositivo  
:::image-end:::  

Por padrão, a Barra de Ferramentas de Dispositivo é aberta no Modo de Exibição Responsivo.  

### <a name="responsive-viewport-mode"></a>Modo de exibição responsivo  

Para testar rapidamente a aparência da sua página em vários tamanhos de tela, arraste as alças para ressizer o viewport para suas dimensões necessárias.  Você também pode inserir valores específicos nas caixas de largura e altura.  Na figura a seguir, a largura é definida como `626` e a altura é definida como `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="As alças para alterar as dimensões do modo de exibição quando no Modo de Exibição Responsivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    As alças para alterar as dimensões do modo de exibição quando no Modo de Exibição Responsivo  
:::image-end:::  

#### <a name="show-media-queries"></a>Mostrar consultas de mídia  

Se você tiver definido consultas de mídia em sua página, pule para as dimensões do viewport onde essas consultas de mídia entrarão em vigor mostrando pontos de interrupção de consulta de mídia acima do seu viewport.  Escolha **Mais opções**Mostrar consultas de  >  **mídia**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas de mídia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Mostrar consultas de mídia**  
:::image-end:::  

Escolha um ponto de interrupção para alterar a largura do modo de exibição para que a consulta de mídia seja disparada.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Escolha um ponto de interrupção para alterar a largura do viewport" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Escolha um ponto de interrupção para alterar a largura do viewport  
:::image-end:::  

#### <a name="set-the-device-type"></a>Definir o tipo de dispositivo  

Use a **lista Tipo de** Dispositivo para simular um dispositivo móvel ou dispositivo de área de trabalho.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="A lista Tipo de Dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   A **lista Tipo de** Dispositivo  
:::image-end:::  

A tabela a seguir descreve as diferenças entre as opções de tipo de dispositivo disponível.  A coluna método Rendering refere-se a se o Microsoft Edge renderiza a página como um modo de exibição móvel ou de área de trabalho.  A coluna Ícone do Cursor refere-se a que tipo de cursor é exibido quando você passar o mouse na página.  A coluna Eventos disparados refere-se a se a página dispara ou ocorre `touch` `click` quando você interage com a página.  

| Opção | Método Rendering | Ícone do cursor | Eventos disparados |  
|:--- |:--- |:--- |:--- |  
| Dispositivos móveis | Dispositivos móveis | Circle | touch |  
| Mobile \(no touch\) | Dispositivos móveis | Normal |  escolha  |  
| Desktop | Desktop | Normal |  escolha  |  
| Área de trabalho \(touch\) | Desktop | Circle | touch |  

> [!NOTE]
> Se a **lista Tipo de** Dispositivo não for exibida, escolha **Mais**opções Adicionar tipo  >  **de dispositivo**.  

### <a name="mobile-device-viewport-mode"></a>Modo de exibição de dispositivo móvel  

Para simular as dimensões de um dispositivo móvel específico, selecione o dispositivo na **lista Dispositivo.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="A lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   A **lista de** dispositivos  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a>Girar o viewport para orientação paisagem  

Teste sua página da Web na orientação paisagem.  

*   Para girar o viewport para orientação paisagem, escolha **Girar** \( ![ Girar ][ImageRotateIcon] \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Página exibida na orientação paisagem" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Página exibida na orientação paisagem  
    :::image-end:::  
    
> [!NOTE]
> O **botão Girar** desaparecerá se a barra de ferramentas do **dispositivo** for estreita.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A **barra de ferramentas de dispositivo**  
:::image-end:::  

Para obter mais informações, navegue até [Definir orientação](#set-orientation).  

#### <a name="show-device-frame"></a>Mostrar quadro do dispositivo  

Exibe o quadro de dispositivo físico ao redor do visor quando você simula as dimensões de um dispositivo móvel específico, como um iPhone 6.  

1.  Abra **mais opções**.  
1.  Escolha **Mostrar quadro do dispositivo**.  

> [!NOTE]
> Se um quadro de dispositivo para um determinado dispositivo não for exibido, isso significa que o DevTools não tem arte para a opção.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar quadro do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Mostrar quadro do dispositivo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="O quadro do dispositivo para o iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         O quadro do dispositivo para o iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a>Adicionar um dispositivo móvel personalizado  

Se a opção de dispositivo móvel de que você precisa não estiver incluída na lista padrão, você poderá adicionar um dispositivo personalizado.  Para adicionar um dispositivo personalizado, conclua as etapas a seguir.  

1.  Escolha a **lista De** dispositivos > **Editar**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Escolha Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Escolha **Editar**  
    :::image-end:::  
    
1.  Escolha **Adicionar dispositivo personalizado**.  
1.  Em **Dispositivos Emulados,** insira um nome de dispositivo, largura de tela e altura da tela para o dispositivo personalizado.  A [taxa de pixel do dispositivo,][MDNWindowDevicePixelRatio]a cadeia de [caracteres][MDNUserAgent]do agente do usuário e os campos de tipo [de](#set-the-device-type) dispositivo são opcionais.  O campo tipo de dispositivo padrão para **Mobile**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Criar um dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Criar um dispositivo personalizado  
    :::image-end:::  
    
### <a name="show-rulers"></a>Mostrar réguas  

Se você precisar medir dimensões de tela, poderá usar réguas para medir o tamanho da tela em pixels.  Escolha **Mais opções**Mostrar  >  **réguas** para exibir réguas acima e à esquerda do visor.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Item de menu para exibir réguas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Item de menu para exibir réguas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Réguas acima e à esquerda do viewport" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Réguas acima e à esquerda do viewport  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a>Ampliar o viewport  

Para testar a aparência da sua página em vários níveis de zoom, use a **lista Zoom** para ampliar ou diminuir o zoom.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a>Acelerar a rede e a CPU  

Dispositivos móveis geralmente têm restrições de rede e CPU.  Certifique-se de testar a rapidez com que sua página é carregada e como ela responde em velocidades diferentes da Internet e da CPU.  

Reduza a rede e a CPU.  

1.  Escolha **Lista de** aceleração e altere a predefinição para celular de camada **média** ou **celular low-end.**  
    *   **O dispositivo móvel de** camada intermediária `fast 3G` simula e acelera sua CPU.  É quatro vezes mais lento do que o normal.  
    *   **O celular de baixo** nível simula `slow 3G` e acelera sua CPU.  É seis vezes mais lento do que o normal.  
    
Toda a throttling se baseia na funcionalidade normal do laptop ou da área de trabalho.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="A lista De aceleração na barra de ferramentas do dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   A **lista De** aceleração na barra de ferramentas do dispositivo  
:::image-end:::  

> [!NOTE]
> Se a **lista De limitação** estiver oculta, sua Barra de **Ferramentas de Dispositivo** será muito estreita.  Para acessar a **lista De aceleração,** aumente a largura da Barra **de Ferramentas de Dispositivo**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="A barra de ferramentas de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   A **barra de ferramentas de dispositivo**  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a>Acelerar somente a CPU  

Para acelerar apenas a CPU e não a rede, conclua as etapas a seguir.

1.  Escolha o **painel Desempenho** e escolha **Configurações de** Captura \( ![ Configurações de Captura ][ImageCaptureIcon] \).
1.  Escolha **a lentidão**da CPU  >  **4x** ou **6x de lentidão**.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="A lista de CPU no painel Desempenho" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       A **lista de CPU** no painel **Desempenho**  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a>Apenas acelerar a rede  

Para acelerar apenas a rede, conclua as etapas a seguir.

1.  Escolha a **ferramenta Rede.**
1.  Escolha **Online**  >  **Fast 3G** ou Slow **3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="A lista De aceleração no painel Rede" lightbox="../media/device-mode-network-throttle.msft.png":::
       A **lista De** aceleração no painel Rede  
    :::image-end:::  
    
    Ou selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) **** `3G` **** **** para abrir o Menu de Comando , digite e escolha Habilitar a desaceleração 3G rápida ou Habilitar a desaceleração lenta do 3G .  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="O Menu De comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       O **Menu De comando**  
    :::image-end:::  
    
Você também pode definir a throttling de rede a partir do **painel Desempenho.**  

1.  Escolha **Configurações de** Captura \( Configurações de Captura \) e escolha a lista Rede e altere a ![ ][ImageCaptureIcon] predefinição para Fast **3G** ou **Slow 3G**. ****  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Definir a throttling de rede do painel Desempenho" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Definir a throttling de rede do **painel Desempenho**  
    :::image-end:::  
    
## <a name="override-geolocation"></a>Substituir geolocalização  

:::row:::
   :::column span="":::
      Se sua página depender das informações de localização geográfica de um dispositivo móvel para renderizar corretamente, forneça diferentes localizações geográficas usando a interface do usuário de sobrelocação geográfica.  

      1.  Escolha **Personalizar e controlar o DevTools** \( `...` \) > Mais sensores de ****  >  **ferramentas.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores para localização geográfica" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** para localização geográfica  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abra o Menu de Comando.  
          *   Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).  
      1. Digite `Sensors` e escolha Mostrar **Sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar Sensores para localização geográfica" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar Sensores** para localização geográfica  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

No painel **Sensores,** você pode selecionar um dos locais predefinidos incluídos no DevTools usando o **menu** suspenso Local.  Para inserir um local personalizado, escolha **Outro...** e insira as coordenadas de sua localização personalizada.  Para testar sua página em um estado de erro quando as informações de local não estão disponíveis, escolha **Local indisponível**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Painel sensores com um local predefinido selecionado" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    **Painel** de sensores com um local predefinido selecionado.  
:::image-end:::

## <a name="set-orientation"></a>Definir orientação  

:::row:::
   :::column span="":::
      Se sua página depender das informações de orientação de um dispositivo móvel para renderizar corretamente, abra a interface do usuário de orientação.  

      1.  Escolha **Personalizar e controlar o DevTools** \( `...` \) > Mais sensores de ****  >  **ferramentas.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores para orientação" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** para orientação  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abra o Menu de Comando.  
          *   Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).  
      1. Digite `Sensors` e escolha Mostrar **Sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar Sensores para orientação" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar Sensores** para orientação  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

No painel **Sensores,** você pode selecionar uma orientação predefinida no menu suspenso **Orientação.**  Para inserir sua própria orientação, escolha **Orientação personalizada**e insira seus próprios valores [alfa,][MDNDeviceOrientaitonAlpha] [beta][MDNDeviceOrientaitonBeta]e [gama.][MDNDeviceOrientaitonGamma]  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Opções de orientação no painel Sensores" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    **Opções** de orientação no painel **Sensores**  
:::image-end:::  

## <a name="set-user-agent-string"></a>Definir cadeia de caracteres de agente do usuário  

:::row:::
   :::column span="":::
      Se sua página depender da cadeia de caracteres do **** agente do usuário de um dispositivo móvel para renderizar corretamente, use o painel Condições de rede para fornecer cadeias de caracteres de agente de usuário diferentes.  
      
      1.  Escolha **Personalizar e controlar o DevTools** \( `...` \) > Mais **ferramentas**Condições  >  **de rede**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrada de condições de rede no menu Mais ferramentas" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         **Entrada de condições** de rede no menu **Mais ferramentas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abra o Menu de Comando.  
          *   Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).  
      1. Digite `Network conditions` e escolha Mostrar condições de **rede**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Mostrar condições de rede" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Mostrar condições de rede**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Ao lado **de Agente de usuário,** desempure a **caixa de seleção Selecionar** automaticamente.  Em seguida, escolha **Personalizado...** para selecionar em uma lista de cadeias de caracteres de agente de usuário predefinidos.  Para inserir sua própria cadeia de caracteres de agente de usuário, insira a cadeia de caracteres em **Enter a custom user agent**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Definir a cadeia de caracteres de agente do usuário como Microsoft Edge no macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Definir a cadeia de caracteres de agente do usuário como Microsoft Edge no macOS  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Começar com a depuração remota de dispositivos Android | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "User Agent | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordem de Aproximação - Primeira Ordem - Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
