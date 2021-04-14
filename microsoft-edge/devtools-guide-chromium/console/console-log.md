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
# <a name="log-messages-in-the-console-tool"></a><span data-ttu-id="76c52-104">Registrar mensagens na ferramenta Console</span><span class="sxs-lookup"><span data-stu-id="76c52-104">Log messages in the Console tool</span></span>  

<span data-ttu-id="76c52-105">Desde que os navegadores começaram a oferecer ferramentas de desenvolvedor, **o Console** é um favorito.</span><span class="sxs-lookup"><span data-stu-id="76c52-105">Ever since browsers started to offer developer tools, the **Console** is a favorite.</span></span>  <span data-ttu-id="76c52-106">O motivo é simples.</span><span class="sxs-lookup"><span data-stu-id="76c52-106">The reason is simple.</span></span>  

*   <span data-ttu-id="76c52-107">Na maioria dos cursos de programação, você aprende a gerar algum tipo de comando de impressão para obter informações sobre o que acontece.</span><span class="sxs-lookup"><span data-stu-id="76c52-107">In most programming courses, you learn to output some kind of print command to gain insights about what happens.</span></span>  

<span data-ttu-id="76c52-108">Antes do DevTools, você estava limitado a uma `alert()` ou `document.write()` instrução para depurar no navegador.</span><span class="sxs-lookup"><span data-stu-id="76c52-108">Before the DevTools, you were limited to an `alert()` or `document.write()` statement to debug in the browser.</span></span>  

