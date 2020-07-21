---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 04859c0a22e8571a4fe8015a089c9b7d708c1dd3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884868"
---
# <span data-ttu-id="5ba12-104">0.9.430-ICoreWebView2NewBrowserVersionAvailableEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="5ba12-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="5ba12-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="5ba12-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="5ba12-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5ba12-106">Summary</span></span>

 <span data-ttu-id="5ba12-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5ba12-107">Members</span></span>                        | <span data-ttu-id="5ba12-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5ba12-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5ba12-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="5ba12-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5ba12-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="5ba12-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5ba12-111">Use o método get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) para obter o novo número de versão.</span><span class="sxs-lookup"><span data-stu-id="5ba12-111">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="5ba12-112">Parte</span><span class="sxs-lookup"><span data-stu-id="5ba12-112">Members</span></span>

#### <span data-ttu-id="5ba12-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="5ba12-113">Invoke</span></span> 

<span data-ttu-id="5ba12-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="5ba12-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5ba12-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5ba12-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

