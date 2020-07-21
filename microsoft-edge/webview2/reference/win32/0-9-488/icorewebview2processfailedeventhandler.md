---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 6b7d48fbec0c3bb0008f0f429bf6414ed855a09f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884789"
---
# <span data-ttu-id="763bb-104">0.9.515-ICoreWebView2ProcessFailedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="763bb-104">0.9.515 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="763bb-105">O chamador implementa essa interface para receber eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="763bb-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="763bb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="763bb-106">Summary</span></span>

 <span data-ttu-id="763bb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="763bb-107">Members</span></span>                        | <span data-ttu-id="763bb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="763bb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="763bb-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="763bb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="763bb-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="763bb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="763bb-111">Parte</span><span class="sxs-lookup"><span data-stu-id="763bb-111">Members</span></span>

#### <span data-ttu-id="763bb-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="763bb-112">Invoke</span></span> 

<span data-ttu-id="763bb-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="763bb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="763bb-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="763bb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>

