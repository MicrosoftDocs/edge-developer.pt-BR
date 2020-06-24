---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757603"
---
# <span data-ttu-id="ee0d0-104">Entender as versões do SDK do WebView2</span><span class="sxs-lookup"><span data-stu-id="ee0d0-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="ee0d0-105">O WebView2 depende do Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-105">WebView2 depends on Microsoft Edge to function.</span></span> <span data-ttu-id="ee0d0-106">Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="ee0d0-107">A versão mínima é refletida na versão do pacote do SDK.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="ee0d0-108">Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span> <span data-ttu-id="ee0d0-109">A versão do navegador também é especificada nas [notas de versão][Webview2Releasenotes]do WebView2.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-109">The browser version is also specified in the WebView2 [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="ee0d0-110">Para obter mais informações sobre as versões mais recentes do navegador, consulte [canais do navegador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="ee0d0-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="ee0d0-111">O WebView2 está atualmente em visualização.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="ee0d0-112">Enquanto a equipe do Microsoft Edge WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido que algumas versões mais recentes do navegador possam não dar suporte a versões mais antigas do SDK.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="ee0d0-113">Se houver alterações significativas entre versões e SDKs do navegador, a equipe do Microsoft Edge WebView especifica as alterações nas [notas de versão][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="ee0d0-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team specifies the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="ee0d0-114">No futuro, o modelo de distribuição para aplicativos do WebView2 será alterado.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-114">In the future, the distribution model for WebView2 applications will change.</span></span> <span data-ttu-id="ee0d0-115">Para obter mais informações, consulte [tempo de execução do WebView2][Webview2IndexEdgeRuntime].</span><span class="sxs-lookup"><span data-stu-id="ee0d0-115">For more information, see [WebView2 Runtime][Webview2IndexEdgeRuntime].</span></span>  
 
## <span data-ttu-id="ee0d0-116">Lançamento e pacote de pré-lançamento</span><span class="sxs-lookup"><span data-stu-id="ee0d0-116">Release and pre-release package</span></span>  

<span data-ttu-id="ee0d0-117">Na visualização, o pacote de lançamento contém o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="ee0d0-118">[APIs C/C++ do Win32][Webview2ReferenceWin3209538]: APIs no SDK que devem permanecer iguais no ga.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-118">[Win32 C/C++ APIs][Webview2ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span> 

<span data-ttu-id="ee0d0-119">Na visualização, o pacote de pré-lançamento contém o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-119">In preview, the pre-release package contains the following.</span></span>  

*   <span data-ttu-id="ee0d0-120">APIs .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]e [núcleo][Webview2ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="ee0d0-120">.NET APIs: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515], and [Core][Webview2ReferenceDotnet09538]</span></span>
*   <span data-ttu-id="ee0d0-121">APIs experimentais.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-121">Experimental APIs.</span></span>  <span data-ttu-id="ee0d0-122">Para obter mais informações, consulte a seção [APIs Experimantal](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="ee0d0-122">For more information, see the [Experimantal APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="ee0d0-123">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="ee0d0-123">Experimental APIs</span></span>  

<span data-ttu-id="ee0d0-124">A equipe da WebView está testando APIs que representam funcionalidades futuras nomeadas APIs experimentais.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-124">The WebView Team is testing APIs that represent future functionality named Experimental APIs.</span></span>  <span data-ttu-id="ee0d0-125">As APIs experimentais são marcadas como `experimental` no SDK.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-125">The Experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="ee0d0-126">Algumas APIs experimentais podem ser entregues como APIs totalmente estáveis no pacote de lançamento.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-126">Some Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="ee0d0-127">Você deve esperar que todas as APIs experimentais sejam alteradas antes do lançamento.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="ee0d0-128">Avalie as APIs experimentais e compartilhe comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="ee0d0-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="ee0d0-129">Evite usar as APIs experimentais em aplicativos de produção.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-129">Avoid using the experimental APIs in production applications.</span></span>  

### <span data-ttu-id="ee0d0-130">Mapa</span><span class="sxs-lookup"><span data-stu-id="ee0d0-130">Roadmap</span></span>  

<span data-ttu-id="ee0d0-131">Após o WebView2 atingir um estado de generally available, o pacote de lançamento contém todas as APIs de C/C++ e .NET do Win32 com suporte estável.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="ee0d0-132">O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos comentários do desenvolvedor e em ideias compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="ee0d0-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
