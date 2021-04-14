---
description: Se você estiver digitando as mesmas expressões JavaScript no Console repetidamente, experimente Expressões Ao Vivo.
title: Assista aos valores de expressão javascript em tempo real com expressões ao vivo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483111"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a>Monitorar alterações em JavaScript usando expressões ao vivo  

**Expressões ao vivo** são uma excelente maneira de monitorar expressões JavaScript que mudam muito.    Em vez de ter muitas mensagens de Console para ler e navegar, você pode fixar suas expressões JavaScript específicas na parte superior do **Console**.  

## <a name="add-a-new-live-expression"></a>Adicionar uma nova expressão ao vivo  

Para começar, escolha o **botão Criar expressão ao vivo** \(eye\) ao lado da caixa de texto **Filtrar.**  Depois de escolher, uma caixa de texto é exibida para que você insira sua nova expressão nele.  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Escolha o botão Nova expressão ao vivo para abrir uma caixa de texto para digitar uma expressão" lightbox="../media/console-live-expressions-new.msft.png":::
    Escolha o `New live expression` botão para abrir uma caixa de texto para digitar uma expressão  
:::image-end:::  

**Expressões ao vivo** podem ser qualquer expressão JavaScript válida.  Para experimentar, conclua as seguintes ações.  

1.  Abra a **caixa de texto Expressão Ao** Vivo.  
1.  Digite `document.activeElement`.  
1.  Para salvar a expressão, conclua uma das seguintes ações.  
    *   Selecione `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` ou \(macOS\).  
    *   Escolha fora da **caixa de texto Expressão Ao** Vivo.  
        
A expressão agora está ao vivo e `body` é exibida como resultado.  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="Expressão ao vivo para document.activeElement exibe o corpo como o resultado" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    Expressão ao vivo `document.activeElement` para exibe o corpo como resultado  
:::image-end:::  

Se você navegar pela página da Web, o valor será alterando.  Por exemplo, na figura a seguir, você abre o menu de pesquisa na página da Web e a expressão agora é exibida `button.nav-bar-button.focus-visible` como o valor.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Para alterar o valor da Expressão Ao Vivo, interaja com diferentes elementos na página da Web" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    Para alterar o valor da **Expressão Ao Vivo**, interaja com diferentes elementos na página da Web  
:::image-end:::  

Para alterar o valor novamente, abra e escolha a caixa de texto Pesquisar na página da Web.  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Navegue até um elemento diferente na página da Web para atualizar a Expressão Ao Vivo" lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    Navegue até um elemento diferente na página da Web para atualizar a **Expressão Ao Vivo**  
:::image-end:::  

## <a name="remove-live-expressions"></a>Remover expressões ao vivo  

Uma **expressão ao vivo** está disponível desde que você a mantenha ativa.  Para se livrar de uma **expressão ao vivo,** escolha `x` o próximo a ela.  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Para remover expressões ao vivo, escolha o x ao lado dele" lightbox="../media/console-live-expressions-remove.msft.png":::
    Para remover **Expressões Ao Vivo,** escolha `x` o próximo a ele  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a>Substituir o registro em log de console por expressões ao vivo  

Você pode criar quantas expressões quiser e persistir em todas as sessões do navegador e janelas.  **Expressões ao vivo** são uma maneira de reduzir o ruído no fluxo de trabalho de depuração.  

Por exemplo, você deseja monitorar o movimento do mouse na página da Web atual.  Navegue [até Logging Mouse Movement demo][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml], abra o **Console**e mova o mouse para exibir os logs com muitas informações.  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="Console exibe muitas informações sobre a posição do mouse" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    **Console** exibe muitas informações sobre a posição do mouse  
:::image-end:::  

A grande quantidade de informações não só retarda o processo de depuração, como também facilita a falta das alterações que você deseja revisar.  À medida **que o Console** exibe mais mensagens e você move o mouse, os valores que você deseja revisar rolam para fora da tela.  

Para experimentar **Expressões Ao Vivo** como uma alternativa, conclua as seguintes ações.  

1.  Navegue até o [movimento do mouse sem registrar a demonstração][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].  
1.  Criar **Expressões Ao Vivo** para e `x` `y` .  
    
Ao usar **expressões**ao vivo, você sempre obterá as informações na mesma parte da tela e manterá logs de **Console** para valores que não mudam tanto.

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Exibir a posição x e y do mouse como Expressões Ao Vivo" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    Exibir a `x` posição e do mouse como `y` **Expressões Ao Vivo**  
:::image-end:::  

**Expressões ao vivo** são executados exclusivamente no computador e você não precisa alterar nada em seu código para exibição.  **Expressões ao vivo** são uma ótima maneira de garantir que você apenas exibe as informações que deseja depurar.  Além disso, **expressões ao** vivo ajudam a limitar o ruído nos computadores dos usuários.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Exemplos de mensagens de console: usando a tabela | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Movimento do mouse sem registro em log | GitHub"  
