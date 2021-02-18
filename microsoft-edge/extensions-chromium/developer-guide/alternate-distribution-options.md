---
description: Saiba como distribuir extensões usando métodos alternativos que não usam armazenamentos verificados
title: Método alternativo para distribuir extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 3b2c72e13488632e2fadea2a7e8eb95888f67170
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343146"
---
# <span data-ttu-id="795da-104">Métodos de distribuição de extensão alternativos</span><span class="sxs-lookup"><span data-stu-id="795da-104">Alternate extension distribution methods</span></span>  

<span data-ttu-id="795da-105">Geralmente, as extensões são distribuídas por meio do armazenamento de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795da-105">Generally, extensions are distributed through the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="795da-106">Há alguns cenários em que os desenvolvedores talvez precisem distribuir extensões usando métodos alternativos.</span><span class="sxs-lookup"><span data-stu-id="795da-106">There are some scenarios where developers may need to distribute extensions using alternate methods.</span></span> <span data-ttu-id="795da-107">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="795da-107">For example:</span></span>

1.  <span data-ttu-id="795da-108">A extensão está associada a outro software e deve ser instalada junto com o restante do software empacotado.</span><span class="sxs-lookup"><span data-stu-id="795da-108">The extension is associated with other software, and it should be installed together with the rest of the bundled software.</span></span>   
1.  <span data-ttu-id="795da-109">Os administradores de rede querem distribuir uma extensão em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="795da-109">Network administrators want to distribute an extension throughout their organization.</span></span>   

<span data-ttu-id="795da-110">Extensões que não são carregadas do armazenamento de Complementos de Borda são conhecidas como extensões instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="795da-110">Extensions that are not loaded from the Edge Add-ons store are referred to as externally installed extensions.</span></span> <span data-ttu-id="795da-111">A lista a seguir fornece métodos alternativos de distribuição de extensões instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="795da-111">The following list provides alternate methods of distributing externally installed extensions.</span></span> 

*   <span data-ttu-id="795da-112">Use o Registro do Windows (somente Windows).</span><span class="sxs-lookup"><span data-stu-id="795da-112">Use the Windows registry (Windows only).</span></span>  
*   <span data-ttu-id="795da-113">Use um arquivo JSON de preferências (macOS e Linux).</span><span class="sxs-lookup"><span data-stu-id="795da-113">Use a preferences JSON file (macOS and Linux).</span></span>  
    
## <span data-ttu-id="795da-114">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="795da-114">Before you begin</span></span>  

<span data-ttu-id="795da-115">Certifique-se de publicar sua extensão no armazenamento de Complementos do Microsoft Edge ou empacote um arquivo e certifique-se de que ele seja instalado com `.crx` êxito no computador.</span><span class="sxs-lookup"><span data-stu-id="795da-115">Ensure that you publish your extension in the Microsoft Edge Add-ons store, or package a `.crx` file and ensure that it installs successfully on your computer.</span></span>  <span data-ttu-id="795da-116">Se você instalar o `.crx` arquivo usando o , `update_URL` certifique-se de navegar até sua extensão nessa URL.</span><span class="sxs-lookup"><span data-stu-id="795da-116">If you install the `.crx` file using the `update_URL`, ensure you can navigate to your extension at that URL.</span></span>  

<span data-ttu-id="795da-117">Além disso, verifique se você tem as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="795da-117">Also, ensure that you have the following information.</span></span>    

1.  <span data-ttu-id="795da-118">O caminho do arquivo `.crx` ou a `update_URL` extensão.</span><span class="sxs-lookup"><span data-stu-id="795da-118">The file path of the `.crx` file, or the `update_URL` of your extension.</span></span>
1.  <span data-ttu-id="795da-119">A versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="795da-119">The version of your extension.</span></span>  <span data-ttu-id="795da-120">As informações de versão estão disponíveis no arquivo de manifesto ou no Microsoft Edge depois `edge://extensions` que você carrega a extensão empacotada.</span><span class="sxs-lookup"><span data-stu-id="795da-120">The version information is available in your manifest file, or in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>   
1.  <span data-ttu-id="795da-121">A ID da extensão.</span><span class="sxs-lookup"><span data-stu-id="795da-121">The ID of your extension.</span></span>  <span data-ttu-id="795da-122">As informações de ID estarão disponíveis no Microsoft Edge depois `edge://extensions` que você carregar a extensão empacotada.</span><span class="sxs-lookup"><span data-stu-id="795da-122">The ID information is available in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>  

