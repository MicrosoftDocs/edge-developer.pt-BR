---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 42031b966f799b788a94938d88d9dec6f4542288
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878537"
---
# <span data-ttu-id="116f2-104">0.8.355-IWebView2DocumentTitleChangedEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="116f2-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="116f2-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="116f2-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="116f2-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="116f2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="116f2-107">O chamador implementa essa interface para receber eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="116f2-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="116f2-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="116f2-108">Summary</span></span>

 <span data-ttu-id="116f2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="116f2-109">Members</span></span>                        | <span data-ttu-id="116f2-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="116f2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="116f2-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="116f2-111">Invoke</span></span>](#invoke) | <span data-ttu-id="116f2-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="116f2-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="116f2-113">Use a propriedade DocumentTitle para obter o título modificado.</span><span class="sxs-lookup"><span data-stu-id="116f2-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="116f2-114">Parte</span><span class="sxs-lookup"><span data-stu-id="116f2-114">Members</span></span>

#### <span data-ttu-id="116f2-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="116f2-115">Invoke</span></span> 

<span data-ttu-id="116f2-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="116f2-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="116f2-117">[chamada](#invoke)a Public HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="116f2-117">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="116f2-118">Não há argumentos de evento e o parâmetro args será nulo.</span><span class="sxs-lookup"><span data-stu-id="116f2-118">There are no event args and the args parameter will be null.</span></span>

