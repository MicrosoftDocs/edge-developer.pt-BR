---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewWindowRequestedEventHandler
ms.openlocfilehash: 61782812565de1d9a958e4bd3838d39519ad25e9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879552"
---
# <span data-ttu-id="3253a-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3253a-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="3253a-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="3253a-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="3253a-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3253a-106">Summary</span></span>

 <span data-ttu-id="3253a-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3253a-107">Members</span></span>                        | <span data-ttu-id="3253a-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3253a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3253a-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3253a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3253a-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3253a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3253a-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3253a-111">Members</span></span>

#### <span data-ttu-id="3253a-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="3253a-112">Invoke</span></span> 

<span data-ttu-id="3253a-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3253a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3253a-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3253a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

