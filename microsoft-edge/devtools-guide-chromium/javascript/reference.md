---
title: Referência de depuração JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581737"
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







# Referência de depuração JavaScript   



Descubra os novos fluxos de trabalho de depuração com esta referência abrangente de recursos de depuração do Microsoft Edge DevTools.  

Consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevToolsJavascriptGetStarted] para aprender as noções básicas de depuração.  

## Pausar código com pontos de interrupção   

Defina um ponto de interrupção para que você possa pausar seu código no meio do tempo de execução.  

Consulte [Pausar um código com pontos de interrupção][DevToolsJavascriptBreakpoints] para saber como definir pontos de interrupção.  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools"  

## Depurar o código   

Depois que o seu código for pausado, percorra-o, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.  

### Etapa sobre linha de código   

Quando pausado em uma linha de código contendo uma função que não é relevante para o problema que você está Depurando, clique no ícone de **etapa sobre** a etapa sobre ![ ][ImageStepOverIcon] para executar a função sem fazer a depuração.  

> ##### Figura 1  
> Selecionando o passar **sobre**  
> ![Selecionando o passar sobre][ImageSelectingStepOver]  

Por exemplo, suponha que você esteja Depurando o código a seguir:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Você está pausado `A` .  Pressionando a **etapa**, o devtools executa todo o código na função que você está Depurando, que é `B` e `C` .  DevTools, em seguida, faz uma pausa `D` .  

### Etapa na linha de código   

Quando pausado em uma linha de código contendo uma chamada de função relacionada ao problema que você está Depurando, clique no ícone **Step Into** ![ Step Into ][ImageStepIntoIcon] para investigar mais a função.  

> ##### Figura 2  
> Selecionando **a etapa em**  
> ![Selecionando a etapa em][ImageSelectingStepInto]  

Por exemplo, suponha que você esteja Depurando o código a seguir:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Você está pausado `A` .  Ao pressionar **Step Into**, o devtools executa essa linha de código e, em seguida, pausa em `B` .  

### Etapa da linha de código   

Quando pausado dentro de uma função que não está relacionada ao problema que você está Depurando, clique no ícone de Step **out** Step Out ![ ][ImageStepOutIcon] para executar o restante do código da função.  

> ##### Figura 3  
> Selecionando o **Step Out**  
> ![Selecionando o Step Out][ImageSelectingStepOut]  

Por exemplo, suponha que você esteja Depurando o código a seguir:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Você está pausado `A` .  Ao pressionar a **etapa**, o devtools executa o restante do código `getName()` , que está apenas `B` neste exemplo e, em seguida, pausa em `C` .  

### Executar todo o código em uma linha específica   

Durante a depuração de uma função longa, pode haver muitos códigos que não estão relacionados ao problema que você está depurando.  

Você pode optar por percorrer todas as linhas, mas isso é entediante.  Você pode optar por definir um ponto de interrupção de linha de código na linha em que você está interessado e clicar no ícone **retomar** a ![ execução do script de retomada de script ][ImageResumeScriptExecutionIcon] , mas há uma maneira mais rápida.  

Clique com o botão direito do mouse na linha de código na qual você está interessado e selecione **continuar até aqui**.  O DevTools executa todo o código até esse ponto e, em seguida, faz uma pausa nessa linha.  

> ##### Figura 4  
> Selecione **continuar até aqui**  
> ![Selecione continuar até aqui][ImageSelectingContinueToHere]  

### Reinicie a função superior da pilha de chamadas   

Enquanto pausado em uma linha de código, clique com o botão direito do mouse em qualquer lugar no painel de **pilha de chamadas** e selecione **reiniciar quadro** para pausar na primeira linha da função superior na pilha de chamadas.  A função Top é a última função que foi chamada.  

Por exemplo, suponha que você esteja percorrendo o código a seguir:  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Você está pausado `A` .  Depois de clicar em **reiniciar quadro**, você deve pausar `B` , sem precisar definir um ponto de interrupção ou pressionar **retomar a execução do script**.  

> ##### Figura 5  
> Selecionar **reiniciar quadro**  
> ![Selecionar reiniciar quadro][ImageSelectingRestartFrame]  

### Retomar o tempo de execução do script   

