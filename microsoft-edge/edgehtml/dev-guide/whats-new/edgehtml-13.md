---
description: Esta página fornece uma visão geral do que há de novo no EdgeHTML 13.
title: Novos recursos e APIs no EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231904"
---
# <span data-ttu-id="bcaee-104">Novidades do EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="bcaee-104">What's new in EdgeHTML 13</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="bcaee-105">Aqui estão as alterações fornecidas com o EdgeHTML 13, o mecanismo que liga o navegador Microsoft Edge na [primeira atualização importante](https://blogs.windows.com/windowsexperience/2015/11/12) para Windows 10 \ (11/2015, Build 10586 \).</span><span class="sxs-lookup"><span data-stu-id="bcaee-105">Here are the changes shipped with EdgeHTML 13, the engine powering the Microsoft Edge browser in the [first major update](https://blogs.windows.com/windowsexperience/2015/11/12) for Windows 10 \(11/2015, Build 10586\).</span></span>  <span data-ttu-id="bcaee-106">Para obter uma visão geral das alterações no navegador geral do Microsoft Edge, consulte [apresentando EdgeHTML 13, nossa primeira atualização de plataforma para o Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span><span class="sxs-lookup"><span data-stu-id="bcaee-106">For an overview of changes to the overall Microsoft Edge browser, see [Introducing EdgeHTML 13, our first platform update for Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span></span>  

<span data-ttu-id="bcaee-107">Aqui está o link permanente para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .</span><span class="sxs-lookup"><span data-stu-id="bcaee-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md).</span></span>  

## <span data-ttu-id="bcaee-108">Recursos</span><span class="sxs-lookup"><span data-stu-id="bcaee-108">Features</span></span>  

### <span data-ttu-id="bcaee-109">CSS</span><span class="sxs-lookup"><span data-stu-id="bcaee-109">CSS</span></span>  

<span data-ttu-id="bcaee-110">O EdgeHTML 13 oferece suporte a novos recursos CSS, incluindo:</span><span class="sxs-lookup"><span data-stu-id="bcaee-110">EdgeHTML 13 supports new CSS features, including:</span></span>  

