---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 9e94291c55680e03c48a5fbf1b48f9d79a790cb6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652504"
---
# <span data-ttu-id="c5842-104">interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="c5842-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="c5842-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c5842-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c5842-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="c5842-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="c5842-107">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5842-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="c5842-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="c5842-108">Summary</span></span>

 <span data-ttu-id="c5842-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c5842-109">Members</span></span>                        | <span data-ttu-id="c5842-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="c5842-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c5842-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c5842-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="c5842-112">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="c5842-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="c5842-113">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c5842-113">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="c5842-114">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="c5842-114">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="c5842-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="c5842-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="c5842-116">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="c5842-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="c5842-117">Consulte [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) e [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="c5842-117">See [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) and [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span></span> 

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

## <span data-ttu-id="c5842-118">Parte</span><span class="sxs-lookup"><span data-stu-id="c5842-118">Members</span></span>

#### <span data-ttu-id="c5842-119">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c5842-119">GetCurrentHeader</span></span> 

<span data-ttu-id="c5842-120">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="c5842-120">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="c5842-121">Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="c5842-121">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="c5842-122">Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.</span><span class="sxs-lookup"><span data-stu-id="c5842-122">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="c5842-123">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="c5842-123">get_HasCurrentHeader</span></span> 

<span data-ttu-id="c5842-124">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="c5842-124">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="c5842-125">[get_HasCurrentHeader](#get_hascurrentheader)público HRESULT (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="c5842-125">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="c5842-126">Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.</span><span class="sxs-lookup"><span data-stu-id="c5842-126">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="c5842-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="c5842-127">MoveNext</span></span> 

<span data-ttu-id="c5842-128">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="c5842-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="c5842-129">Public HRESULT [MoveNext](#movenext)(bool \* HasNext)</span><span class="sxs-lookup"><span data-stu-id="c5842-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="c5842-130">O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5842-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="c5842-131">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="c5842-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

