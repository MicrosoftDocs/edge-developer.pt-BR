---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: fa1debd3b212492eea03e4ecf6e5daff5751f89b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652554"
---
# <span data-ttu-id="c5532-104">interface IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c5532-104">interface IWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c5532-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c5532-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c5532-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c5532-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="c5532-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="c5532-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="c5532-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c5532-108">Summary</span></span>

 <span data-ttu-id="c5532-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c5532-109">Members</span></span>                        | <span data-ttu-id="c5532-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c5532-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c5532-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="c5532-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="c5532-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c5532-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="c5532-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="c5532-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="c5532-114">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="c5532-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="c5532-115">Parte</span><span class="sxs-lookup"><span data-stu-id="c5532-115">Members</span></span>

#### <span data-ttu-id="c5532-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="c5532-116">get_IsSuccess</span></span> 

<span data-ttu-id="c5532-117">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c5532-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="c5532-118">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="c5532-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="c5532-119">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="c5532-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="c5532-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="c5532-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="c5532-121">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="c5532-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="c5532-122">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="c5532-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

