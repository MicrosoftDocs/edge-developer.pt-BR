---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 132ccab0f9f378eedd8c83a7404c350161556f2e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182392"
---
# <span data-ttu-id="d1087-104">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="d1087-104">Understand WebView2 SDK versions</span></span>

<span data-ttu-id="d1087-105">As novas versões do SDK do WebView2 são fornecidas na mesma cadência geral do navegador Microsoft Edge \ (Chromium \), que é aproximadamente a cada seis semanas.</span><span class="sxs-lookup"><span data-stu-id="d1087-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="d1087-106">Liberar e lançar pacote</span><span class="sxs-lookup"><span data-stu-id="d1087-106">Release and prerelease package</span></span>  

<span data-ttu-id="d1087-107">O pacote NuGet WebView2 contém um pacote de pré-lançamento e de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="d1087-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="d1087-108">O pacote de versão é compatível com o redirecionamento e contém as [APIs C/C++ do Win32][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="d1087-108">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="d1087-109">APIs neste SDK são totalmente suportadas.</span><span class="sxs-lookup"><span data-stu-id="d1087-109">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="d1087-110">O pacote de pré-lançamento é um superconjunto do pacote de versão com os componentes adicionais listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="d1087-110">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="d1087-111">APIs .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]e [núcleo][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="d1087-111">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="d1087-112">APIs experimentais: para obter mais informações, navegue até a seção [APIs experimentais](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="d1087-112">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="d1087-113">Mapa</span><span class="sxs-lookup"><span data-stu-id="d1087-113">Roadmap</span></span>  

<span data-ttu-id="d1087-114">O pacote de lançamento contém todas as APIs C/C++ de Win32 compatíveis e estáveis.</span><span class="sxs-lookup"><span data-stu-id="d1087-114">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="d1087-115">No futuro, o pacote de lançamento conterá todas as APIs do .NET compatíveis e estáveis, quando elas forem disponibilizadas de forma geral.</span><span class="sxs-lookup"><span data-stu-id="d1087-115">In the future, the release package will contain all stable, supported .NET APIs when they're made generally available.</span></span>  <span data-ttu-id="d1087-116">O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos seus comentários.</span><span class="sxs-lookup"><span data-stu-id="d1087-116">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span> 

## <span data-ttu-id="d1087-117">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="d1087-117">Experimental APIs</span></span>  

