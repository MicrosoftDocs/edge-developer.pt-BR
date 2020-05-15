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
ms.openlocfilehash: d808f4b112d3688b4e50a2f6b69db38bbb4808c5
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652691"
---
# <span data-ttu-id="66364-104">interface ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="66364-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="66364-105">O chamador implementa essa interface para receber o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="66364-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="66364-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="66364-106">Summary</span></span>

 <span data-ttu-id="66364-107">Parte</span><span class="sxs-lookup"><span data-stu-id="66364-107">Members</span></span>                        | <span data-ttu-id="66364-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="66364-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66364-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="66364-109">Invoke</span></span>](#invoke) | <span data-ttu-id="66364-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="66364-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="66364-111">Parte</span><span class="sxs-lookup"><span data-stu-id="66364-111">Members</span></span>

#### <span data-ttu-id="66364-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="66364-112">Invoke</span></span> 

<span data-ttu-id="66364-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="66364-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="66364-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="66364-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

