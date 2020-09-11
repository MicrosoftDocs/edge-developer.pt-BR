---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: 0477f9868dc472cab71dad4b10ff85fa034515a1
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011610"
---
# <span data-ttu-id="96c57-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="96c57-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="96c57-105">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="96c57-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="96c57-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="96c57-106">Summary</span></span>

 <span data-ttu-id="96c57-107">Parte</span><span class="sxs-lookup"><span data-stu-id="96c57-107">Members</span></span>                        | <span data-ttu-id="96c57-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="96c57-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="96c57-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="96c57-109">Invoke</span></span>](#invoke) | <span data-ttu-id="96c57-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="96c57-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="96c57-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="96c57-111">There are no event args for this event.</span></span>

## <span data-ttu-id="96c57-112">Parte</span><span class="sxs-lookup"><span data-stu-id="96c57-112">Members</span></span>

#### <span data-ttu-id="96c57-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="96c57-113">Invoke</span></span> 

<span data-ttu-id="96c57-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="96c57-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="96c57-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="96c57-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="96c57-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="96c57-116">There are no event args and the args parameter will be null.</span></span>

