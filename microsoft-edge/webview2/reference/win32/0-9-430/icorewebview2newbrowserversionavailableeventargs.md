---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652587"
---
# <span data-ttu-id="e1402-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="e1402-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e1402-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e1402-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e1402-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e1402-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="e1402-107">Args de evento para o evento NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="e1402-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="e1402-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e1402-108">Summary</span></span>

 <span data-ttu-id="e1402-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e1402-109">Members</span></span>                        | <span data-ttu-id="e1402-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e1402-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1402-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="e1402-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="e1402-112">As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="e1402-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="e1402-113">Parte</span><span class="sxs-lookup"><span data-stu-id="e1402-113">Members</span></span>

#### <span data-ttu-id="e1402-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="e1402-114">get_NewVersion</span></span> 

<span data-ttu-id="e1402-115">As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="e1402-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="e1402-116">[get_NewVersion](#get_newversion)público HRESULT (LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="e1402-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

