---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2Deferral
ms.openlocfilehash: 533aefe8b14ae3cabfddd32cb588014067bfdd42
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010282"
---
# <span data-ttu-id="5ebaf-104">0.9.579-ICoreWebView2Deferral de interface</span><span class="sxs-lookup"><span data-stu-id="5ebaf-104">0.9.579 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="5ebaf-105">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="5ebaf-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="5ebaf-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5ebaf-106">Summary</span></span>

 <span data-ttu-id="5ebaf-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5ebaf-107">Members</span></span>                        | <span data-ttu-id="5ebaf-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="5ebaf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5ebaf-109">Concluída</span><span class="sxs-lookup"><span data-stu-id="5ebaf-109">Complete</span></span>](#complete) | <span data-ttu-id="5ebaf-110">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="5ebaf-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="5ebaf-111">Parte</span><span class="sxs-lookup"><span data-stu-id="5ebaf-111">Members</span></span>

#### <span data-ttu-id="5ebaf-112">Concluída</span><span class="sxs-lookup"><span data-stu-id="5ebaf-112">Complete</span></span> 

<span data-ttu-id="5ebaf-113">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="5ebaf-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="5ebaf-114">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="5ebaf-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="5ebaf-115">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="5ebaf-115">Complete should only be called once for each deferral taken.</span></span>

