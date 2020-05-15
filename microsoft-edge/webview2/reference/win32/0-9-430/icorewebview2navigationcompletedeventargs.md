---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: f9d24d10d9487198988b4c6d3ad4a941a32dc396
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652751"
---
# <span data-ttu-id="bd00c-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="bd00c-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="bd00c-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="bd00c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="bd00c-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="bd00c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="bd00c-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="bd00c-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="bd00c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="bd00c-108">Summary</span></span>

 <span data-ttu-id="bd00c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bd00c-109">Members</span></span>                        | <span data-ttu-id="bd00c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="bd00c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd00c-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="bd00c-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="bd00c-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bd00c-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="bd00c-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="bd00c-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="bd00c-114">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="bd00c-114">The error code if the navigation failed.</span></span>
[<span data-ttu-id="bd00c-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="bd00c-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="bd00c-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="bd00c-116">The ID of the navigation.</span></span>

## <span data-ttu-id="bd00c-117">Parte</span><span class="sxs-lookup"><span data-stu-id="bd00c-117">Members</span></span>

#### <span data-ttu-id="bd00c-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="bd00c-118">get_IsSuccess</span></span> 

<span data-ttu-id="bd00c-119">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bd00c-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="bd00c-120">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="bd00c-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="bd00c-121">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="bd00c-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="bd00c-122">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="bd00c-122">get_WebErrorStatus</span></span> 

<span data-ttu-id="bd00c-123">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="bd00c-123">The error code if the navigation failed.</span></span>

> <span data-ttu-id="bd00c-124">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="bd00c-124">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="bd00c-125">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="bd00c-125">get_NavigationId</span></span> 

<span data-ttu-id="bd00c-126">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="bd00c-126">The ID of the navigation.</span></span>

> <span data-ttu-id="bd00c-127">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="bd00c-127">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

