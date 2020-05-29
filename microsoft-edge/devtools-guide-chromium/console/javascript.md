---
title: Começar a executar o JavaScript no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 724d0e3c7c8439551538383e68a5fc4465eade94
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601723"
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







# Começar a executar o JavaScript no console   



Este tutorial interativo mostra como executar JavaScript no console DevTools do Microsoft Edge.  Consulte [introdução às mensagens de registro][DevToolsConsoleLoggingMessages] em log para saber como registrar mensagens no console.  Consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex] para saber como pausar o código JavaScript e passar por ele uma linha por vez.  

> ##### Figura 1  
> O **console**  
> ![O console][ImageConsole]  

## Visão geral   

O **console** é [repl][WikiReadEvalPrintLoop], que significa ler, avaliar, imprimir e fazer loop.  Ele lê o JavaScript que você digita, avalia seu código, imprime o resultado da sua [expressão][2alityExpressionsVersusStatements]e, em seguida, volta para a primeira etapa.  

## Configurar o DevTools   

Este tutorial foi projetado para você abrir a demonstração e experimentar todos os fluxos de trabalho.  Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.

1.  Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o **console**.  
1.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplo de JavaScript do console** para abrir em uma nova janela.  
    
    [Exemplo de JavaScript do console][GlitchConsoleJavascriptExample]  
    
    > ##### Figura 2  
    > A página de exemplo de JavaScript do console à esquerda e DevTools à direita  
    > ![A página de exemplo de JavaScript do console à esquerda e DevTools à direita][ImageTutorialDevToolsJs]  

## Exibir e alterar o JavaScript ou o DOM da página   

Ao criar ou depurar uma página, geralmente é útil executar instruções no **console** para alterar a aparência ou a execução da página.  
    
1.  Observe o texto no botão.  
1.  Digite `document.getElementById('hello').textContent = 'Hello, Console!'` o **console** e, em seguida, pressione `Enter` para avaliar a expressão.  Observe como o texto dentro do botão muda.  
    
    > ##### Figura 3  
    > Como o console se parece após avaliar a expressão  
    > ![Como o console se parece após avaliar a expressão][ImageConsoleAfterEvaluating]  
    
    Abaixo do código que você avaliou para ver `"Hello, Console!"` .  Lembre-se das 4 etapas de REPL: ler, avaliar, imprimir, repetir.  Depois de avaliar seu código, um REPL imprime o resultado da expressão.  Portanto, `"Hello, Console!"` deve ser o resultado da avaliação `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Executar JavaScript arbitrário que não está relacionado à página   

Às vezes, você só quer um código playground onde você pode testar algum código ou experimentar novos recursos JavaScript com os quais não está familiarizado.  O console é um lugar perfeito para estes tipos de experimentos.  

1.  Digite `5 + 15` o console e pressione `Enter` para avaliar a expressão. O console imprime o resultado da expressão abaixo do código.  A **Figura 4** abaixo mostra como deve ser a aparência do seu console depois da avaliação dessa expressão.  

1.  Digite o código a seguir no **console**.  Tente digitá-lo, caractere por caractere, em vez de copiar-colar.  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    Consulte [definir valores padrão para argumentos de função][Esma6DefaultParameterValues] se você não estiver familiarizado com a `b=20` sintaxe.  
    
1.  Agora, chame a função que você acabou de definir.  
    
    ```javascript
    add(25);
    ```  
    
    > ##### Figura 4  
    > Como o console se parece após avaliar as expressões acima  
    > ![Como o console se parece após avaliar as expressões acima][ImagePlayground]  
    
    `add(25)` é avaliado `45` porque quando a `add` função é chamada sem um segundo argumento, o `b` padrão é `20` .  

## Próximas etapas   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools permite pausar um script no meio da execução.  Durante a pausa, você pode usar o **console** para exibir e alterar a `window` ou `DOM` da página nesse momento.  Isso torna um fluxo de trabalho de depuração avançado.  Consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex] para um tutorial interativo.  

O **console** também tem um conjunto de funções de conveniência que facilita a interação com uma página.  Por exemplo:  

*   Em vez de digitar `document.querySelector()` para selecionar um elemento, digite `$()` .  Essa sintaxe é inspirada pelo jQuery, mas não é realmente jQuery.  É apenas um alias para `document.querySelector()` .  
*   `debug(function)` define efetivamente um ponto de interrupção na primeira linha dessa função.  
*   `keys(object)` Retorna uma matriz que contém as chaves do objeto especificado.  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Figura 1: o console"  
[ImageTutorialDevToolsJs]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-empty.msft.png "Figura 2: a página de exemplo de JavaScript do console à esquerda e DevTools à direita"  
[ImageConsoleAfterEvaluating]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-change-button-text.msft.png "Figura 3: aparência do console após a avaliação da expressão"  
[ImagePlayground]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Figura 4: a aparência do console após a avaliação das expressões acima"  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference#run-javascript "Referência do console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium//console/utilities "Referência de API de utilitários de console"  

[DevToolsJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressões versus instruções em JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parâmetro padrão-manipulação de parâmetro estendido-ECMAScript 6 – novos recursos: visão geral & comparação"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemplo de JavaScript do console | Problema"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Leitura – eval – loop de impressão-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/javascript) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
