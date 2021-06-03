---
description: Uma introdução ao uso da ferramenta Console dentro do Microsoft Edge de Desenvolvedor como um ambiente JavaScript.
title: O Console como um ambiente JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, JavaScript, desenvolvimento da Web, ferramentas f12, devtools
ms.openlocfilehash: f75ac6d728c9a69542b2f58df85248759267f76d
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483288"
---
# <a name="the-console-as-a-javascript-environment"></a>O Console como um ambiente JavaScript  

A **ferramenta Console** dentro do navegador DevTools é um ambiente [REPL.][WikiReadEvalPrintLoop]  Isso significa que você pode gravar qualquer JavaScript no **Console** que seja executado imediatamente.

Para experimentar, conclua as seguintes ações.  

1.  Abra o **Console**.  
    *   Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  
1.  Digite `2 + 2`.  O **Console** já exibe o resultado `4` na próxima linha enquanto você o digita.  O `Eager evaluation` recurso ajuda você a escrever JavaScript válido.  Ele exibe o resultado enquanto você digita se ele está errado ou se existe um resultado válido.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="Console exibe o resultado de 2 + 2 ao vivo à medida que você digita" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   **Console** exibe o resultado de `2 + 2` vida ao digitá-lo  
:::image-end:::  

Se você selecionar , o Console executará o comando JavaScript, lhe dará o resultado e permitirá que `Enter` você escreva o próximo comando. ****  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Executar várias expressões JavaScript em sucessão" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Executar várias expressões JavaScript em sucessão  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a>Autocompleção para gravar expressões complexas

O último exemplo pode parecer assustador, mas o **Console** ajuda você a escrever JavaScript complexo usando um excelente recurso de autocompleção.  Esse recurso é uma ótima maneira de aprender sobre métodos que você não sabia antes.  

Para experimentar, conclua as seguintes ações.  

1.  Digite `doc`.  
1.  Escolha `document` no menu suspenso.  
1.  Selecione a `tab` chave para escolher.  
1.  Digite `.bo`.  
1.  Selecione `tab` para obter `document.body` .  
1.  Digite outro para obter uma lista grande de possíveis propriedades e métodos disponíveis no corpo `.` da página da Web atual.  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Console autocompletion of JavaScript expressions" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Console** autocompletion of JavaScript expressions  
:::image-end:::  

## <a name="console-history"></a>Histórico do console

Assim como em muitas outras experiências de linha de comando, você também tem um histórico de comandos.  Selecione `Arrow Up` para exibir os comandos inseridos antes.  A comcompleção automática também mantém um histórico dos comandos digitados anteriormente.  Você pode digitar as primeiras letras de comandos anteriores e suas opções anteriores exibidas em uma caixa de texto.  

Além disso, **o Console** também oferece alguns métodos [utilitários que][DevtoolsConsoleUtilities] facilitam sua vida.  Por exemplo, `$_` sempre contém o resultado da última expressão que você publicou no **Console**.

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="A expressão $_ no Console sempre contém o último resultado" lightbox="../media/console-javascript-console-history.msft.png":::
    A `$_` expressão no **Console** sempre contém o último resultado  
:::image-end:::  

## <a name="multiline-edits"></a>Edições de várias linhas

Por padrão, o **Console** fornece apenas uma linha para gravar sua expressão JavaScript.  O código é executado quando você seleciona `Enter` . A limitação de uma linha pode frustrar você.  Para trabalhar em torno da limitação de uma linha, selecione `Shift` + `Enter` em vez de `Enter` .  No exemplo a seguir, o valor exibido é o resultado de todas as linhas em ordem.  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Selecione Shift+Enter para gravar várias linhas de JavaScript e o valor resultante é executado em ordem" lightbox="../media/console-javascript-multiline.msft.png":::
   Selecione `Shift` + `Enter` para gravar várias linhas de JavaScript e o valor resultante é executado em ordem  
:::image-end:::  

Se você iniciar uma instrução multiline no **Console**, ela será automaticamente reconhecida e recuada.  Por exemplo, se você iniciar uma instrução block com uma chaveta.  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="Console já reconhece expressões multi-linha usando chaves e recuos cada uma para você" lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    **Console** já reconhece expressões multi-linha usando chaves e recuos cada uma para você  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a>Solicitações de rede usando o aguardado de nível superior()  

Além de seus próprios scripts, **o Console** oferece suporte a espera de nível superior para executar JavaScript assíncrono arbitrário nele. [][GithubTc39ProposalTopLevelAwait]  Por exemplo, use a `fetch` API sem envolver a `await` instrução com uma função assíncrona.  

Para obter os últimos 50 problemas arquivados no Microsoft Edge [ferramentas][GithubMicrosoftVscodeEdgeDevtools] de desenvolvedor para Visual Studio Code GitHub repo, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Copie e colar o trecho de código a seguir para obter um objeto que contém 10 entradas.  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="Console exibe o resultado de uma solicitação de busca assíncrona de nível superior" lightbox="../media/console-javascript-top-level-await.msft.png":::
    **Console** exibe o resultado de uma solicitação assíncrona de nível `fetch` superior  
:::image-end:::  

As 10 entradas são difíceis de reconhecer, pois muitas informações são exibidas.  Felizmente, você pode usar o método log para receber apenas as informações nas quais `console.table()` você está interessado.  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Exibir o último resultado em um formato acessível por humanos usando console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    Exibir o último resultado em um formato acessível usando `console.table`  
:::image-end:::  

Para reutilizar os dados retornados de uma expressão, você pode usar o método `copy()` utilitário do **Console**.  O trecho de código a seguir envia a solicitação e copia os dados da resposta à área de transferência.  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

Use o **Console** como uma ótima maneira de praticar a funcionalidade JavaScript e fazer alguns cálculos rápidos.  A potência real é o fato de que você tem acesso ao [objeto window.][MdnDocsWebApiWindow]  Você pode [interagir com o DOM no Console.][DevtoolsConsoleConsoleDomInteraction]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use o Console para interagir com o dom | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "Proposta do ECMAScript: Espera de nível superior - tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Loop de leitura-eval-print | Wikipédia"  
