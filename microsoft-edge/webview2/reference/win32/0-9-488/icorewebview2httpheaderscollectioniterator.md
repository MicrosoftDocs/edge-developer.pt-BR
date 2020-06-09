---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 2f0a41c72c6ac6f7bcfbf7a5cbd5eef61ffa3a68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697263"
---
# <span data-ttu-id="67c03-104">interface ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="67c03-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="67c03-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="67c03-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="67c03-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="67c03-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="67c03-107">Iterador para uma coleção de cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="67c03-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="67c03-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="67c03-108">Summary</span></span>

 <span data-ttu-id="67c03-109">Parte</span><span class="sxs-lookup"><span data-stu-id="67c03-109">Members</span></span>                        | <span data-ttu-id="67c03-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="67c03-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67c03-111">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="67c03-111">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="67c03-112">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="67c03-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="67c03-113">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="67c03-113">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="67c03-114">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="67c03-114">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="67c03-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="67c03-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="67c03-116">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="67c03-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="67c03-117">Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) e [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="67c03-117">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="67c03-118">Parte</span><span class="sxs-lookup"><span data-stu-id="67c03-118">Members</span></span>

#### <span data-ttu-id="67c03-119">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="67c03-119">get_HasCurrentHeader</span></span> 

<span data-ttu-id="67c03-120">True quando o iterador não ficar fora dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="67c03-120">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="67c03-121">[get_HasCurrentHeader](#get_hascurrentheader)público HRESULT (bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="67c03-121">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="67c03-122">Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.</span><span class="sxs-lookup"><span data-stu-id="67c03-122">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="67c03-123">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="67c03-123">GetCurrentHeader</span></span> 

<span data-ttu-id="67c03-124">Obter o nome e o valor do cabeçalho HTTP atual do iterador.</span><span class="sxs-lookup"><span data-stu-id="67c03-124">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="67c03-125">Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR \* Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="67c03-125">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="67c03-126">Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.</span><span class="sxs-lookup"><span data-stu-id="67c03-126">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="67c03-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="67c03-127">MoveNext</span></span> 

<span data-ttu-id="67c03-128">Mover o iterador para o próximo cabeçalho HTTP na coleção.</span><span class="sxs-lookup"><span data-stu-id="67c03-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="67c03-129">Public HRESULT [MoveNext](#movenext)(bool \* HasNext)</span><span class="sxs-lookup"><span data-stu-id="67c03-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="67c03-130">O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP.</span><span class="sxs-lookup"><span data-stu-id="67c03-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="67c03-131">Após isso ocorrer, o método GetCurrentHeader falhará se chamado.</span><span class="sxs-lookup"><span data-stu-id="67c03-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

