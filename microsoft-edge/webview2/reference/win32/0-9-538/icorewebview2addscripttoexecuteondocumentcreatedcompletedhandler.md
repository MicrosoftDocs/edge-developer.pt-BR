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
ms.openlocfilehash: 9777a27c1b9252d0d1a5f91a4692b9043fffc569
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698311"
---
# <span data-ttu-id="7af38-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7af38-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7af38-105">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="7af38-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="7af38-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7af38-106">Summary</span></span>

 <span data-ttu-id="7af38-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7af38-107">Members</span></span>                        | <span data-ttu-id="7af38-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7af38-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7af38-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="7af38-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7af38-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="7af38-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7af38-111">Parte</span><span class="sxs-lookup"><span data-stu-id="7af38-111">Members</span></span>

#### <span data-ttu-id="7af38-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="7af38-112">Invoke</span></span> 

<span data-ttu-id="7af38-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="7af38-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7af38-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="7af38-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

