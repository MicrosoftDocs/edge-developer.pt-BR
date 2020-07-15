---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: cbff39e9393026f51471bdfb3189600e2d7bf109
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879692"
---
# <span data-ttu-id="dcd1b-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="dcd1b-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

<span data-ttu-id="dcd1b-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="dcd1b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="dcd1b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="dcd1b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="dcd1b-107">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="dcd1b-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="dcd1b-108">Summary</span></span>

 <span data-ttu-id="dcd1b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="dcd1b-109">Members</span></span>                        | <span data-ttu-id="dcd1b-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="dcd1b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dcd1b-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="dcd1b-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="dcd1b-112">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="dcd1b-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="dcd1b-113">Kind</span></span>](#kind) | <span data-ttu-id="dcd1b-114">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="dcd1b-115">Mensagem</span><span class="sxs-lookup"><span data-stu-id="dcd1b-115">Message</span></span>](#message) | <span data-ttu-id="dcd1b-116">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-116">The message of the dialog box.</span></span>
[<span data-ttu-id="dcd1b-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="dcd1b-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="dcd1b-118">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="dcd1b-119">Uri</span><span class="sxs-lookup"><span data-stu-id="dcd1b-119">Uri</span></span>](#uri) | <span data-ttu-id="dcd1b-120">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="dcd1b-121">Aceitar</span><span class="sxs-lookup"><span data-stu-id="dcd1b-121">Accept</span></span>](#accept) | <span data-ttu-id="dcd1b-122">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="dcd1b-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="dcd1b-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="dcd1b-124">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="dcd1b-125">Parte</span><span class="sxs-lookup"><span data-stu-id="dcd1b-125">Members</span></span>

#### <span data-ttu-id="dcd1b-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="dcd1b-126">DefaultText</span></span> 

<span data-ttu-id="dcd1b-127">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="dcd1b-128">Cadeia de caracteres de [texto](#defaulttext) público</span><span class="sxs-lookup"><span data-stu-id="dcd1b-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="dcd1b-129">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="dcd1b-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="dcd1b-130">Kind</span></span> 

<span data-ttu-id="dcd1b-131">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="dcd1b-132">[tipo](#kind) de CoreWebView2ScriptDialogKind público</span><span class="sxs-lookup"><span data-stu-id="dcd1b-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="dcd1b-133">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="dcd1b-134">Mensagem</span><span class="sxs-lookup"><span data-stu-id="dcd1b-134">Message</span></span> 

<span data-ttu-id="dcd1b-135">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-135">The message of the dialog box.</span></span>

> <span data-ttu-id="dcd1b-136">[mensagem](#message) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="dcd1b-136">public string [Message](#message)</span></span>

<span data-ttu-id="dcd1b-137">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="dcd1b-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="dcd1b-138">ResultText</span></span> 

<span data-ttu-id="dcd1b-139">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="dcd1b-140">Cadeia de caracteres pública [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="dcd1b-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="dcd1b-141">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="dcd1b-142">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="dcd1b-143">Uri</span><span class="sxs-lookup"><span data-stu-id="dcd1b-143">Uri</span></span> 

<span data-ttu-id="dcd1b-144">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="dcd1b-145">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="dcd1b-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="dcd1b-146">Aceitar</span><span class="sxs-lookup"><span data-stu-id="dcd1b-146">Accept</span></span> 

<span data-ttu-id="dcd1b-147">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="dcd1b-148">[aceitação](#accept)de void público ()</span><span class="sxs-lookup"><span data-stu-id="dcd1b-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="dcd1b-149">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="dcd1b-150">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="dcd1b-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="dcd1b-151">GetDeferral</span></span> 

<span data-ttu-id="dcd1b-152">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="dcd1b-153">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="dcd1b-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="dcd1b-154">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="dcd1b-154">You can use this to complete the event at a later time.</span></span>

