---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 54d62de00a89a3c433fd77e9ec20945adbfc19c3
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191607"
---
# <span data-ttu-id="8535a-104">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="8535a-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="8535a-105">As novas versões do SDK do WebView2 são fornecidas na mesma cadência geral do navegador Microsoft Edge \ (Chromium \), que é aproximadamente a cada seis semanas.</span><span class="sxs-lookup"><span data-stu-id="8535a-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="8535a-106">Liberar e lançar pacote</span><span class="sxs-lookup"><span data-stu-id="8535a-106">Release and prerelease package</span></span>  

<span data-ttu-id="8535a-107">O pacote NuGet WebView2 contém um pacote de pré-lançamento e de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="8535a-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="8535a-108">O **pacote de versão** é compatível com o redirecionamento e contém os componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="8535a-108">The **release package** is forward compatible and contains the following components.</span></span>  

*   [<span data-ttu-id="8535a-109">APIs C/C++ Win32</span><span class="sxs-lookup"><span data-stu-id="8535a-109">Win32 C/C++ APIs</span></span>][ReferenceWin32]
*   <span data-ttu-id="8535a-110">APIs .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]e [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span><span class="sxs-lookup"><span data-stu-id="8535a-110">.NET APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span></span>  
    
<span data-ttu-id="8535a-111">APIs no SDK são totalmente compatíveis.</span><span class="sxs-lookup"><span data-stu-id="8535a-111">APIs in the SDK are fully supported.</span></span>  

<span data-ttu-id="8535a-112">O **pacote** de pré-lançamento é um superconjunto do pacote de versão com [APIs experimentais](#experimental-apis).</span><span class="sxs-lookup"><span data-stu-id="8535a-112">The **prerelease package** is a superset of the release package with [Experimental APIs](#experimental-apis).</span></span>  

### <span data-ttu-id="8535a-113">Mapa</span><span class="sxs-lookup"><span data-stu-id="8535a-113">Roadmap</span></span>  

<span data-ttu-id="8535a-114">O pacote de lançamento contém todas as APIs C/C++ e .NET de Win32 com suporte estáveis.</span><span class="sxs-lookup"><span data-stu-id="8535a-114">The release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="8535a-115">O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos seus comentários.</span><span class="sxs-lookup"><span data-stu-id="8535a-115">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span>  

## <span data-ttu-id="8535a-116">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="8535a-116">Experimental APIs</span></span>  

<span data-ttu-id="8535a-117">A equipe da WebView está procurando comentários sobre APIs experimentais que podem ser incluídas em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="8535a-117">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="8535a-118">As APIs experimentais são marcadas como `experimental` no SDK.</span><span class="sxs-lookup"><span data-stu-id="8535a-118">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="8535a-119">Para ajudá-lo a avaliar as APIs experimentais e compartilhar seus comentários, navegue até o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="8535a-119">To help you evaluate the Experimental APIs and share your feedback, navigate to the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="8535a-120">APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.</span><span class="sxs-lookup"><span data-stu-id="8535a-120">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="8535a-121">Evite usar as APIs experimentais em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="8535a-121">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="8535a-122">APIs experimentais podem não estar disponíveis na versão instalada do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="8535a-122">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="8535a-123">Correspondentes às versões do tempo de execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="8535a-123">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="8535a-124">Os aplicativos do WebView2 exigem que os usuários instalem um [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="8535a-124">WebView2 apps require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span>  <span data-ttu-id="8535a-125">O tempo de execução do WebView2 é atualizado automaticamente para a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8535a-125">The WebView2 Runtime automatically updates to the latest version available.</span></span>  <span data-ttu-id="8535a-126">Em alguns cenários, os usuários talvez queiram parar as atualizações automáticas do tempo de execução do WebView2, o que pode causar problemas de compatibilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8535a-126">In some scenarios, users may want to stop automatic WebView2 Runtime updates, which may cause app compatibility issues.</span></span>  

<span data-ttu-id="8535a-127">Se as atualizações do tempo de execução do WebView2 forem interrompidas, verifique se você entendeu a versão mínima do [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8535a-127">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] required by your app.</span></span>  <span data-ttu-id="8535a-128">Considere os dois itens a seguir:</span><span class="sxs-lookup"><span data-stu-id="8535a-128">Consider the following two items:</span></span>  

1.  <span data-ttu-id="8535a-129">A versão mínima necessária do SDK, localizada nas [notas de versão][Webview2Releasenotes] do WebView2, abaixo da **versão mínima do WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="8535a-129">The minimum required version of the SDK, in found in the WebView2 [Release Notes][Webview2Releasenotes] under **minimum WebView2 Runtime version**.</span></span>  <span data-ttu-id="8535a-130">Por exemplo, para o SDK versão [1.0.622.22][Webview2Releasenotes1062222], você deve instalar o [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] ou um [canal do Microsoft Edge não estável][MicrosoftedgeinsiderDownload] com um número de versão de `86.0.616.0` ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8535a-130">For example, for SDK version [1.0.622.22][Webview2Releasenotes1062222], you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of `86.0.616.0` or later.</span></span>  <span data-ttu-id="8535a-131">A versão mínima exigida pelo SDK muda apenas quando ocorre uma alteração de quebra na plataforma da Web.</span><span class="sxs-lookup"><span data-stu-id="8535a-131">The minimum version required by the SDK only changes when a breaking change occurs in the web platform.</span></span>  
1.  <span data-ttu-id="8535a-132">A versão mínima necessária do pacote NuGet necessária para dar suporte às interfaces e APIs que você usa em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8535a-132">The minimum required version of the NuGet package required to support the interfaces and APIs that you use in your app.</span></span>  <span data-ttu-id="8535a-133">Novas interfaces e APIs são adicionadas periodicamente ao WebView2.</span><span class="sxs-lookup"><span data-stu-id="8535a-133">New interfaces and APIs are added periodically to WebView2.</span></span>  <span data-ttu-id="8535a-134">APIs e interfaces incluídas em um SDK exigem versões diferentes do tempo de execução do WebView2, porque APIs e interface são adicionadas ao SDK em momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8535a-134">APIs and interfaces bundled in an SDK require different versions of the WebView2 Runtime, because APIs and interface are added to the SDK at different times.</span></span>  <span data-ttu-id="8535a-135">A versão necessária do tempo de execução do WebView2 corresponde ao número da compilação, o terceiro número da versão do SDK na qual a API foi introduzida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="8535a-135">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span>  <span data-ttu-id="8535a-136">Por exemplo, uma nova API ou interface adicionada ao SDK versão [1.0.622.22][Webview2Releasenotes1062222] requer a versão do WebView2 Runtime:  `86.0.622.0`  uma API ou interface adicionada em uma versão do SDK mais recente requer o WebView2 Runtime que tem o mesmo número de versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="8535a-136">For example, a new API or interface added in SDK version [1.0.622.22][Webview2Releasenotes1062222] requires the WebView2 Runtime version:  `86.0.622.0`  An API or interface added in a later SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span>  <span data-ttu-id="8535a-137">Para ajudá-lo a determinar se a versão do tempo de execução do WebView2 suporta uma interface ou API, navegue para [determinar o requisito de tempo de execução do WebView2](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="8535a-137">To help you determine if the WebView2 Runtime version supports an interface or API, navigate to [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="8535a-138">Ao desenvolver [aplicativos do WebView2][Webview2ConceptsDistributionEvergreenDistributionMode]para o meio do tempo de execução, teste regularmente o aplicativo nas versões mais recentes do tempo de execução do WebView2 e dos navegadores não estáveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8535a-138">When developing [Evergreen WebView2 apps][Webview2ConceptsDistributionEvergreenDistributionMode], regularly test your app against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="8535a-139">Como a plataforma da Web está em constante evolução, o teste regular é a melhor maneira de garantir que seu aplicativo funcione conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="8535a-139">Because the web platform is constantly evolving, regular testing is the best way to ensure your app performs as intended.</span></span>  

### <span data-ttu-id="8535a-140">Determinar requisito de tempo de execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="8535a-140">Determine WebView2 Runtime requirement</span></span>  

<span data-ttu-id="8535a-141">Dependendo de qual SDK você usa, considere os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="8535a-141">Depending on which SDK you use, consider the following items:</span></span>  

*   <span data-ttu-id="8535a-142">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="8535a-142">**Win32 C/C++**.</span></span>  <span data-ttu-id="8535a-143">Ao usar `QueryInterface` para obter uma nova interface, verifique o valor de retorno `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="8535a-143">When using `QueryInterface` to obtain a new interface, verify a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="8535a-144">O valor pode indicar que o tempo de execução do WebView2 é uma versão anterior e não dá suporte a essa interface.</span><span class="sxs-lookup"><span data-stu-id="8535a-144">The value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  <span data-ttu-id="8535a-145">Para obter um exemplo de como ele funciona, navegue até a [linha 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span><span class="sxs-lookup"><span data-stu-id="8535a-145">For an example of how it works, navigate to [Line 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span></span>  
*   <span data-ttu-id="8535a-146">**.Net e WinUI**.</span><span class="sxs-lookup"><span data-stu-id="8535a-146">**.NET and WinUI**.</span></span>  <span data-ttu-id="8535a-147">Verifique se há uma `No such interface supported` exceção ao usar métodos, propriedades e eventos que foram adicionados a SDKs mais recentes.</span><span class="sxs-lookup"><span data-stu-id="8535a-147">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="8535a-148">A exceção pode ocorrer quando o tempo de execução do WebView2 é uma versão anterior e não é compatível com as APIs.</span><span class="sxs-lookup"><span data-stu-id="8535a-148">The exception may occur when the WebView2 Runtime is a previous version, and does not support the APIs.</span></span>  
    
<span data-ttu-id="8535a-149">Se uma API estiver indisponível, considere remover o recurso associado ou informar aos usuários que uma atualização para o tempo de execução do WebView2 é necessária.</span><span class="sxs-lookup"><span data-stu-id="8535a-149">If an API is unavailable, consider removing the associated feature, or inform your users that an update to the WebView2 Runtime is required.</span></span>  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribuição em verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22 – notas de versão para WebView2 SDK | Documentos da Microsoft"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft. Web. WebView2. Core | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft. Web. WebView2. WPF | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft. Web. WebView2. WinForms | Documentos da Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referência de C++ do WebView2 Win32 | Documentos da Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desenvolvedor da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Linha 622-AppWindow. cpp-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  
