---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 909b055af0f9594bb3c85b215cb8e02f13606aa0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011528"
---
# <span data-ttu-id="1a7fc-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1a7fc-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1a7fc-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="1a7fc-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1a7fc-106">Summary</span></span>

 <span data-ttu-id="1a7fc-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1a7fc-107">Members</span></span>                        | <span data-ttu-id="1a7fc-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1a7fc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1a7fc-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="1a7fc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1a7fc-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="1a7fc-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1a7fc-111">Members</span></span>

#### <span data-ttu-id="1a7fc-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="1a7fc-112">Invoke</span></span> 

<span data-ttu-id="1a7fc-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="1a7fc-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="1a7fc-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1a7fc-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

