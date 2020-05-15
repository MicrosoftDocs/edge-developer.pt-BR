---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8ed1a10a65a07fc359deea18b8aadd4df3a7b055
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652779"
---
# <span data-ttu-id="e1ef4-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="e1ef4-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e1ef4-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e1ef4-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="e1ef4-107">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="e1ef4-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="e1ef4-108">Summary</span></span>

 <span data-ttu-id="e1ef4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e1ef4-109">Members</span></span>                        | <span data-ttu-id="e1ef4-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="e1ef4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1ef4-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e1ef4-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e1ef4-112">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="e1ef4-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="e1ef4-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="e1ef4-114">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="e1ef4-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="e1ef4-115">get_Message</span></span>](#get_message) | <span data-ttu-id="e1ef4-116">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-116">The message of the dialog box.</span></span>
[<span data-ttu-id="e1ef4-117">Aceitar</span><span class="sxs-lookup"><span data-stu-id="e1ef4-117">Accept</span></span>](#accept) | <span data-ttu-id="e1ef4-118">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="e1ef4-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="e1ef4-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="e1ef4-120">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="e1ef4-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="e1ef4-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="e1ef4-122">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="e1ef4-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="e1ef4-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="e1ef4-124">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-124">Set the ResultText property.</span></span>
[<span data-ttu-id="e1ef4-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e1ef4-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e1ef4-126">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ef4-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="e1ef4-127">Parte</span><span class="sxs-lookup"><span data-stu-id="e1ef4-127">Members</span></span>

#### <span data-ttu-id="e1ef4-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e1ef4-128">get_Uri</span></span> 

<span data-ttu-id="e1ef4-129">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="e1ef4-130">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e1ef4-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="e1ef4-131">get_Kind</span></span> 

<span data-ttu-id="e1ef4-132">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="e1ef4-133">[get_Kind](#get_kind)público HRESULT (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="e1ef4-134">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="e1ef4-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="e1ef4-135">get_Message</span></span> 

<span data-ttu-id="e1ef4-136">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-136">The message of the dialog box.</span></span>

> <span data-ttu-id="e1ef4-137">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="e1ef4-138">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="e1ef4-139">Aceitar</span><span class="sxs-lookup"><span data-stu-id="e1ef4-139">Accept</span></span> 

<span data-ttu-id="e1ef4-140">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="e1ef4-141">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="e1ef4-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="e1ef4-142">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="e1ef4-143">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="e1ef4-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="e1ef4-144">get_DefaultText</span></span> 

<span data-ttu-id="e1ef4-145">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="e1ef4-146">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="e1ef4-147">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="e1ef4-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="e1ef4-148">get_ResultText</span></span> 

<span data-ttu-id="e1ef4-149">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="e1ef4-150">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="e1ef4-151">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="e1ef4-152">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="e1ef4-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="e1ef4-153">put_ResultText</span></span> 

<span data-ttu-id="e1ef4-154">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-154">Set the ResultText property.</span></span>

> <span data-ttu-id="e1ef4-155">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="e1ef4-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e1ef4-156">GetDeferral</span></span> 

<span data-ttu-id="e1ef4-157">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ef4-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="e1ef4-158">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="e1ef4-159">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-159">You can use this to complete the event at a later time.</span></span>

