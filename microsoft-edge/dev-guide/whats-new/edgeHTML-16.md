---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no Microsoft Edge.
title: Novos recursos e APIs no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: a15888bc8c1314d61d436759e5d63be942174ea4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941935"
---
# <span data-ttu-id="fcc96-104">O que há de novo no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="fcc96-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="fcc96-105">Aqui está uma lista dos recursos novos e atualizados fornecidos na plataforma da Web [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) , como parte da [atualização do Windows 10 para criadores de outono](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \ (10/2017, Build 16299 \).</span><span class="sxs-lookup"><span data-stu-id="fcc96-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="fcc96-106">Para alterações em compilações específicas do Windows Insider Preview, consulte o [changelog do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) e [o que há de novo no EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="fcc96-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="fcc96-107">Aqui está o link permanente para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc96-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="fcc96-108">Recursos novos e atualizados</span><span class="sxs-lookup"><span data-stu-id="fcc96-108">New and updated features</span></span>  

### <span data-ttu-id="fcc96-109">Layout de grade CSS</span><span class="sxs-lookup"><span data-stu-id="fcc96-109">CSS Grid Layout</span></span>  

<span data-ttu-id="fcc96-110">O Microsoft Edge agora oferece suporte à implementação prefixada do [layout de grade CSS](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="fcc96-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="fcc96-111">O [layout de grade](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define um sistema de layout baseado em grade bidimensional que permite mais fluidos de layout do que o possível com posicionamento com floats ou scripts.</span><span class="sxs-lookup"><span data-stu-id="fcc96-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="fcc96-112">O exemplo a seguir usa o layout de grade CSS para criar a estrutura de uma página da Web básica.</span><span class="sxs-lookup"><span data-stu-id="fcc96-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="fcc96-113">Layout de grade CSS</span><span class="sxs-lookup"><span data-stu-id="fcc96-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="fcc96-114">Consulte o <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> layout de grade CSS da caneta </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="fcc96-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="fcc96-115">Objeto CSS-ajustar e posição do objeto</span><span class="sxs-lookup"><span data-stu-id="fcc96-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="fcc96-116">EdgeHTML 16 introduz suporte para propriedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) e [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="fcc96-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="fcc96-117">Essas propriedades controlam a posição e o tamanho do conteúdo substituído na caixa conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fcc96-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="fcc96-118">Ferramentas de Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="fcc96-118">Developer Tools</span></span>  

<span data-ttu-id="fcc96-119">Este lançamento, começamos a usar um importante esforço de refatoração do Microsoft Edge DevTools para melhorar a eficiência e o desempenho, além de adicionar um monte de novos recursos que você pode começar a usar hoje mesmo em compilações do [Windows Insider](https://insider.windows.com) .</span><span class="sxs-lookup"><span data-stu-id="fcc96-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="fcc96-120">Confira o [Guia do Microsoft Edge devtools](../whats-new.md) para saber mais sobre o que mudou!</span><span class="sxs-lookup"><span data-stu-id="fcc96-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="fcc96-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="fcc96-121">JavaScript</span></span>  

<span data-ttu-id="fcc96-122">[EdgeHTML 16 cria](https://blogs.windows.com/msedgedev/2017/10/31) otimizações de desempenho de JavaScript de versões anteriores ao expandir a capacidade do mecanismo chakra de adiar/readiar funções, usar caches embutidos polimórficos e otimizar funções com `try` / `finally` blocos.</span><span class="sxs-lookup"><span data-stu-id="fcc96-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="fcc96-123">Além disso, os recursos primeiro visualizados no EdgeHTML 15 agora são estáveis e habilitados por padrão:</span><span class="sxs-lookup"><span data-stu-id="fcc96-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="fcc96-124">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="fcc96-124">New features</span></span>  

<span data-ttu-id="fcc96-125">Ativado por padrão</span><span class="sxs-lookup"><span data-stu-id="fcc96-125">On by default</span></span>  

*   <span data-ttu-id="fcc96-126">[Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \ ([demonstração](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="fcc96-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="fcc96-127">Memória compartilhada e Atomicidades</span><span class="sxs-lookup"><span data-stu-id="fcc96-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="fcc96-128">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="fcc96-128">Payment Request API</span></span>  

<span data-ttu-id="fcc96-129">A [API de solicitação de pagamento](../windows-integration/payment-request-api.md) é um padrão de navegador cruzado aberto que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \ (como cartões de crédito \) que os consumidores armazenaram na nuvem.</span><span class="sxs-lookup"><span data-stu-id="fcc96-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="fcc96-130">A API no EdgeHTML 16 foi atualizada para corresponder à especificação da [API de solicitação de pagamento](https://w3c.github.io/payment-request) W3C mais recente.</span><span class="sxs-lookup"><span data-stu-id="fcc96-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="fcc96-131">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="fcc96-131">This includes:</span></span>  

*   <span data-ttu-id="fcc96-132">Suporte para o `canMakePayment()` método</span><span class="sxs-lookup"><span data-stu-id="fcc96-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="fcc96-133">Suporte para a `requestId` Propriedade</span><span class="sxs-lookup"><span data-stu-id="fcc96-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="fcc96-134">Suporte para a `id` Propriedade</span><span class="sxs-lookup"><span data-stu-id="fcc96-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="fcc96-135">O valor padrão para o `complete()` parâmetro do método `result` mudou de "" para "desconhecido"</span><span class="sxs-lookup"><span data-stu-id="fcc96-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="fcc96-136">Profissionais de Serviço</span><span class="sxs-lookup"><span data-stu-id="fcc96-136">Service Workers</span></span>  

<span data-ttu-id="fcc96-137">[Os funcionários de serviço](https://www.w3.org/TR/service-workers-1) são scripts orientados por eventos que são executados em segundo plano de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="fcc96-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="fcc96-138">Os funcionários de serviço habilitam a funcionalidade anteriormente somente disponível em aplicativos nativos, como interceptação e manipulação de solicitações na rede, gerenciamento e manipulação de sincronização em segundo plano, armazenamento local e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="fcc96-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="fcc96-139">O suporte para o serviço de trabalho ainda está em desenvolvimento, mas você pode testar o PWA no Microsoft Edge com o nosso serviço de trabalho experimental ao habilitar o recurso de trabalho do serviço `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="fcc96-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="fcc96-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="fcc96-140">WebVR</span></span>  

<span data-ttu-id="fcc96-141">O WebVR para Microsoft Edge incluiu suporte para [controladores de movimento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span><span class="sxs-lookup"><span data-stu-id="fcc96-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="fcc96-142">Esses controladores têm uma posição precisa em espaço, permitindo uma interação refinada com objetos digitais em realidade virtual.</span><span class="sxs-lookup"><span data-stu-id="fcc96-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de animação" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="fcc96-144">Controladores de animação</span><span class="sxs-lookup"><span data-stu-id="fcc96-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="fcc96-145">O WebVR também foi otimizado para dar suporte a dois tipos diferentes de experiências.</span><span class="sxs-lookup"><span data-stu-id="fcc96-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="fcc96-146">**PCs Windows Mixed Reality** -desktops e laptops com elementos gráficos integrados.</span><span class="sxs-lookup"><span data-stu-id="fcc96-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="fcc96-147">Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 60 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="fcc96-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="fcc96-148">**Windows Mixed Reality ultra PCs** -desktops e laptops com elementos gráficos discretos.</span><span class="sxs-lookup"><span data-stu-id="fcc96-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="fcc96-149">Quando conectados a esses dispositivos, nossos fones de ouvido com microfone de imersão serão executados em 90 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="fcc96-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="fcc96-150">Ambas as configurações aceitarão as mesmas experiências de vídeo e de jogos imersivas.</span><span class="sxs-lookup"><span data-stu-id="fcc96-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="fcc96-151">Para obter mais informações sobre as futuras atualizações da realidade do Windows Mixed, confira a postagem do blog de atualização de férias do [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) .</span><span class="sxs-lookup"><span data-stu-id="fcc96-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="fcc96-152">Para guias e demonstrações, vá para o [Guia do desenvolvedor do WebVR](/microsoft-edge/webvr).</span><span class="sxs-lookup"><span data-stu-id="fcc96-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="fcc96-153">Como a especificação do WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar posteriormente na linha.</span><span class="sxs-lookup"><span data-stu-id="fcc96-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="fcc96-154">Novas APIs no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="fcc96-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="fcc96-155">Aqui está a lista completa de novas APIs no EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="fcc96-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="fcc96-156">Elas são listadas no formato de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="fcc96-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="fcc96-157">Embora as seguintes APIs sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="fcc96-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="fcc96-158">Consulte o  [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para obter a palavra oficial sobre o suporte ao recurso.</span><span class="sxs-lookup"><span data-stu-id="fcc96-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="fcc96-159">Novas APIs no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="fcc96-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="fcc96-160">Consulte as <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> novas APIs de caneta no EdgeHTML 16 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="fcc96-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="fcc96-161">Versões anteriores do EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="fcc96-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="fcc96-162">EdgeHTML 12/Build do Windows 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="fcc96-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="fcc96-163">EdgeHTML 13/Build do Windows 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="fcc96-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="fcc96-164">EdgeHTML 14/Build do Windows 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="fcc96-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="fcc96-165">EdgeHTML 15/Build do Windows 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="fcc96-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
