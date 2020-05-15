---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 69c569be7e712d0f5cfddbaa180419be8d475ad0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652735"
---
# <span data-ttu-id="d9ca8-104">interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d9ca8-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d9ca8-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d9ca8-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d9ca8-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="d9ca8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="d9ca8-107">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="d9ca8-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="d9ca8-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="d9ca8-108">Summary</span></span>

 <span data-ttu-id="d9ca8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d9ca8-109">Members</span></span>                        | <span data-ttu-id="d9ca8-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="d9ca8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9ca8-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="d9ca8-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="d9ca8-112">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="d9ca8-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="d9ca8-113">Parte</span><span class="sxs-lookup"><span data-stu-id="d9ca8-113">Members</span></span>

#### <span data-ttu-id="d9ca8-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="d9ca8-114">get_IsNewDocument</span></span> 

<span data-ttu-id="d9ca8-115">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="d9ca8-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="d9ca8-116">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="d9ca8-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

