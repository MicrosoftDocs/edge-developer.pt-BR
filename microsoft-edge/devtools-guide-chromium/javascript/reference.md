---
description: Descubra novos fluxos de trabalho de depuração nesta referência abrangente dos recursos de depuração do Microsoft Edge DevTools.
title: Usar os recursos de depurador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 6fb90a70e0aac9f556fa9f5f02afee1fd5b4962e
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519601"
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

# <a name="use-the-debugger-features"></a>Usar os recursos de depurador

Este artigo aborda como usar o depurador no Microsoft Edge DevTools, incluindo como definir um ponto de interrupção de linha de código.  Para definir outros tipos de pontos de interrupção, consulte [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].  

Para saber as noções básicas de depuração, navegue até Introdução à depuração do JavaScript no [Microsoft Edge DevTools,][DevToolsJavascriptGetStarted]que é um tutorial que usa uma página da Web baseada em formulário existente.  O tutorial tem capturas de tela, para que você possa skim-lo.  Você pode experimentar facilmente os recursos de depurador usando a página da Web de demonstração.

## <a name="view-and-edit-javascript-code"></a>Exibir e editar código JavaScript

Ao corrigir um bug, muitas vezes você deseja experimentar algumas alterações no código JavaScript.  Não é necessário fazer as alterações em um editor externo ou no IDE, carregar o arquivo no servidor e atualizar a página. em vez disso, para testar alterações, você pode editar seu código JavaScript diretamente no DevTools e ver o resultado imediatamente.  

Para exibir e editar um arquivo JavaScript:  

1.  Navegue até a **ferramenta Sources.**  
1.  No painel **Navegador,** selecione seu arquivo, para abri-lo no **painel Editor.**
1.  No painel **Editor,** edite seu arquivo.  
1.  Selecione `Ctrl` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar.  Em seguida, o DevTools carrega o arquivo JavaScript no mecanismo JavaScript do Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="O painel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       O **painel Editor**  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a>Reformata um arquivo JavaScript minificado com impressão bastante impressa

Para tornar um arquivo minificado acessível, escolha o botão **Formatar** \( Formatar \) na parte inferior ![ do painel ](../media/format-icon.msft.png) **Editor.**

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="O botão Formatar" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   O **botão Formatar**  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a>Definir um ponto de interrupção, para pausar código

Para pausar seu código no meio do tempo de execução, de definir um ponto de interrupção.  O tipo de ponto de interrupção mais básico e conhecido é um ponto de interrupção de linha de código.

Use um ponto de interrupção de linha de código quando você conhecer a região exata do código que precisa investigar.  O DevTools sempre pausa na linha de código especificada, antes de ser executado.

Para definir um ponto de interrupção de linha de código:  

1.  Navegue até a **ferramenta Sources.**  
1.  Abra o arquivo que contém a linha de código.  
1.  Selecione a área à esquerda do número de linha para a linha de código.  Ou clique com o botão direito do mouse no número da linha e escolha **Adicionar ponto de interrupção**.  Em seguida, um círculo vermelho aparece ao lado do número da linha, indicando um ponto de interrupção.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Um ponto de interrupção de linha de código  
    :::image-end:::  

Os pontos de interrupção de linha de código podem ser ineficientes para definir, especialmente se você não sabe exatamente onde procurar ou se sua base de código é grande.  Para economizar tempo durante a depuração, saiba como e quando usar os outros tipos de pontos de interrupção.  Para obter mais informações, navegue até [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].

## <a name="step-through-code"></a>Passo a passo código  

Depois que seu código é pausado em um ponto de interrupção, passo pelo código, uma linha por vez, investigando o fluxo de controle e os valores de propriedade ao longo do caminho.  

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

Você pode optar por passar por todas as linhas, mas isso é entediante.  Você pode optar por definir um ponto de interrupção de linha de código na linha na qual você está interessado e, em seguida, escolher o botão Retomar execução de **script** \( Retomar execução de script \) mas há uma maneira mais ![ ](../media/resume-script-run-icon.msft.png) rápida.  

Passe o mouse na linha de código na qual você está **interessado,** abra o menu contextual \(clique com o botão direito do mouse\) e escolha Continuar até aqui .  O DevTools executa todo o código até esse ponto e pausa nessa linha.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Escolha Continuar até aqui" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Escolha **Continuar até aqui**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Reinicie a função superior da pilha de chamada  

Para pausar na primeira linha da função superior na pilha de chamada, enquanto pausada em uma linha de código, passe o mouse em qualquer lugar no painel **Pilha** de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Reiniciar**quadro .  A função superior é a última função que foi executado.  

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

Você está pausado em `A` .  Depois de **escolher Reiniciar quadro**, você deve ser pausado em , sem nunca definir um ponto de interrupção ou escolher Retomar execução de `B` **script**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Escolha Reiniciar quadro" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Escolha **Reiniciar quadro**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Retomar o tempo de execução do script  

