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
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652622"
---
# <span data-ttu-id="af7e1-104">interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="af7e1-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="af7e1-105">Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="af7e1-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="af7e1-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="af7e1-106">Summary</span></span>

 <span data-ttu-id="af7e1-107">Parte</span><span class="sxs-lookup"><span data-stu-id="af7e1-107">Members</span></span>                        | <span data-ttu-id="af7e1-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="af7e1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af7e1-109">Concluída</span><span class="sxs-lookup"><span data-stu-id="af7e1-109">Complete</span></span>](#complete) | <span data-ttu-id="af7e1-110">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="af7e1-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="af7e1-111">Parte</span><span class="sxs-lookup"><span data-stu-id="af7e1-111">Members</span></span>

#### <span data-ttu-id="af7e1-112">Concluída</span><span class="sxs-lookup"><span data-stu-id="af7e1-112">Complete</span></span> 

<span data-ttu-id="af7e1-113">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="af7e1-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="af7e1-114">público HRESULT [concluído](#complete)()</span><span class="sxs-lookup"><span data-stu-id="af7e1-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="af7e1-115">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="af7e1-115">Complete should only be called once for each deferral taken.</span></span>

