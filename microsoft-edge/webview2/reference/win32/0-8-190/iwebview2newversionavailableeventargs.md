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
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652686"
---
# <span data-ttu-id="1a770-104">interface IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="1a770-104">interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1a770-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="1a770-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1a770-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="1a770-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="1a770-107">Args de evento para o evento NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="1a770-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="1a770-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="1a770-108">Summary</span></span>

 <span data-ttu-id="1a770-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1a770-109">Members</span></span>                        | <span data-ttu-id="1a770-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="1a770-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1a770-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="1a770-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="1a770-112">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="1a770-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="1a770-113">Parte</span><span class="sxs-lookup"><span data-stu-id="1a770-113">Members</span></span>

#### <span data-ttu-id="1a770-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="1a770-114">get_NewVersion</span></span> 

<span data-ttu-id="1a770-115">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="1a770-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="1a770-116">[get_NewVersion](#get_newversion)público HRESULT (LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="1a770-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

