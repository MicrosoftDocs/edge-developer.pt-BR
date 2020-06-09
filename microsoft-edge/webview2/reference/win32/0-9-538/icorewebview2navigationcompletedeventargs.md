---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 11d7e5ffef11a445c55cd4a9d70fcbbb8087c024
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698336"
---
# <span data-ttu-id="9288d-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9288d-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="9288d-105">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9288d-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="9288d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="9288d-106">Summary</span></span>

 <span data-ttu-id="9288d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="9288d-107">Members</span></span>                        | <span data-ttu-id="9288d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="9288d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9288d-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="9288d-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="9288d-110">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9288d-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="9288d-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="9288d-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="9288d-112">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="9288d-112">The ID of the navigation.</span></span>
[<span data-ttu-id="9288d-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="9288d-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="9288d-114">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="9288d-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="9288d-115">Parte</span><span class="sxs-lookup"><span data-stu-id="9288d-115">Members</span></span>

#### <span data-ttu-id="9288d-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="9288d-116">get_IsSuccess</span></span> 

<span data-ttu-id="9288d-117">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9288d-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="9288d-118">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="9288d-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="9288d-119">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="9288d-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="9288d-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="9288d-120">get_NavigationId</span></span> 

<span data-ttu-id="9288d-121">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="9288d-121">The ID of the navigation.</span></span>

> <span data-ttu-id="9288d-122">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="9288d-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="9288d-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="9288d-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="9288d-124">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="9288d-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="9288d-125">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="9288d-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

