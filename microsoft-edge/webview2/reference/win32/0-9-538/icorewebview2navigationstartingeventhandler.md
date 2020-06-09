---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: faeafdb0f2da5fa5037f41faab0d0b5ee8434eb4
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698327"
---
# <span data-ttu-id="bb28b-104">interface ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="bb28b-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="bb28b-105">O chamador implementa essa interface para receber o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="bb28b-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="bb28b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="bb28b-106">Summary</span></span>

 <span data-ttu-id="bb28b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="bb28b-107">Members</span></span>                        | <span data-ttu-id="bb28b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="bb28b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bb28b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="bb28b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bb28b-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="bb28b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="bb28b-111">Parte</span><span class="sxs-lookup"><span data-stu-id="bb28b-111">Members</span></span>

#### <span data-ttu-id="bb28b-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="bb28b-112">Invoke</span></span> 

<span data-ttu-id="bb28b-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="bb28b-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bb28b-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="bb28b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

