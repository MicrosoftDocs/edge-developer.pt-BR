---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: d50f84edeb532d90a1268f553b38e4cbf256556a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884082"
---
# <span data-ttu-id="5e18c-104">0.9.430-ICoreWebView2MoveFocusRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="5e18c-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="5e18c-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="5e18c-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="5e18c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5e18c-106">Summary</span></span>

 <span data-ttu-id="5e18c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5e18c-107">Members</span></span>                        | <span data-ttu-id="5e18c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5e18c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5e18c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="5e18c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5e18c-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e18c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5e18c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5e18c-111">Members</span></span>

#### <span data-ttu-id="5e18c-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="5e18c-112">Invoke</span></span> 

<span data-ttu-id="5e18c-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="5e18c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5e18c-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5e18c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

