---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 42f63855c97363dab1a19cc784cf654afc40de74
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877844"
---
# <span data-ttu-id="b293e-104">0.9.430-ICoreWebView2NewBrowserVersionAvailableEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="b293e-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b293e-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b293e-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b293e-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b293e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="b293e-107">O chamador implementa essa interface para receber eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="b293e-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="b293e-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b293e-108">Summary</span></span>

 <span data-ttu-id="b293e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b293e-109">Members</span></span>                        | <span data-ttu-id="b293e-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b293e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b293e-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="b293e-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b293e-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b293e-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b293e-113">Use o método get_NewVersion de [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) para obter o novo número de versão.</span><span class="sxs-lookup"><span data-stu-id="b293e-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="b293e-114">Parte</span><span class="sxs-lookup"><span data-stu-id="b293e-114">Members</span></span>

#### <span data-ttu-id="b293e-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="b293e-115">Invoke</span></span> 

<span data-ttu-id="b293e-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="b293e-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b293e-117">[chamada](#invoke)a Public HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b293e-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

