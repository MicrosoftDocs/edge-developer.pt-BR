---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: 906b09ad99d6d6d9e74c52c0582584b9e46f74ba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010534"
---
# <span data-ttu-id="66051-104">0.9.579-ICoreWebView2ContentLoadingEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="66051-104">0.9.579 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="66051-105">O chamador implementa essa interface para receber o evento ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="66051-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="66051-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="66051-106">Summary</span></span>

 <span data-ttu-id="66051-107">Parte</span><span class="sxs-lookup"><span data-stu-id="66051-107">Members</span></span>                        | <span data-ttu-id="66051-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="66051-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66051-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="66051-109">Invoke</span></span>](#invoke) | <span data-ttu-id="66051-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="66051-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="66051-111">Parte</span><span class="sxs-lookup"><span data-stu-id="66051-111">Members</span></span>

#### <span data-ttu-id="66051-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="66051-112">Invoke</span></span> 

<span data-ttu-id="66051-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="66051-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="66051-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="66051-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

