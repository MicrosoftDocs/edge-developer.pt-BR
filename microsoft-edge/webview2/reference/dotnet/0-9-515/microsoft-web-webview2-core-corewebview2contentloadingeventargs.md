---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: abe167548b7e604bd60c792660ea5b52dec9b848
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697298"
---
# <span data-ttu-id="a71a1-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a71a1-104">Microsoft.Web.WebView2.Core.CoreWebView2ContentLoadingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="a71a1-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a71a1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a71a1-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a71a1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="a71a1-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a71a1-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a71a1-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="a71a1-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a71a1-109">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a71a1-109">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="a71a1-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="a71a1-110">Summary</span></span>

 <span data-ttu-id="a71a1-111">Parte</span><span class="sxs-lookup"><span data-stu-id="a71a1-111">Members</span></span>                        | <span data-ttu-id="a71a1-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="a71a1-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a71a1-113">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a71a1-113">IsErrorPage</span></span>](#iserrorpage) | <span data-ttu-id="a71a1-114">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="a71a1-114">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="a71a1-115">Navigationid</span><span class="sxs-lookup"><span data-stu-id="a71a1-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="a71a1-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a71a1-116">The ID of the navigation.</span></span>

## <span data-ttu-id="a71a1-117">Parte</span><span class="sxs-lookup"><span data-stu-id="a71a1-117">Members</span></span>

#### <span data-ttu-id="a71a1-118">IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a71a1-118">IsErrorPage</span></span> 

<span data-ttu-id="a71a1-119">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="a71a1-119">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="a71a1-120">Public bool [IsErrorPage](#iserrorpage)</span><span class="sxs-lookup"><span data-stu-id="a71a1-120">public bool [IsErrorPage](#iserrorpage)</span></span>

#### <span data-ttu-id="a71a1-121">Navigationid</span><span class="sxs-lookup"><span data-stu-id="a71a1-121">NavigationId</span></span> 

<span data-ttu-id="a71a1-122">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a71a1-122">The ID of the navigation.</span></span>

> <span data-ttu-id="a71a1-123">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="a71a1-123">public ulong [NavigationId](#navigationid)</span></span>

