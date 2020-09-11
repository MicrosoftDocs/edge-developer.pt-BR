---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewWindowRequestedEventHandler
ms.openlocfilehash: 6b9bf26b4788819d890d54b3484ee376a3968b87
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010816"
---
# <span data-ttu-id="c1423-104">0.9.579-ICoreWebView2NewWindowRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="c1423-104">0.9.579 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c1423-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="c1423-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="c1423-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c1423-106">Summary</span></span>

 <span data-ttu-id="c1423-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c1423-107">Members</span></span>                        | <span data-ttu-id="c1423-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c1423-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1423-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="c1423-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c1423-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c1423-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c1423-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c1423-111">Members</span></span>

#### <span data-ttu-id="c1423-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="c1423-112">Invoke</span></span> 

<span data-ttu-id="c1423-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="c1423-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c1423-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c1423-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

