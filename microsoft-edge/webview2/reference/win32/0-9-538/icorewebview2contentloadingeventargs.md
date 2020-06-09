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
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698308"
---
# <span data-ttu-id="d034c-104">interface ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="d034c-104">interface ICoreWebView2ContentLoadingEventArgs</span></span> 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

<span data-ttu-id="d034c-105">Args de evento para o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d034c-105">Event args for the ContentLoading event.</span></span>

## <span data-ttu-id="d034c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d034c-106">Summary</span></span>

 <span data-ttu-id="d034c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d034c-107">Members</span></span>                        | <span data-ttu-id="d034c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d034c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d034c-109">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d034c-109">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="d034c-110">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="d034c-110">True if the loaded content is an error page.</span></span>
[<span data-ttu-id="d034c-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d034c-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="d034c-112">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="d034c-112">The ID of the navigation.</span></span>

## <span data-ttu-id="d034c-113">Parte</span><span class="sxs-lookup"><span data-stu-id="d034c-113">Members</span></span>

#### <span data-ttu-id="d034c-114">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="d034c-114">get_IsErrorPage</span></span> 

<span data-ttu-id="d034c-115">Verdadeiro se o conteúdo carregado for uma página de erro.</span><span class="sxs-lookup"><span data-stu-id="d034c-115">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="d034c-116">[get_IsErrorPage](#get_iserrorpage)público HRESULT (bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="d034c-116">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

#### <span data-ttu-id="d034c-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="d034c-117">get_NavigationId</span></span> 

<span data-ttu-id="d034c-118">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="d034c-118">The ID of the navigation.</span></span>

> <span data-ttu-id="d034c-119">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="d034c-119">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

