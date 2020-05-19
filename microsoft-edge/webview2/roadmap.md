---
description: Saiba mais sobre o que vem a seguir para WebView2
title: Mapa da WebView da Microsoft Edge 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: bc55c5a731ab6cba8f9be15208029aad0ad5357a
ms.sourcegitcommit: a75e062b71831ea850c85287a8d7d7ce3b55ec84
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659741"
---
# <span data-ttu-id="b56b1-104">Mapa de WebView2 do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b56b1-104">Microsoft Edge WebView2 Roadmap</span></span>

##### <span data-ttu-id="b56b1-105">Última atualização: maio de 2020</span><span class="sxs-lookup"><span data-stu-id="b56b1-105">Last Updated: May 2020</span></span>

<span data-ttu-id="b56b1-106">O controle WebView2 permite que os desenvolvedores insiram tecnologias da Web em seus aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="b56b1-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span> <span data-ttu-id="b56b1-107">Este documento descreve o roteiro potencial para WebView2.</span><span class="sxs-lookup"><span data-stu-id="b56b1-107">This document outlines the prospective roadmap for WebView2.</span></span> 

> [!NOTE]
> <span data-ttu-id="b56b1-108">O WebView2 está em desenvolvimento ativo, e o roteiro continuará evoluindo com base nas mudanças do mercado e nos comentários dos clientes, portanto observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="b56b1-108">WebView2 is under active development and the roadmap will continue to evolve based on market changes and customer feedback, so please note that the plans outlined here aren't exhaustive and are subject to change.</span></span> 

<span data-ttu-id="b56b1-109">Se você tiver dúvidas ou dúvidas sobre o roteiro, deixe comentários no repositório de [comentários](https://github.com/MicrosoftEdge/WebViewFeedback).</span><span class="sxs-lookup"><span data-stu-id="b56b1-109">If you have concerns or questions about the Roadmap, please leave feedback in the [feedback repo](https://github.com/MicrosoftEdge/WebViewFeedback).</span></span>

<span data-ttu-id="b56b1-110">A equipe WebView2 tem alguns esforços importantes em andamento:</span><span class="sxs-lookup"><span data-stu-id="b56b1-110">The WebView2 team has a few major efforts underway:</span></span>

1.  <span data-ttu-id="b56b1-111">Instalador do WebView2 Runtime (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="b56b1-111">WebView2 Runtime Installer (Q4 2020)</span></span>
2.  <span data-ttu-id="b56b1-112">Versão corrigida (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="b56b1-112">Fixed Version (Q4 2020)</span></span>
3.  <span data-ttu-id="b56b1-113">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="b56b1-113">General Availability</span></span> 
    *   <span data-ttu-id="b56b1-114">Win32 C/C++ (4º trimestre de 2020)</span><span class="sxs-lookup"><span data-stu-id="b56b1-114">Win32 C/C++ (Q4 2020)</span></span>
    *   <span data-ttu-id="b56b1-115">.NET (Q4 2020)</span><span class="sxs-lookup"><span data-stu-id="b56b1-115">.NET (Q4 2020)</span></span>
    *   [<span data-ttu-id="b56b1-116">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="b56b1-116">WinUI 3.0</span></span>](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## <span data-ttu-id="b56b1-117">Instalador & do WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="b56b1-117">WebView2 Runtime & Installer</span></span>

<span data-ttu-id="b56b1-118">WebView2 o modelo de distribuição [verde](./concepts/distribution.md#microsoft-edge-webview2-runtime) permitirá que você direcione ou reinstale o tempo de execução do WebView2 na máquina do usuário.</span><span class="sxs-lookup"><span data-stu-id="b56b1-118">WebView2 [Evergreen](./concepts/distribution.md#microsoft-edge-webview2-runtime) distribution model will allow you to target or chain install the WebView2 Runtime onto your user's machine.</span></span> <span data-ttu-id="b56b1-119">Espera-se que uma visualização do tempo de execução do WebView2 e do instalador esteja disponível no 3º trimestre de 2020 e em GA 2020.</span><span class="sxs-lookup"><span data-stu-id="b56b1-119">A preview of the WebView2 Runtime and installer is expected to be available Q3 2020 and GA in Q4 2020.</span></span>

## <span data-ttu-id="b56b1-120">Versão corrigida</span><span class="sxs-lookup"><span data-stu-id="b56b1-120">Fixed Version</span></span>

<span data-ttu-id="b56b1-121">O modelo de distribuição [fixa](./concepts/distribution.md#roadmap) WebView2 permite empacotar os binários do Microsoft Edge dentro de seu aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="b56b1-121">WebView2 [Fixed](./concepts/distribution.md#roadmap) distribution model allows you to package the Microsoft Edge binaries inside your native application.</span></span> <span data-ttu-id="b56b1-122">No momento, o trabalho de engenharia está em meio a uma visualização prevista para estar pronto até o final do 3º trimestre de 2020 e do GA trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="b56b1-122">Engineering work is currently under way with a preview anticipated to be ready towards the end of  Q3 2020 and GA Q4 2020.</span></span>

## <span data-ttu-id="b56b1-123">Disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="b56b1-123">General Availability</span></span> 

### <span data-ttu-id="b56b1-124">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="b56b1-124">Win32 C/C++</span></span>

<span data-ttu-id="b56b1-125">O SDK do Win32 C/C++ é esperado para GA no quarto trimestre de 2020, logo depois do tempo de execução do WebView2 e do instalador GA.</span><span class="sxs-lookup"><span data-stu-id="b56b1-125">The Win32 C/C++ SDK is expected to GA in Q4 2020, shortly after the WebView2 Runtime and installer GA.</span></span>

### <span data-ttu-id="b56b1-126">.NET</span><span class="sxs-lookup"><span data-stu-id="b56b1-126">.NET</span></span>

<span data-ttu-id="b56b1-127">O SDK do .NET encapsula o SDK C/C++ do Win32.</span><span class="sxs-lookup"><span data-stu-id="b56b1-127">The .NET SDK wraps the Win32 C/C++ SDK.</span></span> <span data-ttu-id="b56b1-128">O SDK do .NET é esperado para GA, logo após o Win32 C/C++ GA no quarto trimestre de 2020.</span><span class="sxs-lookup"><span data-stu-id="b56b1-128">The .NET SDK is expected to GA shortly after the Win32 C/C++ GA in Q4 2020.</span></span>

### <span data-ttu-id="b56b1-129">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="b56b1-129">WinUI 3.0</span></span>

<span data-ttu-id="b56b1-130">Você pode trazer o WebView2 para aplicativos UWP por meio [da interface do usuário do Win 3,0](/uwp/toolkits/winui3/), atualmente em Alpha.</span><span class="sxs-lookup"><span data-stu-id="b56b1-130">You can bring WebView2 to UWP applications through [Win UI 3.0](/uwp/toolkits/winui3/), currently in alpha.</span></span> <span data-ttu-id="b56b1-131">Fazer check-out do [roteiro da Windows UI library](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) para manter-se atualizado.</span><span class="sxs-lookup"><span data-stu-id="b56b1-131">Checkout the [Windows UI Library Roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) to keep up to date.</span></span>  
