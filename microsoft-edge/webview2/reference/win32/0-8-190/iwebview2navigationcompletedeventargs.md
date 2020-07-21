---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: b496c37949e934fadf0af736059566edcab9f5c3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885925"
---
# <span data-ttu-id="6db6f-104">0.8.355-IWebView2NavigationCompletedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="6db6f-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="6db6f-105">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6db6f-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="6db6f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="6db6f-106">Summary</span></span>

 <span data-ttu-id="6db6f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="6db6f-107">Members</span></span>                        | <span data-ttu-id="6db6f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="6db6f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6db6f-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6db6f-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="6db6f-110">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6db6f-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="6db6f-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6db6f-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="6db6f-112">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="6db6f-112">The error code if the navigation failed.</span></span>

## <span data-ttu-id="6db6f-113">Parte</span><span class="sxs-lookup"><span data-stu-id="6db6f-113">Members</span></span>

#### <span data-ttu-id="6db6f-114">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6db6f-114">get_IsSuccess</span></span> 

<span data-ttu-id="6db6f-115">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6db6f-115">True when the navigation is successful.</span></span>

> <span data-ttu-id="6db6f-116">[get_IsSuccess](#get_issuccess)público HRESULT (bool \* IsSuccess)</span><span class="sxs-lookup"><span data-stu-id="6db6f-116">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="6db6f-117">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="6db6f-117">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="6db6f-118">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6db6f-118">get_WebErrorStatus</span></span> 

<span data-ttu-id="6db6f-119">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="6db6f-119">The error code if the navigation failed.</span></span>

> <span data-ttu-id="6db6f-120">[get_WebErrorStatus](#get_weberrorstatus)público HRESULT (WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="6db6f-120">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

