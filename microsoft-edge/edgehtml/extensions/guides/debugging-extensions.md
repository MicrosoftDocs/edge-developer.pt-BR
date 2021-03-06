---
description: Com as Ferramentas de Desenvolvedor F12, saiba como depurar o script em segundo plano, scripts de conteúdo e páginas de extensão de uma extensão.
title: Depuração | Extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, javascript, desenvolvedor, depuração, depuração
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399362"
---
# <a name="debugging-extensions"></a><span data-ttu-id="e9b5a-104">Depurar extensões</span><span class="sxs-lookup"><span data-stu-id="e9b5a-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="e9b5a-105">Você pode depurar suas extensões no Microsoft Edge usando as Ferramentas de Desenvolvedor F12.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>  

<span data-ttu-id="e9b5a-106">O vídeo a seguir passa por uma extensão de bugs do Microsoft Edge, acompanhando cada cenário de depuração e corrigindo-o ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span>  <span data-ttu-id="e9b5a-107">Confira as instruções passo a passo abaixo para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-107">See the step-by-step instructions below for more info.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> <span data-ttu-id="e9b5a-108">Para aproveitar a depuração de extensão com F12, primeiro você deve ativar os recursos do desenvolvedor em about:flags.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span>  <span data-ttu-id="e9b5a-109">Consulte [Adicionando e removendo extensões](./adding-and-removing-extensions.md) para obter detalhes sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>  

## <a name="background-script-debugging"></a><span data-ttu-id="e9b5a-110">Depuração de script em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e9b5a-110">Background script debugging</span></span>  

<span data-ttu-id="e9b5a-111">Para começar a depurar o script em segundo plano da extensão:</span><span class="sxs-lookup"><span data-stu-id="e9b5a-111">To start debugging the background script of your extension:</span></span>  

1.  <span data-ttu-id="e9b5a-112">Clique em **Mais (...)** seguido de **Extensões** para entrar no painel de extensão.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
    
    ![botão mais](../media/morebutton.png)  
    
1.  <span data-ttu-id="e9b5a-114">Clique na extensão que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-114">Click on the extension that you want to debug.</span></span>  
1.  <span data-ttu-id="e9b5a-115">Clique no link **Página em segundo** plano para trazer o F12 para o processo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
    
    ![exibição de extensão selecionada de opções com link de inspeção](../media/debug-inspect.png)  
    
1.  <span data-ttu-id="e9b5a-117">Selecione a **guia Depurador** no F12.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-117">Select the **Debugger** tab in F12.</span></span>  
1.  <span data-ttu-id="e9b5a-118">Navegue até e selecione o script em segundo plano da extensão.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-118">Navigate to and select your extension's background script.</span></span>  
1.  <span data-ttu-id="e9b5a-119">Coloque pontos de interrupção para depuração clicando à esquerda do número da linha de código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![console f12 mostrando script em segundo plano com pontos de quebra](../media/debug-f12-background.png)  
    
