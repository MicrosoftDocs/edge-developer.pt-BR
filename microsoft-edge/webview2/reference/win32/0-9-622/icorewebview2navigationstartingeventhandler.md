---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: ab4181d8a334ae4263665d964448f67cca965ff5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011565"
---
# <span data-ttu-id="55854-104">interface ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="55854-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="55854-105">O chamador implementa essa interface para receber o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="55854-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="55854-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="55854-106">Summary</span></span>

 <span data-ttu-id="55854-107">Parte</span><span class="sxs-lookup"><span data-stu-id="55854-107">Members</span></span>                        | <span data-ttu-id="55854-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="55854-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="55854-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="55854-109">Invoke</span></span>](#invoke) | <span data-ttu-id="55854-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="55854-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="55854-111">Parte</span><span class="sxs-lookup"><span data-stu-id="55854-111">Members</span></span>

#### <span data-ttu-id="55854-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="55854-112">Invoke</span></span> 

<span data-ttu-id="55854-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="55854-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="55854-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="55854-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

