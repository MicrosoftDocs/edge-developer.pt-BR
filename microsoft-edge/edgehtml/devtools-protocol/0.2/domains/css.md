---
description: Referência para o domínio CSS. Esse domínio expõe operações CSS de leitura/gravação. Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado. Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes. Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM). Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.
title: Protocolo CSS Domain-DevTools versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf5efdef09b7e2d9041cd8536faaff8fb99a7f71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231688"
---
# <span data-ttu-id="c798c-108">CSS</span><span class="sxs-lookup"><span data-stu-id="c798c-108">CSS</span></span>

<span data-ttu-id="c798c-109">Esse domínio expõe operações CSS de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c798c-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="c798c-110">Todos os objetos CSS (folhas de estilo, regras e estilos) têm um associado `id` usado em operações subsequentes no objeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="c798c-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="c798c-111">Cada tipo de objeto tem uma `id` estrutura específica, e não é intercambiável entre objetos de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c798c-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="c798c-112">Objetos CSS podem ser carregados usando-se as `get*ForNode()` chamadas (que aceitam uma ID de nó DOM).</span><span class="sxs-lookup"><span data-stu-id="c798c-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="c798c-113">Um cliente também pode controlar as folhas de estilo por meio dos `styleSheetAdded` / `styleSheetRemoved` eventos e carregar subseqüentemente o conteúdo da folha de estilos usando os `getStyleSheet[Text]()` métodos.</span><span class="sxs-lookup"><span data-stu-id="c798c-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="c798c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c798c-114">Methods</span></span>**](#methods) | <span data-ttu-id="c798c-115">[habilitar](#enable), [desabilitar](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="c798c-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="c798c-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="c798c-116">Events</span></span>**](#events) | <span data-ttu-id="c798c-117">[styleSheetAdded](#stylesheetadded), [stylesheetchanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="c798c-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="c798c-118">Tipos</span><span class="sxs-lookup"><span data-stu-id="c798c-118">Types</span></span>**](#types) | <span data-ttu-id="c798c-119">[Stylesheetid](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [selectorlist](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span><span class="sxs-lookup"><span data-stu-id="c798c-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="c798c-120">Dependências</span><span class="sxs-lookup"><span data-stu-id="c798c-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="c798c-121">DOM</span><span class="sxs-lookup"><span data-stu-id="c798c-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="c798c-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="c798c-122">Methods</span></span>

### <span data-ttu-id="c798c-123">Habilitar</span><span class="sxs-lookup"><span data-stu-id="c798c-123">enable</span></span>
<span data-ttu-id="c798c-124">Habilita o agente CSS para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="c798c-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="c798c-125">Os clientes não devem presumir que o agente de CSS foi habilitado até que o resultado desse comando seja recebido.</span><span class="sxs-lookup"><span data-stu-id="c798c-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="c798c-126">Desabilitar </span><span class="sxs-lookup"><span data-stu-id="c798c-126">disable</span></span>
<span data-ttu-id="c798c-127">Desabilita o agente CSS para a página especificada.</span><span class="sxs-lookup"><span data-stu-id="c798c-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="c798c-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="c798c-128">getInlineStylesForNode</span></span>
<span data-ttu-id="c798c-129">Retorna os estilos embutidos definidos (explicitamente no atributo "Style" e implicitamente, usando atributos DOM) para um nó DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="c798c-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-131">NodeId</span><span class="sxs-lookup"><span data-stu-id="c798c-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-132">Devolver</span><span class="sxs-lookup"><span data-stu-id="c798c-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-133">inlinestyle</span><span class="sxs-lookup"><span data-stu-id="c798c-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="c798c-134">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-135">Estilo embutido para o nó DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="c798c-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-136">attributestyle</span><span class="sxs-lookup"><span data-stu-id="c798c-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="c798c-137">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-138">Estilo de elemento definido pelo atributo (por exemplo, resultante de "width = 20 Height = 100%").</span><span class="sxs-lookup"><span data-stu-id="c798c-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c798c-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="c798c-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="c798c-140">Retorna os estilos solicitados para um nó DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="c798c-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-141">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-142">NodeId</span><span class="sxs-lookup"><span data-stu-id="c798c-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-143">Devolver</span><span class="sxs-lookup"><span data-stu-id="c798c-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-144">inlinestyle</span><span class="sxs-lookup"><span data-stu-id="c798c-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="c798c-145">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-146">Estilo embutido para o nó DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="c798c-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-147">attributestyle</span><span class="sxs-lookup"><span data-stu-id="c798c-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="c798c-148">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-149">Estilo de elemento definido pelo atributo (por exemplo, resultante de "width = 20 Height = 100%").</span><span class="sxs-lookup"><span data-stu-id="c798c-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="c798c-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="c798c-151">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="c798c-152">Regras CSS correspondentes a esse nó, de todas as folhas de estilo aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="c798c-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="c798c-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="c798c-154">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="c798c-155">O pseudo estilo corresponde a este nó.</span><span class="sxs-lookup"><span data-stu-id="c798c-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-156">substituir</span><span class="sxs-lookup"><span data-stu-id="c798c-156">inherited</span></span> <br /> <i><span data-ttu-id="c798c-157">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="c798c-158">Uma cadeia de estilos herdados (do pai do nó imediato até a raiz da árvore DOM).</span><span class="sxs-lookup"><span data-stu-id="c798c-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="c798c-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="c798c-160">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="c798c-161">Uma lista de animações em quadros-chave CSS que correspondem a esse nó.</span><span class="sxs-lookup"><span data-stu-id="c798c-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c798c-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="c798c-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="c798c-163">Solicita informações sobre as fontes da plataforma que usamos para renderizar os textnodes filho no nó fornecido.</span><span class="sxs-lookup"><span data-stu-id="c798c-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-164">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-165">NodeId</span><span class="sxs-lookup"><span data-stu-id="c798c-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-166">Devolver</span><span class="sxs-lookup"><span data-stu-id="c798c-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-167">Font</span><span class="sxs-lookup"><span data-stu-id="c798c-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="c798c-168">Estatísticas de uso para todas as fontes empregadas da plataforma.</span><span class="sxs-lookup"><span data-stu-id="c798c-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c798c-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="c798c-169">getComputedStyleForNode</span></span>
<span data-ttu-id="c798c-170">Retorna o estilo calculado de um nó DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="c798c-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-171">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-172">NodeId</span><span class="sxs-lookup"><span data-stu-id="c798c-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-173">Devolver</span><span class="sxs-lookup"><span data-stu-id="c798c-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-174">computedStyle</span><span class="sxs-lookup"><span data-stu-id="c798c-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="c798c-175">Estilo calculado para o nó DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="c798c-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="c798c-176">Eventos</span><span class="sxs-lookup"><span data-stu-id="c798c-176">Events</span></span>

### <span data-ttu-id="c798c-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="c798c-177">styleSheetAdded</span></span>
<span data-ttu-id="c798c-178">Disparado sempre que uma folha de estilo de documento ativa é adicionada.</span><span class="sxs-lookup"><span data-stu-id="c798c-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-179">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-180">header</span><span class="sxs-lookup"><span data-stu-id="c798c-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="c798c-181">Metainformações da folha de estilos adicionadas.</span><span class="sxs-lookup"><span data-stu-id="c798c-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c798c-182">styleSheetchanged</span><span class="sxs-lookup"><span data-stu-id="c798c-182">styleSheetChanged</span></span>
<span data-ttu-id="c798c-183">Acionado sempre que uma folha de estilos é alterada como resultado da operação do cliente.</span><span class="sxs-lookup"><span data-stu-id="c798c-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-184">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-185">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="c798c-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="c798c-186">styleSheetRemoved</span></span>
<span data-ttu-id="c798c-187">Disparado sempre que uma folha de estilos de documento ativa é removida.</span><span class="sxs-lookup"><span data-stu-id="c798c-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-188">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c798c-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-189">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="c798c-190">Identificador da folha de estilos removida.</span><span class="sxs-lookup"><span data-stu-id="c798c-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="c798c-191">Tipos</span><span class="sxs-lookup"><span data-stu-id="c798c-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="c798c-192">StyleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="c798c-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="c798c-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="c798c-194">Coleção de regras CSS para um único pseudocódigo.</span><span class="sxs-lookup"><span data-stu-id="c798c-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-195">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-196">pseudotype</span><span class="sxs-lookup"><span data-stu-id="c798c-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="c798c-197">Pseudo-tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="c798c-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-198">corresponde</span><span class="sxs-lookup"><span data-stu-id="c798c-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="c798c-199">Correspondências de regras CSS aplicáveis ao pseudo estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="c798c-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="c798c-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="c798c-201">Coleção de regras CSS herdada do nó ancestral.</span><span class="sxs-lookup"><span data-stu-id="c798c-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-202">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-203">inlinestyle</span><span class="sxs-lookup"><span data-stu-id="c798c-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="c798c-204">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-205">O estilo embutido do nó ancestral, se houver, na cadeia de herança de estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="c798c-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="c798c-207">Correspondências de regras CSS correspondentes ao nó ancestral na cadeia de herança de estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="c798c-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="c798c-208">RuleMatch</span></span> `object`

<span data-ttu-id="c798c-209">Corresponder dados de uma regra CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-210">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-211">das</span><span class="sxs-lookup"><span data-stu-id="c798c-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="c798c-212">Regra CSS na coincidência.</span><span class="sxs-lookup"><span data-stu-id="c798c-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="c798c-213">Valor</span><span class="sxs-lookup"><span data-stu-id="c798c-213">Value</span></span> `object`

<span data-ttu-id="c798c-214">Dados para um seletor simples (eles são delimitados por vírgulas em uma lista seletora).</span><span class="sxs-lookup"><span data-stu-id="c798c-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-215">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-216">texto</span><span class="sxs-lookup"><span data-stu-id="c798c-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-217">Valor do texto.</span><span class="sxs-lookup"><span data-stu-id="c798c-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-218">gama</span><span class="sxs-lookup"><span data-stu-id="c798c-218">range</span></span> <br /> <i><span data-ttu-id="c798c-219">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="c798c-220">Intervalo de valores no recurso subjacente (se disponível).</span><span class="sxs-lookup"><span data-stu-id="c798c-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="c798c-221">Seletor de seletor</span><span class="sxs-lookup"><span data-stu-id="c798c-221">SelectorList</span></span> `object`

<span data-ttu-id="c798c-222">Dados da lista seletor.</span><span class="sxs-lookup"><span data-stu-id="c798c-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-223">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-224">seletores</span><span class="sxs-lookup"><span data-stu-id="c798c-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="c798c-225">Seletores na lista.</span><span class="sxs-lookup"><span data-stu-id="c798c-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-226">texto</span><span class="sxs-lookup"><span data-stu-id="c798c-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-227">Texto do seletor de regra.</span><span class="sxs-lookup"><span data-stu-id="c798c-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="c798c-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="c798c-228">CSSRule</span></span> `object`

<span data-ttu-id="c798c-229">Representação de regra CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-230">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-231">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="c798c-232">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="c798c-233">O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</span><span class="sxs-lookup"><span data-stu-id="c798c-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-234">seletor de seletor</span><span class="sxs-lookup"><span data-stu-id="c798c-234">selectorList</span></span> <br /> <i><span data-ttu-id="c798c-235">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="c798c-236">Dados do seletor de regras.</span><span class="sxs-lookup"><span data-stu-id="c798c-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-237">Origin</span><span class="sxs-lookup"><span data-stu-id="c798c-237">origin</span></span> <br /> <i><span data-ttu-id="c798c-238">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="c798c-239">Origem da folha de estilos pai.</span><span class="sxs-lookup"><span data-stu-id="c798c-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-240">estilo</span><span class="sxs-lookup"><span data-stu-id="c798c-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-241">Declaração de estilo associada.</span><span class="sxs-lookup"><span data-stu-id="c798c-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-242">mídia</span><span class="sxs-lookup"><span data-stu-id="c798c-242">media</span></span> <br /> <i><span data-ttu-id="c798c-243">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="c798c-244">Matriz de lista de mídia (para regras que envolvem consultas de mídia).</span><span class="sxs-lookup"><span data-stu-id="c798c-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="c798c-245">A matriz enumera consultas de mídia começando com a mais interna, indo para cima.</span><span class="sxs-lookup"><span data-stu-id="c798c-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="c798c-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="c798c-246">SourceRange</span></span> `object`

<span data-ttu-id="c798c-247">Intervalo de texto em um recurso.</span><span class="sxs-lookup"><span data-stu-id="c798c-247">Text range within a resource.</span></span> <span data-ttu-id="c798c-248">Todos os números são baseados em zero.</span><span class="sxs-lookup"><span data-stu-id="c798c-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-249">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-250">início</span><span class="sxs-lookup"><span data-stu-id="c798c-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c798c-251">Linha de início do intervalo.</span><span class="sxs-lookup"><span data-stu-id="c798c-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-252">startColumn</span><span class="sxs-lookup"><span data-stu-id="c798c-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c798c-253">Coluna inicial do intervalo (inclusivo).</span><span class="sxs-lookup"><span data-stu-id="c798c-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-254">Line</span><span class="sxs-lookup"><span data-stu-id="c798c-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c798c-255">Linha final do intervalo</span><span class="sxs-lookup"><span data-stu-id="c798c-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-256">Coluna de EndColumn</span><span class="sxs-lookup"><span data-stu-id="c798c-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="c798c-257">Coluna final do intervalo (exclusivo).</span><span class="sxs-lookup"><span data-stu-id="c798c-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="c798c-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="c798c-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-259">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-260">name</span><span class="sxs-lookup"><span data-stu-id="c798c-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-261">Nome abreviado.</span><span class="sxs-lookup"><span data-stu-id="c798c-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-262">value</span><span class="sxs-lookup"><span data-stu-id="c798c-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-263">Valor Abreviado.</span><span class="sxs-lookup"><span data-stu-id="c798c-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-264">principais</span><span class="sxs-lookup"><span data-stu-id="c798c-264">important</span></span> <br /> <i><span data-ttu-id="c798c-265">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-266">Se a propriedade tem a anotação "! importante" (implica `false` se estar ausente).</span><span class="sxs-lookup"><span data-stu-id="c798c-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="c798c-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="c798c-267">CSSStyle</span></span> `object`

<span data-ttu-id="c798c-268">Representação de estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-269">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-270">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="c798c-271">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="c798c-272">O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</span><span class="sxs-lookup"><span data-stu-id="c798c-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="c798c-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="c798c-274">Propriedades CSS no estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="c798c-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="c798c-276">Valores calculados para todas as abreviações encontradas no estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-277">cssText</span><span class="sxs-lookup"><span data-stu-id="c798c-277">cssText</span></span> <br /> <i><span data-ttu-id="c798c-278">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-279">Texto da declaração de estilo (se disponível).</span><span class="sxs-lookup"><span data-stu-id="c798c-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-280">gama</span><span class="sxs-lookup"><span data-stu-id="c798c-280">range</span></span> <br /> <i><span data-ttu-id="c798c-281">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="c798c-282">Intervalo de declaração de estilo na folha de estilos delimitadora (se disponível).</span><span class="sxs-lookup"><span data-stu-id="c798c-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="c798c-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="c798c-283">CSSProperty</span></span> `object`

<span data-ttu-id="c798c-284">Dados de declaração de propriedade CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-285">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-286">name</span><span class="sxs-lookup"><span data-stu-id="c798c-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-287">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c798c-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-288">value</span><span class="sxs-lookup"><span data-stu-id="c798c-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-289">O valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c798c-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-290">principais</span><span class="sxs-lookup"><span data-stu-id="c798c-290">important</span></span> <br /> <i><span data-ttu-id="c798c-291">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-292">Se a propriedade tem a anotação "! importante" (implica `false` se estar ausente).</span><span class="sxs-lookup"><span data-stu-id="c798c-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-293">implícito</span><span class="sxs-lookup"><span data-stu-id="c798c-293">implicit</span></span> <br /> <i><span data-ttu-id="c798c-294">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-295">Se a propriedade é implícita (implica `false` se estiver ausente).</span><span class="sxs-lookup"><span data-stu-id="c798c-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-296">texto</span><span class="sxs-lookup"><span data-stu-id="c798c-296">text</span></span> <br /> <i><span data-ttu-id="c798c-297">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-298">O texto completo da propriedade, conforme especificado no estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="c798c-299">parsedOk</span></span> <br /> <i><span data-ttu-id="c798c-300">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-301">Se a propriedade é compreendida pelo navegador (implica `true` se estiver ausente).</span><span class="sxs-lookup"><span data-stu-id="c798c-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-302">ativo</span><span class="sxs-lookup"><span data-stu-id="c798c-302">disabled</span></span> <br /> <i><span data-ttu-id="c798c-303">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-304">Se a propriedade está desabilitada pelo usuário (apenas para Propriedades baseadas na origem).</span><span class="sxs-lookup"><span data-stu-id="c798c-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-305">gama</span><span class="sxs-lookup"><span data-stu-id="c798c-305">range</span></span> <br /> <i><span data-ttu-id="c798c-306">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="c798c-307">Todo o intervalo de propriedades na declaração de estilo delimitador (se disponível).</span><span class="sxs-lookup"><span data-stu-id="c798c-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="c798c-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="c798c-308">CSSMedia</span></span> `object`

<span data-ttu-id="c798c-309">Descritor de regras de mídia CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-310">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-311">texto</span><span class="sxs-lookup"><span data-stu-id="c798c-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-312">Texto de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-313">bibliográfica</span><span class="sxs-lookup"><span data-stu-id="c798c-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="c798c-314">Valores permitidos: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="c798c-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="c798c-315">Fonte da consulta de mídia: "mediaRule" se especificado por uma regra de @media, "importRule" se especificado por uma regra de @import, "linkedSheet" se especificado por um atributo "Media" na marca de LINK de uma folha de estilos vinculada, "inlineSheet", se especificado por um atributo "Media" em uma marca de estilo da folha de estilos embutida.</span><span class="sxs-lookup"><span data-stu-id="c798c-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="c798c-316">sourceURL</span></span> <br /> <i><span data-ttu-id="c798c-317">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-318">URL do documento que contém a descrição da consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-319">gama</span><span class="sxs-lookup"><span data-stu-id="c798c-319">range</span></span> <br /> <i><span data-ttu-id="c798c-320">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="c798c-321">O intervalo de cabeçalhos de regra (@media ou @import) associado na folha de estilos delimitadora (se disponível).</span><span class="sxs-lookup"><span data-stu-id="c798c-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-322">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="c798c-323">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="c798c-324">Identificador da folha de estilos que contém esse objeto (se houver).</span><span class="sxs-lookup"><span data-stu-id="c798c-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-325">medialist</span><span class="sxs-lookup"><span data-stu-id="c798c-325">mediaList</span></span> <br /> <i><span data-ttu-id="c798c-326">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="c798c-327">Matriz de consultas de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="c798c-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="c798c-328">MediaQuery</span></span> `object`

<span data-ttu-id="c798c-329">Descritor de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-330">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-331">expressão</span><span class="sxs-lookup"><span data-stu-id="c798c-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="c798c-332">Matriz de expressões de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-333">active</span><span class="sxs-lookup"><span data-stu-id="c798c-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-334">Se a condição de consulta de mídia é satisfeita.</span><span class="sxs-lookup"><span data-stu-id="c798c-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="c798c-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="c798c-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="c798c-336">Descritor de expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-337">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-338">value</span><span class="sxs-lookup"><span data-stu-id="c798c-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="c798c-339">Valor da expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-340">organizacional</span><span class="sxs-lookup"><span data-stu-id="c798c-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-341">Unidades de expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-342">recurso</span><span class="sxs-lookup"><span data-stu-id="c798c-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-343">Recurso de expressão de consulta de mídia.</span><span class="sxs-lookup"><span data-stu-id="c798c-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="c798c-344">valueRange</span></span> <br /> <i><span data-ttu-id="c798c-345">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="c798c-346">O intervalo associado do valor do texto na folha de estilos de delimitador (se disponível).</span><span class="sxs-lookup"><span data-stu-id="c798c-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="c798c-347">computedLength</span></span> <br /> <i><span data-ttu-id="c798c-348">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="c798c-349">Duração calculada da expressão de consulta de mídia (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="c798c-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="c798c-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="c798c-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="c798c-351">Informações sobre a quantidade de glifos que foram renderizados com determinada fonte.</span><span class="sxs-lookup"><span data-stu-id="c798c-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-352">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-353">FamilyName</span><span class="sxs-lookup"><span data-stu-id="c798c-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-354">Nome da família da fonte informado pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="c798c-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="c798c-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-356">Indica se a fonte foi baixada ou resolvida localmente.</span><span class="sxs-lookup"><span data-stu-id="c798c-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="c798c-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="c798c-358">Valor dos glifos renderizados com essa fonte.</span><span class="sxs-lookup"><span data-stu-id="c798c-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="c798c-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="c798c-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="c798c-360">Representação de regras de quadros-chave CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-361">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-362">animationname</span><span class="sxs-lookup"><span data-stu-id="c798c-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="c798c-363">Nome da animação.</span><span class="sxs-lookup"><span data-stu-id="c798c-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-364">quadros-chave</span><span class="sxs-lookup"><span data-stu-id="c798c-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="c798c-365">Lista de quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="c798c-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="c798c-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="c798c-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="c798c-367">Representação de regra do quadro-chave CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-368">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-369">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="c798c-370">opcional</span><span class="sxs-lookup"><span data-stu-id="c798c-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="c798c-371">O identificador de folha de estilos CSS (ausente para a folha de estilos de agente do usuário e as regras de folha de estilos especificadas pelo usuário) a partir da qual essa</span><span class="sxs-lookup"><span data-stu-id="c798c-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-372">Origin</span><span class="sxs-lookup"><span data-stu-id="c798c-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="c798c-373">Origem da folha de estilos pai.</span><span class="sxs-lookup"><span data-stu-id="c798c-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-374">keytext</span><span class="sxs-lookup"><span data-stu-id="c798c-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="c798c-375">Texto de chave associado.</span><span class="sxs-lookup"><span data-stu-id="c798c-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-376">estilo</span><span class="sxs-lookup"><span data-stu-id="c798c-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="c798c-377">Declaração de estilo associada.</span><span class="sxs-lookup"><span data-stu-id="c798c-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="c798c-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="c798c-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-379">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-380">name</span><span class="sxs-lookup"><span data-stu-id="c798c-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-381">Nome da propriedade de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="c798c-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-382">value</span><span class="sxs-lookup"><span data-stu-id="c798c-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-383">Valor da propriedade de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="c798c-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="c798c-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="c798c-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="c798c-385">Metainformação da folha de estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="c798c-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="c798c-386">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c798c-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="c798c-387">styleSheetid</span><span class="sxs-lookup"><span data-stu-id="c798c-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="c798c-388">O identificador de folha de estilos.</span><span class="sxs-lookup"><span data-stu-id="c798c-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="c798c-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="c798c-390">URL do recurso de folha de estilo.</span><span class="sxs-lookup"><span data-stu-id="c798c-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-391">ativo</span><span class="sxs-lookup"><span data-stu-id="c798c-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-392">Indica se a folha de estilo está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="c798c-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-393">IsInline</span><span class="sxs-lookup"><span data-stu-id="c798c-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="c798c-394">Se essa folha de estilos é criada para marcação de estilo por analisador.</span><span class="sxs-lookup"><span data-stu-id="c798c-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="c798c-395">Este sinalizador não está definido para marcas de estilo Document. Write.</span><span class="sxs-lookup"><span data-stu-id="c798c-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-396">início</span><span class="sxs-lookup"><span data-stu-id="c798c-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="c798c-397">Deslocamento de linha da folha de estilos dentro do recurso (com base em zero).</span><span class="sxs-lookup"><span data-stu-id="c798c-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-398">startColumn</span><span class="sxs-lookup"><span data-stu-id="c798c-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="c798c-399">Deslocamento de coluna da folha de estilos dentro do recurso (com base em zero).</span><span class="sxs-lookup"><span data-stu-id="c798c-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="c798c-400">das</span><span class="sxs-lookup"><span data-stu-id="c798c-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="c798c-401">Tamanho do conteúdo (em caracteres).</span><span class="sxs-lookup"><span data-stu-id="c798c-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="c798c-402">Dependências</span><span class="sxs-lookup"><span data-stu-id="c798c-402">Dependencies</span></span>

[<span data-ttu-id="c798c-403">DOM</span><span class="sxs-lookup"><span data-stu-id="c798c-403">DOM</span></span>](dom.md)
