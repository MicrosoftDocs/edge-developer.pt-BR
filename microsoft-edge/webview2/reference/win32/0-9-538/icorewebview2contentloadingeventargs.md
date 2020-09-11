---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: d70673714e3641e19f5c3d6367278c0c7bd2729b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010296"
---
# <span data-ttu-id="a5b99-104">0.9.579-ICoreWebView2ContentLoadingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="a5b99-104">0.9.579 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="a5b99-105">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a5b99-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="a5b99-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="a5b99-106">Summary</span></span>

 <span data-ttu-id="a5b99-107">Parte</span><span class="sxs-lookup"><span data-stu-id="a5b99-107">Members</span></span>                        | <span data-ttu-id="a5b99-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="a5b99-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5b99-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a5b99-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="a5b99-110">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="a5b99-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="a5b99-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a5b99-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a5b99-112">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a5b99-112">The ID of the navigation.</span></span>

## <span data-ttu-id="a5b99-113">Parte</span><span class="sxs-lookup"><span data-stu-id="a5b99-113">Members</span></span>

#### <span data-ttu-id="a5b99-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="a5b99-114">get_IsErrorPage</span></span> 

<span data-ttu-id="a5b99-115">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="a5b99-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="a5b99-116">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="a5b99-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="a5b99-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a5b99-117">get_NavigationId</span></span> 

<span data-ttu-id="a5b99-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="a5b99-118">The ID of the navigation.</span></span>

> <span data-ttu-id="a5b99-119">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="a5b99-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

