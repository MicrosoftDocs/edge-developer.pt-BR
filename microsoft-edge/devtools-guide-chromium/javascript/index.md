---
description: Saiba como usar o Microsoft Edge DevTools para encontrar e corrigir bugs javaScript.
title: Começar a depurar JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e146c6708f097b1ea8dc82f08be58f5aa5e52d1f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398438"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a>Começar a depurar JavaScript no Microsoft Edge DevTools  

Este artigo ensina o fluxo de trabalho básico para depurar qualquer problema javascript no DevTools.  

## <a name="step-1-reproduce-the-bug"></a>Etapa 1: Reproduzir o bug  

Encontrar uma série de ações que reproduzam consistentemente um bug é sempre a primeira etapa para a depuração.  

1.  Escolha **Abrir Demonstração**.  Segure `Control` \(Windows, Linux\) `Command` ou \(macOS\) e abra a demonstração em uma nova guia do navegador.  
    
    [Abrir Demonstração][OpenDebugJSDemo]  
    
1.  Insira `5` na caixa de texto Número **1.**  
1.  Insira `1` na caixa de texto Número **2.**  
1.  Escolha **Adicionar Número 1 e Número 2**.  O rótulo abaixo do botão diz `5 + 1 = 51` .  O resultado deve ser `6` .  Em seguida, corrige o erro de adição que é o bug.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 resulta em 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` resulta `51` em , mas deve ser `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a>Etapa 2: Familiarizar-se com a interface do usuário da ferramenta Sources  

O DevTools fornece muitas ferramentas diferentes para tarefas diferentes.  Tarefas diferentes incluem alterar CSS, perfil de desempenho de carga de página e monitoramento de solicitações de rede.  A **ferramenta Sources** é onde você depura JavaScript.  

1.  Para abrir a **ferramenta Console** no DevTools, selecione `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="A ferramenta Console" lightbox="../media/javascript-console-empty.msft.png":::
       A **ferramenta Console**  
    :::image-end:::  
    
1.  Escolha a **ferramenta Fontes.**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="A ferramenta Sources" lightbox="../media/javascript-sources-sections.msft.png":::
       A **ferramenta Sources**  
    :::image-end:::  
    
A **interface do usuário** da ferramenta Sources tem três partes.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário da ferramenta Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   As 3 partes da interface do **usuário da ferramenta Sources**  
:::image-end:::  

1.  O **painel Navegador** de Arquivos \(Seção 1 na figura anterior\).  Todos os arquivos que a página da Web solicita estão listados aqui.  
1.  O **painel Editor de** Código \(Seção 2 na figura anterior\).  Depois de selecionar um arquivo no painel **Navegador** de Arquivos, o conteúdo desse arquivo será exibido aqui.  
1.  O **painel Depuração** de JavaScript \(Seção 3 na figura anterior\).  Várias ferramentas para inspecionar o JavaScript para a página da Web.  Se sua janela DevTools for ampla, esse painel será exibido à direita do painel **Editor de** Código.  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a>Etapa 3: Pausar o código com um ponto de interrupção  

Um método comum para depurar esse tipo de problema é inserir várias instruções no código e inspecionar valores conforme `console.log()` o script é executado.  Por exemplo:  

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

O `console.log()` método pode fazer o trabalho, mas os pontos de **interrupção** o aceleram.  Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.  Os pontos de interrupção têm as seguintes vantagens sobre o `console.log()` método.  

*   Com , você precisa abrir manualmente o código-fonte, encontrar o código relevante, inserir as instruções e atualizar a página da Web para exibir as mensagens `console.log()` `console.log()` no **Console**.  Com pontos de interrupção, você pode pausar o código relevante sem saber como o código é estruturado.  
*   Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que deseja inspecionar.  Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.  Às vezes, as variáveis que afetam seu código são ocultas e ofuscados.  
    
Em resumo, pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rapidamente do que o `console.log()` método.  

Se você voltar e pensar em como o aplicativo funciona, você pode fazer uma suposição educada de que a soma incorreta \( \) é calculada no ouvinte de eventos associado ao botão Adicionar Número 1 e Número `5 + 1 = 51` `click` **2.**  Portanto, você provavelmente deseja pausar o código na hora em que o `click` ouvinte é executado.  **Os Pontos de Interrupção do** Ouvinte de Eventos permitem que você faça exatamente isso:  

1.  No painel **Depuração de JavaScript,** escolha Pontos de Interrupção do Ouvinte **de** Eventos para expandir a seção.  O DevTools revela uma lista de categorias de eventos expansíveis, como **Animação** e **Área de Transferência.**  
1.  Ao lado da categoria de evento **Mouse,** escolha **Expandir** \( ![ Expand icon ][ImageExpandIcon] \).  O DevTools revela uma lista de eventos do mouse, como **clique** e **mouse para baixo.**  Cada evento tem uma caixa de seleção ao lado dele.  
1.  Escolha a caixa de seleção ao lado de **clicar em**.  O DevTools agora está definido para pausar automaticamente quando qualquer `click` ouvinte de eventos for executado.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Escolha a caixa de seleção ao lado de clicar" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Escolha a caixa de seleção ao lado de **clicar**  
    :::image-end:::  
    
1.  De volta à demonstração, escolha **Adicionar Número 1 e Número 2** novamente.  O DevTools pausa a demonstração e realça uma linha de código na **ferramenta Sources.**  DevTools deve pausar na linha 16 em `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Se você pausar em uma linha de código diferente, escolha Retomar Execução de **Script** \( Retomar Execução de Script \) até pausar ![ na linha ][ImageResumeIcon] correta.  
    
    > [!NOTE]
    > Se você fez uma pausa em uma linha diferente, você tem uma extensão do navegador que registra um ouvinte de eventos em cada página da `click` Web que você visitar.  Você é pausado no `click` ouvinte da extensão.  Se você usar o Modo InPrivate para navegar em particular **,** o que desabilita todas as extensões, você pode ver que você pausa na linha de código desejada sempre.  

