---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 20b9fe69f4aa02f2ec96082ec995bb5c1c4b218e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881037"
---
# <span data-ttu-id="bd8cf-104">0.9.430-ICoreWebView2FocusChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="bd8cf-104">0.9.430 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="bd8cf-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="bd8cf-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="bd8cf-107">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="bd8cf-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="bd8cf-108">Summary</span></span>

 <span data-ttu-id="bd8cf-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bd8cf-109">Members</span></span>                        | <span data-ttu-id="bd8cf-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="bd8cf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd8cf-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="bd8cf-111">Invoke</span></span>](#invoke) | <span data-ttu-id="bd8cf-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="bd8cf-113">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-113">There are no event args for this event.</span></span>

## <span data-ttu-id="bd8cf-114">Parte</span><span class="sxs-lookup"><span data-stu-id="bd8cf-114">Members</span></span>

#### <span data-ttu-id="bd8cf-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="bd8cf-115">Invoke</span></span> 

<span data-ttu-id="bd8cf-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bd8cf-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="bd8cf-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="bd8cf-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="bd8cf-118">There are no event args and the args parameter will be null.</span></span>