> [!NOTE] 
> <span data-ttu-id="795da-123">Os exemplos a seguir `1.0` usam como a versão e para a `aaaaaaaaaabbbbbbbbbbcccccccccc` ID.</span><span class="sxs-lookup"><span data-stu-id="795da-123">The following examples use `1.0` as the version, and `aaaaaaaaaabbbbbbbbbbcccccccccc` for the ID.</span></span>  

## <span data-ttu-id="795da-124">Usar o Registro do Windows (somente Windows)</span><span class="sxs-lookup"><span data-stu-id="795da-124">Use the Windows registry (Windows only)</span></span>  

<span data-ttu-id="795da-125">Para distribuir sua extensão usando o Registro do Windows, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="795da-125">To distribute your extension using the Windows registry, perform the following steps.</span></span>

1.  <span data-ttu-id="795da-126">Encontre ou crie a seguinte chave no Registro:</span><span class="sxs-lookup"><span data-stu-id="795da-126">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="795da-127">Windows de 32 bits:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="795da-127">32-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`.</span></span>  
    *   <span data-ttu-id="795da-128">Windows de 64 bits:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="795da-128">64-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`.</span></span>  
1.  <span data-ttu-id="795da-129">Crie uma nova chave ou pasta em **Extensões** com o mesmo nome da ID da extensão.</span><span class="sxs-lookup"><span data-stu-id="795da-129">Create a new key, or folder, under **Extensions** with the same name as the ID of your extension.</span></span> <span data-ttu-id="795da-130">Por exemplo, crie a chave com o `aaaaaaaaaabbbbbbbbbbcccccccccc` nome.</span><span class="sxs-lookup"><span data-stu-id="795da-130">For example, create the key with the name `aaaaaaaaaabbbbbbbbbbcccccccccc`.</span></span>  
1.  <span data-ttu-id="795da-131">Na chave **Extensions,** crie a `update_url` propriedade e de definida o valor como `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="795da-131">In the **Extensions** key, create the `update_url` property, and set the value to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="795da-132">A propriedade aponta para o arquivo da extensão no armazenamento de `update_url` `.crx` Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="795da-132">The `update_url` property points to the `.crx` file of your extension in the Microsoft Edge Add-ons store.</span></span>  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="795da-133">Se você quiser instalar uma extensão da Chrome Web Store, de definida como `update_url` `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="795da-133">If you want to install an extension from the Chrome Web Store, set the value of `update_url` to `https://clients2.google.com/service/update2/crx`.</span></span>  
  
