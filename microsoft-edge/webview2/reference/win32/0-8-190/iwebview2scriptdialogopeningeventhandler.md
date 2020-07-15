---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 70f1708d7cc908a761e96d14f25e0f1751d1923d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878215"
---
# <span data-ttu-id="a5866-104">0.8.355-IWebView2ScriptDialogOpeningEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="a5866-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a5866-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a5866-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a5866-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="a5866-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="a5866-107">O chamador implementa essa interface para receber o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="a5866-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="a5866-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="a5866-108">Summary</span></span>

 <span data-ttu-id="a5866-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a5866-109">Members</span></span>                        | <span data-ttu-id="a5866-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="a5866-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5866-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="a5866-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a5866-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a5866-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a5866-113">Parte</span><span class="sxs-lookup"><span data-stu-id="a5866-113">Members</span></span>

#### <span data-ttu-id="a5866-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="a5866-114">Invoke</span></span> 

<span data-ttu-id="a5866-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a5866-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a5866-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a5866-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

