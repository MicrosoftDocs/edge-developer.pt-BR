---
description: Hospedar e publicar extensões na empresa para Microsoft Edge (Chromium).
title: Publicar e atualizar extensões no Microsoft Edge de complementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 2249462b0a2dac86efa4b775171e2a3229a34431
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461217"
---
# <a name="publish-and-update-extensions-in-the-microsoft-edge-add-ons-store"></a><span data-ttu-id="30082-104">Publicar e atualizar extensões no Microsoft Edge de complementos</span><span class="sxs-lookup"><span data-stu-id="30082-104">Publish and update extensions in the Microsoft Edge Add-ons store</span></span>  

<span data-ttu-id="30082-105">A maioria das extensões é publicada no Microsoft Edge [de complementos para][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] proteger os usuários contra extensões mal-intencionadas.</span><span class="sxs-lookup"><span data-stu-id="30082-105">Most extensions are published to the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] to protect users from malicious extensions.</span></span>  

## <a name="publish-options-for-extensions"></a><span data-ttu-id="30082-106">Opções de publicação para extensões</span><span class="sxs-lookup"><span data-stu-id="30082-106">Publish options for extensions</span></span>  

<span data-ttu-id="30082-107">Todas as extensões são distribuídas aos usuários como um arquivo de arquivo especial \( `.zip` \) com `.crx` um sufixo.</span><span class="sxs-lookup"><span data-stu-id="30082-107">All extensions are distributed to users as a special archive \(`.zip`\) file with a `.crx` suffix.</span></span>  <span data-ttu-id="30082-108">Extensões publicadas no Microsoft Edge de complementos são carregadas como `.zip` arquivos.</span><span class="sxs-lookup"><span data-stu-id="30082-108">Extensions published to the Microsoft Edge Add-ons store are uploaded as `.zip` files.</span></span>  <span data-ttu-id="30082-109">O processo de publicação converte automaticamente o `.zip` arquivo em um `.crx` arquivo.</span><span class="sxs-lookup"><span data-stu-id="30082-109">The publishing process automatically converts the `.zip` file into a `.crx` file.</span></span>  

<span data-ttu-id="30082-110">Os dois cenários a seguir não exigem que você publique sua extensão no Microsoft Edge de complementos.</span><span class="sxs-lookup"><span data-stu-id="30082-110">The following two scenarios don't require you to publish your extension in the Microsoft Edge Add-ons store.</span></span>  

*   <span data-ttu-id="30082-111">Extensões distribuídas usando Enterprise política.</span><span class="sxs-lookup"><span data-stu-id="30082-111">Extensions distributed using Enterprise policy.</span></span>  
*   <span data-ttu-id="30082-112">Usando diretórios de extensão descompactados em uma máquina local quando Microsoft Edge está no modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="30082-112">Using unpacked extension directories on a local machine when Microsoft Edge is in developer mode.</span></span>  

## <a name="updates-to-extensions"></a><span data-ttu-id="30082-113">Atualizações para extensões</span><span class="sxs-lookup"><span data-stu-id="30082-113">Updates to extensions</span></span>

<span data-ttu-id="30082-114">O Microsoft Edge navegador verifica automaticamente as novas versões de Extensões instaladas.</span><span class="sxs-lookup"><span data-stu-id="30082-114">The Microsoft Edge browser automatically checks for new versions of installed Extensions.</span></span> <span data-ttu-id="30082-115">As atualizações são instaladas sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="30082-115">Updates are installed without user intervention.</span></span>  


<!-- image links -->

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensões - Microsoft Edge Addons do Insider | Microsoft"  

> [!NOTE]
> <span data-ttu-id="30082-117">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="30082-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="30082-118">A página original é encontrada [aqui](https://developer.chrome.com/extensions/hosting).</span><span class="sxs-lookup"><span data-stu-id="30082-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="30082-120">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="30082-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
