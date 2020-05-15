---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8fd3533d8f479866989f719be6e48c437fae4ddb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652697"
---
# <span data-ttu-id="7d0ad-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7d0ad-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7d0ad-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7d0ad-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7d0ad-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="7d0ad-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7d0ad-107">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="7d0ad-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="7d0ad-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="7d0ad-108">Summary</span></span>

 <span data-ttu-id="7d0ad-109">Parte</span><span class="sxs-lookup"><span data-stu-id="7d0ad-109">Members</span></span>                        | <span data-ttu-id="7d0ad-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="7d0ad-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7d0ad-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="7d0ad-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7d0ad-112">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="7d0ad-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="7d0ad-113">Parte</span><span class="sxs-lookup"><span data-stu-id="7d0ad-113">Members</span></span>

#### <span data-ttu-id="7d0ad-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="7d0ad-114">Invoke</span></span> 

<span data-ttu-id="7d0ad-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="7d0ad-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="7d0ad-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7d0ad-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>

