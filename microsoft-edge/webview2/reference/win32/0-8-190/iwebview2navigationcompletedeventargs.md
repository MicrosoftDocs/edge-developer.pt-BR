---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 7c10e669b4caf13f43f858e343c9bad3da155518
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878411"
---
# <span data-ttu-id="8d8ec-104">0.8.355-IWebView2NavigationCompletedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="8d8ec-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8d8ec-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="8d8ec-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="8d8ec-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="8d8ec-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8d8ec-108">Summary</span></span>

 <span data-ttu-id="8d8ec-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8d8ec-109">Members</span></span>                        | <span data-ttu-id="8d8ec-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8d8ec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8d8ec-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="8d8ec-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="8d8ec-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="8d8ec-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="8d8ec-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="8d8ec-114">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="8d8ec-115">Parte</span><span class="sxs-lookup"><span data-stu-id="8d8ec-115">Members</span></span>

#### <span data-ttu-id="8d8ec-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="8d8ec-116">get_IsSuccess</span></span> 

<span data-ttu-id="8d8ec-117">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="8d8ec-118">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="8d8ec-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="8d8ec-119">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="8d8ec-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="8d8ec-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="8d8ec-121">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="8d8ec-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="8d8ec-122">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="8d8ec-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

