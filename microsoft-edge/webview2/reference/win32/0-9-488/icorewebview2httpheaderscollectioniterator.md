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
# interface ICoreWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterador para uma coleção de cabeçalhos HTTP.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_HasCurrentHeader](#get_hascurrentheader) | True quando o iterador não ficar fora dos cabeçalhos.
[GetCurrentHeader](#getcurrentheader) | Obter o nome e o valor do cabeçalho HTTP atual do iterador.
[MoveNext](#movenext) | Mover o iterador para o próximo cabeçalho HTTP na coleção.

Consulte [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) e [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md). 
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

## Parte

#### get_HasCurrentHeader 

True quando o iterador não ficar fora dos cabeçalhos.

> [get_HasCurrentHeader](#get_hascurrentheader)público HRESULT (bool * hasCurrent)

Se a coleção na qual o iterador estiver sendo iterada estiver vazia ou se o iterador ultrapassar o final da coleta, isso será falso.

#### GetCurrentHeader 

Obter o nome e o valor do cabeçalho HTTP atual do iterador.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(nome LPWSTR * Name, LPWStr * Value)

Esse método irá falhar se a última chamada para MoveNext definir has_next como FALSE.

#### MoveNext 

Mover o iterador para o próximo cabeçalho HTTP na coleção.

> Public HRESULT [MoveNext](#movenext)(bool * HasNext)

O parâmetro hasNext será definido como FALSE se não houver mais cabeçalhos HTTP. Após isso ocorrer, o método GetCurrentHeader falhará se chamado.

