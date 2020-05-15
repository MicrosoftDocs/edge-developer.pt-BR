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
ms.openlocfilehash: 91c4e7885526def5de6fd1910a4a6f06c6a6953a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652442"
---
# <span data-ttu-id="79228-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="79228-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="79228-105">Esta é uma API experimental que é fornecida com a versão 0.9.488 do SDK de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="79228-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="79228-106">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="79228-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="79228-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="79228-107">Summary</span></span>

 <span data-ttu-id="79228-108">Parte</span><span class="sxs-lookup"><span data-stu-id="79228-108">Members</span></span>                        | <span data-ttu-id="79228-109">Descrições</span><span class="sxs-lookup"><span data-stu-id="79228-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="79228-110">Invocar</span><span class="sxs-lookup"><span data-stu-id="79228-110">Invoke</span></span>](#invoke) | <span data-ttu-id="79228-111">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="79228-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="79228-112">Parte</span><span class="sxs-lookup"><span data-stu-id="79228-112">Members</span></span>

#### <span data-ttu-id="79228-113">Invocar</span><span class="sxs-lookup"><span data-stu-id="79228-113">Invoke</span></span> 

<span data-ttu-id="79228-114">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="79228-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="79228-115">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="79228-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

