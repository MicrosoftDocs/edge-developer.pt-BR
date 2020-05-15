---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2a18fe9f8f79a109047d029affab8d84a6ef845c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652364"
---
# <span data-ttu-id="7fae2-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7fae2-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="7fae2-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7fae2-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7fae2-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="7fae2-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7fae2-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="7fae2-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="7fae2-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7fae2-108">Summary</span></span>

 <span data-ttu-id="7fae2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7fae2-109">Members</span></span>                        | <span data-ttu-id="7fae2-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7fae2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7fae2-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="7fae2-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="7fae2-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7fae2-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="7fae2-113">Navigationid</span><span class="sxs-lookup"><span data-stu-id="7fae2-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="7fae2-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="7fae2-114">The ID of the navigation.</span></span>
[<span data-ttu-id="7fae2-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7fae2-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="7fae2-116">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="7fae2-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="7fae2-117">Parte</span><span class="sxs-lookup"><span data-stu-id="7fae2-117">Members</span></span>

#### <span data-ttu-id="7fae2-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="7fae2-118">IsSuccess</span></span> 

<span data-ttu-id="7fae2-119">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7fae2-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="7fae2-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="7fae2-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="7fae2-121">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para itens adicionais, como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="7fae2-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="7fae2-122">Navigationid</span><span class="sxs-lookup"><span data-stu-id="7fae2-122">NavigationId</span></span> 

<span data-ttu-id="7fae2-123">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="7fae2-123">The ID of the navigation.</span></span>

> <span data-ttu-id="7fae2-124">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="7fae2-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="7fae2-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7fae2-125">WebErrorStatus</span></span> 

<span data-ttu-id="7fae2-126">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="7fae2-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="7fae2-127">CoreWebView2WebErrorStatus público [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="7fae2-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

