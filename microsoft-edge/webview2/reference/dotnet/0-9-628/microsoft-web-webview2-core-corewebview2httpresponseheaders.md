---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011506"
---
# <span data-ttu-id="61f04-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="61f04-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders class</span></span> 

<span data-ttu-id="61f04-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="61f04-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="61f04-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="61f04-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="61f04-107">Cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="61f04-107">HTTP response headers.</span></span>

## <span data-ttu-id="61f04-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="61f04-108">Summary</span></span>

 <span data-ttu-id="61f04-109">Parte</span><span class="sxs-lookup"><span data-stu-id="61f04-109">Members</span></span>                        | <span data-ttu-id="61f04-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="61f04-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61f04-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="61f04-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="61f04-112">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="61f04-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="61f04-113">Contém</span><span class="sxs-lookup"><span data-stu-id="61f04-113">Contains</span></span>](#contains) | <span data-ttu-id="61f04-114">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="61f04-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="61f04-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="61f04-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="61f04-116">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="61f04-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="61f04-117">Getheaders</span><span class="sxs-lookup"><span data-stu-id="61f04-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="61f04-118">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="61f04-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="61f04-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="61f04-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="61f04-120">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="61f04-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="61f04-121">Usado para construir um WebResourceResponse para o evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="61f04-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="61f04-122">Parte</span><span class="sxs-lookup"><span data-stu-id="61f04-122">Members</span></span>

#### <span data-ttu-id="61f04-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="61f04-123">AppendHeader</span></span> 

<span data-ttu-id="61f04-124">Acrescenta uma linha de cabeçalho com nome e valor.</span><span class="sxs-lookup"><span data-stu-id="61f04-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="61f04-125">public void [AppendHeader](#appendheader)(nome da cadeia de caracteres, valor da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="61f04-125">public void [AppendHeader](#appendheader)(string name, string value)</span></span>

#### <span data-ttu-id="61f04-126">Contém</span><span class="sxs-lookup"><span data-stu-id="61f04-126">Contains</span></span> 

<span data-ttu-id="61f04-127">Verifica se os cabeçalhos contêm entradas correspondentes ao nome do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="61f04-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="61f04-128">Public bool [contém](#contains)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="61f04-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="61f04-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="61f04-129">GetHeader</span></span> 

<span data-ttu-id="61f04-130">Obtém o primeiro valor de cabeçalho na coleção que corresponde ao nome.</span><span class="sxs-lookup"><span data-stu-id="61f04-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="61f04-131">Cadeia de caracteres pública [GetHeader](#getheader)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="61f04-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="61f04-132">Getheaders</span><span class="sxs-lookup"><span data-stu-id="61f04-132">GetHeaders</span></span> 

<span data-ttu-id="61f04-133">Obtém os valores de cabeçalho correspondentes ao nome.</span><span class="sxs-lookup"><span data-stu-id="61f04-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="61f04-134">[CoreWebView2HttpHeadersCollectionIterator público](#getheaders)(nome da cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="61f04-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="61f04-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="61f04-135">GetIterator</span></span> 

<span data-ttu-id="61f04-136">Obtém um iterador sobre a coleção de cabeçalhos de resposta inteiros.</span><span class="sxs-lookup"><span data-stu-id="61f04-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="61f04-137">Public CoreWebView2HttpHeadersCollectionIterator [Getiteration](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="61f04-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

