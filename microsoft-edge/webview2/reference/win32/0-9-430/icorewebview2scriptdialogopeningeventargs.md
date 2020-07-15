---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: dfd3383318daf94e8060ba62ef1511c9944efe54
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880210"
---
# <span data-ttu-id="9a37e-104">0.9.430-ICoreWebView2ScriptDialogOpeningEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="9a37e-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9a37e-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9a37e-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9a37e-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="9a37e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="9a37e-107">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="9a37e-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="9a37e-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="9a37e-108">Summary</span></span>

 <span data-ttu-id="9a37e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9a37e-109">Members</span></span>                        | <span data-ttu-id="9a37e-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="9a37e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9a37e-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9a37e-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="9a37e-112">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9a37e-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="9a37e-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="9a37e-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="9a37e-114">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9a37e-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="9a37e-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="9a37e-115">get_Message</span></span>](#get_message) | <span data-ttu-id="9a37e-116">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9a37e-116">The message of the dialog box.</span></span>
[<span data-ttu-id="9a37e-117">Aceitar</span><span class="sxs-lookup"><span data-stu-id="9a37e-117">Accept</span></span>](#accept) | <span data-ttu-id="9a37e-118">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="9a37e-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="9a37e-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="9a37e-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="9a37e-120">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9a37e-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="9a37e-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="9a37e-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="9a37e-122">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="9a37e-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="9a37e-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="9a37e-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="9a37e-124">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="9a37e-124">Set the ResultText property.</span></span>
[<span data-ttu-id="9a37e-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9a37e-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9a37e-126">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="9a37e-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="9a37e-127">Parte</span><span class="sxs-lookup"><span data-stu-id="9a37e-127">Members</span></span>

#### <span data-ttu-id="9a37e-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="9a37e-128">get_Uri</span></span> 

<span data-ttu-id="9a37e-129">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9a37e-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="9a37e-130">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="9a37e-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="9a37e-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="9a37e-131">get_Kind</span></span> 

<span data-ttu-id="9a37e-132">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9a37e-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="9a37e-133">[get_Kind](#get_kind)público HRESULT (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="9a37e-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="9a37e-134">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="9a37e-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="9a37e-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="9a37e-135">get_Message</span></span> 

<span data-ttu-id="9a37e-136">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9a37e-136">The message of the dialog box.</span></span>

> <span data-ttu-id="9a37e-137">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="9a37e-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="9a37e-138">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="9a37e-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="9a37e-139">Aceitar</span><span class="sxs-lookup"><span data-stu-id="9a37e-139">Accept</span></span> 

<span data-ttu-id="9a37e-140">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="9a37e-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="9a37e-141">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="9a37e-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="9a37e-142">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="9a37e-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="9a37e-143">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9a37e-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="9a37e-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="9a37e-144">get_DefaultText</span></span> 

<span data-ttu-id="9a37e-145">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9a37e-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="9a37e-146">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="9a37e-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="9a37e-147">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="9a37e-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="9a37e-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="9a37e-148">get_ResultText</span></span> 

<span data-ttu-id="9a37e-149">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="9a37e-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="9a37e-150">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="9a37e-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="9a37e-151">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="9a37e-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="9a37e-152">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="9a37e-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="9a37e-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="9a37e-153">put_ResultText</span></span> 

<span data-ttu-id="9a37e-154">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="9a37e-154">Set the ResultText property.</span></span>

> <span data-ttu-id="9a37e-155">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="9a37e-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="9a37e-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9a37e-156">GetDeferral</span></span> 

<span data-ttu-id="9a37e-157">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="9a37e-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="9a37e-158">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="9a37e-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="9a37e-159">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="9a37e-159">You can use this to complete the event at a later time.</span></span>

