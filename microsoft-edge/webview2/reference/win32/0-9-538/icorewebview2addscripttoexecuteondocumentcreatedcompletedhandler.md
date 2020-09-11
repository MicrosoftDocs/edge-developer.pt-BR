---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 9321f7912cb1217a3b6a28f322469ea12e5820dc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010625"
---
# <span data-ttu-id="58c1b-104">0.9.579-ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler de interface</span><span class="sxs-lookup"><span data-stu-id="58c1b-104">0.9.579 - interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="58c1b-105">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="58c1b-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="58c1b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="58c1b-106">Summary</span></span>

 <span data-ttu-id="58c1b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="58c1b-107">Members</span></span>                        | <span data-ttu-id="58c1b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="58c1b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="58c1b-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="58c1b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="58c1b-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="58c1b-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="58c1b-111">Parte</span><span class="sxs-lookup"><span data-stu-id="58c1b-111">Members</span></span>

#### <span data-ttu-id="58c1b-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="58c1b-112">Invoke</span></span> 

<span data-ttu-id="58c1b-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="58c1b-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="58c1b-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="58c1b-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

