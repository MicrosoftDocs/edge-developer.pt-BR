---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 400053b557a8b6d997be74f0aed5bfafe717d2df
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884866"
---
# <span data-ttu-id="16f15-104">0.9.430-ICoreWebView2NavigationStartingEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="16f15-104">0.9.430 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="16f15-105">O chamador implementa essa interface para receber o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="16f15-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="16f15-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="16f15-106">Summary</span></span>

 <span data-ttu-id="16f15-107">Parte</span><span class="sxs-lookup"><span data-stu-id="16f15-107">Members</span></span>                        | <span data-ttu-id="16f15-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="16f15-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16f15-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="16f15-109">Invoke</span></span>](#invoke) | <span data-ttu-id="16f15-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="16f15-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="16f15-111">Parte</span><span class="sxs-lookup"><span data-stu-id="16f15-111">Members</span></span>

#### <span data-ttu-id="16f15-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="16f15-112">Invoke</span></span> 

<span data-ttu-id="16f15-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="16f15-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="16f15-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="16f15-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationStartingEventArgs](ICoreWebView2NavigationStartingEventArgs.md) \* args)</span></span>

