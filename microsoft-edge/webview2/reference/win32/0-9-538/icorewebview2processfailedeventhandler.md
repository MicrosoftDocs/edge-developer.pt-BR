---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: d65c6ae63f5c79540587f99e3ff42c4ebb3e409e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010828"
---
# <span data-ttu-id="ed913-104">0.9.579-ICoreWebView2ProcessFailedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="ed913-104">0.9.579 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="ed913-105">O chamador implementa essa interface para receber eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="ed913-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="ed913-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ed913-106">Summary</span></span>

 <span data-ttu-id="ed913-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ed913-107">Members</span></span>                        | <span data-ttu-id="ed913-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ed913-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed913-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ed913-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ed913-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ed913-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ed913-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ed913-111">Members</span></span>

#### <span data-ttu-id="ed913-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="ed913-112">Invoke</span></span> 

<span data-ttu-id="ed913-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ed913-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ed913-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ed913-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>

