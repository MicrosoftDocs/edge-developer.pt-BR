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
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a><span data-ttu-id="3efc8-104">Analisar o suporte ao teclado em formulários usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="3efc8-104">Analyze keyboard support on forms using the DevTools</span></span>

<span data-ttu-id="3efc8-105">Este artigo usa a **ferramenta Inspecionar** e a guia **Ouvintes** de Eventos para analisar a falta de suporte ao teclado em uma página de demonstração que tem botões que usam o `div` elemento.</span><span class="sxs-lookup"><span data-stu-id="3efc8-105">This article uses the **Inspect** tool and **Event Listeners** tab to analyze the lack of keyboard support on a demo page which has buttons that use the `div` element.</span></span>

<span data-ttu-id="3efc8-106">No formulário **Doar,** a quantidade de botões e o **botão** Doar não funciona com um teclado.</span><span class="sxs-lookup"><span data-stu-id="3efc8-106">On the **Donate** form, the amount buttons and **Donate** button doesn't work with a keyboard.</span></span>  <span data-ttu-id="3efc8-107">A depuração do formulário de doação requer a compreensão do motivo pelo qual a falta de estilo de foco não é sinalizada como um problema com ferramentas de teste automáticas, como a **ferramenta Issues.**</span><span class="sxs-lookup"><span data-stu-id="3efc8-107">Debugging the donation form requires understanding why the lack of focus styling isn't flagged as a problem with automatic testing tools like the **Issues** tool.</span></span>  <span data-ttu-id="3efc8-108">Neste exemplo, os botões são implementados usando elementos, que não são reconhecidos por essas ferramentas como `div` um controle em um formulário.</span><span class="sxs-lookup"><span data-stu-id="3efc8-108">In this example, the buttons are implemented using `div` elements, which are not recognized by these tools as a control on a form.</span></span>

<span data-ttu-id="3efc8-109">Para usar a ferramenta Inspecionar e a guia Ouvintes de Eventos para analisar a falta de suporte ao teclado na página de demonstração:</span><span class="sxs-lookup"><span data-stu-id="3efc8-109">To use the Inspect tool and Event Listeners tab to analyze the lack of keyboard support on the demo page:</span></span>

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  <span data-ttu-id="3efc8-110">Abra a página da Web de [demonstração][DevToolsA11yErrorsDemopage] de teste de acessibilidade em uma nova guia do navegador e selecione **F12** para abrir o DevTools.</span><span class="sxs-lookup"><span data-stu-id="3efc8-110">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>
    
1.  <span data-ttu-id="3efc8-111">Selecione o **botão Inspecionar** \( Inspecionar ícone \) no canto superior esquerdo do DevTools para que o botão seja ![ ](../media/inspect-icon.msft.png) realçado (azul).</span><span class="sxs-lookup"><span data-stu-id="3efc8-111">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="3efc8-112">Passe o mouse sobre **os botões 50**, **100**e **200** doações.</span><span class="sxs-lookup"><span data-stu-id="3efc8-112">Hover over the **50**, **100**, and **200** donation buttons.</span></span>  <span data-ttu-id="3efc8-113">A ferramenta Inspecionar aparece na página da Web, como uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="3efc8-113">The Inspect tool appears on the webpage, as an overlay.</span></span>  <span data-ttu-id="3efc8-114">A **linha focalizada** no teclado da sobreposição Inspecionar mostra que nenhum dos botões de quantidade de doação é acessível ao teclado, conforme indicado por um círculo cinza com linha diagonal.</span><span class="sxs-lookup"><span data-stu-id="3efc8-114">The **keyboard-focusable** row of the Inspect overlay shows that none of the donation amount buttons are keyboard-accessible, as indicated by a gray circle with diagonal line.</span></span>  <span data-ttu-id="3efc8-115">Os botões não têm nome e têm uma função de porque são elementos, o que significa que os botões não são acessíveis à `generic` `div` tecnologia assistida.</span><span class="sxs-lookup"><span data-stu-id="3efc8-115">The buttons have no name, and have a role of `generic` because they are `div` elements, which means that the buttons aren't accessible to assistive technology.</span></span>

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Inspecionar os botões do formulário mostra que eles não são acessíveis ao teclado" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        <span data-ttu-id="3efc8-117">Inspecionar os botões do formulário mostra que eles não são acessíveis ao teclado</span><span class="sxs-lookup"><span data-stu-id="3efc8-117">Inspecting the buttons of the form shows that they aren't keyboard-accessible</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="3efc8-118">Quando a **ferramenta Inspecionar** estiver ativa, na página da Web, selecione a caixa de texto **Outra** entrada, acima do **botão Doar.**</span><span class="sxs-lookup"><span data-stu-id="3efc8-118">When the **Inspect** tool is active, on the webpage, select the **Other** input textbox, above the **Donate** button.</span></span>  <span data-ttu-id="3efc8-119">A **ferramenta Elements** é aberta, mostrando a árvore DOM para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="3efc8-119">The **Elements** tool opens, showing the DOM tree for the webpage.</span></span>  <span data-ttu-id="3efc8-120">O elemento `<input id="freedonation" class="smallinput">` está selecionado.</span><span class="sxs-lookup"><span data-stu-id="3efc8-120">The element `<input id="freedonation" class="smallinput">` is selected.</span></span>

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

    <span data-ttu-id="3efc8-121">O uso dos elementos e na caixa de texto Outro é válido, o que significa que o rótulo Other está vinculado corretamente à caixa de texto `label` `input` de entrada. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3efc8-121">The use of the `label` and `input` elements on the **Other** textbox is valid, which means that the **Other** label is correctly linked with the input textbox.</span></span>  <span data-ttu-id="3efc8-122">A `input` caixa de texto também é acessível ao teclado.</span><span class="sxs-lookup"><span data-stu-id="3efc8-122">The `input` textbox is also keyboard-accessible.</span></span>  <span data-ttu-id="3efc8-123">O restante da marcação do formulário são elementos, que são fáceis de `div` estilo, mas não têm significado semântico.</span><span class="sxs-lookup"><span data-stu-id="3efc8-123">The rest of the form's markup are `div` elements, which are easy to style, but have no semantic meaning.</span></span>

    <!-- 2. Elements tool: Event Listeners tab -->

    <span data-ttu-id="3efc8-124">A funcionalidade do formulário é criada com JavaScript e você pode testar isso verificando a guia **Ouvintes** de Eventos, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3efc8-124">The form's functionality is created with JavaScript, and you can test this by checking the **Event Listeners** tab, as follows.</span></span>

