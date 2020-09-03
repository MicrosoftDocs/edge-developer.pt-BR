---
description: Saiba como usar o Microsoft Edge DevTools para localizar e corrigir erros de JavaScript.
title: Introdução à depuração de JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f8846388f92ba330940b4b6842964d96d9bbce4d
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993391"
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







# Introdução à depuração de JavaScript no Microsoft Edge DevTools   



Este tutorial ensina o fluxo de trabalho básico para a depuração de qualquer problema de JavaScript no DevTools.  

## Etapa 1: reproduzir o bug   

Encontrar uma série de ações que reproduzem um bug consistentemente é sempre a primeira etapa da depuração.  

1.  Clique em **abrir demonstração**.  Segure `Control` \ (Windows \) ou `Command` \ (MacOS \) e abra a demonstração em uma nova guia.  
    
    [Abrir demonstração][OpenDebugJSDemo]  
    
1.  Digite `5` na caixa de texto **número 1** .  
1.  Digite `1` na caixa de texto **número 2** .  
1.  Clique em **Adicionar número 1 e número 2**.  A etiqueta abaixo do botão diz `5 + 1 = 51` .  O resultado deve ser `6` .  Esse é o bug que você vai corrigir.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="O resultado de 5 + 1 é 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       O resultado de `5 + 1` é `51` , mas deve ser `6`  
    :::image-end:::  
    
## Etapa 2: Familiarize-se com a interface do usuário do painel fontes   

O DevTools oferece muitas ferramentas diferentes para tarefas diferentes, como a alteração de CSS, o profiling do desempenho da carga da página e o monitoramento de solicitações de rede.  O painel **fontes** é onde você depura o JavaScript.  

1.  Para abrir o devtools, pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).  Esse atalho abre o painel do **console** .  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Painel do console" lightbox="../media/javascript-console-empty.msft.png":::
       Painel do **console**  
    :::image-end:::  
    
1.  Clique na guia **fontes** .  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="O painel fontes" lightbox="../media/javascript-sources-sections.msft.png":::
       O painel **fontes**  
    :::image-end:::  
    
A interface do usuário do painel **fontes** tem 3 partes.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário do painel fontes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   As 3 partes da interface do usuário do painel **fontes**  
:::image-end:::  

1.  O painel do **navegador de arquivos** \ (seção 1 na figura anterior \).  Cada arquivo que as solicitações de página está listado aqui.  
1.  O painel **Editor de código** \ (seção 2 na figura anterior \).  Depois de selecionar um arquivo no painel do **navegador de arquivos** , o conteúdo desse arquivo é exibido aqui.  
1.  O painel de **depuração JavaScript** \ (seção 3 na figura anterior \).  Várias ferramentas para inspecionar o JavaScript para a página.  Se a janela do DevTools for ampla, esse painel será exibido à direita do painel do **Editor de código** .  
    
## Etapa 3: pausar o código com um ponto de interrupção   

Um método comum para depurar um problema como este é inserir muitas `console.log()` instruções no código, para inspecionar valores conforme o script é executado.  Por exemplo:  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

O `console.log()` método pode executar o trabalho, mas os **pontos de interrupção** são capazes de fazer uma realização mais rápida.  Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.  Os pontos de interrupção têm algumas vantagens sobre o `console.log()` método:  

*   Com o `console.log()` , você precisa abrir manualmente o código-fonte, encontrar o código relevante, inserir as `console.log()` instruções e, em seguida, recarregar a página para ver as mensagens no console.  Com pontos de interrupção, você pode pausar no código relevante sem mesmo saber como o código está estruturado.  
*   Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que você deseja inspecionar.  Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.  Às vezes, há variáveis que afetam seu código que você ainda não conhece.  

Em resumo, os pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rápido do que o `console.log()` método.  

Se você retomar uma etapa e pensar sobre como o aplicativo funciona, você poderá fazer uma estimativa de que a soma incorreta ( `5 + 1 = 51` ) é calculada no `click` ouvinte de eventos associado ao botão **Adicionar número 1 e número 2** .  Portanto, você provavelmente desejará pausar o código no momento em que o `click` ouvinte for executado.  Os **pontos de interrupção do ouvinte de eventos** permitem que você faça exatamente isso:  

