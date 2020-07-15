---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: bd2ff8092ce0b8367ce4cc381e94dbd273ae1849
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880826"
---
# <span data-ttu-id="ca52f-104">0.9.515-ICoreWebView2Deferral de interface</span><span class="sxs-lookup"><span data-stu-id="ca52f-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="ca52f-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ca52f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ca52f-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ca52f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="ca52f-107">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="ca52f-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ca52f-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ca52f-108">Summary</span></span>

 <span data-ttu-id="ca52f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ca52f-109">Members</span></span>                        | <span data-ttu-id="ca52f-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ca52f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca52f-111">Concluída</span><span class="sxs-lookup"><span data-stu-id="ca52f-111">Complete</span></span>](#complete) | <span data-ttu-id="ca52f-112">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="ca52f-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ca52f-113">Parte</span><span class="sxs-lookup"><span data-stu-id="ca52f-113">Members</span></span>

#### <span data-ttu-id="ca52f-114">Concluída</span><span class="sxs-lookup"><span data-stu-id="ca52f-114">Complete</span></span> 

<span data-ttu-id="ca52f-115">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="ca52f-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ca52f-116">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ca52f-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="ca52f-117">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="ca52f-117">Complete should only be called once for each deferral taken.</span></span>

