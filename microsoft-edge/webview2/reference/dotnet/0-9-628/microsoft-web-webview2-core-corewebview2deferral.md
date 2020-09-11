---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Deferral
ms.openlocfilehash: dcefefd37167b6ff78f2d994f84af6c707423bb4
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011514"
---
# <span data-ttu-id="ea6c1-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="ea6c1-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="ea6c1-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ea6c1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ea6c1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ea6c1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ea6c1-107">Essa classe é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.</span><span class="sxs-lookup"><span data-stu-id="ea6c1-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ea6c1-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="ea6c1-108">Summary</span></span>

 <span data-ttu-id="ea6c1-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ea6c1-109">Members</span></span>                        | <span data-ttu-id="ea6c1-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="ea6c1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea6c1-111">Concluída</span><span class="sxs-lookup"><span data-stu-id="ea6c1-111">Complete</span></span>](#complete) | <span data-ttu-id="ea6c1-112">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="ea6c1-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ea6c1-113">Parte</span><span class="sxs-lookup"><span data-stu-id="ea6c1-113">Members</span></span>

#### <span data-ttu-id="ea6c1-114">Concluída</span><span class="sxs-lookup"><span data-stu-id="ea6c1-114">Complete</span></span> 

<span data-ttu-id="ea6c1-115">Conclui o evento adiado associado.</span><span class="sxs-lookup"><span data-stu-id="ea6c1-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ea6c1-116">public void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ea6c1-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="ea6c1-117">Concluir só deve ser chamado uma vez para cada adiamento tirado.</span><span class="sxs-lookup"><span data-stu-id="ea6c1-117">Complete should only be called once for each deferral taken.</span></span>

