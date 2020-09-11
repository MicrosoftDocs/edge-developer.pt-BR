---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: bec7596457800713eda5286c4ea1584bcfe9ed35
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011255"
---
# <span data-ttu-id="440cf-104">0.9.579-ICoreWebView2NavigationStartingEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="440cf-104">0.9.579 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="440cf-105">O chamador implementa essa interface para receber o evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="440cf-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="440cf-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="440cf-106">Summary</span></span>

 <span data-ttu-id="440cf-107">Parte</span><span class="sxs-lookup"><span data-stu-id="440cf-107">Members</span></span>                        | <span data-ttu-id="440cf-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="440cf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="440cf-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="440cf-109">Invoke</span></span>](#invoke) | <span data-ttu-id="440cf-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="440cf-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="440cf-111">Parte</span><span class="sxs-lookup"><span data-stu-id="440cf-111">Members</span></span>

#### <span data-ttu-id="440cf-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="440cf-112">Invoke</span></span> 

<span data-ttu-id="440cf-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="440cf-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="440cf-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="440cf-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

