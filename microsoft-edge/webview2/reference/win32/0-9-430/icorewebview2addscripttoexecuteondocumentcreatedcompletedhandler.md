---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 3c34c75e62fd73530d338e618469e071648f2fcb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884341"
---
# <span data-ttu-id="b1edc-104">0.9.430-ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="b1edc-104">0.9.430 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b1edc-105">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="b1edc-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="b1edc-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="b1edc-106">Summary</span></span>

 <span data-ttu-id="b1edc-107">Parte</span><span class="sxs-lookup"><span data-stu-id="b1edc-107">Members</span></span>                        | <span data-ttu-id="b1edc-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="b1edc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1edc-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="b1edc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b1edc-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b1edc-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b1edc-111">Parte</span><span class="sxs-lookup"><span data-stu-id="b1edc-111">Members</span></span>

#### <span data-ttu-id="b1edc-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="b1edc-112">Invoke</span></span> 

<span data-ttu-id="b1edc-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="b1edc-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b1edc-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b1edc-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

