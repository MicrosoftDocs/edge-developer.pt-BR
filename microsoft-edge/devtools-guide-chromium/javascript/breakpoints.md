---
description: Saiba mais sobre as maneiras como você pode pausar seu código no Microsoft Edge DevTools.
title: Como pausar um código com pontos de interrupção no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 95aba99c2cfe87f26704faa20964ace5d2abdf51
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992803"
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







# Como pausar um código com pontos de interrupção no Microsoft Edge DevTools   



Use pontos de interrupção para pausar o código JavaScript.  Este guia explica cada tipo de ponto de interrupção que está disponível no DevTools, bem como quando usar e como definir cada tipo.  Para um tutorial prático do processo de depuração, consulte [introdução à depuração de JavaScript no Microsoft Edge devtools][DevtoolsJavascriptIndex].  

## Visão geral de quando usar cada tipo de ponto de interrupção   

O tipo mais conhecido de ponto de interrupção é linha de código.  Mas os pontos de interrupção de linha de código podem ser ineficientemente definidos, especialmente se você não souber exatamente onde procurar ou se estiver trabalhando com uma grande codebase.  Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.  

| Tipo de ponto de interrupção | Use isso quando desejar pausar...  |  
|:--- |:--- |  
| [Linha de código](#line-of-code-breakpoints) | Em uma região de código exata.  |  
| [Linha de código condicional](#conditional-line-of-code-breakpoints) | Em uma região de código exata, mas somente quando alguma outra condição for verdadeira.  |  
| [DOM](#dom-change-breakpoints) | No código que altera ou remove um nó DOM específico ou os filhos.  |  
| [XHR](#xhrfetch-breakpoints) | Quando uma URL XHR contém um padrão de cadeia de caracteres.  |  
| [Ouvinte de eventos](#event-listener-breakpoints) | No código que é executado após um evento, como `click` , é executado.  |  
| [Extremamente](#exception-breakpoints) | Na linha de código que está lançando uma exceção capturada ou não capturada.  |  
| [Função](#function-breakpoints) | Sempre que um comando, função ou método específico é executado.  |  

## Pontos de interrupção de linha do código   

Use um ponto de interrupção de linha de código quando souber a região exata de código que você precisa investigar.  O DevTools sempre pausa antes da execução desta linha de código.  

Para definir um ponto de interrupção de linha de código no DevTools:  

1.  Clique na guia **fontes** .  
1.  Abra o arquivo que contém a linha de código que você deseja quebrar.  
1.  Vá para a linha de código.  
1.  À esquerda da linha de código está a coluna número da linha.  Clique nela.  Um ícone vermelho é exibido ao lado da coluna número da linha.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha do código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Um ponto de interrupção de linha do código  
    :::image-end:::  
    
### Pontos de interrupção de linha de código no código   

Execute o `debugger` método do seu código para pausar na linha.  Isso equivale a um [ponto de interrupção de linha de código](#line-of-code-breakpoints), exceto pelo fato de o ponto de interrupção ser definido no seu código, não na interface do usuário do devtools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### Pontos de interrupção de linha de código condicionais   

Use um ponto de interrupção de linha de código condicional quando souber a região exata do código que você precisa investigar, mas deseja pausar somente quando outra condição for verdadeira.  

Para definir um ponto de interrupção de linha de código condicional:  

1.  Clique na guia **fontes** .  
1.  Abra o arquivo que contém a linha de código que você deseja quebrar.  
1.  Vá para a linha de código.  
1.  À esquerda da linha de código está a coluna número da linha.  Clique com o botão direito do mouse no número da linha.  
1.  Selecione **Adicionar ponto de interrupção condicional**.  Uma caixa de diálogo é exibida abaixo da linha de código.  
1.  Insira sua condição na caixa de diálogo.  
1.  Pressione `Enter` para ativar o ponto de interrupção.  Um ícone próximo à coluna número da linha.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Um ponto de interrupção de linha de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Um ponto de interrupção de linha de código condicional  
    :::image-end:::  
    
### Gerenciar pontos de interrupção de linha de código   

Use o painel **pontos de interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="O painel pontos de interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   O painel **pontos de interrupção**  
:::image-end:::  

*   Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.  
*   Clique com o botão direito do mouse em uma entrada para remover esse ponto de interrupção.  
*   Clique com o botão direito do mouse em qualquer lugar no painel **pontos de interrupção** para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.  Desabilitar todos os pontos de interrupção é equivalente a desmarcar cada um deles.  A desativação de todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes da reativação de cada um.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Pontos de interrupção desativados no painel pontos de interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Pontos de interrupção desativados no painel **pontos de interrupção**  
    :::image-end:::  
    
## Alterar o DOM dos pontos de interrupção   

Use um ponto de interrupção de alteração DOM quando desejar pausar no código que altera um nó DOM ou filhos.  

Para definir um ponto de interrupção de alteração DOM:  

1.  Clique na guia **elementos** .  
1.  Vá para o elemento no qual você deseja definir o ponto de interrupção.  
1.  Clique com o botão direito do mouse no elemento.  
1.  Passe o mouse sobre a **pausa**e, em seguida, selecione **modificações de subárvore**, **modificações de atributo**ou remoção de **nó**.  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="O menu de contexto para a criação de um ponto de interrupção de alteração DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       O menu de contexto para a criação de um ponto de interrupção de alteração DOM  
    :::image-end:::  
    
### Tipos de pontos de interrupção de alteração DOM   

*   **Modificações em subárvores**.  Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.  Não disparado em alterações de atributo de nó filho ou em qualquer alteração do nó atualmente selecionado.  
*   **Modificações de atributos**: disparadas quando um atributo é adicionado ou removido no nó selecionado atualmente ou quando um valor de atributo é alterado.  
*   **Remoção de nó**: disparada quando o nó selecionado no momento é removido.  
    
## Pontos de interrupção XHR/Fetch   

Use um ponto de interrupção XHR quando você quiser interromper quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.  DevTools pausa na linha de código em que XHR executa o `send()` método.  

> [!NOTE]
> Esse recurso também funciona com solicitações de [busca de API][MDNFetchApi] .  

Um exemplo de quando isso é útil é quando você vê que sua página está solicitando uma URL incorreta, e você deseja localizar rapidamente o código-fonte do AJAX ou de busca que está causando a solicitação incorreta.  

Para definir um ponto de interrupção XHR:  

1.  Clique na guia **fontes** .  
1.  Expanda o painel **pontos de interrupção XHR** .  
1.  Clique em **Adicionar ponto de interrupção**.  
1.  Digite a cadeia de caracteres na qual você deseja interromper.  DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.  
1.  Pressione `Enter` para confirmar.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Criar um ponto de interrupção XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Criar um ponto de interrupção XHR  
    :::image-end:::  
    
## Pontos de interrupção do ouvinte de eventos 

Use pontos de interrupção de ouvinte de eventos quando desejar pausar no código de ouvinte de eventos que é executado após a disparação de um evento.  Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.  

1.  Clique na guia **fontes** .  
1.  Expanda o painel **pontos de interrupção de ouvinte de eventos** .  DevTools mostra uma lista de categorias de eventos, como **animação**.  
1.  Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expandir a categoria e verificar um evento específico.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Criar um ponto de interrupção de ouvinte de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Criar um ponto de interrupção de ouvinte de eventos  
    :::image-end:::  
    
## Pontos de interrupção de exceção   

Use pontos de interrupção de exceção quando desejar pausar na linha de código que está lançando uma exceção capturada ou não percebida.  

1.  Clique na guia **fontes** .  
1.  Clique em **Pausar nas exceções** \ ( ![ Pausar exceções ][ImagePauseOnExceptionsIcon] \).  O ícone fica azul quando habilitado.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="O botão Pausar exceções" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       O botão **Pausar exceções**  
    :::image-end:::  
    
1.  **Opcional**.  Marque a caixa de seleção **Pausar exceções capturadas** se você também quiser pausar em exceções capturadas, além de não capturadas.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausado em uma exceção não capturada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Pausado em uma exceção não capturada  
    :::image-end:::  
    
## Pontos de interrupção de função   

Execute o `debug(method)` método, onde `method` é o comando, a função ou o método que você deseja depurar, quando desejar pausar sempre que uma função específica for executada.  Você pode inserir `debug()` no seu código (como uma `console.log()` instrução) ou executar o método no console do devtools.  `debug()` equivale a definir um [ponto de interrupção de linha do código](#line-of-code-breakpoints) na primeira linha da função.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### Verifique se a função de destino está em escopo   

DevTools lança uma `ReferenceError` se a função que você deseja depurar não está em escopo.  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

Garantir que a função de destino está em escopo é difícil se você estiver executando o `debug()` método do console devtools.  Aqui está uma estratégia:  

1.  Defina um [ponto de interrupção de linha do código](#line-of-code-breakpoints) em um local onde a função esteja no escopo.
1.  Disparar o ponto de interrupção.  
1.  Execute o `debug()` método no console devtools enquanto o código ainda está pausado no ponto de interrupção da linha de código.  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introdução à depuração JavaScript no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar API | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
