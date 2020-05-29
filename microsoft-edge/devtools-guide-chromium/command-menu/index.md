---
title: Executar comandos com o menu de comando do Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601744"
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





# Executar comandos com o menu de comando do Microsoft Edge DevTools   

  

O menu de comando fornece uma maneira rápida de navegar na interface do usuário do Microsoft Edge DevTools e realizar tarefas comuns, como [desabilitar o JavaScript][JavascriptDisable].  Você pode estar familiarizado com um recurso semelhante no código do Visual Studio chamado de [paleta de comandos][VisualStudioCodeUICommandPalette], que era a inspiração original para o menu de comando.  

> ##### Figura 1  
> Usar o menu de comandos para desativar o JavaScript  
> ![Usar o menu de comandos para desativar o JavaScript][ImageDisableJS]  

## Abrir o menu de comandos   

Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \). Ou clique em **Personalizar e controlar devtools** `...` e, em seguida, selecione **executar comando**.  

> ##### Figura 2  
> Comando executar  
> ![Comando executar][ImageRunCommand]  

## Ver outras ações disponíveis   

Se você usar o fluxo de trabalho descrito em [abrir o menu de comando](#open-the-command-menu), o menu de comandos será aberto com um `>` caractere colocado na caixa de texto do menu de comandos.  

> ##### Figura 3  
> O caractere de comando  
> ![O caractere de comando][ImageCommandCharacter]  

Exclua o `>` caractere e digite `?` para ver outras ações que estão disponíveis no menu de comando.  

> ##### Figura 4  
> Outras ações disponíveis  
> ![Outras ações disponíveis][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Figura 1: usar o menu de comando para desabilitar o JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Figura 2: comando executar"  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Figura 3: o caractere de comando"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Figura 4: outras ações disponíveis"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Desabilitar JavaScript com o Microsoft Edge DevTools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos-UI de código do Visual Studio"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
