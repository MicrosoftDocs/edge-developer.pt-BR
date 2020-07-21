---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884858"
---
# <span data-ttu-id="72876-104">0.9.430-ICoreWebView2NewBrowserVersionAvailableEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="72876-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="72876-105">Args de evento para o evento NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="72876-105">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="72876-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="72876-106">Summary</span></span>

 <span data-ttu-id="72876-107">Parte</span><span class="sxs-lookup"><span data-stu-id="72876-107">Members</span></span>                        | <span data-ttu-id="72876-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="72876-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="72876-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="72876-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="72876-110">As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="72876-110">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="72876-111">Parte</span><span class="sxs-lookup"><span data-stu-id="72876-111">Members</span></span>

#### <span data-ttu-id="72876-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="72876-112">get_NewVersion</span></span> 

<span data-ttu-id="72876-113">As informações de versão do navegador do [ICoreWebView2Environment](ICoreWebView2Environment.md)atual.</span><span class="sxs-lookup"><span data-stu-id="72876-113">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="72876-114">[get_NewVersion](#get_newversion)público HRESULT (LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="72876-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

