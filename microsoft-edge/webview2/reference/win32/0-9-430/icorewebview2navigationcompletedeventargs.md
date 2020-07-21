---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883725"
---
# <span data-ttu-id="6f0ac-104">0.9.430-ICoreWebView2NavigationCompletedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="6f0ac-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="6f0ac-105">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="6f0ac-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6f0ac-106">Summary</span></span>

 <span data-ttu-id="6f0ac-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6f0ac-107">Members</span></span>                        | <span data-ttu-id="6f0ac-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6f0ac-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f0ac-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6f0ac-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="6f0ac-110">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="6f0ac-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6f0ac-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="6f0ac-112">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-112">The error code if the navigation failed.</span></span>
[<span data-ttu-id="6f0ac-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6f0ac-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6f0ac-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-114">The ID of the navigation.</span></span>

## <span data-ttu-id="6f0ac-115">Parte</span><span class="sxs-lookup"><span data-stu-id="6f0ac-115">Members</span></span>

#### <span data-ttu-id="6f0ac-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6f0ac-116">get_IsSuccess</span></span> 

<span data-ttu-id="6f0ac-117">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="6f0ac-118">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="6f0ac-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="6f0ac-119">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="6f0ac-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6f0ac-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="6f0ac-121">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="6f0ac-122">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="6f0ac-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="6f0ac-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6f0ac-123">get_NavigationId</span></span> 

<span data-ttu-id="6f0ac-124">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="6f0ac-124">The ID of the navigation.</span></span>

> <span data-ttu-id="6f0ac-125">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="6f0ac-125">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

