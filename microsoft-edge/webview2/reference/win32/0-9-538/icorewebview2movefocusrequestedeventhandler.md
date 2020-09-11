---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: bd07256203944b4d640d859451fa000cbc1fcd46
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011311"
---
# <span data-ttu-id="ba7d8-104">0.9.579-ICoreWebView2MoveFocusRequestedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="ba7d8-104">0.9.579 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ba7d8-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ba7d8-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="ba7d8-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ba7d8-106">Summary</span></span>

 <span data-ttu-id="ba7d8-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ba7d8-107">Members</span></span>                        | <span data-ttu-id="ba7d8-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ba7d8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ba7d8-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ba7d8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ba7d8-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ba7d8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ba7d8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ba7d8-111">Members</span></span>

#### <span data-ttu-id="ba7d8-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="ba7d8-112">Invoke</span></span> 

<span data-ttu-id="ba7d8-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ba7d8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ba7d8-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ba7d8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

