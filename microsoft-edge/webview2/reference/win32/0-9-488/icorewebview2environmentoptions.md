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
ms.openlocfilehash: fcb17996774ac9a3a0ed32810f095c828a8b5c82
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652444"
---
# <span data-ttu-id="ca60e-104">interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="ca60e-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="ca60e-105">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca60e-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="ca60e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="ca60e-106">Summary</span></span>

 <span data-ttu-id="ca60e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="ca60e-107">Members</span></span>                        | <span data-ttu-id="ca60e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="ca60e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca60e-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ca60e-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="ca60e-110">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="ca60e-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="ca60e-111">get_Language</span><span class="sxs-lookup"><span data-stu-id="ca60e-111">get_Language</span></span>](#get_language) | <span data-ttu-id="ca60e-112">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-112">The default language that WebView will run with.</span></span>
[<span data-ttu-id="ca60e-113">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ca60e-113">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="ca60e-114">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="ca60e-114">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="ca60e-115">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ca60e-115">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="ca60e-116">Defina a propriedade AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="ca60e-116">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="ca60e-117">put_Language</span><span class="sxs-lookup"><span data-stu-id="ca60e-117">put_Language</span></span>](#put_language) | <span data-ttu-id="ca60e-118">Defina a propriedade Language.</span><span class="sxs-lookup"><span data-stu-id="ca60e-118">Set the Language property.</span></span>
[<span data-ttu-id="ca60e-119">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ca60e-119">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="ca60e-120">Defina o TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="ca60e-120">Set the TargetCompatibleBrowserVersion.</span></span>

<span data-ttu-id="ca60e-121">Uma implementação padrão é fornecida em WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="ca60e-121">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

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

## <span data-ttu-id="ca60e-122">Parte</span><span class="sxs-lookup"><span data-stu-id="ca60e-122">Members</span></span>

#### <span data-ttu-id="ca60e-123">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ca60e-123">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="ca60e-124">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="ca60e-124">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="ca60e-125">[get_AdditionalBrowserArguments](#get_additionalbrowserarguments)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ca60e-125">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="ca60e-126">Eles serão passados para o processo do navegador como parte da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ca60e-126">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="ca60e-127">Consulte [executar Chromium com sinalizadores](https://aka.ms/RunChromiumWithFlags) para obter mais informações sobre as opções de linha de comando para o processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="ca60e-127">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="ca60e-128">Se o aplicativo for iniciado com uma linha de comando Alternar `--edge-webview-switches=xxx` o valor dessa opção (xxx no exemplo acima) também será acrescentado à linha de comando do processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="ca60e-128">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="ca60e-129">Determinadas opções `--user-data-dir` , como são internas e importantes para o WebView.</span><span class="sxs-lookup"><span data-stu-id="ca60e-129">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="ca60e-130">Essas opções serão ignoradas, mesmo que especificado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-130">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="ca60e-131">Se as mesmas opções forem especificadas várias vezes, o último WINS.</span><span class="sxs-lookup"><span data-stu-id="ca60e-131">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="ca60e-132">Não há nenhuma tentativa de mesclar os valores diferentes da mesma opção, exceto para recursos desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="ca60e-132">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="ca60e-133">Os recursos especificados por `--enable-features` e `--disable-features` serão mesclados com uma lógica simples: os recursos serão a União dos recursos e recursos internos especificados e, se um recurso estiver desabilitado, ele será removido da lista de recursos habilitados.</span><span class="sxs-lookup"><span data-stu-id="ca60e-133">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="ca60e-134">O valor da linha de comando do processo de aplicativo é `--edge-webview-switches` processado após o parâmetro additionalBrowserArguments ser processado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-134">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="ca60e-135">Certos recursos são desabilitados internamente e não podem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="ca60e-135">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="ca60e-136">Se a análise falhar para as opções especificadas, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="ca60e-136">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="ca60e-137">Padrão é executar o processo do navegador sem sinalizadores extras.</span><span class="sxs-lookup"><span data-stu-id="ca60e-137">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="ca60e-138">get_Language</span><span class="sxs-lookup"><span data-stu-id="ca60e-138">get_Language</span></span> 

<span data-ttu-id="ca60e-139">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-139">The default language that WebView will run with.</span></span>

> <span data-ttu-id="ca60e-140">[get_Language](#get_language)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ca60e-140">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="ca60e-141">Ele se aplica a UIs do navegador, como menus de contexto e caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ca60e-141">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="ca60e-142">Ele também se aplica ao cabeçalho HTTP Accept-Languages que o WebView envia para sites da Web.</span><span class="sxs-lookup"><span data-stu-id="ca60e-142">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="ca60e-143">Ele está no formato de `language[-country]` onde `language` está o código de duas letras da ISO 639 e `country` é o código de duas letras da ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="ca60e-143">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="ca60e-144">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ca60e-144">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="ca60e-145">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="ca60e-145">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="ca60e-146">[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="ca60e-146">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="ca60e-147">Esse padrão é o Edge WebView2 versão do tempo de execução que corresponde à versão do SDK que o aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="ca60e-147">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="ca60e-148">O formato desse valor é o mesmo que o formato da propriedade BrowserVersionString e outros valores BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="ca60e-148">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="ca60e-149">Somente a parte de versão do valor BrowserVersion é respeitada.</span><span class="sxs-lookup"><span data-stu-id="ca60e-149">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="ca60e-150">O sufixo do canal, se existir, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-150">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="ca60e-151">A versão do Edge WebView2 os binários do tempo de execução realmente usados podem ser diferentes do TargetCompatibleBrowserVersion especificado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-151">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="ca60e-152">Eles são garantidos apenas como compatíveis.</span><span class="sxs-lookup"><span data-stu-id="ca60e-152">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="ca60e-153">Você pode verificar a versão real na propriedade BrowserVersionString no ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="ca60e-153">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="ca60e-154">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="ca60e-154">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="ca60e-155">Defina a propriedade AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="ca60e-155">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="ca60e-156">Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ca60e-156">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="ca60e-157">put_Language</span><span class="sxs-lookup"><span data-stu-id="ca60e-157">put_Language</span></span> 

<span data-ttu-id="ca60e-158">Defina a propriedade Language.</span><span class="sxs-lookup"><span data-stu-id="ca60e-158">Set the Language property.</span></span>

> <span data-ttu-id="ca60e-159">Public HRESULT [put_Language](#put_language)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ca60e-159">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="ca60e-160">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="ca60e-160">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="ca60e-161">Defina o TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="ca60e-161">Set the TargetCompatibleBrowserVersion.</span></span>

> <span data-ttu-id="ca60e-162">Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ca60e-162">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

