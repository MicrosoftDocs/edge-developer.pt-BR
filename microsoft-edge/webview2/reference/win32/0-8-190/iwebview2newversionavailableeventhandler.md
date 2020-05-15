---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: a02a7ac3e31f959e80d5a3bdc41e39f653b9949c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652685"
---
# <span data-ttu-id="f41df-104">interface IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="f41df-104">interface IWebView2NewVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f41df-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="f41df-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f41df-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="f41df-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="f41df-107">O chamador implementa essa interface para receber eventos NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="f41df-107">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="f41df-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="f41df-108">Summary</span></span>

 <span data-ttu-id="f41df-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f41df-109">Members</span></span>                        | <span data-ttu-id="f41df-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="f41df-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f41df-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="f41df-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f41df-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f41df-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f41df-113">Use o método get_NewVersion de [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) para obter o novo número de versão.</span><span class="sxs-lookup"><span data-stu-id="f41df-113">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="f41df-114">Parte</span><span class="sxs-lookup"><span data-stu-id="f41df-114">Members</span></span>

#### <span data-ttu-id="f41df-115">Invocar</span><span class="sxs-lookup"><span data-stu-id="f41df-115">Invoke</span></span> 

<span data-ttu-id="f41df-116">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="f41df-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f41df-117">[chamada](#invoke)a Public HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f41df-117">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

