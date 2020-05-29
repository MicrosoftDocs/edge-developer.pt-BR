---
title: Marcar scripts de conteúdo como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581786"
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





# Marcar scripts de conteúdo como código de biblioteca   



Ao usar o painel **fontes** do Microsoft Edge devtools para percorrer o [código][DevToolsJavascriptStepThroughCode], às vezes, você pode pausar o código que não reconhece.  Você provavelmente pausou no código de uma das extensões do Microsoft Edge instaladas.  Conclua as etapas a seguir para não pausar no código de extensão.  

1.  Abra o DevTools, selecione **Personalizar e controle devtools** `...` e clique em **configurações**.  Você também pode abrir **as configurações** pressionando `F1` .  

1.  Selecione a guia **código de biblioteca** que abre a seção de código da biblioteca de **estrutura** de **configurações**.  
1.  Habilite a caixa de seleção **Marcar scripts de conteúdo como código de biblioteca** .  
    
    > ##### Figura 1  
    > Habilitar a caixa de seleção **Marcar scripts de conteúdo como código de biblioteca**  
    > ![Habilitar a caixa de seleção Marcar scripts de conteúdo como código de biblioteca][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Figura 1: habilitar a caixa de seleção Marcar scripts de conteúdo como código de biblioteca"  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Etapa 4: percorrer o código-introdução à depuração JavaScript no Microsoft Edge DevTools"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
