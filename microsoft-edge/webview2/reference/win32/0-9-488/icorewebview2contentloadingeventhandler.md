---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 53410d7592f6a217ffd72e410d46491c78262f87
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883865"
---
# <span data-ttu-id="a1219-104">0.9.515-ICoreWebView2ContentLoadingEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="a1219-104">0.9.515 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="a1219-105">O chamador implementa essa interface para receber o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a1219-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="a1219-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="a1219-106">Summary</span></span>

 <span data-ttu-id="a1219-107">Parte</span><span class="sxs-lookup"><span data-stu-id="a1219-107">Members</span></span>                        | <span data-ttu-id="a1219-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="a1219-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1219-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="a1219-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a1219-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a1219-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a1219-111">Parte</span><span class="sxs-lookup"><span data-stu-id="a1219-111">Members</span></span>

#### <span data-ttu-id="a1219-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="a1219-112">Invoke</span></span> 

<span data-ttu-id="a1219-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="a1219-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a1219-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a1219-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

