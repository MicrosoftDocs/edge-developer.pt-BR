---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: f5c1799225df5460029b3ad0c40db63a2e16113c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011423"
---
# <span data-ttu-id="189bb-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="189bb-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="189bb-105">O chamador implementa essa interface para receber eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="189bb-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="189bb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="189bb-106">Summary</span></span>

 <span data-ttu-id="189bb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="189bb-107">Members</span></span>                        | <span data-ttu-id="189bb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="189bb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="189bb-109">Invocar</span><span class="sxs-lookup"><span data-stu-id="189bb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="189bb-110">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="189bb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="189bb-111">Parte</span><span class="sxs-lookup"><span data-stu-id="189bb-111">Members</span></span>

#### <span data-ttu-id="189bb-112">Invocar</span><span class="sxs-lookup"><span data-stu-id="189bb-112">Invoke</span></span> 

<span data-ttu-id="189bb-113">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="189bb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="189bb-114">[chamada](#invoke)a Public HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="189bb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="189bb-115">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="189bb-115">There are no event args and the args parameter will be null.</span></span>