Para continuar o tempo de execução após uma pausa do script, escolha o botão Retomar execução de **script** \( ![ Retomar execução de script ](../media/resume-script-run-icon.msft.png) \).  O DevTools executa o script até o próximo ponto de interrupção, se for o caso.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Escolha Retomar execução de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Escolha **Retomar execução de script**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Forçar o tempo de execução do script  

Para ignorar todos os pontos de interrupção e forçar seu script a continuar a ser executado, escolha e segure o botão Retomar execução de script **\(** Retomar execução de script \) e escolha o botão Forçar execução de script \( Forçar execução ![ de script ](../media/resume-script-run-icon.msft.png) **** ![ ](../media/force-script-run-icon.msft.png) \) .  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Escolha Forçar execução de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Escolha **Forçar execução de script**  
:::image-end:::  

### <a name="change-thread-context"></a>Alterar contexto de thread  

Ao trabalhar com funcionários da Web ou funcionários de serviços, escolha um contexto listado no **painel Threads** para alternar para esse contexto.  O ícone de seta azul representa qual contexto está selecionado no momento.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="O painel Threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   O **painel Threads**  
:::image-end:::  

Por exemplo, suponha que você tenha pausado em um ponto de interrupção no script principal e no script de trabalho do serviço.  Você deseja exibir as propriedades locais e globais para o contexto de trabalho do serviço, mas a ferramenta **Sources** está mostrando o contexto de script principal.  Para alternar para o contexto de trabalho do serviço, no **painel Threads,** escolha a entrada do trabalhador do serviço.  

## <a name="view-and-edit-properties-and-variables"></a>Exibir e editar propriedades e variáveis

Enquanto estiver pausado em uma linha de código, use o painel **Escopo** para exibir e editar os valores de propriedades e variáveis nos escopos local, fechamento e global.  

*   Clique duas vezes em um valor de propriedade para alterá-lo.  
*   Propriedades não enumeradas estão acinzenadas.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   O **painel Escopo**  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a>Assista aos valores das expressões JavaScript  

Use o **painel** de relógio para observar os valores de expressões personalizadas.  Você pode assistir a qualquer expressão JavaScript válida.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="O painel de relógio" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   O **painel** de relógio  
:::image-end:::  

*   Para criar uma nova expressão de relógio, selecione o botão **Adicionar expressão de relógio** \( Adicionar expressão de relógio ![ ](../media/add-expression-icon.msft.png) \).  
*   Para atualizar os valores de todas as expressões existentes, selecione o botão **Atualizar** \( ![ Atualizar ](../media/refresh-icon.msft.png) \)  Os valores são atualizados automaticamente ao passar pelo código.  
*   Para excluir uma expressão de relógio, clique com o botão direito do mouse na expressão e selecione Excluir expressão de **relógio** \( ![ Excluir expressão de relógio ](../media/delete-expression-icon.msft.png) \).  

## <a name="view-the-call-stack"></a>Exibir a pilha de chamada  

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

Para copiar a pilha de chamada atual para **** a área de transferência, passe o mouse em qualquer lugar no painel Pilha de Chamada, abra o menu contextual \(clique com o botão direito do mouse\) e escolha Copiar rastreamento **de**pilha .  

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

Por exemplo, no trecho de código a seguir, a linha `A` usa , que é uma biblioteca de `lib` terceiros.  Se você estiver confiante de que o problema que você está depurando não está relacionado a essa biblioteca de terceiros, então faz sentido marcar o script como código **biblioteca**.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Marcar um script como código biblioteca do painel Editor  

Para marcar um script como **código biblioteca** do **painel Editor:**  

1.  Abra o arquivo.  
1.  Passe o mouse em qualquer lugar e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Adicionar script para ignorar lista** (anteriormente mostrado como Marca como código da **biblioteca**).  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Marcar um script como **código biblioteca** do **painel Editor**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Marcar um script como código biblioteca do painel Pilha de Chamada  

Para marcar um script como **código biblioteca do** painel Pilha **de** Chamada:  

1.  Passe o mouse em uma função do script e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Adicionar script para ignorar lista** (anteriormente mostrado como Marca como código da **biblioteca**).  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar um script como código biblioteca do painel Pilha de Chamada" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Marcar um script como **código biblioteca do** painel Pilha **de** Chamada  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Marcar um script como código de biblioteca a partir de Configurações  

Para marcar um único script ou padrão de scripts de **Configurações**:  

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

Consulte [Executar trechos de código javascript em qualquer página da Web][DevToolsJavascriptSnippets].  

## <a name="see-also"></a>Ver também  

*   [Introdução à depuração de JavaScript no Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - Um tutorial simples e curto usando código existente, com capturas de tela.
*   [Visão geral da][DevToolsSourcesIndex] ferramenta Sources - A **ferramenta Sources** inclui o depurador e editor javaScript.
*   [Desabilitar JavaScript com o Microsoft Edge DevTools][DevToolsJavascriptDisable].

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Desabilitar JavaScript com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Execute trechos de código do JavaScript em qualquer página com o Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
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
