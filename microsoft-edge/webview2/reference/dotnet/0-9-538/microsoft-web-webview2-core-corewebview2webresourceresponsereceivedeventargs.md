---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
ms.openlocfilehash: a8c988fdfee72ed22e74886b440819d7a9d6fe24
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010506"
---
# <span data-ttu-id="49d0a-104">classe 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="49d0a-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseReceivedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="49d0a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="49d0a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="49d0a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="49d0a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="49d0a-107">Args de evento para o evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="49d0a-107">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="49d0a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="49d0a-108">Summary</span></span>

 <span data-ttu-id="49d0a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="49d0a-109">Members</span></span>                        | <span data-ttu-id="49d0a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="49d0a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49d0a-111">Solicitação</span><span class="sxs-lookup"><span data-stu-id="49d0a-111">Request</span></span>](#request) | <span data-ttu-id="49d0a-112">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="49d0a-112">Web resource request object.</span></span>
[<span data-ttu-id="49d0a-113">Resposta</span><span class="sxs-lookup"><span data-stu-id="49d0a-113">Response</span></span>](#response) | <span data-ttu-id="49d0a-114">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="49d0a-114">Web resource response object.</span></span>
[<span data-ttu-id="49d0a-115">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="49d0a-115">PopulateResponseContentAsync</span></span>](#populateresponsecontentasync) | <span data-ttu-id="49d0a-116">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="49d0a-116">Async method to request the Content stream of the response.</span></span>

## <span data-ttu-id="49d0a-117">Parte</span><span class="sxs-lookup"><span data-stu-id="49d0a-117">Members</span></span>

#### <span data-ttu-id="49d0a-118">Solicitação</span><span class="sxs-lookup"><span data-stu-id="49d0a-118">Request</span></span> 

<span data-ttu-id="49d0a-119">Objeto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="49d0a-119">Web resource request object.</span></span>

> <span data-ttu-id="49d0a-120">[solicitação](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="49d0a-120">public HttpRequestMessage [Request](#request)</span></span>

<span data-ttu-id="49d0a-121">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="49d0a-121">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="49d0a-122">Resposta</span><span class="sxs-lookup"><span data-stu-id="49d0a-122">Response</span></span> 

<span data-ttu-id="49d0a-123">Objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="49d0a-123">Web resource response object.</span></span>

> <span data-ttu-id="49d0a-124">[resposta](#response) HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="49d0a-124">public HttpResponseMessage [Response](#response)</span></span>

<span data-ttu-id="49d0a-125">Todas as modificações feitas neste objeto serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="49d0a-125">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="49d0a-126">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="49d0a-126">PopulateResponseContentAsync</span></span> 

<span data-ttu-id="49d0a-127">Método Async para solicitar o fluxo de conteúdo da resposta.</span><span class="sxs-lookup"><span data-stu-id="49d0a-127">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="49d0a-128">[PopulateResponseContentAsync](#populateresponsecontentasync)de tarefas assíncronas públicas ()</span><span class="sxs-lookup"><span data-stu-id="49d0a-128">public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span></span>

