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
ms.openlocfilehash: 7c5aece49cf2a3e8e6a65eba3fbb4d46f0ff2997
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652522"
---
# <span data-ttu-id="9a781-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9a781-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9a781-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9a781-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9a781-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="9a781-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9a781-107">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="9a781-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="9a781-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9a781-108">Summary</span></span>

 <span data-ttu-id="9a781-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9a781-109">Members</span></span>                        | <span data-ttu-id="9a781-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9a781-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9a781-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="9a781-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9a781-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="9a781-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9a781-113">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9a781-113">There are no event args for this event.</span></span>

## <span data-ttu-id="9a781-114">Parte</span><span class="sxs-lookup"><span data-stu-id="9a781-114">Members</span></span>

#### <span data-ttu-id="9a781-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="9a781-115">Invoke</span></span> 

<span data-ttu-id="9a781-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="9a781-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9a781-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9a781-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="9a781-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="9a781-118">There are no event args and the args parameter will be null.</span></span>

