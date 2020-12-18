---
Description: Forçar o Microsoft Edge DevTools no modo de visualização do esquema de cores.
title: Forçar o Microsoft Edge DevTools no modo de visualização do esquema de cores (CSS prefere o esquema de cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 29b0121a616a037fa11b61799efeffd201eb1821
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230793"
---
# <span data-ttu-id="e69a1-104">Simulação de esquema de cores escuras ou leves</span><span class="sxs-lookup"><span data-stu-id="e69a1-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="e69a1-105">Os sistemas operacionais têm uma maneira de exibir qualquer aplicativo em cores mais escuras ou mais claras.</span><span class="sxs-lookup"><span data-stu-id="e69a1-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="e69a1-106">Ter um produto da Web com um tema claro em um sistema operacional em modo escuro está de meio funcionamento e pode ser um problema de acessibilidade para alguns usuários.</span><span class="sxs-lookup"><span data-stu-id="e69a1-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="e69a1-107">Na Web, você pode usar a consulta de mídia CSS de [preferência esquema de cores][MDNPrefersColorScheme] para detectar se os usuários preferem ver o produto em um esquema de cores mais escuro ou mais claro.</span><span class="sxs-lookup"><span data-stu-id="e69a1-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="e69a1-108">Use o [Microsoft Edge devtools][DevtoolsGuideChromiumMain] para simular uma alteração do modo escuro para Light sem ter que alterar todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e69a1-108">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="e69a1-109">Abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="e69a1-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="e69a1-110">Selecione `Control` + `Shift` + `P` no Windows/Linux ou `Command` + `Shift` + `P` no MacOS.</span><span class="sxs-lookup"><span data-stu-id="e69a1-110">Select `Control`+`Shift`+`P`  on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="e69a1-112">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="e69a1-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="e69a1-113">Digite `emulate color` , escolha **emular CSS prefere opções-esquema de cores: escuro** ou **emular CSS prefere-Color-esquema: Light** e, em seguida, selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e69a1-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opção esquema de cores do menu de comandos" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="e69a1-115">Opção esquema de cores do menu de **comandos**</span><span class="sxs-lookup"><span data-stu-id="e69a1-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="e69a1-116">Basta digitar `dark` ou `light` não revelar a ferramenta certa, pois também há uma maneira de [escolher um tema para devtools][DevtoolsGuideChromiumCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="e69a1-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="e69a1-117">Se você estiver imaginando o que escolher, verifique se está escolhendo um item de menu de **renderização** , não um item de menu de **aparência** .</span><span class="sxs-lookup"><span data-stu-id="e69a1-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="e69a1-118">Depois de escolher um esquema de cores, recarregue o documento atual para ver o modo simulado.</span><span class="sxs-lookup"><span data-stu-id="e69a1-118">After you choose a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulado dentro do Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="e69a1-120">Modo de luz simulado dentro do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e69a1-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e69a1-121">Exiba e altere sua CSS como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="e69a1-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="e69a1-122">Para obter mais informações, consulte [introdução à visualização e à alteração de CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="e69a1-122">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "preferência – esquema de cores | MDN"  
