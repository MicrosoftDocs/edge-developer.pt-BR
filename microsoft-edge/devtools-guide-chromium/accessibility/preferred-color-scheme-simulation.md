---
description: Force o Microsoft Edge DevTools no modo de Visualização do Esquema de Cores.
title: Forçar o Microsoft Edge DevTools no modo de Visualização de Esquema de Cores (CSS prefere Esquema de Cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1cdc9601e9e6fea1f6921c6cc40a1ed8232a0da8
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519146"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="2ce19-104">Simulação do Esquema de Cores Escuras ou Claras</span><span class="sxs-lookup"><span data-stu-id="2ce19-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="2ce19-105">Os sistemas operacionais têm uma maneira de exibir qualquer aplicativo em cores mais escuras ou mais claras.</span><span class="sxs-lookup"><span data-stu-id="2ce19-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="2ce19-106">Ter um produto Web com um tema claro em um sistema operacional de modo escuro é irritante e pode ser um problema de acessibilidade para alguns usuários.</span><span class="sxs-lookup"><span data-stu-id="2ce19-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="2ce19-107">Na Web, você pode usar a Consulta de Mídia CSS do esquema [prefers-color][MDNPrefersColorScheme] para detectar se os usuários preferem exibir seu produto em um esquema de cores mais escuro ou mais claro.</span><span class="sxs-lookup"><span data-stu-id="2ce19-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to display your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="2ce19-108">Use [o Microsoft Edge DevTools][DevtoolsIndex] para simular uma alteração do modo escuro para o modo claro sem precisar alterar todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2ce19-108">Use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="2ce19-109">Abra o **Menu de Comando**.</span><span class="sxs-lookup"><span data-stu-id="2ce19-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="2ce19-110">Selecione `Ctrl` + `Shift` + `P` \(Windows/Linux\) ou `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2ce19-110">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O Menu De comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="2ce19-112">O **Menu De comando**</span><span class="sxs-lookup"><span data-stu-id="2ce19-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="2ce19-113">Digite `emulate color` , escolha **Emular CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2ce19-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opção de esquema de cores do Menu de Comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="2ce19-115">Opção de esquema de cores do Menu **de** Comando</span><span class="sxs-lookup"><span data-stu-id="2ce19-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="2ce19-116">Basta digitar ou não revelar a ferramenta certa, pois também há uma maneira de escolher um `dark` `light` tema para [DevTools][DevtoolsCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="2ce19-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="2ce19-117">Se você estiver se perguntando o que escolher, certifique-se de que você está escolhendo um **item** de menu de renderização, não um item de menu **de** aparência.</span><span class="sxs-lookup"><span data-stu-id="2ce19-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="2ce19-118">Depois de escolher um esquema de cores, atualize o documento atual para exibir o modo simulado.</span><span class="sxs-lookup"><span data-stu-id="2ce19-118">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulado dentro do Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="2ce19-120">Modo de luz simulado dentro do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2ce19-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="2ce19-121">Exibir e alterar o CSS como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="2ce19-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="2ce19-122">Para obter mais informações, navegue [até Começar a exibir e alterar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="2ce19-122">For more information, navigate to [Get Started With Viewing And Changing CSS][DevtoolsCssIndex].</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Começar a exibir e alterar o css | Microsoft Docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
