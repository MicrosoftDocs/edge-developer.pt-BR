---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Guias para recursos de navegador no Microsoft Edge.
title: Guia de desenvolvimento de navegador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2579fad881496e2197f9f696bb2c12c47c7f723e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231787"
---
# <span data-ttu-id="aa368-104">Recursos do navegador</span><span class="sxs-lookup"><span data-stu-id="aa368-104">Browser features</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## <span data-ttu-id="aa368-105">Políticas de reprodução automática</span><span class="sxs-lookup"><span data-stu-id="aa368-105">Autoplay policies</span></span>  

 <span data-ttu-id="aa368-106">O Microsoft Edge fornece aos clientes a capacidade de personalizar suas preferências de navegação em sites que a mídia de reprodução automática com som para minimizar distrações na Web e conservar a largura de banda.</span><span class="sxs-lookup"><span data-stu-id="aa368-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="aa368-107">Os usuários podem personalizar o comportamento de mídia com os controles de reprodução automática global e por site.</span><span class="sxs-lookup"><span data-stu-id="aa368-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span>  <span data-ttu-id="aa368-108">Além disso, o Microsoft Edge automaticamente suprime a reprodução automática de mídia em guias de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="aa368-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="aa368-109">Confira [as políticas de reprodução automática](./browser-features/autoplay-policies.md) para obter detalhes e práticas recomendadas para garantir uma boa experiência do usuário com mídia hospedada em seu site.</span><span class="sxs-lookup"><span data-stu-id="aa368-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>  

## <span data-ttu-id="aa368-110">Flash</span><span class="sxs-lookup"><span data-stu-id="aa368-110">Flash</span></span>  

<span data-ttu-id="aa368-111">Se o Flash for usado na sua página, mas o usuário não o tiver habilitado, o Microsoft Edge normalmente mostrará um ícone de peça de quebra-cabeça na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="aa368-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span>  <span data-ttu-id="aa368-112">Se você estiver adicionando dinamicamente o controle de flash após a página ser carregada, o ícone de quebra-cabeça pode não ser exibido, e nesse caso, você desejará [testar se o flash está carregado e oferecer uma experiência de fallback normal](./browser-features/flash.md) , se não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="aa368-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>  

## <span data-ttu-id="aa368-113">Modo de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="aa368-113">Reading view</span></span>  

<span data-ttu-id="aa368-114">O Microsoft Edge fornece um [modo de exibição de leitura](./browser-features/reading-view.md) para uma experiência de leitura mais simplificada do que o livro de páginas da Web, sem a distração de conteúdo não relacionado ou outro conteúdo secundário na página.</span><span class="sxs-lookup"><span data-stu-id="aa368-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="aa368-115">Aqui estão dicas sobre como garantir uma excelente experiência de exibição de leitura com seu site e também instruções para optar por não usar o seu site no modo de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="aa368-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>  

## <span data-ttu-id="aa368-116">Descoberta de provedores de pesquisa</span><span class="sxs-lookup"><span data-stu-id="aa368-116">Search provider discovery</span></span>  

<span data-ttu-id="aa368-117">A integração de pesquisa avançada está embutida na barra de endereços do Microsoft Edge, incluindo sugestões de pesquisa, resultados da Web, seu histórico de navegação e favoritos.</span><span class="sxs-lookup"><span data-stu-id="aa368-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="aa368-118">[Veja mais informações para provedores de pesquisa](./browser-features/search-provider-discovery.md) que buscam oferecer suporte para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aa368-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>  