---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: acf3103f39d33586ee0614aeb0f10de0ab71c89a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894309"
---
# <span data-ttu-id="b41e0-104">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="b41e0-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="b41e0-105">O WebView2 depende do Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="b41e0-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="b41e0-106">Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.</span><span class="sxs-lookup"><span data-stu-id="b41e0-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="b41e0-107">A versão mínima é refletida na versão do pacote do SDK.</span><span class="sxs-lookup"><span data-stu-id="b41e0-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="b41e0-108">Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b41e0-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="b41e0-109">A versão do navegador também é especificada nas [notas de versão][Releasenotes]do WebView2.</span><span class="sxs-lookup"><span data-stu-id="b41e0-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="b41e0-110">Para obter mais informações sobre as versões mais recentes do navegador, consulte [canais do navegador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="b41e0-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="b41e0-111">O WebView2 está atualmente em visualização.</span><span class="sxs-lookup"><span data-stu-id="b41e0-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="b41e0-112">Enquanto a equipe da WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido porque versões mais recentes do navegador podem não dar suporte a versões anteriores do SDK.</span><span class="sxs-lookup"><span data-stu-id="b41e0-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="b41e0-113">Se houver alterações significativas entre versões e SDKs do navegador, especificaremos as alterações nas [notas de versão][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="b41e0-113">If there are breaking changes between browser versions and SDKs, we specify the changes in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="b41e0-114">No futuro, pretendemos alterar o modelo de distribuição para aplicativos do WebView2.</span><span class="sxs-lookup"><span data-stu-id="b41e0-114">In the future, we plan to change the distribution model for WebView2 applications.</span></span>  <span data-ttu-id="b41e0-115">Para obter mais informações, consulte [modo de distribuição em verde][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="b41e0-115">For more information, see [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  
 
## <span data-ttu-id="b41e0-116">Lançamento e pacote de pré-lançamento</span><span class="sxs-lookup"><span data-stu-id="b41e0-116">Release and pre-release package</span></span>  

<span data-ttu-id="b41e0-117">Na visualização, o pacote de lançamento contém o seguinte.</span><span class="sxs-lookup"><span data-stu-id="b41e0-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="b41e0-118">[APIs C/C++ do Win32][ReferenceWin3209538]: APIs no SDK que devem permanecer iguais no ga.</span><span class="sxs-lookup"><span data-stu-id="b41e0-118">[Win32 C/C++ APIs][ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="b41e0-119">Na visualização, o pacote de pré-lançamento contém os componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="b41e0-119">In preview, the pre-release package contains the following components.</span></span>  

*   <span data-ttu-id="b41e0-120">APIs .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]e [núcleo][ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="b41e0-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09538]</span></span>  
*   <span data-ttu-id="b41e0-121">APIs experimentais.</span><span class="sxs-lookup"><span data-stu-id="b41e0-121">Experimental APIs.</span></span>  <span data-ttu-id="b41e0-122">Para obter mais informações, consulte a seção [APIs experimentais](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="b41e0-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="b41e0-123">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="b41e0-123">Experimental APIs</span></span>  

<span data-ttu-id="b41e0-124">Estamos testando APIs experimentais que podem representar futuras funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="b41e0-124">We are testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="b41e0-125">As APIs experimentais são marcadas como `experimental` no SDK.</span><span class="sxs-lookup"><span data-stu-id="b41e0-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="b41e0-126">APIs experimentais podem ser entregues como APIs totalmente estáveis no pacote de lançamento.</span><span class="sxs-lookup"><span data-stu-id="b41e0-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="b41e0-127">Você deve esperar que todas as APIs experimentais sejam alteradas antes do lançamento.</span><span class="sxs-lookup"><span data-stu-id="b41e0-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="b41e0-128">Avalie as APIs experimentais e compartilhe comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="b41e0-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="b41e0-129">Evite usar as APIs experimentais em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="b41e0-129">Avoid using the experimental APIs in production applications.</span></span>  

## <span data-ttu-id="b41e0-130">Mapa</span><span class="sxs-lookup"><span data-stu-id="b41e0-130">Roadmap</span></span>  

<span data-ttu-id="b41e0-131">Após o WebView2 atingir um estado de generally available, o pacote de lançamento contém todas as APIs de C/C++ e .NET do Win32 com suporte estável.</span><span class="sxs-lookup"><span data-stu-id="b41e0-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="b41e0-132">O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos comentários do desenvolvedor e em ideias compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="b41e0-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribuição em verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
