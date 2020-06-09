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
ms.openlocfilehash: 1359e9472455acf2949cc329de4280ad970a3b68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697305"
---
# <span data-ttu-id="1c985-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="1c985-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="1c985-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1c985-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1c985-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="1c985-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="1c985-107">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1c985-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1c985-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="1c985-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1c985-109">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="1c985-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="1c985-110">Resumo</span><span class="sxs-lookup"><span data-stu-id="1c985-110">Summary</span></span>

 <span data-ttu-id="1c985-111">Parte</span><span class="sxs-lookup"><span data-stu-id="1c985-111">Members</span></span>                        | <span data-ttu-id="1c985-112">Descrições</span><span class="sxs-lookup"><span data-stu-id="1c985-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1c985-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="1c985-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="1c985-114">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1c985-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="1c985-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c985-115">Kind</span></span>](#kind) | <span data-ttu-id="1c985-116">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1c985-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="1c985-117">Mensagem</span><span class="sxs-lookup"><span data-stu-id="1c985-117">Message</span></span>](#message) | <span data-ttu-id="1c985-118">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1c985-118">The message of the dialog box.</span></span>
[<span data-ttu-id="1c985-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="1c985-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="1c985-120">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="1c985-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="1c985-121">Uri</span><span class="sxs-lookup"><span data-stu-id="1c985-121">Uri</span></span>](#uri) | <span data-ttu-id="1c985-122">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1c985-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="1c985-123">Aceitar</span><span class="sxs-lookup"><span data-stu-id="1c985-123">Accept</span></span>](#accept) | <span data-ttu-id="1c985-124">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="1c985-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="1c985-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1c985-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="1c985-126">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="1c985-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="1c985-127">Parte</span><span class="sxs-lookup"><span data-stu-id="1c985-127">Members</span></span>

#### <span data-ttu-id="1c985-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="1c985-128">DefaultText</span></span> 

<span data-ttu-id="1c985-129">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1c985-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="1c985-130">Cadeia de caracteres de [texto](#defaulttext) público</span><span class="sxs-lookup"><span data-stu-id="1c985-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="1c985-131">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="1c985-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="1c985-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c985-132">Kind</span></span> 

<span data-ttu-id="1c985-133">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1c985-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="1c985-134">[tipo](#kind) de CoreWebView2ScriptDialogKind público</span><span class="sxs-lookup"><span data-stu-id="1c985-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="1c985-135">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="1c985-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="1c985-136">Mensagem</span><span class="sxs-lookup"><span data-stu-id="1c985-136">Message</span></span> 

<span data-ttu-id="1c985-137">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1c985-137">The message of the dialog box.</span></span>

> <span data-ttu-id="1c985-138">[mensagem](#message) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="1c985-138">public string [Message](#message)</span></span>

<span data-ttu-id="1c985-139">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="1c985-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="1c985-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="1c985-140">ResultText</span></span> 

<span data-ttu-id="1c985-141">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="1c985-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="1c985-142">Cadeia de caracteres pública [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="1c985-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="1c985-143">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="1c985-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="1c985-144">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="1c985-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="1c985-145">Uri</span><span class="sxs-lookup"><span data-stu-id="1c985-145">Uri</span></span> 

<span data-ttu-id="1c985-146">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1c985-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="1c985-147">[URI](#uri) da cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="1c985-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="1c985-148">Aceitar</span><span class="sxs-lookup"><span data-stu-id="1c985-148">Accept</span></span> 

<span data-ttu-id="1c985-149">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="1c985-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="1c985-150">[aceitação](#accept)de void público ()</span><span class="sxs-lookup"><span data-stu-id="1c985-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="1c985-151">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="1c985-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="1c985-152">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1c985-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="1c985-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="1c985-153">GetDeferral</span></span> 

<span data-ttu-id="1c985-154">Getadiamento pode ser chamado para retornar um objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="1c985-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="1c985-155">Public CoreWebView2Deferral [getadiamento](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="1c985-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="1c985-156">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="1c985-156">You can use this to complete the event at a later time.</span></span>

