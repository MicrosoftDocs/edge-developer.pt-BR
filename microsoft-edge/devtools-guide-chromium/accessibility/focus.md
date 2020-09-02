---
title: Acompanhar Qual Elemento Tem o Foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5261824b725384240453f216071255494e88e98d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991173"
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

# Acompanhar Qual Elemento Tem o Foco  

Suponha que você esteja testando o acesso à navegação pelo teclado de uma página.  Ao navegar a página com a `Tab` chave, o anel de foco às vezes desaparece porque o elemento que tem o foco está oculto.  

Conclua as ações a seguir para acompanhar o elemento focalizado no DevTools.  

1.  Abra o **console**.  
1.  Clique em **criar expressão ao vivo** \ ( ![ criar expressão ao vivo ][ImageCreateIcon] \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Criar uma expressão ao vivo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Criar uma expressão ao vivo  
    :::image-end:::  
    
1.  Digite `document.activeElement`.  
1.  Clique fora da interface de usuário do **Live Expression** para salvar.  
    
O valor que você vê abaixo `document.activeElement` é o resultado da expressão.  

Como essa expressão sempre representa o elemento destaques, agora você tem uma maneira de sempre manter o controle de qual elemento está focalizado.  

*   Passe o mouse sobre o resultado para realçar o elemento focalizado no visor.  
*   Clique com o botão direito do mouse no resultado e selecione **revelar no painel de elementos** para mostrar o elemento na árvore DOM do painel **elementos** .  
*   Clique com o botão direito do mouse no resultado e selecione **armazenar como variável global** para criar uma referência de variável para o nó que você pode usar no **console**.  

## Entrar em contato com a equipe do Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
