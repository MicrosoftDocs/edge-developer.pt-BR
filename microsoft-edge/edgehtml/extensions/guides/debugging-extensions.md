---
description: Com as ferramentas de desenvolvedor F12, saiba como depurar um script de fundo de extensão, scripts de conteúdo e páginas de extensão.
title: Extensões-depuração
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, JavaScript, desenvolvedor, depuração, depuração
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 17da1a2badd99dd57bb8b1e3de063fe045b34333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231864"
---
# <span data-ttu-id="7d359-104">Depurar extensões</span><span class="sxs-lookup"><span data-stu-id="7d359-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7d359-105">Você pode depurar as extensões no Microsoft Edge usando as ferramentas de desenvolvedor F12.</span><span class="sxs-lookup"><span data-stu-id="7d359-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>

<span data-ttu-id="7d359-106">O vídeo a seguir passa por uma extensão de depuração do Microsoft Edge, acompanhando cada cenário de depuração e corrigindo-o ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="7d359-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span> <span data-ttu-id="7d359-107">Para obter mais informações, consulte as instruções passo a passo abaixo.</span><span class="sxs-lookup"><span data-stu-id="7d359-107">See the step-by-step instructions below for more info.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> <span data-ttu-id="7d359-108">Para aproveitar a depuração de extensão com F12, você deve primeiro ativar os recursos de desenvolvedor em About: flags.</span><span class="sxs-lookup"><span data-stu-id="7d359-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span> <span data-ttu-id="7d359-109">Consulte [adicionando e removendo extensões](./adding-and-removing-extensions.md) para obter detalhes sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="7d359-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>


## <span data-ttu-id="7d359-110">Depuração de script em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7d359-110">Background script debugging</span></span>
<span data-ttu-id="7d359-111">Para iniciar a depuração do script de tela de fundo de sua extensão:</span><span class="sxs-lookup"><span data-stu-id="7d359-111">To start debugging the background script of your extension:</span></span>

1. <span data-ttu-id="7d359-112">Clique em **mais (...)** seguido de **extensões** para ir para o painel extensão.</span><span class="sxs-lookup"><span data-stu-id="7d359-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
 ![botão mais](./../media/morebutton.png)
2. <span data-ttu-id="7d359-114">Clique na extensão que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="7d359-114">Click on the extension that you want to debug.</span></span>
3. <span data-ttu-id="7d359-115">Clique no link da **página de plano de fundo** para exibir F12 para o processo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7d359-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
 ![exibição de extensão selecionada de opções com o link inspecionar](./../media/debug-inspect.png)
4. <span data-ttu-id="7d359-117">Selecione a guia **depurador** em F12.</span><span class="sxs-lookup"><span data-stu-id="7d359-117">Select the **Debugger** tab in F12.</span></span>
5. <span data-ttu-id="7d359-118">Navegue até o script de plano de fundo da extensão e selecione-o.</span><span class="sxs-lookup"><span data-stu-id="7d359-118">Navigate to and select your extension's background script.</span></span>
6. <span data-ttu-id="7d359-119">Coloque pontos de interrupção para depuração clicando à esquerda do número de linha do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="7d359-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![console F12 mostrando o script de fundo com pontos de interrupção](./../media/debug-f12-background.png)
7. <span data-ttu-id="7d359-121">Selecionar a guia **console** e executar o comando " `location.reload()` ".</span><span class="sxs-lookup"><span data-stu-id="7d359-121">Select the **Console** tab and execute the command "`location.reload()`".</span></span> <span data-ttu-id="7d359-122">Isso reexecutará o script em segundo plano, permitindo que você percorra o código.</span><span class="sxs-lookup"><span data-stu-id="7d359-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
 ![console com local. recarregar inserido](./../media/debug-f12-background-console.png)


## <span data-ttu-id="7d359-124">Depuração de script de conteúdo</span><span class="sxs-lookup"><span data-stu-id="7d359-124">Content script debugging</span></span>
<span data-ttu-id="7d359-125">Para iniciar a depuração do script de conteúdo de sua extensão:</span><span class="sxs-lookup"><span data-stu-id="7d359-125">To start debugging the content script of your extension:</span></span>

