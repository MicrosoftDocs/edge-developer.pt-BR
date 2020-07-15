---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877851"
---
# <span data-ttu-id="9e768-104">0.9.430-ICoreWebView2NewBrowserVersionAvailableEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="9e768-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9e768-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9e768-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9e768-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="9e768-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="9e768-107">Args de evento para o evento NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="9e768-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="9e768-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9e768-108">Summary</span></span>

 <span data-ttu-id="9e768-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9e768-109">Members</span></span>                        | <span data-ttu-id="9e768-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9e768-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e768-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="9e768-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="9e768-112">As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="9e768-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="9e768-113">Parte</span><span class="sxs-lookup"><span data-stu-id="9e768-113">Members</span></span>

#### <span data-ttu-id="9e768-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="9e768-114">get_NewVersion</span></span> 

<span data-ttu-id="9e768-115">As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="9e768-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="9e768-116">[get_NewVersion](#get_newversion)público HRESULT (LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="9e768-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