1.  <span data-ttu-id="e9b5a-121">Selecione a **guia Console** e execute o `location.reload()` comando.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-121">Select the **Console** tab and execute the `location.reload()` command.</span></span>  <span data-ttu-id="e9b5a-122">Isso executará o script em segundo plano, permitindo que você execute o código.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
    
    ![console com location.reload inserido](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a><span data-ttu-id="e9b5a-124">Depuração de script de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e9b5a-124">Content script debugging</span></span>  

<span data-ttu-id="e9b5a-125">Para começar a depurar o script de conteúdo da extensão:</span><span class="sxs-lookup"><span data-stu-id="e9b5a-125">To start debugging the content script of your extension:</span></span>  

1.  <span data-ttu-id="e9b5a-126">Iniciar F12 navegando até o botão **Mais (...)** e selecionando Ferramentas de Desenvolvedor **F12** ou pressionando `F12` o teclado.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-126">Launch F12 by either navigating to the **More (...)** button and selecting **F12 Developer Tools** or by pressing `F12` on your keyboard.</span></span>  
1.  <span data-ttu-id="e9b5a-127">Navegue até e selecione o script de conteúdo da extensão.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-127">Navigate to and select your extension's content script.</span></span>  <span data-ttu-id="e9b5a-128">Scripts de conteúdo para extensões em execução serão representados por uma pasta diferente para cada extensão.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e9b5a-129">Somente os scripts de conteúdo em execução serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-129">Only running content scripts will appear.</span></span>  
    
1.  <span data-ttu-id="e9b5a-130">Coloque pontos de interrupção para depuração clicando à esquerda do número da linha de código-fonte.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![f12 com script de conteúdo sendo depurado](../media/debug-content-f12.png)  
    
1.  <span data-ttu-id="e9b5a-132">Atualize a guia do navegador para começar a fazer a revisão do código.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-132">Refresh the browser tab to begin stepping though your code.</span></span>  
    
## <a name="extension-page-debugging"></a><span data-ttu-id="e9b5a-133">Depuração de página de extensão</span><span class="sxs-lookup"><span data-stu-id="e9b5a-133">Extension page debugging</span></span>  

<span data-ttu-id="e9b5a-134">Há dois métodos que podem ser usados para acessar o código-fonte da página de extensão para depuração.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span>  <span data-ttu-id="e9b5a-135">Um método se aplica a uma variedade de páginas enquanto o outro só funciona para páginas pop-up.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>  

### <a name="debugging-any-extension-page"></a><span data-ttu-id="e9b5a-136">Depurando qualquer página de extensão</span><span class="sxs-lookup"><span data-stu-id="e9b5a-136">Debugging any extension page</span></span>  

<span data-ttu-id="e9b5a-137">O método a seguir funciona para todas as páginas de extensão, como a página de opções e pop-ups:</span><span class="sxs-lookup"><span data-stu-id="e9b5a-137">The following method works for all extension pages like the options page and popups:</span></span>  

1.  <span data-ttu-id="e9b5a-138">Clique com o botão direito do mouse no plano de fundo da página.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-138">Right-click on the background of your page.</span></span>  
1.  <span data-ttu-id="e9b5a-139">Selecione **Exibir fonte**.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-139">Select **View source**.</span></span>  
    
    ![Abrir depuração pop-up com f12](../media/debug-popup-select.png)  
    
1.  <span data-ttu-id="e9b5a-141">Quando f12 é aberto, coloque pontos de interrupção no arquivo que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>  
    
    ![depuração pop-up com f12](../media/debug-popup-f12.png)  
    
1.  <span data-ttu-id="e9b5a-143">Selecione a **guia Console** e execute o comando `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="e9b5a-143">Select the **Console** tab and execute the command `location.reload()`.</span></span>  <span data-ttu-id="e9b5a-144">Isso executará o script de página de novo, permitindo que você execute seu código.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-144">This will re-execute the page script, allowing you to step through your code.</span></span>  
    
    ![console com location.reload inserido](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a><span data-ttu-id="e9b5a-146">Depurando uma página de extensão pop-up</span><span class="sxs-lookup"><span data-stu-id="e9b5a-146">Debugging a popup extension page</span></span>  

<span data-ttu-id="e9b5a-147">Embora o método de depuração de páginas de extensão também se aplique a páginas de extensão pop-up, as etapas a seguir definem outra maneira de depurar seu pop-up:</span><span class="sxs-lookup"><span data-stu-id="e9b5a-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>  

1.  <span data-ttu-id="e9b5a-148">Clique com o botão direito do mouse no ícone da extensão.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-148">Right-click your extension's icon.</span></span>  
1.  <span data-ttu-id="e9b5a-149">Selecione **Inspecionar pop-up**.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-149">Select **Inspect popup**.</span></span>  
    
    ![inspeção de depuração pop-up](../media/debug-popup-inspect.png)  
    
1.  <span data-ttu-id="e9b5a-151">Siga as etapas 3 e 4 acima para colocar pontos de interrupção e recarregar o pop-up.</span><span class="sxs-lookup"><span data-stu-id="e9b5a-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>  
    