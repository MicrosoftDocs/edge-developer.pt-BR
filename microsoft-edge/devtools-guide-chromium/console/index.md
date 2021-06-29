---
description: Uma introdução à ferramenta Console dentro das ferramentas Microsoft Edge Desenvolvedor.
title: Usar o Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: badcaae0ad637fe7a027f78d00daf9133789693e
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624742"
---
# <a name="use-the-console"></a>Usar o Console  

A **ferramenta Console** do DevTools ajuda você com várias tarefas.  A lista a seguir inclui algumas das tarefas.  

*   Descubra por que algo não está funcionando no projeto atual e [rastreia problemas.][DevtoolsConsoleConsoleDebugJavascript]  
*   [Obter informações sobre o projeto Web][DevtoolsConsoleConsoleFilters] no navegador como mensagens de log.  
*   [Informações de][DevtoolsConsoleConsoleLog] log em scripts para fins de depuração.  
*   [Experimente expressões JavaScript ao][DevtoolsConsoleConsoleJavascript] vivo em um [ambiente REPL.][WikiReadEvalPrintLoop]  
*   [Interaja com o projeto web no navegador usando][DevtoolsConsoleConsoleDomInteraction] JavaScript.  
    
O **Console** é uma ótima ferramenta de companhia a ser usada com outras ferramentas.  O **Console** fornece uma maneira poderosa de executar scripts, inspecionar e manipular a página da Web atual usando JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="A ferramenta Console aberta no painel superior" lightbox="../media/console-intro-console-main.msft.png":::
         A **ferramenta Console** aberta no painel superior  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Console no painel inferior com a ferramenta Elements aberta acima dele" lightbox="../media/console-intro-console-panel.msft.png":::
         **Console** no painel inferior com a **ferramenta Elements** aberta acima dele  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

