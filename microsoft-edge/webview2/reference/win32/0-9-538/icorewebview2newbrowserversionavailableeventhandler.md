---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 82a5e73b8b928897e5c0af1610631c9e7d636337
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879741"
---
# <span data-ttu-id="8f2b5-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="8f2b5-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="8f2b5-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8f2b5-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="8f2b5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="8f2b5-106">Summary</span></span>

 <span data-ttu-id="8f2b5-107">Parte</span><span class="sxs-lookup"><span data-stu-id="8f2b5-107">Members</span></span>                        | <span data-ttu-id="8f2b5-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="8f2b5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8f2b5-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="8f2b5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8f2b5-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8f2b5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8f2b5-111">Parte</span><span class="sxs-lookup"><span data-stu-id="8f2b5-111">Members</span></span>

#### <span data-ttu-id="8f2b5-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="8f2b5-112">Invoke</span></span> 

<span data-ttu-id="8f2b5-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8f2b5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8f2b5-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="8f2b5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

