---
description: Descubra novos fluxos de trabalho de depuração nesta referência abrangente dos recursos de depuração do Microsoft Edge DevTools.
title: Referências de depuração de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2944e054a08a901d2e1752fa7c4e48ae110f5787
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439455"
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

# <a name="javascript-debugging-reference"></a>Referências de depuração de JavaScript  

Descubra novos fluxos de trabalho de depuração com a seguinte referência abrangente dos recursos de depuração do Microsoft Edge DevTools.  

Para saber as noções básicas de depuração, navegue até Começar a [depurar JavaScript no Microsoft Edge DevTools][DevToolsJavascriptGetStarted].  

## <a name="pause-code-with-breakpoints"></a>Pausar código com pontos de interrupção  

De definir um ponto de interrupção para que você possa pausar seu código no meio do tempo de execução.  

Para saber como definir pontos de interrupção, navegue até [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].  

## <a name="step-through-code"></a>Passo a passo código  

Depois que seu código for pausado, passo a passo por ele, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.  

### <a name="step-over-line-of-code"></a>Passo a passo sobre a linha de código  

Quando pausado em uma linha de código que contém uma função que não é relevante para o problema que você está depurando, escolha o botão **Passo** a passo \( Passo a passo \) para executar a função sem entrar ![ ](../media/step-over-icon.msft.png) nele.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Escolha Passo a passo" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Escolha **Passo a passo**  
:::image-end:::  

Por exemplo, suponha que você está depurando o seguinte trecho de código.  

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

Você está pausado em `A` .  Depois de escolher **Passo a Passo,** o DevTools executa todo o código na função que você está passando, que é `B` e `C` .  Em seguida, o DevTools pausa `D` em .  

### <a name="step-into-line-of-code"></a>Entrar na linha de código  

Quando pausado em uma linha de código que contém uma chamada de função relacionada ao problema que você está depurando, escolha o botão **Entrar** em \( Entrar em \) para investigar ainda mais essa ![ ](../media/step-into-icon.msft.png) função.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Escolha Entrar" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Escolha **Entrar**  
:::image-end:::  

Por exemplo, suponha que você está depurando o seguinte trecho de código.  

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

Você está pausado em `A` .  Depois de escolher **Entrar,** o DevTools executa essa linha de código e pausa em `B` .  

### <a name="step-out-of-line-of-code"></a>Sair da linha de código  

Quando pausado dentro de uma função que não está relacionada ao problema que você está depurando, escolha o botão **Sair** \( Sair \) para executar o restante do código da ![ ](../media/step-out-icon.msft.png) função.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Escolha Sair" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Escolha **Sair**  
:::image-end:::  

Por exemplo, suponha que você está depurando o seguinte trecho de código.  

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

Você está pausado em `A` .  Depois de escolher **Sair,** o DevTools executa o restante do código em , que está apenas neste exemplo e, em `getName()` `B` seguida, pausa em `C` .  

### <a name="run-all-code-up-to-a-specific-line"></a>Executar todo o código até uma linha específica  

Ao depurar uma função longa, pode haver muito código que não está relacionado ao problema que você está depurando.  

Você pode optar por passar por todas as linhas, mas isso é entediante.  Você pode optar por definir um ponto de interrupção de linha de código na linha na qual você está interessado e, em seguida, escolher o botão Retomar Execução de **Script** \( Retomar Execução de Script \) mas há uma maneira mais ![ ](../media/resume-script-run-icon.msft.png) rápida.  

Passe o mouse na linha de código na qual você está **interessado,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha Continuar até aqui .  O DevTools executa todo o código até esse ponto e pausa nessa linha.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Escolha Continuar até aqui" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Escolha **Continuar até aqui**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Reinicie a função superior da pilha de chamada  

Para pausar na primeira linha da função superior na pilha de chamada, enquanto estiver pausado em uma linha de código, passe o mouse em qualquer lugar no painel **Pilha** de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Reiniciar Quadro**.  A função superior é a última função que foi executado.  

