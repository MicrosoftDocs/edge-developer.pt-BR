---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885867"
---
# <span data-ttu-id="c1be9-104">0.8.355-IWebView2NewVersionAvailableEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="c1be9-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="c1be9-105">Args de evento para o evento NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="c1be9-105">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="c1be9-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c1be9-106">Summary</span></span>

 <span data-ttu-id="c1be9-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c1be9-107">Members</span></span>                        | <span data-ttu-id="c1be9-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c1be9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1be9-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="c1be9-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="c1be9-110">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="c1be9-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="c1be9-111">Parte</span><span class="sxs-lookup"><span data-stu-id="c1be9-111">Members</span></span>

#### <span data-ttu-id="c1be9-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="c1be9-112">get_NewVersion</span></span> 

<span data-ttu-id="c1be9-113">As informações de versão do navegador do [IWebView2Environment](IWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="c1be9-113">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="c1be9-114">[get_NewVersion](#get_newversion)público HRESULT (LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="c1be9-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

