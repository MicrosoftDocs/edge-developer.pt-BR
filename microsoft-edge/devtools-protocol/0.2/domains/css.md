---
description: Referência para o domínio CSS. Esse domínio expõe operações CSS de leitura/gravação. Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado. Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes. Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM). Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.
title: Protocolo CSS Domain-DevTools versão 0,2
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 939eda0ae2f5228657d35899ab75b39493eff917
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561344"
---
# <span data-ttu-id="a1807-108">CSS</span><span class="sxs-lookup"><span data-stu-id="a1807-108">CSS</span></span>
<span data-ttu-id="a1807-109">Esse domínio expõe operações CSS de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a1807-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="a1807-110">Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="a1807-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="a1807-111">Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="a1807-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="a1807-112">Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM).</span><span class="sxs-lookup"><span data-stu-id="a1807-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="a1807-113">Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.</span><span class="sxs-lookup"><span data-stu-id="a1807-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="a1807-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a1807-114">Methods</span></span>**](#methods) | <span data-ttu-id="a1807-115">[habilitar](#enable), [desabilitar](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="a1807-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="a1807-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="a1807-116">Events</span></span>**](#events) | <span data-ttu-id="a1807-117">[styleSheetAdded](#stylesheetadded), [stylesheetchanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="a1807-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="a1807-118">Tipos</span><span class="sxs-lookup"><span data-stu-id="a1807-118">Types</span></span>**](#types) | <span data-ttu-id="a1807-119">[Stylesheetid](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [selectorlist](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span><span class="sxs-lookup"><span data-stu-id="a1807-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="a1807-120">Dependências</span><span class="sxs-lookup"><span data-stu-id="a1807-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="a1807-121">DOM</span><span class="sxs-lookup"><span data-stu-id="a1807-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="a1807-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="a1807-122">Methods</span></span>

### <span data-ttu-id="a1807-123">Habilitar</span><span class="sxs-lookup"><span data-stu-id="a1807-123">enable</span></span>
<span data-ttu-id="a1807-124">Habilita o agente CSS para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="a1807-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="a1807-125">Os clientes não devem presumir que o agente de CSS foi habilitado até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="a1807-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="a1807-126">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="a1807-126">disable</span></span>
<span data-ttu-id="a1807-127">Desabilita o agente CSS para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="a1807-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="a1807-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="a1807-128">getInlineStylesForNode</span></span>
<span data-ttu-id="a1807-129">Retorna os estilos embutidos definidos (explicitamente no atributo "Style" e implicitamente, usando atributos DOM) para um nó DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="a1807-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-131">NodeId</span><span class="sxs-lookup"><span data-stu-id="a1807-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-132">Devolver</span><span class="sxs-lookup"><span data-stu-id="a1807-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-133">inlinestyle</span><span class="sxs-lookup"><span data-stu-id="a1807-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="a1807-134">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-135">Estilo embutido para o nó DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="a1807-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-136">attributestyle</span><span class="sxs-lookup"><span data-stu-id="a1807-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="a1807-137">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-138">Estilo de elemento definido pelo atributo (por exemplo, resultante de "width = 20 Height = 100%").</span><span class="sxs-lookup"><span data-stu-id="a1807-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a1807-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="a1807-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="a1807-140">Retorna os estilos solicitados para um nó DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="a1807-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-141">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-142">NodeId</span><span class="sxs-lookup"><span data-stu-id="a1807-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-143">Devolver</span><span class="sxs-lookup"><span data-stu-id="a1807-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-144">inlinestyle</span><span class="sxs-lookup"><span data-stu-id="a1807-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="a1807-145">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-146">Estilo embutido para o nó DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="a1807-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-147">attributestyle</span><span class="sxs-lookup"><span data-stu-id="a1807-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="a1807-148">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-149">Estilo de elemento definido pelo atributo (por exemplo, resultante de "width = 20 Height = 100%").</span><span class="sxs-lookup"><span data-stu-id="a1807-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="a1807-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="a1807-151">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="a1807-152">Regras CSS correspondentes a esse nó, de todas as folhas de estilo aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="a1807-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="a1807-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="a1807-154">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="a1807-155">O pseudo estilo corresponde a este nó.</span><span class="sxs-lookup"><span data-stu-id="a1807-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-156">substituir</span><span class="sxs-lookup"><span data-stu-id="a1807-156">inherited</span></span> <br /> <i><span data-ttu-id="a1807-157">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="a1807-158">Uma cadeia de estilos herdados (do pai do nó imediato até a raiz da árvore DOM).</span><span class="sxs-lookup"><span data-stu-id="a1807-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="a1807-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="a1807-160">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="a1807-161">Uma lista de animações em quadros-chave CSS que correspondem a esse nó.</span><span class="sxs-lookup"><span data-stu-id="a1807-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a1807-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="a1807-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="a1807-163">Solicita informações sobre as fontes da plataforma que usamos para renderizar os textnodes filho no nó fornecido.</span><span class="sxs-lookup"><span data-stu-id="a1807-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-164">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-165">NodeId</span><span class="sxs-lookup"><span data-stu-id="a1807-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-166">Devolver</span><span class="sxs-lookup"><span data-stu-id="a1807-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-167">Font</span><span class="sxs-lookup"><span data-stu-id="a1807-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="a1807-168">Estatísticas de uso para todas as fontes empregadas da plataforma.</span><span class="sxs-lookup"><span data-stu-id="a1807-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a1807-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="a1807-169">getComputedStyleForNode</span></span>
<span data-ttu-id="a1807-170">Retorna o estilo calculado de um nó DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="a1807-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-171">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-172">NodeId</span><span class="sxs-lookup"><span data-stu-id="a1807-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-173">Devolver</span><span class="sxs-lookup"><span data-stu-id="a1807-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-174">computedStyle</span><span class="sxs-lookup"><span data-stu-id="a1807-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="a1807-175">Estilo calculado para o nó DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="a1807-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="a1807-176">Eventos</span><span class="sxs-lookup"><span data-stu-id="a1807-176">Events</span></span>

### <span data-ttu-id="a1807-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="a1807-177">styleSheetAdded</span></span>
<span data-ttu-id="a1807-178">Disparado sempre que uma folha de estilo de documento ativa é adicionada.</span><span class="sxs-lookup"><span data-stu-id="a1807-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-179">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-180">header</span><span class="sxs-lookup"><span data-stu-id="a1807-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="a1807-181">Metainformações da folha de estilos adicionadas.</span><span class="sxs-lookup"><span data-stu-id="a1807-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a1807-182">styleSheetchanged</span><span class="sxs-lookup"><span data-stu-id="a1807-182">styleSheetChanged</span></span>
<span data-ttu-id="a1807-183">Acionado sempre que uma folha de estilos é alterada como resultado da operação do cliente.</span><span class="sxs-lookup"><span data-stu-id="a1807-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-184">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-185">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="a1807-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="a1807-186">styleSheetRemoved</span></span>
<span data-ttu-id="a1807-187">Disparado sempre que uma folha de estilos de documento ativa é removida.</span><span class="sxs-lookup"><span data-stu-id="a1807-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-188">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1807-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-189">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="a1807-190">Identificador da folha de estilos removida.</span><span class="sxs-lookup"><span data-stu-id="a1807-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="a1807-191">Tipos</span><span class="sxs-lookup"><span data-stu-id="a1807-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="a1807-192">StyleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="a1807-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="a1807-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="a1807-194">Coleção de regras CSS para um único pseudocódigo.</span><span class="sxs-lookup"><span data-stu-id="a1807-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-195">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-196">pseudotype</span><span class="sxs-lookup"><span data-stu-id="a1807-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="a1807-197">Pseudo-tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="a1807-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-198">corresponde</span><span class="sxs-lookup"><span data-stu-id="a1807-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="a1807-199">Correspondências de regras CSS aplicáveis ao pseudo estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="a1807-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="a1807-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="a1807-201">Coleção de regras CSS herdada do nó ancestral.</span><span class="sxs-lookup"><span data-stu-id="a1807-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-202">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-203">inlinestyle</span><span class="sxs-lookup"><span data-stu-id="a1807-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="a1807-204">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-205">O estilo embutido do nó ancestral, se houver, na cadeia de herança de estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="a1807-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="a1807-207">Correspondências de regras CSS correspondentes ao nó ancestral na cadeia de herança de estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="a1807-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="a1807-208">RuleMatch</span></span> `object`

<span data-ttu-id="a1807-209">Corresponder dados de uma regra CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-210">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-211">das</span><span class="sxs-lookup"><span data-stu-id="a1807-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="a1807-212">Regra CSS na coincidência.</span><span class="sxs-lookup"><span data-stu-id="a1807-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="a1807-213">Value</span><span class="sxs-lookup"><span data-stu-id="a1807-213">Value</span></span> `object`

<span data-ttu-id="a1807-214">Dados para um seletor simples (eles são delimitados por vírgulas em uma lista seletora).</span><span class="sxs-lookup"><span data-stu-id="a1807-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-215">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-216">texto</span><span class="sxs-lookup"><span data-stu-id="a1807-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-217">Valor do texto.</span><span class="sxs-lookup"><span data-stu-id="a1807-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-218">gama</span><span class="sxs-lookup"><span data-stu-id="a1807-218">range</span></span> <br /> <i><span data-ttu-id="a1807-219">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="a1807-220">Intervalo de valores no recurso subjacente (se disponível).</span><span class="sxs-lookup"><span data-stu-id="a1807-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="a1807-221">Seletor de seletor</span><span class="sxs-lookup"><span data-stu-id="a1807-221">SelectorList</span></span> `object`

<span data-ttu-id="a1807-222">Dados da lista seletor.</span><span class="sxs-lookup"><span data-stu-id="a1807-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-223">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-224">seletores</span><span class="sxs-lookup"><span data-stu-id="a1807-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="a1807-225">Seletores na lista.</span><span class="sxs-lookup"><span data-stu-id="a1807-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-226">texto</span><span class="sxs-lookup"><span data-stu-id="a1807-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-227">Texto do seletor de regra.</span><span class="sxs-lookup"><span data-stu-id="a1807-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="a1807-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="a1807-228">CSSRule</span></span> `object`

<span data-ttu-id="a1807-229">Representação de regra CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-230">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-231">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="a1807-232">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="a1807-233">O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</span><span class="sxs-lookup"><span data-stu-id="a1807-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-234">seletor de seletor</span><span class="sxs-lookup"><span data-stu-id="a1807-234">selectorList</span></span> <br /> <i><span data-ttu-id="a1807-235">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="a1807-236">Dados do seletor de regras.</span><span class="sxs-lookup"><span data-stu-id="a1807-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-237">Origin</span><span class="sxs-lookup"><span data-stu-id="a1807-237">origin</span></span> <br /> <i><span data-ttu-id="a1807-238">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="a1807-239">Origem da folha de estilos pai.</span><span class="sxs-lookup"><span data-stu-id="a1807-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-240">estilo</span><span class="sxs-lookup"><span data-stu-id="a1807-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-241">Declaração de estilo associada.</span><span class="sxs-lookup"><span data-stu-id="a1807-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-242">mídia</span><span class="sxs-lookup"><span data-stu-id="a1807-242">media</span></span> <br /> <i><span data-ttu-id="a1807-243">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="a1807-244">Matriz de lista de mídia (para regras que envolvem consultas de mídia).</span><span class="sxs-lookup"><span data-stu-id="a1807-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="a1807-245">A matriz enumera consultas de mídia começando com a mais interna, indo para cima.</span><span class="sxs-lookup"><span data-stu-id="a1807-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="a1807-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="a1807-246">SourceRange</span></span> `object`

<span data-ttu-id="a1807-247">Intervalo de texto em um recurso.</span><span class="sxs-lookup"><span data-stu-id="a1807-247">Text range within a resource.</span></span> <span data-ttu-id="a1807-248">Todos os números são baseados em zero.</span><span class="sxs-lookup"><span data-stu-id="a1807-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-249">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-250">início</span><span class="sxs-lookup"><span data-stu-id="a1807-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a1807-251">Linha de início do intervalo.</span><span class="sxs-lookup"><span data-stu-id="a1807-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-252">startColumn</span><span class="sxs-lookup"><span data-stu-id="a1807-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a1807-253">Coluna inicial do intervalo (inclusivo).</span><span class="sxs-lookup"><span data-stu-id="a1807-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-254">Line</span><span class="sxs-lookup"><span data-stu-id="a1807-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a1807-255">Linha final do intervalo</span><span class="sxs-lookup"><span data-stu-id="a1807-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-256">Coluna de EndColumn</span><span class="sxs-lookup"><span data-stu-id="a1807-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="a1807-257">Coluna final do intervalo (exclusivo).</span><span class="sxs-lookup"><span data-stu-id="a1807-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="a1807-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="a1807-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-259">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-260">name</span><span class="sxs-lookup"><span data-stu-id="a1807-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-261">Nome abreviado.</span><span class="sxs-lookup"><span data-stu-id="a1807-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-262">value</span><span class="sxs-lookup"><span data-stu-id="a1807-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-263">Valor Abreviado.</span><span class="sxs-lookup"><span data-stu-id="a1807-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-264">principais</span><span class="sxs-lookup"><span data-stu-id="a1807-264">important</span></span> <br /> <i><span data-ttu-id="a1807-265">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-266">Se a propriedade tem a anotação "! importante" (implica `false` se estar ausente).</span><span class="sxs-lookup"><span data-stu-id="a1807-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="a1807-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="a1807-267">CSSStyle</span></span> `object`

<span data-ttu-id="a1807-268">Representação de estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-269">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-270">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="a1807-271">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="a1807-272">O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</span><span class="sxs-lookup"><span data-stu-id="a1807-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="a1807-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="a1807-274">Propriedades CSS no estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="a1807-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="a1807-276">Valores calculados para todas as abreviações encontradas no estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-277">cssText</span><span class="sxs-lookup"><span data-stu-id="a1807-277">cssText</span></span> <br /> <i><span data-ttu-id="a1807-278">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-279">Texto da declaração de estilo (se disponível).</span><span class="sxs-lookup"><span data-stu-id="a1807-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-280">gama</span><span class="sxs-lookup"><span data-stu-id="a1807-280">range</span></span> <br /> <i><span data-ttu-id="a1807-281">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="a1807-282">Intervalo de declaração de estilo na folha de estilos delimitadora (se disponível).</span><span class="sxs-lookup"><span data-stu-id="a1807-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="a1807-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="a1807-283">CSSProperty</span></span> `object`

<span data-ttu-id="a1807-284">Dados de declaração de propriedade CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-285">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-286">name</span><span class="sxs-lookup"><span data-stu-id="a1807-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-287">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1807-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-288">value</span><span class="sxs-lookup"><span data-stu-id="a1807-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-289">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1807-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-290">principais</span><span class="sxs-lookup"><span data-stu-id="a1807-290">important</span></span> <br /> <i><span data-ttu-id="a1807-291">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-292">Se a propriedade tem a anotação "! importante" (implica `false` se estar ausente).</span><span class="sxs-lookup"><span data-stu-id="a1807-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-293">implícito</span><span class="sxs-lookup"><span data-stu-id="a1807-293">implicit</span></span> <br /> <i><span data-ttu-id="a1807-294">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-295">Se a propriedade é implícita (implica `false` se estiver ausente).</span><span class="sxs-lookup"><span data-stu-id="a1807-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-296">texto</span><span class="sxs-lookup"><span data-stu-id="a1807-296">text</span></span> <br /> <i><span data-ttu-id="a1807-297">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-298">O texto completo da propriedade, conforme especificado no estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="a1807-299">parsedOk</span></span> <br /> <i><span data-ttu-id="a1807-300">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-301">Se a propriedade é compreendida pelo navegador (implica `true` se estiver ausente).</span><span class="sxs-lookup"><span data-stu-id="a1807-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-302">ativo</span><span class="sxs-lookup"><span data-stu-id="a1807-302">disabled</span></span> <br /> <i><span data-ttu-id="a1807-303">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-304">Se a propriedade está desabilitada pelo usuário (apenas para Propriedades baseadas na origem).</span><span class="sxs-lookup"><span data-stu-id="a1807-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-305">gama</span><span class="sxs-lookup"><span data-stu-id="a1807-305">range</span></span> <br /> <i><span data-ttu-id="a1807-306">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="a1807-307">Todo o intervalo de propriedades na declaração de estilo delimitador (se disponível).</span><span class="sxs-lookup"><span data-stu-id="a1807-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="a1807-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="a1807-308">CSSMedia</span></span> `object`

<span data-ttu-id="a1807-309">Descritor de regras de mídia CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-310">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-311">texto</span><span class="sxs-lookup"><span data-stu-id="a1807-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-312">Texto de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-313">bibliográfica</span><span class="sxs-lookup"><span data-stu-id="a1807-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="a1807-314">Valores permitidos: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="a1807-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="a1807-315">Fonte da consulta de mídia: "mediaRule" se especificado por uma regra de @media, "importRule" se especificado por uma regra de @import, "linkedSheet" se especificado por um atributo "Media" na marca de LINK de uma folha de estilos vinculada, "inlineSheet", se especificado por um atributo "Media" em uma marca de estilo da folha de estilos embutida.</span><span class="sxs-lookup"><span data-stu-id="a1807-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="a1807-316">sourceURL</span></span> <br /> <i><span data-ttu-id="a1807-317">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-318">URL do documento que contém a descrição da consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-319">gama</span><span class="sxs-lookup"><span data-stu-id="a1807-319">range</span></span> <br /> <i><span data-ttu-id="a1807-320">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="a1807-321">O intervalo de cabeçalhos de regra (@media ou @import) associado na folha de estilos delimitadora (se disponível).</span><span class="sxs-lookup"><span data-stu-id="a1807-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-322">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="a1807-323">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="a1807-324">Identificador da folha de estilos que contém esse objeto (se houver).</span><span class="sxs-lookup"><span data-stu-id="a1807-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-325">medialist</span><span class="sxs-lookup"><span data-stu-id="a1807-325">mediaList</span></span> <br /> <i><span data-ttu-id="a1807-326">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="a1807-327">Matriz de consultas de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="a1807-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="a1807-328">MediaQuery</span></span> `object`

<span data-ttu-id="a1807-329">Descritor de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-330">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-331">expressão</span><span class="sxs-lookup"><span data-stu-id="a1807-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="a1807-332">Matriz de expressões de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-333">active</span><span class="sxs-lookup"><span data-stu-id="a1807-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-334">Se a condição de consulta de mídia é satisfeita.</span><span class="sxs-lookup"><span data-stu-id="a1807-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="a1807-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="a1807-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="a1807-336">Descritor de expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-337">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-338">value</span><span class="sxs-lookup"><span data-stu-id="a1807-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="a1807-339">Valor da expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-340">organizacional</span><span class="sxs-lookup"><span data-stu-id="a1807-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-341">Unidades de expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-342">recurso</span><span class="sxs-lookup"><span data-stu-id="a1807-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-343">Recurso de expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="a1807-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="a1807-344">valueRange</span></span> <br /> <i><span data-ttu-id="a1807-345">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="a1807-346">O intervalo associado do valor do texto na folha de estilos de delimitador (se disponível).</span><span class="sxs-lookup"><span data-stu-id="a1807-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="a1807-347">computedLength</span></span> <br /> <i><span data-ttu-id="a1807-348">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="a1807-349">Duração calculada da expressão de consulta de mídia (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="a1807-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="a1807-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="a1807-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="a1807-351">Informações sobre a quantidade de glifos que foram renderizados com determinada fonte.</span><span class="sxs-lookup"><span data-stu-id="a1807-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-352">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-353">FamilyName</span><span class="sxs-lookup"><span data-stu-id="a1807-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-354">Nome da família da fonte informado pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="a1807-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="a1807-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-356">Indica se a fonte foi baixada ou resolvida localmente.</span><span class="sxs-lookup"><span data-stu-id="a1807-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="a1807-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="a1807-358">Valor dos glifos renderizados com essa fonte.</span><span class="sxs-lookup"><span data-stu-id="a1807-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="a1807-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="a1807-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="a1807-360">Representação de regras de quadros-chave CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-361">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-362">animationname</span><span class="sxs-lookup"><span data-stu-id="a1807-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="a1807-363">Nome da animação.</span><span class="sxs-lookup"><span data-stu-id="a1807-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-364">quadros-chave</span><span class="sxs-lookup"><span data-stu-id="a1807-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="a1807-365">Lista de quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="a1807-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="a1807-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="a1807-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="a1807-367">Representação de regra do quadro-chave CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-368">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-369">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="a1807-370">opcional</span><span class="sxs-lookup"><span data-stu-id="a1807-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="a1807-371">O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</span><span class="sxs-lookup"><span data-stu-id="a1807-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-372">Origin</span><span class="sxs-lookup"><span data-stu-id="a1807-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="a1807-373">Origem da folha de estilos pai.</span><span class="sxs-lookup"><span data-stu-id="a1807-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-374">keytext</span><span class="sxs-lookup"><span data-stu-id="a1807-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="a1807-375">Texto de chave associado.</span><span class="sxs-lookup"><span data-stu-id="a1807-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-376">estilo</span><span class="sxs-lookup"><span data-stu-id="a1807-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="a1807-377">Declaração de estilo associada.</span><span class="sxs-lookup"><span data-stu-id="a1807-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="a1807-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="a1807-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-379">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-380">name</span><span class="sxs-lookup"><span data-stu-id="a1807-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-381">Nome da propriedade de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="a1807-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-382">value</span><span class="sxs-lookup"><span data-stu-id="a1807-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-383">Valor da propriedade de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="a1807-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="a1807-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="a1807-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="a1807-385">Metainformação da folha de estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="a1807-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="a1807-386">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a1807-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="a1807-387">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="a1807-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="a1807-388">O identificador de folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="a1807-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="a1807-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="a1807-390">URL do recurso de folha de estilo.</span><span class="sxs-lookup"><span data-stu-id="a1807-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-391">ativo</span><span class="sxs-lookup"><span data-stu-id="a1807-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-392">Indica se a folha de estilo está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a1807-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-393">IsInline</span><span class="sxs-lookup"><span data-stu-id="a1807-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="a1807-394">Se essa folha de estilos é criada para marcação de estilo por analisador.</span><span class="sxs-lookup"><span data-stu-id="a1807-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="a1807-395">Este sinalizador não está definido para marcas de estilo Document. Write.</span><span class="sxs-lookup"><span data-stu-id="a1807-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-396">início</span><span class="sxs-lookup"><span data-stu-id="a1807-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="a1807-397">Deslocamento de linha da folha de estilos dentro do recurso (com base em zero).</span><span class="sxs-lookup"><span data-stu-id="a1807-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-398">startColumn</span><span class="sxs-lookup"><span data-stu-id="a1807-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="a1807-399">Deslocamento de coluna da folha de estilos dentro do recurso (com base em zero).</span><span class="sxs-lookup"><span data-stu-id="a1807-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="a1807-400">das</span><span class="sxs-lookup"><span data-stu-id="a1807-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="a1807-401">Tamanho do conteúdo (em caracteres).</span><span class="sxs-lookup"><span data-stu-id="a1807-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="a1807-402">Dependências</span><span class="sxs-lookup"><span data-stu-id="a1807-402">Dependencies</span></span>

[<span data-ttu-id="a1807-403">DOM</span><span class="sxs-lookup"><span data-stu-id="a1807-403">DOM</span></span>](dom.md)