O trecho de código a seguir é um exemplo para você fazer o passo a passo.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Você está pausado em `A` .  Depois de **escolher Reiniciar Quadro**, você deve ser pausado em , sem nunca definir um ponto de interrupção ou escolher Retomar execução de `B` **script**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Escolha Reiniciar Quadro" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Escolha **Reiniciar Quadro**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Retomar o tempo de execução do script  

Para continuar o tempo de execução após uma pausa do seu script, escolha o botão Retomar Execução de **Script** \( ![ Retomar Execução de Script ](../media/resume-script-run-icon.msft.png) \).  O DevTools executa o script até o próximo ponto de interrupção, se for o caso.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Escolha Retomar execução de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Escolha **Retomar execução de script**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Forçar o tempo de execução do script  

Para ignorar todos os pontos de interrupção e forçar seu script a continuar em execução, escolha e segure o botão Retomar Execução de Script **\(** Retomar Execução de Script \) e escolha o botão Forçar execução de script \( Forçar execução ![ de script ](../media/resume-script-run-icon.msft.png) **** ![ ](../media/force-script-run-icon.msft.png) \) .  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Escolha Forçar execução de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Escolha **Forçar execução de script**  
:::image-end:::  

### <a name="change-thread-context"></a>Alterar contexto de thread  

Ao trabalhar com funcionários da Web ou funcionários de serviços, escolha um contexto listado no **painel Threads** para alternar para esse contexto.  O ícone de seta azul representa qual contexto está selecionado no momento.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="O painel Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   O **painel Threads**  
:::image-end:::  

Por exemplo, suponha que você tenha pausado em um ponto de interrupção no script principal e no script de trabalho do serviço.  Você deseja exibir as propriedades locais e globais para o contexto de trabalho do serviço, mas o painel **Fontes** está mostrando o contexto principal do script.  Ao escolher a entrada do trabalhador do serviço no **painel Threads,** você deve ser capaz de alternar para esse contexto.  

## <a name="view-and-edit-local-closure-and-global-properties"></a>Exibir e editar propriedades locais, de fechamento e globais  

Enquanto estiver pausado em uma linha de código, use o painel **Escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.  

*   Clique duas vezes em um valor de propriedade para alterá-lo.  
*   Propriedades não enumeradas estão acinzenadas.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   O **painel Escopo**  
:::image-end:::  

## <a name="view-the-current-call-stack"></a>Exibir a pilha de chamada atual  

Enquanto estiver pausado em uma linha de código, use o painel **Pilha** de Chamada para exibir a pilha de chamada que o fez chegar a esse ponto.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Escolha uma entrada para ir para a linha de código onde essa função foi chamada.  O ícone de seta azul representa qual função DevTools está realçando no momento.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="O painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   O **painel Pilha de** Chamada  
:::image-end:::  

> [!NOTE]
> Quando não pausado em uma linha de código, o painel **Pilha de** Chamada fica vazio.  

### <a name="copy-stack-trace"></a>Copiar rastreamento de pilha  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

para copiar a pilha de chamada atual para **** a área de transferência, passe o mouse em qualquer lugar no painel Pilha de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar rastreamento **de**pilha .  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Escolha Copiar Rastreamento de Pilha" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Escolha **Copiar Rastreamento de Pilha**  
:::image-end:::  

O trecho de código a seguir é um exemplo da saída.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a>Ignorar um script ou um padrão de scripts  

Marque um script como código de biblioteca quando quiser ignorar esse script durante a depuração.  Quando marcado como código biblioteca, um **** script é obscurecido no painel Pilha de Chamada e você nunca entra nas funções do script quando passa pelo código.  

