---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 85de243c00364f7fb57d3842b2ddbf78848905f6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652681"
---
# <span data-ttu-id="cc648-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="cc648-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="cc648-105">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="cc648-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="cc648-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="cc648-106">Summary</span></span>

 <span data-ttu-id="cc648-107">Parte</span><span class="sxs-lookup"><span data-stu-id="cc648-107">Members</span></span>                        | <span data-ttu-id="cc648-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="cc648-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cc648-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="cc648-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cc648-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="cc648-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="cc648-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="cc648-111">There are no event args for this event.</span></span>

## <span data-ttu-id="cc648-112">Parte</span><span class="sxs-lookup"><span data-stu-id="cc648-112">Members</span></span>

#### <span data-ttu-id="cc648-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="cc648-113">Invoke</span></span> 

<span data-ttu-id="cc648-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="cc648-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="cc648-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="cc648-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="cc648-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="cc648-116">There are no event args and the args parameter will be null.</span></span>