1.  <span data-ttu-id="795da-134">Verifique se sua extensão está listada no Microsoft Edge navegando até `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="795da-134">Verify that your extension is listed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="795da-135">Usar um arquivo JSON de preferências (macOS e Linux)</span><span class="sxs-lookup"><span data-stu-id="795da-135">Use a preferences JSON file (macOS and Linux)</span></span>  

<span data-ttu-id="795da-136">Para distribuir sua extensão usando um arquivo JSON de preferências, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="795da-136">To distribute your extension using a preferences JSON file, perform the following steps.</span></span>

1.  <span data-ttu-id="795da-137">Ao usar o Linux, verifique se o arquivo de extensão está disponível no computador em que a extensão `.crx` será instalada.</span><span class="sxs-lookup"><span data-stu-id="795da-137">When using Linux, ensure your `.crx` extension file is available on the machine that the extension will be installed on.</span></span> <span data-ttu-id="795da-138">Copie o arquivo de extensão para um diretório local ou use um compartilhamento de rede `.crx` acessível do computador.</span><span class="sxs-lookup"><span data-stu-id="795da-138">Copy the `.crx` extension file to a local directory, or use a  network share that is reachable from the machine.</span></span> 
1.  <span data-ttu-id="795da-139">Crie um arquivo JSON em que o nome do arquivo corresponda à ID da extensão.</span><span class="sxs-lookup"><span data-stu-id="795da-139">Create a JSON file where the name of the file corresponds to the ID of your extension.</span></span> <span data-ttu-id="795da-140">Por exemplo, crie um arquivo JSON com o nome de `aaaaaaaaaabbbbbbbbbbcccccccccc.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="795da-140">For example, create a JSON file with the file name `aaaaaaaaaabbbbbbbbbbcccccccccc.json`.</span></span>  
1.  <span data-ttu-id="795da-141">Dependendo do sistema operacional, salve o arquivo JSON em uma das pastas a seguir.</span><span class="sxs-lookup"><span data-stu-id="795da-141">Depending on your operating system, save the JSON file to one of the following folders.</span></span>   
    *   **<span data-ttu-id="795da-142">macOS</span><span class="sxs-lookup"><span data-stu-id="795da-142">macOS</span></span>**  
        *   <span data-ttu-id="795da-143">Específico do usuário:</span><span class="sxs-lookup"><span data-stu-id="795da-143">User specific:</span></span> `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   <span data-ttu-id="795da-144">Todos os usuários:</span><span class="sxs-lookup"><span data-stu-id="795da-144">All users:</span></span> `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        <span data-ttu-id="795da-145">Para impedir que usuários não autorizados instalem extensões para todos os usuários, verifique se o arquivo de extensão é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="795da-145">To prevent unauthorized users from installing extensions for all users, ensure your extension file is read only.</span></span> <span data-ttu-id="795da-146">Além disso, certifique-se de que as seguintes condições sejam atendidas:</span><span class="sxs-lookup"><span data-stu-id="795da-146">Additionally, ensure that the following conditions are met:</span></span>
        
        *   <span data-ttu-id="795da-147">Cada diretório no caminho pertence à raiz do usuário.</span><span class="sxs-lookup"><span data-stu-id="795da-147">Every directory in the path is owned by the user root.</span></span>  
        *   <span data-ttu-id="795da-148">Todos os diretórios no caminho são atribuídos ao `admin` grupo `wheel` ou ao grupo.</span><span class="sxs-lookup"><span data-stu-id="795da-148">Every directory in the path is assigned to the `admin` or `wheel` group.</span></span>  
        *   <span data-ttu-id="795da-149">Cada diretório no caminho não é world writable.</span><span class="sxs-lookup"><span data-stu-id="795da-149">Every directory in the path isn't world writable.</span></span>  
        *   <span data-ttu-id="795da-150">O caminho também deve estar livre de links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="795da-150">The path must also be free of symbolic links.</span></span>  
        
    *   **<span data-ttu-id="795da-151">Linux</span><span class="sxs-lookup"><span data-stu-id="795da-151">Linux</span></span>**  
        *   <span data-ttu-id="795da-152">Específico do usuário:</span><span class="sxs-lookup"><span data-stu-id="795da-152">User specific:</span></span> `~/.config/microsoft-edge/External Extensions/`  
        *   <span data-ttu-id="795da-153">Todos os usuários:</span><span class="sxs-lookup"><span data-stu-id="795da-153">All users:</span></span> `/usr/share/microsoft-edge/extensions/`  
