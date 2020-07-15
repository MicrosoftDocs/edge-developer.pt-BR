---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 14c238a5a625e40e9abba3d786d6b80aef8f7773
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877830"
---
# <span data-ttu-id="65da5-104">0.9.430-ICoreWebView2NewWindowRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="65da5-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="65da5-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="65da5-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="65da5-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="65da5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="65da5-107">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="65da5-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="65da5-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="65da5-108">Summary</span></span>

 <span data-ttu-id="65da5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="65da5-109">Members</span></span>                        | <span data-ttu-id="65da5-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="65da5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65da5-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="65da5-111">Invoke</span></span>](#invoke) | <span data-ttu-id="65da5-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="65da5-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="65da5-113">Parte</span><span class="sxs-lookup"><span data-stu-id="65da5-113">Members</span></span>

#### <span data-ttu-id="65da5-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="65da5-114">Invoke</span></span> 

<span data-ttu-id="65da5-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="65da5-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="65da5-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2NewWindowRequestedEventArgs](ICoreWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="65da5-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NewWindowRequestedEventArgs](ICoreWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>

