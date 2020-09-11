---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 7cadbfddca9c05c8649b79503de3ce4f3695ea4c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011269"
---
# <span data-ttu-id="8e451-104">0.9.579-ICoreWebView2NewBrowserVersionAvailableEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="8e451-104">0.9.579 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="8e451-105">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8e451-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="8e451-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="8e451-106">Summary</span></span>

 <span data-ttu-id="8e451-107">Parte</span><span class="sxs-lookup"><span data-stu-id="8e451-107">Members</span></span>                        | <span data-ttu-id="8e451-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="8e451-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8e451-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="8e451-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8e451-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8e451-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8e451-111">Parte</span><span class="sxs-lookup"><span data-stu-id="8e451-111">Members</span></span>

#### <span data-ttu-id="8e451-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="8e451-112">Invoke</span></span> 

<span data-ttu-id="8e451-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="8e451-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8e451-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="8e451-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

