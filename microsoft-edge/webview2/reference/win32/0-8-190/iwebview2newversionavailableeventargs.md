---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878341"
---
# <span data-ttu-id="8fbe3-104">0.8.355-IWebView2NewVersionAvailableEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="8fbe3-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8fbe3-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="8fbe3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="8fbe3-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8fbe3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="8fbe3-107">Args de evento para o evento NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="8fbe3-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="8fbe3-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8fbe3-108">Summary</span></span>

 <span data-ttu-id="8fbe3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8fbe3-109">Members</span></span>                        | <span data-ttu-id="8fbe3-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8fbe3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8fbe3-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="8fbe3-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="8fbe3-112">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="8fbe3-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="8fbe3-113">Parte</span><span class="sxs-lookup"><span data-stu-id="8fbe3-113">Members</span></span>

#### <span data-ttu-id="8fbe3-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="8fbe3-114">get_NewVersion</span></span> 

<span data-ttu-id="8fbe3-115">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="8fbe3-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="8fbe3-116">[get_NewVersion](#get_newversion)público HRESULT (LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="8fbe3-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

