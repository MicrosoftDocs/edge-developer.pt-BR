---
description: Saiba como filtrar mensagens de console
title: Começar a filtrar mensagens no Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b493bb790b48bc1c4dca0e6802d2f638099b7644
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483305"
---
# <a name="filter-console-messages"></a><span data-ttu-id="c10b3-104">Filtrar mensagens de Console</span><span class="sxs-lookup"><span data-stu-id="c10b3-104">Filter Console messages</span></span>  

<span data-ttu-id="c10b3-105">Ao navegar na Web, você pode encontrar que **o Console** está inundado com todos os tipos de informações.</span><span class="sxs-lookup"><span data-stu-id="c10b3-105">When you surf the web, you may find the **Console** is flooded with all kinds of information.</span></span>  <span data-ttu-id="c10b3-106">Muitas vezes, as informações não são relevantes para você.</span><span class="sxs-lookup"><span data-stu-id="c10b3-106">Often the information isn't relevant to you.</span></span>  <span data-ttu-id="c10b3-107">Como informações sobre o projeto ao vivo que outro desenvolvedor registrou enquanto você depura.</span><span class="sxs-lookup"><span data-stu-id="c10b3-107">Such as information about the live project that another developer logged while you debug.</span></span>  <span data-ttu-id="c10b3-108">Ou mais informações sobre violações e avisos sobre o desempenho do site atual que você não pode alterar.</span><span class="sxs-lookup"><span data-stu-id="c10b3-108">Or more information about violations and warnings about the performance of the current site that you aren't able to change.</span></span>  <span data-ttu-id="c10b3-109">Faz sentido usar as opções de filtro do **Console** para reduzir o ruído.</span><span class="sxs-lookup"><span data-stu-id="c10b3-109">It makes sense to use the filter options of **Console** to reduce the noise.</span></span>  

## <a name="filter-by-log-level"></a><span data-ttu-id="c10b3-110">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="c10b3-110">Filter by log level</span></span>  

