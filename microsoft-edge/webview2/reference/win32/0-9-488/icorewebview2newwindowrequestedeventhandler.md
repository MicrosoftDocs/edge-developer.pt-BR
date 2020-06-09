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
ms.openlocfilehash: df43e9cb1d036482a73e1ff92446a5a74b921d5d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698152"
---
# <span data-ttu-id="ea312-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ea312-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ea312-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ea312-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ea312-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ea312-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ea312-107">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ea312-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="ea312-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ea312-108">Summary</span></span>

 <span data-ttu-id="ea312-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ea312-109">Members</span></span>                        | <span data-ttu-id="ea312-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ea312-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea312-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="ea312-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ea312-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea312-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ea312-113">Parte</span><span class="sxs-lookup"><span data-stu-id="ea312-113">Members</span></span>

#### <span data-ttu-id="ea312-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="ea312-114">Invoke</span></span> 

<span data-ttu-id="ea312-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea312-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ea312-116">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ea312-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

