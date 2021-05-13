---
description: Uma referência de comandos de conveniência disponíveis no console Microsoft Edge DevTools.
title: Referência de API de Utilitários do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 436f2807c5fab1723ca6cc93fddc68d9ecf12db7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564529"
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
# <a name="console-utilities-api-reference"></a>Referência de API de Utilitários do console  

A API Utilitários de Console contém uma coleção de comandos de conveniência para concluir as seguintes tarefas comuns.  

*   Escolher e inspecionar elementos DOM  
*   Exibir dados em formato acessível  
*   Parar e iniciar o profiler  
*   Monitorar eventos DOM  
    
> [!WARNING]
> Os comandos a seguir só funcionam no console **** Microsoft Edge DevTools .  Os comandos não funcionarão se executados de seus scripts.  

Para obter mais informações sobre os métodos e e o restante dos `console.log()` `console.error()` `console.*` métodos, navegue até [Console API Reference][DevToolsConsoleApi].  

## <a name="recently-evaluated-expression"></a>Expressão avaliada recentemente  

### <a name="console-syntax"></a>Sintaxe do console  

```console
$_
```  

Este comando retorna o valor da expressão avaliada mais recentemente.  

### <a name="console-example"></a>Exemplo de console  

Na figura a seguir, uma expressão simples \( `2 + 2` \) é avaliada.  Em `$_` seguida, a propriedade é avaliada, que contém o mesmo valor.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ é a expressão avaliada mais recentemente" lightbox="../media/console-arithmatic.msft.png":::
   `$_` é a expressão avaliada mais recentemente  
:::image-end:::  

Na figura a seguir, a expressão avaliada inicialmente contém uma matriz de nomes.  Avaliando para encontrar o comprimento da matriz, o valor armazenado se torna a expressão avaliada mais `$_.length` `$_` recente, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ muda quando novos comandos são avaliados" lightbox="../media/console-array-length.msft.png":::
   `$_` muda quando novos comandos são avaliados  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a>Elemento escolhido recentemente ou objeto JavaScript  

### <a name="console-syntax"></a>Sintaxe do console  

```console
$0
```  

Este comando retorna o elemento escolhido mais recentemente ou o objeto JavaScript.  `$1` retorna o segundo escolhido mais recentemente e assim por diante.  Os comandos , , e funcionam como uma referência histórica aos últimos cinco elementos DOM inspecionados na ferramenta Elements ou os cinco últimos objetos de pilha JavaScript escolhidos na `$0` `$1` ferramenta `$2` `$3` `$4` **Memória.** ****  

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
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a>Exemplo de console  

Na figura a seguir, um `img` elemento é escolhido na ferramenta **Elements.**  Na gaveta **Console,** `$0` foi avaliado e exibe o mesmo elemento.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Os $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   O `$0`  
:::image-end:::  

Na figura a seguir, a imagem exibe um elemento diferente escolhido na mesma página da Web.  O `$0` agora se refere ao elemento recém-escolhido, enquanto retorna o escolhido `$1` anteriormente.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="O $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   O `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a>Seletor de consulta  

### <a name="console-syntax"></a>Sintaxe do console  

```console
$(selector, [startNode])
```  

Este comando retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.  Este método é um alias para o [método document.querySelector().][MdnDocsWebApiDocumentQueryselector]  

### <a name="console-example"></a>Exemplo de console  

Na figura a seguir, uma referência ao primeiro `<img>` elemento na página da Web é retornada.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   O `$('img')`  
:::image-end:::  

Para encontrar o primeiro elemento no DOM ou para encontrá-lo e exibi-lo na página da Web, conclua as seguintes ações.  

1.  Passe o mouse no resultado retornado.  
1.  Abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Revelar no Painel de Elementos**.  

Na figura a seguir, uma referência ao elemento escolhido no momento é retornada e a `src` propriedade é exibida.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   O `$('img').src`  
:::image-end:::  

Este método também dá suporte a um segundo parâmetro, , que especifica um elemento ou nó do qual `startNode` procurar elementos.  O valor padrão do parâmetro é `document` .  

