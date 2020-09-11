---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 68cecdec63e64bde978156f17d6755a483abcc66
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011339"
---
# <span data-ttu-id="cefaf-104">0.9.579-ICoreWebView2HistoryChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="cefaf-104">0.9.579 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="cefaf-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="cefaf-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="cefaf-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="cefaf-106">Summary</span></span>

 <span data-ttu-id="cefaf-107">Parte</span><span class="sxs-lookup"><span data-stu-id="cefaf-107">Members</span></span>                        | <span data-ttu-id="cefaf-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="cefaf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cefaf-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="cefaf-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cefaf-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="cefaf-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="cefaf-111">Parte</span><span class="sxs-lookup"><span data-stu-id="cefaf-111">Members</span></span>

#### <span data-ttu-id="cefaf-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="cefaf-112">Invoke</span></span> 

<span data-ttu-id="cefaf-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="cefaf-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="cefaf-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="cefaf-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

