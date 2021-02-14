---
description: Hospedar e publicar extensões na empresa para o Microsoft Edge (Chromium).
title: Publicar e atualizar extensões no armazenamento de Complementos do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327684"
---
# <span data-ttu-id="7c06d-104">Publicar e atualizar extensões no armazenamento de Complementos do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7c06d-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="7c06d-105">A maioria das extensões são [publicadas no armazenamento de Complementos][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] do Microsoft Edge para proteger os usuários contra extensões mal-intencionadas.</span><span class="sxs-lookup"><span data-stu-id="7c06d-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <span data-ttu-id="7c06d-106">Opções de publicação para extensões</span><span class="sxs-lookup"><span data-stu-id="7c06d-106">Publish options for extensions</span></span>  

<span data-ttu-id="7c06d-107">Todas as extensões são distribuídas aos usuários como um arquivo morto especial \( `.zip` \) com `.crx` um sufixo.</span><span class="sxs-lookup"><span data-stu-id="7c06d-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="7c06d-108">As extensões publicadas no armazenamento de Complementos do Microsoft Edge são carregadas como `.zip` arquivos.</span><span class="sxs-lookup"><span data-stu-id="7c06d-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="7c06d-109">O processo de publicação converte automaticamente `.zip` o arquivo em um `.crx` arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c06d-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="7c06d-110">Os dois cenários a seguir não exigem que você publique sua extensão no armazenamento de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7c06d-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="7c06d-111">Extensões distribuídas usando a política Enterprise.</span><span class="sxs-lookup"><span data-stu-id="7c06d-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="7c06d-112">Usar diretórios de extensão não descompactados em um computador local quando o Microsoft Edge está no modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="7c06d-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <span data-ttu-id="7c06d-113">Atualizações para extensões</span><span class="sxs-lookup"><span data-stu-id="7c06d-113">Updates to extensions</span></span>

<span data-ttu-id="7c06d-114">O navegador Microsoft Edge verifica periodicamente se há novas versões de extensões instaladas e atualiza cada uma sem a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c06d-114">The Microsoft Edge browser periodically checks for new versions of installed extensions and updates each without user intervention.</span></span>  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensões - Complementos do Microsoft Edge Insider | Microsoft"  

> [!NOTE]
> <span data-ttu-id="7c06d-116">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7c06d-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7c06d-117">A página original é encontrada [aqui.](https://developer.chrome.com/extensions/hosting)</span><span class="sxs-lookup"><span data-stu-id="7c06d-117">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7c06d-119">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7c06d-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
