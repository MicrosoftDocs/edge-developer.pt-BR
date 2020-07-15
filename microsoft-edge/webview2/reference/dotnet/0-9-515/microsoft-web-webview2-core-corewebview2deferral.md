---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 4df74c4a645b6bfa17228860f627910d374e19c4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878719"
---
# <span data-ttu-id="ebbf8-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="ebbf8-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="ebbf8-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="ebbf8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="ebbf8-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="ebbf8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="ebbf8-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ebbf8-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ebbf8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ebbf8-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ebbf8-109">Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="ebbf8-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ebbf8-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="ebbf8-110">Summary</span></span>

 <span data-ttu-id="ebbf8-111">Parte</span><span class="sxs-lookup"><span data-stu-id="ebbf8-111">Members</span></span>                        | <span data-ttu-id="ebbf8-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="ebbf8-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ebbf8-113">Concluída</span><span class="sxs-lookup"><span data-stu-id="ebbf8-113">Complete</span></span>](#complete) | <span data-ttu-id="ebbf8-114">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="ebbf8-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ebbf8-115">Parte</span><span class="sxs-lookup"><span data-stu-id="ebbf8-115">Members</span></span>

#### <span data-ttu-id="ebbf8-116">Concluída</span><span class="sxs-lookup"><span data-stu-id="ebbf8-116">Complete</span></span> 

<span data-ttu-id="ebbf8-117">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="ebbf8-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ebbf8-118">public void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ebbf8-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="ebbf8-119">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="ebbf8-119">Complete should only be called once for each deferral taken.</span></span>

