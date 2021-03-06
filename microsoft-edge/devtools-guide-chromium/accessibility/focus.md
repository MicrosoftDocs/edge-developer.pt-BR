---
description: Abra o Console, crie uma Expressão Ativa e dejuste a expressão como document.activeElement.
title: Acompanhar qual elemento tem o foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2fd53caccefefb0b0bce4b5c82f30632e11a3cb6
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597107"
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
# <a name="track-which-element-has-focus"></a>Acompanhar qual elemento tem o foco  

Suponha que você está testando a acessibilidade de navegação do teclado de uma página.  Ao navegar pela página com a chave, o anel de foco às vezes desaparece porque o elemento que `Tab` tem foco está oculto.  

Para rastrear o elemento focado no DevTools:

1.  Abra o **Console**.  
1.  Escolha **Criar expressão ao vivo** \( Criar expressão ao vivo ![ ](../media/create-live-expression-icon.msft.png) \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Criar uma expressão ao vivo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Criar uma expressão ao vivo  
    :::image-end:::  
    
1.  Digite `document.activeElement`.  
1.  Para salvar a expressão, selecione fora da expressão ao vivo.
    
O valor exibido abaixo `document.activeElement` é o resultado da expressão.  

Como essa expressão sempre representa o elemento focado, agora você tem uma maneira de sempre acompanhar qual elemento tem foco.  

*   Passe o mouse no resultado para realçar o elemento focado no viewport.  
*   Passe o mouse no resultado, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Revelar** em Elementos painel para mostrar o elemento na Árvore DOM na **ferramenta Elementos.**  
*   Passe o mouse no resultado, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Store como **variável global** para criar uma referência variável ao nó que você pode usar no **Console**.  


## <a name="see-also"></a>Consulte também

*  [Analise a falta de indicação do foco do teclado em um menu de barra lateral](test-analyze-no-focus-indicator.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
