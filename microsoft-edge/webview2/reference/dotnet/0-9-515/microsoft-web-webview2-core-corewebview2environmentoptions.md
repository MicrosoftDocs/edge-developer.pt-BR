---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 8378c6388f0bc7cda26ef4a34b8ef5e8d5c95f4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885041"
---
# <span data-ttu-id="79f32-104">classe 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="79f32-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2EnvironmentOptions class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="79f32-105">Namespace: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="79f32-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="79f32-106">Assembly: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="79f32-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="79f32-107">Opções usadas para criar o ambiente WebView2.</span><span class="sxs-lookup"><span data-stu-id="79f32-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="79f32-108">Resumo</span><span class="sxs-lookup"><span data-stu-id="79f32-108">Summary</span></span>

 <span data-ttu-id="79f32-109">Parte</span><span class="sxs-lookup"><span data-stu-id="79f32-109">Members</span></span>                        | <span data-ttu-id="79f32-110">Descrições</span><span class="sxs-lookup"><span data-stu-id="79f32-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="79f32-111">AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="79f32-111">AdditionalBrowserArguments</span></span>](#additionalbrowserarguments) | <span data-ttu-id="79f32-112">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="79f32-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="79f32-113">Idioma</span><span class="sxs-lookup"><span data-stu-id="79f32-113">Language</span></span>](#language) | <span data-ttu-id="79f32-114">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="79f32-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="79f32-115">TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="79f32-115">TargetCompatibleBrowserVersion</span></span>](#targetcompatiblebrowserversion) | <span data-ttu-id="79f32-116">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="79f32-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="79f32-117">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="79f32-117">CoreWebView2EnvironmentOptions</span></span>](#corewebview2environmentoptions) | <span data-ttu-id="79f32-118">Inicializa uma nova instância da classe CoreWebView2EnvironmentOptions.</span><span class="sxs-lookup"><span data-stu-id="79f32-118">Initializes a new instance of the CoreWebView2EnvironmentOptions class.</span></span>

<span data-ttu-id="79f32-119">Uma implementação padrão é fornecida em WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="79f32-119">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

## <span data-ttu-id="79f32-120">Parte</span><span class="sxs-lookup"><span data-stu-id="79f32-120">Members</span></span>

#### <span data-ttu-id="79f32-121">AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="79f32-121">AdditionalBrowserArguments</span></span> 

<span data-ttu-id="79f32-122">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="79f32-122">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="79f32-123">Cadeia de caracteres pública [AdditionalBrowserArguments](#additionalbrowserarguments)</span><span class="sxs-lookup"><span data-stu-id="79f32-123">public string [AdditionalBrowserArguments](#additionalbrowserarguments)</span></span>

<span data-ttu-id="79f32-124">Eles serão passados para o processo do navegador como parte da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="79f32-124">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="79f32-125">Consulte [executar Chromium com sinalizadores](https://aka.ms/RunChromiumWithFlags) para obter mais informações sobre as opções de linha de comando para o processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="79f32-125">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="79f32-126">Se o aplicativo for iniciado com uma linha de comando Alternar `--edge-webview-switches=xxx` o valor dessa opção (xxx no exemplo acima) também será acrescentado à linha de comando do processo do navegador.</span><span class="sxs-lookup"><span data-stu-id="79f32-126">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="79f32-127">Determinadas opções `--user-data-dir` , como são internas e importantes para o WebView.</span><span class="sxs-lookup"><span data-stu-id="79f32-127">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="79f32-128">Essas opções serão ignoradas, mesmo que especificado.</span><span class="sxs-lookup"><span data-stu-id="79f32-128">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="79f32-129">Se as mesmas opções forem especificadas várias vezes, o último WINS.</span><span class="sxs-lookup"><span data-stu-id="79f32-129">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="79f32-130">Não há nenhuma tentativa de mesclar os valores diferentes da mesma opção, exceto para recursos desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="79f32-130">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="79f32-131">Os recursos especificados por `--enable-features` e `--disable-features` serão mesclados com uma lógica simples: os recursos serão a União dos recursos e recursos internos especificados e, se um recurso estiver desabilitado, ele será removido da lista de recursos habilitados.</span><span class="sxs-lookup"><span data-stu-id="79f32-131">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="79f32-132">O valor da linha de comando do processo de aplicativo é `--edge-webview-switches` processado após o parâmetro additionalBrowserArguments ser processado.</span><span class="sxs-lookup"><span data-stu-id="79f32-132">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="79f32-133">Certos recursos são desabilitados internamente e não podem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="79f32-133">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="79f32-134">Se a análise falhar para as opções especificadas, elas serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="79f32-134">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="79f32-135">Padrão é executar o processo do navegador sem sinalizadores extras.</span><span class="sxs-lookup"><span data-stu-id="79f32-135">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="79f32-136">Idioma</span><span class="sxs-lookup"><span data-stu-id="79f32-136">Language</span></span> 

<span data-ttu-id="79f32-137">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="79f32-137">The default language that WebView will run with.</span></span>

> <span data-ttu-id="79f32-138">[linguagem](#language) de cadeia de caracteres pública</span><span class="sxs-lookup"><span data-stu-id="79f32-138">public string [Language](#language)</span></span>

<span data-ttu-id="79f32-139">Ele se aplica a UIs do navegador, como menus de contexto e caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="79f32-139">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="79f32-140">Ele também se aplica ao cabeçalho HTTP Accept-Languages que o WebView envia para sites da Web.</span><span class="sxs-lookup"><span data-stu-id="79f32-140">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="79f32-141">Ele está no formato de `language[-country]` onde `language` está o código de duas letras da ISO 639 e `country` é o código de duas letras da ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="79f32-141">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="79f32-142">TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="79f32-142">TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="79f32-143">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="79f32-143">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="79f32-144">Cadeia de caracteres pública [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)</span><span class="sxs-lookup"><span data-stu-id="79f32-144">public string [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)</span></span>

<span data-ttu-id="79f32-145">Esse padrão é o Edge WebView2 versão do tempo de execução que corresponde à versão do SDK que o aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="79f32-145">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="79f32-146">O formato desse valor é o mesmo que o formato da propriedade BrowserVersionString e outros valores BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="79f32-146">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="79f32-147">Somente a parte de versão do valor BrowserVersion é respeitada.</span><span class="sxs-lookup"><span data-stu-id="79f32-147">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="79f32-148">O sufixo do canal, se existir, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="79f32-148">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="79f32-149">A versão do Edge WebView2 os binários do tempo de execução realmente usados podem ser diferentes do TargetCompatibleBrowserVersion especificado.</span><span class="sxs-lookup"><span data-stu-id="79f32-149">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="79f32-150">Eles são garantidos apenas como compatíveis.</span><span class="sxs-lookup"><span data-stu-id="79f32-150">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="79f32-151">Você pode verificar a versão real na propriedade BrowserVersionString no CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="79f32-151">You can check the actual version on the BrowserVersionString property on the CoreWebView2Environment.</span></span>

#### <span data-ttu-id="79f32-152">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="79f32-152">CoreWebView2EnvironmentOptions</span></span> 

<span data-ttu-id="79f32-153">Inicializa uma nova instância da classe CoreWebView2EnvironmentOptions.</span><span class="sxs-lookup"><span data-stu-id="79f32-153">Initializes a new instance of the CoreWebView2EnvironmentOptions class.</span></span>

> <span data-ttu-id="79f32-154">Public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(cadeia de caracteres additionalBrowserArguments, linguagem de cadeia de caracteres, targetCompatibleBrowserVersion de cadeia de caracteres)</span><span class="sxs-lookup"><span data-stu-id="79f32-154">public  [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(string additionalBrowserArguments, string language, string targetCompatibleBrowserVersion)</span></span>

##### <span data-ttu-id="79f32-155">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79f32-155">Parameters</span></span>
* `additionalBrowserArguments` <span data-ttu-id="79f32-156">AdditionalBrowserArguments pode ser especificado para alterar o comportamento do WebView.</span><span class="sxs-lookup"><span data-stu-id="79f32-156">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span> 

* `language` <span data-ttu-id="79f32-157">O idioma padrão com o qual o WebView será executado.</span><span class="sxs-lookup"><span data-stu-id="79f32-157">The default language that WebView will run with.</span></span> 

* `targetCompatibleBrowserVersion` <span data-ttu-id="79f32-158">A versão dos binários do tempo de execução do Edge WebView2 necessária para ser compatível com o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="79f32-158">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