Para continuar o tempo de execução após uma pausa do seu script, clique no ícone de execução **retomar** ![ script de retomada de execução de script ][ImageResumeScriptExecutionIcon] .  DevTools executa o script até o próximo ponto de interrupção, se houver.  

> ##### Figura 6  
> Selecionando **continuar execução do script**  
> ![Selecionando continuar execução do script][ImageSelectingResumeScriptExecution]  

#### Forçar tempo de execução de script   

Para ignorar todos os pontos de interrupção e forçar o reinício do script, clique e mantenha pressionado o ícone de execução do script de retomada da **execução** do script ![ ][ImageResumeScriptExecutionIcon] e, em seguida, selecione **forçar** execução do script ![ Force ][ImageForceScriptExecutionIcon] .  

> ##### Figura 7  
> Selecionar **forçar execução de script**  
> ![Selecionar forçar execução de script][ImageSelectingForceScriptExecution]  

### Alterar o contexto do thread   

Ao trabalhar com trabalhadores da Web ou funcionários do serviço, clique em um contexto listado no painel **threads** para alternar para esse contexto.  O ícone de seta azul representa qual contexto está selecionado no momento.  

> ##### Figura 8  
> O painel **threads**  
> ![O painel threads][ImageThreadsPane]  

Por exemplo, suponha que você está pausado em um ponto de interrupção no script principal e no seu roteiro de trabalho do serviço.  Você deseja exibir as propriedades locais e globais do contexto do trabalho do serviço, mas o painel **fontes** está mostrando o contexto do script principal.  Ao clicar na entrada do serviço de trabalho no painel **threads** , você deve ser capaz de alternar para esse contexto.  

## Exibir e editar propriedades locais, de fechamento e globais   

Enquanto pausado em uma linha de código, use o painel **escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.  

*   Clique duas vezes em um valor de propriedade para alterá-lo.  
*   As propriedades não enumeráveis ficam acinzentadas.  

> ##### Figura 9  
> O painel **escopo**  
> ![O painel escopo][ImageScopePane]  

## Exibir a pilha de chamadas atual   

Enquanto pausado em uma linha de código, use o painel de **pilha de chamadas** para ver a pilha de chamadas que você recebeu para este ponto.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Clique em uma entrada para saltar para a linha de código em que essa função foi chamada.  O ícone de seta azul representa qual função DevTools está realçando no momento.  

> ##### Figura 10  
> O painel **pilha de chamadas**  
> ![O painel pilha de chamadas][ImageCallStackPane]  

> [!NOTE]
> Quando não pausa em uma linha de código, o painel **pilha de chamadas** está vazio.  

### Copiar rastreamento de pilha   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Clique com o botão direito do mouse em qualquer lugar no painel de **pilha de chamadas** e selecione **copiar rastreamento de pilha** para copiar a pilha de chamadas atual para a área de transferência.  

> ##### Figura 11  
> Selecionar o **rastreamento de pilha de cópia**  
> ![Selecionar o rastreamento de pilha de cópia][ImageSelectingCopyStackTrace]  

Veja a seguir um exemplo da saída:  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Ignorar um script ou um padrão de scripts  

Marque um script como código da biblioteca quando quiser ignorar esse script durante a depuração.  Quando marcado como código de biblioteca, um script fica obscurecido no painel de **pilha de chamadas** , e você nunca percorre as funções do script quando percorre o código.  

