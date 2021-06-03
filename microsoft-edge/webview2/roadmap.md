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
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398410"
---
# <a name="microsoft-edge-webview2-roadmap"></a><span data-ttu-id="6fdce-104">Microsoft Edge Roteiro webView2</span><span class="sxs-lookup"><span data-stu-id="6fdce-104">Microsoft Edge WebView2 roadmap</span></span>  

> [!NOTE]
> <span data-ttu-id="6fdce-105">Last Updated: November 2020</span><span class="sxs-lookup"><span data-stu-id="6fdce-105">Last Updated:  November 2020</span></span>  

<span data-ttu-id="6fdce-106">O controle WebView2 permite que os desenvolvedores invistam tecnologias web em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="6fdce-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="6fdce-107">A página a seguir descreve o roteiro prospectivo para WebView2.</span><span class="sxs-lookup"><span data-stu-id="6fdce-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="6fdce-108">O WebView2 está em desenvolvimento ativo e o roteiro continua a evoluir com base nas alterações de mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="6fdce-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="6fdce-109">Se você tiver preocupações ou dúvidas sobre o Roteiro, forneça seus comentários no [repo de comentários.][GithubMicrosoftedgeWebviewfeedbackMain]</span><span class="sxs-lookup"><span data-stu-id="6fdce-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="6fdce-110">A equipe webView2 está planejando os seguintes grandes esforços para atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="6fdce-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="6fdce-111">Instalador do Tempo de Execução do WebView2</span><span class="sxs-lookup"><span data-stu-id="6fdce-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="6fdce-112">4º trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="6fdce-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="6fdce-113">Versão Não Editável</span><span class="sxs-lookup"><span data-stu-id="6fdce-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="6fdce-114">4º trimestre de 2020</span><span class="sxs-lookup"><span data-stu-id="6fdce-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="6fdce-115">Disponibilidade Geral</span><span class="sxs-lookup"><span data-stu-id="6fdce-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="6fdce-116">Win32 C/C++ \(Q4 2020\)</span><span class="sxs-lookup"><span data-stu-id="6fdce-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="6fdce-117">.NET \(Q4 2020\)</span><span class="sxs-lookup"><span data-stu-id="6fdce-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="6fdce-118">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="6fdce-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a><span data-ttu-id="6fdce-119">WebView2 Runtime e Installer</span><span class="sxs-lookup"><span data-stu-id="6fdce-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="6fdce-120">[O modelo de distribuição Evergreen][ConceptDistributionEvergreenModel] permite direcionar ou encadear a instalação do Tempo de Execução do WebView2 no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="6fdce-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="6fdce-121">O Evergreen WebView2 Runtime e o instalador atingiram a Disponibilidade Geral \(GA\).</span><span class="sxs-lookup"><span data-stu-id="6fdce-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <a name="fixed-version"></a><span data-ttu-id="6fdce-122">Versão fixa</span><span class="sxs-lookup"><span data-stu-id="6fdce-122">Fixed version</span></span>  

<span data-ttu-id="6fdce-123">[O modelo de distribuição de versão][ConceptsDistributionFixedVersionModel] fixa permite que você empacote os Microsoft Edge binários dentro do aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="6fdce-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="6fdce-124">A Versão Fixa atingiu Disponibilidade Geral \(GA\).</span><span class="sxs-lookup"><span data-stu-id="6fdce-124">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <a name="general-availability"></a><span data-ttu-id="6fdce-125">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="6fdce-125">General availability</span></span>  

### <a name="win32-cc"></a><span data-ttu-id="6fdce-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="6fdce-126">Win32 C/C++</span></span>  

<span data-ttu-id="6fdce-127">O SDK do Win32 C/C++ atingiu GA.</span><span class="sxs-lookup"><span data-stu-id="6fdce-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <a name="net"></a><span data-ttu-id="6fdce-128">.NET</span><span class="sxs-lookup"><span data-stu-id="6fdce-128">.NET</span></span>  

<span data-ttu-id="6fdce-129">O SDK .NET atingiu GA.</span><span class="sxs-lookup"><span data-stu-id="6fdce-129">The .NET SDK has reached GA.</span></span> 

### <a name="winui-30"></a><span data-ttu-id="6fdce-130">WinUI 3.0</span><span class="sxs-lookup"><span data-stu-id="6fdce-130">WinUI 3.0</span></span>  

<span data-ttu-id="6fdce-131">Você pode acessar WebView2 em seus aplicativos UWP usando [Win UI 3.0][UwpToolkitsWinui3Index], atualmente em alfa.</span><span class="sxs-lookup"><span data-stu-id="6fdce-131">You can access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="6fdce-132">Para obter mais informações sobre como manter-se atualizado, navegue até Windows roteiro da biblioteca da interface [do usuário.][GithubMicrosoftUiXamlRoadmap]</span><span class="sxs-lookup"><span data-stu-id="6fdce-132">For more information about keeping up to date, navigate to [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição evergreen - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa - Distribuição de aplicativos usando webView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows Biblioteca de interface do usuário 3.0 Visualização 1 (maio de 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Roteiro da Biblioteca da Interface do Usuário - microsoft/microsoft-ui-xaml | GitHub"  
