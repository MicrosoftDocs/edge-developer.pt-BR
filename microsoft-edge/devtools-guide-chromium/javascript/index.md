---
description: Saiba como usar o Microsoft Edge DevTools para encontrar e corrigir bugs do JavaScript.
title: Começar a depurar JavaScript no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325942"
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
# Começar a depurar JavaScript no Microsoft Edge DevTools  

Este artigo ensina o fluxo de trabalho básico para depurar qualquer problema do JavaScript no DevTools.  

## Etapa 1: Reproduzir o bug  

Encontrar uma série de ações que reproduzem consistentemente um bug é sempre a primeira etapa para a depuração.  

1.  Escolha **Abrir Demonstração.**  Segure `Control` \(Windows, Linux\) ou `Command` \(macOS\) e abra a demonstração em uma nova guia do navegador.  
    
    [Open Demo][OpenDebugJSDemo]  
    
1.  Digite `5` a caixa de texto Número **1.**  
1.  Digite `1` a caixa de texto Número **2.**  
1.  Escolha **Adicionar Número 1 e Número 2.**  O rótulo abaixo do botão diz `5 + 1 = 51` .  O resultado deve ser `6` .  Em seguida, corrige o erro de adição que é o bug.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 resulta em 51, mas deve ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` resultados `51` em, mas deve ser `6`  
    :::image-end:::  
    
## Etapa 2: familiarizar-se com a interface do usuário do painel fontes  

O DevTools fornece várias ferramentas diferentes para tarefas diferentes.  Tarefas diferentes incluem alterar CSS, criação de perfil de desempenho de carga de página e monitoramento de solicitações de rede.  O **painel Fontes** é onde você depura JavaScript.  

1.  Abra o DevTools `Control` + `Shift` + `J` pressionando \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\).  Esse atalho abre o **painel do** Console.  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="O painel do Console" lightbox="../media/javascript-console-empty.msft.png":::
       A **ferramenta Console**  
    :::image-end:::  
    
1.  Escolha a **ferramenta** Fontes.  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="O painel Fontes" lightbox="../media/javascript-sources-sections.msft.png":::
       O **painel Fontes**  
    :::image-end:::  
    
A **interface do** usuário do painel Fontes tem três partes.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="As 3 partes da interface do usuário do painel Fontes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   As 3 partes da interface **do usuário do painel** Fontes  
:::image-end:::  

1.  O **painel Navegador** de Arquivos \(Seção 1 na figura anterior\).  Todos os arquivos que a página da Web solicita estão listados aqui.  
1.  O **painel Editor** de Código \(Seção 2 na figura anterior\).  Depois de selecionar um arquivo no painel **Navegador** de Arquivos, o conteúdo desse arquivo será exibido aqui.  
1.  O **painel Depuração** de JavaScript \(Seção 3 na figura anterior\).  Várias ferramentas para inspecionar o JavaScript para a página da Web.  Se a janela DevTools for larga, esse painel será exibido à direita do painel **Editor de** Código.  
    
## Etapa 3: Pausar o código com um ponto de interrupção  

Um método comum para depurar esse tipo de problema é inserir várias instruções no código e inspecionar valores à medida que `console.log()` o script é executado.  Por exemplo:  

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

O método pode fazer o trabalho, mas pontos de interrupção `console.log()` o fazer mais rapidamente. ****  Um ponto de interrupção permite pausar seu código no meio do tempo de execução e examinar todos os valores nesse momento.  Pontos de interrupção têm algumas vantagens em relação ao `console.log()` método:  

*   With `console.log()` , you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.  Com pontos de interrupção, você pode pausar o código relevante sem saber como o código está estruturado.  
*   Em suas `console.log()` instruções, você precisa especificar explicitamente cada valor que deseja inspecionar.  Com pontos de interrupção, o DevTools mostra os valores de todas as variáveis nesse momento.  Às vezes, as variáveis que afetam seu código são ocultas e ofuscados.  
    
Em resumo, pontos de interrupção podem ajudá-lo a encontrar e corrigir bugs mais rapidamente do que o `console.log()` método.  

Se voltar e pensar em como o aplicativo funciona, você pode fazer uma suposição instrucionada de que a soma incorreta \( \) é calculada no ouvinte de eventos associado ao botão Adicionar Número 1 e Número `5 + 1 = 51` `click` **2.**  Portanto, você provavelmente deseja pausar o código no horário em que o `click` ouvinte é executado.  **Os Pontos de Interrupção do Ouvinte de** Eventos permitem que você faça exatamente isso:  

1.  No painel **Depuração de JavaScript,** escolha Pontos de Interrupção do Ouvinte **de** Eventos para expandir a seção.  O DevTools revela uma lista de categorias de eventos expansíveis, como **Animação e** **Área de Transferência.**  
1.  Ao lado da categoria de evento **Mouse,** escolha **Expandir** \( ![ ícone Expandir ][ImageExpandIcon] \).  O DevTools revela uma lista de eventos do mouse, como **clique** e **mouse para baixo.**  Cada evento tem uma caixa de seleção ao lado dele.  
1.  Escolha a caixa de seleção ao lado de **clicar.**  O DevTools agora está definido para pausar automaticamente quando qualquer `click` ouvinte de eventos for executado.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Escolha a caixa de seleção ao lado de clicar" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Escolha a caixa de seleção ao lado de **clicar**  
    :::image-end:::  
    
1.  Novamente na demonstração, escolha **Adicionar Número 1 e Número 2** novamente.  O DevTools pausa a demonstração e realça uma linha de código no **painel** Fontes.  DevTools deve pausar na linha 16 em `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Se você pausar em uma linha de código diferente, pressione **Resume Script Execution** \( Resume Script Execution ![ ][ImageResumeIcon] \) até pausar na linha correta.  
    
    > [!NOTE]
    > Se você tiver pausado em uma linha diferente, terá uma extensão de navegador que registra um ouvinte de eventos em cada página `click` da Web visitada.  Você foi pausado no `click` ouvinte da extensão.  Se você usar o Modo **** InPrivate para navegar em particular, o que desabilita todas as extensões, você poderá ver que pausa na linha de código desejada sempre.  

