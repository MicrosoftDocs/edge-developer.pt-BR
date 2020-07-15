---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Deferral
ms.openlocfilehash: 85c8a795a79bae461ad958e6586b9bf1f6778075
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880119"
---
# <span data-ttu-id="d60ba-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="d60ba-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="d60ba-105">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="d60ba-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="d60ba-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d60ba-106">Summary</span></span>

 <span data-ttu-id="d60ba-107">Parte</span><span class="sxs-lookup"><span data-stu-id="d60ba-107">Members</span></span>                        | <span data-ttu-id="d60ba-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="d60ba-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d60ba-109">Concluída</span><span class="sxs-lookup"><span data-stu-id="d60ba-109">Complete</span></span>](#complete) | <span data-ttu-id="d60ba-110">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="d60ba-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="d60ba-111">Parte</span><span class="sxs-lookup"><span data-stu-id="d60ba-111">Members</span></span>

#### <span data-ttu-id="d60ba-112">Concluída</span><span class="sxs-lookup"><span data-stu-id="d60ba-112">Complete</span></span> 

<span data-ttu-id="d60ba-113">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="d60ba-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="d60ba-114">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="d60ba-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="d60ba-115">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="d60ba-115">Complete should only be called once for each deferral taken.</span></span>

