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
ms.openlocfilehash: c720b700257554891f13477f5f3508e331ac6b25
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698201"
---
# <span data-ttu-id="b902b-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="b902b-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b902b-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b902b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b902b-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b902b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="b902b-107">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="b902b-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="b902b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b902b-108">Summary</span></span>

 <span data-ttu-id="b902b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b902b-109">Members</span></span>                        | <span data-ttu-id="b902b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b902b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b902b-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="b902b-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="b902b-112">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="b902b-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="b902b-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="b902b-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="b902b-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="b902b-114">The ID of the navigation.</span></span>

## <span data-ttu-id="b902b-115">Parte</span><span class="sxs-lookup"><span data-stu-id="b902b-115">Members</span></span>

#### <span data-ttu-id="b902b-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="b902b-116">get_IsErrorPage</span></span> 

<span data-ttu-id="b902b-117">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="b902b-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="b902b-118">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="b902b-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="b902b-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="b902b-119">get_NavigationId</span></span> 

<span data-ttu-id="b902b-120">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="b902b-120">The ID of the navigation.</span></span>

> <span data-ttu-id="b902b-121">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="b902b-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

