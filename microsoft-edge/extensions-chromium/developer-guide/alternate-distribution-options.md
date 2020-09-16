---
description: O processo de distribuição da extensão por mecanismo diferente das lojas verificadas
title: Método alternativo de distribuição de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: e28a84fd75ad1ac0be2000a22c26371ca73d0293
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015692"
---
# <span data-ttu-id="5ee9d-104">Método alternativo de distribuição de extensão</span><span class="sxs-lookup"><span data-stu-id="5ee9d-104">Alternate Method of Distributing Extension</span></span>  

<span data-ttu-id="5ee9d-105">Se você for um desenvolvedor que deseja distribuir uma extensão como parte do processo de instalação para outro software ou um administrador de rede que queira distribuir uma extensão em toda a organização, o Microsoft Edge oferece suporte aos seguintes métodos de instalação de extensão:</span><span class="sxs-lookup"><span data-stu-id="5ee9d-105">If you are a developer who wants to distribute an Extension as part of the installation process for other software, or a network admin that want to distribute an Extension throughout their organization, Microsoft Edge supports the following Extension installation methods:</span></span>  

*   **<span data-ttu-id="5ee9d-106">Usando o registro do Windows \ (somente Windows \)</span><span class="sxs-lookup"><span data-stu-id="5ee9d-106">Using the Windows registry \(Windows only\)</span></span>**  

<span data-ttu-id="5ee9d-107">O Microsoft Edge suporta a instalação de uma extensão hospedada em um `update_URL` .</span><span class="sxs-lookup"><span data-stu-id="5ee9d-107">Microsoft Edge supports installing an Extension hosted at an `update_URL`.</span></span>  <span data-ttu-id="5ee9d-108">No Windows, o `update_URL` deve apontar para o catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \) onde a extensão deve ser hospedada.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-108">On Windows, the `update_URL` must point to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\) where the Extension must be hosted.</span></span>  

> [!NOTE]
> <span data-ttu-id="5ee9d-109">Instalação externa da extensão por meio de um arquivo JSON de preferências para o macOS</span><span class="sxs-lookup"><span data-stu-id="5ee9d-109">External installation of Extension via a preferences json file for macOS</span></span> <!--and Linux--> <span data-ttu-id="5ee9d-110">Ainda não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-110">are not supported yet.</span></span>  <span data-ttu-id="5ee9d-111">Este recurso de suporte estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-111">This feature support will soon be available.</span></span>

## <span data-ttu-id="5ee9d-112">Usar o registro do Windows</span><span class="sxs-lookup"><span data-stu-id="5ee9d-112">Using the Windows registry</span></span>  

<span data-ttu-id="5ee9d-113">Primeiro, publique a extensão nos Complementos do Microsoft Edge ou empacote um arquivo. crx e certifique-se de que ele seja instalado com êxito.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-113">First, publish the Extension in the Microsoft Edge Addons, or package a .crx file and make sure that it installs successfully.</span></span>  

<span data-ttu-id="5ee9d-114">As etapas para instalar a extensão pelo registro no Windows são:</span><span class="sxs-lookup"><span data-stu-id="5ee9d-114">The steps to install Extension via registry in windows are:</span></span>  

*   <span data-ttu-id="5ee9d-115">Localize ou crie a seguinte chave no registro:</span><span class="sxs-lookup"><span data-stu-id="5ee9d-115">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="5ee9d-116">Windows de 32 bits:</span><span class="sxs-lookup"><span data-stu-id="5ee9d-116">32-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   <span data-ttu-id="5ee9d-117">Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="5ee9d-117">64-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   <span data-ttu-id="5ee9d-118">Crie uma nova chave \ (pasta \) na chave extensões com o mesmo nome que a ID da extensão \ (por exemplo, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).</span><span class="sxs-lookup"><span data-stu-id="5ee9d-118">Create a new key \(folder\) under the Extensions key with the same name as the ID of your Extension \(for example, `aaaaaaaaaabbbbbbbbbbcccccccccc`\).</span></span>  
*   <span data-ttu-id="5ee9d-119">Na sua chave de extensão, crie uma propriedade, `update_url` e defina-a como o valor: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (isso aponta para o CRX de sua extensão nos Complementos do Microsoft Edge \).</span><span class="sxs-lookup"><span data-stu-id="5ee9d-119">In your Extension key, create a property, `update_url`, and set it to the value: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`,  \(this points to the crx of your extension in the Microsoft Edge Addons\).</span></span> <span data-ttu-id="5ee9d-120">Se você quiser instalar uma extensão da loja da Web Chrome, forneça a URL de atualização do Chrome Web Store `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="5ee9d-120">If you want to install an extension from the Chrome Web Store, please provide the Chrome Web Store update URL, `https://clients2.google.com/service/update2/crx`.</span></span>  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   <span data-ttu-id="5ee9d-121">Inicie o navegador e vá para `edge://extensions` ; você deve ver a extensão listada.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-121">Launch the browser and go to `edge://extensions`; you should see the extension listed.</span></span>  

## <span data-ttu-id="5ee9d-122">Atualização e desinstalação</span><span class="sxs-lookup"><span data-stu-id="5ee9d-122">Updating and uninstalling</span></span>  

<span data-ttu-id="5ee9d-123">O Microsoft Edge verifica as entradas de metadados no registro toda vez que o navegador é iniciado e faz as alterações necessárias nas extensões externas instaladas.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-123">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any necessary changes to the installed external extensions.</span></span>  

<span data-ttu-id="5ee9d-124">Para atualizar a extensão para uma nova versão, atualize o arquivo e atualize a versão no registro.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-124">To update your extension to a new version, update the file, and then update the version in the registry.</span></span>  

<span data-ttu-id="5ee9d-125">Para desinstalar a extensão \ (por exemplo, se o seu software for desinstalado \), remova o arquivo de preferência \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) ou os metadados do registro.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-125">To uninstall your extension \(for example, if your software is uninstalled\), remove your preference file \(`aaaaaaaaaabbbbbbbbbbcccccccccc.json`\) or the metadata from the registry.</span></span>  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="5ee9d-126">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5ee9d-126">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5ee9d-127">A página original foi encontrada [aqui](https://developer.chrome.com/apps/external_extensions).</span><span class="sxs-lookup"><span data-stu-id="5ee9d-127">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5ee9d-129">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5ee9d-129">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
