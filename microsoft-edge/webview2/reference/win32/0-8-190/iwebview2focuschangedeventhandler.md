---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 44e24ef8e0e4b41968835ff7cd70fd9904482c6c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878446"
---
# <span data-ttu-id="aaf3b-104">0.8.355-IWebView2FocusChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="aaf3b-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="aaf3b-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="aaf3b-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="aaf3b-107">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="aaf3b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="aaf3b-108">Summary</span></span>

 <span data-ttu-id="aaf3b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="aaf3b-109">Members</span></span>                        | <span data-ttu-id="aaf3b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="aaf3b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aaf3b-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="aaf3b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="aaf3b-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="aaf3b-113">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-113">There are no event args for this event.</span></span>

## <span data-ttu-id="aaf3b-114">Parte</span><span class="sxs-lookup"><span data-stu-id="aaf3b-114">Members</span></span>

#### <span data-ttu-id="aaf3b-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="aaf3b-115">Invoke</span></span> 

<span data-ttu-id="aaf3b-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="aaf3b-117">[chamada](#invoke)a Public HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="aaf3b-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="aaf3b-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="aaf3b-118">There are no event args and the args parameter will be null.</span></span>

