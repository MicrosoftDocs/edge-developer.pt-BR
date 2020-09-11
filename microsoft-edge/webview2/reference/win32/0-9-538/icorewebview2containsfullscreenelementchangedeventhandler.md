---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: e1c51ee30a7b61d5a5638adb4130b1add3bddb23
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010555"
---
# <span data-ttu-id="ea26f-104">0.9.579-ICoreWebView2ContainsFullScreenElementChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="ea26f-104">0.9.579 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ea26f-105">O chamador implementa esse método para receber os eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="ea26f-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="ea26f-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ea26f-106">Summary</span></span>

 <span data-ttu-id="ea26f-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ea26f-107">Members</span></span>                        | <span data-ttu-id="ea26f-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ea26f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea26f-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ea26f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ea26f-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea26f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ea26f-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="ea26f-111">There are no event args for this event.</span></span>

## <span data-ttu-id="ea26f-112">Parte</span><span class="sxs-lookup"><span data-stu-id="ea26f-112">Members</span></span>

#### <span data-ttu-id="ea26f-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="ea26f-113">Invoke</span></span> 

<span data-ttu-id="ea26f-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea26f-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ea26f-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ea26f-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ea26f-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="ea26f-116">There are no event args and the args parameter will be null.</span></span>

