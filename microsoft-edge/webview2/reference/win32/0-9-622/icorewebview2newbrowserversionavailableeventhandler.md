---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 5221a08f8da8e0b51bb873a2e312e4012c868528
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011564"
---
# <span data-ttu-id="b300d-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="b300d-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="b300d-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="b300d-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="b300d-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b300d-106">Summary</span></span>

 <span data-ttu-id="b300d-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b300d-107">Members</span></span>                        | <span data-ttu-id="b300d-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b300d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b300d-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b300d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b300d-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b300d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b300d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b300d-111">Members</span></span>

#### <span data-ttu-id="b300d-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="b300d-112">Invoke</span></span> 

<span data-ttu-id="b300d-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b300d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b300d-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b300d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

