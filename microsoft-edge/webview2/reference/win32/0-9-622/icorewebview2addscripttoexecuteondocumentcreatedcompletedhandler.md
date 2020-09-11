---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 1580f119a83a171f304b7b05ecbc88edfe31e26d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011576"
---
# <span data-ttu-id="1f8e4-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1f8e4-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="1f8e4-105">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="1f8e4-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="1f8e4-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="1f8e4-106">Summary</span></span>

 <span data-ttu-id="1f8e4-107">Parte</span><span class="sxs-lookup"><span data-stu-id="1f8e4-107">Members</span></span>                        | <span data-ttu-id="1f8e4-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="1f8e4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1f8e4-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="1f8e4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1f8e4-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="1f8e4-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="1f8e4-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1f8e4-111">Members</span></span>

#### <span data-ttu-id="1f8e4-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="1f8e4-112">Invoke</span></span> 

<span data-ttu-id="1f8e4-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="1f8e4-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="1f8e4-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1f8e4-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

