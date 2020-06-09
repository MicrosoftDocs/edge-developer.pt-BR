---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 33450805c7f5117806feb1fb561cd7e0c364f00e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698096"
---
# <span data-ttu-id="193e6-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="193e6-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="193e6-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="193e6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="193e6-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="193e6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="193e6-107">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="193e6-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="193e6-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="193e6-108">Summary</span></span>

 <span data-ttu-id="193e6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="193e6-109">Members</span></span>                        | <span data-ttu-id="193e6-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="193e6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="193e6-111">Aceitar</span><span class="sxs-lookup"><span data-stu-id="193e6-111">Accept</span></span>](#accept) | <span data-ttu-id="193e6-112">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="193e6-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="193e6-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="193e6-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="193e6-114">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="193e6-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="193e6-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="193e6-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="193e6-116">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="193e6-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="193e6-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="193e6-117">get_Message</span></span>](#get_message) | <span data-ttu-id="193e6-118">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="193e6-118">The message of the dialog box.</span></span>
[<span data-ttu-id="193e6-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="193e6-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="193e6-120">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="193e6-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="193e6-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="193e6-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="193e6-122">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="193e6-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="193e6-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="193e6-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="193e6-124">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="193e6-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="193e6-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="193e6-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="193e6-126">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="193e6-126">Set the ResultText property.</span></span>

## <span data-ttu-id="193e6-127">Parte</span><span class="sxs-lookup"><span data-stu-id="193e6-127">Members</span></span>

#### <span data-ttu-id="193e6-128">Aceitar</span><span class="sxs-lookup"><span data-stu-id="193e6-128">Accept</span></span> 

<span data-ttu-id="193e6-129">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="193e6-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="193e6-130">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="193e6-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="193e6-131">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="193e6-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="193e6-132">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="193e6-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="193e6-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="193e6-133">get_DefaultText</span></span> 

<span data-ttu-id="193e6-134">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="193e6-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="193e6-135">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="193e6-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="193e6-136">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="193e6-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="193e6-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="193e6-137">get_Kind</span></span> 

<span data-ttu-id="193e6-138">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="193e6-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="193e6-139">[get_Kind](#get_kind)público HRESULT (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="193e6-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="193e6-140">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="193e6-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="193e6-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="193e6-141">get_Message</span></span> 

<span data-ttu-id="193e6-142">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="193e6-142">The message of the dialog box.</span></span>

> <span data-ttu-id="193e6-143">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="193e6-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="193e6-144">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="193e6-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="193e6-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="193e6-145">get_ResultText</span></span> 

<span data-ttu-id="193e6-146">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="193e6-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="193e6-147">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="193e6-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="193e6-148">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="193e6-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="193e6-149">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="193e6-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="193e6-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="193e6-150">get_Uri</span></span> 

<span data-ttu-id="193e6-151">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="193e6-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="193e6-152">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="193e6-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="193e6-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="193e6-153">GetDeferral</span></span> 

<span data-ttu-id="193e6-154">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="193e6-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="193e6-155">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="193e6-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="193e6-156">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="193e6-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="193e6-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="193e6-157">put_ResultText</span></span> 

<span data-ttu-id="193e6-158">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="193e6-158">Set the ResultText property.</span></span>

> <span data-ttu-id="193e6-159">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="193e6-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