<!--todo: add inprivate section when available -->  

**Os Pontos de Interrupção do** Ouvinte de Eventos são apenas um dos vários tipos de pontos de interrupção disponíveis no DevTools.  Memorize todos os tipos diferentes para ajudá-lo a depurar cenários diferentes o mais rápido possível.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Etapa 4: Passar pelo código  

Uma causa comum de bugs é quando um script é executado na ordem errada.  Passar pelo código permite que você ande pelo tempo de execução do seu código.  Você passa por uma linha por vez para ajudá-lo a descobrir exatamente onde seu código está sendo executado em uma ordem diferente do esperado.  Experimente agora:  

1.  Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).  O DevTools executa o código a seguir sem entrar nele.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > O DevTools ignora algumas linhas de código.  Isso porque é `inputsAreEmpty()` avaliada como false, portanto, o bloco de código para a `if` instrução não é executado.  
    
1.  No painel **Fontes** do DevTools, escolha Step **into next function call** \( Step into next function call \) para passar pelo tempo de execução da função, uma linha ![ por ][ImageIntoIcon] `updateLabel()` vez.  
    
Revisar uma linha por vez é a ideia básica de passar pelo código.  Se você olhar para o `get-started.js` código, verá que o bug provavelmente está em algum lugar na `updateLabel()` função.  Em vez de passar por cada linha de código, você pode usar outro tipo de ponto de interrupção para pausar o código mais próximo da localização provável do bug.  

## Etapa 5: Definir um ponto de interrupção de linha de código  

Os pontos de interrupção de linha de código são o tipo mais comum de ponto de interrupção.  Quando você chegar à linha de código específica que deseja pausar, use um ponto de interrupção de linha de código.  

1.  Veja a última linha de código `updateLabel()` em:  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  À esquerda, o número dessa linha específica de código é exibido como **34**.  Escolha a **linha 34.**  O DevTools coloca um ícone vermelho à esquerda de **34**.  O ícone vermelho indica que um ponto de interrupção de linha de código está nessa linha.  O DevTools sempre pausa antes que essa linha de código seja executado.  
1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  O script continua em execução até atingir a linha 33.  Nas linhas 31, 32 e 33, o DevTools imprime os valores de , e à direita dos pontos e vírgulas em `addend1` `addend2` cada `sum` linha.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="O DevTools pausa no ponto de interrupção de linha de código na linha 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       O DevTools pausa no ponto de interrupção de linha de código na linha 34  
    :::image-end:::  
    
## Etapa 6: Verificar valores variáveis  

Os valores `addend1` de , e parecem `addend2` `sum` suspeitos.  Os valores são entre aspas.  As aspas significam que o valor é uma cadeia de caracteres, o que é uma boa hipótese para explicar a causa do bug.  Reúna mais informações sobre a situação.  O DevTools fornece muitas ferramentas para examinar valores variáveis.  

### Método 1: O painel Escopo  

