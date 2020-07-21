---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 135289994bdfe5481018c479b7a1d9c372ecb256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885104"
---
# <span data-ttu-id="4b192-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="4b192-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="4b192-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4b192-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4b192-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4b192-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4b192-107">Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="4b192-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="4b192-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="4b192-108">Summary</span></span>

 <span data-ttu-id="4b192-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4b192-109">Members</span></span>                        | <span data-ttu-id="4b192-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="4b192-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4b192-111">Concluída</span><span class="sxs-lookup"><span data-stu-id="4b192-111">Complete</span></span>](#complete) | <span data-ttu-id="4b192-112">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="4b192-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="4b192-113">Parte</span><span class="sxs-lookup"><span data-stu-id="4b192-113">Members</span></span>

#### <span data-ttu-id="4b192-114">Concluída</span><span class="sxs-lookup"><span data-stu-id="4b192-114">Complete</span></span> 

<span data-ttu-id="4b192-115">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="4b192-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="4b192-116">public void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="4b192-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="4b192-117">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="4b192-117">Complete should only be called once for each deferral taken.</span></span>

