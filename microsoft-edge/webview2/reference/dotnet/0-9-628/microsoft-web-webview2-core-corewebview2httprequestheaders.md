---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011442"
---
# <span data-ttu-id="9b36c-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="9b36c-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders class</span></span> 

<span data-ttu-id="9b36c-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9b36c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9b36c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="9b36c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9b36c-107">Cabeçalhos de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b36c-107">HTTP request headers.</span></span>

## <span data-ttu-id="9b36c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9b36c-108">Summary</span></span>

 <span data-ttu-id="9b36c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9b36c-109">Members</span></span>                        | <span data-ttu-id="9b36c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9b36c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b36c-111">Contém</span><span class="sxs-lookup"><span data-stu-id="9b36c-111">Contains</span></span>](#contains) | <span data-ttu-id="9b36c-112">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9b36c-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="9b36c-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="9b36c-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="9b36c-114">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="9b36c-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="9b36c-115">Getheaders</span><span class="sxs-lookup"><span data-stu-id="9b36c-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="9b36c-116">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="9b36c-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="9b36c-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="9b36c-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="9b36c-118">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9b36c-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="9b36c-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="9b36c-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="9b36c-120">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="9b36c-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="9b36c-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="9b36c-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="9b36c-122">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="9b36c-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="9b36c-123">Usado para inspecionar a solicitação HTTP no evento WebResourceRequested e no evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9b36c-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="9b36c-124">Observe que você pode modificar os cabeçalhos de solicitação HTTP de um evento WebResourceRequested, mas não de um evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="9b36c-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="9b36c-125">Parte</span><span class="sxs-lookup"><span data-stu-id="9b36c-125">Members</span></span>

#### <span data-ttu-id="9b36c-126">Contém</span><span class="sxs-lookup"><span data-stu-id="9b36c-126">Contains</span></span> 

<span data-ttu-id="9b36c-127">Verifica se os cabeçalhos contêm uma entrada correspondente ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9b36c-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="9b36c-128">Public bool [contém](#contains)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="9b36c-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="9b36c-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="9b36c-129">GetHeader</span></span> 

<span data-ttu-id="9b36c-130">Obtém o valor do cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="9b36c-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="9b36c-131">Cadeia de caracteres pública [GetHeader](#getheader)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="9b36c-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="9b36c-132">Getheaders</span><span class="sxs-lookup"><span data-stu-id="9b36c-132">GetHeaders</span></span> 

<span data-ttu-id="9b36c-133">Obtém o valor do cabeçalho que corresponde ao nome por meio de um iterador.</span><span class="sxs-lookup"><span data-stu-id="9b36c-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="9b36c-134">[CoreWebView2HttpHeadersCollectionIterator público](#getheaders)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="9b36c-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="9b36c-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="9b36c-135">GetIterator</span></span> 

<span data-ttu-id="9b36c-136">Obtém um iterador sobre a coleção de cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="9b36c-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="9b36c-137">Public CoreWebView2HttpHeadersCollectionIterator [Getiteration](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="9b36c-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

#### <span data-ttu-id="9b36c-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="9b36c-138">RemoveHeader</span></span> 

<span data-ttu-id="9b36c-139">Remove o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="9b36c-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="9b36c-140">public void [RemoveHeader](#removeheader)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="9b36c-140">public void [RemoveHeader](#removeheader)(string name)</span></span>

#### <span data-ttu-id="9b36c-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="9b36c-141">SetHeader</span></span> 

<span data-ttu-id="9b36c-142">Adiciona ou atualiza o cabeçalho que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="9b36c-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="9b36c-143">valor de [cadeia de caracteres void público](#setheader)(nome da cadeia de caracteres, valor da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="9b36c-143">public void [SetHeader](#setheader)(string name, string value)</span></span>

