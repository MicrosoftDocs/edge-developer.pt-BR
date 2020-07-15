---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 9ea8f860d637c5d9e49e68917d167380c0418b87
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877368"
---
# <span data-ttu-id="8dd23-104">0.9.515-ICoreWebView2SourceChangedEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="8dd23-104">0.9.515 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8dd23-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="8dd23-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8dd23-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="8dd23-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="8dd23-107">Argumentos de evento para o evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="8dd23-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="8dd23-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="8dd23-108">Summary</span></span>

 <span data-ttu-id="8dd23-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8dd23-109">Members</span></span>                        | <span data-ttu-id="8dd23-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="8dd23-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8dd23-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="8dd23-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="8dd23-112">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="8dd23-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="8dd23-113">Parte</span><span class="sxs-lookup"><span data-stu-id="8dd23-113">Members</span></span>

#### <span data-ttu-id="8dd23-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="8dd23-114">get_IsNewDocument</span></span> 

<span data-ttu-id="8dd23-115">True se a página à qual está sendo acessada for um novo documento.</span><span class="sxs-lookup"><span data-stu-id="8dd23-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="8dd23-116">[get_IsNewDocument](#get_isnewdocument)público HRESULT (bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="8dd23-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

