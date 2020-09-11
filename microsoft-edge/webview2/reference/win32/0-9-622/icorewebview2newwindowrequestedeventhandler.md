---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewWindowRequestedEventHandler
ms.openlocfilehash: 99fb8261e6ed170b09bc87f9a1372e0e2cc53954
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011587"
---
# <span data-ttu-id="abab9-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="abab9-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="abab9-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="abab9-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="abab9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="abab9-106">Summary</span></span>

 <span data-ttu-id="abab9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="abab9-107">Members</span></span>                        | <span data-ttu-id="abab9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="abab9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="abab9-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="abab9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="abab9-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="abab9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="abab9-111">Parte</span><span class="sxs-lookup"><span data-stu-id="abab9-111">Members</span></span>

#### <span data-ttu-id="abab9-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="abab9-112">Invoke</span></span> 

<span data-ttu-id="abab9-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="abab9-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="abab9-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="abab9-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

