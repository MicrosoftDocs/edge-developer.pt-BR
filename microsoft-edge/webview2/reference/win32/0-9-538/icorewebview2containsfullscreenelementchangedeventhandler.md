---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: 0f0efc8cc5315c35bef4c0ad122be37f26444f8d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877424"
---
# <span data-ttu-id="e9b60-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9b60-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e9b60-105">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="e9b60-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="e9b60-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="e9b60-106">Summary</span></span>

 <span data-ttu-id="e9b60-107">Parte</span><span class="sxs-lookup"><span data-stu-id="e9b60-107">Members</span></span>                        | <span data-ttu-id="e9b60-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="e9b60-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e9b60-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="e9b60-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e9b60-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="e9b60-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e9b60-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="e9b60-111">There are no event args for this event.</span></span>

## <span data-ttu-id="e9b60-112">Parte</span><span class="sxs-lookup"><span data-stu-id="e9b60-112">Members</span></span>

#### <span data-ttu-id="e9b60-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="e9b60-113">Invoke</span></span> 

<span data-ttu-id="e9b60-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="e9b60-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e9b60-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e9b60-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e9b60-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="e9b60-116">There are no event args and the args parameter will be null.</span></span>

