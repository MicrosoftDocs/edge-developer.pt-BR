---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: dfa6aedb10e60a2af15c7b098c479f8537d6c747
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011436"
---
# <span data-ttu-id="9ca3d-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ca3d-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="9ca3d-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9ca3d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9ca3d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="9ca3d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9ca3d-107">Args de evento para o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="9ca3d-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9ca3d-108">Summary</span></span>

 <span data-ttu-id="9ca3d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9ca3d-109">Members</span></span>                        | <span data-ttu-id="9ca3d-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9ca3d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ca3d-111">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="9ca3d-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="9ca3d-112">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="9ca3d-113">Navigationid</span><span class="sxs-lookup"><span data-stu-id="9ca3d-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="9ca3d-114">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-114">The ID of the navigation.</span></span>
[<span data-ttu-id="9ca3d-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="9ca3d-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="9ca3d-116">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="9ca3d-117">Parte</span><span class="sxs-lookup"><span data-stu-id="9ca3d-117">Members</span></span>

#### <span data-ttu-id="9ca3d-118">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="9ca3d-118">IsSuccess</span></span> 

<span data-ttu-id="9ca3d-119">Verdadeiro quando a navegação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="9ca3d-120">Public bool [IsSuccess](#issuccess)</span><span class="sxs-lookup"><span data-stu-id="9ca3d-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="9ca3d-121">Isso é falso para uma navegação que terminou em uma página de erro (falhas devido à falta de rede, falha na pesquisa de DNS, o servidor HTTP responde com 4xx), mas também pode ser falso para cenários adicionais como Window. Stop () chamado na página navegada.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="9ca3d-122">Navigationid</span><span class="sxs-lookup"><span data-stu-id="9ca3d-122">NavigationId</span></span> 

<span data-ttu-id="9ca3d-123">A ID da navegação.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-123">The ID of the navigation.</span></span>

> <span data-ttu-id="9ca3d-124">[navegação](#navigationid) de ULong do ULONG público</span><span class="sxs-lookup"><span data-stu-id="9ca3d-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="9ca3d-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="9ca3d-125">WebErrorStatus</span></span> 

<span data-ttu-id="9ca3d-126">O código de erro se a navegação falhar.</span><span class="sxs-lookup"><span data-stu-id="9ca3d-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="9ca3d-127">CoreWebView2WebErrorStatus público [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="9ca3d-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

