---
title: Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601343"
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





# Alterar o posicionamento do Microsoft Edge DevTools (desencaixar, encaixar na parte inferior, encaixar à esquerda)   



Por padrão, o DevTools está encaixado à direita do seu visor.  Você também pode encaixar na parte inferior, encaixar à esquerda ou desencaixar o DevTools em uma janela separada.  

> ##### Figura 1  
> Encaixar à esquerda  
> ![Encaixar à esquerda][ImageDockLeft]  

> ##### Figura 2  
> Encaixar na parte inferior  
> ![Encaixar na parte inferior][ImageDockBottom]  

> ##### Figura 3  
> Navegador em janela separada  
> ![Navegador em janela separada][ImageUndockBrowser]  

> ##### Figura 4  
> DevTools desencaixada em janela separada  
> ![DevTools desencaixada em janela separada][ImageUndockDevTools]  

## Alterar o posicionamento a partir do menu principal   

1.  Clique em **Personalizar e controle devtools** `...` e selecione desencaixar em desencaixar de **janela separado** ![ ][ImageUndockIcon] , **encaixar na barra inferior** ![ para baixo ][ImageBottomIcon] ou **encaixar à esquerda** para a ![ esquerda ][ImageLeftIcon] .  
    
    > ##### Figura 5  
    > Selecionar **desencaixar em uma janela separada**  
    > ![Selecionar desencaixar em uma janela separada][ImageUndockSettings]  
    
## Alterar o posicionamento no menu de comando   

1.  [Abrir o menu de comandos][DevtoolsCommandMenu].  
1.  Execute um dos seguintes comandos: `Dock To Bottom` , `Undock Into Separate Window` .  No momento, não há um comando para encaixar à esquerda, mas você pode acessá-lo no [menu principal](#change-placement-from-the-main-menu).  
    
    > ##### Figura 6  
    > O comando desencaixar  
    > ![O comando desencaixar][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Figura 1: encaixar à esquerda"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Figura 2: encaixar na parte inferior"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Figura 3: navegador em uma janela separada"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Figura 4: DevTools desencaixada em janela separada"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Figura 5: selecionando desencaixar em uma janela separada"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Figura 6: o comando desencaixar"  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/customize/placement) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
