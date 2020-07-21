---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 41687dcb162d8d56e773b9050898e9f22bd034ab
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883879"
---
# <span data-ttu-id="de4b4-104">0.9.515-ICoreWebView2ContainsFullScreenElementChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="de4b4-104">0.9.515 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="de4b4-105">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="de4b4-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="de4b4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="de4b4-106">Summary</span></span>

 <span data-ttu-id="de4b4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="de4b4-107">Members</span></span>                        | <span data-ttu-id="de4b4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="de4b4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="de4b4-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="de4b4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="de4b4-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="de4b4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="de4b4-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="de4b4-111">There are no event args for this event.</span></span>

## <span data-ttu-id="de4b4-112">Parte</span><span class="sxs-lookup"><span data-stu-id="de4b4-112">Members</span></span>

#### <span data-ttu-id="de4b4-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="de4b4-113">Invoke</span></span> 

<span data-ttu-id="de4b4-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="de4b4-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="de4b4-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="de4b4-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="de4b4-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="de4b4-116">There are no event args and the args parameter will be null.</span></span>

