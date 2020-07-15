---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879909"
---
# <span data-ttu-id="4e1cd-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4e1cd-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4e1cd-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="4e1cd-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4e1cd-106">Summary</span></span>

 <span data-ttu-id="4e1cd-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4e1cd-107">Members</span></span>                        | <span data-ttu-id="4e1cd-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4e1cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4e1cd-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="4e1cd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4e1cd-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="4e1cd-111">Parte</span><span class="sxs-lookup"><span data-stu-id="4e1cd-111">Members</span></span>

#### <span data-ttu-id="4e1cd-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="4e1cd-112">Invoke</span></span> 

<span data-ttu-id="4e1cd-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="4e1cd-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4e1cd-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

