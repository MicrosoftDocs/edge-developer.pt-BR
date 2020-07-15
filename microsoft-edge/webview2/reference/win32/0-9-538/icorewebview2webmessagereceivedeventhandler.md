---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WebMessageReceivedEventHandler
ms.openlocfilehash: 47402035918c49a86c8e973c207d4f54d7d829c7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879349"
---
# <span data-ttu-id="35011-104">interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="35011-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="35011-105">O chamador implementa essa interface para receber o evento WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="35011-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="35011-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="35011-106">Summary</span></span>

 <span data-ttu-id="35011-107">Parte</span><span class="sxs-lookup"><span data-stu-id="35011-107">Members</span></span>                        | <span data-ttu-id="35011-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="35011-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35011-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="35011-109">Invoke</span></span>](#invoke) | <span data-ttu-id="35011-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="35011-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="35011-111">Parte</span><span class="sxs-lookup"><span data-stu-id="35011-111">Members</span></span>

#### <span data-ttu-id="35011-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="35011-112">Invoke</span></span> 

<span data-ttu-id="35011-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="35011-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="35011-114">Public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="35011-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

