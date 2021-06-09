---
description: Force Microsoft Edge DevTools no modo de Visualização do Esquema de Cores.
title: Forçar Microsoft Edge DevTools no modo de Visualização de Esquema de Cores (CSS prefere Esquema de Cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597062"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="382d2-104">Simulação de esquema de cores escuro ou claro</span><span class="sxs-lookup"><span data-stu-id="382d2-104">Dark or light color scheme simulation</span></span>  

<span data-ttu-id="382d2-105">Muitos sistemas operacionais têm uma maneira de exibir qualquer aplicativo em cores mais escuras ou mais claras.</span><span class="sxs-lookup"><span data-stu-id="382d2-105">Many operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="382d2-106">Ter um produto Web com um tema claro em um sistema operacional de modo escuro é irritante e pode ser um problema de acessibilidade para alguns usuários.</span><span class="sxs-lookup"><span data-stu-id="382d2-106">Having a web product that has a light theme in a dark-mode operating system is grating and can be an accessibility issue for some users.</span></span>  

<span data-ttu-id="382d2-107">Para uma página da Web, você pode usar a Consulta de Mídia CSS de esquema de cores [prefers-color][MDNPrefersColorScheme] para detectar se o usuário prefere exibir seu produto em um esquema de cores mais escuro ou mais claro.</span><span class="sxs-lookup"><span data-stu-id="382d2-107">For a webpage, you can use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect whether the user prefers to display your product in a darker or lighter color scheme.</span></span>  <span data-ttu-id="382d2-108">Em seguida, para testar o resultado, use [Microsoft Edge DevTools][DevtoolsIndex] para simular uma alteração do modo escuro para o modo claro, sem precisar alterar a configuração de todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="382d2-108">Then to test the result, use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode, without having to change the setting for your entire operating system.</span></span>  

**<span data-ttu-id="382d2-109">Para emular tema escuro ou claro:</span><span class="sxs-lookup"><span data-stu-id="382d2-109">To emulate dark or light theme:</span></span>**

1.  <span data-ttu-id="382d2-110">Abra o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="382d2-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="382d2-111">Selecione `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="382d2-111">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="382d2-113">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="382d2-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="382d2-114">Digite `emulate color` , escolha **Emular CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="382d2-114">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opção de esquema de cores do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="382d2-116">Opção de esquema de cores do Menu **de** Comando</span><span class="sxs-lookup"><span data-stu-id="382d2-116">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="382d2-117">Basta digitar ou não revelar a ferramenta certa, pois também há uma maneira de escolher um `dark` `light` tema para [DevTools][DevtoolsCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="382d2-117">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="382d2-118">Se você estiver se perguntando o que escolher, certifique-se de que você está escolhendo um **item** de menu de renderização, não um item de menu **de** aparência.</span><span class="sxs-lookup"><span data-stu-id="382d2-118">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="382d2-119">Depois de escolher um esquema de cores, atualize o documento atual para exibir o modo simulado.</span><span class="sxs-lookup"><span data-stu-id="382d2-119">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulado dentro Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="382d2-121">Modo de luz simulado dentro Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="382d2-121">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="382d2-122">Exibir e alterar o CSS como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="382d2-122">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="382d2-123">Para obter mais informações, navegue [até Começar a exibir e alterar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="382d2-123">For more information, navigate to [Get started with viewing and changing CSS][DevtoolsCssIndex].</span></span>  


## <a name="see-also"></a><span data-ttu-id="382d2-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="382d2-124">See also</span></span>

* [<span data-ttu-id="382d2-125">Verifique se há problemas de contraste com o tema escuro e o tema claro</span><span class="sxs-lookup"><span data-stu-id="382d2-125">Check for contrast issues with dark theme and light theme</span></span>](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Começar a exibir e alterar o CSS | Microsoft Docs"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
