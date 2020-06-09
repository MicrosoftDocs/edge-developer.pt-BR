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
ms.openlocfilehash: 212e515c07446fefefc91292595f15fe655b46e5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698040"
---
# <span data-ttu-id="b5e15-104">interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="b5e15-104">interface ICoreWebView2EnvironmentOptions</span></span> 

> [!NOTE]
> <span data-ttu-id="b5e15-105">Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b5e15-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b5e15-106">Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.</span><span class="sxs-lookup"><span data-stu-id="b5e15-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="b5e15-107">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="b5e15-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="b5e15-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="b5e15-108">Summary</span></span>

 <span data-ttu-id="b5e15-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b5e15-109">Members</span></span>                        | <span data-ttu-id="b5e15-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="b5e15-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b5e15-111">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b5e15-111">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="b5e15-112">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="b5e15-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="b5e15-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="b5e15-113">get_Language</span></span>](#get_language) | <span data-ttu-id="b5e15-114">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="b5e15-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="b5e15-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b5e15-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="b5e15-116">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b5e15-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="b5e15-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b5e15-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="b5e15-118">Defina a propriedade AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="b5e15-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="b5e15-119">put_Language</span><span class="sxs-lookup"><span data-stu-id="b5e15-119">put_Language</span></span>](#put_language) | <span data-ttu-id="b5e15-120">Defina a propriedade Language.</span><span class="sxs-lookup"><span data-stu-id="b5e15-120">Set the Language property.</span></span>
[<span data-ttu-id="b5e15-121">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b5e15-121">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="b5e15-122">Defina o TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="b5e15-122">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="b5e15-123">Uma implementação padrão é fornecida em WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="b5e15-123">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="b5e15-124">Parte</span><span class="sxs-lookup"><span data-stu-id="b5e15-124">Members</span></span>

#### <span data-ttu-id="b5e15-125">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b5e15-125">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="b5e15-126">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="b5e15-126">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="b5e15-127">[get_AdditionalBrowserArguments](#get_additionalbrowserarguments)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b5e15-127">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="b5e15-128">Eles serão passados para o processo do navegador como parte da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b5e15-128">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="b5e15-129">Consulte [executar Chromium com sinalizadores](https://aka.ms/RunChromiumWithFlags) para obter mais informações sobre as opções de linha de comando para o processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="b5e15-129">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="b5e15-130">Se o aplicativo for iniciado com uma linha de comando Alternar `--edge-webview-switches=xxx` o valor dessa opção (xxx no exemplo acima) também será acrescentado à linha de comando do processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="b5e15-130">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="b5e15-131">Determinadas opções `--user-data-dir` , como são internas e importantes para o WebView.</span><span class="sxs-lookup"><span data-stu-id="b5e15-131">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="b5e15-132">Essas opções serão ignoradas, mesmo que especificado.</span><span class="sxs-lookup"><span data-stu-id="b5e15-132">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="b5e15-133">Se as mesmas opções forem especificadas várias vezes, o último WINS.</span><span class="sxs-lookup"><span data-stu-id="b5e15-133">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="b5e15-134">Não há nenhuma tentativa de mesclar os valores diferentes da mesma opção, exceto para recursos desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="b5e15-134">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="b5e15-135">Os recursos especificados por `--enable-features` e `--disable-features` serão mesclados com uma lógica simples: os recursos serão a União dos recursos e recursos internos especificados e, se um recurso estiver desabilitado, ele será removido da lista de recursos habilitados.</span><span class="sxs-lookup"><span data-stu-id="b5e15-135">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="b5e15-136">O valor da linha de comando do processo de aplicativo é `--edge-webview-switches` processado após o parâmetro additionalBrowserArguments ser processado.</span><span class="sxs-lookup"><span data-stu-id="b5e15-136">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="b5e15-137">Certos recursos são desabilitados internamente e não podem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="b5e15-137">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="b5e15-138">Se a análise falhar para as opções especificadas, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="b5e15-138">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="b5e15-139">Padrão é executar o processo do navegador sem sinalizadores extras.</span><span class="sxs-lookup"><span data-stu-id="b5e15-139">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="b5e15-140">get_Language</span><span class="sxs-lookup"><span data-stu-id="b5e15-140">get_Language</span></span> 

<span data-ttu-id="b5e15-141">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="b5e15-141">The default language that WebView will run with.</span></span>

> <span data-ttu-id="b5e15-142">[get_Language](#get_language)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b5e15-142">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="b5e15-143">Ele se aplica a UIs do navegador, como menus de contexto e caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b5e15-143">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="b5e15-144">Ele também se aplica ao cabeçalho HTTP Accept-Languages que o WebView envia para sites da Web.</span><span class="sxs-lookup"><span data-stu-id="b5e15-144">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="b5e15-145">Ele está no formato de `language[-country]` onde `language` está o código de duas letras da ISO 639 e `country` é o código de duas letras da ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="b5e15-145">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="b5e15-146">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b5e15-146">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="b5e15-147">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b5e15-147">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="b5e15-148">[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b5e15-148">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="b5e15-149">Esse padrão é o Edge WebView2 versão do tempo de execução que corresponde à versão do SDK que o aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="b5e15-149">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="b5e15-150">O formato desse valor é o mesmo que o formato da propriedade BrowserVersionString e outros valores BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="b5e15-150">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="b5e15-151">Somente a parte de versão do valor BrowserVersion é respeitada.</span><span class="sxs-lookup"><span data-stu-id="b5e15-151">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="b5e15-152">O sufixo do canal, se existir, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="b5e15-152">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="b5e15-153">A versão do Edge WebView2 os binários do tempo de execução realmente usados podem ser diferentes do TargetCompatibleBrowserVersion especificado.</span><span class="sxs-lookup"><span data-stu-id="b5e15-153">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="b5e15-154">Eles são garantidos apenas como compatíveis.</span><span class="sxs-lookup"><span data-stu-id="b5e15-154">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="b5e15-155">Você pode verificar a versão real na propriedade BrowserVersionString no ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="b5e15-155">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="b5e15-156">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="b5e15-156">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="b5e15-157">Defina a propriedade AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="b5e15-157">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="b5e15-158">Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b5e15-158">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="b5e15-159">put_Language</span><span class="sxs-lookup"><span data-stu-id="b5e15-159">put_Language</span></span> 

<span data-ttu-id="b5e15-160">Defina a propriedade Language.</span><span class="sxs-lookup"><span data-stu-id="b5e15-160">Set the Language property.</span></span>

> <span data-ttu-id="b5e15-161">Public HRESULT [put_Language](#put_language)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b5e15-161">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="b5e15-162">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="b5e15-162">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="b5e15-163">Defina o TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="b5e15-163">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="b5e15-164">Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b5e15-164">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

