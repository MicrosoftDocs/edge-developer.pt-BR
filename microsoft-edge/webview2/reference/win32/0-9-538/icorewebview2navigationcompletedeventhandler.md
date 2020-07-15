---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 24651585298998eaa42b2be242785de1bf4d6f84
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879790"
---
# <span data-ttu-id="3153c-104">interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3153c-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="3153c-105">O chamador implementa essa interface para receber o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="3153c-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="3153c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="3153c-106">Summary</span></span>

 <span data-ttu-id="3153c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="3153c-107">Members</span></span>                        | <span data-ttu-id="3153c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="3153c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3153c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="3153c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3153c-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3153c-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3153c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="3153c-111">Members</span></span>

#### <span data-ttu-id="3153c-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="3153c-112">Invoke</span></span> 

<span data-ttu-id="3153c-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="3153c-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3153c-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3153c-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>

