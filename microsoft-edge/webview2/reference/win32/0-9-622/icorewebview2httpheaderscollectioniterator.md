---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: 8044b629c5b182d98e4731409301f615a6fba18e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011575"
---
# <span data-ttu-id="ba805-104">interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="ba805-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="ba805-105">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="ba805-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="ba805-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ba805-106">Summary</span></span>

 <span data-ttu-id="ba805-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ba805-107">Members</span></span>                        | <span data-ttu-id="ba805-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ba805-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ba805-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ba805-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="ba805-110">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="ba805-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="ba805-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ba805-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="ba805-112">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="ba805-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="ba805-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="ba805-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="ba805-114">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="ba805-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="ba805-115">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) e [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="ba805-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span>

```cpp
std::wstring RequestHeadersToJsonString(ICoreWebView2HttpRequestHeaders* requestHeaders)
{
    wil::com_ptr<ICoreWebView2HttpHeadersCollectionIterator> iterator;
    CHECK_FAILURE(requestHeaders->GetIterator(&iterator));
    BOOL hasCurrent = FALSE;
    std::wstring result = L"[";

    while (SUCCEEDED(iterator->get_HasCurrentHeader(&hasCurrent)) && hasCurrent)
    {
        wil::unique_cotaskmem_string name;
        wil::unique_cotaskmem_string value;

        CHECK_FAILURE(iterator->GetCurrentHeader(&name, &value));
        result += L"{\"name\": " + EncodeQuote(name.get())
            + L", \"value\": " + EncodeQuote(value.get()) + L"}";

        BOOL hasNext = FALSE;
        CHECK_FAILURE(iterator->MoveNext(&hasNext));
        if (hasNext)
        {
            result += L", ";
        }
    }

    return result + L"]";
}
```

## <span data-ttu-id="ba805-116">Parte</span><span class="sxs-lookup"><span data-stu-id="ba805-116">Members</span></span>

#### <span data-ttu-id="ba805-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ba805-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="ba805-118">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="ba805-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="ba805-119">[get_HasCurrentHeader](#get_hascurrentheader)público HRESULT (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="ba805-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="ba805-120">Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.</span><span class="sxs-lookup"><span data-stu-id="ba805-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="ba805-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="ba805-121">GetCurrentHeader</span></span> 

<span data-ttu-id="ba805-122">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="ba805-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="ba805-123">Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="ba805-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="ba805-124">Esse método irá falhar se a última chamada para MoveNext definir hasNext como FALSE.</span><span class="sxs-lookup"><span data-stu-id="ba805-124">This method will fail if the last call to MoveNext set hasNext to FALSE.</span></span>

#### <span data-ttu-id="ba805-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="ba805-125">MoveNext</span></span> 

<span data-ttu-id="ba805-126">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="ba805-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="ba805-127">Public HRESULT [MoveNext](#movenext)(bool \* HasNext)</span><span class="sxs-lookup"><span data-stu-id="ba805-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="ba805-128">O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="ba805-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="ba805-129">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="ba805-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