<span data-ttu-id="76c52-109">Se você quiser registrar informações no **Console,** muitos métodos estarão disponíveis para você.</span><span class="sxs-lookup"><span data-stu-id="76c52-109">If you want to log information in the **Console**, lots of methods are available to you.</span></span>  <span data-ttu-id="76c52-110">Revise todos os métodos disponíveis na referência [da API][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="76c52-110">Review all of available methods in the [API reference][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="76c52-111">O trecho de código a seguir lista os métodos mais importantes.</span><span class="sxs-lookup"><span data-stu-id="76c52-111">The following code snippet lists the most important methods.</span></span>  

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

<span data-ttu-id="76c52-112">Copie e colar o trecho de código anterior no Console ou navegue até **Console** mensagens [exemplos: log, informações,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]erro e aviso .</span><span class="sxs-lookup"><span data-stu-id="76c52-112">Copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: log, info, error, and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml].</span></span>  <span data-ttu-id="76c52-113">Quando você tenta qualquer método no **Console**, os métodos e parecem fazer a mesma coisa, enquanto os métodos e exibem um ícone ao lado da mensagem e uma maneira de inspecionar o rastreamento de pilha da `log()` `info()` `error()` `warn()` mensagem. [][WikiStackTrace]</span><span class="sxs-lookup"><span data-stu-id="76c52-113">When you try any method in the **Console**, the `log()` and `info()` methods seem to do the same thing, while the `error()` and `warn()` methods display an icon next to the message and a way to inspect the [stack trace][WikiStackTrace] of the message.</span></span>  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="O Console exibe as mensagens de APIs de log diferentes" lightbox="../media/console-log-examples.msft.png":::
   <span data-ttu-id="76c52-115">O **Console** exibe as mensagens de APIs de log diferentes</span><span class="sxs-lookup"><span data-stu-id="76c52-115">The **Console** displays the messages from different log APIs</span></span>  
:::image-end:::  

<span data-ttu-id="76c52-116">No entanto, ainda é uma boa ideia usar e para tarefas de log diferentes, pois isso permite filtrar usando o tipo `info()` `log()` no [Console][DevtoolsConsoleConsoleFilters].</span><span class="sxs-lookup"><span data-stu-id="76c52-116">It is, however, still a good idea to use `info()` and `log()` for different log tasks as that allows you to [filter using type in the Console][DevtoolsConsoleConsoleFilters].</span></span>  

## <a name="different-types-of-logs"></a><span data-ttu-id="76c52-117">Tipos diferentes de logs</span><span class="sxs-lookup"><span data-stu-id="76c52-117">Different types of logs</span></span>  

<span data-ttu-id="76c52-118">Em vez de texto de log, você pode enviar quaisquer referências javaScript ou DOM válidas para o **Console**.</span><span class="sxs-lookup"><span data-stu-id="76c52-118">Instead of log text you may send any valid JavaScript or DOM references to the **Console**.</span></span>  <span data-ttu-id="76c52-119">O **Console** é elegante e determina o tipo que você o envia.</span><span class="sxs-lookup"><span data-stu-id="76c52-119">The **Console** is elegant and it determines the type that you send it.</span></span>  <span data-ttu-id="76c52-120">Em seguida, ele oferece a melhor representação possível.</span><span class="sxs-lookup"><span data-stu-id="76c52-120">It then gives you the best possible representation.</span></span>  <span data-ttu-id="76c52-121">Copie e colar o seguinte trecho de código no **Console** ou para exibir os resultados, navegue até [Console messages examples: logging different types][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span><span class="sxs-lookup"><span data-stu-id="76c52-121">Copy and paste the following code snippet in the **Console** or to display the results, navigate to [Console messages examples: logging different types][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span></span>  

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

<span data-ttu-id="76c52-122">Cada resultado é exibido de uma maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="76c52-122">Each result is displayed in a different way.</span></span>  <span data-ttu-id="76c52-123">Use os triângulos para alternar as informações e analisar cada um deles com mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="76c52-123">Use the triangles to toggle the information and analyze each one in more detail.</span></span>  <span data-ttu-id="76c52-124">Os caracteres de chaves ao redor da variável são um pequeno truque para evitar muitas mensagens de log nas quais você só tem um valor, mas não sabe de onde `{}` `x` ele se originou.</span><span class="sxs-lookup"><span data-stu-id="76c52-124">The curly brace characters `{}` around the `x` variable are a nice little trick to avoid lots of log messages where you only get a value but you don't know where it originated.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Variáveis de log de diferentes tipos no console" lightbox="../media/console-log-types.msft.png":::
         <span data-ttu-id="76c52-126">Variáveis de log de diferentes tipos no **Console**</span><span class="sxs-lookup"><span data-stu-id="76c52-126">Log variables of different types in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Variáveis de log de diferentes tipos no console com informações extras expandidas" lightbox="../media/console-log-types-expanded.msft.png":::
         <span data-ttu-id="76c52-128">Variáveis de log de diferentes tipos no **Console com** informações extras expandidas</span><span class="sxs-lookup"><span data-stu-id="76c52-128">Log variables of different types in the **Console** with expanded extra information</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a><span data-ttu-id="76c52-129">Formatar e converter valores com especificadores</span><span class="sxs-lookup"><span data-stu-id="76c52-129">Format and convert values with specifiers</span></span>

<span data-ttu-id="76c52-130">Um recurso especial de todos os métodos de log é que você pode usar especificadores em sua mensagem de log.</span><span class="sxs-lookup"><span data-stu-id="76c52-130">A special feature of all the log methods is that you may use specifiers in your log message.</span></span>  <span data-ttu-id="76c52-131">Os especificadores fazem parte de uma mensagem de log e começam com um caractere de sinal de porcentagem \( \) e permitem que você registre determinados valores em formatos diferentes e `%` até converta cada um deles.</span><span class="sxs-lookup"><span data-stu-id="76c52-131">Specifiers are part of a log message and start with a percentage sign \(`%`\) character and allow you to log certain values in different formats and even convert each.</span></span>  

*   `%s` <span data-ttu-id="76c52-132">logs como Cadeias de Caracteres</span><span class="sxs-lookup"><span data-stu-id="76c52-132">logs as Strings</span></span>
*   `%i` <span data-ttu-id="76c52-133">ou `%d` logs como Inteiros</span><span class="sxs-lookup"><span data-stu-id="76c52-133">or `%d` logs as Integers</span></span>
*   `%f` <span data-ttu-id="76c52-134">logs como um valor de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="76c52-134">logs as a floating-point value</span></span>
*   `%o` <span data-ttu-id="76c52-135">logs como um elemento DOM expansível</span><span class="sxs-lookup"><span data-stu-id="76c52-135">logs as an expandable DOM element</span></span>
*   `%O` <span data-ttu-id="76c52-136">logs como um objeto JavaScript expansível</span><span class="sxs-lookup"><span data-stu-id="76c52-136">logs as an expandable JavaScript object</span></span>
*   `%c` <span data-ttu-id="76c52-137">permite que você estilmente sua mensagem com CSS</span><span class="sxs-lookup"><span data-stu-id="76c52-137">allows you to style you message with CSS</span></span>

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

<span data-ttu-id="76c52-138">O primeiro exemplo exibe que a ordem de substituição de especificadores é a ordem de parâmetros após a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76c52-138">The first example displays that the order of replacement of specifiers is the parameter order following the string.</span></span>  <span data-ttu-id="76c52-139">Para exibir os resultados, copie e colar o trecho de código anterior no **Console** ou navegue até Console messages [examples: Logging with specifiers][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span><span class="sxs-lookup"><span data-stu-id="76c52-139">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: Logging with specifiers][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span></span>  <span data-ttu-id="76c52-140">Expanda as informações no log para exibir a enorme diferença entre `%o` e `%O` .</span><span class="sxs-lookup"><span data-stu-id="76c52-140">Expand the information in the log to display the huge difference between `%o` and `%O`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Usar especificadores para registrar e converter valores" lightbox="../media/console-log-specifiers.msft.png":::
         <span data-ttu-id="76c52-142">Usar especificadores para registrar e converter valores</span><span class="sxs-lookup"><span data-stu-id="76c52-142">Use specifiers to log and convert values</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Expandir os resultados exibe a diferença entre %O e %o especificador - o corpo é exibido como um nó DOM expansível ou como uma lista completa de todas as propriedades JavaScript no corpo da página da Web" lightbox="../media/console-log-specifiers-expanded.msft.png":::
        <span data-ttu-id="76c52-144">Expanda os resultados exibe a diferença entre o e o especificador - o corpo é exibido como um nó DOM expansível ou como uma lista completa de todas as propriedades JavaScript no corpo da página da `%O` `%o` Web</span><span class="sxs-lookup"><span data-stu-id="76c52-144">Expand the results displays the difference between the `%O` and `%o` specifier - the body is either displayed as an expandable DOM node or as a full list of all JavaScript properties on the webpage body</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a><span data-ttu-id="76c52-145">Mensagens de log de grupo</span><span class="sxs-lookup"><span data-stu-id="76c52-145">Group log messages</span></span>

<span data-ttu-id="76c52-146">Se você registrar muitas informações, poderá usar os métodos e para exibir mensagens de log como grupos expansíveis e retutíveis `group` `groupCollapsed` no **Console**.</span><span class="sxs-lookup"><span data-stu-id="76c52-146">If you log much information, you may use the `group` and `groupCollapsed` methods to display log messages as expandable and collapsible groups in the **Console**.</span></span>  <span data-ttu-id="76c52-147">Os grupos podem ser aninhados e nomeados para facilitar a compreensão dos dados.</span><span class="sxs-lookup"><span data-stu-id="76c52-147">Groups may be nested and named to make the data much easier to understand.</span></span>  

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

<span data-ttu-id="76c52-148">Também no segundo exemplo, os nomes de grupo podem ser gerados opcionalmente.</span><span class="sxs-lookup"><span data-stu-id="76c52-148">Also in the second example, the group names may be optionally generated.</span></span>  <span data-ttu-id="76c52-149">Para exibir os resultados, copie e colar o trecho de código anterior no **Console** ou navegue até Console de exemplos de [mensagens: agrupando logs][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span><span class="sxs-lookup"><span data-stu-id="76c52-149">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: grouping logs][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span></span>  <span data-ttu-id="76c52-150">Você pode expandir e fechar cada uma das seções.</span><span class="sxs-lookup"><span data-stu-id="76c52-150">You may expand and collapse each of the sections.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Registrar muitos valores como grupos" lightbox="../media/console-log-groups.msft.png":::
         <span data-ttu-id="76c52-152">Registrar muitos valores como grupos</span><span class="sxs-lookup"><span data-stu-id="76c52-152">Log lots of values as groups</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Cada grupo pode ser expandido e recolhido" lightbox="../media/console-log-groups-expanded.msft.png":::
        <span data-ttu-id="76c52-154">Cada grupo pode ser expandido e recolhido</span><span class="sxs-lookup"><span data-stu-id="76c52-154">Each group may be expanded and collapsed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a><span data-ttu-id="76c52-155">Exibir dados complexos como tabelas</span><span class="sxs-lookup"><span data-stu-id="76c52-155">Display complex data as tables</span></span>  

<span data-ttu-id="76c52-156">O método registra dados complexos não como um objeto retlegível e expansível, mas como uma tabela que você pode `console.table()` classificar usando diferentes headers.</span><span class="sxs-lookup"><span data-stu-id="76c52-156">The `console.table()` method logs complex data not as a collapsible and expandable object, but as a table that you may sort using different headers.</span></span>  <span data-ttu-id="76c52-157">Uma tabela ordenada torna muito mais fácil para as pessoas revisarem as informações.</span><span class="sxs-lookup"><span data-stu-id="76c52-157">A sorted table makes it much easier for people to review the information.</span></span>  <span data-ttu-id="76c52-158">Para exibi-lo em um exemplo, navegue até [Console messages examples: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span><span class="sxs-lookup"><span data-stu-id="76c52-158">To display it in an example, navigate to [Console messages examples: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span></span>

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
   <span data-ttu-id="76c52-160">Exibir dados com `console.table` para facilitar a leitura</span><span class="sxs-lookup"><span data-stu-id="76c52-160">Display data with `console.table` to make it much easier to read</span></span>
:::image-end:::  

<span data-ttu-id="76c52-161">A saída de `console.table` tem um formato de tabela não somente quando é exibido no **Console**.</span><span class="sxs-lookup"><span data-stu-id="76c52-161">The output of `console.table` has a table format not only when it displays in the **Console**.</span></span>    <span data-ttu-id="76c52-162">Por exemplo, se você copiar e colar uma tabela no Excel, no Word ou em qualquer outro produto que suporte dados tabular, a estrutura permanecerá intacta.</span><span class="sxs-lookup"><span data-stu-id="76c52-162">For example, if you copy and paste a table into Excel, Word, or any other product that supports tabular data, the structure remains intact.</span></span>  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

<span data-ttu-id="76c52-163">Se os dados têm parâmetros nomeados, o método também permite que você especifique uma das colunas para cada propriedade a ser exibida `console.table()` `Array` como um segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="76c52-163">If the data has named parameters, the `console.table()` method also allows you to specify an `Array` of columns for each property to display as a second parameter.</span></span>  <span data-ttu-id="76c52-164">O exemplo a seguir exibe como especificar uma matriz de colunas mais acessível.</span><span class="sxs-lookup"><span data-stu-id="76c52-164">The following example displays how to specify an array of columns that is more readable.</span></span>  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filtrar informações que console.table exibe e fornece uma matriz de propriedades a ser exibida como um segundo parâmetro" lightbox="../media/console-log-table-filtered.msft.png":::
   <span data-ttu-id="76c52-166">Filtrar informações `console.table` que exibem e fornecem uma matriz de propriedades a ser exibida como um segundo parâmetro</span><span class="sxs-lookup"><span data-stu-id="76c52-166">Filter information that `console.table` displays and provide an array of properties to display as a second parameter</span></span>  
:::image-end:::  

<span data-ttu-id="76c52-167">Você pode estar tentado a usar os métodos de log como seus principais meios para depurar páginas da Web, pois os métodos de log são simples de usar.</span><span class="sxs-lookup"><span data-stu-id="76c52-167">You may be tempted to use the log methods as your main means to debug webpages, because log methods are simple to use.</span></span>  <span data-ttu-id="76c52-168">Considere o resultado de qualquer `console.log()` solicitação.</span><span class="sxs-lookup"><span data-stu-id="76c52-168">Consider the result of any `console.log()` request.</span></span>  <span data-ttu-id="76c52-169">Os produtos live não devem usar nenhum log usado para depurar.</span><span class="sxs-lookup"><span data-stu-id="76c52-169">Live products shouldn't use any log that was used to debug.</span></span>  <span data-ttu-id="76c52-170">Ele pode revelar informações internas para as pessoas.</span><span class="sxs-lookup"><span data-stu-id="76c52-170">It may reveal inside information to people.</span></span>  <span data-ttu-id="76c52-171">E o ruído criado no **Console** é avassalador.</span><span class="sxs-lookup"><span data-stu-id="76c52-171">And the noise created in the **Console** is overwhelming.</span></span>  <span data-ttu-id="76c52-172">Quando você usa [a Depuração][DevtoolsJavascriptBreakpoints] de Pontos de Interrupção ou Expressões Ao [Vivo,][DevtoolsConsoleLiveExpressions]você pode descobrir que seus fluxos de trabalho são mais eficazes e obter resultados melhores.</span><span class="sxs-lookup"><span data-stu-id="76c52-172">When you use [Breakpoint Debugging][DevtoolsJavascriptBreakpoints] or [Live Expressions][DevtoolsConsoleLiveExpressions], you may find that your workflows are more effective and you get better results.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="76c52-173">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="76c52-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