*   [<span data-ttu-id="bcaee-111">Pseudo-classes de imutabilidade CSS</span><span class="sxs-lookup"><span data-stu-id="bcaee-111">CSS Mutability Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [<span data-ttu-id="bcaee-112">Pseudo-classes de faixa CSS</span><span class="sxs-lookup"><span data-stu-id="bcaee-112">CSS Range Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   <span data-ttu-id="bcaee-113">Palavras-chave CSS [iniciais](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) e de [subdefinição](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue)</span><span class="sxs-lookup"><span data-stu-id="bcaee-113">CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) and [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) keywords</span></span>  

### <span data-ttu-id="bcaee-114">Extensões de mídia criptografadas</span><span class="sxs-lookup"><span data-stu-id="bcaee-114">Encrypted Media Extensions</span></span>  

<span data-ttu-id="bcaee-115">O Microsoft Edge agora oferece suporte às novas APIs de [extensões de mídia criptografadas sem](https://w3.org/TR/encrypted-media) prefixo.</span><span class="sxs-lookup"><span data-stu-id="bcaee-115">Microsoft Edge now supports the new unprefixed [Encrypted Media Extensions](https://w3.org/TR/encrypted-media) APIs.</span></span>  <span data-ttu-id="bcaee-116">Extensões de mídia criptografadas \ (EME \) estende os elementos de vídeo e áudio para habilitar o conteúdo protegido do gerenciamento de direitos digitais \ (DRM \) sem usar plug-ins.  Leia mais sobre o EME:  [extensões de mídia criptografadas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span><span class="sxs-lookup"><span data-stu-id="bcaee-116">Encrypted Media Extensions \(EME\) extends the video and audio elements to enable Digital Rights Management \(DRM\) protected content without using plug-ins.  Read more about EME:  [Encrypted Media Extensions](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span></span>  

### <span data-ttu-id="bcaee-117">Elementos gráficos</span><span class="sxs-lookup"><span data-stu-id="bcaee-117">Graphics</span></span>  

<span data-ttu-id="bcaee-118">EdgeHTML 13 introduz as seguintes atualizações de gráficos:</span><span class="sxs-lookup"><span data-stu-id="bcaee-118">EdgeHTML 13 introduces the following graphics updates:</span></span>  

*   [<span data-ttu-id="bcaee-119">Elipse da tela</span><span class="sxs-lookup"><span data-stu-id="bcaee-119">Canvas ellipse</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [<span data-ttu-id="bcaee-120">Modos de mesclagem de tela</span><span class="sxs-lookup"><span data-stu-id="bcaee-120">Canvas blending modes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> <span data-ttu-id="bcaee-121">sub-elemento</span><span class="sxs-lookup"><span data-stu-id="bcaee-121">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [<span data-ttu-id="bcaee-122">Conteúdo externo SVG</span><span class="sxs-lookup"><span data-stu-id="bcaee-122">SVG external content</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### <span data-ttu-id="bcaee-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bcaee-123">JavaScript</span></span>  

<span data-ttu-id="bcaee-124">O EdgeHTML 13 inclui [grandes melhorias e suporte a novos recursos no Chakra](https://blogs.windows.com/msedgedev/2015/09/30), o mecanismo JavaScript que o Microsoft Edge desliga, incluindo:</span><span class="sxs-lookup"><span data-stu-id="bcaee-124">EdgeHTML 13 includes [major improvements and new feature support in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), the JavaScript engine powering Microsoft Edge, including:</span></span>  

#### <span data-ttu-id="bcaee-125">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="bcaee-125">New features</span></span>  

<span data-ttu-id="bcaee-126">Ativado por padrão</span><span class="sxs-lookup"><span data-stu-id="bcaee-126">On by default</span></span>  

*   <span data-ttu-id="bcaee-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) habilitada por padrão \ ([postagem de blog](https://blogs.windows.com/msedgedev/2015/11/10), [demonstração](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span><span class="sxs-lookup"><span data-stu-id="bcaee-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) enabled by default \([blog post](https://blogs.windows.com/msedgedev/2015/11/10), [demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span></span>  
*   <span data-ttu-id="bcaee-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \ (ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="bcaee-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span></span>  

#### <span data-ttu-id="bcaee-129">Recursos de JavaScript experimental</span><span class="sxs-lookup"><span data-stu-id="bcaee-129">Experimental JavaScript features</span></span>  

<span data-ttu-id="bcaee-130">Habilitado com</span><span class="sxs-lookup"><span data-stu-id="bcaee-130">Enabled with</span></span> `about:flags`  

*   <span data-ttu-id="bcaee-131">[Funções assíncronas](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \ (ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="bcaee-131">[Async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span></span>  
*   <span data-ttu-id="bcaee-132">[Operador de exponenciação](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \ (ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="bcaee-132">[Exponentiation operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span></span>  
*   <span data-ttu-id="bcaee-133">[Deestruturando](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \ (ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="bcaee-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span></span>  

### <span data-ttu-id="bcaee-134">Entrada do usuário</span><span class="sxs-lookup"><span data-stu-id="bcaee-134">User Input</span></span>  

<span data-ttu-id="bcaee-135">Os seguintes recursos introduzidos no EdgeHTML 13 aprimoram a entrada do usuário:</span><span class="sxs-lookup"><span data-stu-id="bcaee-135">The following features introduced in EdgeHTML 13 improve user input:</span></span>  

*   [\<meter\> <span data-ttu-id="bcaee-136">sub-elemento</span><span class="sxs-lookup"><span data-stu-id="bcaee-136">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [<span data-ttu-id="bcaee-137">manipulador de eventos oninvalid para o elemento e a janela do documento</span><span class="sxs-lookup"><span data-stu-id="bcaee-137">oninvalid event handler for the element document and window</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### <span data-ttu-id="bcaee-138">Bloqueio de ponteiro</span><span class="sxs-lookup"><span data-stu-id="bcaee-138">Pointer Lock</span></span>  

<span data-ttu-id="bcaee-139">O Microsoft Edge agora dá suporte à API de bloqueio de ponteiro \ (anteriormente chamada de bloqueio do mouse \) para acessar o movimento bruto do mouse, bloqueando o destino de eventos do mouse para um único elemento, eliminando os limites de quão longe o movimento do mouse pode ir em uma única direção e removendo o cursor do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="bcaee-139">Microsoft Edge now supports the Pointer Lock API \(previously called Mouse Lock\) for access to raw mouse movement, locking the target of mouse events to a single element, eliminating limits of how far mouse movement can go in a single direction, and removing the cursor from view.</span></span>  

## <span data-ttu-id="bcaee-140">Novas APIs no EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="bcaee-140">New APIs in EdgeHTML 13</span></span>  

<span data-ttu-id="bcaee-141">Aqui está a lista completa de APIs novas em EdgeHTML 13.</span><span class="sxs-lookup"><span data-stu-id="bcaee-141">Here's the full list of new APIs in EdgeHTML 13.</span></span>  <span data-ttu-id="bcaee-142">Elas são listadas no formato de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="bcaee-142">They are listed in the format of `[interface name].[api name]`.</span></span>  

<iframe height='584' scrolling='no' title='<span data-ttu-id="bcaee-143">Novas APIs no EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="bcaee-143">New APIs in EdgeHTML 13</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'><span data-ttu-id="bcaee-144">Veja a caneta <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> New APIs no EdgeHTML 13 </a> ao Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="bcaee-144">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'>New APIs in EdgeHTML 13</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  
