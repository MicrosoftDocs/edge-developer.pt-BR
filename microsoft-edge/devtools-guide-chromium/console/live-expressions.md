---
title: Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: c388e44ca5507dd88ad9ad7b7ee985e658dfc569
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601737"
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





# Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas   

  

Se você mesmo digitar a mesma expressão de JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.  Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.  O valor da expressão é atualizado em tempo real quase em tempo real.  

## Criar uma expressão ao vivo   

1.  [Abra o console][DevToolsConsoleReferenceOpenConsole].  
1.  Clique em **criar** expressão ao vivo ![ criar uma expressão ao vivo ][ImageCreateLiveExpressionIcon] .  A caixa de texto **expressão ao vivo** é exibida.  
    
    > ##### Figura 1  
    > Digitando `document.activeElement` na caixa de texto **expressão dinâmica**  
    > ![Digitando documento. ActiveElement na caixa de texto expressão dinâmica][ImageLiveExpressionTextbox]  
    
1.  Digite `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para salvar a expressão ou clique fora da caixa de texto **expressão ao vivo** .  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpressionTextbox]: /microsoft-edge/devtools-guide-chromium/media/console-create-live-expression.msft.png "Figura 1: digitando documento. ActiveElement na caixa de texto expressão dinâmica"  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console "Abrir o console-referência do console"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
