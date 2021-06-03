---
description: Uma visão geral de como interagir com a página da Web atual no navegador usando a ferramenta Console
title: Usar o Console para interagir com o DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 80b0e4368b1c8feaf28a58ac2e3bd9c1ea2f1f92
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483292"
---
# <a name="use-the-console-to-interact-with-the-dom"></a>Usar o Console para interagir com o DOM

A **ferramenta Console** não é apenas para informações de registro em [log][DevtoolsConsoleConsoleLog] ou para [executar JavaScript arbitrário.][DevtoolsConsoleConsoleJavascript]  Também é uma ótima maneira de interagir com a página da Web no navegador.  Considere-a uma versão de ambiente de script da **ferramenta Inspecionar.**  

## <a name="read-from-the-dom"></a>Leitura do DOM

Para fazer referência ao header da página da Web, conclua as seguintes ações.  

1.  Abra o **Console**.
    *   Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).  
1.  Digite ou copie e copie o seguinte trecho de código no **Console**.  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Para fazer referência ao header no console, use document.querySelector" lightbox="../media/console-dom-get-reference.msft.png":::
    Para fazer referência ao header no console, use `document.querySelector`  
:::image-end:::  

Se você selecionar ou mover o cursor do mouse sobre o resultado `Shift` + `Tab` HTML, o DevTools realça o header para você.  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools realça a seção escolhida no Console" lightbox="../media/console-dom-highlight-element.msft.png":::
    DevTools realça a seção escolhida no **Console**  
:::image-end:::  

## <a name="manipulate-the-dom"></a>Manipular o DOM

Você também pode manipular a página da Web.  Por exemplo, se você copiar e colar ou digitar o seguinte no **Console**, uma borda verde será exibida ao redor do header.

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Para adicionar uma borda a um elemento, use o Console" lightbox="../media/console-dom-add-border.msft.png":::
    Para adicionar uma borda a um elemento, use o **Console**  
:::image-end:::  

Dependendo da complexidade da página da Web, pode ser difícil encontrar o elemento certo para manipular.  Mas você pode usar a **ferramenta Inspecionar** para ajudá-lo.  Digamos que você queira manipular `Documentation` a parte no header.

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Exibir o elemento que você inspecionar na tela" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    Exibir o elemento que você inspecionar na tela  
:::image-end:::  

Para obter uma referência direta ao elemento a ser manipulado, conclua as seguintes ações.  

1.  Use a **ferramenta Inspecionar** para escolher o elemento.  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Para escolher um elemento, use a ferramenta Inspector" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        Para escolher um elemento, use a **ferramenta Inspector**  
    :::image-end:::  
    
1.  Escolha-o e o DevTools saltará para a **ferramenta Elements.**  
1.  Escolha o `...` menu ao lado do elemento no exibição DOM.  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="O elemento escolhido é exibido na árvore DOM da ferramenta Elementos, escolha o menu de estouro para obter mais recursos" lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        O elemento escolhido é exibido na árvore DOM da ferramenta **Elementos,** escolha o menu de estouro para obter mais recursos  
    :::image-end:::  
    
1.  Abra o menu contextual e escolha `Copy`  >  `Copy JS Path` .  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Copie o caminho JavaScript de um elemento na exibição DOM da ferramenta Elements" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        Copie o caminho JavaScript de um elemento na exibição DOM da **ferramenta Elements**  
    :::image-end:::  
    
1.  Volte para o **Console e** colar o comando.  
    
Para alterar o texto do link para `My Playground` , adicione ao comando que você `.textContent = "My Playground"` colara anteriormente.  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Usar o Console para alterar o conteúdo de um elemento" lightbox="../media/console-dom-change-content.msft.png":::
    Usar o **Console** para alterar o conteúdo de um elemento  
:::image-end:::  

Use quaisquer manipulações de DOM JavaScript que você deseja fazer no **Console**.  Para torná-lo mais conveniente, o **Console** vem com alguns métodos auxiliares.  

## <a name="helpful-console-utility-methods"></a>Métodos úteis de utilitário de Console  

Muitos métodos e atalhos de conveniência estão disponíveis para você como [Utilitários de Console.][DevtoolsConsoleUtilities]  Alguns dos métodos são extremamente poderosos e são coisas que você provavelmente escreveu como uma série de `console.log()` instruções no passado.

### <a name="the-power-to-the-"></a>A potência para $

O `$` tem potências especiais **no Console** e você pode se lembrar disso do jQuery.

*   `$_` armazena o resultado do último comando.  Portanto, se você digitar `2 + 2` e selecionar e digitar , o `Enter` `$_` **Console** exibirá você `4` .
*   `$0` to `$4` é uma pilha dos últimos elementos inspecionados é sempre o mais `$0` recente.  Portanto, no exemplo anterior, você acabou de escolher o elemento na ferramenta **Inspector** e digite `$0.textContent = "My Playground"` para obter o mesmo efeito.
*   `$x()` permite que você escolha elementos DOM usando XPATH.
*   `$()` e `$$()` são versões mais curtas de para `document.querySelector()` e `document.querySelectorAll()` .  
    
Por exemplo, o trecho de código a seguir recupera todos os links na página da Web \(como é curto para \) e exibe os links como uma tabela sortível para copiar e colar, por exemplo, em `$$('a')` `document.querySelectorAll('a')` Excel.

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Obter todos os links na página da Web e exibir o resultado como uma tabela" lightbox="../media/console-dom-get-all-links.msft.png":::
    Obter todos os links na página da Web e exibir o resultado como uma tabela  
:::image-end:::  

