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
ms.openlocfilehash: fec7fd7399222d8223d1022cd1e528bc9ed0d161
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652664"
---
# <span data-ttu-id="00be7-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="00be7-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="00be7-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="00be7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="00be7-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="00be7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="00be7-107">Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="00be7-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="00be7-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="00be7-108">Summary</span></span>

 <span data-ttu-id="00be7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="00be7-109">Members</span></span>                        | <span data-ttu-id="00be7-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="00be7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="00be7-111">Concluída</span><span class="sxs-lookup"><span data-stu-id="00be7-111">Complete</span></span>](#complete) | <span data-ttu-id="00be7-112">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="00be7-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="00be7-113">Parte</span><span class="sxs-lookup"><span data-stu-id="00be7-113">Members</span></span>

#### <span data-ttu-id="00be7-114">Concluída</span><span class="sxs-lookup"><span data-stu-id="00be7-114">Complete</span></span> 

<span data-ttu-id="00be7-115">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="00be7-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="00be7-116">public void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="00be7-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="00be7-117">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="00be7-117">Complete should only be called once for each deferral taken.</span></span>