1.  <span data-ttu-id="3efc8-125">Com o elemento ainda selecionado na árvore DOM, selecione a guia Ouvintes de Eventos à direita da guia Estilos e expanda `<input id="freedonation" class="smallinput">` o ouvinte de \*\*\*\* \*\*\*\* `click` eventos.</span><span class="sxs-lookup"><span data-stu-id="3efc8-125">With the element `<input id="freedonation" class="smallinput">` still selected in the DOM tree, select the **Event Listeners** tab to the right of the **Styles** tab, and then expand the `click` event listener.</span></span>

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="A ferramenta Ouvintes de eventos mostrando onde o JavaScript é que faz o formulário funcionar" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        <span data-ttu-id="3efc8-127">A ferramenta Ouvintes de eventos mostrando onde o JavaScript é que faz o formulário funcionar</span><span class="sxs-lookup"><span data-stu-id="3efc8-127">The Event listeners tool showing you where the JavaScript is that makes the form work</span></span>
    :::image-end:::

1.  <span data-ttu-id="3efc8-128">Selecione o `buttons.js:18` link.</span><span class="sxs-lookup"><span data-stu-id="3efc8-128">Select the `buttons.js:18` link.</span></span>  <span data-ttu-id="3efc8-129">A **ferramenta Sources** é aberta, mostrando o JavaScript aplicado.</span><span class="sxs-lookup"><span data-stu-id="3efc8-129">The **Sources** tool opens, showing the applied JavaScript.</span></span>

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="O JavaScript responsável pela funcionalidade do formulário de doação, mostrado na ferramenta Sources" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        <span data-ttu-id="3efc8-131">O JavaScript responsável pela funcionalidade do formulário de doação, mostrado na ferramenta Sources</span><span class="sxs-lookup"><span data-stu-id="3efc8-131">The JavaScript responsible for the donation form's functionality, shown in the Sources tool</span></span>
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

<span data-ttu-id="3efc8-132">Usar um evento para ler os botões é uma boa prática, pois um evento dispara tanto no ponteiro do mouse quanto `click` `click` na interação do teclado.</span><span class="sxs-lookup"><span data-stu-id="3efc8-132">Using a `click` event to read the buttons is good practice, because a `click` event fires both on mouse pointer and keyboard interaction.</span></span>  <span data-ttu-id="3efc8-133">No entanto, como um elemento não é acessível ao teclado e esse botão Doar é implementado como um elemento ( ), essa funcionalidade JavaScript nunca é executada, a menos que você use um mouse ou outra fonte de um evento, como um botão especial disponível em alguns `div` \*\*\*\* `div` `<div class="submitbutton">Donate</div>` `click` teclados.</span><span class="sxs-lookup"><span data-stu-id="3efc8-133">However, because a `div` element isn't keyboard-accessible, and this **Donate** button is implemented as a `div` element (`<div class="submitbutton">Donate</div>`), this JavaScript functionality never runs unless you use a mouse or another source of a `click` event, such as a special button available on some keyboards.</span></span>

<span data-ttu-id="3efc8-134">Este é um exemplo clássico em que o JavaScript foi adicionado para criar a funcionalidade que `button` os elementos fornecem de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="3efc8-134">This is a classic example where JavaScript was added to create functionality that `button` elements provide natively.</span></span>  <span data-ttu-id="3efc8-135">Simular a funcionalidade de botões com elementos `div` acabou produzindo uma experiência inacessível.</span><span class="sxs-lookup"><span data-stu-id="3efc8-135">Simulating the functionality of buttons with `div` elements ended up producing an inaccessible experience.</span></span>


## <a name="see-also"></a><span data-ttu-id="3efc8-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3efc8-136">See also</span></span>

*  [<span data-ttu-id="3efc8-137">Visão geral dos testes de acessibilidade usando o DevTools</span><span class="sxs-lookup"><span data-stu-id="3efc8-137">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3efc8-138">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3efc8-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
