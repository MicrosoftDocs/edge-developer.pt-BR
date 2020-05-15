---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652630"
---
# <span data-ttu-id="fc4fb-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="fc4fb-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="fc4fb-105">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="fc4fb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="fc4fb-106">Summary</span></span>

 <span data-ttu-id="fc4fb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="fc4fb-107">Members</span></span>                        | <span data-ttu-id="fc4fb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="fc4fb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fc4fb-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="fc4fb-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="fc4fb-110">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="fc4fb-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="fc4fb-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="fc4fb-112">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-112">The ID of the navigation.</span></span>

## <span data-ttu-id="fc4fb-113">Parte</span><span class="sxs-lookup"><span data-stu-id="fc4fb-113">Members</span></span>

#### <span data-ttu-id="fc4fb-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="fc4fb-114">get_IsErrorPage</span></span> 

<span data-ttu-id="fc4fb-115">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="fc4fb-116">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="fc4fb-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="fc4fb-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="fc4fb-117">get_NavigationId</span></span> 

<span data-ttu-id="fc4fb-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="fc4fb-118">The ID of the navigation.</span></span>

> <span data-ttu-id="fc4fb-119">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="fc4fb-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

