---
description: Fornece orientações sobre como personalizar a exibição do botão revelar senha
title: Personalizar o botão revelar senha
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma web, revelação de senha, ícone de olho
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327705"
---
# <span data-ttu-id="e33a9-104">Personalizar o botão revelar senha</span><span class="sxs-lookup"><span data-stu-id="e33a9-104">Customize the password reveal button</span></span>  

<span data-ttu-id="e33a9-105">O `password` tipo de entrada no Microsoft Edge inclui um controle de **revelação de** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="e33a9-106">Um usuário pode escolher o botão **de entrada de** senha para revelar o campo **de** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="e33a9-107">O campo **de senha** revelado ajuda o usuário a verificar se a senha está corretamente.</span><span class="sxs-lookup"><span data-stu-id="e33a9-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="e33a9-108">Depois que um usuário inserir texto no **campo** \*\*\*\* de senha, um usuário poderá escolher o botão de revelar a senha ou optar por alternar a `Alt` + `F8` visibilidade da entrada.</span><span class="sxs-lookup"><span data-stu-id="e33a9-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e33a9-109">Um **campo** de senha com pontos ocultando os caracteres inseridos por um usuário.</span><span class="sxs-lookup"><span data-stu-id="e33a9-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="e33a9-110">O **botão revelar** senha aparece à direita do campo **de** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="e33a9-112">O ícone em forma de olho aparece ao lado dos pontos que ocultam o texto da senha</span><span class="sxs-lookup"><span data-stu-id="e33a9-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e33a9-113">Alterne o **botão de** revelação de senha para alterar o ícone de olho para um ícone de olho com uma barra através dele e para revelar o texto original da senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="O ícone em forma de olho tem uma barra nele e o texto original da senha é exibido" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="e33a9-115">O ícone em forma de olho tem uma barra nele e o texto original da senha é exibido</span><span class="sxs-lookup"><span data-stu-id="e33a9-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e33a9-116">Por padrão, o **botão de revelar** senha insere no SHADOW DOM de todos os elementos HTML com o conjunto como `input` `type` `"password"` .</span><span class="sxs-lookup"><span data-stu-id="e33a9-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="e33a9-117">A partir da versão 87 do Microsoft Edge, os usuários ou empresas [podem][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] desabilitar esse recurso globalmente.</span><span class="sxs-lookup"><span data-stu-id="e33a9-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="e33a9-118">Você, web designers e desenvolvedores devem esperar que a maioria dos usuários do Microsoft Edge tenha a experiência padrão.</span><span class="sxs-lookup"><span data-stu-id="e33a9-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <span data-ttu-id="e33a9-119">Remover o controle de revelação de senha</span><span class="sxs-lookup"><span data-stu-id="e33a9-119">Remove the password reveal control</span></span>  

<span data-ttu-id="e33a9-120">Você pode remover completamente o **botão de revelar** senha direcionando o pseudo `::-ms-reveal` elemento.</span><span class="sxs-lookup"><span data-stu-id="e33a9-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="e33a9-121">No entanto, você deve considerar tirar proveito do botão **de revelar senha.**</span><span class="sxs-lookup"><span data-stu-id="e33a9-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="e33a9-122">O botão **de revelar senha** nativa tem medidas de segurança importantes [internas](#visibility-of-the-control) ao comportamento.</span><span class="sxs-lookup"><span data-stu-id="e33a9-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <span data-ttu-id="e33a9-123">Personalizar o estilo de controle</span><span class="sxs-lookup"><span data-stu-id="e33a9-123">Customize the control style</span></span>  

<span data-ttu-id="e33a9-124">Em vez de remover totalmente o controle, você pode \*\*\*\* modificar o estilo do botão de revelar senha para melhor corresponder à linguagem visual do site.</span><span class="sxs-lookup"><span data-stu-id="e33a9-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="e33a9-125">O trecho a seguir fornece um exemplo desse estilo.</span><span class="sxs-lookup"><span data-stu-id="e33a9-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="e33a9-126">Lembre-se do seguinte ao estilcar o botão **de revelar a** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="e33a9-127">O ícone de olho é implementado como uma imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="e33a9-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="e33a9-128">Para adicionar uma cor de plano de fundo **ao** botão de revelar senha, use a propriedade CSS em vez da `background-color` propriedade `background` shorthand.</span><span class="sxs-lookup"><span data-stu-id="e33a9-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="e33a9-129">Você pode ajustar o tamanho e a escala do botão revelar **senha.**</span><span class="sxs-lookup"><span data-stu-id="e33a9-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="e33a9-130">O navegador oculta qualquer estouro fora dos limites do controle de entrada de senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="e33a9-131">Atualmente, nenhum seletor de estado está disponível para estilgrafar o estado de alternância do botão de revelação **de** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <span data-ttu-id="e33a9-132">Visibilidade do controle</span><span class="sxs-lookup"><span data-stu-id="e33a9-132">Visibility of the control</span></span>  

<span data-ttu-id="e33a9-133">O **botão de revelar** senha não estará disponível até que o usuário insira texto no campo **de** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="e33a9-134">Para ajudar a manter a entrada de senha do usuário segura, o navegador suprime o botão nos cenários a seguir.</span><span class="sxs-lookup"><span data-stu-id="e33a9-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="e33a9-135">Se o foco se mover para fora do campo **de** senha, o navegador removerá o **botão de revelar senha.**</span><span class="sxs-lookup"><span data-stu-id="e33a9-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="e33a9-136">Se os scripts modificarem **o campo de** senha, o navegador removerá o botão revelar **a** senha.</span><span class="sxs-lookup"><span data-stu-id="e33a9-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="e33a9-137">Se um usuário remover o botão revelar senha, ele \*\*\*\* deverá excluir \*\*\*\* o conteúdo do campo de senha antes que o botão de revelar senha seja exibido novamente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e33a9-137">If a user removes the **password reveal** button, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e33a9-138">Esse recurso impede que alguém faz um ajuste secundário para exibir a senha, caso o usuário saia de um dispositivo desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="e33a9-138">This feature prevents someone from making a minor adjustment to view the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="e33a9-139">O **botão de revelar** senha não estará disponível se o campo de senha for automaticamente preenchimento usando o gerenciador de senhas. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e33a9-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Políticas | Microsoft Docs"  