A maneira mais rápida de abrir diretamente o **Console** é selecionar `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  

## <a name="error-reports-and-console"></a>Relatórios de erro e Console  

**Console** é o local padrão em que os erros de conectividade e JavaScript são relatados.  Se ocorrer algum erro, o contador **Problemas** será exibido ao lado do ícone Configurações **no** DevTools que fornece o número de erros e avisos.  Selecione o **contador Problemas** para abrir a **ferramenta Problemas** e exibir o problema.  Para obter mais informações, navegue até [Depurar erros relatados no Console][DevtoolsConsoleConsoleDebugJavascript].

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="O DevTools fornece informações detalhadas sobre o erro no Console" lightbox="../media/console-debug-displays-error.msft.png":::
   O DevTools fornece informações detalhadas sobre o erro no **Console**  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a>Inspecionar e filtrar informações na página da Web atual  

Quando você abre o DevTools em uma página da Web, pode haver uma quantidade avassaladora de informações no **Console.**  A quantidade de informações se torna um problema quando você precisa identificar informações importantes.  Para exibir as informações importantes que precisam de ação, use a [ferramenta Problemas][DevtoolsIssuesIndex] no DevTools.

Os problemas estão sendo movidos gradualmente do **Console** para a **ferramenta Issues.**  No entanto, ainda há muitas informações no **Console**, e é por isso que é uma boa ideia saber sobre as opções automatizadas de log e filtro no **Console**.  Para obter mais informações, navegue até [Filtrar mensagens de Console.][DevtoolsConsoleConsoleFilters]

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools com um Console cheio de mensagens" lightbox="../media/console-intro-noise.msft.png":::
   DevTools com um **Console** cheio de mensagens  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a>Informações de log a ser exibidas no Console  

O caso de uso mais popular para **o Console** é registrar informações de seus scripts usando o método ou outros `console.log()` métodos semelhantes.  Para experimentar, conclua as seguintes ações.  

1.  Para abrir **Console,** selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  
1.  Navegue [até Console de exemplos de mensagens: log, informações,][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]erro e aviso , ou copie e execute o seguinte trecho de código no **Console**.  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  O **Console** exibe os resultados.  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Console cheio de mensagens causadas pelo código de demonstração" lightbox="../media/console-intro-logging.msft.png":::
       **Console** cheio de mensagens causadas pelo código de demonstração  
    :::image-end:::  
    
Muitos métodos úteis estão disponíveis quando você trabalha com o **Console**.  Para obter mais informações, navegue até [Registrar mensagens na ferramenta Console.][DevtoolsConsoleConsoleLog]  

## <a name="try-your-javascript-live-in-the-console"></a>Experimente seu JavaScript ao vivo no Console  

O **Console** não é apenas um local para registrar informações.  O **Console** é um [ambiente REPL.][WikiReadEvalPrintLoop]  Quando você escreve qualquer JavaScript no **Console**, o código é executado imediatamente.  Você pode achar útil testar alguns novos recursos JavaScript ou fazer alguns cálculos rápidos.  Além disso, você pode obter todos os recursos esperados de um ambiente de edição moderno, como autocompleção, realce de sintaxe e histórico.  Para experimentar, conclua as seguintes ações.  

1.  Navegue até **o Console**.  
1.  Digite `2 + 2`.  
    
O **Console** exibe o resultado `4` na linha a seguir.  Esse **recurso de avaliação** do Eager é útil para depurar e verificar se você não está cometendo erros em seu código.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="O Console exibe o resultado de 2 + 2 ao vivo à medida que você digita" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   O **Console** exibe o resultado de `2 + 2` vida ao digitá-lo  
:::image-end:::  

Para executar a expressão JavaScript no **Console** e, opcionalmente, exibir um resultado, selecione `Enter` .  Em seguida, você pode escrever o próximo código JavaScript a ser executado no **Console**.  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Executar várias linhas de código JavaScript em sucessão" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Executar várias linhas de código JavaScript em sucessão  
:::image-end:::  

Por padrão, você executar código JavaScript em uma única linha.  Para executar uma linha, digite o JavaScript e selecione `Enter` .  Para trabalhar com a limitação de linha única, selecione em `Shift` + `Enter` vez de `Enter` .  Semelhante a outras experiências de linha de comando, para acessar seus comandos JavaScript anteriores, selecione `Arrow-Up` .  O recurso de comcompleção automática do **Console** é uma ótima maneira de aprender sobre métodos desconhecidos.  Para experimentar, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Digite `doc`.  
1.  Escolha `document` no menu suspenso.  
1.  Selecione a `tab` chave para escolher.  
1.  Digite `.bo`.  
1.  Selecione `tab` para obter `document.body` .  
1.  Digite outro para exibir a lista completa de propriedades e métodos disponíveis no corpo `.` da página da Web atual.  
    
Para obter mais informações sobre todas as maneiras de trabalhar com **Console,** navegue até [Console como um ambiente JavaScript.][DevtoolsConsoleConsoleJavascript]  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Console autocompletion of JavaScript expressions" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Console** autocompletion of JavaScript expressions  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a>Interagir com a página da Web atual no navegador  

O **Console** tem acesso ao [objeto Window][MdnDocsWebApiWindow] do navegador.  Você pode escrever scripts que interagem com a página da Web atual.  Para experimentar, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Copie e colar o seguinte trecho de código.  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copiar o conteúdo de título superior (h1) do DOM e exibir no Console" lightbox="../media/console-intro-reading-DOM.msft.png":::
   Copie o conteúdo de título superior \( `h1` \) do DOM e exibido no **Console**  
:::image-end:::  

Em vez de apenas ler da página da Web, você também pode alterá-la.  Para tentar alterar a página da Web, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Copie e colar o seguinte trecho de código.  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Gravar texto no DOM no Console" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   Gravar texto no DOM no **Console**  
:::image-end:::  

Você alterou o título principal da página da Web para **"Balançando o Console".**  Os **métodos Utilitário** de Console facilitam o acesso e manipulação da página da Web atual.  Para obter mais informações, navegue até [Console Utilities API reference][DevtoolsConsoleUtilities].  Por exemplo, para adicionar uma borda verde em torno de todos os links na página da Web atual, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Copie e colar o seguinte trecho de código.  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    
:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipular uma seleção de elementos usando o Console" lightbox="../media/console-intro-changing-styles.msft.png":::
    Manipular uma seleção de elementos usando o **Console**  
:::image-end:::  

Para obter mais informações sobre como trabalhar com o DOM, navegue até [Usar o Console para interagir com o DOM][DevtoolsConsoleConsoleDomInteraction].  

## <a name="learn-more-about-console"></a>Saiba mais sobre Console  

Para obter mais informações sobre **o Console,** navegue até [Referência de Console,][DevtoolsConsoleReference]Referência da [API de Utilitários][DevtoolsConsoleUtilities]de Console e [Referência da API do Console.][DevtoolsConsoleApi]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Erros de depuração relatados no Console | Microsoft Docs"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use o Console para interagir com o dom | Microsoft Docs" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrar mensagens de console | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console como um ambiente JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensagens na ferramenta Console | Microsoft Docs"  
[DevtoolsConsoleReference]: ./reference.md "Console reference | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Encontre e corrige problemas usando a ferramenta Problemas | Microsoft Docs"  
<!-- external links -->
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Exemplos de mensagens de console: log, informações, erro e aviso | GitHub"  
[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Janela | MDN"  
[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Loop de leitura-eval-print | Wikipédia"  
