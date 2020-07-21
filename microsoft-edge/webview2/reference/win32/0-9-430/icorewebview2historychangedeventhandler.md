---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: e47ca26475ba1b59fa4ea8c87a7aada0d8d6695f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884131"
---
# <span data-ttu-id="9a23c-104">0.9.430-ICoreWebView2HistoryChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="9a23c-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9a23c-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="9a23c-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="9a23c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="9a23c-106">Summary</span></span>

 <span data-ttu-id="9a23c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="9a23c-107">Members</span></span>                        | <span data-ttu-id="9a23c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="9a23c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9a23c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="9a23c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9a23c-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="9a23c-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="9a23c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="9a23c-111">Members</span></span>

#### <span data-ttu-id="9a23c-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="9a23c-112">Invoke</span></span> 

<span data-ttu-id="9a23c-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="9a23c-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="9a23c-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9a23c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>

