---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 3ff529c649eb455e8ea1b14ebbd25533631d2b99
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011558"
---
# <span data-ttu-id="93f60-104">interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="93f60-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="93f60-105">O chamador implementa essa interface para receber o evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="93f60-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="93f60-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="93f60-106">Summary</span></span>

 <span data-ttu-id="93f60-107">Parte</span><span class="sxs-lookup"><span data-stu-id="93f60-107">Members</span></span>                        | <span data-ttu-id="93f60-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="93f60-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="93f60-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="93f60-109">Invoke</span></span>](#invoke) | <span data-ttu-id="93f60-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="93f60-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="93f60-111">Parte</span><span class="sxs-lookup"><span data-stu-id="93f60-111">Members</span></span>

#### <span data-ttu-id="93f60-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="93f60-112">Invoke</span></span> 

<span data-ttu-id="93f60-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="93f60-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="93f60-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="93f60-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>

