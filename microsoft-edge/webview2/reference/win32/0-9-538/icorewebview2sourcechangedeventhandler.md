---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: 9c5054c296657d851f0a88773d5eb96cba2af64a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010443"
---
# <span data-ttu-id="896c8-104">0.9.579-ICoreWebView2SourceChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="896c8-104">0.9.579 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="896c8-105">O chamador implementa essa interface para receber o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="896c8-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="896c8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="896c8-106">Summary</span></span>

 <span data-ttu-id="896c8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="896c8-107">Members</span></span>                        | <span data-ttu-id="896c8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="896c8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="896c8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="896c8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="896c8-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="896c8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="896c8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="896c8-111">Members</span></span>

#### <span data-ttu-id="896c8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="896c8-112">Invoke</span></span> 

<span data-ttu-id="896c8-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="896c8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="896c8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="896c8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