<!--todo: add inprivate section when available -->  

**Os Pontos de Interrupção do** Ouvinte de Eventos são apenas um dos vários tipos de pontos de interrupção disponíveis no DevTools.  Memorize todos os tipos diferentes para ajudá-lo a depurar cenários diferentes o mais rápido possível.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a>Etapa 4: Passar pelo código  

Uma causa comum de bugs é quando um script é executado na ordem errada.  Passar pelo código permite que você ande pelo tempo de execução do código.  Você passa por uma linha de cada vez para ajudá-lo a descobrir exatamente onde seu código está sendo executado em uma ordem diferente do esperado.  Experimente agora:  

1.  Escolha **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).  O DevTools executa o código a seguir sem entrar nele.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > O DevTools ignora algumas linhas de código.  Isso acontece porque `inputsAreEmpty()` é avaliada como false, para que o bloco de código da `if` instrução não seja executado.  
    
1.  Na ferramenta **Sources** do DevTools, escolha Etapa na próxima chamada de função **\(** Passo a passo na próxima chamada de função \) para passar pelo tempo de execução da função, uma linha por ![ ][ImageIntoIcon] `updateLabel()` vez.  
    
Revisar uma linha de cada vez é a ideia básica de passar pelo código.  Se você revisar o código em `get-started.js` , o bug provavelmente está em algum lugar na `updateLabel()` função.  Em vez de passar por cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo do local provável do bug.  

## <a name="step-5-set-a-line-of-code-breakpoint"></a>Etapa 5: Definir um ponto de interrupção de linha de código  

Pontos de interrupção de linha de código são o tipo de ponto de interrupção mais comum.  Quando você chegar à linha de código específica que deseja pausar, use um ponto de interrupção de linha de código.  

