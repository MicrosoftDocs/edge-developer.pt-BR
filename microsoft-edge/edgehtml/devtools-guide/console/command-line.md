---
description: Usar a linha de comando do console para interagir com uma página em execução
title: DevTools-console-linha de comando
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, linha de comando do console
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d7ea2bef9fa0014e4d61745636a06d508565df91
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231500"
---
# <span data-ttu-id="a356e-104">Linha de comando do console</span><span class="sxs-lookup"><span data-stu-id="a356e-104">Console command line</span></span>

<span data-ttu-id="a356e-105">Use a linha de comando do console para exibir e alterar valores em uma página e executar o código de depuração instantaneamente, tudo isso aproveitando a conclusão de código automático do Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) .</span><span class="sxs-lookup"><span data-stu-id="a356e-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="a356e-106">Basta inserir qualquer JavaScript válido no prompt da linha de comando e pressionar `Enter` para executar.</span><span class="sxs-lookup"><span data-stu-id="a356e-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="a356e-107">Para a entrada de várias linhas, use `Shift+Enter` para adicionar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="a356e-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="a356e-108">Use as `Up` `Down` teclas de direção para navegar pelos comandos de console anteriores que você inseriu durante a sessão atual do devtools.</span><span class="sxs-lookup"><span data-stu-id="a356e-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="a356e-109">Além do JavaScript padrão e da [API do console](./console-api.md), o console também oferece suporte aos seguintes comandos para:</span><span class="sxs-lookup"><span data-stu-id="a356e-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="a356e-110">Selecionando objetos DOM</span><span class="sxs-lookup"><span data-stu-id="a356e-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="a356e-111">Inspecionar as propriedades do objeto</span><span class="sxs-lookup"><span data-stu-id="a356e-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="a356e-112">Localizando todos os ouvintes de eventos em um determinado objeto</span><span class="sxs-lookup"><span data-stu-id="a356e-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="a356e-113">O script inserido na linha de comando é executado no [escopo global](/scripting/javascript/advanced/variable-scope-javascript) da janela selecionada no momento, a menos que a página seja pausada em um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="a356e-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="a356e-114">Os comandos de console inseridos durante a pausa da página serão executados no [escopo local](/scripting/javascript/advanced/variable-scope-javascript) da função atual dentro da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="a356e-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="a356e-115">O console tem um menu suspenso de contexto de execução de **destino** logo acima da área de saída do console.</span><span class="sxs-lookup"><span data-stu-id="a356e-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="a356e-116">A seleção padrão é o documento de nível superior, **_top**.</span><span class="sxs-lookup"><span data-stu-id="a356e-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="a356e-117">Qualquer iframe no documento ou extensões em execução também aparecerão como opções, permitindo que você execute comandos de forma alternada nesses escopos.</span><span class="sxs-lookup"><span data-stu-id="a356e-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="a356e-118">Seletores DOM</span><span class="sxs-lookup"><span data-stu-id="a356e-118">DOM selectors</span></span>
<span data-ttu-id="a356e-119">Esses seletores de console fornecem abreviações simples para acessar rapidamente objetos no DOM:</span><span class="sxs-lookup"><span data-stu-id="a356e-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="a356e-120">$ (*Cadeia de caracteres do seletor CSS*)</span><span class="sxs-lookup"><span data-stu-id="a356e-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="a356e-121">Retorna o primeiro elemento dentro do documento que corresponde à cadeia de caracteres do [seletor CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  especificado (ou grupo de seletores separados por vírgula).</span><span class="sxs-lookup"><span data-stu-id="a356e-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="a356e-122">Abreviação de [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="a356e-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="a356e-123">Exemplo: Abra o console e digite `$('#main')` para retornar o objeto div com `id='main'` nesta página.</span><span class="sxs-lookup"><span data-stu-id="a356e-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Exemplo de uso do seletor ' $ '](../media/console_cmd_$.png)

### <span data-ttu-id="a356e-125">$ $ (*Cadeia de caracteres do seletor CSS*)</span><span class="sxs-lookup"><span data-stu-id="a356e-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="a356e-126">Retorna uma matriz de elementos dentro do documento que corresponde à cadeia de caracteres do [seletor CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  especificado (ou grupo de seletores separados por vírgula).</span><span class="sxs-lookup"><span data-stu-id="a356e-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="a356e-127">Abreviação de [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="a356e-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="a356e-128">Exemplo: Abra o console e digite `$$('.container')` para retornar todos os objetos div com `class='container'` nesta página.</span><span class="sxs-lookup"><span data-stu-id="a356e-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Exemplo de uso do seletor ' $ $ '](../media/console_cmd_$$.png)

### <span data-ttu-id="a356e-130">$0, $1, $2,...</span><span class="sxs-lookup"><span data-stu-id="a356e-130">$0, $1, $2,...</span></span>
<span data-ttu-id="a356e-131">Retorna os últimos elementos selecionados no painel [**elementos**](../elements.md) , onde `$0` representa o item atualmente selecionado, `$1` foi o item selecionado antes dele e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a356e-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="a356e-132">Exemplo: abrir DevTools na guia **elementos** , pressione `CTRL + B` para ativar a ferramenta **selecionar elemento** e clique em uma área desta página com o mouse.</span><span class="sxs-lookup"><span data-stu-id="a356e-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="a356e-133">Agora, abra o console e digite `$0` para retornar o elemento que você acabou de clicar.</span><span class="sxs-lookup"><span data-stu-id="a356e-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Exemplo de uso do seletor ' $0 '](../media/console_cmd_$0.png)

