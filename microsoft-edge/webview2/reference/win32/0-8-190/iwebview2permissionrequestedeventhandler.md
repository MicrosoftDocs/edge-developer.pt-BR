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
ms.openlocfilehash: d669b73edd8def1d8a44491705e0f80888da2b3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652551"
---
# <span data-ttu-id="de942-104">interface IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="de942-104">interface IWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="de942-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="de942-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="de942-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="de942-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="de942-107">O chamador implementa essa interface para receber o evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="de942-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="de942-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="de942-108">Summary</span></span>

 <span data-ttu-id="de942-109">Parte</span><span class="sxs-lookup"><span data-stu-id="de942-109">Members</span></span>                        | <span data-ttu-id="de942-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="de942-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="de942-111">Invocar</span><span class="sxs-lookup"><span data-stu-id="de942-111">Invoke</span></span>](#invoke) | <span data-ttu-id="de942-112">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="de942-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="de942-113">Parte</span><span class="sxs-lookup"><span data-stu-id="de942-113">Members</span></span>

#### <span data-ttu-id="de942-114">Invocar</span><span class="sxs-lookup"><span data-stu-id="de942-114">Invoke</span></span> 

<span data-ttu-id="de942-115">Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="de942-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="de942-116">Public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="de942-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

