---
description: Saiba mais sobre o que vem a seguir para WebView2
title: Mapa da WebView da Microsoft Edge 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 151eca3da5909b9d418451617b6bf09319752c55
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844408"
---
# <span data-ttu-id="290ce-104">Mapa de WebView2 do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="290ce-104">Microsoft Edge WebView2 roadmap</span></span>  

##### <span data-ttu-id="290ce-105">Última atualização: maio de 2020</span><span class="sxs-lookup"><span data-stu-id="290ce-105">Last Updated: May 2020</span></span>  

<span data-ttu-id="290ce-106">O controle WebView2 permite que os desenvolvedores insiram tecnologias da Web em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="290ce-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="290ce-107">A página a seguir descreve o mapa potencial para WebView2.</span><span class="sxs-lookup"><span data-stu-id="290ce-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="290ce-108">O WebView2 está em desenvolvimento ativo, e o mapa continua a evoluir com base nas mudanças do mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="290ce-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="290ce-109">Se você tiver dúvidas ou dúvidas sobre o roteiro, deixe comentários no repositório de [comentários][GithubMicrosoftedgeWebviewfeedbackMain].</span><span class="sxs-lookup"><span data-stu-id="290ce-109">If you have concerns or questions about the Roadmap, please leave feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="290ce-110">A equipe do WebView2 está planejando os principais esforços para atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="290ce-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="290ce-111">Instalador do WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="290ce-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="290ce-112">Quarto trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="290ce-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="290ce-113">Versão corrigida</span><span class="sxs-lookup"><span data-stu-id="290ce-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="290ce-114">Quarto trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="290ce-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="290ce-115">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="290ce-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="290ce-116">Win32 C/C++ \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="290ce-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="290ce-117">.NET \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="290ce-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="290ce-118">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="290ce-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="290ce-119">Tempo de execução do WebView2 e instalador</span><span class="sxs-lookup"><span data-stu-id="290ce-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="290ce-120">O [modelo de distribuição verde][ConceptDistributionEvergreenModel] permite que você direcione ou reinstale o tempo de execução do WebView2 no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="290ce-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="290ce-121">Espera-se que uma visualização do tempo de execução do WebView2 e do instalador esteja disponível no 3º trimestre de 2020 e em GA 2020.</span><span class="sxs-lookup"><span data-stu-id="290ce-121">A preview of the WebView2 Runtime and installer is expected to be available Q3 2020 and GA in Q4 2020.</span></span>  

## <span data-ttu-id="290ce-122">Versão corrigida</span><span class="sxs-lookup"><span data-stu-id="290ce-122">Fixed version</span></span>  

<span data-ttu-id="290ce-123">O [modelo de distribuição de versão fixa][ConceptsDistributionFixedVersionModel] permite empacotar os binários do Microsoft Edge dentro de seu aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="290ce-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="290ce-124">No momento, o trabalho de engenharia está em meio a uma visualização prevista para estar pronto até o final do 3º trimestre de 2020 e do GA trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="290ce-124">Engineering work is currently under way with a preview anticipated to be ready towards the end of Q3 2020 and GA Q4 2020.</span></span>  

## <span data-ttu-id="290ce-125">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="290ce-125">General availability</span></span>  

### <span data-ttu-id="290ce-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="290ce-126">Win32 C/C++</span></span>  

<span data-ttu-id="290ce-127">O SDK do Win32 C/C++ é esperado para GA no quarto trimestre de 2020, logo depois do tempo de execução do WebView2 e do instalador GA.</span><span class="sxs-lookup"><span data-stu-id="290ce-127">The Win32 C/C++ SDK is expected to GA in Q4 2020, shortly after the WebView2 Runtime and installer GA.</span></span>  

### <span data-ttu-id="290ce-128">.NET</span><span class="sxs-lookup"><span data-stu-id="290ce-128">.NET</span></span>  

<span data-ttu-id="290ce-129">O SDK do .NET encapsula o SDK C/C++ do Win32.</span><span class="sxs-lookup"><span data-stu-id="290ce-129">The .NET SDK wraps the Win32 C/C++ SDK.</span></span>  <span data-ttu-id="290ce-130">O SDK do .NET é esperado para GA, logo após o Win32 C/C++ GA no quarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="290ce-130">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>  

### <span data-ttu-id="290ce-131">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="290ce-131">WinUI 3.0</span></span>  

<span data-ttu-id="290ce-132">Você pode acessar o WebView2 em seus aplicativos UWP usando a [interface do usuário do Win 3,0][UwpToolkitsWinui3Index], atualmente em Alpha.</span><span class="sxs-lookup"><span data-stu-id="290ce-132">You are able to access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="290ce-133">Para obter mais informações sobre como manter-se atualizado, consulte o [mapa de biblioteca da interface do usuário do Windows][GithubMicrosoftUiXamlRoadmap].</span><span class="sxs-lookup"><span data-stu-id="290ce-133">For more information about keeping up to date, see [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI library 3,0 Preview 1 (2020 de maio) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Mapa da Windows UI library-Microsoft/Microsoft-UI-XAML | GitHub"  
