---
description: Como registrar mensagens e executar JavaScript no Console do Microsoft Edge DevTools.
title: Registrar mensagens na ferramenta Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d48a48de7b261a628ac99f58680deb119268a980
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483294"
---
# <a name="log-messages-in-the-console-tool"></a>Registrar mensagens na ferramenta Console  

Desde que os navegadores começaram a oferecer ferramentas de desenvolvedor, **o Console** é um favorito.  O motivo é simples.  

*   Na maioria dos cursos de programação, você aprende a gerar algum tipo de comando de impressão para obter informações sobre o que acontece.  

Antes do DevTools, você estava limitado a uma `alert()` ou `document.write()` instrução para depurar no navegador.  

Se você quiser registrar informações no **Console,** muitos métodos estarão disponíveis para você.  Revise todos os métodos disponíveis na referência [da API][DevtoolsConsoleApi].  O trecho de código a seguir lista os métodos mais importantes.  

```javascript
// prints the text to the console as  a log message
console.log('This is a log message')
// prints the text to the console as an informational message
console.info('This is some information') 
// prints the text to the console as an error message
console.error('This is an error')
// prints the text to the console as a warning
console.warn('This is a warning') 
```  

Copie e colar o trecho de código anterior no Console ou navegue até **Console** mensagens [exemplos: log, informações,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]erro e aviso .  Quando você tenta qualquer método no **Console**, os métodos e parecem fazer a mesma coisa, enquanto os métodos e exibem um ícone ao lado da mensagem e uma maneira de inspecionar o rastreamento de pilha da `log()` `info()` `error()` `warn()` mensagem. [][WikiStackTrace]  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="O Console exibe as mensagens de APIs de log diferentes" lightbox="../media/console-log-examples.msft.png":::
   O **Console** exibe as mensagens de APIs de log diferentes  
:::image-end:::  

No entanto, ainda é uma boa ideia usar e para tarefas de log diferentes, pois isso permite filtrar usando o tipo `info()` `log()` no [Console][DevtoolsConsoleConsoleFilters].  

## <a name="different-types-of-logs"></a>Tipos diferentes de logs  

Em vez de texto de log, você pode enviar quaisquer referências javaScript ou DOM válidas para o **Console**.  O **Console** é elegante e determina o tipo que você o envia.  Em seguida, ele oferece a melhor representação possível.  Copie e colar o seguinte trecho de código no **Console** ou para exibir os resultados, navegue até [Console messages examples: logging different types][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].  

```javascript
let x = 2;
// logs the value of x
console.log(x);
// logs the name x and value of x
console.log({x})   
// logs a DOM reference  
console.log(document.querySelector('body'));
// logs an Object
console.log({"type":"life", "meaning": 42});
let w3techs = ['HTML', 'CSS', 'SVG', 'MathML'];
// logs an Array
console.log(w3techs);
```  

Cada resultado é exibido de uma maneira diferente.  Use os triângulos para alternar as informações e analisar cada um deles com mais detalhes.  Os caracteres de chaves ao redor da variável são um pequeno truque para evitar muitas mensagens de log nas quais você só tem um valor, mas não sabe de onde `{}` `x` ele se originou.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Variáveis de log de diferentes tipos no console" lightbox="../media/console-log-types.msft.png":::
         Variáveis de log de diferentes tipos no **Console**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Variáveis de log de diferentes tipos no console com informações extras expandidas" lightbox="../media/console-log-types-expanded.msft.png":::
         Variáveis de log de diferentes tipos no **Console com** informações extras expandidas  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a>Formatar e converter valores com especificadores

Um recurso especial de todos os métodos de log é que você pode usar especificadores em sua mensagem de log.  Os especificadores fazem parte de uma mensagem de log e começam com um caractere de sinal de porcentagem \( \) e permitem que você registre determinados valores em formatos diferentes e `%` até converta cada um deles.  

*   `%s` logs como Cadeias de Caracteres
*   `%i` ou `%d` logs como Inteiros
*   `%f` logs como um valor de ponto flutuante
*   `%o` logs como um elemento DOM expansível
*   `%O` logs como um objeto JavaScript expansível
*   `%c` permite que você estilmente sua mensagem com CSS

```javascript
// logs "10x console developer"
console.log('%ix %s developer', 10, 'console');
// logs PI => 3.141592653589793
console.log(Math.PI); 
// logs PI as an integer = 3
console.log('%i', Math.PI); 
// logs the webpage body as a DOM node
console.log('%o', document.body); 
// logs the body of the webpage as a JavaScript object with all properties
console.log('%O', document.body); 
// Displays the message as red and big
console.log('%cImportant message follows','color:red;font-size:40px');
```  

