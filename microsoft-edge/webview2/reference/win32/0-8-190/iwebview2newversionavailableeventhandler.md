---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: da17bad643ac7f0a9614754bf57c7d208c265ace
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878355"
---
# <span data-ttu-id="d386a-104">0.8.355-IWebView2NewVersionAvailableEventHandler de interface</span><span class="sxs-lookup"><span data-stu-id="d386a-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d386a-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d386a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d386a-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d386a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="d386a-107">O chamador implementa essa interface para receber eventos NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="d386a-107">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="d386a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d386a-108">Summary</span></span>

 <span data-ttu-id="d386a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d386a-109">Members</span></span>                        | <span data-ttu-id="d386a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d386a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d386a-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="d386a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d386a-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d386a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d386a-113">Use o método get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) para obter o novo número de versão.</span><span class="sxs-lookup"><span data-stu-id="d386a-113">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="d386a-114">Parte</span><span class="sxs-lookup"><span data-stu-id="d386a-114">Members</span></span>

#### <span data-ttu-id="d386a-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="d386a-115">Invoke</span></span> 

<span data-ttu-id="d386a-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d386a-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d386a-117">[chamada](#invoke)a Public HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d386a-117">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