Por exemplo, suponha que você esteja passando por esse código:  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` é uma biblioteca de terceiros em que você confia.  Se você tiver certeza de que o problema que está depurando não está relacionado à biblioteca de terceiros, faça sentido marcar o script como código de **biblioteca**.  

### Marcar um script como código da biblioteca no painel do editor  

Para marcar um script como **código de biblioteca** no painel do **Editor** :  

1.  Abra o arquivo.  
1.  Clique com o botão direito do mouse em qualquer lugar.  
1.  Selecione **Marcar como código da biblioteca**.  

> ##### Figura 12  
> Marcando um script como **código de biblioteca** no painel do **Editor**  
> ![Marcando um script como código de biblioteca no painel do editor][ImageMarkEditorPane]  

### Marcar um script como código da biblioteca no painel pilha de chamadas  

Para marcar um script como **código de biblioteca** no painel **pilha de chamadas** :  

1.  Clique com o botão direito do mouse em uma função do script.  
1.  Selecione **Marcar como código da biblioteca**.  

> ##### Figura 13  
> Marcando um script como **código da biblioteca** no painel pilha de **chamadas**  
> ![Marcando um script como código da biblioteca no painel pilha de chamadas][ImageMarkCallStackPane]  

### Marcar um script como código de biblioteca em configurações  

Para marcar um único script ou um padrão de scripts em configurações:  

1.  Abrir [as configurações][DevToolsCustomize].  
1.  Vá para a guia **código da biblioteca** .  
1.  Clique em **Adicionar padrão**.  
1.  Digite o nome do script ou um padrão de Regex de nomes de script para marcar como **código de biblioteca**.  
1.  Clique em **Adicionar**.  

> ##### Figura 14  
> Marcando um script como **código de biblioteca** em configurações  
> ![Marcando um script como código de biblioteca em configurações][ImageMarkScriptSettings]  

## Executar trechos de código de depuração de qualquer página   

Se você estiver executando o mesmo código de depuração no console repetidamente, considere os trechos de código.  Trechos de código são scripts de tempo de execução que você cria, armazena e executa dentro do DevTools.  

Consulte [executar trechos de código em qualquer página][DevToolsJavascriptSnippets] para saber mais.  

## Assista aos valores de expressões JavaScript personalizadas   

Use o painel de **inspeção** para ver os valores de expressões personalizadas.  Você pode assistir a uma expressão JavaScript válida.  

> ##### Figura 15  
> O painel de **inspeção**  
> ![O painel de inspeção][ImageWatchPane]  

*   Clique no ícone **Adicionar expressão** ![ Adicionar expressão ][ImageAddExpressionIcon] para criar uma nova expressão de inspeção.  
*   Clique no ícone **Atualizar** ![ atualização ][ImageRefreshIcon] para atualizar os valores de todas as expressões existentes.  Valores são atualizados automaticamente durante a depuração do código.  
*   Passe o mouse sobre uma expressão e clique no ícone **excluir** expressão de ![ exclusão de expressão ][ImageDeleteExpressionIcon] para excluí-la.  

## Torne um arquivo do minified legível   

Clique no ícone formato de **formato** ![ ][ImageFormatIcon] para fazer com que um arquivo do minified seja legível pelo homem.  

> ##### Figura 16  
> O botão **Formatar**  
> ![O botão Formatar][ImageFormat]  

## Editar um script   

Ao corrigir um bug, você muitas vezes deseja testar algumas alterações no código JavaScript.  Você não precisa fazer as alterações em um editor externo ou IDE e, em seguida, recarregar a página.  Você pode editar o script no DevTools.  

Para editar um script:  

1.  Abra o arquivo no painel **Editor** do painel **fontes** .  
1.  Faça suas alterações no painel do **Editor** .  
1.  Pressione `Ctrl` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar.  O DevTools patches de todo o arquivo JS para o mecanismo JavaScript do Microsoft Edge.  

> ##### Figura 17  
> Painel do **Editor**  
> ![Painel do editor][ImageEditorPane]  

## Desabilitar JavaScript   

Consulte [desabilitar JavaScript com o Microsoft Edge devtools][DevToolsJavascriptDisable].  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Figura 1: selecionando a etapa sobre"  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Figura 2: selecionando Step in"  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Figura 3: selecionando o Step Out"  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Figura 4: selecionar continuar até aqui"  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Figura 5: selecionando reiniciar quadro"  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Figura 6: selecionando retomar execução do script"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Figura 7: seleção forçar execução de script"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Figura 8: o painel threads"  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Figura 9: o painel escopo"  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Figura 10: o painel de pilha de chamadas"  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Figura 11: selecionando o rastreamento de pilha de cópia"  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Figura 12: marcando um script como código da biblioteca no painel do editor"  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Figura 13: marcando um script como código de biblioteca a partir do painel de pilha de chamadas"  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Figura 14: marcando um script como código de biblioteca de configurações"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Figura 15: o painel de inspeção"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Figura 16: o botão Formatar"  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Figura 17: painel do editor"  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools"  
[DevToolsJavascriptGetStarted]: index.md "Introdução à depuração de JavaScript no Microsoft Edge DevTools"  
[DevToolsJavascriptSnippets]: snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  

[DevToolsCustomize]: ../customize/index.md "Personalizar o Microsoft Edge DevTools"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
