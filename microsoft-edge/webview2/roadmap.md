---
description: Saiba mais sobre o que está por vir para WebView2
title: Roteiro para Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 7b67e4a6844ead0f845667a70df8657745ece938
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643417"
---
# <a name="microsoft-edge-webview2-roadmap"></a><span data-ttu-id="07b29-104">Microsoft Edge Roteiro webView2</span><span class="sxs-lookup"><span data-stu-id="07b29-104">Microsoft Edge WebView2 roadmap</span></span>  

> [!NOTE]
> <span data-ttu-id="07b29-105">Last Updated: July 2021</span><span class="sxs-lookup"><span data-stu-id="07b29-105">Last Updated:  July 2021</span></span>  

<span data-ttu-id="07b29-106">O controle WebView2 permite que os desenvolvedores invistam tecnologias web em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="07b29-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="07b29-107">A página a seguir descreve o roteiro prospectivo para WebView2.</span><span class="sxs-lookup"><span data-stu-id="07b29-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="07b29-108">O WebView2 está em desenvolvimento ativo e o roteiro continua a evoluir com base nas alterações de mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="07b29-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="07b29-109">Se você tiver preocupações ou dúvidas sobre o Roteiro, forneça seus comentários no [repo de comentários.][GithubMicrosoftedgeWebviewfeedbackMain]</span><span class="sxs-lookup"><span data-stu-id="07b29-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="07b29-110">A equipe webView2 está planejando os seguintes grandes esforços para atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="07b29-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

* <span data-ttu-id="07b29-111">Visualização UWP</span><span class="sxs-lookup"><span data-stu-id="07b29-111">UWP Preview</span></span>
* <span data-ttu-id="07b29-112">Visualização do MacOS</span><span class="sxs-lookup"><span data-stu-id="07b29-112">MacOS Preview</span></span>
* <span data-ttu-id="07b29-113">Visualização do Xbox</span><span class="sxs-lookup"><span data-stu-id="07b29-113">Xbox Preview</span></span>
* <span data-ttu-id="07b29-114">HoloLens Visualizar</span><span class="sxs-lookup"><span data-stu-id="07b29-114">HoloLens Preview</span></span>

## <a name="webview2-runtime-and-installer"></a><span data-ttu-id="07b29-115">WebView2 Runtime e Installer</span><span class="sxs-lookup"><span data-stu-id="07b29-115">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="07b29-116">[O modelo de distribuição Evergreen][ConceptDistributionEvergreenModel] permite direcionar ou encadear a instalação do Tempo de Execução do WebView2 no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="07b29-116">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="07b29-117">O Evergreen WebView2 Runtime e o instalador atingiram a Disponibilidade Geral \(GA\).</span><span class="sxs-lookup"><span data-stu-id="07b29-117">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <a name="fixed-version"></a><span data-ttu-id="07b29-118">Versão fixa</span><span class="sxs-lookup"><span data-stu-id="07b29-118">Fixed version</span></span>  

<span data-ttu-id="07b29-119">[O modelo de distribuição de versão][ConceptsDistributionFixedVersionModel] fixa permite que você empacote os Microsoft Edge binários dentro do aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="07b29-119">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="07b29-120">A Versão Fixa atingiu Disponibilidade Geral \(GA\).</span><span class="sxs-lookup"><span data-stu-id="07b29-120">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <a name="general-availability"></a><span data-ttu-id="07b29-121">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="07b29-121">General availability</span></span>  

### <a name="win32-cc"></a><span data-ttu-id="07b29-122">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="07b29-122">Win32 C/C++</span></span>  

<span data-ttu-id="07b29-123">O SDK do Win32 C/C++ atingiu GA.</span><span class="sxs-lookup"><span data-stu-id="07b29-123">The Win32 C/C++ SDK has reached GA.</span></span>  

### <a name="net"></a><span data-ttu-id="07b29-124">.NET</span><span class="sxs-lookup"><span data-stu-id="07b29-124">.NET</span></span>  

<span data-ttu-id="07b29-125">O SDK .NET atingiu GA.</span><span class="sxs-lookup"><span data-stu-id="07b29-125">The .NET SDK has reached GA.</span></span> 

### <a name="windows-ui-library-3"></a><span data-ttu-id="07b29-126">Windows Biblioteca de interface do usuário 3</span><span class="sxs-lookup"><span data-stu-id="07b29-126">Windows UI Library 3</span></span>

<span data-ttu-id="07b29-127">Você pode acessar controles WebView2 em seus aplicativos usando Windows biblioteca de interface do usuário [3 (WinUI3)][UwpToolkitsWinui3Index] com o SDK do Windows App.</span><span class="sxs-lookup"><span data-stu-id="07b29-127">You can access WebView2 controls in your applications using [Windows UI Library 3 (WinUI3)][UwpToolkitsWinui3Index] with the Windows App SDK.</span></span> <span data-ttu-id="07b29-128">Isso está atualmente em visualização.</span><span class="sxs-lookup"><span data-stu-id="07b29-128">This is currently in preview.</span></span> <span data-ttu-id="07b29-129">Para obter mais informações, navegue até o [mapa Windows SDK do aplicativo.][WindowsAppSDK|::ref1::|]</span><span class="sxs-lookup"><span data-stu-id="07b29-129">For more information, navigate to the [Windows App SDK roadmap][WindowsAppSDK|::ref1::|].</span></span>

 
<!-- links -->  

[WindowsAppSDKRoadmap]: https://github.com/microsoft/WindowsAppSDK/blob/main/docs/roadmap.md "Roteiro"
[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição evergreen - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa - Distribuição de aplicativos usando webView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows Biblioteca de interface do usuário 3.0 Visualização 1 (maio de 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Roteiro da Biblioteca da Interface do Usuário - microsoft/microsoft-ui-xaml | GitHub"  
