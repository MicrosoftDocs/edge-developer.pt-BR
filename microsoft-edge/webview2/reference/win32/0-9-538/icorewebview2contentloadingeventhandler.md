---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: fb6e3cfabae0116ac746d6e8e5cc03efa0f1c1b6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877444"
---
# <span data-ttu-id="638fe-104">interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="638fe-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="638fe-105">O chamador implementa essa interface para receber o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="638fe-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="638fe-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="638fe-106">Summary</span></span>

 <span data-ttu-id="638fe-107">Parte</span><span class="sxs-lookup"><span data-stu-id="638fe-107">Members</span></span>                        | <span data-ttu-id="638fe-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="638fe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="638fe-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="638fe-109">Invoke</span></span>](#invoke) | <span data-ttu-id="638fe-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="638fe-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="638fe-111">Parte</span><span class="sxs-lookup"><span data-stu-id="638fe-111">Members</span></span>

#### <span data-ttu-id="638fe-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="638fe-112">Invoke</span></span> 

<span data-ttu-id="638fe-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="638fe-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="638fe-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="638fe-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