Se você pausar em uma **** linha de código, o painel Escopo exibirá as variáveis locais e globais definidas no momento, juntamente com o valor de cada variável.  Ele também exibe variáveis de fechamento, conforme aplicável.  Clique duas vezes em um valor variável para editá-lo.  Se você não pausar em uma linha de código, **o** painel Escopo será vazio.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="O painel Escopo" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   O **painel** Escopo  
:::image-end:::  

### Método 2: Expressões de relógio  

O **painel Expressões** de Relógio permite monitorar os valores das variáveis ao longo do tempo.  Como o nome sugere, **as expressões de relógio** não são limitadas a variáveis.  Você pode armazenar qualquer expressão JavaScript válida em uma **expressão de relógio.**  Experimente agora.  

1.  Escolha o **painel** de relógio.  
1.  Escolha **Adicionar expressão** \( Adicionar expressão ![ ][ImageAddIcon] \).  
1.  Digite `typeof sum`.  
1.  Selecione `Enter` .  O DevTools mostra `typeof sum: "string"` .  O valor à direita dos dois-pontos é o resultado de sua expressão de relógio.  
    
> [!NOTE]
> No painel **expressão** de relógio \(inferior direito\) na figura a seguir, a expressão `typeof sum` de relógio é exibida.  Se a janela DevTools for grande, o painel **DevTools** fica à direita acima do painel Pontos de Interrupção do Ouvinte **de** Eventos.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="O painel Expressão de Relógio" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   O **painel Expressão** de Relógio  
:::image-end:::  

Como suspeito, `sum` está sendo avaliado como uma cadeia de caracteres, quando deve ser um número.  Você agora confirma que o tipo de valor é a causa do bug.  

### Método 3: O console  

O **Console** permite exibir mensagens e você também pode usá-lo para avaliar `console.log()` instruções JavaScript arbitrárias.  Para depuração, você pode usar o **Console** para testar possíveis correções de bugs.  Experimente agora.  

1.  Se a **gaveta do Console** estiver fechada, selecione para `Escape` abri-la.  A **gaveta console** é aberta no painel inferior da janela DevTools.  
1.  No **Console,** digite `parseInt(addend1) + parseInt(addend2)` .  A instrução em que a ferramenta está pausada em uma linha de código onde `addend1` `addend2` está no escopo.  
1.  Selecione `Enter` .  DevTools avalia a instrução e imprime `6` , que é o resultado que você espera que a demonstração produza.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="A gaveta console, depois de avaliar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       A **gaveta console,** depois de avaliar `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Etapa 7: Aplicar uma correção  

Se você encontrar uma correção para o bug, experimente a correção editando o código e reruindo a demonstração.  Você pode editar o código JavaScript diretamente na interface do usuário do DevTools e aplicar a correção.  Experimente agora.  

1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  
1.  No **Editor de Código,** substitua a linha 32, `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Selecione `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) para salvar a alteração.  
1.  Choose **Deactivate breakpoints** \( ![ Deactivate breakpoints ][ImageDeactivateIcon] \).  Ele muda azul para indicar que a opção está ativa.  Enquanto **desativa pontos de interrupção definidos,** o DevTools ignora todos os pontos de interrupção que você definir.  
1.  Experimente a demonstração com valores diferentes.  A demonstração agora calcula corretamente.  
    
> [!CAUTION]
> Esse fluxo de trabalho aplica apenas uma correção ao código que está sendo executado no navegador.  Ele não corrige o código para todos os usuários que visitam sua página da Web.  Para fazer isso, você precisa corrigir o código que está em seus servidores.  

## Próximas etapas  

Parabéns!  Agora você sabe como fazer o máximo do Microsoft Edge DevTools ao depurar JavaScript.  As ferramentas e os métodos que você aprendeu neste artigo podem poupar-lhe inúmeras horas.  

Este artigo ensinava apenas duas maneiras de definir pontos de interrupção.  O DevTools oferece muitas outras maneiras, incluindo as configurações a seguir.  

*   Pontos de interrupção condicionais que só são disparados quando a condição que você fornece é verdadeira.  
*   Pontos de interrupção em exceções capturadas ou não capturadas.  
*   Pontos de interrupção XHR que são disparados quando a URL solicitada corresponde a uma substring que você fornece.  
    
Para obter mais informações sobre quando e como usar cada tipo, navegue até [Pausar seu código com pontos de interrupção.][DevtoolsJavscriptBreakpoints]  

Alguns controles de passo a passo de código não são explicados neste artigo.  Para obter mais informações, [navegue até a linha de código Step over.][DevtoolsJavascriptReferenceStepThroughCode]  

## Entrar em contato com a equipe Microsoft Edge DevTools  

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

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abrir demonstração | Falha"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Meio\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
