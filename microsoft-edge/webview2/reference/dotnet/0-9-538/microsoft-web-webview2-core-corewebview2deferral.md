---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: 77a3540a64c9894f10cb0c03998dafda90e4f15b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878929"
---
# <span data-ttu-id="e455a-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="e455a-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="e455a-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e455a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e455a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e455a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e455a-107">Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="e455a-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="e455a-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e455a-108">Summary</span></span>

 <span data-ttu-id="e455a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e455a-109">Members</span></span>                        | <span data-ttu-id="e455a-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e455a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e455a-111">Concluída</span><span class="sxs-lookup"><span data-stu-id="e455a-111">Complete</span></span>](#complete) | <span data-ttu-id="e455a-112">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="e455a-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="e455a-113">Parte</span><span class="sxs-lookup"><span data-stu-id="e455a-113">Members</span></span>

#### <span data-ttu-id="e455a-114">Concluída</span><span class="sxs-lookup"><span data-stu-id="e455a-114">Complete</span></span> 

<span data-ttu-id="e455a-115">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="e455a-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="e455a-116">public void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="e455a-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="e455a-117">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="e455a-117">Complete should only be called once for each deferral taken.</span></span>

