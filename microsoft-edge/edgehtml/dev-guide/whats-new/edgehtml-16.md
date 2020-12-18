---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Este guia fornece uma visão geral dos novos recursos e APIs do EdgeHTML 16.
title: Novos recursos e APIs no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7697114546153555d947903eda6bf8477cca3516
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231587"
---
# <span data-ttu-id="76be0-104">O que há de novo no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="76be0-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="76be0-105">Aqui está uma lista dos recursos novos e atualizados fornecidos na plataforma da Web [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) , como parte da [atualização do Windows 10 para criadores de outono](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \ (10/2017, Build 16299 \).</span><span class="sxs-lookup"><span data-stu-id="76be0-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="76be0-106">Para alterações em compilações específicas do Windows Insider Preview, consulte o [changelog do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) e [o que há de novo no EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="76be0-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="76be0-107">Aqui está o link permanente para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="76be0-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="76be0-108">Recursos novos e atualizados</span><span class="sxs-lookup"><span data-stu-id="76be0-108">New and updated features</span></span>  

### <span data-ttu-id="76be0-109">Layout de grade CSS</span><span class="sxs-lookup"><span data-stu-id="76be0-109">CSS Grid Layout</span></span>  

<span data-ttu-id="76be0-110">O Microsoft Edge agora oferece suporte à implementação prefixada do [layout de grade CSS](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="76be0-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="76be0-111">O [layout de grade](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define um sistema de layout baseado em grade bidimensional que permite mais fluidos de layout do que o possível com posicionamento com floats ou scripts.</span><span class="sxs-lookup"><span data-stu-id="76be0-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="76be0-112">O exemplo a seguir usa o layout de grade CSS para criar a estrutura de uma página da Web básica.</span><span class="sxs-lookup"><span data-stu-id="76be0-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="76be0-113">Layout de grade CSS</span><span class="sxs-lookup"><span data-stu-id="76be0-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="76be0-114">Consulte o <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> layout de grade CSS da caneta </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="76be0-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="76be0-115">Objeto CSS-ajustar e posição do objeto</span><span class="sxs-lookup"><span data-stu-id="76be0-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="76be0-116">EdgeHTML 16 introduz suporte para propriedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) e [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="76be0-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="76be0-117">Essas propriedades controlam a posição e o tamanho do conteúdo substituído na caixa conteúdo.</span><span class="sxs-lookup"><span data-stu-id="76be0-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="76be0-118">Ferramentas de Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="76be0-118">Developer Tools</span></span>  

<span data-ttu-id="76be0-119">Este lançamento, começamos a usar um importante esforço de refatoração do Microsoft Edge DevTools para melhorar a eficiência e o desempenho, além de adicionar um monte de novos recursos que você pode começar a usar hoje mesmo em compilações do [Windows Insider](https://insider.windows.com) .</span><span class="sxs-lookup"><span data-stu-id="76be0-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="76be0-120">Confira o [Guia do Microsoft Edge devtools](../whats-new.md) para saber mais sobre o que mudou!</span><span class="sxs-lookup"><span data-stu-id="76be0-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="76be0-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="76be0-121">JavaScript</span></span>  

<span data-ttu-id="76be0-122">[EdgeHTML 16 cria](https://blogs.windows.com/msedgedev/2017/10/31) otimizações de desempenho de JavaScript de versões anteriores ao expandir a capacidade do mecanismo chakra de adiar/readiar funções, usar caches embutidos polimórficos e otimizar funções com `try` / `finally` blocos.</span><span class="sxs-lookup"><span data-stu-id="76be0-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="76be0-123">Além disso, os recursos primeiro visualizados no EdgeHTML 15 agora são estáveis e habilitados por padrão:</span><span class="sxs-lookup"><span data-stu-id="76be0-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="76be0-124">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="76be0-124">New features</span></span>  

<span data-ttu-id="76be0-125">Ativado por padrão</span><span class="sxs-lookup"><span data-stu-id="76be0-125">On by default</span></span>  

*   <span data-ttu-id="76be0-126">[Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \ ([demonstração](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="76be0-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="76be0-127">Memória compartilhada e Atomicidades</span><span class="sxs-lookup"><span data-stu-id="76be0-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="76be0-128">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="76be0-128">Payment Request API</span></span>  

<span data-ttu-id="76be0-129">A [API de solicitação de pagamento](../windows-integration/payment-request-api.md) é um padrão de navegador cruzado aberto que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \ (como cartões de crédito \) que os consumidores armazenaram na nuvem.</span><span class="sxs-lookup"><span data-stu-id="76be0-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="76be0-130">A API no EdgeHTML 16 foi atualizada para corresponder à especificação da [API de solicitação de pagamento](https://w3c.github.io/payment-request) W3C mais recente.</span><span class="sxs-lookup"><span data-stu-id="76be0-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="76be0-131">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="76be0-131">This includes:</span></span>  

*   <span data-ttu-id="76be0-132">Suporte para o `canMakePayment()` método</span><span class="sxs-lookup"><span data-stu-id="76be0-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="76be0-133">Suporte para a `requestId` Propriedade</span><span class="sxs-lookup"><span data-stu-id="76be0-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="76be0-134">Suporte para a `id` Propriedade</span><span class="sxs-lookup"><span data-stu-id="76be0-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="76be0-135">O valor padrão para o `complete()` parâmetro do método `result` mudou de "" para "desconhecido"</span><span class="sxs-lookup"><span data-stu-id="76be0-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="76be0-136">Profissionais de Serviço</span><span class="sxs-lookup"><span data-stu-id="76be0-136">Service Workers</span></span>  

<span data-ttu-id="76be0-137">[Os funcionários de serviço](https://www.w3.org/TR/service-workers-1) são scripts orientados por eventos que são executados em segundo plano de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="76be0-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="76be0-138">Os funcionários de serviço habilitam a funcionalidade anteriormente somente disponível em aplicativos nativos, como interceptação e manipulação de solicitações na rede, gerenciamento e manipulação de sincronização em segundo plano, armazenamento local e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="76be0-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="76be0-139">O suporte para o serviço de trabalho ainda está em desenvolvimento, mas você pode testar o PWA no Microsoft Edge com o nosso serviço de trabalho experimental ao habilitar o recurso de trabalho do serviço `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="76be0-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="76be0-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="76be0-140">WebVR</span></span>  

<span data-ttu-id="76be0-141">O WebVR para Microsoft Edge incluiu suporte para [controladores de movimento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span><span class="sxs-lookup"><span data-stu-id="76be0-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="76be0-142">Esses controladores têm uma posição precisa em espaço, permitindo uma interação refinada com objetos digitais em realidade virtual.</span><span class="sxs-lookup"><span data-stu-id="76be0-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de animação" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="76be0-144">Controladores de animação</span><span class="sxs-lookup"><span data-stu-id="76be0-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="76be0-145">O WebVR também foi otimizado para dar suporte a dois tipos diferentes de experiências.</span><span class="sxs-lookup"><span data-stu-id="76be0-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="76be0-146">**PCs Windows Mixed Reality** -desktops e laptops com elementos gráficos integrados.</span><span class="sxs-lookup"><span data-stu-id="76be0-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="76be0-147">Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 60 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="76be0-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="76be0-148">**Windows Mixed Reality ultra PCs** -desktops e laptops com elementos gráficos discretos.</span><span class="sxs-lookup"><span data-stu-id="76be0-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="76be0-149">Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 90 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="76be0-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="76be0-150">Ambas as configurações aceitarão as mesmas experiências de vídeo e de jogos imersivas.</span><span class="sxs-lookup"><span data-stu-id="76be0-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="76be0-151">Para obter mais informações sobre as futuras atualizações da realidade do Windows Mixed, confira a postagem do blog de atualização de férias do [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) .</span><span class="sxs-lookup"><span data-stu-id="76be0-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="76be0-152">Para guias e demonstrações, vá para o [Guia do desenvolvedor do WebVR](/microsoft-edge/webvr).</span><span class="sxs-lookup"><span data-stu-id="76be0-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="76be0-153">Como a especificação do WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar posteriormente na linha.</span><span class="sxs-lookup"><span data-stu-id="76be0-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="76be0-154">Novas APIs no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="76be0-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="76be0-155">Aqui está a lista completa de novas APIs no EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="76be0-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="76be0-156">Elas são listadas no formato de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="76be0-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="76be0-157">Embora as seguintes APIs sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="76be0-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="76be0-158">Consulte o  [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para obter a palavra oficial sobre o suporte ao recurso.</span><span class="sxs-lookup"><span data-stu-id="76be0-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="76be0-159">Novas APIs no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="76be0-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="76be0-160">Consulte as <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> novas APIs de caneta no EdgeHTML 16 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="76be0-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="76be0-161">Versões anteriores do EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="76be0-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="76be0-162">EdgeHTML 12/Build do Windows 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="76be0-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="76be0-163">EdgeHTML 13/Build do Windows 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="76be0-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="76be0-164">EdgeHTML 14/Build do Windows 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="76be0-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="76be0-165">EdgeHTML 15/Build do Windows 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="76be0-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
