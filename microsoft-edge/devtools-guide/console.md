---
description: Use a ferramenta de console para depuração interativa e testes ad hoc.
title: DevTools-console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, console
ms.custom: seodec18
ms.openlocfilehash: f2733cac57ed5f2364747ee64e669fa83aae41f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561445"
---
# <span data-ttu-id="8cbe9-104">Console</span><span class="sxs-lookup"><span data-stu-id="8cbe9-104">Console</span></span>

<span data-ttu-id="8cbe9-105">A ferramenta de desenvolvedor de console no Microsoft Edge registra informações que estão associadas a uma página da Web, como JavaScript, solicitações de rede e erros de segurança.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-105">The Console developer tool in Microsoft Edge logs information that's associated with a webpage, such as JavaScript, network requests, and security errors.</span></span> <span data-ttu-id="8cbe9-106">Você pode usar o console para depuração interativa e testes ad hoc.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-106">You can use the Console for interactive debugging and ad hoc testing.</span></span> 

<span data-ttu-id="8cbe9-107">Para abrir a ferramenta de console no Microsoft Edge, pressione a tecla F12 para acessar a janela da ferramenta de desenvolvedor (ou clique com o botão direito do mouse na página e selecione **inspecionar elemento**).</span><span class="sxs-lookup"><span data-stu-id="8cbe9-107">To open the Console tool in Microsoft Edge, press the F12 key to access the developer tool window (or right-click on the page, and then select **Inspect Element**).</span></span> <span data-ttu-id="8cbe9-108">Em seguida, selecione a guia **console** na parte superior da janela.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-108">Then, select the **Console** tab at the top of the window.</span></span> 

<span data-ttu-id="8cbe9-109">Você também pode usar a ferramenta de console para se comunicar com uma página da Web em execução e a partir dela.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-109">You can also use the Console tool to communicate to and from a running webpage.</span></span> <span data-ttu-id="8cbe9-110">Você pode usar o console para:</span><span class="sxs-lookup"><span data-stu-id="8cbe9-110">You can use the Console to:</span></span>

- <span data-ttu-id="8cbe9-111">Poste [códigos de erro e de status](./console/error-and-status-codes.md) padrão e mensagens informativas à medida que seu código é executado.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-111">Post standard [error and status codes](./console/error-and-status-codes.md) and informational messages as your code runs.</span></span>
- <span data-ttu-id="8cbe9-112">Gere logs de depuração personalizados nas chamadas de [API do console](./console/console-api.md) que você incluir no seu código.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-112">Generate custom debug logs from the [Console API](./console/console-api.md) calls you include in your code.</span></span>
- <span data-ttu-id="8cbe9-113">Fornecer uma [linha de comando](./console/command-line.md) e uma exibição de árvore interativa para inspecionar os valores de retorno atuais de variáveis e funções chave.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-113">Provide a [command line](./console/command-line.md) and interactive tree view for inspecting current return values of key variables and functions.</span></span>

## <span data-ttu-id="8cbe9-114">Partes do console</span><span class="sxs-lookup"><span data-stu-id="8cbe9-114">Parts of the Console</span></span>

<span data-ttu-id="8cbe9-115">A imagem a seguir mostra as partes principais do console:</span><span class="sxs-lookup"><span data-stu-id="8cbe9-115">The following image shows the key parts of the Console:</span></span>

![O console do Microsoft Edge DevTools](./media/console.png)

1. <span data-ttu-id="8cbe9-117">**Erros**  /  de **Avisos**  /  **Informações**  /  Botões de **log** : filtra a saída do console pelo tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-117">**Errors** / **Warnings** / **Info** / **Logs** buttons: Filter console output by the specified type.</span></span> <span data-ttu-id="8cbe9-118">Você pode selecionar vários botões mantendo pressionada a tecla **Ctrl** .</span><span class="sxs-lookup"><span data-stu-id="8cbe9-118">You can multi-select buttons by holding down the **Ctrl** key.</span></span> <span data-ttu-id="8cbe9-119">O botão **todos** limpa todos os filtros.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-119">The **All** button clears all filters.</span></span>

2. <span data-ttu-id="8cbe9-120">Botão **limpar** (**Ctrl + L**): o botão **limpar** limpa a exibição atual do console.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-120">**Clear** button (**Ctrl+L**): The **Clear** button clears the current console display.</span></span>

3. <span data-ttu-id="8cbe9-121">Caixa de seleção **preservar log** : marcar a caixa de seleção **preservar log** persiste a saída do seu console nas atualizações da página e fechar e reabrir o devtools.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-121">**Preserve Log** check box: Selecting the **Preserve Log** check box persists your console output across page refreshes and closing and reopening DevTools.</span></span> <span data-ttu-id="8cbe9-122">O histórico do console é limpo apenas quando a guia é fechada ou você limpa manualmente o console.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-122">The Console history clears only when the tab is closed or you manually clear the Console.</span></span>

4. <span data-ttu-id="8cbe9-123">**Destino**: Use o menu suspenso de **destino** para alternar para um contexto de execução diferente, como `<iframe>` em sua página ou em uma extensão em execução.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-123">**Target**: Use the **Target** drop-down menu to switch to a different execution context, such as an `<iframe>` in your page or a running extension.</span></span> <span data-ttu-id="8cbe9-124">Por padrão, o quadro de nível superior da sua página é selecionado.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-124">By default, the top-level frame of your page is selected.</span></span> <span data-ttu-id="8cbe9-125">Passar o mouse sobre um quadro selecionado exibe uma dica de ferramenta que mostra a URL completa desse recurso.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-125">Hovering over a selected frame displays a tooltip that shows the full URL for that resource.</span></span>

