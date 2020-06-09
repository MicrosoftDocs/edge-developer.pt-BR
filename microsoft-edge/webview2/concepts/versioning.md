---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: cc924a146057a3c8c578ccea187e1dd63dedcbe6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697214"
---
# <span data-ttu-id="005b0-104">Noções básicas sobre versões do navegador e WebView2</span><span class="sxs-lookup"><span data-stu-id="005b0-104">Understanding browser versions and WebView2</span></span>  

<span data-ttu-id="005b0-105">O WebView2 depende do Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="005b0-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="005b0-106">Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.</span><span class="sxs-lookup"><span data-stu-id="005b0-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="005b0-107">Esta versão do navegador está especificada nas nossas [notas de lançamento][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="005b0-107">This browser version is specified in our [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="005b0-108">Você pode ver a versão mínima refletida na versão do pacote do SDK.</span><span class="sxs-lookup"><span data-stu-id="005b0-108">You may see the minimum version reflected in the package version of the SDK.</span></span>  <span data-ttu-id="005b0-109">Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="005b0-109">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="005b0-110">Para obter mais informações sobre as versões mais recentes do navegador, consulte [canais do navegador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="005b0-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="005b0-111">O WebView2 está atualmente em visualização.</span><span class="sxs-lookup"><span data-stu-id="005b0-111">WebView2 is currently in Preview.</span></span>  <span data-ttu-id="005b0-112">Enquanto a equipe do Microsoft Edge WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido que algumas versões mais recentes do navegador possam não dar suporte a versões mais antigas do SDK.</span><span class="sxs-lookup"><span data-stu-id="005b0-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="005b0-113">Se houver alterações significativas entre versões e SDKs do navegador, a equipe do Microsoft Edge WebView indicará as alterações nas [notas de versão][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="005b0-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team indicates the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="005b0-114">No futuro, a equipe do Microsoft Edge WebView planeja alterar o modelo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="005b0-114">In the future, the Microsoft Edge WebView team plans to change the distribution model.</span></span>  <span data-ttu-id="005b0-115">A equipe do Microsoft Edge WebView planeja remover a dependência direta do navegador Microsoft Edge da WebView2.</span><span class="sxs-lookup"><span data-stu-id="005b0-115">The Microsoft Edge WebView team plans to remove the direct dependency on the Microsoft Edge browser from WebView2.</span></span>  <span data-ttu-id="005b0-116">Para saber mais, consulte [tempo de execução do WebView2][Webview2IndexEdgeRuntime] na seção [distribuição][Webview2Distibution] .</span><span class="sxs-lookup"><span data-stu-id="005b0-116">To learn more, see [WebView2 Runtime][Webview2IndexEdgeRuntime] in the [Distribution][Webview2Distibution] section.</span></span>  

## <span data-ttu-id="005b0-117">APIs experimentais</span><span class="sxs-lookup"><span data-stu-id="005b0-117">Experimental APIs</span></span>  

<span data-ttu-id="005b0-118">Embora o WebView2 seja uma visualização, espera-se que as APIs no SDK permaneçam as mesmas no GA.</span><span class="sxs-lookup"><span data-stu-id="005b0-118">While WebView2 is a preview, the APIs in the SDK are expected to remain the same at GA.</span></span>  <span data-ttu-id="005b0-119">Há [APIs experimentais][Webview2ReferenceWin3209538Experimental] incluídas no SDK.</span><span class="sxs-lookup"><span data-stu-id="005b0-119">There are [experimental APIs][Webview2ReferenceWin3209538Experimental] included in the SDK.</span></span>  <span data-ttu-id="005b0-120">Avalie as APIs experimentais e envie seus comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="005b0-120">Please evaluate the experimental APIs and send your feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

### <span data-ttu-id="005b0-121">Mapa</span><span class="sxs-lookup"><span data-stu-id="005b0-121">Roadmap</span></span>  

<span data-ttu-id="005b0-122">Depois que o WebView2 atinge um estado de general General estável e lançamos o SDK do 1.0.0, a equipe do Microsoft Edge WebView planeja mover todas as APIs experimentais para um pacote de pré-lançamento.</span><span class="sxs-lookup"><span data-stu-id="005b0-122">After WebView2 reaches a stable general available state and we release the 1.0.0 SDK, the Microsoft Edge WebView team plans to move all experimental APIs to a pre-release package.</span></span>  <span data-ttu-id="005b0-123">O pacote de pré-lançamento continua a permitir comentários e obter informações sobre os recursos mais recentes, enquanto a versão de lançamento estável mantém a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="005b0-123">The pre-release package continues to allow for feedback and insight into the latest features, while the stable release version maintains backward compatibility.</span></span>  

<!--links -->

[Webview2Distibution]: ./distribution.md "Distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2ReferenceWin3209538Experimental]: ../reference/win32/0-9-538-reference-webview2.md#experimental "Experimental-Reference (WebView2) | Documentos da Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
