---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Deferral
ms.openlocfilehash: d8abff93df317a42c1bfe89dd32ac1d5f7e8c329
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011600"
---
# <span data-ttu-id="24685-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="24685-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="24685-105">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="24685-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="24685-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="24685-106">Summary</span></span>

 <span data-ttu-id="24685-107">Parte</span><span class="sxs-lookup"><span data-stu-id="24685-107">Members</span></span>                        | <span data-ttu-id="24685-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="24685-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="24685-109">Concluída</span><span class="sxs-lookup"><span data-stu-id="24685-109">Complete</span></span>](#complete) | <span data-ttu-id="24685-110">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="24685-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="24685-111">Parte</span><span class="sxs-lookup"><span data-stu-id="24685-111">Members</span></span>

#### <span data-ttu-id="24685-112">Concluída</span><span class="sxs-lookup"><span data-stu-id="24685-112">Complete</span></span> 

<span data-ttu-id="24685-113">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="24685-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="24685-114">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="24685-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="24685-115">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="24685-115">Complete should only be called once for each deferral taken.</span></span>