No entanto, se você não quiser exibir as informações, mas quiser agarrá-la como dados.  O `$$('a')` atalho fornece os links de âncora e todas as propriedades para cada uma delas.  O problema é que você só deseja os links e o texto relacionado.  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="O atalho $$ retorna muitas informações" lightbox="../media/console-dom-too-much-link-information.msft.png":::
    O `$$` atalho retorna informações demais  
:::image-end:::  

O `$$` atalho tem um recurso extra interessante.  Em vez de retornar uma forma `NodeList` pura como , o atalho fornece todos os `document.querySelectorAll()` `$$` `Array` métodos.  Use `map()` o método para reduzir as informações ao que você precisa.  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

O trecho de código retorna uma Matriz de todos os links como objetos `url` com e `text` propriedades.  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Usar mapa em $$ para filtrar informações até o mínimo" lightbox="../media/console-dom-filter-link-data.msft.png":::
    Usar o mapa para `$$` filtrar informações até o mínimo  
:::image-end:::  

Você ainda não terminou, vários links são links internos para a página da Web ou têm texto vazio.  Use o método filter para se livrar dos links internos.  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Obter os links que não estão vazios e são externos" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    Obter os links que não estão vazios e são externos  
:::image-end:::  

Conforme exibido no início da página da Web, você também pode alterar esses elementos.  Por exemplo, o trecho de código a seguir cria uma borda verde em torno de todos os links externos:

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Para realçar todos os links externos, adicione uma borda verde ao redor de cada" lightbox="../media/console-dom-highlight-links.msft.png":::
    Para realçar todos os links externos, adicione uma borda verde ao redor de cada  
:::image-end:::  

Em vez de escrever JavaScript complexo para filtrar resultados, use o poder dos seletores CSS.  

Para criar uma tabela e informações para todas as imagens na página da Web que não são imagens em `src` `alt` linha, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Digite ou copie e copie o trecho de código a seguir.  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Para escolher elementos, use um seletor CSS complexo" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    Para escolher elementos, use um seletor CSS complexo  
:::image-end:::  

Pronto para um exemplo ainda mais complexo?  As páginas da Web HTML geradas a partir da marcação, como este artigo, têm valores de ID automáticos para cada título para permitir que você vincule profundamente essa seção.  Por exemplo, uma `# New features` alteração para `<h1 id="new-features">New features</h1>` .  

Para listar todos os títulos automáticos para copiar e colar, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Digite ou copie e copie o trecho de código a seguir.  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

O resultado é o texto que contém conteúdo para cada título seguido pela URL completa que aponta para ele.  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Obter todos os títulos e AS URLs geradas na página da Web" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    Obter todos os títulos e AS URLs geradas na página da Web  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a>Limpar com limpar e copiar

Ao desenvolver no **Console,** as coisas podem ficar confusas.  Você pode achar frustrante tentar escolher resultados enquanto copia e colar.  Os dois métodos utilitários a seguir ajudam você.  

*   `copy()` copia o que você der à área de transferência.  O `copy()` método é especialmente útil quando você o mistura com o que copia o último `$_` resultado.
*   `clear()` limpa o **Console**.

### <a name="read-and-monitor-events"></a>Ler e monitorar eventos

Dois outros métodos utilitários interessantes de **Console** lidam com o tratamento de eventos.

*   `getEventListeners(node)` lista todos os ouvintes de eventos de um nó.
*   `monitorEvents(node, events)` monitora e registra os eventos que ocorrem em um nó.

Para listar todos os ouvintes de eventos atribuídos ao primeiro formulário na página da Web, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Digite ou copie e copie o trecho de código a seguir.  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Obter todos os ouvintes de eventos para o primeiro formulário na página da Web" lightbox="../media/console-dom-get-form-events.msft.png":::
    Obter todos os ouvintes de eventos para o primeiro formulário na página da Web  
:::image-end:::  

Quando você monitora, você recebe uma notificação no **Console** sempre que algo muda para os elementos especificados.  Você define os eventos que deseja escutar como um segundo parâmetro.  É importante que você defina os eventos que deseja monitorar, caso contrário, qualquer evento que aconteça com o elemento será relatado.

Para receber uma notificação no **Console** sempre que rolar, resize a janela ou quando o usuário digita no formulário de pesquisa, conclua as seguintes ações.  

1.  Abra o **Console**.  
1.  Digite ou copie e copie o trecho de código a seguir.  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="Console exibe cada evento de rolagem que acontece na Janela" lightbox="../media/console-dom-monitor-events.msft.png":::
    **Console** exibe cada evento de rolagem que acontece na Janela  
:::image-end:::  

Para registrar qualquer ação de chave no elemento escolhido no momento, concentre-se no formulário de pesquisa no header e selecione algumas teclas.  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="Console exibe eventos de keyup que ocorrem no formulário" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    **Console** exibe `keyup` eventos que ocorrem no formulário  
:::image-end:::  

Para impedi-lo, remova o monitoramento definido usando o trecho de código a seguir.  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a>Reutilizar scripts de manipulação dom

Você pode achar útil manipular o DOM a partir do **Console**.  Em breve, você poderá executar as limitações do **Console** como uma plataforma de desenvolvimento.  A boa notícia é que a [ferramenta Sources][DevtoolsSourcesIndex] no DevTools oferece um ambiente de desenvolvimento totalmente em destaque.  Na ferramenta **Fontes,** você pode concluir as seguintes ações.  

*   Armazene seus scripts para **o Console** [como trechos de código.][DevToolsJavascriptSnippets]  
*   Execute os scripts em uma página da Web usando um atalho de teclado ou o editor.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console como um ambiente JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Logs na ferramenta console | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página com Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSourcesIndex]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  
