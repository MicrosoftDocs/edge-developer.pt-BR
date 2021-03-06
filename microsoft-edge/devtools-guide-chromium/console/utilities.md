---
description: Uma referência de comandos de conveniência disponíveis no Console do Microsoft Edge DevTools.
title: Referência da API de Utilitários de Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398823"
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

# <a name="console-utilities-api-reference"></a>Referência da API de Utilitários de Console  

A API de Utilitários de Console contém uma coleção de comandos de conveniência para executar tarefas comuns: selecionar e inspecionar elementos DOM, exibir dados em formato acessível, interromper e iniciar o profiler e monitorar eventos DOM.  

> [!WARNING]
> Os comandos a seguir só funcionam no Console do Microsoft Edge DevTools.  Os comandos não funcionarão se executados de seus scripts.  

Para os `console.log()` métodos e o restante dos `console.error()` `console.*` métodos, navegue até [Console API Reference][DevToolsConsoleApi].  

## <a name="recently-evaluated-expression"></a>Expressão avaliada recentemente  

```console
$_
```  

Retorna o valor da expressão avaliada mais recentemente.  

Na figura a seguir, uma expressão simples \( `2 + 2` \) é avaliada.  Em `$_` seguida, a propriedade é avaliada, que contém o mesmo valor.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ é a expressão avaliada mais recentemente" lightbox="../media/console-arithmatic.msft.png":::
   Figura 1:  `$_` é a expressão avaliada mais recentemente  
:::image-end:::  

Na figura a seguir, a expressão avaliada inicialmente contém uma matriz de nomes.  Avaliando para encontrar o comprimento da matriz, o valor armazenado em alterações para se tornar a expressão avaliada mais `$_.length` `$_` recente, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ muda quando novos comandos são avaliados" lightbox="../media/console-array-length.msft.png":::
   Figura 2:  `$_` alterações quando novos comandos são avaliados  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a>Elemento escolhido recentemente ou objeto JavaScript  

```console
$0
```  

Retorna o elemento selecionado mais recentemente ou o objeto JavaScript.  `$1` retorna o segundo selecionado mais recentemente e assim por diante.  Os comandos , , e funcionam como uma referência histórica aos últimos cinco elementos DOM inspecionados na ferramenta Elements ou os cinco últimos objetos de pilha JavaScript selecionados na `$0` `$1` ferramenta `$2` `$3` `$4` **Memória.** ****  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

Na figura a seguir, um `img` elemento é selecionado na ferramenta **Elements.**  Na gaveta **Console,** `$0` foi avaliado e exibe o mesmo elemento.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Os $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Figura 3: O `$0`  
:::image-end:::  

Na figura a seguir, a imagem mostra um elemento diferente selecionado na mesma página.  O `$0` agora se refere ao elemento recém-selecionado, enquanto retorna o elemento selecionado `$1` anteriormente.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="O $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Figura 4: O `$1`  
:::image-end:::  

## <a name="query-selector"></a>Seletor de consulta  

```console
$(selector, [startNode])
```  

Retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.  Este método é um alias para o [método document.querySelector().][MDNDocumentQuerySelector]  

Na figura a seguir, uma referência ao primeiro `<img>` elemento do documento é retornada.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   Figura 5: O `$('img')`  
:::image-end:::  

Passe o mouse no resultado retornado, abra o menu contextual \(clique com o botão **** direito do mouse\) e escolha **Revelar** no Painel de Elementos para encontrá-lo no DOM ou Role para Exibir para exibi-lo na página.  

Na figura a seguir, uma referência ao elemento selecionado no momento é retornada e a propriedade src é exibida.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Figura 6: O `$('img').src`  
:::image-end:::  

Esse método também dá suporte a um segundo parâmetro, startNode, que especifica um "elemento" ou Nó do qual procurar elementos.  O valor padrão do parâmetro é `document` .  

