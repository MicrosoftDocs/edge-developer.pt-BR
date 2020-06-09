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
ms.openlocfilehash: d3b3f4e78ef37ad2101a3a8f817279e999cea3e3
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697613"
---
# <span data-ttu-id="54619-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="54619-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="54619-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="54619-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="54619-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="54619-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="54619-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="54619-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="54619-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="54619-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="54619-109">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="54619-109">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="54619-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="54619-110">Summary</span></span>

 <span data-ttu-id="54619-111">Parte</span><span class="sxs-lookup"><span data-stu-id="54619-111">Members</span></span>                        | <span data-ttu-id="54619-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="54619-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54619-113">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="54619-113">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="54619-114">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="54619-114">True when the navigation is successful.</span></span>
[<span data-ttu-id="54619-115">Navigationid</span><span class="sxs-lookup"><span data-stu-id="54619-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="54619-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="54619-116">The ID of the navigation.</span></span>
[<span data-ttu-id="54619-117">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="54619-117">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="54619-118">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="54619-118">The error code if the navigation failed.</span></span>

## <span data-ttu-id="54619-119">Parte</span><span class="sxs-lookup"><span data-stu-id="54619-119">Members</span></span>

#### <span data-ttu-id="54619-120">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="54619-120">IsSuccess</span></span> 

<span data-ttu-id="54619-121">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="54619-121">True when the navigation is successful.</span></span>

> <span data-ttu-id="54619-122">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="54619-122">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="54619-123">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="54619-123">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="54619-124">Navigationid</span><span class="sxs-lookup"><span data-stu-id="54619-124">NavigationId</span></span> 

<span data-ttu-id="54619-125">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="54619-125">The ID of the navigation.</span></span>

> <span data-ttu-id="54619-126">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="54619-126">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="54619-127">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="54619-127">WebErrorStatus</span></span> 

<span data-ttu-id="54619-128">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="54619-128">The error code if the navigation failed.</span></span>

> <span data-ttu-id="54619-129">CoreWebView2WebErrorStatus público [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="54619-129">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

