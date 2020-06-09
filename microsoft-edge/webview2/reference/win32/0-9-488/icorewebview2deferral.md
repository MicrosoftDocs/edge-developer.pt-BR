---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 7d21db7c3f0a66f60f32e92b3951151b8d13a002
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698075"
---
# <span data-ttu-id="6f4f8-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="6f4f8-104">interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="6f4f8-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="6f4f8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6f4f8-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="6f4f8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="6f4f8-107">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="6f4f8-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="6f4f8-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="6f4f8-108">Summary</span></span>

 <span data-ttu-id="6f4f8-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6f4f8-109">Members</span></span>                        | <span data-ttu-id="6f4f8-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="6f4f8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f4f8-111">Concluída</span><span class="sxs-lookup"><span data-stu-id="6f4f8-111">Complete</span></span>](#complete) | <span data-ttu-id="6f4f8-112">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="6f4f8-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="6f4f8-113">Parte</span><span class="sxs-lookup"><span data-stu-id="6f4f8-113">Members</span></span>

#### <span data-ttu-id="6f4f8-114">Concluída</span><span class="sxs-lookup"><span data-stu-id="6f4f8-114">Complete</span></span> 

<span data-ttu-id="6f4f8-115">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="6f4f8-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="6f4f8-116">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="6f4f8-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="6f4f8-117">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="6f4f8-117">Complete should only be called once for each deferral taken.</span></span>

