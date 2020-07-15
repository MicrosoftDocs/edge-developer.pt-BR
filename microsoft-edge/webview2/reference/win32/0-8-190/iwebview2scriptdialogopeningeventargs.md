---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 052f380caadf08814cc9364f3ccfbb5251fa7c7e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878194"
---
# <span data-ttu-id="56ae3-104">0.8.355-IWebView2ScriptDialogOpeningEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="56ae3-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="56ae3-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="56ae3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="56ae3-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="56ae3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="56ae3-107">Argumentos de evento para o evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="56ae3-107">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="56ae3-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="56ae3-108">Summary</span></span>

 <span data-ttu-id="56ae3-109">Parte</span><span class="sxs-lookup"><span data-stu-id="56ae3-109">Members</span></span>                        | <span data-ttu-id="56ae3-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="56ae3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56ae3-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="56ae3-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="56ae3-112">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="56ae3-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="56ae3-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="56ae3-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="56ae3-114">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="56ae3-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="56ae3-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="56ae3-115">get_Message</span></span>](#get_message) | <span data-ttu-id="56ae3-116">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="56ae3-116">The message of the dialog box.</span></span>
[<span data-ttu-id="56ae3-117">Aceitar</span><span class="sxs-lookup"><span data-stu-id="56ae3-117">Accept</span></span>](#accept) | <span data-ttu-id="56ae3-118">O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="56ae3-118">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="56ae3-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="56ae3-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="56ae3-120">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="56ae3-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="56ae3-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ae3-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="56ae3-122">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="56ae3-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="56ae3-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ae3-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="56ae3-124">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="56ae3-124">Set the ResultText property.</span></span>
[<span data-ttu-id="56ae3-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="56ae3-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="56ae3-126">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="56ae3-126">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="56ae3-127">Parte</span><span class="sxs-lookup"><span data-stu-id="56ae3-127">Members</span></span>

#### <span data-ttu-id="56ae3-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="56ae3-128">get_Uri</span></span> 

<span data-ttu-id="56ae3-129">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="56ae3-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="56ae3-130">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="56ae3-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="56ae3-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="56ae3-131">get_Kind</span></span> 

<span data-ttu-id="56ae3-132">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="56ae3-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="56ae3-133">[get_Kind](#get_kind)público HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="56ae3-133">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="56ae3-134">get_Message</span><span class="sxs-lookup"><span data-stu-id="56ae3-134">get_Message</span></span> 

<span data-ttu-id="56ae3-135">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="56ae3-135">The message of the dialog box.</span></span>

> <span data-ttu-id="56ae3-136">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="56ae3-136">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="56ae3-137">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt.</span><span class="sxs-lookup"><span data-stu-id="56ae3-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="56ae3-138">Aceitar</span><span class="sxs-lookup"><span data-stu-id="56ae3-138">Accept</span></span> 

<span data-ttu-id="56ae3-139">O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="56ae3-139">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="56ae3-140">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="56ae3-140">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="56ae3-141">De JavaScript isso significa que a função Confirm retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="56ae3-141">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="56ae3-142">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="56ae3-142">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="56ae3-143">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="56ae3-143">get_DefaultText</span></span> 

<span data-ttu-id="56ae3-144">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="56ae3-144">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="56ae3-145">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="56ae3-145">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="56ae3-146">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="56ae3-146">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="56ae3-147">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ae3-147">get_ResultText</span></span> 

<span data-ttu-id="56ae3-148">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="56ae3-148">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="56ae3-149">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="56ae3-149">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="56ae3-150">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="56ae3-150">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="56ae3-151">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="56ae3-151">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="56ae3-152">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="56ae3-152">put_ResultText</span></span> 

<span data-ttu-id="56ae3-153">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="56ae3-153">Set the ResultText property.</span></span>

> <span data-ttu-id="56ae3-154">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="56ae3-154">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="56ae3-155">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="56ae3-155">GetDeferral</span></span> 

<span data-ttu-id="56ae3-156">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="56ae3-156">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="56ae3-157">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="56ae3-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="56ae3-158">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="56ae3-158">You can use this to complete the event at a later time.</span></span>

