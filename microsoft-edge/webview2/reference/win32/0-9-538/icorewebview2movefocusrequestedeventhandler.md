---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: b0e7f3f005b90c5656eeeac09716130544b0ee20
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879832"
---
# <span data-ttu-id="b37fe-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b37fe-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b37fe-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="b37fe-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="b37fe-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b37fe-106">Summary</span></span>

 <span data-ttu-id="b37fe-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b37fe-107">Members</span></span>                        | <span data-ttu-id="b37fe-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b37fe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b37fe-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b37fe-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b37fe-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b37fe-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b37fe-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b37fe-111">Members</span></span>

#### <span data-ttu-id="b37fe-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="b37fe-112">Invoke</span></span> 

<span data-ttu-id="b37fe-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b37fe-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b37fe-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b37fe-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

