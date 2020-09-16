---
description: Extensions Enterprise documentação para extensões Edge (Chromium).
title: Hospedagem e Atualização
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: d918aec12e56daf66d13488d360a454d736031e8
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015699"
---
# <span data-ttu-id="3a56f-104">Hospedagem e atualização de loja da Web</span><span class="sxs-lookup"><span data-stu-id="3a56f-104">Web Store Hosting and Updating</span></span>  

<span data-ttu-id="3a56f-105">A maioria das extensões está hospedada no [Catálogo de Complementos do Microsoft Edge Insider \ (Complementos do Microsoft Edge Insider \)][MicrosoftStoreExtensions] para melhor proteger os usuários contra extensões mal-intencionadas.</span><span class="sxs-lookup"><span data-stu-id="3a56f-105">Most Extensions are hosted in the [Microsoft Edge Insider Addons catalog \(Microsoft Edge Insider Addons\)][MicrosoftStoreExtensions] to best protect users from malicious Extensions.</span></span>  

## <span data-ttu-id="3a56f-106">Hospedagem</span><span class="sxs-lookup"><span data-stu-id="3a56f-106">Hosting</span></span>  

<span data-ttu-id="3a56f-107">Todas as extensões são distribuídas aos usuários como um arquivo ZIP especial com um sufixo. crx.</span><span class="sxs-lookup"><span data-stu-id="3a56f-107">All Extensions are distributed to users as a special ZIP file with a .crx suffix.</span></span>  <span data-ttu-id="3a56f-108">As extensões hospedadas nos Complementos do Microsoft Edge são carregadas como arquivos. zip.</span><span class="sxs-lookup"><span data-stu-id="3a56f-108">Extensions hosted in the Microsoft Edge Addons are uploaded as .zip files.</span></span> <span data-ttu-id="3a56f-109">O processo de publicação converte automaticamente o. zip em um arquivo. crx.</span><span class="sxs-lookup"><span data-stu-id="3a56f-109">The publishing process automatically converts the .zip into a .crx file.</span></span>  

<span data-ttu-id="3a56f-110">Há duas exceções à regra de Hospedagem de Complementos do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="3a56f-110">There are two exceptions to the Microsoft Edge Addons hosting rule:</span></span>  

1.  <span data-ttu-id="3a56f-111">Extensões que são distribuídas por meio da política da empresa.</span><span class="sxs-lookup"><span data-stu-id="3a56f-111">Extensions that are distributed through the Enterprise policy.</span></span>  
1.  <span data-ttu-id="3a56f-112">Diretórios de extensão descompactados de um computador local enquanto estiver no modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="3a56f-112">Unpacked Extension directories from a local machine while in developer mode.</span></span>  

## <span data-ttu-id="3a56f-113">Atualizar</span><span class="sxs-lookup"><span data-stu-id="3a56f-113">Updating</span></span>  

<span data-ttu-id="3a56f-114">O navegador Microsoft Edge verifica periodicamente se há novas versões instaladas de extensões instaladas e as atualiza sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a56f-114">The Microsoft Edge browser periodically checks for new versions of installed Extensions and updates each without user intervention.</span></span>  

> [!NOTE]
> <span data-ttu-id="3a56f-115">As etapas para atualizar uma extensão em Complementos do Microsoft Edge são previstas como adicionadas.</span><span class="sxs-lookup"><span data-stu-id="3a56f-115">Steps to update an Extension on Microsoft Edge Addons are planned be added.</span></span>  

<!-- image links -->

<!-- links -->  

[MicrosoftStoreExtensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensões-complementos do Microsoft Edge Insider"  

> [!NOTE]
> <span data-ttu-id="3a56f-117">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="3a56f-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3a56f-118">A página original foi encontrada [aqui](https://developer.chrome.com/extensions/hosting).</span><span class="sxs-lookup"><span data-stu-id="3a56f-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3a56f-120">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3a56f-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