<span data-ttu-id="c10b3-111">Cada método do `console` objeto tem um nível de gravidade anexado a ele.</span><span class="sxs-lookup"><span data-stu-id="c10b3-111">Each method of the `console` object has a severity level attached to it.</span></span>  <span data-ttu-id="c10b3-112">Os níveis de gravidade `Verbose` são , , ou `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="c10b3-112">The severity levels are `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="c10b3-113">Exibe os níveis de severidade na documentação [da API][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="c10b3-113">Display the severity levels in the [API documentation][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="c10b3-114">Por exemplo, `console.log()` é uma mensagem de `Info` nível, mas é uma mensagem `console.error()` de `Error` nível.</span><span class="sxs-lookup"><span data-stu-id="c10b3-114">For example, `console.log()` is an `Info`-level message, but `console.error()` is an `Error`-level message.</span></span>  

<span data-ttu-id="c10b3-115">Para filtrar mensagens no **Console,** use o menu suspenso **Nível** de Log.</span><span class="sxs-lookup"><span data-stu-id="c10b3-115">To filter messages in the **Console**, use the **Log Level** dropdown menu.</span></span>  <span data-ttu-id="c10b3-116">Você pode alternar o estado de cada nível.</span><span class="sxs-lookup"><span data-stu-id="c10b3-116">You may toggle the state of each level.</span></span>  <span data-ttu-id="c10b3-117">Para desativar cada nível, remova a marca de seleção ao lado de cada um.</span><span class="sxs-lookup"><span data-stu-id="c10b3-117">To turn off each level, remove the checkmark next to each.</span></span>  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="O menu suspenso filtra mensagens de console usando o nível de log" lightbox="../media/console-filter-dropdown.msft.png":::
    <span data-ttu-id="c10b3-119">O menu suspenso filtra mensagens **de console** usando o nível de log</span><span class="sxs-lookup"><span data-stu-id="c10b3-119">The dropdown menu filters **Console** messages using the log level</span></span>  
:::image-end:::  

<span data-ttu-id="c10b3-120">Como nenhum filtro é aplicado, a figura a seguir exibe dezenas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c10b3-120">Since no filter is applied, the following figure displays dozens of messages.</span></span>  <span data-ttu-id="c10b3-121">Em seguida, reduza e gerencie o número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c10b3-121">Next, reduce and manage the number of messages.</span></span>  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Nenhum conjunto de filtros significa que você pode exibir muitas mensagens de console" lightbox="../media/console-filter-displays-all.msft.png":::
    <span data-ttu-id="c10b3-123">Nenhum conjunto de filtros significa que você pode exibir muitas mensagens de console</span><span class="sxs-lookup"><span data-stu-id="c10b3-123">No filter set means you may display many console messages</span></span>  
:::image-end:::  

<span data-ttu-id="c10b3-124">Escolha ocultar todas as mensagens de nível de aviso para reduzir o ruído.</span><span class="sxs-lookup"><span data-stu-id="c10b3-124">Choose to hide all the Warning-level messages to cut down on the noise.</span></span>  <span data-ttu-id="c10b3-125">Navegue até o **menu suspenso Níveis** de Log e desmarque o `Warnings` nível.</span><span class="sxs-lookup"><span data-stu-id="c10b3-125">Navigate to the **Log Levels** dropdown and uncheck the `Warnings` level.</span></span>  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Ocultar todas as mensagens de nível de aviso no Console para filtrar grande parte do ruído" lightbox="../media/console-filter-hide-warning.msft.png":::
    <span data-ttu-id="c10b3-127">Ocultar todas as mensagens de nível de aviso no **Console** para filtrar grande parte do ruído</span><span class="sxs-lookup"><span data-stu-id="c10b3-127">Hide all the warning level messages in the **Console** to filter much of the noise</span></span>  
:::image-end:::  

## <a name="filter-by-text"></a><span data-ttu-id="c10b3-128">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="c10b3-128">Filter by text</span></span>  

<span data-ttu-id="c10b3-129">Se você quiser revisar mais detalhes, para filtrar mensagens usando texto, digite uma cadeia de caracteres na **caixa de** texto Filtro.</span><span class="sxs-lookup"><span data-stu-id="c10b3-129">If you want to review more detail, to filter messages using text, type a string into the **Filter** textbox.</span></span>  <span data-ttu-id="c10b3-130">Por exemplo, digite na caixa para exibir apenas suas mensagens `block` sobre o navegador bloqueando o carregamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="c10b3-130">For example, type `block` into the box to only display your messages about the browser blocking resources from loading.</span></span>

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Exibe as mensagens que contêm o bloco de palavras" lightbox="../media/console-filter-text.msft.png":::
    <span data-ttu-id="c10b3-132">Exibe as mensagens que contêm a palavra</span><span class="sxs-lookup"><span data-stu-id="c10b3-132">Displays the messages that contain the word</span></span> `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a><span data-ttu-id="c10b3-133">Filtrar por expressão regular</span><span class="sxs-lookup"><span data-stu-id="c10b3-133">Filter by regular expression</span></span>

<span data-ttu-id="c10b3-134">[Expressões regulares][MdnDocsWebJavascriptGuideRegularExpressions] são uma maneira poderosa de filtrar mensagens.</span><span class="sxs-lookup"><span data-stu-id="c10b3-134">[Regular expressions][MdnDocsWebJavascriptGuideRegularExpressions] are a powerful way to filter messages.</span></span>  <span data-ttu-id="c10b3-135">Por exemplo, digite na caixa de texto Filtro para exibir apenas `/^Tracking/` mensagens que começam com o termo \*\*\*\* `Tracking` .</span><span class="sxs-lookup"><span data-stu-id="c10b3-135">For example, type `/^Tracking/` into the **Filter** textbox to only displays messages that start with the term `Tracking`.</span></span>  <span data-ttu-id="c10b3-136">Se você não estiver familiarizado com expressões regulares, [RegExr][|::ref1::|Main] é um ótimo recurso para aprender sobre como usar expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="c10b3-136">If you're unfamiliar with regular expressions, [RegExr][|::ref1::|Main] is a great resource to learn about using regular expressions.</span></span>

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Exibe as mensagens que começam com o filtro de palavras usando uma expressão regular na caixa de texto Filtro" lightbox="../media/console-filter-regex.msft.png":::
    <span data-ttu-id="c10b3-138">Exibe as mensagens que começam com a palavra usando uma expressão regular na caixa de texto `filter` **Filtro**</span><span class="sxs-lookup"><span data-stu-id="c10b3-138">Displays the messages that start with the word `filter` using a regular expression in the **Filter** textbox</span></span>  
:::image-end:::  

## <a name="filter-by-message-source"></a><span data-ttu-id="c10b3-139">Filtrar por fonte de mensagem</span><span class="sxs-lookup"><span data-stu-id="c10b3-139">Filter by message source</span></span>  

<span data-ttu-id="c10b3-140">Você também pode definir que tipo de mensagens deseja exibir e onde cada uma delas foi originada usando a **Barra lateral** do **Console**.</span><span class="sxs-lookup"><span data-stu-id="c10b3-140">You may also define what kind of messages you want to display and where each originated using the **Sidebar** of the **Console**.</span></span>  <span data-ttu-id="c10b3-141">Para fazer isso, escolha o botão **Mostrar barra lateral do console.**</span><span class="sxs-lookup"><span data-stu-id="c10b3-141">To do it, choose the **Show console sidebar** button.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Para abrir a barra lateral, escolha o ícone barra lateral" lightbox="../media/console-filter-sidebar-icon.msft.png":::
    <span data-ttu-id="c10b3-143">Para abrir a **barra lateral,** escolha o botão **Mostrar barra lateral do console**</span><span class="sxs-lookup"><span data-stu-id="c10b3-143">To open the **Sidebar**, choose the **Show console sidebar** button</span></span>  
:::image-end:::  

<span data-ttu-id="c10b3-144">Quando a **Barra lateral** estiver aberta, você poderá exibir o número geral de mensagens e onde cada uma delas se originou.</span><span class="sxs-lookup"><span data-stu-id="c10b3-144">When the **Sidebar** is open, you may display the overall number of messages and where each originated.</span></span>  <span data-ttu-id="c10b3-145">As opções são `All messages` , , , , e `User Messages` `Errors` `Warnings` `Info` `Verbose` .</span><span class="sxs-lookup"><span data-stu-id="c10b3-145">The options are `All messages`, `User Messages`, `Errors`, `Warnings`, `Info`, and `Verbose`.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="A Barra Lateral do Console exibe as diferentes mensagens de origem de fontes" lightbox="../media/console-filter-sidebar-open.msft.png":::
    <span data-ttu-id="c10b3-147">A **Barra Lateral do Console** exibe as diferentes mensagens de origem de fontes</span><span class="sxs-lookup"><span data-stu-id="c10b3-147">The **Console Sidebar** displays the different sources messages originated from</span></span>  
:::image-end:::  

<span data-ttu-id="c10b3-148">Escolha qualquer uma das opções para exibir apenas as mensagens desse tipo.</span><span class="sxs-lookup"><span data-stu-id="c10b3-148">Choose any of the options to display only the messages of that type.</span></span>  <span data-ttu-id="c10b3-149">Por exemplo, para exibir mensagens de usuário, escolha a opção mensagens de usuário para exibir menos ruído.</span><span class="sxs-lookup"><span data-stu-id="c10b3-149">For example, to display user messages, choose the user messages option to display less noise.</span></span>

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Escolha exibir apenas mensagens de usuário no Console usando o filtro na barra lateral" lightbox="../media/console-filter-select-user-messages.msft.png":::
    <span data-ttu-id="c10b3-151">Escolha exibir apenas mensagens de usuário no **Console** usando o filtro na **barra lateral**</span><span class="sxs-lookup"><span data-stu-id="c10b3-151">Choose to display only user messages in the **Console** using the filter in the **Sidebar**</span></span>  
:::image-end:::  

<span data-ttu-id="c10b3-152">Para filtrar mais e expandir a opção, escolha o ícone de triângulo ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="c10b3-152">To filter more and expand the choice, choose the triangle icon next to it.</span></span>  <span data-ttu-id="c10b3-153">Dessa forma, você tem mais opções para exibir apenas mensagens que se originam de uma fonte específica.</span><span class="sxs-lookup"><span data-stu-id="c10b3-153">That way you get more choices to display only messages that originate from a specific source.</span></span>  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Escolha o ícone de seta expande cada uma das seções" lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    <span data-ttu-id="c10b3-155">Escolha o ícone de seta expande cada uma das seções</span><span class="sxs-lookup"><span data-stu-id="c10b3-155">Choose the arrow icon expands each of the sections</span></span>  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Escolha qualquer uma das novas opções para filtrar usando tipo e fonte" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    <span data-ttu-id="c10b3-157">Escolha qualquer uma das novas opções para filtrar usando tipo e fonte</span><span class="sxs-lookup"><span data-stu-id="c10b3-157">Choose any of the new options to filter using type and source</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c10b3-158">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c10b3-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
