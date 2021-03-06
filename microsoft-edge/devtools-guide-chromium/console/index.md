---
description: Os principais usos do Console do Microsoft Edge DevTools são registrar mensagens e executar JavaScript.
title: Visão geral do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399117"
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

# <a name="console-overview"></a>Visão geral do console  

  

Esta página explica como o Console do Microsoft Edge DevTools facilita o desenvolvimento de páginas da Web.  O **Console** tem 2 usos principais: [exibição de mensagens registradas e](#viewing-logged-messages) execução de [JavaScript](#running-javascript).  

## <a name="viewing-logged-messages"></a>Exibindo mensagens registradas  

Os desenvolvedores da Web geralmente registram mensagens no Console para garantir que o JavaScript deles está funcionando conforme o esperado.  Para registrar uma mensagem, insira uma expressão como `console.log('Hello, Console!')` em seu JavaScript.  Quando o navegador executa o JavaScript e processa uma expressão como essa, o navegador registra a mensagem no **Console**.  

:::row:::
   :::column span="":::
      O HTML e JavaScript para a página.  
      
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
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
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
   :::column-end:::
   :::column span="":::
      Na figura a seguir, o **Console** exibe os resultados de carregar a página e aguardar 3 segundos.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="O painel Console" lightbox="../media/console-console-demo.msft.png":::
         A **ferramenta Console**  
      :::image-end:::  
      
      Tente determinar quais linhas de código fizeram com que o navegador registrava as mensagens.  
   :::column-end:::
:::row-end:::  

Os desenvolvedores da Web registram mensagens pelos dois motivos gerais a seguir.  

*   Certifique-se de que o código está sendo executado na ordem certa.  
*   Inspecionando os valores das variáveis em um determinado momento no tempo.  

Para obter a experiência prática com o registro em log, navegue até [Começar a registrar mensagens][DevtoolsConsoleLoggingMessages].  Para procurar a lista completa `console` de métodos, navegue até a [Referência da API do Console.][DevToolsConsoleAPI]  A principal diferença entre os métodos é como os dados que estão sendo registrados são exibidos.  

## <a name="running-javascript"></a>Executando JavaScript  

O **Console** também é [um REPL][WikiREPLoop].  Você pode executar JavaScript no **Console para** interagir com a página que está sendo inspecionada.   

:::row:::
   :::column span="":::
      Na figura a seguir, **o Console** é mostrado ao lado da homepage DevTools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="A ferramenta Console ao lado da página inicial do DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         A **ferramenta Console** ao lado da página inicial do DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Na figura a seguir, a mesma página é mostrada depois de usar o **Console** para alterar o título superior da página.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Use o Console para alterar o título superior da página" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Use o **Console** para alterar o título superior da página  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Modificar a página do **Console** é possível porque o **Console** tem acesso total à [janela][MDNWindow] da página.  O DevTools tem algumas funções de conveniência que facilitam a inspeção de uma página.  Por exemplo, suponha que seu JavaScript contenha uma função chamada `hideModal` .  A `debug(hideModal)` execução pausa seu código na primeira linha da próxima vez que você o `hideModal` executa.  Para obter mais informações sobre a lista completa de funções de utilitário, navegue até Referência da [API de Utilitários de Console.][DevtoolsConsoleUtilitiesDebug]  

Ao executar o JavaScript, você não precisa interagir com a página.  Você pode usar o **Console** para experimentar um novo código não relacionado à página.  Por exemplo, suponha que você acabou de aprender sobre o método JavaScript Array [map()][MDNMap] integrado e deseja experimentar com ele.  
O **Console** é um bom lugar para experimentar a função.  

Para obter mais experiência prática com a execução de JavaScript no **Console,** navegue até [Começar a executar JavaScript][DevtoolsConsoleRunningJavascript].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Começar a registrar mensagens no console | Microsoft Docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Começar a executar JavaScript no console | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "depuração - Referência da API de Utilitários de Console | Microsoft Docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Loop de leitura-eval-print - Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
