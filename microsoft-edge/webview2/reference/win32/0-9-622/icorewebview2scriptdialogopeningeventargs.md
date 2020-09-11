---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: 442bd26caeb78804ceb202b302123b0ee1127f09
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011554"
---
# <span data-ttu-id="c1cdb-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="c1cdb-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="c1cdb-105">Args de evento para o evento ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="c1cdb-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="c1cdb-106">Summary</span></span>

 <span data-ttu-id="c1cdb-107">Parte</span><span class="sxs-lookup"><span data-stu-id="c1cdb-107">Members</span></span>                        | <span data-ttu-id="c1cdb-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="c1cdb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1cdb-109">Aceitar</span><span class="sxs-lookup"><span data-stu-id="c1cdb-109">Accept</span></span>](#accept) | <span data-ttu-id="c1cdb-110">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-110">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="c1cdb-111">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="c1cdb-111">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="c1cdb-112">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="c1cdb-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="c1cdb-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="c1cdb-114">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="c1cdb-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="c1cdb-115">get_Message</span></span>](#get_message) | <span data-ttu-id="c1cdb-116">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-116">The message of the dialog box.</span></span>
[<span data-ttu-id="c1cdb-117">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="c1cdb-117">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="c1cdb-118">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="c1cdb-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c1cdb-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="c1cdb-120">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="c1cdb-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c1cdb-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c1cdb-122">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="c1cdb-122">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="c1cdb-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="c1cdb-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="c1cdb-124">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-124">Set the ResultText property.</span></span>

## <span data-ttu-id="c1cdb-125">Parte</span><span class="sxs-lookup"><span data-stu-id="c1cdb-125">Members</span></span>

#### <span data-ttu-id="c1cdb-126">Aceitar</span><span class="sxs-lookup"><span data-stu-id="c1cdb-126">Accept</span></span> 

<span data-ttu-id="c1cdb-127">O host pode chamá-lo para responder com as caixas de diálogo OK para confirmar, solicitar e beforeunload ou não chamar este método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-127">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="c1cdb-128">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="c1cdb-128">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="c1cdb-129">Em JavaScript, isso significa que a função Confirm e beforeunload retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-129">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="c1cdb-130">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-130">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="c1cdb-131">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="c1cdb-131">get_DefaultText</span></span> 

<span data-ttu-id="c1cdb-132">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-132">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="c1cdb-133">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-133">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="c1cdb-134">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-134">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="c1cdb-135">get_Kind</span><span class="sxs-lookup"><span data-stu-id="c1cdb-135">get_Kind</span></span> 

<span data-ttu-id="c1cdb-136">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-136">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="c1cdb-137">[get_Kind](#get_kind)público HRESULT (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-137">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="c1cdb-138">Aceite, confirme, avise ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-138">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="c1cdb-139">get_Message</span><span class="sxs-lookup"><span data-stu-id="c1cdb-139">get_Message</span></span> 

<span data-ttu-id="c1cdb-140">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-140">The message of the dialog box.</span></span>

> <span data-ttu-id="c1cdb-141">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-141">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="c1cdb-142">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt e está vazio para beforeunload.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-142">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="c1cdb-143">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="c1cdb-143">get_ResultText</span></span> 

<span data-ttu-id="c1cdb-144">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-144">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="c1cdb-145">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-145">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="c1cdb-146">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-146">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="c1cdb-147">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-147">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="c1cdb-148">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c1cdb-148">get_Uri</span></span> 

<span data-ttu-id="c1cdb-149">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-149">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="c1cdb-150">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-150">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="c1cdb-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c1cdb-151">GetDeferral</span></span> 

<span data-ttu-id="c1cdb-152">Getadiamento pode ser chamado para retornar um objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="c1cdb-152">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="c1cdb-153">público HRESULT [getadiamento](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c1cdb-154">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-154">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="c1cdb-155">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="c1cdb-155">put_ResultText</span></span> 

<span data-ttu-id="c1cdb-156">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="c1cdb-156">Set the ResultText property.</span></span>

> <span data-ttu-id="c1cdb-157">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="c1cdb-157">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

