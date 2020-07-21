---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: cd8f96787d289ab0fe649244ce665445efdbcecf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884040"
---
# <span data-ttu-id="ec3f0-104">0.9.430-ICoreWebView2ScriptDialogOpeningEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="ec3f0-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="ec3f0-105">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="ec3f0-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ec3f0-106">Summary</span></span>

 <span data-ttu-id="ec3f0-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ec3f0-107">Members</span></span>                        | <span data-ttu-id="ec3f0-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ec3f0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec3f0-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ec3f0-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ec3f0-110">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="ec3f0-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="ec3f0-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="ec3f0-112">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="ec3f0-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="ec3f0-113">get_Message</span></span>](#get_message) | <span data-ttu-id="ec3f0-114">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-114">The message of the dialog box.</span></span>
[<span data-ttu-id="ec3f0-115">Aceitar</span><span class="sxs-lookup"><span data-stu-id="ec3f0-115">Accept</span></span>](#accept) | <span data-ttu-id="ec3f0-116">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-116">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="ec3f0-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="ec3f0-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="ec3f0-118">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="ec3f0-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="ec3f0-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="ec3f0-120">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="ec3f0-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="ec3f0-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="ec3f0-122">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-122">Set the ResultText property.</span></span>
[<span data-ttu-id="ec3f0-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ec3f0-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ec3f0-124">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3f0-124">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="ec3f0-125">Parte</span><span class="sxs-lookup"><span data-stu-id="ec3f0-125">Members</span></span>

#### <span data-ttu-id="ec3f0-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ec3f0-126">get_Uri</span></span> 

<span data-ttu-id="ec3f0-127">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="ec3f0-128">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ec3f0-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="ec3f0-129">get_Kind</span></span> 

<span data-ttu-id="ec3f0-130">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="ec3f0-131">[get_Kind](#get_kind)público HRESULT (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-131">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="ec3f0-132">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-132">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="ec3f0-133">get_Message</span><span class="sxs-lookup"><span data-stu-id="ec3f0-133">get_Message</span></span> 

<span data-ttu-id="ec3f0-134">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-134">The message of the dialog box.</span></span>

> <span data-ttu-id="ec3f0-135">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-135">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="ec3f0-136">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-136">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="ec3f0-137">Aceitar</span><span class="sxs-lookup"><span data-stu-id="ec3f0-137">Accept</span></span> 

<span data-ttu-id="ec3f0-138">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-138">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="ec3f0-139">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="ec3f0-139">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="ec3f0-140">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-140">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="ec3f0-141">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-141">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="ec3f0-142">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="ec3f0-142">get_DefaultText</span></span> 

<span data-ttu-id="ec3f0-143">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-143">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="ec3f0-144">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-144">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="ec3f0-145">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-145">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="ec3f0-146">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="ec3f0-146">get_ResultText</span></span> 

<span data-ttu-id="ec3f0-147">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-147">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="ec3f0-148">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-148">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="ec3f0-149">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-149">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="ec3f0-150">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-150">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="ec3f0-151">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="ec3f0-151">put_ResultText</span></span> 

<span data-ttu-id="ec3f0-152">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-152">Set the ResultText property.</span></span>

> <span data-ttu-id="ec3f0-153">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-153">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="ec3f0-154">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ec3f0-154">GetDeferral</span></span> 

<span data-ttu-id="ec3f0-155">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="ec3f0-155">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="ec3f0-156">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="ec3f0-156">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="ec3f0-157">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ec3f0-157">You can use this to complete the event at a later time.</span></span>

