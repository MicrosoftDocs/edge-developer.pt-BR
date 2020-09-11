---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011509"
---
# <span data-ttu-id="89115-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="89115-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpHeadersCollectionIterator class</span></span> 

<span data-ttu-id="89115-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="89115-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="89115-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="89115-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="89115-107">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="89115-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="89115-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="89115-108">Summary</span></span>

 <span data-ttu-id="89115-109">Parte</span><span class="sxs-lookup"><span data-stu-id="89115-109">Members</span></span>                        | <span data-ttu-id="89115-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="89115-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89115-111">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="89115-111">HasCurrentHeader</span></span>](#hascurrentheader) | <span data-ttu-id="89115-112">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="89115-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="89115-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="89115-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="89115-114">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="89115-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="89115-115">Consulte CoreWebView2HttpRequestHeaders e CoreWebView2HttpResponseHeaders.</span><span class="sxs-lookup"><span data-stu-id="89115-115">See CoreWebView2HttpRequestHeaders and CoreWebView2HttpResponseHeaders.</span></span>

## <span data-ttu-id="89115-116">Parte</span><span class="sxs-lookup"><span data-stu-id="89115-116">Members</span></span>

#### <span data-ttu-id="89115-117">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="89115-117">HasCurrentHeader</span></span> 

<span data-ttu-id="89115-118">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="89115-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="89115-119">Public bool [HasCurrentHeader](#hascurrentheader)</span><span class="sxs-lookup"><span data-stu-id="89115-119">public bool [HasCurrentHeader](#hascurrentheader)</span></span>

<span data-ttu-id="89115-120">Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.</span><span class="sxs-lookup"><span data-stu-id="89115-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="89115-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="89115-121">MoveNext</span></span> 

<span data-ttu-id="89115-122">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="89115-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="89115-123">Public bool [MoveNext](#movenext)()</span><span class="sxs-lookup"><span data-stu-id="89115-123">public bool [MoveNext](#movenext)()</span></span>

<span data-ttu-id="89115-124">O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="89115-124">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="89115-125">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="89115-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

