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
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652521"
---
# <span data-ttu-id="04bda-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="04bda-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="04bda-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="04bda-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="04bda-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="04bda-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="04bda-107">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="04bda-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="04bda-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="04bda-108">Summary</span></span>

 <span data-ttu-id="04bda-109">Parte</span><span class="sxs-lookup"><span data-stu-id="04bda-109">Members</span></span>                        | <span data-ttu-id="04bda-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="04bda-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04bda-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="04bda-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="04bda-112">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="04bda-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="04bda-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="04bda-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="04bda-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="04bda-114">The ID of the navigation.</span></span>

## <span data-ttu-id="04bda-115">Parte</span><span class="sxs-lookup"><span data-stu-id="04bda-115">Members</span></span>

#### <span data-ttu-id="04bda-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="04bda-116">get_IsErrorPage</span></span> 

<span data-ttu-id="04bda-117">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="04bda-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="04bda-118">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="04bda-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="04bda-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="04bda-119">get_NavigationId</span></span> 

<span data-ttu-id="04bda-120">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="04bda-120">The ID of the navigation.</span></span>

> <span data-ttu-id="04bda-121">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="04bda-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

