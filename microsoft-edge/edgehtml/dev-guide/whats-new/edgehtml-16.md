---
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no EdgeHTML 16.
title: Novos recursos e APIs no EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399194"
---
# <a name="whats-new-in-edgehtml-16"></a><span data-ttu-id="bda3b-104">Novidades no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="bda3b-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="bda3b-105">Aqui está uma lista dos recursos novos e atualizados fornecidos na plataforma Web [EdgeHTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) como parte da Atualização de Criadores de Fall do [Windows 10](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span><span class="sxs-lookup"><span data-stu-id="bda3b-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="bda3b-106">Para alterações em builds específicos do Windows Insider Preview, consulte o [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) e [Novidades no EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="bda3b-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="bda3b-107">Aqui está o permalink para a seguinte lista de alterações:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="bda3b-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <a name="new-and-updated-features"></a><span data-ttu-id="bda3b-108">Recursos novos e atualizados</span><span class="sxs-lookup"><span data-stu-id="bda3b-108">New and updated features</span></span>  

### <a name="css-grid-layout"></a><span data-ttu-id="bda3b-109">Layout da Grade CSS</span><span class="sxs-lookup"><span data-stu-id="bda3b-109">CSS Grid Layout</span></span>  

<span data-ttu-id="bda3b-110">O Microsoft Edge agora dá suporte à implementação não prefixada de [Layout de Grade CSS.](https://www.w3.org/TR/css-grid-1)</span><span class="sxs-lookup"><span data-stu-id="bda3b-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="bda3b-111">[Layout de Grade](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define um sistema de layout baseado em grade bidimensional que permite mais fluidez de layout do que possível com o posicionamento usando floats ou scripts.</span><span class="sxs-lookup"><span data-stu-id="bda3b-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="bda3b-112">O exemplo a seguir usa Layout de Grade CSS para criar a estrutura de uma página da Web básica.</span><span class="sxs-lookup"><span data-stu-id="bda3b-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="bda3b-113">Layout da Grade CSS</span><span class="sxs-lookup"><span data-stu-id="bda3b-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="bda3b-114">Consulte o Layout da Grade CSS da Caneta <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) em </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="bda3b-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <a name="css-object-fit-and-object-position"></a><span data-ttu-id="bda3b-115">Css object-fit and object-position</span><span class="sxs-lookup"><span data-stu-id="bda3b-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="bda3b-116">EdgeHTML 16 apresenta suporte para propriedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) e [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="bda3b-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="bda3b-117">Essas propriedades controlam a posição e o tamanho do conteúdo substituído dentro da caixa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bda3b-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <a name="developer-tools"></a><span data-ttu-id="bda3b-118">Ferramentas de Desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="bda3b-118">Developer Tools</span></span>  

<span data-ttu-id="bda3b-119">Esta versão iniciamos um grande esforço de novafação do Microsoft Edge DevTools para melhorar a robustez e o desempenho e também adicionamos um monte de novos recursos que você pode começar a usar hoje em builds [do Windows Insider.](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="bda3b-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="bda3b-120">Confira o [guia Microsoft Edge DevTools](../whats-new.md) para saber mais sobre o que mudou!</span><span class="sxs-lookup"><span data-stu-id="bda3b-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <a name="javascript"></a><span data-ttu-id="bda3b-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bda3b-121">JavaScript</span></span>  

<span data-ttu-id="bda3b-122">[O EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) se cria em otimizações de desempenho javascript de versões anteriores expandindo a capacidade do mecanismo de Chakra de adiar/adiar funções, usar caches embutidos polimórficos e otimizar funções com `try` / `finally` blocos.</span><span class="sxs-lookup"><span data-stu-id="bda3b-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="bda3b-123">Além disso, os recursos visualizados pela primeira vez no EdgeHTML 15 agora estão estáveis e habilitados por padrão:</span><span class="sxs-lookup"><span data-stu-id="bda3b-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <a name="new-features"></a><span data-ttu-id="bda3b-124">Novos recursos</span><span class="sxs-lookup"><span data-stu-id="bda3b-124">New features</span></span>  

<span data-ttu-id="bda3b-125">Ativado por padrão</span><span class="sxs-lookup"><span data-stu-id="bda3b-125">On by default</span></span>  

*   <span data-ttu-id="bda3b-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="bda3b-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="bda3b-127">Memória Compartilhada e Atomics</span><span class="sxs-lookup"><span data-stu-id="bda3b-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a><span data-ttu-id="bda3b-128">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="bda3b-128">Payment Request API</span></span>  

<span data-ttu-id="bda3b-129">A [API](../windows-integration/payment-request-api.md) de Solicitação de Pagamento é um padrão aberto entre navegadores que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \(como cartões de crédito\) que os consumidores armazenaram na nuvem.</span><span class="sxs-lookup"><span data-stu-id="bda3b-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="bda3b-130">A API no EdgeHTML 16 foi atualizada para corresponder à especificação mais recente da [API](https://w3c.github.io/payment-request) de Solicitação de Pagamento W3C.</span><span class="sxs-lookup"><span data-stu-id="bda3b-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="bda3b-131">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="bda3b-131">This includes:</span></span>  

*   <span data-ttu-id="bda3b-132">Suporte para o `canMakePayment()` método</span><span class="sxs-lookup"><span data-stu-id="bda3b-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="bda3b-133">Suporte para a `requestId` propriedade</span><span class="sxs-lookup"><span data-stu-id="bda3b-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="bda3b-134">Suporte para a `id` propriedade</span><span class="sxs-lookup"><span data-stu-id="bda3b-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="bda3b-135">O valor padrão do parâmetro do método foi `complete()` alterado de " " para `result` "desconhecido"</span><span class="sxs-lookup"><span data-stu-id="bda3b-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <a name="service-workers"></a><span data-ttu-id="bda3b-136">Profissionais de Serviço</span><span class="sxs-lookup"><span data-stu-id="bda3b-136">Service Workers</span></span>  

<span data-ttu-id="bda3b-137">[Os Trabalhadores do](https://www.w3.org/TR/service-workers-1) Serviço são scripts orientados por eventos que são executados em segundo plano de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="bda3b-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="bda3b-138">Os funcionários de serviço habilitam a funcionalidade anteriormente disponível apenas com aplicativos nativos, como interceptação e manipulação de solicitações da rede, gerenciamento e tratamento de sincronização em segundo plano, armazenamento local e notificações por push.</span><span class="sxs-lookup"><span data-stu-id="bda3b-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="bda3b-139">O suporte para o trabalhador do serviço ainda está em desenvolvimento, mas você pode testar seu PWA no Microsoft Edge com nosso suporte de funcionário de serviço experimental habilitando o recurso de trabalho do serviço em `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="bda3b-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <a name="webvr"></a><span data-ttu-id="bda3b-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="bda3b-140">WebVR</span></span>  

<span data-ttu-id="bda3b-141">WebVR para Microsoft Edge adicionou suporte para [controladores de movimento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span><span class="sxs-lookup"><span data-stu-id="bda3b-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="bda3b-142">Esses controladores têm uma posição precisa no espaço, permitindo uma interação fina com objetos digitais na realidade virtual.</span><span class="sxs-lookup"><span data-stu-id="bda3b-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de movimento" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="bda3b-144">Controladores de movimento</span><span class="sxs-lookup"><span data-stu-id="bda3b-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="bda3b-145">A WebVR também foi otimizada para dar suporte a dois tipos diferentes de experiências.</span><span class="sxs-lookup"><span data-stu-id="bda3b-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="bda3b-146">**Computadores de realidade mista do Windows** - Desktops e laptops com elementos gráficos integrados.</span><span class="sxs-lookup"><span data-stu-id="bda3b-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="bda3b-147">Quando conectados a esses dispositivos, nossos fones de ouvido imersivos serão executados a 60 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="bda3b-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="bda3b-148">**Windows Mixed Reality Ultra PCs** - Desktops e laptops com gráficos discretos.</span><span class="sxs-lookup"><span data-stu-id="bda3b-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="bda3b-149">Quando conectados a esses dispositivos, nossos fones de ouvido imersivos serão executados a 90 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="bda3b-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="bda3b-150">Ambas as configurações darão suporte às mesmas experiências imersivas de vídeo e jogos.</span><span class="sxs-lookup"><span data-stu-id="bda3b-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="bda3b-151">Para obter mais informações sobre as próximas atualizações de Realidade Mista do Windows, confira a postagem do blog de atualização de feriados da Realidade Mista do [Windows.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)</span><span class="sxs-lookup"><span data-stu-id="bda3b-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="bda3b-152">Para guias e demonstrações, vá para o [Guia do Desenvolvedor webvr.](/microsoft-edge/webvr)</span><span class="sxs-lookup"><span data-stu-id="bda3b-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="bda3b-153">Como a especificação WebVR ainda está em desenvolvimento, a implementação do Microsoft Edge pode mudar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="bda3b-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <a name="new-apis-in-edgehtml-16"></a><span data-ttu-id="bda3b-154">Novas APIs no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="bda3b-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="bda3b-155">Aqui está a lista completa de novas APIs no EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="bda3b-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="bda3b-156">Eles estão listados no formato de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="bda3b-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="bda3b-157">Embora as APIs a seguir sejam expostas no DOM, o comportamento de ponta a ponta de algumas ainda pode estar em desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="bda3b-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="bda3b-158">Consulte o [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para o suporte oficial do word on feature.</span><span class="sxs-lookup"><span data-stu-id="bda3b-158">Refer to [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="bda3b-159">Novas APIs no EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="bda3b-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="bda3b-160">Consulte as <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> APIs Caneta Novas no EdgeHTML 16 </a> by MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) em </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="bda3b-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <a name="previous-edgehtml-releases"></a><span data-ttu-id="bda3b-161">Versões anteriores do EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="bda3b-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="bda3b-162">EdgeHTML 12 / build do Windows 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="bda3b-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="bda3b-163">EdgeHTML 13 / build do Windows 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="bda3b-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="bda3b-164">EdgeHTML 14 / Build do Windows 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="bda3b-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="bda3b-165">EdgeHTML 15 / build do Windows 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="bda3b-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
