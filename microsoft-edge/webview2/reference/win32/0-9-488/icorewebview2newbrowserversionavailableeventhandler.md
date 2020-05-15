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
ms.openlocfilehash: 9196f2d9503efbaf9f15b43e7e6d7e80c2de00f7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652606"
---
# <span data-ttu-id="582a8-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="582a8-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="582a8-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="582a8-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="582a8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="582a8-106">Summary</span></span>

 <span data-ttu-id="582a8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="582a8-107">Members</span></span>                        | <span data-ttu-id="582a8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="582a8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="582a8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="582a8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="582a8-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="582a8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="582a8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="582a8-111">Members</span></span>

#### <span data-ttu-id="582a8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="582a8-112">Invoke</span></span> 

<span data-ttu-id="582a8-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="582a8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="582a8-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="582a8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

