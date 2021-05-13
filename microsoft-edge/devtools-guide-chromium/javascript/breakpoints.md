---
description: Saiba mais sobre todas as maneiras de pausar seu código Microsoft Edge DevTools.
title: Como pausar seu código com pontos de interrupção Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: fda536deb7177b933013120fc11b0896acfbbe5c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564172"
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
# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a>Como pausar seu código com pontos de interrupção Microsoft Edge DevTools  

Use pontos de interrupção para pausar seu código JavaScript.  Este artigo explica cada tipo de ponto de interrupção disponível no DevTools, bem como quando usar e como definir cada tipo.

Para obter um tutorial introdutório usando uma página da Web existente, navegue até Introdução à [depuração de JavaScript no Microsoft Edge DevTools][DevtoolsJavascriptIndex].

## <a name="overview-of-when-to-use-each-breakpoint-type"></a>Visão geral de quando usar cada tipo de ponto de interrupção  

O tipo de ponto de interrupção mais conhecido é a linha de código.  Mas pontos de interrupção de linha de código podem ser ineficientes para definir, especialmente se você não sabe exatamente onde procurar ou se estiver trabalhando com uma base de código grande.  Você pode economizar tempo ao depurar sabendo como e quando usar os outros tipos de pontos de interrupção.  

| Tipo de ponto de interrupção | Use isso quando quiser pausar... |  
|:--- |:--- |  
| [Linha de código](#line-of-code-breakpoints) | Em uma região exata do código.  |  
| [Linha de código condicional](#conditional-line-of-code-breakpoints) | Em uma região exata do código, mas somente quando alguma outra condição for verdadeira.  |  
| [DOM](#dom-change-breakpoints) | No código que altera ou remove um nó DOM específico ou os filhos.  |  
| [XHR](#xhrfetch-breakpoints) | Quando uma URL XHR contém um padrão de cadeia de caracteres.  |  
| [Ouvinte de eventos](#event-listener-breakpoints) | No código que é executado após um evento, como `click` , é executado.  |  
| [Exceção](#exception-breakpoints) | Na linha de código que está lançando uma exceção capturada ou não capturada.  |  
| [Função](#function-breakpoints) | Sempre que um comando, função ou método específico é executado.  |  

## <a name="line-of-code-breakpoints"></a>Pontos de interrupção de linha de código  

Use um ponto de interrupção de linha de código quando você conhecer a região exata do código que precisa investigar.  O DevTools sempre pausa antes que essa linha de código seja executado.  

Para definir um ponto de interrupção de linha de código no DevTools:  

1.  Escolha a **ferramenta Fontes.**  
1.  Abra o arquivo que contém a linha de código na qual você deseja quebrar.  
1.  Vá para a linha de código.  
1.  À esquerda da linha de código está a coluna de número de linha.  Escolha-o.  Um ícone vermelho aparece ao lado da coluna de número de linha.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Um ponto de interrupção de linha de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Um ponto de interrupção de linha de código  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a>Pontos de interrupção de linha de código em seu código  

Execute o `debugger` método do código para pausar nessa linha.  Isso é equivalente [a](#line-of-code-breakpoints)um ponto de interrupção de linha de código , exceto que o ponto de interrupção está definido em seu código, não na interface do usuário de DevTools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a>Pontos de interrupção de linha de código condicional  

Use um ponto de interrupção de linha de código condicional quando você conhecer a região exata do código que precisa investigar, mas deseja pausar somente quando alguma outra condição for verdadeira.  

Para definir um ponto de interrupção de linha de código condicional:  

1.  Escolha a **ferramenta Fontes.**  
1.  Abra o arquivo que contém a linha de código na qual você deseja quebrar.  
1.  Vá para a linha de código.  
1.  À esquerda da linha de código está a coluna de número de linha.  Passe o mouse no número da linha e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Escolha **Adicionar ponto de interrupção condicional**.  Uma caixa de diálogo é exibida abaixo da linha de código.  
1.  Insira sua condição na caixa de diálogo.  
1.  Selecione `Enter` para ativar o ponto de interrupção.  Um ícone ao lado da coluna de número de linha.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Um ponto de interrupção de linha de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Um ponto de interrupção de linha de código condicional  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a>Gerenciar pontos de interrupção de linha de código  

Use o **painel Pontos de Interrupção** para desabilitar ou remover pontos de interrupção de linha de código de um único local.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="O painel Pontos de Interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   O **painel Pontos de** Interrupção  
:::image-end:::  

*   Marque a caixa de seleção ao lado de uma entrada para desabilitar esse ponto de interrupção.  
*   Passe o mouse em uma entrada e abra o menu contextual \(clique com o botão direito do mouse\) para remover esse ponto de interrupção.  
*   Passe o **** mouse em qualquer lugar no painel Pontos de Interrupção e abra o menu contextual \(clique com o botão direito do mouse\) para desativar todos os pontos de interrupção, desabilitar todos os pontos de interrupção ou remover todos os pontos de interrupção.  Desabilitar todos os pontos de interrupção equivale a desmarcar cada um deles.  Desativar todos os pontos de interrupção instrui o DevTools a ignorar todos os pontos de interrupção de linha de código, mas também manter o estado habilitado para que cada um esteja no mesmo estado de antes quando você reativar cada um deles.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Pontos de interrupção desativados no painel Pontos de Interrupção" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Pontos de interrupção desativados no painel **Pontos de** Interrupção  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a>Pontos de interrupção de alteração dom  

Use um ponto de interrupção de alteração dom quando quiser pausar o código que altera um nó DOM ou os filhos.  

Para definir um ponto de interrupção de alteração dom:  

1.  Escolha a **ferramenta Elementos.**  
1.  Vá para o elemento no qual você deseja definir o ponto de interrupção.  
1.  Passe o mouse no elemento e abra o menu contextual \(clique com o botão direito do mouse\).  
1.  Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="O menu de contexto para criar um ponto de interrupção de alteração dom" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       O menu de contexto para criar um ponto de interrupção de alteração dom  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a>Tipos de pontos de interrupção de alteração dom  

*   **Modificações de subárvore**.  Disparado quando um filho do nó selecionado no momento é removido ou adicionado, ou o conteúdo de um filho é alterado.  Não acionada em alterações de atributo de nó filho ou em quaisquer alterações no nó selecionado no momento.  
*   **Modificações de atributos**: disparado quando um atributo é adicionado ou removido no nó selecionado no momento ou quando um valor de atributo é modificado.  
*   **Remoção do**nó : disparado quando o nó selecionado no momento é removido.  
    
## <a name="xhrfetch-breakpoints"></a>Pontos de interrupção XHR/Fetch  

Use um ponto de interrupção XHR quando quiser quebrar quando a URL de solicitação de um XHR contiver uma cadeia de caracteres especificada.  O DevTools pausa na linha de código em que o XHR executa o `send()` método.  

> [!NOTE]
> Esse recurso também funciona com [solicitações de API de][MDNFetchApi] Busca.  

Um exemplo de quando isso é útil é quando sua página da Web está solicitando uma URL incorreta e você deseja encontrar rapidamente o código-fonte AJAX ou Fetch que está causando a solicitação incorreta.  

Para definir um ponto de interrupção XHR:  

1.  Escolha a **ferramenta Fontes.**  
1.  Expanda o **painel Pontos de Interrupção XHR.**  
1.  Escolha **Adicionar ponto de interrupção**.  
1.  Insira a cadeia de caracteres na qual você deseja quebrar.  O DevTools pausa quando essa cadeia de caracteres está presente em qualquer lugar em uma URL de solicitação XHR.  
1.  Selecione `Enter` para confirmar.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Criar um ponto de interrupção XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Criar um ponto de interrupção XHR  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a>Pontos de interrupção do ouvinte de eventos  

Use pontos de interrupção do ouvinte de eventos quando quiser pausar o código do ouvinte de eventos que é executado após um evento ser disparado.  Você pode selecionar eventos específicos, como `click` , ou categorias de eventos, como todos os eventos do mouse.  

1.  Escolha a **ferramenta Fontes.**  
1.  Expanda o **painel Pontos de Interrupção do Ouvinte de** Eventos.  DevTools mostra uma lista de categorias de eventos, como **Animação**.  
1.  Verifique uma dessas categorias para pausar sempre que qualquer evento dessa categoria for acionado ou expanda a categoria e verifique um evento específico.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Criar um ponto de interrupção do ouvinte de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Criar um ponto de interrupção do ouvinte de eventos  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a>Pontos de interrupção de exceção  

Use pontos de interrupção de exceção quando quiser pausar na linha de código que está lançando uma exceção capturada ou não capturada.  

1.  Escolha a **ferramenta Fontes.**  
1.  Escolha **Pausar em exceções** \( Pause on ![ exceptions ](../media/pause-on-exceptions-icon.msft.png) \).  O ícone fica azul quando habilitado.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="O botão Pausar exceções" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       O **botão Pausar exceções**  
    :::image-end:::  
    
1.  **Opcional**.  Marque a **caixa de seleção Pausar** Exceções Capturadas se você também quiser pausar em exceções capturadas, além de exceções não capturadas.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausada em uma exceção não acatada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Pausada em uma exceção não acatada  
    :::image-end:::  
    
## <a name="function-breakpoints"></a>Pontos de interrupção de função  

Execute o método, onde está o comando, a função ou o método que você deseja depurar, quando quiser pausar sempre que `debug(method)` uma função específica for `method` executado.  Você pode inserir em seu código (como uma instrução) ou executar `debug()` o método no Console de `console.log()` DevTools.  `debug()` equivale a definir um [ponto de interrupção de](#line-of-code-breakpoints) linha de código na primeira linha da função.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a>Certifique-se de que a função de destino está no escopo  

DevTools lança um se a `ReferenceError` função que você deseja depurar não estiver no escopo.  

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

A garantia de que a função de destino está no escopo é complicada se você estiver executando o método no `debug()` Console de DevTools.  Aqui está uma estratégia:  

1.  De definir [um ponto de interrupção de linha de código](#line-of-code-breakpoints) em algum lugar onde a função está no escopo.
1.  Acionar o ponto de interrupção.  
1.  Execute o `debug()` método no Console de DevTools enquanto o código ainda está pausado no ponto de interrupção de linha de código.  
    
## <a name="related-articles"></a>Artigos relacionados

*   [Use os recursos de depurador][DevtoolsJavascriptReference] - Usando a interface do usuário do depurador na **ferramenta Sources.**
*   [Introdução à depuração do JavaScript no Microsoft Edge DevTools][DevtoolsJavascriptIndex] - Um tutorial introdutório usando uma página da Web existente.
*   [Visão geral da][DevtoolsSourcesIndex] ferramenta Sources - O depurador faz parte da ferramenta **Sources,** que inclui um editor JavaScript.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptReference]: ./reference.md "Use os recursos de depurador | Microsoft Docs"  

[DevtoolsJavascriptIndex]: index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsSourcesIndex]: ../sources/index.md "Visão geral da ferramenta Sources | Microsoft Docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Buscar api | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
