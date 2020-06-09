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
ms.openlocfilehash: 0305517d17bfa812dbaee9b238403f2d9f1fb22d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697802"
---
# <span data-ttu-id="e44f0-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e44f0-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e44f0-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e44f0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e44f0-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e44f0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e44f0-107">O chamador implementa essa interface para receber o evento Historychanged.</span><span class="sxs-lookup"><span data-stu-id="e44f0-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="e44f0-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e44f0-108">Summary</span></span>

 <span data-ttu-id="e44f0-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e44f0-109">Members</span></span>                        | <span data-ttu-id="e44f0-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e44f0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e44f0-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="e44f0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e44f0-112">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="e44f0-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="e44f0-113">Parte</span><span class="sxs-lookup"><span data-stu-id="e44f0-113">Members</span></span>

#### <span data-ttu-id="e44f0-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="e44f0-114">Invoke</span></span> 

<span data-ttu-id="e44f0-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="e44f0-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="e44f0-116">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e44f0-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

