---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e24db15aba667f1002c95ed84ead63d812284586
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652366"
---
# <span data-ttu-id="3f883-104">interface IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3f883-104">interface IWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3f883-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3f883-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3f883-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="3f883-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="3f883-107">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="3f883-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="3f883-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="3f883-108">Summary</span></span>

 <span data-ttu-id="3f883-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3f883-109">Members</span></span>                        | <span data-ttu-id="3f883-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="3f883-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f883-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="3f883-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3f883-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3f883-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3f883-113">Parte</span><span class="sxs-lookup"><span data-stu-id="3f883-113">Members</span></span>

#### <span data-ttu-id="3f883-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="3f883-114">Invoke</span></span> 

<span data-ttu-id="3f883-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3f883-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3f883-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3f883-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

