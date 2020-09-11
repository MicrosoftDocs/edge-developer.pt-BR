---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: 7e02fb9480f70dbffe6d33cfd7fb436c26c97da3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011360"
---
# <span data-ttu-id="2b3f3-104">0.9.579-ICoreWebView2FocusChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="2b3f3-104">0.9.579 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2b3f3-105">O chamador implementa esse método para receber os eventos GotFocus e LostFocus.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="2b3f3-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="2b3f3-106">Summary</span></span>

 <span data-ttu-id="2b3f3-107">Parte</span><span class="sxs-lookup"><span data-stu-id="2b3f3-107">Members</span></span>                        | <span data-ttu-id="2b3f3-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="2b3f3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2b3f3-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="2b3f3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2b3f3-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2b3f3-111">Não há argumentos de evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-111">There are no event args for this event.</span></span>

## <span data-ttu-id="2b3f3-112">Parte</span><span class="sxs-lookup"><span data-stu-id="2b3f3-112">Members</span></span>

#### <span data-ttu-id="2b3f3-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="2b3f3-113">Invoke</span></span> 

<span data-ttu-id="2b3f3-114">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2b3f3-115">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2b3f3-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="2b3f3-116">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="2b3f3-116">There are no event args and the args parameter will be null.</span></span>

