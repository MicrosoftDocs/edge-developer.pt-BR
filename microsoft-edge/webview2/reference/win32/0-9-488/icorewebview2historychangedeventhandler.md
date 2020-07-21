---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: d90f461f6c2a1e573b0514213ec34f83f0d23366
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885491"
---
# <span data-ttu-id="47e21-104">0.9.515-ICoreWebView2HistoryChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="47e21-104">0.9.515 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="47e21-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="47e21-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="47e21-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="47e21-106">Summary</span></span>

 <span data-ttu-id="47e21-107">Parte</span><span class="sxs-lookup"><span data-stu-id="47e21-107">Members</span></span>                        | <span data-ttu-id="47e21-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="47e21-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47e21-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="47e21-109">Invoke</span></span>](#invoke) | <span data-ttu-id="47e21-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="47e21-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="47e21-111">Parte</span><span class="sxs-lookup"><span data-stu-id="47e21-111">Members</span></span>

#### <span data-ttu-id="47e21-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="47e21-112">Invoke</span></span> 

<span data-ttu-id="47e21-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="47e21-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="47e21-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="47e21-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

