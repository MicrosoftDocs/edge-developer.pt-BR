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
ms.openlocfilehash: 45ac3cf4728f8b09f9ce65a30b53506fc2829c9d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698299"
---
# <span data-ttu-id="ee0cd-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ee0cd-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ee0cd-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="ee0cd-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="ee0cd-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ee0cd-106">Summary</span></span>

 <span data-ttu-id="ee0cd-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ee0cd-107">Members</span></span>                        | <span data-ttu-id="ee0cd-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ee0cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ee0cd-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="ee0cd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ee0cd-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="ee0cd-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ee0cd-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ee0cd-111">Members</span></span>

#### <span data-ttu-id="ee0cd-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="ee0cd-112">Invoke</span></span> 

<span data-ttu-id="ee0cd-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="ee0cd-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ee0cd-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="ee0cd-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

