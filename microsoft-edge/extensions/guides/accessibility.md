---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Para garantir que o ícone da extensão esteja visível enquanto estiver no modo claro e escuro, siga o guia de acessibilidade.
title: Extensões-acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 514e68fc1b797a28c76bda79c8fab88b4ea2216c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561260"
---
# <span data-ttu-id="1fc9f-104">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="1fc9f-104">Accessibility</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="1fc9f-105">Criando ícones de extensão acessíveis para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1fc9f-105">Creating accessible extension icons for Microsoft Edge</span></span>

<span data-ttu-id="1fc9f-106">Os desenvolvedores de extensão de terceiros são incentivados a usar ativos de imagem que atendam aos requisitos de acessibilidade estritos da Microsoft, de forma que os ícones sejam claramente visíveis para temas claros e escuros.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-106">Third-party extension developers are encouraged to use image assets that meet Microsoft’s strict accessibility requirements so that icons are clearly visible for both light and dark themes.</span></span> <span data-ttu-id="1fc9f-107">Recomendamos que todos os ícones de extensão tenham uma proporção de 14:1 entre a cor da tela de fundo do ícone e a cor dominante do próprio ícone.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-107">We recommend that all extension icons have a 14:1 ratio between the icon’s background color and the dominant color of the icon itself.</span></span>


<span data-ttu-id="1fc9f-108">Extensões de primeira empresa desenvolvida pela Microsoft aplicam um tratamento Visual "Stickering" para atender a esses requisitos.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-108">First-party extensions developed by Microsoft apply a “stickering” visual treatment to satisfy these requirements.</span></span>

### <span data-ttu-id="1fc9f-109">Exemplos de "Stickering"</span><span class="sxs-lookup"><span data-stu-id="1fc9f-109">Examples of the "stickering"</span></span>

<span data-ttu-id="1fc9f-110">O objetivo principal de "Stickering" é tornar o ícone visualmente acessível em qualquer cor de tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-110">The main goal of “stickering” is to make the icon visually accessible on any background color.</span></span> <span data-ttu-id="1fc9f-111">A proporção de cores recomendável entre o traço externo branco e seu ícone deve ser 14:1 para dar suporte aos requisitos de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-111">The recommended color ratio between the white outer stroke and your icon should be 14:1 to support the high contrast requirements.</span></span>

#### <span data-ttu-id="1fc9f-112">Ícone bom</span><span class="sxs-lookup"><span data-stu-id="1fc9f-112">Good icon</span></span>
<span data-ttu-id="1fc9f-113">Com o Stickering, um ícone essencialmente escuro permanecerá visível em qualquer cor de tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-113">With stickering, a primarily dark icon will remain visible on any background color.</span></span>


![imagem do ícone visível em qualquer cor do plano de fundo](./../media/accessibility-light-to-dark-good.png)

#### <span data-ttu-id="1fc9f-115">Ícone incorreto</span><span class="sxs-lookup"><span data-stu-id="1fc9f-115">Bad icon</span></span>
<span data-ttu-id="1fc9f-116">Sem o Stickering, um ícone pode misturar-se com o segundo plano e ter impossível ver.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-116">Without stickering, an icon could blend in with the background and become impossible to see.</span></span>


![imagem do ícone mesclando em tela de fundo preta](./../media/accessibility-light-to-dark-bad.png)

### <span data-ttu-id="1fc9f-118">"Stickering" seu ícone de extensão</span><span class="sxs-lookup"><span data-stu-id="1fc9f-118">"Stickering" your extension icon</span></span>

<span data-ttu-id="1fc9f-119">As cinco etapas a seguir descrevem o método sugerido de criação de um ícone de extensão que atenda aos requisitos de acessibilidade da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="1fc9f-119">The following five steps outline the suggested method of creating an extension icon that meets Microsoft’s accessibility requirements:</span></span>


| <span data-ttu-id="1fc9f-120">Etapa 1</span><span class="sxs-lookup"><span data-stu-id="1fc9f-120">Step 1</span></span>                                       | <span data-ttu-id="1fc9f-121">Etapa 2</span><span class="sxs-lookup"><span data-stu-id="1fc9f-121">Step 2</span></span>                                       | <span data-ttu-id="1fc9f-122">Etapa 3</span><span class="sxs-lookup"><span data-stu-id="1fc9f-122">Step 3</span></span>                                                                                 | <span data-ttu-id="1fc9f-123">Etapa 4</span><span class="sxs-lookup"><span data-stu-id="1fc9f-123">Step 4</span></span>                                                                          | <span data-ttu-id="1fc9f-124">Etapa 5</span><span class="sxs-lookup"><span data-stu-id="1fc9f-124">Step 5</span></span>                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="1fc9f-125">Defina o ícone na sua grade especificada.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-125">Set your icon within your specified grid.</span></span>    | <span data-ttu-id="1fc9f-126">Reduza o tamanho do ícone em 2 pixels.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-126">Reduce your icon size by 2 pixels.</span></span>           | <span data-ttu-id="1fc9f-127">Copie o ícone e cole no lugar.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-127">Copy your icon and paste in place.</span></span> <span data-ttu-id="1fc9f-128">Criar um traçado externo de 2 pixels com cantos arredondados.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-128">Create a 2 pixel outer stroke with rounded corners.</span></span> | <span data-ttu-id="1fc9f-129">Descreva o seu traço, libere o caminho composto e mescle as formas restantes.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-129">Outline your stroke, release the compound path, and merge the remaining shapes.</span></span> | <span data-ttu-id="1fc9f-130">Colorir o branco de traço externo e o ícone interno como desejar.</span><span class="sxs-lookup"><span data-stu-id="1fc9f-130">Color the outer stroke white and the inner icon as you wish.</span></span> |
| ![step1](./../media/accessibility-step1.png) | ![step2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![step4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

