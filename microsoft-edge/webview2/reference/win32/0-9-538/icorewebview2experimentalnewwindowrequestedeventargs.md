---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 39d52b1231e767739b63b3759cdd08e4c9b26be3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879986"
---
# <span data-ttu-id="452cc-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="452cc-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="452cc-105">Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="452cc-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="452cc-106">Args de evento para o evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="452cc-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="452cc-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="452cc-107">Summary</span></span>

 <span data-ttu-id="452cc-108">Parte</span><span class="sxs-lookup"><span data-stu-id="452cc-108">Members</span></span>                        | <span data-ttu-id="452cc-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="452cc-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="452cc-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="452cc-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="452cc-111">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="452cc-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="452cc-112">O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)</span><span class="sxs-lookup"><span data-stu-id="452cc-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="452cc-113">Parte</span><span class="sxs-lookup"><span data-stu-id="452cc-113">Members</span></span>

#### <span data-ttu-id="452cc-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="452cc-114">get_WindowFeatures</span></span> 

<span data-ttu-id="452cc-115">Recursos de janela especificados pela chamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="452cc-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="452cc-116">Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="452cc-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="452cc-117">Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.</span><span class="sxs-lookup"><span data-stu-id="452cc-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