1.  Veja a última linha de código em `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  À esquerda, o número dessa linha de código específica é exibido como **34**.  Escolha a **linha 34**.  DevTools exibe um ícone vermelho à esquerda de **34**.  O ícone vermelho indica que um ponto de interrupção de linha de código está nessa linha.  O DevTools sempre pausa antes que essa linha de código seja executado.  
1.  Escolha **Retomar execução de script** \( Retomar execução de script ![ ][ImageResumeIcon] \).  O script continua a ser executado até atingir a linha 33.  Nas linhas 31, 32 e 33, DevTools imprime os valores de , e à direita dos pontos e vírgulas em `addend1` `addend2` cada `sum` linha.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa o ponto de interrupção de linha de código na linha 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       O DevTools pausa o ponto de interrupção de linha de código na linha 34  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a>Etapa 6: Verificar valores de variável  

Os valores `addend1` de , e parecem `addend2` `sum` suspeitos.  Os valores são empacotados entre aspas.  As aspas significam que o valor é uma cadeia de caracteres, o que é uma boa hipótese para explicar a causa do bug.  Reúna mais informações sobre a situação.  O DevTools fornece muitas ferramentas para examinar valores variáveis.  

### <a name="method-1-the-scope-panel"></a>Método 1: o painel Escopo  

Se você pausar em uma linha de código, o painel **Escopo** exibirá as variáveis locais e globais que estão definidas no momento, juntamente com o valor de cada variável.  Ele também exibe variáveis de fechamento, conforme aplicável.  Clique duas vezes em um valor variável para editá-lo.  Se você não pausar em uma linha de código, o painel **Escopo** será vazio.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   O **painel Escopo**  
:::image-end:::  

### <a name="method-2-watch-expressions"></a>Método 2: Expressões de Assistir  

O **painel Expressões de** Assistir permite monitorar os valores das variáveis ao longo do tempo.  Como o nome sugere, **Expressões de** Relógio não estão limitadas a variáveis.  Você pode armazenar qualquer expressão JavaScript válida em uma **expressão watch**.  Experimente agora.  

1.  Escolha o **painel** Assistir.  
1.  Escolha **Adicionar Expressão** \( Adicionar Expressão ![ ][ImageAddIcon] \).  
1.  Digite `typeof sum`.  
1.  Selecione `Enter` .  DevTools mostra `typeof sum: "string"` .  O valor à direita dos dois pontos é o resultado da expressão do relógio.  
    
> [!NOTE]
> No painel **Expressão do** Relógio \(inferior à direita\) na figura a seguir, a Expressão do Relógio `typeof sum` é exibida.  Se sua janela DevTools for grande, o **painel** Expressão do Relógio fica à direita acima do painel Pontos de Interrupção do Ouvinte **de** Eventos.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel Expressão do Relógio" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   O **painel Expressão do** Relógio  
:::image-end:::  

Como suspeita, `sum` está sendo avaliado como uma cadeia de caracteres, quando deve ser um número.  O tipo de valor confirmado agora é a causa do bug.  

### <a name="method-3-the-console"></a>Método 3: o console  

O **Console** permite que você veja mensagens e você também pode `console.log()` usá-la para avaliar instruções JavaScript arbitrárias.  Para depuração, você pode usar o **Console** para testar possíveis correções para bugs.  Experimente agora.  

1.  Se a **ferramenta Console** estiver fechada, selecione `Escape` abri-la.  A **ferramenta Console** é aberta no painel inferior da janela DevTools.  
1.  No **Console,** digite `parseInt(addend1) + parseInt(addend2)` .  A instrução da ferramenta é pausada em uma linha de código onde `addend1` e `addend2` estão no escopo.  
1.  Selecione `Enter` .  DevTools avalia a instrução e as impressões , que `6` é o resultado que você espera que a demonstração produza.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A ferramenta Console, após avaliar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       A **ferramenta Console,** após a avaliação `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a>Etapa 7: Aplicar uma correção  

Se você encontrar uma correção para o bug, experimente a correção editando o código e rerurindo a demonstração.  Você pode editar o código JavaScript diretamente na interface do usuário do DevTools e aplicar a correção.  Experimente agora.  

1.  Escolha **Retomar execução de script** \( Retomar execução de script ![ ][ImageResumeIcon] \).  
1.  No Editor **de Código,** substitua a linha 32, `var sum = addend1 + addend2` , por `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar sua alteração.  
1.  Escolha **Desativar pontos de interrupção** \( Desativar pontos de ![ interrupção ][ImageDeactivateIcon] \).  Ele muda em azul para indicar que a opção está ativa.  Embora os pontos de interrupção de desativação **estão definidos,** o DevTools ignora todos os pontos de interrupção que você definir.  
1.  Experimente a demonstração com valores diferentes.  A demonstração agora calcula corretamente.  
    
> [!CAUTION]
> Esse fluxo de trabalho aplica apenas uma correção ao código que está sendo executado no navegador.  Ele não corrige o código para todos os usuários que visitam sua página da Web.  Para fazer isso, você precisa corrigir o código que está em seus servidores.  

## <a name="next-steps"></a>Próximas etapas  

Parabéns!  Agora você sabe como usar o Microsoft Edge DevTools ao depurar JavaScript.  As ferramentas e os métodos que você aprendeu neste artigo podem salvar inúmeras horas.  

Este artigo ensinava apenas duas maneiras de definir pontos de interrupção.  O DevTools oferece muitas outras maneiras, incluindo as configurações a seguir.  

*   Pontos de interrupção condicionais que são disparados somente quando a condição que você fornece é verdadeira.  
*   Pontos de interrupção em exceções capturadas ou não capturadas.  
*   Pontos de interrupção XHR disparados quando a URL solicitada corresponde a uma subdstring que você fornece.  
    
Para obter mais informações sobre quando e como usar cada tipo, navegue até [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].  

Alguns controles de revisão de código não são explicados neste artigo.  Para obter mais informações, navegue [até Passo sobre a linha de código][DevtoolsJavascriptReferenceStepThroughCode].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Código passo a passo - referência de depuração do JavaScript | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Open Demo | Glitch"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
