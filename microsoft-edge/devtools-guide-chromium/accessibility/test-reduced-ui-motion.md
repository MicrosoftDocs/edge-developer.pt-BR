---
description: Verifique se as páginas da Web são usáveis com a animação da interface do usuário desligada (movimento reduzido) usando o recurso de mídia CSS emular prefere a lista suspensa de movimento reduzido na ferramenta Rendering.
title: Verifique se a página pode ser usada com a animação da interface do usuário desligada
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597171"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a>Verifique se a página pode ser usada com a animação da interface do usuário desligada

Uma página da Web não deve mostrar animações para um usuário que desligou animações no sistema operacional.  As animações podem ajudar a usabilidade de um produto, mas também podem causar distrações, confusão ou enjoo.

Para verificar se uma página da Web pode ser usada com a animação da interface do usuário desligada (movimento reduzido), na ferramenta **Renderização,** use o recurso de mídia **CSS emular** prefere a lista suspensa de movimento reduzido.

Na página da Web de demonstração de teste de acessibilidade, quando você desativar animações no sistema operacional ou emular essas configurações usando DevTools, a página da Web não usa rolagem suave quando você seleciona os links do menu de navegação de barra lateral.  Isso é obtido envolvendo a configuração de rolagem suave em CSS em uma consulta de mídia e, em seguida, usando a ferramenta **Rendering** para emular a configuração do sistema operacional para animação reduzida.

Para verificar se a página pode ser usável com animações desligadas:

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.

1.  Na parte superior do DevTools, selecione a ferramenta **Fontes** e, no **painel** navegação à esquerda, selecione `styles.css` .  O arquivo CSS aparece no **painel Editor.**

1.  Selecione **Ctrl+F no** Windows/Linux ou **Command+F** no macOS e insira `@media` .  A seguinte consulta de mídia CSS é exibida, o que confirma que ela é usada na página da Web.

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    Em seguida, emular a configuração do sistema operacional para reduzir a animação, da seguinte forma.

1.  Selecione **Esc** para abrir a Gaveta na parte inferior do DevTools.  Selecione o **botão Mais ferramentas** ( ) na parte superior da Gaveta para ver a lista de ferramentas e selecione **+** **Renderização**.  

1.  No recurso **de mídia CSS emular prefere a** lista suspenso de movimento reduzido, selecione **prefers-reduced-motion: reduced**.

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulando o movimento reduzido e o CSS que garante que a rolagem suave só acontece quando o usuário o deseja" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        Simulando o movimento reduzido e o CSS que garante que a rolagem suave só acontece quando o usuário o deseja
    :::image-end:::

1.  Na página da Web, selecione os itens de menu azul, como **Cavalos** ou **Alpacas**.  Agora, a página da Web rola instantaneamente para a seção selecionada, em vez de usar a animação de rolagem suave.

1.  Na ferramenta **Rendering,** abaixo Emular o recurso de mídia **CSS prefere movimento reduzido,** selecione **Sem emulação** para remover essa configuração.
   
Observe que a página da Web de demonstração ainda executa as seguintes animações, mesmo com as configurações de consulta e emulação de mídia acima. Ao criar seu produto Web, certifique-se de corrigir todas as animações semelhantes.  
*  Animação dos itens de menu azul quando você passar o mouse sobre eles.
*  Animação dos círculos nos links **Mais** quando você passar o mouse sobre eles.



## <a name="see-also"></a>Consulte também

*  [Simulação de movimento reduzido](reduced-motion-simulation.md)
*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
