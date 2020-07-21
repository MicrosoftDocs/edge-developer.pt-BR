---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b30b6e35388ab01433b2c879db82d9c4136fae99
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885412"
---
# <span data-ttu-id="f6716-104">0.9.515-ICoreWebView2Deferral de interface</span><span class="sxs-lookup"><span data-stu-id="f6716-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="f6716-105">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="f6716-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="f6716-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="f6716-106">Summary</span></span>

 <span data-ttu-id="f6716-107">Parte</span><span class="sxs-lookup"><span data-stu-id="f6716-107">Members</span></span>                        | <span data-ttu-id="f6716-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="f6716-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f6716-109">Concluída</span><span class="sxs-lookup"><span data-stu-id="f6716-109">Complete</span></span>](#complete) | <span data-ttu-id="f6716-110">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="f6716-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="f6716-111">Parte</span><span class="sxs-lookup"><span data-stu-id="f6716-111">Members</span></span>

#### <span data-ttu-id="f6716-112">Concluída</span><span class="sxs-lookup"><span data-stu-id="f6716-112">Complete</span></span> 

<span data-ttu-id="f6716-113">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="f6716-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="f6716-114">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="f6716-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="f6716-115">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="f6716-115">Complete should only be called once for each deferral taken.</span></span>

