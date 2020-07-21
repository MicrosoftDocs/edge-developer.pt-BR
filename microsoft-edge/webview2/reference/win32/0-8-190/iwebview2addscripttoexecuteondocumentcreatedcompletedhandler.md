---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 464192c119ddb7dd59ee7cb5981f172eb44dbb78
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885013"
---
# <span data-ttu-id="b37c6-104">0.8.355-IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="b37c6-104">0.8.355 - interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b37c6-105">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="b37c6-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="b37c6-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b37c6-106">Summary</span></span>

 <span data-ttu-id="b37c6-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b37c6-107">Members</span></span>                        | <span data-ttu-id="b37c6-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b37c6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b37c6-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b37c6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b37c6-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b37c6-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b37c6-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b37c6-111">Members</span></span>

#### <span data-ttu-id="b37c6-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="b37c6-112">Invoke</span></span> 

<span data-ttu-id="b37c6-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b37c6-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b37c6-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b37c6-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

