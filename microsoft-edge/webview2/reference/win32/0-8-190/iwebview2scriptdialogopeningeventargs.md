---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 867a8f3656b04a566708fc6fc1a24e80b967c1e2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652368"
---
# <span data-ttu-id="10901-104">interface IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="10901-104">interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="10901-105">Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="10901-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="10901-106">Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.</span><span class="sxs-lookup"><span data-stu-id="10901-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="10901-107">Argumentos de evento para o evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="10901-107">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="10901-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="10901-108">Summary</span></span>

 <span data-ttu-id="10901-109">Parte</span><span class="sxs-lookup"><span data-stu-id="10901-109">Members</span></span>                        | <span data-ttu-id="10901-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="10901-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10901-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10901-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="10901-112">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="10901-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="10901-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="10901-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="10901-114">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10901-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="10901-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="10901-115">get_Message</span></span>](#get_message) | <span data-ttu-id="10901-116">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="10901-116">The message of the dialog box.</span></span>
[<span data-ttu-id="10901-117">Aceitar</span><span class="sxs-lookup"><span data-stu-id="10901-117">Accept</span></span>](#accept) | <span data-ttu-id="10901-118">O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="10901-118">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="10901-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="10901-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="10901-120">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10901-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="10901-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="10901-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="10901-122">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="10901-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="10901-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="10901-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="10901-124">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="10901-124">Set the ResultText property.</span></span>
[<span data-ttu-id="10901-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="10901-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="10901-126">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="10901-126">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="10901-127">Parte</span><span class="sxs-lookup"><span data-stu-id="10901-127">Members</span></span>

#### <span data-ttu-id="10901-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10901-128">get_Uri</span></span> 

<span data-ttu-id="10901-129">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="10901-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="10901-130">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="10901-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="10901-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="10901-131">get_Kind</span></span> 

<span data-ttu-id="10901-132">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10901-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="10901-133">[get_Kind](#get_kind)público HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="10901-133">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="10901-134">get_Message</span><span class="sxs-lookup"><span data-stu-id="10901-134">get_Message</span></span> 

<span data-ttu-id="10901-135">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="10901-135">The message of the dialog box.</span></span>

> <span data-ttu-id="10901-136">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="10901-136">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="10901-137">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt.</span><span class="sxs-lookup"><span data-stu-id="10901-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="10901-138">Aceitar</span><span class="sxs-lookup"><span data-stu-id="10901-138">Accept</span></span> 

<span data-ttu-id="10901-139">O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="10901-139">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="10901-140">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="10901-140">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="10901-141">De JavaScript isso significa que a função Confirm retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="10901-141">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="10901-142">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="10901-142">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="10901-143">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="10901-143">get_DefaultText</span></span> 

<span data-ttu-id="10901-144">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10901-144">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="10901-145">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="10901-145">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="10901-146">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="10901-146">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="10901-147">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="10901-147">get_ResultText</span></span> 

<span data-ttu-id="10901-148">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="10901-148">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="10901-149">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="10901-149">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="10901-150">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="10901-150">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="10901-151">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="10901-151">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="10901-152">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="10901-152">put_ResultText</span></span> 

<span data-ttu-id="10901-153">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="10901-153">Set the ResultText property.</span></span>

> <span data-ttu-id="10901-154">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="10901-154">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="10901-155">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="10901-155">GetDeferral</span></span> 

<span data-ttu-id="10901-156">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="10901-156">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="10901-157">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="10901-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="10901-158">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="10901-158">You can use this to complete the event at a later time.</span></span>

