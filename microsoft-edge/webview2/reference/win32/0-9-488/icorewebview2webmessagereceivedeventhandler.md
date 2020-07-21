---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b69854163a45c09d605cac2f544866d58546c71b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885181"
---
# <span data-ttu-id="1785d-104">0.9.515-ICoreWebView2WebMessageReceivedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="1785d-104">0.9.515 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="1785d-105">O chamador implementa essa interface para receber o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="1785d-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="1785d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1785d-106">Summary</span></span>

 <span data-ttu-id="1785d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1785d-107">Members</span></span>                        | <span data-ttu-id="1785d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1785d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1785d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="1785d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1785d-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="1785d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="1785d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1785d-111">Members</span></span>

#### <span data-ttu-id="1785d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="1785d-112">Invoke</span></span> 

<span data-ttu-id="1785d-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="1785d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1785d-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="1785d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

