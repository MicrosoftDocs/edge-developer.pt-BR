---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: 89b1e7fada56bcf535ae07be109acbb340fdc9a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011493"
---
# <span data-ttu-id="ca523-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ca523-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ca523-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="ca523-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="ca523-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ca523-106">Summary</span></span>

 <span data-ttu-id="ca523-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ca523-107">Members</span></span>                        | <span data-ttu-id="ca523-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ca523-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca523-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ca523-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ca523-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ca523-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ca523-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ca523-111">Members</span></span>

#### <span data-ttu-id="ca523-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="ca523-112">Invoke</span></span> 

<span data-ttu-id="ca523-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ca523-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ca523-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ca523-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

