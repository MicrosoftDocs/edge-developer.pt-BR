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
ms.openlocfilehash: 8631b046e1de776a6059ba0cd09ed34c8c5adc26
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652367"
---
# <span data-ttu-id="94744-104">interface IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="94744-104">interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="94744-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="94744-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="94744-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="94744-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="94744-107">O chamador implementa essa interface para receber o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="94744-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="94744-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="94744-108">Summary</span></span>

 <span data-ttu-id="94744-109">Parte</span><span class="sxs-lookup"><span data-stu-id="94744-109">Members</span></span>                        | <span data-ttu-id="94744-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="94744-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="94744-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="94744-111">Invoke</span></span>](#invoke) | <span data-ttu-id="94744-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="94744-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="94744-113">Parte</span><span class="sxs-lookup"><span data-stu-id="94744-113">Members</span></span>

#### <span data-ttu-id="94744-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="94744-114">Invoke</span></span> 

<span data-ttu-id="94744-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="94744-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="94744-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="94744-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

