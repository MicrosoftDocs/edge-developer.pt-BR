---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: d18ccc91d16213cf0a915420b406b65823b3f9d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886448"
---
# <span data-ttu-id="be631-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="be631-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="be631-105">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="be631-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="be631-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="be631-106">Summary</span></span>

 <span data-ttu-id="be631-107">Parte</span><span class="sxs-lookup"><span data-stu-id="be631-107">Members</span></span>                        | <span data-ttu-id="be631-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="be631-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be631-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="be631-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="be631-110">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="be631-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="be631-111">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="be631-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="be631-112">Parte</span><span class="sxs-lookup"><span data-stu-id="be631-112">Members</span></span>

#### <span data-ttu-id="be631-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="be631-113">get_WindowFeatures</span></span> 

<span data-ttu-id="be631-114">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="be631-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="be631-115">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="be631-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="be631-116">Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.</span><span class="sxs-lookup"><span data-stu-id="be631-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

