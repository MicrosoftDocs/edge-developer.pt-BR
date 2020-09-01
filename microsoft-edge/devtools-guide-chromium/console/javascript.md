---
title: Começar a executar o JavaScript no console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 7e91d9844b2926bc8302331c6b9d971922d27ea3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982246"
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



Este tutorial interativo mostra como executar JavaScript no **console**devtools do Microsoft Edge.  Para obter mais informações sobre como registrar mensagens no **console**, consulte [introdução ao registro de mensagens][DevToolsConsoleLoggingMessages].  Para obter mais informações sobre como pausar o código JavaScript e passar por ele uma linha por vez, consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   O **console**  
:::image-end:::  

## Visão geral   

O **console** é [repl][WikiReadEvalPrintLoop], que significa ler, avaliar, imprimir e fazer loop.  Ele lê o JavaScript que você digita, avalia seu código, imprime o resultado da sua [expressão][2alityExpressionsVersusStatements]e, em seguida, volta para a primeira etapa.  

## Configurar o DevTools   

Este tutorial foi projetado para você abrir a demonstração e experimentar todos os fluxos de trabalho.  Ao acompanhar fisicamente, é mais provável que você se lembre dos fluxos de trabalho mais tarde.

1.  Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o **console**.  
1.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e clique em **exemplo de JavaScript do console** para abrir em uma nova janela.  
    
    *   [Exemplo de JavaScript do console][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="A página de exemplo de JavaScript do console à esquerda e DevTools à direita" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       A página de exemplo de JavaScript do console à esquerda e DevTools à direita  
    :::image-end:::  
    
## Exibir e alterar o JavaScript ou o DOM da página   

Ao criar ou depurar uma página, geralmente é útil executar instruções no **console** para alterar a aparência ou a execução da página.  
    
1.  Observe o texto no botão.  
1.  Digite `document.getElementById('hello').textContent = 'Hello, Console!'` o **console** e, em seguida, pressione `Enter` para avaliar a expressão.  Observe como o texto dentro do botão muda.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Como o console se parece após avaliar a expressão" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Como o **console** se parece após avaliar a expressão  
    :::image-end:::  
    
    Abaixo do código que você avaliou para ver `"Hello, Console!"` .  Lembre-se das 4 etapas de REPL: ler, avaliar, imprimir, repetir.  Depois de avaliar seu código, um REPL imprime o resultado da expressão.  Portanto, `"Hello, Console!"` deve ser o resultado da avaliação `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Executar JavaScript arbitrário que não está relacionado à página   

Às vezes, você só quer um código playground onde você pode testar algum código ou experimentar novos recursos JavaScript com os quais não está familiarizado.  O console é um lugar perfeito para estes tipos de experimentos.  

1.  Digite `5 + 15` o console e pressione `Enter` para avaliar a expressão. O console imprime o resultado da expressão abaixo do código.  Na figura a seguir, o seu **console** deve exibir o resultado após avaliar a expressão.  

1.  Digite o código a seguir no **console**.  Tente digitá-lo, caractere por caractere, em vez de copiar-colar.  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    Se você não estiver familiarizado com a `b=20` sintaxe, consulte [definir valores padrão para argumentos de função][Esma6DefaultParameterValues].  
    
1.  Agora, execute a função que você acabou de definir.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O console é exibido após avaliar as expressões no trecho de código" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             O **console** é exibido após avaliar as expressões no trecho de código  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` é avaliado `45` porque quando a `add` função é chamada sem um segundo argumento, o `b` padrão é `20` .  

## Próximas etapas   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools permite pausar um script no meio da execução.  Durante a pausa, você pode usar o **console** para exibir e alterar a `window` ou `DOM` da página nesse momento.  O fluxo de trabalho torna um fluxo de trabalho avançado de depuração.  Para obter um tutorial interativo, consulte [introdução à depuração de JavaScript][DevToolsJavascriptIndex].  

O **console** também tem um conjunto de funções de conveniência que facilita a interação com uma página.  Por exemplo:  

*   Em vez de digitar `document.querySelector()` para selecionar um elemento, digite `$()` .  Essa sintaxe é inspirada pelo jQuery, mas não é realmente jQuery.  É apenas um alias para `document.querySelector()` .  
*   `debug(function)` define efetivamente um ponto de interrupção na primeira linha dessa função.  
*   `keys(object)` Retorna uma matriz que contém as chaves do objeto especificado.  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Introdução ao registro de mensagens no console | Documentos da Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Referência do console | Documentos da Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência de API de utilitários de console | Documentos da Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  

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
