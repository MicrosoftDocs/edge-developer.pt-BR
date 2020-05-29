---
title: Acompanhar qual elemento está focalizado
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: a1bcb7e97357d1348b363ecd4842d1b6a78feb45
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581528"
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





# Acompanhar qual elemento está focalizado   



Suponha que você esteja testando o acesso à navegação pelo teclado de uma página.  Ao navegar a página com a `Tab` chave, o anel de foco às vezes desaparece porque o elemento que tem o foco está oculto.  Para acompanhar o elemento focalizado no DevTools:  

1.  Abra o **console**.  
1.  Clique em **criar** expressão ao vivo ![ criar uma expressão ao vivo ][ImageCreateIcon] .  

    > ##### Figura 1  
    > Criando uma **expressão ao vivo**  
    > ![Criando uma expressão ao vivo][ImageLiveExpression]  
    
1.  Digite `document.activeElement`.
1.  Clique fora da interface de usuário do **Live Expression** para salvar.

O valor que você vê abaixo `document.activeElement` é o resultado da expressão.  
Como essa expressão sempre representa o elemento destaques, agora você tem uma maneira de sempre manter o controle de qual elemento está focalizado.  

*   Passe o mouse sobre o resultado para realçar o elemento focalizado no visor.  
*   Clique com o botão direito do mouse no resultado e selecione **revelar no painel de elementos** para mostrar o elemento na árvore DOM do painel **elementos** .  
*   Clique com o botão direito do mouse no resultado e selecione **armazenar como variável global** para criar uma referência de variável para o nó que você pode usar no **console**.  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCreateIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpression]: /microsoft-edge/devtools-guide-chromium/media/accessibility-console-create-live-expression-empty.msft.png "Figura 1: criando uma expressão ao vivo"  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
