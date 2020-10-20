---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: a47c7295e87cf4295f8cdf898b62aa3b550aa9a5
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120336"
---
# <span data-ttu-id="12247-104">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="12247-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="12247-105">Para desenvolver um aplicativo do WebView2, você deve instalar o [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] ou um [canal do Microsoft Edge não estável][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="12247-105">To develop a WebView2 application, you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload].</span></span>  <span data-ttu-id="12247-106">A versão mínima necessária está incluída na versão do pacote NuGet do SDK.</span><span class="sxs-lookup"><span data-stu-id="12247-106">The minimum version that's required is included in the NuGet package version of the SDK.</span></span>  <span data-ttu-id="12247-107">Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o tempo de [execução do WebView2][MicrosoftDeveloperEdgeWebview2] ou um [canal do Microsoft Edge não estável][MicrosoftedgeinsiderDownload] com um número de versão de 488 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="12247-107">For example, if you use the `SDK package version 0.9.488`, then you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of 488 or later.</span></span>  <span data-ttu-id="12247-108">A versão mínima necessária também é especificada nas notas de [versão][Releasenotes]do WebView2.</span><span class="sxs-lookup"><span data-stu-id="12247-108">The minimum version required is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="12247-109">As novas versões do SDK do WebView2 são fornecidas na mesma cadência geral do navegador Microsoft Edge \ (Chromium \), que é aproximadamente a cada seis semanas.</span><span class="sxs-lookup"><span data-stu-id="12247-109">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="12247-110">Ao desenvolver aplicativos do WebView2 para o meio do tempo de execução, teste regularmente o aplicativo nas versões mais recentes do tempo de execução do WebView2 e dos navegadores não estáveis do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12247-110">When developing Evergreen WebView2 applications, regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="12247-111">Como a plataforma da Web está em constante evolução, o teste regular é a melhor maneira de garantir que seu aplicativo seja executado conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="12247-111">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

## <span data-ttu-id="12247-112">Liberar e lançar pacote</span><span class="sxs-lookup"><span data-stu-id="12247-112">Release and prerelease package</span></span>  

<span data-ttu-id="12247-113">O pacote NuGet WebView2 contém um pacote de pré-lançamento e de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="12247-113">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="12247-114">O pacote de versão é compatível com o redirecionamento e contém as [APIs C/C++ do Win32][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="12247-114">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="12247-115">APIs neste SDK são totalmente suportadas.</span><span class="sxs-lookup"><span data-stu-id="12247-115">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="12247-116">O pacote de pré-lançamento é um superconjunto do pacote de versão com os componentes adicionais listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="12247-116">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="12247-117">APIs .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]e [núcleo][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="12247-117">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="12247-118">APIs experimentais: para obter mais informações, navegue até a seção [APIs experimentais](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="12247-118">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="12247-119">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="12247-119">Experimental APIs</span></span>  

<span data-ttu-id="12247-120">A equipe da WebView está testando APIs experimentais que podem estar incluídas em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="12247-120">The WebView team is testing experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="12247-121">As APIs experimentais são marcadas como `experimental` no SDK.</span><span class="sxs-lookup"><span data-stu-id="12247-121">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="12247-122">APIs experimentais podem ser entregues como APIs totalmente estáveis no pacote de lançamento.</span><span class="sxs-lookup"><span data-stu-id="12247-122">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="12247-123">Você pode avaliar as APIs experimentadas e compartilhar comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="12247-123">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="12247-124">Evite usar as APIs experimentais em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="12247-124">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="12247-125">Correspondentes às versões do tempo de execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="12247-125">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="12247-126">Ao escrever um aplicativo do WebView2 usando uma versão específica do SDK, os usuários do aplicativo poderão executá-lo com várias versões compatíveis do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="12247-126">When writing a WebView2 app using a particular SDK version, users of your app may run it with several compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="12247-127">A equipe da WebView está trabalhando em uma versão compatível do WebView2 Runtime que contém APIs não experimentais de versões anteriores do tempo de execução e novas APIs não experimentais.</span><span class="sxs-lookup"><span data-stu-id="12247-127">The WebView team is working on a compatible WebView2 Runtime version that contains non-experimental APIs from previous versions of the Runtime and new non-experimental APIs.</span></span>  

<span data-ttu-id="12247-128">Dependendo de qual SDK você usa, considere os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="12247-128">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="12247-129">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="12247-129">**Win32 C/C++**.</span></span>  <span data-ttu-id="12247-130">Ao usar `QueryInterface` para obter uma nova interface, verifique se há um valor de retorno `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="12247-130">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="12247-131">Esse valor pode indicar que o tempo de execução do WebView2 é uma versão anterior e não dá suporte a essa interface.</span><span class="sxs-lookup"><span data-stu-id="12247-131">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  
*   <span data-ttu-id="12247-132">**.Net e WinUI**.</span><span class="sxs-lookup"><span data-stu-id="12247-132">**.NET and WinUI**.</span></span>  <span data-ttu-id="12247-133">Verifique se há uma `No such interface supported` exceção ao usar métodos, propriedades e eventos que foram adicionados a SDKs mais recentes.</span><span class="sxs-lookup"><span data-stu-id="12247-133">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="12247-134">Essa exceção pode ocorrer quando o tempo de execução do WebView2 é uma versão anterior e não é compatível com essas APIs.</span><span class="sxs-lookup"><span data-stu-id="12247-134">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="12247-135">Se uma API estiver indisponível, considere remover o recurso associado ou informar aos usuários que eles precisam atualizar a versão do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="12247-135">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  

<span data-ttu-id="12247-136">APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.</span><span class="sxs-lookup"><span data-stu-id="12247-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="12247-137">APIs experimentais podem não estar disponíveis na versão instalada do tempo de execução do WebView2.</span><span class="sxs-lookup"><span data-stu-id="12247-137">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="12247-138">Mapa</span><span class="sxs-lookup"><span data-stu-id="12247-138">Roadmap</span></span>  

<span data-ttu-id="12247-139">O pacote de lançamento contém todas as APIs C/C++ de Win32 compatíveis e estáveis.</span><span class="sxs-lookup"><span data-stu-id="12247-139">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="12247-140">No futuro, o pacote de lançamento conterá todas as APIs do .NET compatíveis e estáveis, quando elas forem disponibilizadas geralmente.</span><span class="sxs-lookup"><span data-stu-id="12247-140">In the future, the release package will contain all stable, supported .NET APIs when they are made generally available.</span></span>  <span data-ttu-id="12247-141">O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos seus comentários e ideias compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="12247-141">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

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
