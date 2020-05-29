---
title: Visão geral do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601779"
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





# Visão geral do console   

  

Esta página explica como o console do Microsoft Edge DevTools torna mais fácil o desenvolvimento de páginas da Web.  O console tem dois usos principais: [Exibir mensagens registradas](#viewing-logged-messages) e [executar JavaScript](#running-javascript).  

## Exibir mensagens registradas   

Os desenvolvedores da Web geralmente registram mensagens no console para verificar se o JavaScript está funcionando conforme o esperado.  Para registrar uma mensagem, insira uma expressão como `console.log('Hello, Console!')` em seu JavaScript.  Quando o navegador executa o JavaScript e vê uma expressão como essa, ele registra a mensagem no console.  Por exemplo, suponha que você esteja escrevendo o HTML e JavaScript para uma página:  

```html
<!doctype html>
<html>
  <head>
    <title>Console Demo</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <script>
      console.log('Loading!');
      const h1 = document.querySelector('h1');
      console.log(h1.textContent);
      console.assert(document.querySelector('h2'), 'h2 not found!');
      const artists = [
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
      ];
      console.table(artists);
      setTimeout(() => {
        h1.textContent = 'Hello, Console!';
        console.log(h1.textContent);
      }, 3000);
    </script>
  </body>
</html>
```  

A [Figura 1](#figure-1) mostra como é a aparência do console depois de carregar a página e esperar 3 segundos.  Tente descobrir quais linhas de código fizeram o navegador registrar as mensagens.  

> ##### Figura 1  
> Painel do console  
> ![Painel do console][ImageConsole]  

Os desenvolvedores da Web registram mensagens por dois motivos gerais:  

*   Verificar se o código está em execução na ordem correta.  
*   Inspecionar os valores de variáveis em um determinado momento no tempo.  

Consulte [introdução ao registro de mensagens][DevtoolsConsoleLoggingMessages] para obter experiência prática com o registro em log.  Consulte a [referência de API do console][DevToolsConsoleAPI] para procurar a lista completa de `console` métodos.  A principal diferença entre os métodos é como os dados que estão sendo registrados são exibidos.  

## Executando JavaScript   

O console também é um [repl][WikiREPLoop].  Você pode executar JavaScript no console para interagir com a página que está sendo inspecionada.  Por exemplo, a [Figura 2](#figure-2) mostra o console ao lado da home page do devtools, e a [Figura 3](#figure-3) mostra essa mesma página depois de usar o console para alterar o título superior da página.  

> ##### Figura 2  
> O painel do console ao lado da home page do DevTools  
> ![O painel do console ao lado da home page do DevTools][ImageConsoleOverview]  

> ##### Figura 3  
> Usar o console para alterar o título superior da página  
> ![Usar o console para alterar o título superior da página][ImageConsoleChangeTitle]  

A modificação da página no console é possível porque o console tem acesso completo à [janela][MDNWindow] da página.  O DevTools tem algumas funções de conveniência que facilitam a inspeção de uma página.  Por exemplo, suponha que o JavaScript contenha uma função chamada `hideModal` .  Executar `debug(hideModal)` pausa o código na primeira linha da `hideModal` próxima vez que você executá-lo.  Consulte [referência da API de utilitários de console][DevtoolsConsoleUtilitiesDebug] para ver a lista completa de funções de utilitário.  

Quando você executa JavaScript, você não precisa interagir com a página.  Você pode usar o console para experimentar um novo código não relacionado à página.  Por exemplo, suponha que você tenha aprendido apenas sobre o método interno de mapas de matrizes JavaScript [()][MDNMap] e queira experimentá-lo.  
O **console** é um bom lugar para experimentar a função.  

Consulte [introdução à execução de JavaScript][ImageConsoleChangeTitle] para obter experiência prática com a execução de JavaScript no console.  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Figura 1: painel do console"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Figura 3: usar o console para alterar o título superior da página"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Figura 2: painel do console ao lado da home page do DevTools"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Começar a executar o JavaScript no console"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Referência de API de utilitários de console de depuração"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. Map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Leitura – eval – loop de impressão-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
