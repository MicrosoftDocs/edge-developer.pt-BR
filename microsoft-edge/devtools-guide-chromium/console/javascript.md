---
description: Saiba como executar JavaScript no Console.
title: Começar a executar JavaScript no Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398816"
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

# <a name="get-started-with-running-javascript-in-the-console"></a>Começar a executar JavaScript no Console  

Este tutorial interativo mostra como executar o JavaScript no **** Console do Microsoft Edge DevTools.  Para obter mais informações sobre como registrar mensagens no **Console,** navegue até [Começar a registrar mensagens][DevToolsConsoleLoggingMessages].  Para obter mais informações sobre como pausar o código JavaScript e percorrer uma linha por vez, navegue até Começar a [depurar JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O Console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   O **Console**  
:::image-end:::  

## <a name="overview"></a>Visão geral  

O **Console** é um [REPL][WikiReadEvalPrintLoop], que significa Leitura, Avaliação, Impressão e Loop.  Ele lê o JavaScript que você digita nele, avalia seu código, imprime o resultado de sua expressão [e,][2alityExpressionsVersusStatements]em seguida, faz um loop de volta para a primeira etapa.  

## <a name="set-up-devtools"></a>Configurar o DevTools  

Este tutorial foi projetado para você abrir a demonstração e experimentar todos os fluxos de trabalho por conta própria.  Quando você acompanha fisicamente, é mais provável que você se lembre mais tarde dos fluxos de trabalho.

1.  Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\) para abrir o **Console**.  
1.  Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e escolha **Console Javascript Example** para abrir em uma nova janela.  
    
    *   [Exemplo de Javascript do Console][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="A página Exemplo javascript do console à esquerda e o DevTools à direita" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       A página Exemplo javascript do console à esquerda e o DevTools à direita  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a>Exibir e alterar o JavaScript ou DOM da página  

Ao criar ou depurar uma página, geralmente é útil executar instruções no **Console** para alterar a aparência ou a aparência da página.  
    
1.  Observe o texto no botão.  
1.  Digite `document.getElementById('hello').textContent = 'Hello, Console!'` o Console **e** selecione para avaliar `Enter` a expressão.  Observe como o texto dentro do botão muda.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Como o Console fica depois de avaliar a expressão" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Como o **Console fica** depois de avaliar a expressão  
    :::image-end:::  
    
    `"Hello, Console!"`, é exibido abaixo do código avaliado.  Lembre-se das 4 etapas do REPL: leitura, avaliação, impressão, loop.  Depois de avaliar seu código, uma REPL imprime o resultado da expressão.  Portanto, `"Hello, Console!"` deve ser o resultado da avaliação `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a>Executar JavaScript arbitrário que não está relacionado à página  

Às vezes, você só quer um playground de código onde você pode testar algum código ou experimentar novos recursos JavaScript com os quais não está familiarizado.  O **Console** é um lugar perfeito para esses tipos de experimentos.  

1.  Digite `5 + 15` o Console e selecione para avaliar a `Enter` expressão. O Console imprime o resultado da expressão abaixo do código.  Na figura a seguir, seu **Console** deve exibir o resultado após avaliar a expressão.  

1.  Digite o código a seguir no **Console**.  Tente digitá-lo, de caractere por caractere, em vez de copiá-lo.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Se você não estiver familiarizado com a `b=20` sintaxe, navegue para [definir valores padrão para argumentos de função][Esma6DefaultParameterValues].  
    
1.  Agora, execute a função que você acabou de definir.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="O Console é exibido após avaliar as expressões no trecho de código" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             O **Console** é exibido após avaliar as expressões no trecho de código  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` avalia porque `45` quando a função é chamada sem um segundo `add` argumento, o padrão é `b` `20` .  

## <a name="next-steps"></a>Próximas etapas  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

O DevTools permite pausar um script no meio da execução.  Enquanto você está pausado, você pode usar o **Console** para exibir e alterar o ou da `window` página nesse momento no `DOM` tempo.  O fluxo de trabalho faz com que um fluxo de trabalho de depuração poderoso.  Para obter um tutorial interativo, navegue até [Introdução à Depuração de JavaScript][DevToolsJavascriptIndex].  

O **Console** também tem um conjunto de funções de conveniência que facilitam a interação com uma página.  Por exemplo:  

*   Em vez de digitar `document.querySelector()` para selecionar um elemento, digite `$()` .  Essa sintaxe é inspirada por jQuery, mas não é realmente jQuery.  É apenas um alias para `document.querySelector()` .  
*   `debug(function)` define efetivamente um ponto de interrupção na primeira linha dessa função.  
*   `keys(object)` retorna uma matriz que contém as chaves do objeto especificado.  

Para obter mais informações sobre as funções de conveniência, navegue até [Console Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Começar a registrar mensagens no console | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Console reference | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressões versus instruções em JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parâmetro padrão - Tratamento de parâmetros estendidos - ECMAScript 6 — Novos recursos: visão geral & comparação"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemplo javascript de console | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Loop de leitura-eval-print - Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/javascript) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
