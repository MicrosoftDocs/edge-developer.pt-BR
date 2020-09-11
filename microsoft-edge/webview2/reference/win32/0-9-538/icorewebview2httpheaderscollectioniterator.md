---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: da1b9f3dbf9ba0ebd309e1017fe4e7f7e6526941
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011316"
---
# <span data-ttu-id="51b58-104">0.9.579-ICoreWebView2HttpHeadersCollectionIterator de interface</span><span class="sxs-lookup"><span data-stu-id="51b58-104">0.9.579 - interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="51b58-105">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="51b58-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="51b58-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="51b58-106">Summary</span></span>

 <span data-ttu-id="51b58-107">Parte</span><span class="sxs-lookup"><span data-stu-id="51b58-107">Members</span></span>                        | <span data-ttu-id="51b58-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="51b58-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51b58-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="51b58-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="51b58-110">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="51b58-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="51b58-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="51b58-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="51b58-112">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="51b58-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="51b58-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="51b58-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="51b58-114">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="51b58-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="51b58-115">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) e [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="51b58-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="51b58-116">Parte</span><span class="sxs-lookup"><span data-stu-id="51b58-116">Members</span></span>

#### <span data-ttu-id="51b58-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="51b58-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="51b58-118">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="51b58-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="51b58-119">[get_HasCurrentHeader](#get_hascurrentheader)público HRESULT (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="51b58-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="51b58-120">Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.</span><span class="sxs-lookup"><span data-stu-id="51b58-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="51b58-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="51b58-121">GetCurrentHeader</span></span> 

<span data-ttu-id="51b58-122">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="51b58-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="51b58-123">Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="51b58-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="51b58-124">Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.</span><span class="sxs-lookup"><span data-stu-id="51b58-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="51b58-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="51b58-125">MoveNext</span></span> 

<span data-ttu-id="51b58-126">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="51b58-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="51b58-127">Public HRESULT [MoveNext](#movenext)(bool \* HasNext)</span><span class="sxs-lookup"><span data-stu-id="51b58-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="51b58-128">O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="51b58-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="51b58-129">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="51b58-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