Na figura a seguir, o primeiro `img` elemento é encontrado depois que o e exibe `title--image` `src` corretamente é retornado.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Figura 7: O `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Se você estiver usando uma biblioteca como jQuery que usa , a funcionalidade será substituída e corresponderá à implementação `$` `$` dessa biblioteca.  

## <a name="query-selector-all"></a>Seletor de Consulta Todos  

```console
$$(selector, [startNode])
```  

Retorna uma matriz de elementos que corresponderão ao seletor CSS especificado.  Esse método equivale a executar o [método document.querySelectorAll().][MDNDocumentQuerySelectorAll]  

Na figura e exemplo de código a seguir, use para criar uma matriz de todos os elementos no documento atual e exibir o valor da propriedade `$$()` `<img>` para cada `src` elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usando $$() para selecionar todas as imagens no documento e exibir as fontes" lightbox="../media/console-element-selector-image-all.msft.png":::
   Figura 8: Usando `$$()` para selecionar todas as imagens no documento e exibir as fontes  
:::image-end:::  

Este método também dá suporte a um segundo parâmetro, startNode, que especifica um elemento ou Nó do qual procurar elementos.  O valor padrão do parâmetro é `document` .  

Na figura e amostra de código a seguir, uma versão modificada do exemplo de código anterior e a figura usam para criar uma matriz de todos os elementos que aparecem no documento atual após o `$$()` `<img>` Nó selecionado.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usando $$() para selecionar todas as imagens que aparecem após o elemento <div> no documento e exibir as fontes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Figura 9: Usando para selecionar todas as imagens que aparecem após `$$()` o elemento especificado no documento e exibir as `<div>` fontes  
:::image-end:::  

> [!NOTE]
> Selecione `Shift` + `Enter` no console para iniciar uma nova linha sem executar o script.  

## <a name="xpath"></a>XPath  

```console
$x(path, [startNode])
```  

Retorna uma matriz de elementos DOM que corresponderão à expressão XPath especificada.  

Na figura e amostra de código a seguir, todos os `<p>` elementos na página são retornados.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usando um seletor XPath" lightbox="../media/console-array-xpath.msft.png":::
   Figura 10: Usando um seletor XPath  
:::image-end:::  

Na figura e amostra de código a seguir, todos os `<p>` elementos que contêm `<a>` elementos são retornados.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usando um seletor XPath mais complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Figura 11: Usando um seletor XPath mais complicado  
:::image-end:::  

Semelhante aos outros comandos do seletor, tem um segundo parâmetro opcional, , que especifica um elemento ou Nó do qual `$x(path)` `startNode` procurar elementos.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usando um seletor XPath com startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Figura 12: Usando um seletor XPath com `startNode`  
:::image-end:::  

## <a name="clear"></a>clear  

```console
clear()
```  

Limpa o console do histórico.  

```console
clear()
```  

## <a name="copy"></a>copy  

```console
copy(object)
```  

O `copy(object)` método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.  

```console
copy($0)
```  

## <a name="debug"></a>depurar  

```console
debug(method)
```  

>[!NOTE]
> O [problema do Chromium #1050237][MonorailIssue1050237] está rastreando um bug com a `debug()` função.  Se você encontrar o problema, tente [usar pontos de interrupção.][DevtoolsJavascriptBreakpoints]  

Quando você solicita o método especificado, o depurador é invocado e quebra dentro do método na ferramenta **Sources,** permitindo passar pelo código e depurá-lo.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Quebrar dentro de um método com depuração()" lightbox="../media/console-debug-text.msft.png":::
   Figura 13: Quebrar dentro de um método com `debug()`  
:::image-end:::  

Use para parar de quebrar o método ou use a interface do usuário `undebug(method)` para desabilitar todos os pontos de interrupção.  

Para obter mais informações sobre pontos de interrupção, navegue até [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].  

## <a name="dir"></a>dir  

```console
dir(object)
```  

Exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.  Este método é um alias para o [método console.dir().][MDNConsoleDir]  

Avalie `document.head` no Console para exibir o HTML entre as marcas `<head>` `</head>` e.  Na figura e exemplo de código a seguir, uma listagem de estilo de objeto é exibida após o `console.dir()` uso no Console.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Método log document.head com dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Figura 14: Log `document.head` com `dir()` método  
:::image-end:::  

Para obter mais informações, navegue [`console.dir()`][DevToolsConsoleApiConsoleDirObject] até a entrada na API do Console.  

## <a name="dirxml"></a>dirxml  

```console
dirxml(object)
```  

Imprime uma representação XML do objeto especificado, conforme exibido na **ferramenta Elements.**  Esse método é equivalente ao [método console.dirxml().][MDNConsoleDirxml]  

## <a name="inspect"></a>inspect  

```console
inspect(object/method)
```  

Abre e seleciona o elemento ou objeto especificado no painel apropriado: a ferramenta **Elements** para elementos DOM ou a ferramenta **Memória** para objetos de pilha JavaScript.  

Na figura e amostra de código a seguir, a `document.body` abre na **ferramenta Elements.**  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecionar um elemento com inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Figura 15: Inspecionar um elemento com `inspect()`  
:::image-end:::  

Ao passar um método para inspecionar, o método abre o documento na **ferramenta Fontes** para você inspecionar.  

## <a name="geteventlisteners"></a>getEventListeners  

```console
getEventListeners(object)
```  

Retorna os ouvintes de eventos registrados no objeto especificado.  O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \(como `click` ou `keydown` \).  Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.  Na figura de exemplo de código a seguir, todos os ouvintes de eventos registrados no objeto do documento são listados.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Saída do uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Figura 16: O resultado do uso `getEventListeners(document)`  
:::image-end:::  

Se mais de um ouvinte estiver registrado no objeto especificado, a matriz conterá um membro para cada ouvinte.  Na figura a seguir, há dois ouvintes de eventos registrados no elemento de documento do `click` evento.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Vários ouvintes" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Figura 17: Vários ouvintes  
:::image-end:::  

Você pode expandir ainda mais cada um dos objetos a seguir para explorar as propriedades.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Exibição expandida do objeto ouvinte" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Figura 18: Exibição expandida do objeto ouvinte  
:::image-end:::  

## <a name="keys"></a>chaves  

```console
keys(object)
```  

Retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.  Para obter os valores associados das mesmas propriedades, use `values()` .  

Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.  

```console
var player1 =   
```  

Na figura e amostras de código a seguir, o resultado supõe que foi definido no `player1` namespace global \(for simplicity\) antes de digitar e `keys(player1)` no `values(player1)` console.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Os comandos keys() e values()" lightbox="../media/console-keys-values.msft.png":::
   Figura 19: Os `keys()` comandos e `values()`  
:::image-end:::  

## <a name="monitor"></a>monitor  

```console
monitor(method)
```  

Registra uma mensagem no console que indica o nome do método juntamente com os argumentos que são passados para o método quando ele foi chamado.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="O método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Figura 20: O `monitor()` método  
:::image-end:::  

Use `unmonitor(method)` para interromper o monitoramento.  

## <a name="monitorevents"></a>monitorEvents  

```console
monitorEvents(object[, events])
```  

Quando um dos eventos especificados ocorre no objeto especificado, o objeto de evento é registrado no console.  Você pode especificar um único evento a ser monitorado, uma matriz de eventos ou um dos tipos de eventos genéricos mapeados para uma coleção predefinida de eventos.  Revise o exemplo de código a seguir e a figura.  

O seguinte monitora todos os eventos de resize no objeto window.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Monitoring window resize events" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Figura 21: Monitoring window resize events  
:::image-end:::  

O seguinte define uma matriz para monitorar eventos `resize` e ambos no objeto `scroll` window.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Você também pode especificar um dos tipos de eventos disponíveis, cadeias de caracteres que mapeiam para conjuntos predefinidos de eventos.  A tabela a seguir exibe os tipos de eventos disponíveis e os mapeamentos de eventos associados.  

| Event type | Eventos mapeados correspondentes |  
|:--- |:--- |  
| `mouse` | "click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel" |  
| `key` | "keydown", "keypress", "keyup", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom" |  

No exemplo de código a seguir, o tipo de evento correspondente a eventos em um campo de texto de entrada está atualmente `key` `key` selecionado na ferramenta **Elements.**  

```console
monitorEvents($0, "key");
```  

Na figura a seguir, a saída de exemplo após digitar um caractere no campo de texto é exibida.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Monitorando os principais eventos" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Figura 22: Monitorando os principais eventos  
:::image-end:::  

## <a name="profile"></a>profile  

```console
profile([name])
```  

Inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.  O [método profileEnd()](#profileend) conclui o perfil e exibe os resultados na **ferramenta Memória.**  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Execute o `profile()` método para iniciar a criação de perfil.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Execute o [método profileEnd()](#profileend) para interromper a criação de perfil e exibir os resultados na **ferramenta Memória.**  

Os perfis também podem ser aninhados.  Nos exemplos de código a seguir e figurar o resultado é o mesmo, independentemente da ordem.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.  

## <a name="profileend"></a>profileEnd  

```console
profileEnd([name])
```  

Conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados na **ferramenta Memória.**  Você deve estar executando o [método profile().](#profile)  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Execute o [método profile()](#profile) para iniciar a criação de perfil.  
1.  Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados na ferramenta **Memória.**  
    
    ```console
    profileEnd("My profile")
    ```  

Os perfis também podem ser aninhados.  No exemplo de código a seguir e figura o resultado é o mesmo, independentemente da ordem.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

O resultado aparece como um Instantâneo de Pilha na **ferramenta Memória.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfis agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Figura 23: Perfis agrupados  
:::image-end:::  

> [!NOTE]
> Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.  

## <a name="queryobjects"></a>queryObjects  

```console
queryObjects(Constructor)
```  

Retornar uma matriz de objetos criados com o construtor especificado.  O escopo de é o contexto de tempo de execução `queryObjects()` selecionado no console.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Retorna todos `Promises` .  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      Retorna todos os elementos HTML.  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      Retorna todos os objetos que foram instautados usando `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>table  