O trecho de código a seguir é um exemplo para você fazer o passo a passo.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` é uma biblioteca de terceiros em que você confia.  Se você estiver confiante de que o problema que você está depurando não está relacionado à biblioteca de terceiros, então faz sentido marcar o script como código **biblioteca**.  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Marcar um script como código biblioteca do painel Editor  

Conclua as seguintes ações para marcar um script como **código biblioteca** no **painel Editor.**  

1.  Abra o arquivo.  
1.  Passe o mouse em qualquer lugar e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Marcar como código da biblioteca.**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marcar um script como **código biblioteca** do **painel Editor**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Marcar um script como código biblioteca do painel Pilha de Chamada  

Conclua as seguintes ações para marcar um script como **código biblioteca** do painel **Pilha de** Chamada.  

1.  Passe o mouse em uma função do script e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Marcar como código da biblioteca.**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marcar um script como **código biblioteca do** painel Pilha **de** Chamada  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Marcar um script como código de biblioteca a partir de Configurações  

Conclua as seguintes ações para marcar um único script ou padrão de scripts de **Configurações**.  

1.  Configurações [abertas][DevToolsCustomize].  
1.  Navegue até **a configuração de código biblioteca.**  
1.  Escolha **Adicionar padrão**.  
1.  Insira o nome do script ou um padrão regex de nomes de script para marcar como **código biblioteca**.  
1.  Escolha **Adicionar**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar um script como código de biblioteca a partir de Configurações" lightbox="../media/javascript-framework-library-code.msft.png":::
       Marcar um script como **código de biblioteca** a partir de **Configurações**  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a>Executar trechos de código de depuração de qualquer página  

Se você estiver executando o mesmo código de depuração no Console uma e outra vez, considere Trechos.  Trechos de código são scripts de tempo de execução que você pode escrever, armazenar e executar no DevTools.  

Para saber mais, navegue [até Executar trechos de código em qualquer página.][DevToolsJavascriptSnippets]  

## <a name="watch-the-values-of-custom-javascript-expressions"></a>Assista aos valores de expressões JavaScript personalizadas  

Use o **painel** de relógio para observar os valores de expressões personalizadas.  Você pode assistir a qualquer expressão JavaScript válida.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="O painel de relógio" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   O **painel** de relógio  
:::image-end:::  

*   Escolha o **botão Adicionar Expressão** \( Adicionar Expressão ![ ](../media/add-expression-icon.msft.png) \) para criar uma nova expressão de relógio.  
*   Escolha o **botão Atualizar** \( ![ Atualizar ](../media/refresh-icon.msft.png) \) para atualizar os valores de todas as expressões existentes.  Os valores são atualizados automaticamente ao passar pelo código.  
*   Passe o mouse em uma expressão e escolha o botão **Excluir Expressão** \( Excluir ![ Expressão ](../media/delete-expression-icon.msft.png) \) para excluí-la.  

## <a name="make-a-minified-file-readable"></a>Tornar um arquivo minificado acessível  

Escolha o **botão Formatar** \( ![ Formatar ](../media/format-icon.msft.png) \) para tornar um arquivo minificado acessível.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="O botão Formatar" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   O **botão Formatar**  
:::image-end:::  

## <a name="edit-a-script"></a>Editar um script  

Ao corrigir um bug, muitas vezes você deseja testar algumas alterações no código JavaScript.  Você não precisa fazer as alterações em um editor externo ou IDE e atualizar a página.  Você pode editar seu script no DevTools.  

Conclua as seguintes ações para editar um script.  

1.  Abra o arquivo no **painel Editor** do painel **Fontes.**  
1.  Faça suas alterações no **painel Editor.**  
1.  Selecione `Ctrl` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.  O DevTools remenda todo o arquivo JS no mecanismo JavaScript do Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="O painel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       O **painel Editor**  
    :::image-end:::  
     
## <a name="disable-javascript"></a>Desabilitar o JavaScript  

Navegue [até Desabilitar JavaScript com o Microsoft Edge DevTools][DevToolsJavascriptDisable].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar o Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