O primeiro exemplo exibe que a ordem de substituição de especificadores é a ordem de parâmetros após a cadeia de caracteres.  Para exibir os resultados, copie e colar o trecho de código anterior no **Console** ou navegue até Console messages [examples: Logging with specifiers][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].  Expanda as informações no log para exibir a enorme diferença entre `%o` e `%O` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Usar especificadores para registrar e converter valores" lightbox="../media/console-log-specifiers.msft.png":::
         Usar especificadores para registrar e converter valores  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Expandir os resultados exibe a diferença entre %O e %o especificador - o corpo é exibido como um nó DOM expansível ou como uma lista completa de todas as propriedades JavaScript no corpo da página da Web" lightbox="../media/console-log-specifiers-expanded.msft.png":::
        Expanda os resultados exibe a diferença entre o e o especificador - o corpo é exibido como um nó DOM expansível ou como uma lista completa de todas as propriedades JavaScript no corpo da página da `%O` `%o` Web  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a>Mensagens de log de grupo

Se você registrar muitas informações, poderá usar os métodos e para exibir mensagens de log como grupos expansíveis e retutíveis `group` `groupCollapsed` no **Console**.  Os grupos podem ser aninhados e nomeados para facilitar a compreensão dos dados.  

```javascript
console.group("Passengers: Heart of Gold");
console.log('Zaphod');
console.log('Trillian');
console.log('Ford');
console.log('Arthur');
console.log('Marvin');
console.groupCollapsed("Hidden");
console.log('(Frankie & Benjy)');
console.groupEnd("Hidden");
console.groupEnd("Passengers: Heart of Gold");

let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
for (tech in technologies) {
  console.groupCollapsed(tech);
  technologies[tech].forEach(t => console.log(t));
  console.groupEnd(tech);
}
```  

Também no segundo exemplo, os nomes de grupo podem ser gerados opcionalmente.  Para exibir os resultados, copie e colar o trecho de código anterior no **Console** ou navegue até Console de exemplos de [mensagens: agrupando logs][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].  Você pode expandir e fechar cada uma das seções.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Registrar muitos valores como grupos" lightbox="../media/console-log-groups.msft.png":::
         Registrar muitos valores como grupos  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Cada grupo pode ser expandido e recolhido" lightbox="../media/console-log-groups-expanded.msft.png":::
        Cada grupo pode ser expandido e recolhido  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a>Exibir dados complexos como tabelas  

O método registra dados complexos não como um objeto retlegível e expansível, mas como uma tabela que você pode `console.table()` classificar usando diferentes headers.  Uma tabela ordenada torna muito mais fácil para as pessoas revisarem as informações.  Para exibi-lo em um exemplo, navegue até [Console messages examples: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].

```javascript
let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
// log technologies as an object
console.log(technologies);
// display technologies as a table
console.table(technologies);

// get the dimensions of the webpage body
let bodyDimensions = document.body.getBoundingClientRect();
// display dimensions as an object
console.log(bodyDimensions);
// display dimensions as a table
console.table(bodyDimensions);
```  

:::image type="complex" source="../media/console-log-table.msft.png" alt-text="Exibir dados com console.table para facilitar a leitura" lightbox="../media/console-log-table.msft.png":::
   Exibir dados com `console.table` para facilitar a leitura
:::image-end:::  

A saída de `console.table` tem um formato de tabela não somente quando é exibido no **Console**.    Por exemplo, se você copiar e colar uma tabela no Excel, no Word ou em qualquer outro produto que suporte dados tabular, a estrutura permanecerá intacta.  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

Se os dados têm parâmetros nomeados, o método também permite que você especifique uma das colunas para cada propriedade a ser exibida `console.table()` `Array` como um segundo parâmetro.  O exemplo a seguir exibe como especificar uma matriz de colunas mais acessível.  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filtrar informações que console.table exibe e fornece uma matriz de propriedades a ser exibida como um segundo parâmetro" lightbox="../media/console-log-table-filtered.msft.png":::
   Filtrar informações `console.table` que exibem e fornecem uma matriz de propriedades a ser exibida como um segundo parâmetro  
:::image-end:::  

Você pode estar tentado a usar os métodos de log como seus principais meios para depurar páginas da Web, pois os métodos de log são simples de usar.  Considere o resultado de qualquer `console.log()` solicitação.  Os produtos live não devem usar nenhum log usado para depurar.  Ele pode revelar informações internas para as pessoas.  E o ruído criado no **Console** é avassalador.  Quando você usa [a Depuração][DevtoolsJavascriptBreakpoints] de Pontos de Interrupção ou Expressões Ao [Vivo,][DevtoolsConsoleLiveExpressions]você pode descobrir que seus fluxos de trabalho são mais eficazes e obter resultados melhores.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrar mensagens de console | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Monitorar alterações no JavaScript usando expressões ao vivo | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-examples.html "Exemplos de mensagens de console: log, informações, erro e aviso | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-types.html "Exemplos de mensagens de console: registrar tipos diferentes | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-groups.html "Exemplos de mensagens de console: agrupar logs | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-specifiers.html "Exemplos de mensagens de console: registro em log com especificadores | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-table.html "Exemplos de mensagens de console: usando a tabela | GitHub"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Rastreamento de pilha | Wikipédia"  
