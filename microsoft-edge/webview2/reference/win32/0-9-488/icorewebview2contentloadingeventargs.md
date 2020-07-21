---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 32b0f46b00195a265238541f8715ec21ca3757a1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883872"
---
# <span data-ttu-id="78ef0-104">0.9.515-ICoreWebView2ContentLoadingEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="78ef0-104">0.9.515 - interface ICoreWebView2ContentLoadingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="78ef0-105">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="78ef0-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="78ef0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="78ef0-106">Summary</span></span>

 <span data-ttu-id="78ef0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="78ef0-107">Members</span></span>                        | <span data-ttu-id="78ef0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="78ef0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="78ef0-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="78ef0-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="78ef0-110">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="78ef0-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="78ef0-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="78ef0-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="78ef0-112">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="78ef0-112">The ID of the navigation.</span></span>

## <span data-ttu-id="78ef0-113">Parte</span><span class="sxs-lookup"><span data-stu-id="78ef0-113">Members</span></span>

#### <span data-ttu-id="78ef0-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="78ef0-114">get_IsErrorPage</span></span> 

<span data-ttu-id="78ef0-115">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="78ef0-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="78ef0-116">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="78ef0-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="78ef0-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="78ef0-117">get_NavigationId</span></span> 

<span data-ttu-id="78ef0-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="78ef0-118">The ID of the navigation.</span></span>

> <span data-ttu-id="78ef0-119">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="78ef0-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

