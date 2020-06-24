---
title: Forçar o Microsoft Edge DevTools no modo de visualização do esquema de cores (CSS prefere o esquema de cores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: a83284b676ad388114a4a0ddb7ebdf2203ebcb90
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758047"
---
# <span data-ttu-id="244a1-103">Simulação de esquema de cores escuras ou leves</span><span class="sxs-lookup"><span data-stu-id="244a1-103">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="244a1-104">Os sistemas operacionais têm uma maneira de exibir qualquer aplicativo em cores mais escuras ou mais claras.</span><span class="sxs-lookup"><span data-stu-id="244a1-104">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="244a1-105">Ter um produto da Web com um tema claro em um sistema operacional em modo escuro está de meio funcionamento e pode ser um problema de acessibilidade para alguns usuários.</span><span class="sxs-lookup"><span data-stu-id="244a1-105">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="244a1-106">Na Web, você pode usar a consulta de mídia CSS de [preferência esquema de cores][MDNPrefersColorScheme] para detectar se os usuários preferem ver o produto em um esquema de cores mais escuro ou mais claro.</span><span class="sxs-lookup"><span data-stu-id="244a1-106">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="244a1-107">Use o [Microsoft Edge devtools][DevtoolsGuideChromiumMain] para simular uma alteração do modo escuro para Light sem ter que alterar todo o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="244a1-107">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="244a1-108">Abrir o **menu de comandos**.</span><span class="sxs-lookup"><span data-stu-id="244a1-108">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="244a1-109">Pressione `Control` + `Shift` + `P` no Windows ou `Command` + `Shift` + `P` no MacOS.</span><span class="sxs-lookup"><span data-stu-id="244a1-109">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="O menu de comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="244a1-111">O **menu de comando**</span><span class="sxs-lookup"><span data-stu-id="244a1-111">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="244a1-112">Tipo `emulate color` , selecione **emular CSS prefere opções-esquema de cores: escuro** ou **emular CSS prefere-Color-esquema: Light** e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="244a1-112">Type `emulate color`, select either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light**  and then press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Seleção do esquema de cores no menu de comandos" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="244a1-114">Seleção do esquema de cores no menu de **comandos**</span><span class="sxs-lookup"><span data-stu-id="244a1-114">Color scheme selection from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="244a1-115">Basta digitar `dark` ou `light` não revelar a ferramenta certa, pois também há uma maneira de [escolher um tema para devtools][DevtoolsGuideChromiumCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="244a1-115">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="244a1-116">Se você estiver imaginando o que escolher, verifique se está selecionando um item de menu de **renderização** , não um item de menu de **aparência** .</span><span class="sxs-lookup"><span data-stu-id="244a1-116">If you are wondering what to choose, make sure that you are selecting a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="244a1-117">Depois de selecionar um esquema de cores, recarregue o documento atual para ver o modo simulado.</span><span class="sxs-lookup"><span data-stu-id="244a1-117">After you select a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulado dentro do Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="244a1-119">Modo de luz simulado dentro do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="244a1-119">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="244a1-120">Exiba e altere sua CSS como qualquer outra página da Web.</span><span class="sxs-lookup"><span data-stu-id="244a1-120">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="244a1-121">Para obter mais informações, consulte [introdução à visualização e à alteração de CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="244a1-121">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) Microsoft | Documentos da Microsoft"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema escuro no Microsoft Edge DevTools | Documentos da Microsoft"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "preferência – esquema de cores | MDN"  