1.  <span data-ttu-id="795da-154">Dependendo do cenário, copie o código apropriado que segue para o arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="795da-154">Depending on your scenario, copy the appropriate code that follows to your JSON file.</span></span> 
    *   <span data-ttu-id="795da-155">Aplica-se somente ao Linux.</span><span class="sxs-lookup"><span data-stu-id="795da-155">Applies to Linux only.</span></span> <span data-ttu-id="795da-156">Se você instalar a partir de um arquivo, especifique o local e a versão usando `external_crx` e `external_version` .</span><span class="sxs-lookup"><span data-stu-id="795da-156">If you install from a file, specify the location and version using `external_crx` and `external_version`.</span></span>  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   <span data-ttu-id="795da-157">Aplica-se ao macOS e Ao Linux.</span><span class="sxs-lookup"><span data-stu-id="795da-157">Applies to macOS and Linux.</span></span> <span data-ttu-id="795da-158">Se você instalar a partir de `update_URL` um , especifique a URL de atualização usando `external_update_url` .</span><span class="sxs-lookup"><span data-stu-id="795da-158">If you install from an `update_URL`, specify the update URL using `external_update_url`.</span></span> 
        
        <span data-ttu-id="795da-159">Copie o código a seguir para o arquivo JSON ao instalar a partir de arquivos locais `.crx` somente no Linux.</span><span class="sxs-lookup"><span data-stu-id="795da-159">Copy the following code to your JSON file when installing from local `.crx` files on Linux only.</span></span>  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  <span data-ttu-id="795da-160">Copie o código a seguir para o arquivo JSON ao instalar a partir da loja de Complementos do Microsoft Edge no macOS e no Linux.</span><span class="sxs-lookup"><span data-stu-id="795da-160">Copy the following code to your JSON file when installing from the Microsoft Edge Add-ons store on macOS and Linux.</span></span>
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  <span data-ttu-id="795da-161">Para instalar extensões para localidades específicas, liste as localidades com suporte usando `supported_locale` .</span><span class="sxs-lookup"><span data-stu-id="795da-161">To install extensions for specific locales, list the supported locales using `supported_locale`.</span></span>  <span data-ttu-id="795da-162">Você também pode especificar localidades pai para instalar sua extensão para todas as localidades de idioma que usam esse pai.</span><span class="sxs-lookup"><span data-stu-id="795da-162">You may also specify parent locales to install your extension for all language locales that use that parent.</span></span> <span data-ttu-id="795da-163">Por exemplo, ao usar a localidade pai, sua extensão é instalada para todas as localidades em inglês, como `en` , e assim por `en-US` `en-GB` diante.</span><span class="sxs-lookup"><span data-stu-id="795da-163">For example, when using the parent locale `en`, your extension installs for all English locales, such as `en-US`, `en-GB`, and so on.</span></span>  <span data-ttu-id="795da-164">Quando os usuários alteram sua localidade no navegador, as extensões instaladas externamente são desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="795da-164">When users change their locale in their browser, externally installed extensions are uninstalled.</span></span>  <span data-ttu-id="795da-165">Para instalar sua extensão para qualquer localidade, não `supported_locales` use.</span><span class="sxs-lookup"><span data-stu-id="795da-165">To install your extension for any locale, do not use `supported_locales`.</span></span>  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  <span data-ttu-id="795da-166">Verifique se sua extensão está instalada no Microsoft Edge navegando até `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="795da-166">Verify that your extension is installed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="795da-167">Atualizar e desinstalar extensões instaladas externamente</span><span class="sxs-lookup"><span data-stu-id="795da-167">Update and uninstall externally installed extensions</span></span>

<span data-ttu-id="795da-168">O Microsoft Edge examina as entradas de metadados no Registro sempre que o navegador é iniciado e faz alterações nas extensões instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="795da-168">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any changes to the externally installed extensions.</span></span>  

<span data-ttu-id="795da-169">Para atualizar sua extensão para uma nova versão, atualize a versão no arquivo de manifesto e atualize a versão no Registro.</span><span class="sxs-lookup"><span data-stu-id="795da-169">To update your extension to a new version, update the version in the manifest file, and then update the version in the registry.</span></span>  

<span data-ttu-id="795da-170">Talvez seja necessário desinstalar extensões instaladas externamente, que foram instaladas como parte de um pacote de software instalado anteriormente no computador.</span><span class="sxs-lookup"><span data-stu-id="795da-170">You may need to uninstall externally installed extensions, which were installed as part of a bundle of software that was previously installed on the machine.</span></span>  <span data-ttu-id="795da-171">Para desinstalar sua extensão, remova o arquivo JSON de preferências ou remova a chave do Registro.</span><span class="sxs-lookup"><span data-stu-id="795da-171">To uninstall your extension, remove your preferences JSON file or remove the key from the registry.</span></span>   

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="795da-172">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="795da-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  <span data-ttu-id="795da-173">A página original é encontrada [aqui.](https://developer.chrome.com/apps/external_extensions)</span><span class="sxs-lookup"><span data-stu-id="795da-173">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="795da-175">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="795da-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
