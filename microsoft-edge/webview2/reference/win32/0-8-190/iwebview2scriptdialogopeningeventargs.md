---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885790"
---
# <span data-ttu-id="4626b-104">0.8.355-IWebView2ScriptDialogOpeningEventArgs de interface</span><span class="sxs-lookup"><span data-stu-id="4626b-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="4626b-105">Argumentos de evento para o evento [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="4626b-105">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="4626b-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="4626b-106">Summary</span></span>

 <span data-ttu-id="4626b-107">Parte</span><span class="sxs-lookup"><span data-stu-id="4626b-107">Members</span></span>                        | <span data-ttu-id="4626b-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="4626b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4626b-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4626b-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="4626b-110">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4626b-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="4626b-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="4626b-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="4626b-112">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4626b-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="4626b-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="4626b-113">get_Message</span></span>](#get_message) | <span data-ttu-id="4626b-114">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4626b-114">The message of the dialog box.</span></span>
[<span data-ttu-id="4626b-115">Aceitar</span><span class="sxs-lookup"><span data-stu-id="4626b-115">Accept</span></span>](#accept) | <span data-ttu-id="4626b-116">O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="4626b-116">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="4626b-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="4626b-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="4626b-118">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4626b-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="4626b-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="4626b-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="4626b-120">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="4626b-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="4626b-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="4626b-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="4626b-122">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="4626b-122">Set the ResultText property.</span></span>
[<span data-ttu-id="4626b-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4626b-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4626b-124">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="4626b-124">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="4626b-125">Parte</span><span class="sxs-lookup"><span data-stu-id="4626b-125">Members</span></span>

#### <span data-ttu-id="4626b-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4626b-126">get_Uri</span></span> 

<span data-ttu-id="4626b-127">O URI da página que solicitou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4626b-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="4626b-128">[get_Uri](#get_uri)público HRESULT (URI LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="4626b-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="4626b-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="4626b-129">get_Kind</span></span> 

<span data-ttu-id="4626b-130">O tipo de caixa de diálogo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4626b-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="4626b-131">[get_Kind](#get_kind)público HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND \* Kind)</span><span class="sxs-lookup"><span data-stu-id="4626b-131">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="4626b-132">get_Message</span><span class="sxs-lookup"><span data-stu-id="4626b-132">get_Message</span></span> 

<span data-ttu-id="4626b-133">A mensagem da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4626b-133">The message of the dialog box.</span></span>

> <span data-ttu-id="4626b-134">Public HRESULT [get_Message](#get_message)(mensagem LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="4626b-134">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="4626b-135">Em JavaScript, esse é o primeiro parâmetro passado para Alert, Confirm e prompt.</span><span class="sxs-lookup"><span data-stu-id="4626b-135">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="4626b-136">Aceitar</span><span class="sxs-lookup"><span data-stu-id="4626b-136">Accept</span></span> 

<span data-ttu-id="4626b-137">O host pode chamá-lo para responder com OK para confirmar e solicitar caixas de diálogo ou não chamar esse método para indicar o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="4626b-137">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="4626b-138">público HRESULT [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="4626b-138">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="4626b-139">De JavaScript isso significa que a função Confirm retornará true se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="4626b-139">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="4626b-140">E para a função prompt, ele retornará o valor de ResultText se Accept for chamado e retornará false de outra forma.</span><span class="sxs-lookup"><span data-stu-id="4626b-140">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="4626b-141">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="4626b-141">get_DefaultText</span></span> 

<span data-ttu-id="4626b-142">O segundo parâmetro passado para a caixa de diálogo do prompt JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4626b-142">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="4626b-143">público HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="4626b-143">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="4626b-144">Esse é o valor padrão a ser usado para o resultado da função JavaScript do prompt.</span><span class="sxs-lookup"><span data-stu-id="4626b-144">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="4626b-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="4626b-145">get_ResultText</span></span> 

<span data-ttu-id="4626b-146">O valor de retorno da função do prompt JavaScript se Accept for chamado.</span><span class="sxs-lookup"><span data-stu-id="4626b-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="4626b-147">público HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="4626b-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="4626b-148">Isso é ignorado para tipos de diálogo diferentes de prompt.</span><span class="sxs-lookup"><span data-stu-id="4626b-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="4626b-149">Se aceito não for chamado, esse valor será ignorado e false será retornado do prompt.</span><span class="sxs-lookup"><span data-stu-id="4626b-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="4626b-150">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="4626b-150">put_ResultText</span></span> 

<span data-ttu-id="4626b-151">Defina a propriedade ResultText.</span><span class="sxs-lookup"><span data-stu-id="4626b-151">Set the ResultText property.</span></span>

> <span data-ttu-id="4626b-152">Public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="4626b-152">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="4626b-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4626b-153">GetDeferral</span></span> 

<span data-ttu-id="4626b-154">Getadiamento pode ser chamado para retornar um objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="4626b-154">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="4626b-155">público HRESULT [getadiamento](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* adiamento)</span><span class="sxs-lookup"><span data-stu-id="4626b-155">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="4626b-156">Você pode usá-lo para concluir o evento mais tarde.</span><span class="sxs-lookup"><span data-stu-id="4626b-156">You can use this to complete the event at a later time.</span></span>

