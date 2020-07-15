---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 215297bf56234452aad33e135cfb03ec079a049b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877970"
---
# <span data-ttu-id="4b209-104">0.9.430-ICoreWebView2NavigationCompletedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="4b209-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4b209-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4b209-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4b209-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="4b209-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="4b209-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="4b209-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="4b209-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4b209-108">Summary</span></span>

 <span data-ttu-id="4b209-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4b209-109">Members</span></span>                        | <span data-ttu-id="4b209-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4b209-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4b209-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="4b209-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="4b209-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4b209-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="4b209-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="4b209-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="4b209-114">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="4b209-114">The error code if the navigation failed.</span></span>
[<span data-ttu-id="4b209-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="4b209-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="4b209-116">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="4b209-116">The ID of the navigation.</span></span>

## <span data-ttu-id="4b209-117">Parte</span><span class="sxs-lookup"><span data-stu-id="4b209-117">Members</span></span>

#### <span data-ttu-id="4b209-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="4b209-118">get_IsSuccess</span></span> 

<span data-ttu-id="4b209-119">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4b209-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="4b209-120">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="4b209-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="4b209-121">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="4b209-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="4b209-122">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="4b209-122">get_WebErrorStatus</span></span> 

<span data-ttu-id="4b209-123">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="4b209-123">The error code if the navigation failed.</span></span>

> <span data-ttu-id="4b209-124">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="4b209-124">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="4b209-125">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="4b209-125">get_NavigationId</span></span> 

<span data-ttu-id="4b209-126">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="4b209-126">The ID of the navigation.</span></span>

> <span data-ttu-id="4b209-127">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="4b209-127">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

