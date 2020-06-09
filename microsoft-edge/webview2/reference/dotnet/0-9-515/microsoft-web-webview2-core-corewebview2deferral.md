---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: bf198781d67761e9d6c29ee9c6a274462e92a61d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697669"
---
# <span data-ttu-id="79e87-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="79e87-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="79e87-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="79e87-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="79e87-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="79e87-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="79e87-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="79e87-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="79e87-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="79e87-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="79e87-109">Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="79e87-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="79e87-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="79e87-110">Summary</span></span>

 <span data-ttu-id="79e87-111">Parte</span><span class="sxs-lookup"><span data-stu-id="79e87-111">Members</span></span>                        | <span data-ttu-id="79e87-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="79e87-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="79e87-113">Concluída</span><span class="sxs-lookup"><span data-stu-id="79e87-113">Complete</span></span>](#complete) | <span data-ttu-id="79e87-114">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="79e87-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="79e87-115">Parte</span><span class="sxs-lookup"><span data-stu-id="79e87-115">Members</span></span>

#### <span data-ttu-id="79e87-116">Concluída</span><span class="sxs-lookup"><span data-stu-id="79e87-116">Complete</span></span> 

<span data-ttu-id="79e87-117">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="79e87-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="79e87-118">public void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="79e87-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="79e87-119">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="79e87-119">Complete should only be called once for each deferral taken.</span></span>

