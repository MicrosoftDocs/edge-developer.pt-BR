---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 6b5cf77e8091d79b582907b4cbfe7c9aa415de9c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879062"
---
# <span data-ttu-id="8420a-104">0.8.355-IWebView2AcceleratorKeyPressedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="8420a-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8420a-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="8420a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="8420a-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8420a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="8420a-107">O chamador implementa essa interface para receber o evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="8420a-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="8420a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8420a-108">Summary</span></span>

 <span data-ttu-id="8420a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8420a-109">Members</span></span>                        | <span data-ttu-id="8420a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8420a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8420a-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="8420a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8420a-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8420a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8420a-113">Parte</span><span class="sxs-lookup"><span data-stu-id="8420a-113">Members</span></span>

#### <span data-ttu-id="8420a-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="8420a-114">Invoke</span></span> 

<span data-ttu-id="8420a-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8420a-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8420a-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8420a-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

