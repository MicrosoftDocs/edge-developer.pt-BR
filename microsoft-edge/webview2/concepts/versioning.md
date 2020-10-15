---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: b673a2b250e46959a2eabaeb88cd8535f9a271e4
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118979"
---
# <span data-ttu-id="d39b9-104">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="d39b9-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="d39b9-105">O WebView2 depende do Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="d39b9-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="d39b9-106">Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.</span><span class="sxs-lookup"><span data-stu-id="d39b9-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="d39b9-107">A versão mínima é refletida na versão do pacote do SDK.</span><span class="sxs-lookup"><span data-stu-id="d39b9-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="d39b9-108">Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d39b9-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="d39b9-109">A versão do navegador também é especificada nas [notas de versão][Releasenotes]do WebView2.</span><span class="sxs-lookup"><span data-stu-id="d39b9-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="d39b9-110">Para obter mais informações sobre a versão mais recente do navegador Microsoft Edge, navegue até [canais do navegador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="d39b9-110">For more information about the latest release of the Microsoft Edge browser, navigate to [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="d39b9-111">O WebView2 está atualmente em visualização.</span><span class="sxs-lookup"><span data-stu-id="d39b9-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="d39b9-112">Enquanto a equipe da WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido porque versões mais recentes do navegador podem não dar suporte a versões anteriores do SDK.</span><span class="sxs-lookup"><span data-stu-id="d39b9-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="d39b9-113">Se houver alterações significativas entre versões e SDKs do navegador, as alterações serão especificadas nas [notas de versão][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="d39b9-113">If there are breaking changes between browser versions and SDKs, the changes are specified in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="d39b9-114">No futuro, a equipe da WebView planeja alterar o modelo de distribuição para aplicativos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="d39b9-114">In the future, the WebView team plans to change the distribution model for WebView2 apps.</span></span>  <span data-ttu-id="d39b9-115">Para obter mais informações, navegue até o [modo de distribuição do verde][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="d39b9-115">For more information, navigate to [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  

## <span data-ttu-id="d39b9-116">Liberar e lançar pacote</span><span class="sxs-lookup"><span data-stu-id="d39b9-116">Release and prerelease package</span></span>  

<span data-ttu-id="d39b9-117">Na visualização, o pacote de lançamento contém o seguinte.</span><span class="sxs-lookup"><span data-stu-id="d39b9-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="d39b9-118">[APIs C/C++ do Win32][ReferenceWin32]: APIs no SDK que devem permanecer iguais no ga.</span><span class="sxs-lookup"><span data-stu-id="d39b9-118">[Win32 C/C++ APIs][ReferenceWin32]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="d39b9-119">Na visualização, o pacote de pré-lançamento contém os componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="d39b9-119">In preview, the prerelease package contains the following components.</span></span>  

