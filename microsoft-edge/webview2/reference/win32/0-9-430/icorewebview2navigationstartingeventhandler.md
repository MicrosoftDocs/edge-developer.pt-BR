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
ms.openlocfilehash: ce6673f8cf188ba4f1d6d9b4dc847464a7e39f61
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652721"
---
# <span data-ttu-id="b031c-104">interface ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="b031c-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b031c-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b031c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b031c-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b031c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="b031c-107">O chamador implementa essa interface para receber o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="b031c-107">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="b031c-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b031c-108">Summary</span></span>

 <span data-ttu-id="b031c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b031c-109">Members</span></span>                        | <span data-ttu-id="b031c-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b031c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b031c-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="b031c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b031c-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b031c-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b031c-113">Parte</span><span class="sxs-lookup"><span data-stu-id="b031c-113">Members</span></span>

#### <span data-ttu-id="b031c-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="b031c-114">Invoke</span></span> 

<span data-ttu-id="b031c-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b031c-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b031c-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b031c-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span></span>

