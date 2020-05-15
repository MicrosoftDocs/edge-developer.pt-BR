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
ms.openlocfilehash: b59eae6966efb6c2ebfc018be5ec0a5d2d5334c7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652381"
---
# <span data-ttu-id="99783-104">interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="99783-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="99783-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="99783-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="99783-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="99783-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="99783-107">O chamador implementa essa interface para receber o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="99783-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="99783-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="99783-108">Summary</span></span>

 <span data-ttu-id="99783-109">Parte</span><span class="sxs-lookup"><span data-stu-id="99783-109">Members</span></span>                        | <span data-ttu-id="99783-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="99783-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99783-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="99783-111">Invoke</span></span>](#invoke) | <span data-ttu-id="99783-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="99783-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="99783-113">Parte</span><span class="sxs-lookup"><span data-stu-id="99783-113">Members</span></span>

#### <span data-ttu-id="99783-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="99783-114">Invoke</span></span> 

<span data-ttu-id="99783-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="99783-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="99783-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="99783-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

