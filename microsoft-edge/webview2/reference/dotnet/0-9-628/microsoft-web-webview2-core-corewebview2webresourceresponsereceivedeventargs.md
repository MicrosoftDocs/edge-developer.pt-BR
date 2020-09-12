---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: 2d0660616de0c234b1535b2af127843fea3a3a53
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011457"
---
# <span data-ttu-id="34fe4-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="34fe4-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseReceivedEventArgs class</span></span> 

<span data-ttu-id="34fe4-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="34fe4-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="34fe4-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="34fe4-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="34fe4-107">Args de evento para o evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="34fe4-107">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="34fe4-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="34fe4-108">Summary</span></span>

 <span data-ttu-id="34fe4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="34fe4-109">Members</span></span>                        | <span data-ttu-id="34fe4-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="34fe4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34fe4-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="34fe4-111">Request</span></span>](#request) | <span data-ttu-id="34fe4-112">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="34fe4-112">Web resource request object.</span></span>
[<span data-ttu-id="34fe4-113">Resposta</span><span class="sxs-lookup"><span data-stu-id="34fe4-113">Response</span></span>](#response) | <span data-ttu-id="34fe4-114">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="34fe4-114">Web resource response object.</span></span>
[<span data-ttu-id="34fe4-115">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="34fe4-115">PopulateResponseContentAsync</span></span>](#populateresponsecontentasync) | <span data-ttu-id="34fe4-116">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="34fe4-116">Async method to request the Content stream of the response.</span></span>

## <span data-ttu-id="34fe4-117">Parte</span><span class="sxs-lookup"><span data-stu-id="34fe4-117">Members</span></span>

#### <span data-ttu-id="34fe4-118">Solicitação</span><span class="sxs-lookup"><span data-stu-id="34fe4-118">Request</span></span> 

<span data-ttu-id="34fe4-119">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="34fe4-119">Web resource request object.</span></span>

> <span data-ttu-id="34fe4-120">[solicitação](#request) de [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) pública</span><span class="sxs-lookup"><span data-stu-id="34fe4-120">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="34fe4-121">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="34fe4-121">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="34fe4-122">Resposta</span><span class="sxs-lookup"><span data-stu-id="34fe4-122">Response</span></span> 

<span data-ttu-id="34fe4-123">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="34fe4-123">Web resource response object.</span></span>

> <span data-ttu-id="34fe4-124">resposta [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response) pública</span><span class="sxs-lookup"><span data-stu-id="34fe4-124">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="34fe4-125">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="34fe4-125">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="34fe4-126">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="34fe4-126">PopulateResponseContentAsync</span></span> 

<span data-ttu-id="34fe4-127">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="34fe4-127">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="34fe4-128">[PopulateResponseContentAsync](#populateresponsecontentasync)de tarefas assíncronas públicas ()</span><span class="sxs-lookup"><span data-stu-id="34fe4-128">public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span></span>