*   <span data-ttu-id="d39b9-120">APIs .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]e [núcleo][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="d39b9-120">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="d39b9-121">APIs experimentais.</span><span class="sxs-lookup"><span data-stu-id="d39b9-121">Experimental APIs.</span></span>  <span data-ttu-id="d39b9-122">Para obter mais informações, consulte a seção [APIs experimentais](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="d39b9-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="d39b9-123">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="d39b9-123">Experimental APIs</span></span>  

<span data-ttu-id="d39b9-124">A equipe da WebView está testando APIs experimentais que podem representar funcionalidades futuras.</span><span class="sxs-lookup"><span data-stu-id="d39b9-124">The WebView team is testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="d39b9-125">As APIs experimentais são marcadas como `experimental` no SDK.</span><span class="sxs-lookup"><span data-stu-id="d39b9-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="d39b9-126">APIs experimentais podem ser entregues como APIs totalmente estáveis no pacote de lançamento.</span><span class="sxs-lookup"><span data-stu-id="d39b9-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="d39b9-127">Você deve esperar que todas as APIs experimentais sejam alteradas antes do lançamento.</span><span class="sxs-lookup"><span data-stu-id="d39b9-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="d39b9-128">Avalie as APIs experimentais e compartilhe comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="d39b9-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="d39b9-129">Evite usar as APIs experimentais em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="d39b9-129">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="d39b9-130">Correspondentes às versões do tempo de execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="d39b9-130">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="d39b9-131">Ao escrever um aplicativo do WebView2 usando uma versão específica do SDK, os usuários do seu aplicativo podem executá-lo com várias versões compatíveis do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="d39b9-131">When writing a WebView2 app using a particular SDK version, the users fo you app may run your it with various compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="d39b9-132">No futuro, uma versão compatível mais recente do WebView2 Runtime contém todas as APIs não experimentais de uma versão de tempo de execução do WebView2 compatível mais antiga, além de novas APIs não experimentais adicionais.</span><span class="sxs-lookup"><span data-stu-id="d39b9-132">In the future, a newer compatible WebView2 Runtime version contains all the non-experimental APIs from an older compatible WebView2 Runtime version plus additional new non-experimental APIs.</span></span>  

*   <span data-ttu-id="d39b9-133">Os desenvolvedores de **C/C++ Win32** , ao usar `QueryInterface` para obter uma nova interface, devem verificar um valor de retorno de `E_NOINTERFACE` , o que pode indicar que o tempo de execução do WebView2 é mais antigo e não dá suporte a essa interface específica.</span><span class="sxs-lookup"><span data-stu-id="d39b9-133">**Win32 C/C++** developers, when using `QueryInterface` to obtain a new interface, should check for a return value of `E_NOINTERFACE`, which may indicate that the WebView2 Runtime is older and does not support that particular interface.</span></span>  
*   <span data-ttu-id="d39b9-134">Os desenvolvedores **.net e WinUI** devem verificar uma `No such interface supported` exceção ao usar métodos, propriedades e eventos adicionados em SDKs posteriores, que podem ocorrer quando o tempo de execução do WebView2 é mais antigo e não dá suporte a essas APIs específicas.</span><span class="sxs-lookup"><span data-stu-id="d39b9-134">**.NET and WinUI** developers should check for a `No such interface supported` exception when using methods, properties, and events added in later SDKs which may occur when the WebView2 Runtime is older and does not support those particular APIs.</span></span>  

<span data-ttu-id="d39b9-135">Se uma API estiver indisponível, considere a possibilidade de desabilitar o recurso associado, se possível, ou informando ao usuário final que ele precisa atualizar a versão do WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="d39b9-135">If an API is unavailable, consider disabling the associated feature, if possible, or otherwise informing the end user they need to update their WebView2 Runtime version.</span></span>  

<span data-ttu-id="d39b9-136">APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.</span><span class="sxs-lookup"><span data-stu-id="d39b9-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="d39b9-137">Ao tentar usar uma API experimental que não está disponível no tempo de execução do WebView2, você pode observar o comportamento descrito anteriormente descrito.</span><span class="sxs-lookup"><span data-stu-id="d39b9-137">When attempting to use an experimental API that is not available in the WebView2 Runtime you may observe the same previously described behavior.</span></span>  

## <span data-ttu-id="d39b9-138">Mapa</span><span class="sxs-lookup"><span data-stu-id="d39b9-138">Roadmap</span></span>  

<span data-ttu-id="d39b9-139">Após o WebView2 atingir um estado de generally available, o pacote de lançamento contém todas as APIs de C/C++ e .NET do Win32 com suporte estável.</span><span class="sxs-lookup"><span data-stu-id="d39b9-139">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="d39b9-140">O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos seus comentários e ideias compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="d39b9-140">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribuição em verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft. Web. WebView2. Core | Documentos da Microsoft"
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft. Web. WebView2. WPF | Documentos da Microsoft"
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft. Web. WebView2. WinForms | Documentos da Microsoft"
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referência de C++ do WebView2 Win32 | Documentos da Microsoft"  
[Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
