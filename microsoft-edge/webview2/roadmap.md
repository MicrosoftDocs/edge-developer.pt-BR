---
description: Saiba mais sobre o que vem a seguir para WebView2
title: Mapa da WebView da Microsoft Edge 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 52a2f6d9ef3447955554a5507c3eaab39e6b6a9e
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120365"
---
# <span data-ttu-id="4a2bd-104">Mapa de WebView2 do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a2bd-104">Microsoft Edge WebView2 roadmap</span></span>  

##### <span data-ttu-id="4a2bd-105">Última atualização: outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="4a2bd-105">Last Updated: Oct 2020</span></span>  

<span data-ttu-id="4a2bd-106">O controle WebView2 permite que os desenvolvedores insiram tecnologias da Web em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="4a2bd-107">A página a seguir descreve o mapa potencial para WebView2.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="4a2bd-108">O WebView2 está em desenvolvimento ativo, e o mapa continua a evoluir com base nas mudanças do mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="4a2bd-109">Se você tiver dúvidas ou dúvidas sobre o roteiro, forneça seus comentários no [repositório de comentários][GithubMicrosoftedgeWebviewfeedbackMain].</span><span class="sxs-lookup"><span data-stu-id="4a2bd-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="4a2bd-110">A equipe do WebView2 está planejando os principais esforços para atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="4a2bd-111">Instalador do WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="4a2bd-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="4a2bd-112">Quarto trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="4a2bd-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="4a2bd-113">Versão corrigida</span><span class="sxs-lookup"><span data-stu-id="4a2bd-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="4a2bd-114">Quarto trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="4a2bd-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="4a2bd-115">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="4a2bd-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="4a2bd-116">Win32 C/C++ \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="4a2bd-117">.NET \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="4a2bd-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="4a2bd-118">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="4a2bd-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="4a2bd-119">Tempo de execução do WebView2 e instalador</span><span class="sxs-lookup"><span data-stu-id="4a2bd-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="4a2bd-120">O [modelo de distribuição verde][ConceptDistributionEvergreenModel] permite que você direcione ou reinstale o tempo de execução do WebView2 no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="4a2bd-121">O tempo de execução do WebView2 e o instalador do verde chegaram à disponibilidade geral \ (GA \).</span><span class="sxs-lookup"><span data-stu-id="4a2bd-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <span data-ttu-id="4a2bd-122">Versão corrigida</span><span class="sxs-lookup"><span data-stu-id="4a2bd-122">Fixed version</span></span>  

<span data-ttu-id="4a2bd-123">O [modelo de distribuição de versão fixa][ConceptsDistributionFixedVersionModel] permite empacotar os binários do Microsoft Edge dentro de seu aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="4a2bd-124">No momento, ele está sendo visualizado e direcionado para o GA, quarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-124">It is currently under preview and targeted to GA Q4 2020.</span></span>  

## <span data-ttu-id="4a2bd-125">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="4a2bd-125">General availability</span></span>  

### <span data-ttu-id="4a2bd-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="4a2bd-126">Win32 C/C++</span></span>  

<span data-ttu-id="4a2bd-127">O SDK C/C++ do Win32 alcançou GA.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <span data-ttu-id="4a2bd-128">.NET</span><span class="sxs-lookup"><span data-stu-id="4a2bd-128">.NET</span></span>  

<span data-ttu-id="4a2bd-129">O SDK do .NET encapsula o SDK C/C++ do Win32.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-129">The .NET SDK wraps the Win32 C/C++ SDK.</span></span>  <span data-ttu-id="4a2bd-130">O SDK do .NET é esperado para GA, logo após o Win32 C/C++ GA no quarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-130">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>  

### <span data-ttu-id="4a2bd-131">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="4a2bd-131">WinUI 3.0</span></span>  

<span data-ttu-id="4a2bd-132">Você pode acessar o WebView2 em seus aplicativos UWP usando a [interface do usuário do Win 3,0][UwpToolkitsWinui3Index], atualmente em Alpha.</span><span class="sxs-lookup"><span data-stu-id="4a2bd-132">You are able to access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="4a2bd-133">Para obter mais informações sobre como manter-se atualizado, consulte o [mapa de biblioteca da interface do usuário do Windows][GithubMicrosoftUiXamlRoadmap].</span><span class="sxs-lookup"><span data-stu-id="4a2bd-133">For more information about keeping up to date, see [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI library 3,0 Preview 1 (2020 de maio) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Mapa da Windows UI library-Microsoft/Microsoft-UI-XAML | GitHub"  
