---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2e55a43282a7548acefdb0b1ed1b8cac2254ef21
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010387"
---
# <span data-ttu-id="640d1-104">0.9.579-ICoreWebView2WebResourceRequestedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="640d1-104">0.9.579 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="640d1-105">Args de evento para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="640d1-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="640d1-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="640d1-106">Summary</span></span>

 <span data-ttu-id="640d1-107">Parte</span><span class="sxs-lookup"><span data-stu-id="640d1-107">Members</span></span>                        | <span data-ttu-id="640d1-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="640d1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="640d1-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="640d1-109">get_Request</span></span>](#get_request) | <span data-ttu-id="640d1-110">Solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="640d1-110">The Web resource request.</span></span>
[<span data-ttu-id="640d1-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="640d1-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="640d1-112">O contexto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="640d1-112">The web resource request context.</span></span>
[<span data-ttu-id="640d1-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="640d1-113">get_Response</span></span>](#get_response) | <span data-ttu-id="640d1-114">Um espaço reservado para o objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="640d1-114">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="640d1-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="640d1-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="640d1-116">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="640d1-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="640d1-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="640d1-117">put_Response</span></span>](#put_response) | <span data-ttu-id="640d1-118">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="640d1-118">Set the Response property.</span></span>

## <span data-ttu-id="640d1-119">Parte</span><span class="sxs-lookup"><span data-stu-id="640d1-119">Members</span></span>

#### <span data-ttu-id="640d1-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="640d1-120">get_Request</span></span> 

<span data-ttu-id="640d1-121">Solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="640d1-121">The Web resource request.</span></span>

> <span data-ttu-id="640d1-122">Public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \* Request)</span><span class="sxs-lookup"><span data-stu-id="640d1-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

<span data-ttu-id="640d1-123">O objeto de solicitação pode não ter alguns cabeçalhos que são adicionados pela pilha de rede mais tarde.</span><span class="sxs-lookup"><span data-stu-id="640d1-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="640d1-124">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="640d1-124">get_ResourceContext</span></span> 

<span data-ttu-id="640d1-125">O contexto de solicitação de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="640d1-125">The web resource request context.</span></span>

> <span data-ttu-id="640d1-126">[get_ResourceContext](#get_resourcecontext)público HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* contexto)</span><span class="sxs-lookup"><span data-stu-id="640d1-126">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="640d1-127">get_Response</span><span class="sxs-lookup"><span data-stu-id="640d1-127">get_Response</span></span> 

<span data-ttu-id="640d1-128">Um espaço reservado para o objeto de resposta de recurso da Web.</span><span class="sxs-lookup"><span data-stu-id="640d1-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="640d1-129">público HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* resposta)</span><span class="sxs-lookup"><span data-stu-id="640d1-129">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="640d1-130">Se esse objeto estiver definido, a solicitação de recurso da Web será concluída com essa resposta.</span><span class="sxs-lookup"><span data-stu-id="640d1-130">If this object is set, the web resource request will be completed with this response.</span></span>

#### <span data-ttu-id="640d1-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="640d1-131">GetDeferral</span></span> 

<span data-ttu-id="640d1-132">Obtenha um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) e coloque o evento em um estado adiado.</span><span class="sxs-lookup"><span data-stu-id="640d1-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="640d1-133">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="640d1-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="640d1-134">Você pode usar o objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para concluir a solicitação em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="640d1-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the request at a later time.</span></span>

#### <span data-ttu-id="640d1-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="640d1-135">put_Response</span></span> 

<span data-ttu-id="640d1-136">Defina a propriedade Response.</span><span class="sxs-lookup"><span data-stu-id="640d1-136">Set the Response property.</span></span>

> <span data-ttu-id="640d1-137">público HRESULT [put_Response](#put_response)(resposta[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="640d1-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

<span data-ttu-id="640d1-138">Um objeto de resposta de recurso da Web vazio pode ser criado com CreateWebResourceResponse e, em seguida, modificado para construir a resposta.</span><span class="sxs-lookup"><span data-stu-id="640d1-138">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