```console
table(data[, columns])
```  

Registra dados de objeto com formatação de tabela com base no objeto de dados em com títulos opcionais de coluna.  Na figura e exemplo de código a seguir, uma lista de nomes usando uma tabela no console é exibida.  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="O resultado do método table()" lightbox="../media/console-table-display.msft.png":::
   Figura 24: O resultado do `table()` método  
:::image-end:::  

## <a name="undebug"></a>undebug  

```console
undebug(method)
```  

Interrompe a depuração do método especificado para que, quando o método for chamado, o depurador não seja mais invocado.  

```console
undebug(getData);
```  

## <a name="unmonitor"></a>unmonitor  

```console
unmonitor(method)
```  

Interrompe o monitoramento do método especificado.  Esse método é usado em conjunto com o [método monitor().](#monitor)  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a>unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Interrompe o monitoramento de eventos para o objeto e eventos especificados.  Por exemplo, o seguinte interrompe todo o monitoramento de eventos no objeto window.  

```console
unmonitorEvents(window);
```  

Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.  Por exemplo, o código a seguir começa a monitorar todos os eventos no elemento selecionado no momento e interrompe o monitoramento de eventos \(talvez para reduzir o ruído na saída `mouse` `mousemove` do console\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a>values  

```console
values(object)
```  

Retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência da API do Console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir - Referência da API de Console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Como pausar seu código com pontos de interrupção no Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar o tempo de execução do JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: depuração(função) não está funcionando | Monotrilho"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/utilities) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
