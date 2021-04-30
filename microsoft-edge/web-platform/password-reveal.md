---
description: Fornece orientações sobre como personalizar a exibição do botão de revelação de senha
title: Personalizar o botão revelar senha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web, revelação de senha, ícone do olho
ms.openlocfilehash: 93f618d28e5fa2f16dda87b4122a097ef40618c9
ms.sourcegitcommit: 1f0b2534b51417bb19d05945fea54ddad977e88f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/29/2021
ms.locfileid: "11526155"
---
# <a name="customize-the-password-reveal-button"></a><span data-ttu-id="7d5a5-104">Personalizar o botão revelar senha</span><span class="sxs-lookup"><span data-stu-id="7d5a5-104">Customize the password reveal button</span></span>  

<span data-ttu-id="7d5a5-105">O `password` tipo de entrada no Microsoft Edge inclui um controle de **revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="7d5a5-106">Um usuário pode escolher o botão **de entrada de** senha para revelar o campo **senha.**</span><span class="sxs-lookup"><span data-stu-id="7d5a5-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="7d5a5-107">O campo **senha revelada** ajuda o usuário a verificar se a senha está corretamente.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="7d5a5-108">Depois que um usuário \*\*\*\* tiver inserido texto no \*\*\*\* campo senha, um usuário poderá escolher o botão de revelação de senha ou selecionar para alternar a `Alt` + `F8` visibilidade da entrada.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7d5a5-109">Um **campo** de senha com pontos ocultando os caracteres inseridos por um usuário.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="7d5a5-110">O **botão de** revelação de senha aparece à direita do campo de **senha.**</span><span class="sxs-lookup"><span data-stu-id="7d5a5-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="7d5a5-112">O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha</span><span class="sxs-lookup"><span data-stu-id="7d5a5-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="7d5a5-113">Alterne o **botão de** revelação de senha para alterar o ícone do olho para um ícone de olho com uma barra através dele e para revelar o texto da senha original.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="O ícone em forma de olho tem uma barra nele e o texto de senha original é exibido" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="7d5a5-115">O ícone em forma de olho tem uma barra nele e o texto de senha original é exibido</span><span class="sxs-lookup"><span data-stu-id="7d5a5-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7d5a5-116">Por padrão, o **botão de** revelação de senha insere no DOM sombra de todos os elementos HTML com o conjunto `input` como `type` `"password"` .</span><span class="sxs-lookup"><span data-stu-id="7d5a5-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="7d5a5-117">A partir do Microsoft Edge Versão 87, os usuários ou [empresas][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] podem desabilitar esse recurso globalmente.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="7d5a5-118">Você, web designers e desenvolvedores, deve esperar que a maioria dos usuários do Microsoft Edge tenha a experiência padrão.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <a name="remove-the-password-reveal-control"></a><span data-ttu-id="7d5a5-119">Remover o controle de revelação de senha</span><span class="sxs-lookup"><span data-stu-id="7d5a5-119">Remove the password reveal control</span></span>  

<span data-ttu-id="7d5a5-120">Você pode remover completamente o **botão de revelação** de senha direcionando o `::-ms-reveal` pseudo elemento.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="7d5a5-121">No entanto, você deve considerar tirar proveito do botão de **revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="7d5a5-122">O botão **de revelação de** senha nativa tem medidas [de segurança importantes internas](#visibility-of-the-control) no comportamento.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <a name="customize-the-control-style"></a><span data-ttu-id="7d5a5-123">Personalizar o estilo de controle</span><span class="sxs-lookup"><span data-stu-id="7d5a5-123">Customize the control style</span></span>  

<span data-ttu-id="7d5a5-124">Em vez de remover totalmente o controle, você pode, em vez disso, modificar o estilo do botão de revelação de senha para melhor corresponder à linguagem visual do site. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7d5a5-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="7d5a5-125">O trecho a seguir fornece um exemplo desse estilo.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="7d5a5-126">Lembre-se das seguintes coisas ao estilo do botão **de revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="7d5a5-127">O ícone do olho é implementado como uma imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="7d5a5-128">Para adicionar uma cor \*\*\*\* de plano de fundo ao botão de revelação de senha, use a propriedade CSS `background-color` em vez da propriedade `background` shorthand.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="7d5a5-129">Você pode ajustar o tamanho e a escala do botão **revelar senha.**</span><span class="sxs-lookup"><span data-stu-id="7d5a5-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="7d5a5-130">O navegador oculta qualquer estouro fora dos limites do controle de entrada de senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="7d5a5-131">Atualmente, nenhum seletor de estado está disponível para estilizou o estado alternado do botão de **revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <a name="visibility-of-the-control"></a><span data-ttu-id="7d5a5-132">Visibilidade do controle</span><span class="sxs-lookup"><span data-stu-id="7d5a5-132">Visibility of the control</span></span>  

<span data-ttu-id="7d5a5-133">O **botão de revelação** de senha não estará disponível até que o usuário insira texto no **campo senha.**</span><span class="sxs-lookup"><span data-stu-id="7d5a5-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="7d5a5-134">Para ajudar a manter a entrada de senha do usuário segura, o navegador suprime o botão nos cenários a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="7d5a5-135">Se o foco se afastar do campo **senha,** o navegador removerá o botão **de revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="7d5a5-136">Se os scripts modificarem o campo **de** senha, o navegador removerá o botão **de revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  

<span data-ttu-id="7d5a5-137">Se o **botão de revelação** de senha for \*\*\*\* removido, \*\*\*\* o usuário deverá excluir o conteúdo do campo de senha antes que o botão de revelação de senha seja exibido novamente.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-137">If the **password reveal** button is removed, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span> <span data-ttu-id="7d5a5-138">Esse comportamento impede que alguém faz um pequeno ajuste para exibir a senha, caso o usuário se afaste de um dispositivo desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-138">This behavior prevents someone from making a minor adjustment to display the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="7d5a5-139">O **botão de revelação** de senha não estará disponível se **o** campo de senha for automaticamente contabilizados usando o gerenciador de senhas.</span><span class="sxs-lookup"><span data-stu-id="7d5a5-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Políticas | Microsoft Docs"  
