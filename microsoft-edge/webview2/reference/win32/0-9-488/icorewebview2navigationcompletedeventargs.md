---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 83f55e19c8c8c0f2fb075ff47e95e34be27c6602
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697333"
---
# <span data-ttu-id="7fb5f-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7fb5f-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7fb5f-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7fb5f-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="7fb5f-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="7fb5f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7fb5f-108">Summary</span></span>

 <span data-ttu-id="7fb5f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7fb5f-109">Members</span></span>                        | <span data-ttu-id="7fb5f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7fb5f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7fb5f-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="7fb5f-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="7fb5f-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="7fb5f-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7fb5f-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7fb5f-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-114">The ID of the navigation.</span></span>
[<span data-ttu-id="7fb5f-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7fb5f-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="7fb5f-116">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="7fb5f-117">Parte</span><span class="sxs-lookup"><span data-stu-id="7fb5f-117">Members</span></span>

#### <span data-ttu-id="7fb5f-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="7fb5f-118">get_IsSuccess</span></span> 

<span data-ttu-id="7fb5f-119">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="7fb5f-120">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="7fb5f-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="7fb5f-121">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="7fb5f-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7fb5f-122">get_NavigationId</span></span> 

<span data-ttu-id="7fb5f-123">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-123">The ID of the navigation.</span></span>

> <span data-ttu-id="7fb5f-124">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="7fb5f-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="7fb5f-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7fb5f-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="7fb5f-126">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="7fb5f-127">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="7fb5f-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

