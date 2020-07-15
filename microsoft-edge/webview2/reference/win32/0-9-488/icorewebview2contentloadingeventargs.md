---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: a5dd8dc0b504faad7c02669ae464ca1ef75c88af
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880777"
---
# <span data-ttu-id="e0d96-104">0.9.515-ICoreWebView2ContentLoadingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="e0d96-104">0.9.515 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e0d96-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e0d96-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e0d96-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e0d96-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="e0d96-107">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="e0d96-107">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="e0d96-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e0d96-108">Summary</span></span>

 <span data-ttu-id="e0d96-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e0d96-109">Members</span></span>                        | <span data-ttu-id="e0d96-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e0d96-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0d96-111">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e0d96-111">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="e0d96-112">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="e0d96-112">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="e0d96-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e0d96-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="e0d96-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="e0d96-114">The ID of the navigation.</span></span>

## <span data-ttu-id="e0d96-115">Parte</span><span class="sxs-lookup"><span data-stu-id="e0d96-115">Members</span></span>

#### <span data-ttu-id="e0d96-116">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="e0d96-116">get_IsErrorPage</span></span> 

<span data-ttu-id="e0d96-117">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="e0d96-117">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="e0d96-118">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="e0d96-118">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="e0d96-119">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="e0d96-119">get_NavigationId</span></span> 

<span data-ttu-id="e0d96-120">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="e0d96-120">The ID of the navigation.</span></span>

> <span data-ttu-id="e0d96-121">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="e0d96-121">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

