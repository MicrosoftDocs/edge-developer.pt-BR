---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: e9f98b43463fe5259d2f9f723b62b78c1d1a4758
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652646"
---
# <span data-ttu-id="fba5c-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="fba5c-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="fba5c-105">O chamador implementa essa interface para receber o resultado do método AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="fba5c-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="fba5c-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="fba5c-106">Summary</span></span>

 <span data-ttu-id="fba5c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="fba5c-107">Members</span></span>                        | <span data-ttu-id="fba5c-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="fba5c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fba5c-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="fba5c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fba5c-110">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="fba5c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="fba5c-111">Parte</span><span class="sxs-lookup"><span data-stu-id="fba5c-111">Members</span></span>

#### <span data-ttu-id="fba5c-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="fba5c-112">Invoke</span></span> 

<span data-ttu-id="fba5c-113">Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.</span><span class="sxs-lookup"><span data-stu-id="fba5c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="fba5c-114">[chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="fba5c-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

