---
description: Uma lista de maneiras de personalizar o Microsoft Edge DevTools
title: Personalizar o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 682ff78b6a5272c1f6462648d64241448838edac
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11189967"
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

# Personalizar o Microsoft Edge DevTools  

Esta página lista as maneiras de personalizar o Microsoft Edge DevTools.  

## Configurações  

**Configurações**  >  de As **preferências** contêm muitas opções para personalizar o devtools.  

Para abrir as configurações, execute uma das seguintes ações.  

*   Selecione `F1` enquanto o devtools está em foco.  
*   Abra o **menu principal** e, em seguida, escolha **configurações**.  
    
:::image type="complex" source="../media/customize-settings-preferences.msft.png" alt-text="Configurações" lightbox="../media/customize-settings-preferences.msft.png":::
   **Configurações**  
:::image-end:::  

## Arquiva  

A **gaveta** é um segundo painel onde as ferramentas da sua escolha são exibidas.  

Para abrir \ (ou fechar \) a **gaveta**, selecione `Escape` .  

:::image type="complex" source="../media/customize-drawer-open.msft.png" alt-text="A gaveta" lightbox="../media/customize-drawer-open.msft.png":::
   A **gaveta**  
:::image-end:::  

Por padrão, algumas ferramentas abrem no painel principal, enquanto outras são exibidas na **gaveta**.  Escolha **mais** \ ( `...` ) para abrir uma ferramenta na **gaveta**.  

:::image type="complex" source="../media/customize-drawer-open-more-tools.msft.png" alt-text="O botão para abrir a gaveta" lightbox="../media/customize-drawer-open-more-tools.msft.png":::
   O botão para abrir a **gaveta**  
:::image-end:::  

Você pode mover ferramentas entre o painel principal e a gaveta.  

*   Para mover uma ferramenta da gaveta para o painel principal, passe o mouse sobre uma ferramenta, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o início**.  
    
    :::image type="complex" source="../media/move-from-drawer.msft.png" alt-text="Mover a ferramenta da gaveta para o painel principal" lightbox="../media/move-from-drawer.msft.png":::
       Mover a ferramenta da **gaveta** para o painel principal  
    :::image-end:::  
    
*   Para mover uma ferramenta do painel principal para a gaveta, passe o mouse sobre uma ferramenta, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **mover para o fim**.  
    
    :::image type="complex" source="../media/move-to-drawer.msft.png" alt-text="Mover a ferramenta do painel principal para a gaveta" lightbox="../media/move-to-drawer.msft.png":::
       Mover a ferramenta do painel principal para a **gaveta**
    :::image-end:::  
    

## Reordenar painéis  

Escolha e arraste uma ferramenta para alterar a ordem.  Sua ordem de ferramenta personalizada persiste entre as sessões do DevTools.  

> [!NOTE]
> Por padrão, a ferramenta de **rede** geralmente é a quarta da esquerda.  Na figura a seguir, o painel de **rede** é o primeiro à esquerda.  

:::image type="complex" source="../media/customize-network-first-position.msft.png" alt-text="Ordem personalizada de devtools em um painel" lightbox="../media/customize-network-first-position.msft.png":::
   Ordem personalizada de devtools em um painel  
:::image-end:::  

## Alterar o posicionamento do DevTools  

Consulte [posicionamento do Microsoft Edge devtools][DevToolsPlacement].  

:::image type="complex" source="../media/customize-dev-tools-dock-side.msft.png" alt-text="DevTools desencaixado" lightbox="../media/customize-dev-tools-dock-side.msft.png":::
   DevTools desencaixado  
:::image-end:::  

## Tema escuro  

Consulte [habilitar tema escuro][DarkTheme].  

:::image type="complex" source="../media/customize-settings-appearance-theme.msft.png" alt-text="O tema escuro" lightbox="../media/customize-settings-appearance-theme.msft.png":::
   O tema escuro  
:::image-end:::  

## Experimentos  

Para habilitar experimentos do DevTools, conclua as ações a seguir.  

1.  Navegue até `edge://flags/#enable-devtools-experiments` .  
1.  Escolha **habilitar**.  
1.  Escolha **reiniciar agora**, na parte inferior da página.  

Da próxima vez que você abrir o DevTools, uma nova página chamada **experimentos** será exibida em [configurações](#settings).  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreIcon]: ../media/more-icon.msft.png  

<!-- links -->  

[DevToolsPlacement]: ./placement.md "Alterar o posicionamento do Microsoft Edge DevTools | Documentos da Microsoft"  
[DarkTheme]: ./dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Documentos da Microsoft"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/customize/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