1.  No painel **depuração de JavaScript** , clique em **pontos de interrupção de ouvinte de eventos** para expandir a seção.  O DevTools revela uma lista de categorias de eventos expansíveis, como **animação** e **área de transferência**.  
1.  Ao lado da categoria de evento **do mouse** , clique em **expandir** \ ( ![ expandir ícone ][ImageExpandIcon] \).  O DevTools revela uma lista de eventos de mouse, como **clique** e **MouseDown**.  Cada evento tem uma caixa de seleção ao lado dele.  
1.  Marque a caixa de seleção **clique** .  O DevTools agora está configurado para pausar automaticamente quando *um* `click` ouvinte de evento é executado.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="A caixa de seleção clicar está habilitada" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       A caixa de seleção **clicar** está habilitada  
    :::image-end:::  
    
1.  De volta à demonstração, clique em **Adicionar número 1 e número 2** novamente.  DevTools pausará a demonstração e realçará uma linha de código no painel **fontes** .  DevTools deve pausar na linha 16 `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Se você pausar em uma linha de código diferente, pressione **retomar a execução do script** \ ( ![ retome a execução ][ImageResumeIcon] do script \) até que você pause na linha correta.  
    
    > [!NOTE]
    > Se você pausar em uma linha diferente, você tem uma extensão de navegador que registra um `click` ouvinte de eventos em cada página que você visita.  Você foi pausado no `click` ouvinte da extensão.  Se você usar o modo InPrivate para **navegar em particular**, o que desabilita todas as extensões, poderá ver que você pausará na linha de código desejada a cada vez.  

<!--todo: add inprivate section when available -->  

Os **pontos de interrupção do ouvinte de eventos** são apenas um dos muitos tipos de pontos de interrupção disponíveis no devtools.  Vale a pena memorizar todos os diferentes tipos, porque cada tipo acaba ajudando a depurar diferentes cenários o mais rápido possível.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Etapa 4: percorrer o código   

Uma causa comum de erros é quando um script é executado na ordem errada.  Percorrer o código permite percorrer o tempo de execução do seu código, uma linha por vez e descobrir exatamente onde ele está sendo executado em uma ordem diferente do esperado.  Experimente agora:  

1.  Clique em **passar sobre a próxima chamada de função** \ ( ![ passo pela próxima chamada de função ][ImageOverIcon] \).  O DevTools executa o código a seguir sem passar a ele.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools ignora algumas linhas de código.  Isso ocorre porque é `inputsAreEmpty()` avaliado como falso; portanto, o bloco de código da `if` instrução não é executado.  
    
1.  No painel **fontes** do devtools, clique em **passar para a próxima chamada de função** \ ( ![ passar para a próxima chamada ][ImageIntoIcon] de função \) para percorrer o tempo de execução da `updateLabel()` função, uma linha por vez.  
    
Essa é a ideia básica de percorrer o código.  Se você examinar o código em `get-started.js` , verá que o bug está provavelmente em algum lugar na `updateLabel()` função.  Em vez de percorrer cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo ao local provável do bug.  

## Etapa 5: definir um ponto de interrupção de linha do código   

Os pontos de interrupção de linha de código são o tipo mais comum de ponto de interrupção.  Quando você obtém a linha específica de código em que deseja pausar, use um ponto de interrupção de linha de código:  

1.  Examine a última linha de código em `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  À esquerda do código, você vê o número da linha dessa linha em particular de código, que é **33**.  Clique em **33**.  DevTools coloca um ícone vermelho à esquerda do **33**.  Isso significa que há um ponto de interrupção de linha de código nesta linha.  O DevTools agora sempre pausa antes da execução desta linha de código.  
1.  Clique em **retomar execução do script** \ ( ![ continuar execução do script ][ImageResumeIcon] \).  O script continuará em execução até chegar à linha 33.  Nas linhas 30, 31 e 32, DevTools imprime os valores de `addend1` , `addend2` e `sum` à direita do ponto-e-vírgula em cada linha.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa no ponto de interrupção de linha do código na linha 32" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       O DevTools pausa no ponto de interrupção de linha do código na linha 32  
    :::image-end:::  
    
## Etapa 6: verificar valores de variáveis   

Os valores de `addend1` , `addend2` e `sum` parecem suspeitos.  Elas são quebradas entre aspas, o que significa que elas são cadeias de caracteres.  Trata-se de uma boa hipótese para explicar a causa do bug.  Agora é hora de obter mais informações.  O DevTools fornece muitas ferramentas para examinar valores variáveis.  

### Método 1: o painel escopo   

Quando você pausa em uma linha de código, o painel **escopo** mostra quais variáveis locais e globais estão definidas no momento, juntamente com o valor de cada variável.  Ele também mostra as variáveis de fechamento, quando aplicável.  Clique duas vezes em um valor de variável para editá-lo.  Quando você não estiver pausado em uma linha de código, o painel **escopo** estará vazio.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   O painel **escopo**  
:::image-end:::  

