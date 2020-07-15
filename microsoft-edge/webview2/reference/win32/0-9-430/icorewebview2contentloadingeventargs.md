---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 95fa97268fb5695aebf5c1414752cf12cf1da57b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881141"
---
# <span data-ttu-id="85d97-104">0.9.430-ICoreWebView2ContentLoadingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="85d97-104">0.9.430 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="85d97-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="85d97-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="85d97-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="85d97-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="85d97-107">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="85d97-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="85d97-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="85d97-108">Summary</span></span>

 <span data-ttu-id="85d97-109">Parte</span><span class="sxs-lookup"><span data-stu-id="85d97-109">Members</span></span>                        | <span data-ttu-id="85d97-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="85d97-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85d97-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="85d97-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="85d97-112">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="85d97-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="85d97-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="85d97-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="85d97-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="85d97-114">The ID of the navigation.</span></span>

## <span data-ttu-id="85d97-115">Parte</span><span class="sxs-lookup"><span data-stu-id="85d97-115">Members</span></span>

#### <span data-ttu-id="85d97-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="85d97-116">get_IsErrorPage</span></span> 

<span data-ttu-id="85d97-117">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="85d97-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="85d97-118">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="85d97-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="85d97-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="85d97-119">get_NavigationId</span></span> 

<span data-ttu-id="85d97-120">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="85d97-120">The ID of the navigation.</span></span>

> <span data-ttu-id="85d97-121">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="85d97-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

