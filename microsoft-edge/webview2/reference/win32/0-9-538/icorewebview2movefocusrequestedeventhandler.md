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
ms.openlocfilehash: a90e7d3479f93d58d72db5c69cca53669a6d4501
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698273"
---
# <span data-ttu-id="19e7d-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="19e7d-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="19e7d-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="19e7d-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="19e7d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="19e7d-106">Summary</span></span>

 <span data-ttu-id="19e7d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="19e7d-107">Members</span></span>                        | <span data-ttu-id="19e7d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="19e7d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19e7d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="19e7d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="19e7d-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="19e7d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="19e7d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="19e7d-111">Members</span></span>

#### <span data-ttu-id="19e7d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="19e7d-112">Invoke</span></span> 

<span data-ttu-id="19e7d-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="19e7d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="19e7d-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="19e7d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