5. <span data-ttu-id="8cbe9-126">**Mostrar console**  /  Botão **ocultar console** (**Ctrl** +  **&grave;** ): além do painel do console, você pode usar o console na parte inferior de qualquer outro painel do devtools pressionando o botão **Mostrar**console  /  **ocultar console** .</span><span class="sxs-lookup"><span data-stu-id="8cbe9-126">**Show Console** / **Hide Console** button (**Ctrl**+ **&grave;** ): In addition to the Console panel, you can use the console from the bottom of any other DevTools panel by pressing the **Show Console** / **Hide Console** button.</span></span> <span data-ttu-id="8cbe9-127">O botão não tem efeito quando o DevTools está aberto no painel do console.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-127">The button has no effect when DevTools is open to the Console panel.</span></span>
 
6. <span data-ttu-id="8cbe9-128">**Filtrar logs** (**Ctrl + F**): você também pode filtrar logs usando uma cadeia de texto específica na caixa de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-128">**Filter logs** (**Ctrl+F**) : You can also filter logs by using a specific text string in the search box.</span></span>

7. <span data-ttu-id="8cbe9-129">**Depurador**: selecione qualquer link de fonte azul para abrir o depurador devtools para essa linha de código específica para inspeção adicional.</span><span class="sxs-lookup"><span data-stu-id="8cbe9-129">**Debugger**: Select any blue source link to open the DevTools Debugger to that particular line of code for further inspection.</span></span>

## <span data-ttu-id="8cbe9-130">Teclado</span><span class="sxs-lookup"><span data-stu-id="8cbe9-130">Shortcuts</span></span>

<span data-ttu-id="8cbe9-131">Ação</span><span class="sxs-lookup"><span data-stu-id="8cbe9-131">Action</span></span>                                            | <span data-ttu-id="8cbe9-132">Atalho</span><span class="sxs-lookup"><span data-stu-id="8cbe9-132">Shortcut</span></span>               
:-------------------------------------------------| :----------------------
<span data-ttu-id="8cbe9-133">Iniciar o DevTools com o console em foco</span><span class="sxs-lookup"><span data-stu-id="8cbe9-133">Launch DevTools with Console in focus</span></span>             | <span data-ttu-id="8cbe9-134">**Ctrl +**  +  **Alterar**  +  **J**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-134">**Ctrl** + **Shift** + **J**</span></span> 
<span data-ttu-id="8cbe9-135">Alternar para o console</span><span class="sxs-lookup"><span data-stu-id="8cbe9-135">Switch to the Console</span></span>                                 | <span data-ttu-id="8cbe9-136">**Ctrl +**  +  **2**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-136">**Ctrl** + **2**</span></span>           
<span data-ttu-id="8cbe9-137">Mostrar/ocultar o console a partir de outra guia DevTools</span><span class="sxs-lookup"><span data-stu-id="8cbe9-137">Show/hide the Console from another DevTools tab</span></span>       | <span data-ttu-id="8cbe9-138">**Ctrl +**  +  **&grave;** (Back-Tick)</span><span class="sxs-lookup"><span data-stu-id="8cbe9-138">**Ctrl** + **&grave;** (back tick)</span></span>  
<span data-ttu-id="8cbe9-139">Executar (comando de linha única)</span><span class="sxs-lookup"><span data-stu-id="8cbe9-139">Execute (single-line command)</span></span>                     | **<span data-ttu-id="8cbe9-140">Tecla Enter</span><span class="sxs-lookup"><span data-stu-id="8cbe9-140">Enter</span></span>**                
<span data-ttu-id="8cbe9-141">Quebra de linha sem execução (comando de várias linhas)</span><span class="sxs-lookup"><span data-stu-id="8cbe9-141">Line break without executing (multi-line command)</span></span> | <span data-ttu-id="8cbe9-142">**Alterar**  +  **Enter** ou **Ctrl +**  +  **Enter**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-142">**Shift** + **Enter** or **Ctrl** + **Enter**</span></span>      
<span data-ttu-id="8cbe9-143">Limpar o console de todas as mensagens</span><span class="sxs-lookup"><span data-stu-id="8cbe9-143">Clear the Console of all messages</span></span>                 | <span data-ttu-id="8cbe9-144">**Ctrl +**  +  **L**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-144">**Ctrl** + **L**</span></span>           
<span data-ttu-id="8cbe9-145">Filtrar logs (definir o foco para a caixa de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="8cbe9-145">Filter logs (set focus to search box)</span></span>             | <span data-ttu-id="8cbe9-146">**Ctrl +**  +  **L**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-146">**Ctrl** + **F**</span></span>           
<span data-ttu-id="8cbe9-147">Aceitar sugestão de preenchimento automático (quando estiver em foco)</span><span class="sxs-lookup"><span data-stu-id="8cbe9-147">Accept auto-completion suggestion (when in focus)</span></span> | <span data-ttu-id="8cbe9-148">**Enter** ou **Tab**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-148">**Enter** or **Tab**</span></span>       
<span data-ttu-id="8cbe9-149">Sugestão de preenchimento automático anterior/seguinte</span><span class="sxs-lookup"><span data-stu-id="8cbe9-149">Previous/next auto-completion suggestion</span></span>          | <span data-ttu-id="8cbe9-150">Tecla de seta **para cima** / **Tecla de seta para baixo**</span><span class="sxs-lookup"><span data-stu-id="8cbe9-150">**Up arrow key**/**Down arrow key**</span></span>   