1. <span data-ttu-id="7d359-126">Inicie o F12 navegando até o botão **mais (...)** e selecionando **"ferramentas de desenvolvedor F12"** ou pressionando F12 no teclado.</span><span class="sxs-lookup"><span data-stu-id="7d359-126">Launch F12 by either navigating to the **More (...)** button and selecting **"F12 Developer Tools"** or by pressing F12 on your keyboard.</span></span>
2. <span data-ttu-id="7d359-127">Navegue até o script de conteúdo da extensão e selecione-o.</span><span class="sxs-lookup"><span data-stu-id="7d359-127">Navigate to and select your extension's content script.</span></span> <span data-ttu-id="7d359-128">Scripts de conteúdo para extensões em execução no momento serão representados por uma pasta diferente para cada extensão.</span><span class="sxs-lookup"><span data-stu-id="7d359-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d359-129">Somente scripts de conteúdo em execução aparecerão.</span><span class="sxs-lookup"><span data-stu-id="7d359-129">Only running content scripts will appear.</span></span>

3. <span data-ttu-id="7d359-130">Coloque pontos de interrupção para depuração clicando à esquerda do número de linha do código-fonte.</span><span class="sxs-lookup"><span data-stu-id="7d359-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![F12 com script de conteúdo sendo depurado](./../media/debug-content-f12.png)
4. <span data-ttu-id="7d359-132">Atualize a guia do navegador para começar a percorrer o código.</span><span class="sxs-lookup"><span data-stu-id="7d359-132">Refresh the browser tab to begin stepping though your code.</span></span>




## <span data-ttu-id="7d359-133">Depuração da página de extensão</span><span class="sxs-lookup"><span data-stu-id="7d359-133">Extension page debugging</span></span>

<span data-ttu-id="7d359-134">Há dois métodos que podem ser usados para acessar o código-fonte da página de extensão para a depuração.</span><span class="sxs-lookup"><span data-stu-id="7d359-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span> <span data-ttu-id="7d359-135">Um método aplica-se a uma variedade de páginas enquanto a outra só funciona para páginas pop-up.</span><span class="sxs-lookup"><span data-stu-id="7d359-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>

### <span data-ttu-id="7d359-136">Depuração de qualquer página de extensão</span><span class="sxs-lookup"><span data-stu-id="7d359-136">Debugging any extension page</span></span>
<span data-ttu-id="7d359-137">O método a seguir funciona para todas as páginas de extensão, como a página opções e pop-ups:</span><span class="sxs-lookup"><span data-stu-id="7d359-137">The following method works for all extension pages like the options page and popups:</span></span>


1. <span data-ttu-id="7d359-138">Clique com o botão direito do mouse no plano de fundo da página.</span><span class="sxs-lookup"><span data-stu-id="7d359-138">Right-click on the background of your page.</span></span>
2. <span data-ttu-id="7d359-139">Selecione **"Exibir fonte"**.</span><span class="sxs-lookup"><span data-stu-id="7d359-139">Select **"View source"**.</span></span>

   ![depuração popup com F12-Select](./../media/debug-popup-select.png)

3. <span data-ttu-id="7d359-141">Quando o F12 abrir, coloque os pontos de interrupção no arquivo que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="7d359-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>

   ![depuração pop-up com F12](./../media/debug-popup-f12.png)
4. <span data-ttu-id="7d359-143">Selecione a guia **console** e execute o comando `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="7d359-143">Select the **Console** tab and execute the command `location.reload()`.</span></span> <span data-ttu-id="7d359-144">Isso reexecutará o script de página, permitindo que você percorra o código.</span><span class="sxs-lookup"><span data-stu-id="7d359-144">This will re-execute the page script, allowing you to step through your code.</span></span>  

   ![console com local. recarregar inserido](./../media/debug-f12-background-console.png)

### <span data-ttu-id="7d359-146">Depurando uma página de extensão pop-up</span><span class="sxs-lookup"><span data-stu-id="7d359-146">Debugging a popup extension page</span></span>
<span data-ttu-id="7d359-147">Embora o método de depuração de páginas de extensão também se aplique às páginas de extensão pop-up, as etapas a seguir descrevem outra maneira de depurar o Popup:</span><span class="sxs-lookup"><span data-stu-id="7d359-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>

1. <span data-ttu-id="7d359-148">Clique com o botão direito do mouse no ícone da extensão.</span><span class="sxs-lookup"><span data-stu-id="7d359-148">Right-click your extension's icon.</span></span>
2. <span data-ttu-id="7d359-149">Selecione **"inspecionar pop-up"**.</span><span class="sxs-lookup"><span data-stu-id="7d359-149">Select **"Inspect popup"**.</span></span>

   ![inspecionar depuração de pop-up](./../media/debug-popup-inspect.png)
3. <span data-ttu-id="7d359-151">Siga as etapas 3 e 4 acima para colocar pontos de interrupção e recarregar o pop-up.</span><span class="sxs-lookup"><span data-stu-id="7d359-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>
