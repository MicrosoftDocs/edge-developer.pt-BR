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
ms.openlocfilehash: c8444741480ba3b07d2755dcac0ec11f7194a783
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698393"
---
# <span data-ttu-id="47c8a-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="47c8a-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="47c8a-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="47c8a-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="47c8a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="47c8a-106">Summary</span></span>

 <span data-ttu-id="47c8a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="47c8a-107">Members</span></span>                        | <span data-ttu-id="47c8a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="47c8a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47c8a-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="47c8a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="47c8a-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="47c8a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="47c8a-111">Parte</span><span class="sxs-lookup"><span data-stu-id="47c8a-111">Members</span></span>

#### <span data-ttu-id="47c8a-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="47c8a-112">Invoke</span></span> 

<span data-ttu-id="47c8a-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="47c8a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="47c8a-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="47c8a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

