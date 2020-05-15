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
ms.openlocfilehash: f9dcfa996058f4499daff03d8cad033ac61db4c9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652610"
---
# <span data-ttu-id="7098b-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7098b-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7098b-105">O chamador implementa esse método para receber o evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7098b-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="7098b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7098b-106">Summary</span></span>

 <span data-ttu-id="7098b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7098b-107">Members</span></span>                        | <span data-ttu-id="7098b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7098b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7098b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="7098b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7098b-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7098b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7098b-111">Parte</span><span class="sxs-lookup"><span data-stu-id="7098b-111">Members</span></span>

#### <span data-ttu-id="7098b-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="7098b-112">Invoke</span></span> 

<span data-ttu-id="7098b-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="7098b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7098b-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7098b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

