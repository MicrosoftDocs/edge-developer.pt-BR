---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2EnvironmentOptions
ms.openlocfilehash: a4e51dc08e2c31664cb77e4e6ee0136bab2f261d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011595"
---
# <span data-ttu-id="7bb1e-104">interface ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="7bb1e-104">interface ICoreWebView2EnvironmentOptions</span></span> 

```
interface ICoreWebView2EnvironmentOptions
  : public IUnknown
```

<span data-ttu-id="7bb1e-105">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-105">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="7bb1e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="7bb1e-106">Summary</span></span>

 <span data-ttu-id="7bb1e-107">Parte</span><span class="sxs-lookup"><span data-stu-id="7bb1e-107">Members</span></span>                        | <span data-ttu-id="7bb1e-108">Descrições</span><span class="sxs-lookup"><span data-stu-id="7bb1e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7bb1e-109">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="7bb1e-109">get_AdditionalBrowserArguments</span></span>](#get_additionalbrowserarguments) | <span data-ttu-id="7bb1e-110">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-110">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="7bb1e-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="7bb1e-111">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#get_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="7bb1e-112">A propriedade AllowSingleSignOnUsingOSPrimaryAccount é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-112">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>
[<span data-ttu-id="7bb1e-113">get_Language</span><span class="sxs-lookup"><span data-stu-id="7bb1e-113">get_Language</span></span>](#get_language) | <span data-ttu-id="7bb1e-114">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="7bb1e-115">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="7bb1e-115">get_TargetCompatibleBrowserVersion</span></span>](#get_targetcompatiblebrowserversion) | <span data-ttu-id="7bb1e-116">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="7bb1e-117">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="7bb1e-117">put_AdditionalBrowserArguments</span></span>](#put_additionalbrowserarguments) | <span data-ttu-id="7bb1e-118">Defina a propriedade AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-118">Set the AdditionalBrowserArguments property.</span></span>
[<span data-ttu-id="7bb1e-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="7bb1e-119">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span>](#put_allowsinglesignonusingosprimaryaccount) | <span data-ttu-id="7bb1e-120">Defina a propriedade AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-120">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>
[<span data-ttu-id="7bb1e-121">put_Language</span><span class="sxs-lookup"><span data-stu-id="7bb1e-121">put_Language</span></span>](#put_language) | <span data-ttu-id="7bb1e-122">Defina a propriedade Language.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-122">Set the Language property.</span></span>
[<span data-ttu-id="7bb1e-123">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="7bb1e-123">put_TargetCompatibleBrowserVersion</span></span>](#put_targetcompatiblebrowserversion) | <span data-ttu-id="7bb1e-124">Defina a propriedade TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-124">Set the TargetCompatibleBrowserVersion property.</span></span>

<span data-ttu-id="7bb1e-125">Uma implementação padrão é fornecida em WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-125">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

```cpp
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    CHECK_FAILURE(options->put_AllowSingleSignOnUsingOSPrimaryAccount(
        m_AADSSOEnabled ? TRUE : FALSE));
    if (!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
```

## <span data-ttu-id="7bb1e-126">Parte</span><span class="sxs-lookup"><span data-stu-id="7bb1e-126">Members</span></span>

#### <span data-ttu-id="7bb1e-127">get_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="7bb1e-127">get_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="7bb1e-128">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-128">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="7bb1e-129">[get_AdditionalBrowserArguments](#get_additionalbrowserarguments)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-129">public HRESULT [get_AdditionalBrowserArguments](#get_additionalbrowserarguments)(LPWSTR \* value)</span></span>

<span data-ttu-id="7bb1e-130">Eles serão passados para o processo do navegador como parte da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-130">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="7bb1e-131">Consulte [executar Chromium com sinalizadores](https://aka.ms/RunChromiumWithFlags) para obter mais informações sobre as opções de linha de comando para o processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-131">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="7bb1e-132">Se o aplicativo for iniciado com uma linha de comando Alternar `--edge-webview-switches=xxx` o valor dessa opção (xxx no exemplo acima) também será acrescentado à linha de comando do processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-132">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="7bb1e-133">Determinadas opções `--user-data-dir` , como são internas e importantes para o WebView.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-133">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="7bb1e-134">Essas opções serão ignoradas, mesmo que especificado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-134">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="7bb1e-135">Se as mesmas opções forem especificadas várias vezes, o último WINS.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-135">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="7bb1e-136">Não há nenhuma tentativa de mesclar os valores diferentes da mesma opção, exceto para recursos desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-136">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="7bb1e-137">Os recursos especificados por `--enable-features` e `--disable-features` serão mesclados com uma lógica simples: os recursos serão a União dos recursos e recursos internos especificados e, se um recurso estiver desabilitado, ele será removido da lista de recursos habilitados.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-137">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="7bb1e-138">O valor da linha de comando do processo de aplicativo é `--edge-webview-switches` processado após o parâmetro additionalBrowserArguments ser processado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-138">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="7bb1e-139">Certos recursos são desabilitados internamente e não podem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-139">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="7bb1e-140">Se a análise falhar para as opções especificadas, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-140">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="7bb1e-141">Padrão é executar o processo do navegador sem sinalizadores extras.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-141">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="7bb1e-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="7bb1e-142">get_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="7bb1e-143">A propriedade AllowSingleSignOnUsingOSPrimaryAccount é usada para habilitar o logon único com recursos do Azure Active Directory (AAD) em WebView usando a conta do Windows conectada e logon único com sites da Web usando a conta da Microsoft associada ao logon na conta do Windows.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-143">The AllowSingleSignOnUsingOSPrimaryAccount property is used to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on with web sites using Microsoft account associated with the login in Windows account.</span></span>

> <span data-ttu-id="7bb1e-144">[get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)público HRESULT (bool \* permitir)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-144">public HRESULT [get_AllowSingleSignOnUsingOSPrimaryAccount](#get_allowsinglesignonusingosprimaryaccount)(BOOL \* allow)</span></span>

<span data-ttu-id="7bb1e-145">O padrão é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-145">Default is disabled.</span></span> <span data-ttu-id="7bb1e-146">Os aplicativos da plataforma universal do Windows também devem declarar o [recurso restrito](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) enterpriseCloudSSO para que o logon único funcione.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-146">Universal Windows Platform apps must also declare enterpriseCloudSSO [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on to work.</span></span>

#### <span data-ttu-id="7bb1e-147">get_Language</span><span class="sxs-lookup"><span data-stu-id="7bb1e-147">get_Language</span></span> 

<span data-ttu-id="7bb1e-148">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-148">The default language that WebView will run with.</span></span>

> <span data-ttu-id="7bb1e-149">[get_Language](#get_language)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-149">public HRESULT [get_Language](#get_language)(LPWSTR \* value)</span></span>

<span data-ttu-id="7bb1e-150">Ele se aplica a UIs do navegador, como menus de contexto e caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-150">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="7bb1e-151">Ele também se aplica ao cabeçalho HTTP Accept-Languages que o WebView envia para sites da Web.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-151">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="7bb1e-152">Ele está no formato de `language[-country]` onde `language` está o código de duas letras da ISO 639 e `country` é o código de duas letras da ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-152">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="7bb1e-153">get_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="7bb1e-153">get_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="7bb1e-154">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-154">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="7bb1e-155">[get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)público HRESULT (valor LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-155">public HRESULT [get_TargetCompatibleBrowserVersion](#get_targetcompatiblebrowserversion)(LPWSTR \* value)</span></span>

<span data-ttu-id="7bb1e-156">Esse padrão é o Edge WebView2 versão do tempo de execução que corresponde à versão do SDK que o aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-156">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="7bb1e-157">O formato desse valor é o mesmo que o formato da propriedade BrowserVersionString e outros valores BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-157">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="7bb1e-158">Somente a parte de versão do valor BrowserVersion é respeitada.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-158">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="7bb1e-159">O sufixo do canal, se existir, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-159">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="7bb1e-160">A versão do Edge WebView2 os binários do tempo de execução realmente usados podem ser diferentes do TargetCompatibleBrowserVersion especificado.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-160">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="7bb1e-161">Eles são garantidos apenas como compatíveis.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-161">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="7bb1e-162">Você pode verificar a versão real na propriedade BrowserVersionString no ICoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-162">You can check the actual version on the BrowserVersionString property on the ICoreWebView2Environment.</span></span>

#### <span data-ttu-id="7bb1e-163">put_AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="7bb1e-163">put_AdditionalBrowserArguments</span></span> 

<span data-ttu-id="7bb1e-164">Defina a propriedade AdditionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-164">Set the AdditionalBrowserArguments property.</span></span>

> <span data-ttu-id="7bb1e-165">Public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-165">public HRESULT [put_AdditionalBrowserArguments](#put_additionalbrowserarguments)(LPCWSTR value)</span></span>

#### <span data-ttu-id="7bb1e-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span><span class="sxs-lookup"><span data-stu-id="7bb1e-166">put_AllowSingleSignOnUsingOSPrimaryAccount</span></span> 

<span data-ttu-id="7bb1e-167">Defina a propriedade AllowSingleSignOnUsingOSPrimaryAccount.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-167">Set the AllowSingleSignOnUsingOSPrimaryAccount property.</span></span>

> <span data-ttu-id="7bb1e-168">público HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(bool allow)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-168">public HRESULT [put_AllowSingleSignOnUsingOSPrimaryAccount](#put_allowsinglesignonusingosprimaryaccount)(BOOL allow)</span></span>

#### <span data-ttu-id="7bb1e-169">put_Language</span><span class="sxs-lookup"><span data-stu-id="7bb1e-169">put_Language</span></span> 

<span data-ttu-id="7bb1e-170">Defina a propriedade Language.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-170">Set the Language property.</span></span>

> <span data-ttu-id="7bb1e-171">Public HRESULT [put_Language](#put_language)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-171">public HRESULT [put_Language](#put_language)(LPCWSTR value)</span></span>

#### <span data-ttu-id="7bb1e-172">put_TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="7bb1e-172">put_TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="7bb1e-173">Defina a propriedade TargetCompatibleBrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="7bb1e-173">Set the TargetCompatibleBrowserVersion property.</span></span>

> <span data-ttu-id="7bb1e-174">Public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(valor LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="7bb1e-174">public HRESULT [put_TargetCompatibleBrowserVersion](#put_targetcompatiblebrowserversion)(LPCWSTR value)</span></span>