### Método 2: expressões de inspeção   

A guia **inspecionar expressões** permite monitorar os valores de variáveis ao longo do tempo.  Como o nome indica, as expressões de inspeção não são apenas limitadas a variáveis.  Você pode armazenar qualquer expressão JavaScript válida em uma expressão de inspeção.  Experimente agora:  

1.  Clique na guia **assistir** .  
1.  Clique em **Adicionar expressão** \ ( ![ Adicionar expressão ][ImageAddIcon] \).  
1.  Digite `typeof sum`.  
1.  Pressione `Enter` .  DevTools mostra `typeof sum: "string"` .  O valor à direita dos dois pontos é o resultado da sua expressão de inspeção.  
    
> [!NOTE]
> No painel da expressão de inspeção \ (inferior-direita \) na figura a seguir, a `typeof sum` expressão de inspeção é exibida.  Se a janela do DevTools for grande, o painel da expressão de inspeção estará no lado direito acima do painel **pontos de interrupção do ouvinte de eventos** .  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel da expressão de inspeção" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   O painel da **expressão de inspeção**  
:::image-end:::  

Como suspeito, `sum` está sendo avaliado como uma cadeia de caracteres quando deve ser um número.  Agora você confirmou que essa é a causa do bug.  

### Método 3: o console   

Além de exibir `console.log()` mensagens, você também pode usar o console para avaliar instruções JavaScript arbitrárias.  Em termos de depuração, você pode usar o console para testar possíveis correções de bugs.  Experimente agora:  

1.  Se você não tiver a gaveta do console aberta, pressione `Escape` para abri-la.  Ele é aberto na parte inferior da janela do DevTools.  
1.  No console, digite `parseInt(addend1) + parseInt(addend2)` .  Essa instrução funciona porque você está pausado em uma linha de código onde `addend1` e `addend2` está em escopo.  
1.  Pressione `Enter` .  O DevTools avalia a instrução e imprime `6` , que é o resultado que você espera que a demonstração produza.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A gaveta do console, depois de avaliar parseInt (addend1) + parseInt (addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       A gaveta do **console** , após a avaliação `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Etapa 7: aplicar uma correção   

Se você encontrar uma correção para o bug, experimente sua correção editando o código e executando a demonstração novamente.  Você não precisa sair do DevTools para aplicar a correção.  Você pode editar o código JavaScript diretamente na interface do usuário do DevTools.  Experimente agora:  

1.  Clique em **retomar execução do script** \ ( ![ continuar execução do script ][ImageResumeIcon] \).  
1.  No **Editor de código**, substitua line 32, `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.  
1.  Clique em **desativar pontos de interrupção** \ ( ![ desativar pontos de interrupção ][ImageDeactivateIcon] \).  Ele muda de azul para indicar que está ativo.  Enquanto isso é definido, DevTools ignora os pontos de interrupção que você definiu.  
1.  Experimente a demonstração com valores diferentes.  A demonstração agora é calculada corretamente.  
    
> [!CAUTION]
> Este fluxo de trabalho aplica-se apenas a uma correção do código que está sendo executado no navegador.  Ele não corrige o código para todos os usuários que acessam sua página.  Para fazer isso, você precisa corrigir o código que está em seus servidores.  

## Próximas etapas   

Parabéns!  Agora você sabe como aproveitar ao máximo o Microsoft Edge DevTools ao Depurar JavaScript.  As ferramentas e os métodos aprendidos neste tutorial podem economizar inúmeras horas.  

Este tutorial mostrou apenas duas maneiras de definir pontos de interrupção.  O DevTools oferece muitas outras maneiras, incluindo as configurações a seguir.  

*   Pontos de interrupção condicionais que são disparados quando a condição que você fornece é verdadeira.  
*   Pontos de interrupção em exceções detectadas ou não capturadas.  
*   XHR pontos de interrupção que são disparados quando a URL solicitada correspondem a uma Subcadeia fornecida.  
    
Para obter mais informações sobre quando e como usar cada tipo, vá para [pausar o código com pontos de interrupção][DevtoolsJavscriptBreakpoints].  

Há alguns controles de revisão de código que não foram explicados neste tutorial.  Para obter mais informações, vá para a [linha passo a passo de código][DevtoolsJavascriptReferenceStepThroughCode].  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Depurar o código-referência de depuração de JavaScript | Documentos da Microsoft"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abrir demonstração | Problema"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
