---
title: Referência de API de utilitários de console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601793"
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





# Referência de API de utilitários de console   



A API de utilitários de console contém um conjunto de comandos de conveniência para realizar tarefas comuns: selecionando e inspecionando os elementos DOM, exibindo dados em um formato legível, interrompendo e iniciando o gerador de perfil e monitorando eventos DOM.  

> [!WARNING]
> Os comandos a seguir só funcionam no console Microsoft Edge DevTools.  Os comandos não funcionam se forem executados a partir de seus scripts.  

Procurando `console.log()` , `console.error()` e o restante dos `console.*` métodos?  Consulte [referência de API do console][DevToolsConsoleApi].  

## Expressão avaliada recentemente  

```console
$_
```  

Retorna o valor da expressão avaliada mais recentemente.  

Na [Figura 1](#figure-1), uma expressão simples \ ( `2 + 2` \) é avaliada.  A `$_` propriedade é então avaliada, que contém o mesmo valor.  

> ##### Figura 1  
> `$_` é a expressão avaliada mais recentemente  
> ![$ _ é a expressão avaliada mais recentemente][ImageRecentExpression]  

Na [Figura 2](#figure-2), a expressão avaliada inicialmente contém uma matriz de nomes.  Avaliando `$_.length` para localizar o comprimento da matriz, o valor armazenado em `$_` alterações para se tornar a expressão avaliada mais recente `4` .  

> ##### Figura 2  
> `$_` alterações quando novos comandos são avaliados  
> ![$ _ muda quando novos comandos são avaliados][ImageChangedRecentExpression]  

## Elemento ou objeto JavaScript selecionado recentemente  

```console
$0
```  

Retorna o elemento do elemento JavaScript ou o objeto selecionado mais recentemente.  `$1` Retorna a segunda opção selecionada mais recentemente e assim por diante.  Os `$0` comandos,,, `$1` `$2` `$3` e `$4` funcionam como uma referência histórica aos cinco últimos elementos DOM inspecionados no painel **elementos** ou nos últimos cinco objetos de heap JavaScript selecionados no painel **memória** .  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

Na [Figura 3](#figure-3), um `img` elemento é selecionado no painel **elementos** .  Na gaveta do **console** , foi `$0` avaliada e exibe o mesmo elemento.  

> ##### Figura 3  
> O `$0`  
> ![O $0][ImageElement0]  

Na [Figura 4](#figure-4), a imagem mostra um elemento diferente selecionado na mesma página.  O `$0` agora se refere ao elemento selecionado recentemente, enquanto `$1` retorna o anterior selecionado.  

> ##### Figura 4  
> O `$1`  
> ![O $1][ImageElement1]  

## Seletor de consulta  

```console
$(selector, [startNode])
```  

Retorna a referência ao primeiro elemento DOM com o seletor CSS especificado.  Esse método é um alias para o método [Document. querySelector ()][MDNDocumentQuerySelector] .  

Na [Figura 5](#figure-5), uma referência para o primeiro `<img>` elemento no documento é retornada.  

> ##### Figura 5  
> O `$('img')`  
> ![$ (' Img ')][ImageElementImg]  

Clique com o botão direito do mouse no resultado retornado e selecione **revelar no painel de elementos** para localizá-lo no dom ou **role para ver para exibi** -lo na página.  

Na [Figura 6](#figure-6), uma referência ao elemento atualmente selecionado é retornada e a propriedade src é exibida.  

> ##### Figura 6  
> O `$('img').src`  
> ![$ (' Img '). src][ImageElementImgSource]  

Esse método também dá suporte a um segundo parâmetro, startNode, que especifica um "elemento" ou um nó do qual Pesquisar elementos.  O valor padrão desse parâmetro é `document` .  

Na [Figura 7](#figure-7), o primeiro `img` elemento é encontrado após a `title--image` e exibe o valor `src` correto.  

> ##### Figura 7  
> $ (' Img ', Document. querySelector (' título--imagem ')). src  
> ![$ (' Img ', Document. querySelector (' título--imagem ')). src][ImageElementImgNodeSource]  

> [!NOTE]
> Se você estiver usando uma biblioteca como o jQuery que usa `$` , essa funcionalidade será sobrescrita e `$` corresponderá à implementação dessa biblioteca.  

## Seletor de consulta tudo  

```console
$$(selector, [startNode])
```  

Retorna uma matriz de elementos que correspondem ao seletor CSS especificado.  Esse método é equivalente a chamar o método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

Na [Figura 8](#figure-8), use `$$()` para criar uma matriz de todos os `<img>` elementos no documento atual e exibir o valor da `src` propriedade de cada elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### Figura 8  
> Usar `$$()` para selecionar todas as imagens no documento e exibir as fontes  
> ![Usando $ $ () para selecionar todas as imagens no documento e exibir as fontes][ImageArrayElementImgSource]  

Esse método também oferece suporte a um segundo parâmetro, startNode, que especifica um elemento ou nó do qual Pesquisar elementos.  O valor padrão desse parâmetro é `document` .  

Na [Figura 9](#figure-9), uma versão modificada da [Figura 8](#figure-8) usa `$$()` para criar uma matriz de todos os `<img>` elementos que aparecem no documento atual após o nó selecionado.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### Figura 9  
> Usar `$$()` para selecionar todas as imagens que aparecem após o `<div>` elemento especificado no documento e exibir as fontes  
> ![Usando $ $ () para selecionar todas as imagens que aparecem após o <div especificado> o elemento no documento e exibir as fontes][ImageArrayElementImgNodeSource]  

> [!NOTE]
> Pressione `Shift` + `Enter` no console para iniciar uma nova linha sem executar o script.  

## XPath  

```console
$x(path, [startNode])
```  

Retorna uma matriz de elementos DOM que correspondem à expressão XPath especificada.  

Na [Figura 10](#figure-10), todos os `<p>` elementos na página são retornados.  

```console
$x("//p")
```  

> ##### Figura 10  
> Usando um seletor XPath  
> ![Usando um seletor XPath][ImageArrayXpath]  

Na [Figura 11](#figure-11), todos os `<p>` elementos que contêm `<a>` elementos são retornados.  

```console
$x("//p[a]")
```  

> ##### Figura 11  
> Usando um seletor XPath mais complicado  
> ![Usando um seletor XPath mais complicado][ImageArrayXpathChild]  

Semelhante aos outros comandos do seletor, `$x(path)` tem um segundo parâmetro opcional, `startNode` que especifica um elemento ou nó do qual Pesquisar elementos.  

> ##### Figura 12  
> Usando um seletor XPath com `startNode`  
> ![Usando um seletor XPath com startNode][ImageArrayXpathNode]  

## elimina  

```console
clear()
```  

Limpa o console do histórico.  

```console
clear()
```  

## copy  

```console
copy(object)
```  

O `copy(object)` método copia uma representação de cadeia de caracteres do objeto especificado para a área de transferência.  

```console
copy($0)
```  

## depurar  

```console
debug(method)
```  

>[!NOTE]
> O [problema Chromium #1050237][MonorailIssue1050237] está acompanhando um bug com a `debug()` função.  Se você encontrar esse problema, tente [usar pontos de interrupção][DevtoolsJavascriptBreakpoints] em vez disso.  

Quando você solicita o método especificado, o depurador é invocado e é quebrado dentro do método no painel **fontes** , permitindo que você percorra o código e depure-o.  

```console
debug("debug");
```  

> ##### Figura 13  
> Quebrando dentro de um método com `debug()`  
> ![Quebrando dentro de um método com debug ()][ImageDebugMethod]  

Use `undebug(method)` para parar de quebrar o método ou use a interface do usuário para desativar todos os pontos de interrupção.  

Para obter mais informações sobre pontos de interrupção, consulte [Pausar um código com pontos de interrupção][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Exibe uma listagem de estilo de objeto de todas as propriedades do objeto especificado.  Esse método é um alias para o método [console. dir ()][MDNConsoleDir] .  

Avaliar `document.head` no console para exibir o HTML entre as `<head>` marcas e `</head>` .  Na [Figura 14](#figure-14), uma listagem de estilo de objeto é exibida após `console.dir()` o uso no console.  

```console
document.head;
dir(document.head);
```  

> ##### Figura 14  
> Registro `document.head` em log com o `dir()` método  
> ![Registrando em log o documento. Head com o método dir ()][ImageLogObject]  

Para obter mais informações, consulte a [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrada na API do console.  

## dirxml  

```console
dirxml(object)
```  

Imprime uma representação XML do objeto especificado, como visto na guia **elementos** .  Esse método é equivalente ao método [console. DirXML ()][MDNConsoleDirxml] .  

## inspeção  

```console
inspect(object/method)
```  

Abre e seleciona o elemento ou o objeto especificado no painel apropriado: o painel **elementos** para elementos DOM ou o painel **memória** para objetos de heap JavaScript.  

Na [Figura 15](#figure-15), o `document.body` abre no painel de **elementos** .  

```console
inspect(document.body);
```  

> ##### Figura 15  
> Inspecionar um elemento com `inspect()`  
> ![Inspecionar um elemento com inspeção ()][ImageInspectElement]  

Ao passar um método para inspecionar, o método abre o documento no painel **fontes** para inspeção.  

## getEventListeners  

```console
getEventListeners(object)
```  

Retorna os ouvintes de eventos registrados no objeto especificado.  O valor de retorno é um objeto que contém uma matriz para cada tipo de evento registrado \ (como `click` ou `keydown` \).  Os membros de cada matriz são objetos que descrevem o ouvinte registrado para cada tipo.  Na [Figura 16](#figure-16), todos os ouvintes de eventos registrados no objeto do documento são listados.  

```console
getEventListeners(document);
```  

> ##### Figura 16  
> Saída de uso `getEventListeners(document)`  
> ![Saída do uso de getEventListeners (documento)][ImageGetListeners]  

Se mais de um ouvinte estiver registrado no objeto especificado, a matriz contém um membro para cada ouvinte.  Na [Figura 16](#figure-16), há dois ouvintes de eventos registrados no elemento do documento para o `click` evento.  

> ##### Figura 17  
> Vários ouvintes  
> ![Vários ouvintes][ImageMultipleListeners]  

Você pode expandir ainda mais cada um dos seguintes objetos para explorar as propriedades.  

> ##### Figura 18  
> Exibição expandida do objeto Listener  
> ![Exibição expandida do objeto Listener][ImageListenersExpanded]  

## chaves  

```console
keys(object)
```  

Retorna uma matriz que contém os nomes das propriedades pertencentes ao objeto especificado.  Para obter os valores associados das mesmas propriedades, use `values()` .  

Por exemplo, suponha que seu aplicativo definiu o objeto a seguir.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

Na [Figura 19](#figure-19), o resultado pressupõe `player1` que foi definido no namespace global \ (para simplicidade \) antes de digitar `keys(player1)` e `values(player1)` no console.  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### Figura 19  
> Os `keys()` `values()` comandos e  
> ![Os comandos Keys () e Values ()][ImageConsoleKeysValues]  

## monitor  

```console
monitor(method)
```  

Registra uma mensagem no console que indica o nome do método juntamente com os argumentos que são passados para o método quando ele é chamado.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### Figura 20  
> O `monitor()` método  
> ![O método monitor ()][ImageConsoleMonitorSum]  

Use `unmonitor(method)` para interromper o monitoramento.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Quando ocorre um dos eventos especificados no objeto especificado, o objeto de evento é registrado no console.  Você pode especificar um único evento para monitorar, uma matriz de eventos ou um dos tipos de eventos genéricos que são mapeados para uma coleção predefinida de eventos.  Veja a [Figura 21](#figure-21).  

Os seguintes monitores redimensionam eventos no objeto Window.  

```console
monitorEvents(window, "resize");
```  

> ##### Figura 21  
> Janela de monitoramento redimensionar eventos  
> ![Janela de monitoramento redimensionar eventos][ImageMonitorResize]  

O seguinte define uma matriz para monitorar os dois `resize` e os `scroll` eventos no objeto Window.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Você também pode especificar um dos tipos de eventos disponíveis, cadeias de caracteres que são mapeados para conjuntos de eventos predefinidos.  A tabela a seguir mostra os tipos de eventos disponíveis e os mapeamentos de eventos associados.  

| Event type | Eventos mapeados correspondentes |  
|:--- |:--- |  
| `mouse` | "clique em", "DblClick", "botão de mouse", "MouseUp", "mouseout", "mouse pressionado", "MouseUp", "MouseWheel" |  
| `key` | "KeyDown", "KeyPress", "KeyUp", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "Blur", "alterar", "enfocar", "selecionar", "enviar", "zoom", "selecionar", "enviar", "zoom" |  

Na [Figura 22](#figure-22), o `key` tipo de evento correspondente a `key` eventos em um campo de texto de entrada está selecionado atualmente no painel de **elementos** .  

```console
monitorEvents($0, "key");
```  

Na [Figura 22](#figure-22) a saída do exemplo após a digitação de um caractere no campo de texto é exibida.  

> ##### Figura 22  
> Monitorar eventos chave  
> ![Monitorar eventos chave][ImageMonitorKey]  

## profile  

```console
profile([name])
```  

Inicia uma sessão de criação de perfil de CPU JavaScript com um nome opcional.  O método [profileEnd ()](#profileend) conclui o perfil e exibe os resultados no painel **memória** .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Execute o `profile()` método para iniciar a criação de perfil.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Execute o método [profileEnd ()](#profileend) para interromper a criação de perfil e exibir os resultados no painel **memória** .  

Perfis também podem ser aninhados.  Na [Figura 23](#figure-23) , o resultado é o mesmo, independentemente da ordem.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Vários perfis de CPU podem operar ao mesmo tempo e não é necessário fechar cada um deles na ordem de criação.  

## profileEnd  

```console
profileEnd([name])
```  

Conclui uma sessão de criação de perfil de CPU JavaScript e exibe os resultados no painel **memória** .  Você deve estar executando o método [Profile ()](#profile) .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Execute o método [Profile ()](#profile) para iniciar a criação de perfil.  
1.  Execute o `profileEnd()` método para interromper a criação de perfil e exibir os resultados no painel **memória** .  
    
    ```console
    profileEnd("My profile")
    ```  

Perfis também podem ser aninhados.  Na [Figura 23](#figure-23) , o resultado é o mesmo, independentemente da ordem.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

O resultado aparece como um instantâneo de heap no painel **memória** .  

> ##### Figura 23  
> Perfis agrupados  
> ![Perfis agrupados][ImageGroupedProfiles]  

> [!NOTE]
> Vários perfis de CPU podem operar ao mesmo tempo e não é necessário fechar cada um deles na ordem de criação.  

## TableName  

```console
table(data[, columns])
```  

Registra dados de objeto com formatação de tabela com base no objeto de dados em títulos de coluna opcionais.  Na [Figura 24](#figure-24), é exibida uma lista de nomes usando uma tabela no console.  

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

> ##### Figura 24  
> O `table()` método  
> ![O método Table ()][ImageConsoleTable]  

## desdepurar  

```console
undebug(method)
```  

Interrompe a depuração do método especificado para que, quando o método for chamado, o depurador não seja mais invocado.  

```console
undebug(getData);
```  

## desmonitorar  

```console
unmonitor(method)
```  

Interrompe o monitoramento do método especificado.  Isso é usado em conjunto com o método [Monitor ()](#monitor) .  

```console
unmonitor(getData);
```  

## unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Interrompe o monitoramento de eventos do objeto e dos eventos especificados.  Por exemplo, o seguinte interrompe todos os monitoramentos de evento no objeto Window.  

```console
unmonitorEvents(window);
```  

Você também pode parar seletivamente o monitoramento de eventos específicos em um objeto.  Por exemplo, o código a seguir começa a monitorar todos os `mouse` eventos no elemento atualmente selecionado e, em seguida, interrompe o monitoramento de `mousemove` eventos \ (talvez reduzir o ruído na saída do console \).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## valores  

```console
values(object)
```  

Retorna uma matriz que contém os valores de todas as propriedades pertencentes ao objeto especificado.  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Figura 1: $ _ é a expressão avaliada mais recentemente"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Figura 2: $ _ muda quando novos comandos são avaliados"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Figura 3: o $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Figura 4: o $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Figura 5: o $ (' img ')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Figura 6: $ (' img '). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Figura 7: $ (' img ', Document. querySelector (' título--imagem ')). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Figura 8: usando $ $ () para selecionar todas as imagens no documento e exibir as fontes"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Figura 9: usando $ $ () para selecionar todas as imagens que aparecem após o <div especificado> o elemento no documento e exibir as fontes"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Figura 10: usando um seletor XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Figura 11: usando um seletor XPath mais complicado"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Figura 12: usando um seletor XPath com startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Figura 13: quebrando dentro de um método com o depurador ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Figura 14: registrando o documento. Body com o método dir ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Figura 15: inspecionar um elemento com inspecionar ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Figura 16: saída do uso de getEventListeners (documento)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Figura 17: vários ouvintes"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Figura 18: exibição expandida do objeto Listener"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Figura 19: os comandos Keys () e Values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Figura 20: o método monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Figura 21: monitorar eventos do Window Resize"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Figura 22: monitorar eventos de chave"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Figura 23: perfis agrupados"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Figura 24: o método Table ()"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Dir-referência de API do console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Como pausar um código com pontos de interrupção no Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar o tempo de execução do JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: a depuração (função) não está funcionando | Monorail"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/utilities) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
