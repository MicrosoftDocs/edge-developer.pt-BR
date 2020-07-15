---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 903574f0372e9d077907b9e9d538007cb71f830f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878670"
---
# <span data-ttu-id="899ea-104">0.8.355-IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="899ea-104">0.8.355 - interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="899ea-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="899ea-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="899ea-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="899ea-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="899ea-107">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="899ea-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="899ea-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="899ea-108">Summary</span></span>

 <span data-ttu-id="899ea-109">Parte</span><span class="sxs-lookup"><span data-stu-id="899ea-109">Members</span></span>                        | <span data-ttu-id="899ea-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="899ea-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="899ea-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="899ea-111">Invoke</span></span>](#invoke) | <span data-ttu-id="899ea-112">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="899ea-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="899ea-113">Parte</span><span class="sxs-lookup"><span data-stu-id="899ea-113">Members</span></span>

#### <span data-ttu-id="899ea-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="899ea-114">Invoke</span></span> 

<span data-ttu-id="899ea-115">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="899ea-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="899ea-116">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="899ea-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

