---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: b45920cfdab8a01d1288fbaf566748545b8a2c98
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011491"
---
# <span data-ttu-id="5b270-104">interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5b270-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="5b270-105">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="5b270-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="5b270-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5b270-106">Summary</span></span>

 <span data-ttu-id="5b270-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5b270-107">Members</span></span>                        | <span data-ttu-id="5b270-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5b270-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5b270-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="5b270-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="5b270-110">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5b270-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="5b270-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="5b270-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="5b270-112">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="5b270-112">The ID of the navigation.</span></span>
[<span data-ttu-id="5b270-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="5b270-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="5b270-114">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="5b270-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="5b270-115">Parte</span><span class="sxs-lookup"><span data-stu-id="5b270-115">Members</span></span>

#### <span data-ttu-id="5b270-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="5b270-116">get_IsSuccess</span></span> 

<span data-ttu-id="5b270-117">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5b270-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="5b270-118">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="5b270-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="5b270-119">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para cenários adicionais como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="5b270-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="5b270-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="5b270-120">get_NavigationId</span></span> 

<span data-ttu-id="5b270-121">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="5b270-121">The ID of the navigation.</span></span>

> <span data-ttu-id="5b270-122">[get_NavigationId](#get_navigationid)público HRESULT (UINT64 \* navigationid)</span><span class="sxs-lookup"><span data-stu-id="5b270-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="5b270-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="5b270-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="5b270-124">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="5b270-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="5b270-125">público HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* WebErrorStatus)</span><span class="sxs-lookup"><span data-stu-id="5b270-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* webErrorStatus)</span></span>

