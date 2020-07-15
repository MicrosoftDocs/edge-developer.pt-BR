---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 70e9ad7782fe495ffd366664ecb132edd0c57df5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878649"
---
# <span data-ttu-id="0d751-104">0.8.355-IWebView2ContainsFullScreenElementChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="0d751-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0d751-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0d751-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0d751-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="0d751-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0d751-107">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="0d751-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="0d751-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="0d751-108">Summary</span></span>

 <span data-ttu-id="0d751-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0d751-109">Members</span></span>                        | <span data-ttu-id="0d751-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="0d751-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0d751-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="0d751-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0d751-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d751-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="0d751-113">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="0d751-113">There are no event args for this event.</span></span>

## <span data-ttu-id="0d751-114">Parte</span><span class="sxs-lookup"><span data-stu-id="0d751-114">Members</span></span>

#### <span data-ttu-id="0d751-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="0d751-115">Invoke</span></span> 

<span data-ttu-id="0d751-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="0d751-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0d751-117">[chamada](#invoke)a Public HRESULT ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0d751-117">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="0d751-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="0d751-118">There are no event args and the args parameter will be null.</span></span>