### <span data-ttu-id="a356e-135">$x (*expressão XPath*)</span><span class="sxs-lookup"><span data-stu-id="a356e-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="a356e-136">Retorna uma matriz de elementos correspondentes à expressão [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) especificada.</span><span class="sxs-lookup"><span data-stu-id="a356e-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="a356e-137">Exemplo: Abra o console e digite `$x('//script[@defer]')` para retornar todos os `<script>` elementos dessa página que contenham um `defer` atributo.</span><span class="sxs-lookup"><span data-stu-id="a356e-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Exemplo de uso do seletor ' $x '](../media/console_cmd_$x.png)

## <span data-ttu-id="a356e-139">Inspeção de objeto</span><span class="sxs-lookup"><span data-stu-id="a356e-139">Object inspection</span></span>

<span data-ttu-id="a356e-140">Esses comandos fornecem maneiras rápidas de inspecionar as propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a356e-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="a356e-141">O objeto especificado deve ser definido no namespace global ou no escopo atual do depurador.</span><span class="sxs-lookup"><span data-stu-id="a356e-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="a356e-142">Dir (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a356e-142">dir(*object*)</span></span>
<span data-ttu-id="a356e-143">Retorna uma lista de modos de exibição de árvore de propriedades do objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a356e-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="a356e-144">Exemplo: Abra o console e digite `dir(document)` para ver as propriedades de objeto do objeto de documento que representam esta página.</span><span class="sxs-lookup"><span data-stu-id="a356e-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Exemplo de uso do método ' dir '](../media/console_cmd_dir.png)

### <span data-ttu-id="a356e-146">Keys (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a356e-146">keys(*object*)</span></span>
<span data-ttu-id="a356e-147">Retorna uma matriz de nomes de propriedade anexada ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a356e-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="a356e-148">Exemplo: Abra o console e digite `keys(window)` para retornar todas as propriedades definidas no objeto da janela global.</span><span class="sxs-lookup"><span data-stu-id="a356e-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Exemplo de uso do método ' Keys '](../media/console_cmd_keys.png)

### <span data-ttu-id="a356e-150">valores (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a356e-150">values(*object*)</span></span>
<span data-ttu-id="a356e-151">Retorna uma matriz de valores de propriedade anexados ao objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a356e-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="a356e-152">Exemplo: Abra o console e digite `values(window)` para retornar os valores de todas as propriedades (chaves) definidas no objeto da janela global.</span><span class="sxs-lookup"><span data-stu-id="a356e-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Exemplo de uso do método ' Values '](../media/console_cmd_values.png)

## <span data-ttu-id="a356e-154">Ouvintes de eventos</span><span class="sxs-lookup"><span data-stu-id="a356e-154">Event listeners</span></span>

<span data-ttu-id="a356e-155">Esse comando permite que você inspecione os ouvintes de eventos registrados para um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="a356e-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="a356e-156">O objeto especificado deve ser definido no namespace global ou no escopo atual do depurador.</span><span class="sxs-lookup"><span data-stu-id="a356e-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="a356e-157">getEventListeners (*objeto*)</span><span class="sxs-lookup"><span data-stu-id="a356e-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="a356e-158">Retorna um objeto que contém uma chave para cada tipo de evento registrado no objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="a356e-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="a356e-159">O valor de cada chave é uma matriz de ouvintes de eventos e suas informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a356e-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="a356e-160">Exemplo: Abra o console e digite `getEventListeners(document)` para ver todos os ouvintes de eventos registrados no objeto de documento desta página.</span><span class="sxs-lookup"><span data-stu-id="a356e-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Exemplo de uso do método ' getEventListeners '](../media/console_cmd_getEventListeners.png)
