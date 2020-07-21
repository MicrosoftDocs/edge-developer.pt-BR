---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: f566cb8aa876304d17e11bb47f24692aefda3b26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883753"
---
# <span data-ttu-id="50e60-104">0.9.430-ICoreWebView2WebMessageReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="50e60-104">0.9.430 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="50e60-105">O chamador implementa essa interface para receber o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="50e60-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="50e60-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="50e60-106">Summary</span></span>

 <span data-ttu-id="50e60-107">Parte</span><span class="sxs-lookup"><span data-stu-id="50e60-107">Members</span></span>                        | <span data-ttu-id="50e60-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="50e60-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="50e60-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="50e60-109">Invoke</span></span>](#invoke) | <span data-ttu-id="50e60-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="50e60-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="50e60-111">Parte</span><span class="sxs-lookup"><span data-stu-id="50e60-111">Members</span></span>

#### <span data-ttu-id="50e60-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="50e60-112">Invoke</span></span> 

<span data-ttu-id="50e60-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="50e60-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="50e60-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="50e60-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

