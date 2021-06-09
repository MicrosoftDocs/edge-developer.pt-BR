---
description: Analisando a falta de suporte ao teclado em um formulário que usa o elemento div com a ferramenta Inspect e a guia Ouvintes de Eventos.
title: Analisar o suporte ao teclado em formulários usando o DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 16ec030ed433fc24d3b2b88bfb423a2479996dfe
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597210"
---
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a>Analisar o suporte ao teclado em formulários usando o DevTools

Este artigo usa a **ferramenta Inspecionar** e a guia **Ouvintes** de Eventos para analisar a falta de suporte ao teclado em uma página de demonstração que tem botões que usam o `div` elemento.

No formulário **Doar,** a quantidade de botões e o **botão** Doar não funciona com um teclado.  A depuração do formulário de doação requer a compreensão do motivo pelo qual a falta de estilo de foco não é sinalizada como um problema com ferramentas de teste automáticas, como a **ferramenta Issues.**  Neste exemplo, os botões são implementados usando elementos, que não são reconhecidos por essas ferramentas como `div` um controle em um formulário.

Para usar a ferramenta Inspecionar e a guia Ouvintes de Eventos para analisar a falta de suporte ao teclado na página de demonstração:

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.
    
1.  Selecione o **botão Inspecionar** \( Inspecionar ícone \) no canto superior esquerdo do DevTools para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).

1.  Passe o mouse sobre **os botões 50**, **100**e **200** doações.  A ferramenta Inspecionar aparece na página da Web, como uma sobreposição.  A **linha focalizada** no teclado da sobreposição Inspecionar mostra que nenhum dos botões de quantidade de doação é acessível ao teclado, conforme indicado por um círculo cinza com linha diagonal.  Os botões não têm nome e têm uma função de porque são elementos, o que significa que os botões não são acessíveis à `generic` `div` tecnologia assistida.

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Inspecionar os botões do formulário mostra que eles não são acessíveis ao teclado" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        Inspecionar os botões do formulário mostra que eles não são acessíveis ao teclado
    :::image-end:::
    
1.  Quando a **ferramenta Inspecionar** estiver ativa, na página da Web, selecione a caixa de texto **Outra** entrada, acima do **botão Doar.**  A **ferramenta Elements** é aberta, mostrando a árvore DOM para a página da Web.  O elemento `<input id="freedonation" class="smallinput">` está selecionado.

    ```html
    <div class="donationrow">
        <div class="donationbutton">50</div>
        <div class="donationbutton">100</div>
        <div class="donationbutton">200</div>
    </div>
    <div class="donationrow">
        <label for="freedonation">Other</label>
        <input id="freedonation" class="smallinput">
    </div>
    <div class="donationrow">
        <div class="submitbutton">Donate</div>
    </div>
    ```

    O uso dos elementos e na caixa de texto Outro é válido, o que significa que o rótulo Other está vinculado corretamente à caixa de texto `label` `input` de entrada. **** ****  A `input` caixa de texto também é acessível ao teclado.  O restante da marcação do formulário são elementos, que são fáceis de `div` estilo, mas não têm significado semântico.

    <!-- 2. Elements tool: Event Listeners tab -->

    A funcionalidade do formulário é criada com JavaScript e você pode testar isso verificando a guia **Ouvintes** de Eventos, da seguinte maneira.

1.  Com o elemento ainda selecionado na árvore DOM, selecione a guia Ouvintes de Eventos à direita da guia Estilos e expanda `<input id="freedonation" class="smallinput">` o ouvinte de **** **** `click` eventos.

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="A ferramenta Ouvintes de eventos mostrando onde o JavaScript é que faz o formulário funcionar" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        A ferramenta Ouvintes de eventos mostrando onde o JavaScript é que faz o formulário funcionar
    :::image-end:::

1.  Selecione o `buttons.js:18` link.  A **ferramenta Sources** é aberta, mostrando o JavaScript aplicado.

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="O JavaScript responsável pela funcionalidade do formulário de doação, mostrado na ferramenta Sources" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        O JavaScript responsável pela funcionalidade do formulário de doação, mostrado na ferramenta Sources
    :::image-end:::

```javascript
donations.addEventListener('click', e => {
  let t = e.target;
  if (t.classList.contains('donationbutton')) {
    if (currentbutton) { currentbutton.classList.remove('current'); }
    t.classList.add('current');
    currentbutton = t;
    e.preventDefault();
  }
  if (t.classList.contains('submitbutton')) {
    alert('Thanks for your donation!')
  } 
})
```

Usar um evento para ler os botões é uma boa prática, pois um evento dispara tanto no ponteiro do mouse quanto `click` `click` na interação do teclado.  No entanto, como um elemento não é acessível ao teclado e esse botão Doar é implementado como um elemento ( ), essa funcionalidade JavaScript nunca é executada, a menos que você use um mouse ou outra fonte de um evento, como um botão especial disponível em alguns `div` **** `div` `<div class="submitbutton">Donate</div>` `click` teclados.

Este é um exemplo clássico em que o JavaScript foi adicionado para criar a funcionalidade que `button` os elementos fornecem de forma nativa.  Simular a funcionalidade de botões com elementos `div` acabou produzindo uma experiência inacessível.


## <a name="see-also"></a>Consulte também

*  [Visão geral dos testes de acessibilidade usando o DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
