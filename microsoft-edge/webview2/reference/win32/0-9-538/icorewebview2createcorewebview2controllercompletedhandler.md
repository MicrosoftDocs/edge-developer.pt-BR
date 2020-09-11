---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 3ecafb8181b04032bf121a93af3771cfcad8fa91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011158"
---
# <span data-ttu-id="1a066-104">0.9.579-ICoreWebView2CreateCoreWebView2ControllerCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="1a066-104">0.9.579 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="1a066-105">O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="1a066-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="1a066-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1a066-106">Summary</span></span>

 <span data-ttu-id="1a066-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1a066-107">Members</span></span>                        | <span data-ttu-id="1a066-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1a066-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1a066-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="1a066-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1a066-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="1a066-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="1a066-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1a066-111">Members</span></span>

#### <span data-ttu-id="1a066-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="1a066-112">Invoke</span></span> 

<span data-ttu-id="1a066-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="1a066-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="1a066-114">[chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="1a066-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