<span data-ttu-id="d1087-118">A equipe da WebView está procurando comentários sobre APIs experimentais que podem ser incluídas em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="d1087-118">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="d1087-119">As APIs experimentais são marcadas como `experimental` no SDK.</span><span class="sxs-lookup"><span data-stu-id="d1087-119">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="d1087-120">Você pode avaliar as APIs experimentadas e compartilhar comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="d1087-120">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="d1087-121">APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.</span><span class="sxs-lookup"><span data-stu-id="d1087-121">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="d1087-122">Evite usar as APIs experimentais em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="d1087-122">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="d1087-123">APIs experimentais podem não estar disponíveis na versão instalada do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="d1087-123">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="d1087-124">Correspondentes às versões do tempo de execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="d1087-124">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="d1087-125">Aplicativos WebView2 exigem que os usuários instalem um [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="d1087-125">WebView2 applications require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span> <span data-ttu-id="d1087-126">O tempo de execução do WebView2 é atualizado automaticamente para a versão mais recente que está disponível.</span><span class="sxs-lookup"><span data-stu-id="d1087-126">The WebView2 Runtime updates automatically to the latest version that's available.</span></span> <span data-ttu-id="d1087-127">Em alguns cenários, os usuários podem precisar parar as atualizações automáticas do tempo de execução do WebView2, o que pode causar problemas de compatibilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1087-127">In some scenarios, users may need to stop automatic WebView2 Runtime updates, which can cause application compatibility issues.</span></span>

<span data-ttu-id="d1087-128">Se as atualizações do tempo de execução do WebView2 forem interrompidas, verifique se você entendeu a versão mínima do [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1087-128">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] that's required by your application.</span></span> <span data-ttu-id="d1087-129">Considere os dois itens a seguir:</span><span class="sxs-lookup"><span data-stu-id="d1087-129">Consider the following two items:</span></span>  

1. <span data-ttu-id="d1087-130">A versão mínima necessária do SDK, que pode ser encontrada nas [notas de versão][Releasenotes] do WebView2 abaixo da **versão mínima do tempo de execução do WebView2**.</span><span class="sxs-lookup"><span data-stu-id="d1087-130">The minimum required version of the SDK, which can be found in the WebView2 [Release Notes][Releasenotes] under **minimum WebView2 Runtime version**.</span></span> <span data-ttu-id="d1087-131">Por exemplo, para o SDK versão [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222), você deve instalar o [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] ou um [canal do Microsoft Edge não estável][MicrosoftedgeinsiderDownload] com um número de compilação de **86.0.616.0** ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d1087-131">For example, for SDK version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222), you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of **86.0.616.0** or later.</span></span> <span data-ttu-id="d1087-132">A versão mínima exigida pelo SDK será alterada apenas quando houver uma alteração significativa na plataforma da Web.</span><span class="sxs-lookup"><span data-stu-id="d1087-132">The minimum version required by the SDK will only change when there's a breaking change in the web platform.</span></span>

2. <span data-ttu-id="d1087-133">A versão mínima necessária do pacote NuGet que é necessário para dar suporte às interfaces e APIs usadas em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1087-133">The minimum required version of the NuGet package that's required to support the interfaces and APIs used in your app.</span></span> <span data-ttu-id="d1087-134">Novas interfaces e APIs são adicionadas periodicamente ao WebView2.</span><span class="sxs-lookup"><span data-stu-id="d1087-134">New interfaces and APIs are added periodically to WebView2.</span></span> <span data-ttu-id="d1087-135">APIs e interfaces incluídas em um SDK exigem versões diferentes do tempo de execução do WebView2, porque elas foram adicionadas ao SDK em momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="d1087-135">APIs and interfaces bundled in an SDK will require different versions of the WebView2 Runtime because they were added to the SDK at different times.</span></span>  <span data-ttu-id="d1087-136">A versão necessária do tempo de execução do WebView2 corresponde ao número da compilação, o terceiro número da versão do SDK na qual a API foi introduzida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="d1087-136">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span> <span data-ttu-id="d1087-137">Por exemplo, uma nova API ou interface adicionada ao SDK versão [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) precisará da versão do WebView2 Runtime: 86,0. **622**. 0.</span><span class="sxs-lookup"><span data-stu-id="d1087-137">For example, a new API or interface added in SDK version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) will need the WebView2 Runtime version: 86.0.**622**.0.</span></span> <span data-ttu-id="d1087-138">Uma API ou interface adicionada em uma versão SDK subsequente exige o tempo de execução WebView2 que tem o mesmo número de versão do SDK.</span><span class="sxs-lookup"><span data-stu-id="d1087-138">An API or interface added in a subsequent SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span> <span data-ttu-id="d1087-139">Você pode determinar se a versão do tempo de execução do WebView2 dá suporte a uma interface ou API [programaticamente](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="d1087-139">You can determine if the WebView2 Runtime version supports an interface or API [programmatically](#determine-webview2-runtime-requirement).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1087-140">Ao desenvolver [aplicativos do WebView2](distribution.md#evergreen-distribution-mode)para o meio do tempo de execução, teste regularmente o aplicativo nas versões mais recentes do tempo de execução do WebView2 e dos navegadores não estáveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d1087-140">When developing [Evergreen WebView2 applications](distribution.md#evergreen-distribution-mode), regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="d1087-141">Como a plataforma da Web está em constante evolução, o teste regular é a melhor maneira de garantir que seu aplicativo seja executado conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="d1087-141">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

### <span data-ttu-id="d1087-142">Determinar requisito de tempo de execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="d1087-142">Determine WebView2 Runtime requirement</span></span>

<span data-ttu-id="d1087-143">Dependendo de qual SDK você usa, considere os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="d1087-143">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="d1087-144">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="d1087-144">**Win32 C/C++**.</span></span>  <span data-ttu-id="d1087-145">Ao usar `QueryInterface` para obter uma nova interface, verifique se há um valor de retorno `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="d1087-145">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="d1087-146">Esse valor pode indicar que o tempo de execução do WebView2 é uma versão anterior e não dá suporte a essa interface.</span><span class="sxs-lookup"><span data-stu-id="d1087-146">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span> <span data-ttu-id="d1087-147">Navegue até o exemplo WebView2API para obter um [exemplo](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) de como isso funciona.</span><span class="sxs-lookup"><span data-stu-id="d1087-147">Navigate to the WebView2API Sample for an [example](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) of how this works.</span></span>
*   <span data-ttu-id="d1087-148">**.Net e WinUI**.</span><span class="sxs-lookup"><span data-stu-id="d1087-148">**.NET and WinUI**.</span></span>  <span data-ttu-id="d1087-149">Verifique se há uma `No such interface supported` exceção ao usar métodos, propriedades e eventos que foram adicionados a SDKs mais recentes.</span><span class="sxs-lookup"><span data-stu-id="d1087-149">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="d1087-150">Essa exceção pode ocorrer quando o tempo de execução do WebView2 é uma versão anterior e não é compatível com essas APIs.</span><span class="sxs-lookup"><span data-stu-id="d1087-150">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="d1087-151">Se uma API estiver indisponível, considere remover o recurso associado ou informar aos usuários que eles precisam atualizar a versão do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="d1087-151">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  



 

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft. Web. WebView2. Core | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft. Web. WebView2. WPF | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft. Web. WebView2. WinForms | Documentos da Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referência de C++ do WebView2 Win32 | Documentos da Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desenvolvedor da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  
