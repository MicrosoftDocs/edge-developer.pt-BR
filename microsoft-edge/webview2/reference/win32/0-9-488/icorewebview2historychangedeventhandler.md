---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 42e3767ad2a42a1d9e9931efa8a4fe844ea80dba
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652402"
---
# <span data-ttu-id="1504b-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1504b-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1504b-105">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="1504b-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="1504b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1504b-106">Summary</span></span>

 <span data-ttu-id="1504b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1504b-107">Members</span></span>                        | <span data-ttu-id="1504b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1504b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1504b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="1504b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1504b-110">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="1504b-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="1504b-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1504b-111">Members</span></span>

#### <span data-ttu-id="1504b-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="1504b-112">Invoke</span></span> 

<span data-ttu-id="1504b-113">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="1504b-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="1504b-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1504b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

