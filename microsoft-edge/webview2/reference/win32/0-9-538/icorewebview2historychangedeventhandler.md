---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 0f14f8d281d4729d797eb5271a19cff67becafab
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698331"
---
# <span data-ttu-id="4ab12-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4ab12-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4ab12-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="4ab12-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="4ab12-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4ab12-106">Summary</span></span>

 <span data-ttu-id="4ab12-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4ab12-107">Members</span></span>                        | <span data-ttu-id="4ab12-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4ab12-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4ab12-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="4ab12-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4ab12-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="4ab12-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="4ab12-111">Parte</span><span class="sxs-lookup"><span data-stu-id="4ab12-111">Members</span></span>

#### <span data-ttu-id="4ab12-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="4ab12-112">Invoke</span></span> 

<span data-ttu-id="4ab12-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="4ab12-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="4ab12-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4ab12-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

