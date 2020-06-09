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
ms.openlocfilehash: c82c37d7127d69700f35fbf9e2a69f85159a7109
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698263"
---
# <span data-ttu-id="762bd-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="762bd-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="762bd-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="762bd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="762bd-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="762bd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="762bd-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="762bd-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="762bd-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="762bd-108">Summary</span></span>

 <span data-ttu-id="762bd-109">Parte</span><span class="sxs-lookup"><span data-stu-id="762bd-109">Members</span></span>                        | <span data-ttu-id="762bd-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="762bd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="762bd-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="762bd-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="762bd-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="762bd-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="762bd-113">Navigationid</span><span class="sxs-lookup"><span data-stu-id="762bd-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="762bd-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="762bd-114">The ID of the navigation.</span></span>
[<span data-ttu-id="762bd-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="762bd-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="762bd-116">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="762bd-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="762bd-117">Parte</span><span class="sxs-lookup"><span data-stu-id="762bd-117">Members</span></span>

#### <span data-ttu-id="762bd-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="762bd-118">IsSuccess</span></span> 

<span data-ttu-id="762bd-119">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="762bd-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="762bd-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="762bd-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="762bd-121">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="762bd-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="762bd-122">Navigationid</span><span class="sxs-lookup"><span data-stu-id="762bd-122">NavigationId</span></span> 

<span data-ttu-id="762bd-123">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="762bd-123">The ID of the navigation.</span></span>

> <span data-ttu-id="762bd-124">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="762bd-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="762bd-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="762bd-125">WebErrorStatus</span></span> 

<span data-ttu-id="762bd-126">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="762bd-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="762bd-127">CoreWebView2WebErrorStatus público [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="762bd-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

