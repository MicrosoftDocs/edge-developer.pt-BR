---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8a9f1b1e44353796c6d3b57d3f4c6f3d4997aad5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880196"
---
# <span data-ttu-id="01e74-104">0.9.430-ICoreWebView2SourceChangedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="01e74-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="01e74-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="01e74-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="01e74-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="01e74-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="01e74-107">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="01e74-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="01e74-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="01e74-108">Summary</span></span>

 <span data-ttu-id="01e74-109">Parte</span><span class="sxs-lookup"><span data-stu-id="01e74-109">Members</span></span>                        | <span data-ttu-id="01e74-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="01e74-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="01e74-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="01e74-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="01e74-112">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="01e74-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="01e74-113">Parte</span><span class="sxs-lookup"><span data-stu-id="01e74-113">Members</span></span>

#### <span data-ttu-id="01e74-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="01e74-114">get_IsNewDocument</span></span> 

<span data-ttu-id="01e74-115">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="01e74-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="01e74-116">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="01e74-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