Na figura a seguir, o primeiro elemento após o elemento é encontrado e a `img` propriedade do elemento é `title--image` `src` `img` retornada.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   O `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Se você estiver usando uma biblioteca como jQuery que usa , a funcionalidade será substituída e corresponderá à implementação `$` `$` dessa biblioteca.  

---  

## <a name="query-selector-all"></a>Seletor de consulta todos  

### <a name="console-syntax"></a>Sintaxe do console  

```console
$$(selector, [startNode])
```  

Este comando retorna uma matriz de elementos que corresponderão ao seletor CSS especificado.  Esse método equivale a executar o [método document.querySelectorAll().][MdnDocsWebApiDocumentQueryselectorall]  

### <a name="console-example"></a>Exemplo de console  

Na figura e exemplo de código a seguir, use para criar uma matriz de todos os elementos na página da Web atual e exibir o valor da propriedade `$$()` `<img>` para cada `src` elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usando $$() para escolher todas as imagens na página da Web e exibir as fontes" lightbox="../media/console-element-selector-image-all.msft.png":::
   Usando `$$()` para escolher todas as imagens na página da Web e exibir as fontes  
:::image-end:::  

Este método também dá suporte a um segundo parâmetro, , que especifica um elemento ou nó do qual `startNode` procurar elementos.  O valor padrão do parâmetro é `document` .  

Na figura e amostra de código a seguir, uma versão modificada do exemplo de código anterior e a figura usam para criar uma matriz de todos os elementos que aparecem na página da Web atual após o `$$()` `<img>` nó escolhido.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usando $$() para escolher todas as imagens que aparecem após o elemento div <div> na página da Web e exibir as fontes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Usando `$$()` para escolher todas as imagens que aparecem após o elemento especificado na página da Web e exibir as `<div>` fontes  
:::image-end:::  

> [!NOTE]
> Selecione `Shift` + `Enter` no **Console para** iniciar uma nova linha sem executar o script.  

---  

## <a name="xpath"></a>XPath  

### <a name="console-syntax"></a>Sintaxe do console  

```console
$x(path, [startNode])
```  

Este comando retorna uma matriz de elementos DOM que combinam com a expressão XPath especificada.  

### <a name="console-example"></a>Exemplo de console  

Na figura e no exemplo de código a seguir, todos os `<p>` elementos na página da Web são retornados.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usando um seletor XPath" lightbox="../media/console-array-xpath.msft.png":::
   Usando um seletor XPath  
:::image-end:::  

Na figura e amostra de código a seguir, todos os `<p>` elementos que contêm `<a>` elementos são retornados.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usando um seletor XPath mais complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Usando um seletor XPath mais complicado  
:::image-end:::  

Semelhante aos outros comandos do seletor, tem um segundo parâmetro opcional, , que especifica um elemento ou nó do qual `$x(path)` `startNode` procurar elementos.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usando um seletor XPath com startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Usando um seletor XPath com `startNode`  
:::image-end:::  

---  

## <a name="clear"></a>clear  

### <a name="console-syntax"></a>Sintaxe do console  

```console
clear()
```  

Essa vírgula limpa o console do histórico.  

### <a name="console-example"></a>Exemplo de console  

```console
clear()
```  

## <a name="copy"></a>copy  

### <a name="console-syntax"></a>Sintaxe do console  

```console
copy(object)
```  

Este método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.  

### <a name="console-example"></a>Exemplo de console  

```console
copy($0)
```  

---  

## <a name="debug"></a>depurar  

### <a name="console-syntax"></a>Sintaxe do console  

```console
debug(method)
```  

>[!NOTE]
> O [Chromium problema #1050237][CR1050237] está rastreando um bug com a `debug()` função.  Se você encontrar o problema, tente usar [pontos de interrupção.][DevtoolsJavascriptBreakpoints]  

Quando você solicita o método especificado, o depurador invoca e quebra dentro do método na **ferramenta Sources.**  Ele permite que você passo a passo e depurar o código.  

### <a name="console-example"></a>Exemplo de console  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Quebrar dentro de um método com depuração()" lightbox="../media/console-debug-text.msft.png":::
   Quebrar dentro de um método com `debug()`  
:::image-end:::  

Use para parar de quebrar o método ou use a interface do usuário `undebug(method)` para desativar todos os pontos de interrupção.  

Para obter mais informações sobre pontos de interrupção, navegue até [How to pause your code with breakpoints in Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].  

---  

## <a name="dir"></a>dir  

### <a name="console-syntax"></a>Sintaxe do console  

```console
dir(object)
```  

Este comando exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.  Este método é um alias para o [método console.dir().][MdnDocsWebApiConsoleDir]  

Avalie `document.head` no Console **para** exibir o HTML entre as `<head>` marcas `</head>` e.  

### <a name="console-example"></a>Exemplo de console  

Na figura e exemplo de código a seguir, uma listagem de estilo de objeto é exibida após o uso `console.dir()` no **Console**.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Método log document.head com dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Log `document.head` com `dir()` método  
:::image-end:::  

Para obter mais informações, [navegue até console.dir()][DevToolsConsoleApiConsoleDirObject] na API do Console.  

---  

## <a name="dirxml"></a>dirxml  

### <a name="console-syntax"></a>Sintaxe do console  

```console
dirxml(object)
```  

Este comando imprime uma representação XML do objeto especificado, conforme exibido na **ferramenta Elements.**  Esse método é equivalente ao [método console.dirxml().][MdnDocsWebApiConsoleDirxml]  

---  

## <a name="inspect"></a>inspect  

### <a name="console-syntax"></a>Sintaxe do console  

```console
inspect(object/method)
```  

Este comando abre e escolhe o elemento ou objeto especificado no painel apropriado: a ferramenta **Elements** para elementos DOM ou a ferramenta **Memória** para objetos de pilha JavaScript.  

### <a name="console-example"></a>Exemplo de console  

Na figura e amostra de código a seguir, a `document.body` abre na **ferramenta Elements.**  

### <a name="console-example"></a>Exemplo de console  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspecionar um elemento com inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Inspecionar um elemento com `inspect()`  
:::image-end:::  

Ao passar um método a ser inspecionado, o método abre a página da Web na **ferramenta Fontes** para você inspecionar.  

---  

## <a name="geteventlisteners"></a>getEventListeners  

### <a name="console-syntax"></a>Sintaxe do console  

```console
getEventListeners(object)
```  

Este comando retorna os ouvintes de eventos registrados no objeto especificado.  O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \(como `click` ou `keydown` \).  Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.  

### <a name="console-example"></a>Exemplo de console  

No trecho de código a seguir e na figura, todos os ouvintes de eventos registrados no `document` objeto são listados.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Saída do uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   O resultado do uso `getEventListeners(document)`  
:::image-end:::  

Se mais de um ouvinte estiver registrado no objeto especificado, a matriz conterá um membro para cada ouvinte.  Na figura a seguir, dois ouvintes de eventos são registrados no `document` elemento do `click` evento.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Vários ouvintes" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Vários ouvintes  
:::image-end:::  

Você pode expandir ainda mais cada um dos objetos a seguir para explorar as propriedades.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Exibição expandida do objeto ouvinte" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Exibição expandida do objeto ouvinte  
:::image-end:::  

---  

## <a name="keys"></a>chaves  

### <a name="console-syntax"></a>Sintaxe do console  

```console
keys(object)
```  

Este comando retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.  Para obter os valores associados das mesmas propriedades, use `values()` .  

### <a name="console-example"></a>Exemplo de console  

Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.  

```console
var player1 = {"name": "Ted", "level": 42}
```  

Na figura e amostras de código a seguir, o resultado supõe que foi definido no `player1` namespace global \(for simplicity\) antes de digitar e `keys(player1)` no `values(player1)` console.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Os comandos keys() e values()" lightbox="../media/console-keys-values.msft.png":::
   Comandos `keys()` e `values()`  
:::image-end:::  

---  

## <a name="monitor"></a>monitor  

### <a name="console-syntax"></a>Sintaxe do console  

```console
monitor(method)
```  

Esse comando registra uma mensagem no console que indica o nome do método juntamente com os argumentos passados para o método como parte de uma solicitação.  

### <a name="console-example"></a>Exemplo de console  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="O método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   O `monitor()` método  
:::image-end:::  

Use `unmonitor(method)` para encerrar o monitoramento.  

---  

## <a name="monitorevents"></a>monitorEvents  

### <a name="console-syntax"></a>Sintaxe do console  

```console
monitorEvents(object[, events])
```  

Quando um dos eventos especificados ocorre no objeto especificado, o objeto de evento é registrado no console.  Você pode especificar um único evento a ser monitorado, uma matriz de eventos ou um dos tipos de eventos genéricos mapeados para uma coleção predefinida de eventos.  

### <a name="console-example"></a>Exemplo de console  

Revise o exemplo de código a seguir e a figura.  

O seguinte monitora todos os eventos de resize no objeto window.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Monitoring window resize events" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Monitoring window resize events  
:::image-end:::  

O trecho de código a seguir define uma matriz para monitorar eventos e eventos `resize` `scroll` no objeto window.  

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

No exemplo de código a seguir, o tipo de evento correspondente a eventos em um campo de texto de entrada é escolhido `key` `key` atualmente na ferramenta **Elements.**  

```console
monitorEvents($0, "key");
```  

Na figura a seguir, a saída de exemplo após digitar um caractere no campo de texto é exibida.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Monitorando os principais eventos" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Monitorando os principais eventos  
:::image-end:::  

---  

## <a name="profile"></a>profile  

### <a name="console-syntax"></a>Sintaxe do console  

```console
profile([name])
```  

Este comando inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.  O [método profileEnd()](#profileend) conclui o perfil e exibe os resultados na **ferramenta Memória.**  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Exemplo de console  

1.  Execute o `profile()` método para iniciar a criação de perfil.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Execute o [método profileEnd()](#profileend) para interromper a criação de perfil e exibir os resultados na **ferramenta Memória.**  

Os perfis também podem ser aninhados.  Na figura e amostras de código a seguir, o resultado é o mesmo, seja qual for a ordem.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.  

---  

## <a name="profileend"></a>profileEnd  

### <a name="console-syntax"></a>Sintaxe do console  

```console
profileEnd([name])
```  

Este comando conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados na **ferramenta Memória.**  Você deve estar executando o [método profile().](#profile)  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Exemplo de console  

1.  Execute o [método profile()](#profile) para iniciar a criação de perfil.  
1.  Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados na ferramenta **Memória.**  
    
    ```console
    profileEnd("My profile")
    ```  

Os perfis também podem ser aninhados.  Na figura e amostra de código a seguir, o resultado é o mesmo, seja qual for a ordem.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

O resultado aparece como um Instantâneo de Pilha na **ferramenta Memória.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfis agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Perfis agrupados  
:::image-end:::  

> [!NOTE]
> Vários perfis de CPU podem operar ao mesmo tempo e você não precisa fechar cada um deles na ordem de criação.  

---  

## <a name="queryobjects"></a>queryObjects  

### <a name="console-syntax"></a>Sintaxe do console  

```console
queryObjects(Constructor)
```  

Este comando retorna uma matriz de objetos criados com o construtor especificado.  O escopo de é o contexto de tempo de execução `queryObjects()` atualmente escolhido no **Console**.  

### <a name="console-example"></a>Exemplo de console  

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

## <a name="table"></a>tabela  

### <a name="console-syntax"></a>Sintaxe do console  

```console
table(data[, columns])
```  

Este comando registra dados de objeto com formatação de tabela com base no objeto de dados em com títulos opcionais de coluna.  

### <a name="console-example"></a>Exemplo de console  

Na figura e exemplo de código a seguir, uma lista de nomes usando uma tabela no console é exibida.  

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
   O resultado do `table()` método  
:::image-end:::  

---  

## <a name="undebug"></a>undebug  

### <a name="console-syntax"></a>Sintaxe do console  

```console
undebug(method)
```  

Este comando interrompe a depuração do método especificado. Portanto, quando o método é solicitado, o depurador não é mais invocado.  

### <a name="console-example"></a>Exemplo de console  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a>unmonitor  

### <a name="console-syntax"></a>Sintaxe do console  

```console
unmonitor(method)
```  

Este comando interrompe o monitoramento do método especificado.  Esse método é usado em conjunto com o [método monitor().](#monitor)  

### <a name="console-example"></a>Exemplo de console  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a>unmonitorEvents  

### <a name="console-syntax"></a>Sintaxe do console  

```console
unmonitorEvents(object[, events])
```  

Este comando interrompe o monitoramento de eventos para o objeto e eventos especificados.  

### <a name="console-example"></a>Exemplo de console  

Por exemplo, o trecho de código a seguir interrompe todo o monitoramento de eventos no objeto window.  

```console
unmonitorEvents(window);
```  

Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.  Por exemplo, o código a seguir começa a monitorar todos os eventos no elemento escolhido no momento e interrompe o monitoramento de eventos \(talvez para reduzir o ruído na saída `mouse` `mousemove` do console\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a>values  

### <a name="console-syntax"></a>Sintaxe do console  

```console
values(object)
```  

Este comando retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.  

### <a name="console-example"></a>Exemplo de console  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir - Referência da API de Console | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Como pausar seu código com pontos de interrupção Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Acelerar o tempo de execução do JavaScript | Microsoft Docs"  

[CR1050237]: https://crbug.com/1050237 "Problema 1050237: depuração(função) não está funcionando | Chromium bugs"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/utilities) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
