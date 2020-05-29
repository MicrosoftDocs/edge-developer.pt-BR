---
description: Diferença entre mensagens nativas da documentação do Chrome
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561313"
---
# <span data-ttu-id="12301-104">Sistema de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="12301-104">Native Messaging</span></span>  

<span data-ttu-id="12301-105">O Microsoft Edge agora permite a extensão instalada do catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \) para trocar mensagens com um aplicativo nativo usando APIs de transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="12301-105">Microsoft Edge now allows Extension installed from Microsoft Edge Addons catalog \(Microsoft Edge Addons\) to exchange messages with a native application using message passing APIs.</span></span>  <span data-ttu-id="12301-106">Para habilitar o recurso, você precisa se certificar dos seguintes itens ao implementar o host de mensagens nativa do seu aplicativo nativo.</span><span class="sxs-lookup"><span data-stu-id="12301-106">To enable the feature, you need to make sure of following things while implementing native messaging host of your Native Application.</span></span>  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  <span data-ttu-id="12301-107">**Host de mensagens nativa**:</span><span class="sxs-lookup"><span data-stu-id="12301-107">**Native messaging host**:</span></span>  
    
    <span data-ttu-id="12301-108">Para registrar um host de mensagens nativa, o aplicativo deve instalar um arquivo de manifesto que define a configuração do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="12301-108">In order to register a native messaging host the application must install a manifest file that defines the native messaging host configuration.</span></span>  <span data-ttu-id="12301-109">Veja a seguir um exemplo do arquivo de manifesto:</span><span class="sxs-lookup"><span data-stu-id="12301-109">Below is an example of the manifest file:</span></span>  
    
    ```xml
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
    ```  
    
<span data-ttu-id="12301-110">O arquivo de manifesto do host de mensagens nativa deve ser um JSON válido e contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="12301-110">The native messaging host manifest file must be valid JSON and contains the following fields:</span></span>  

| <span data-ttu-id="12301-111">Nome</span><span class="sxs-lookup"><span data-stu-id="12301-111">Name</span></span> | <span data-ttu-id="12301-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="12301-112">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="12301-113">Nome do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="12301-113">Name of the native messaging host.</span></span> <span data-ttu-id="12301-114">Os clientes passam esta cadeia de caracteres para `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="12301-114">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="12301-115">Esse nome deve conter apenas caracteres alfanuméricos minúsculos, sublinhados e pontos.</span><span class="sxs-lookup"><span data-stu-id="12301-115">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="12301-116">O nome não deve começar ou terminar com um ponto e um ponto não deve ser seguido por outro ponto.</span><span class="sxs-lookup"><span data-stu-id="12301-116">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="12301-117">Breve descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="12301-117">Short application description.</span></span> |  
| `path` | <span data-ttu-id="12301-118">Caminho para o binário do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="12301-118">Path to the native messaging host binary.</span></span>  <span data-ttu-id="12301-119">No Windows, o caminho pode ser relativo ao diretório no qual o arquivo de manifesto está localizado.</span><span class="sxs-lookup"><span data-stu-id="12301-119">On Windows, the path may be relative to the directory in which the manifest file is located.</span></span>  <span data-ttu-id="12301-120">No macOS, o caminho deve ser absoluto.</span><span class="sxs-lookup"><span data-stu-id="12301-120">On macOS, the path must be absolute.</span></span>  <span data-ttu-id="12301-121">O processo de host é iniciado com o diretório atual definido como o diretório que contém o binário do host.</span><span class="sxs-lookup"><span data-stu-id="12301-121">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="12301-122">Por exemplo, se esse parâmetro for definido como `C:\Application\nm_host.exe` , o binário será iniciado usando o diretório atual `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="12301-122">For example if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="12301-123">Tipo de interface usado para se comunicar com o host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="12301-123">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="12301-124">Atualmente, há apenas um valor possível para esse parâmetro: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="12301-124">Currently there is only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="12301-125">Esse valor indica que o Chrome deve usar `stdin` e `stdout` para se comunicar com o host.</span><span class="sxs-lookup"><span data-stu-id="12301-125">This value indicates that Chrome should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="12301-126">lista de extensões que devem acessar o host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="12301-126">list of Extension that should access to the native messaging host.</span></span>  <span data-ttu-id="12301-127">Para habilitar o aplicativo nativo para identificar e se comunicar com o Microsoft Edge addons Extension, defina- `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` o no seu arquivo de manifesto do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="12301-127">To enable your Native Application identify and communicate with Microsoft Edge Addons Extension, set `allowedorigins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  

1.  **<span data-ttu-id="12301-128">Local do host de mensagens nativa</span><span class="sxs-lookup"><span data-stu-id="12301-128">Native messaging host location</span></span>**  
    
    <span data-ttu-id="12301-129">O local do arquivo de manifesto depende da plataforma.</span><span class="sxs-lookup"><span data-stu-id="12301-129">The location of the manifest file depends on the platform.</span></span>  
    
    <span data-ttu-id="12301-130">No Windows, o arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="12301-130">On Windows, the manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="12301-131">O instalador do aplicativo deve criar a chave do registro</span><span class="sxs-lookup"><span data-stu-id="12301-131">The application installer must create registry key</span></span>  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="12301-132">ou</span><span class="sxs-lookup"><span data-stu-id="12301-132">or</span></span>  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="12301-133">,</span><span class="sxs-lookup"><span data-stu-id="12301-133">,</span></span>  
    
    <span data-ttu-id="12301-134">e defina o valor padrão dessa chave para o caminho completo para o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="12301-134">and set default value of that key to the full path to the manifest file.</span></span>  <span data-ttu-id="12301-135">Por exemplo, usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="12301-135">For example, using the following command:</span></span>  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    <span data-ttu-id="12301-136">ou use o seguinte arquivo. reg:</span><span class="sxs-lookup"><span data-stu-id="12301-136">or using the following .reg file:</span></span>  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    <span data-ttu-id="12301-137">Quando o Microsoft Edge procura hosts de mensagens nativos, o registro de 32 bits é consultado primeiro e, em seguida, o registro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="12301-137">When Microsoft Edge looks for native messaging hosts, the 32-bit registry is queried first, then the 64-bit registry.</span></span>  

<span data-ttu-id="12301-138">No macOS, os hosts de mensagens nativas de todo o sistema são pesquisados em um local fixo, enquanto os hosts de mensagens nativas em nível de usuário são pesquisados em um subdiretório no diretório de perfil do usuário chamado `NativeMessagingHosts` .</span><span class="sxs-lookup"><span data-stu-id="12301-138">On macOS, the system-wide native messaging hosts are looked up at a fixed location, while the user-level native messaging hosts are looked up in a subdirectory within the user profile directory called `NativeMessagingHosts`.</span></span>  

<span data-ttu-id="12301-139">Microsoft Edge no macOS \ (todo o sistema \):</span><span class="sxs-lookup"><span data-stu-id="12301-139">Microsoft Edge on macOS \(system-wide\) :</span></span>  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

<span data-ttu-id="12301-140">Microsoft Edge no macOS \ (caminho padrão específico do usuário \):</span><span class="sxs-lookup"><span data-stu-id="12301-140">Microsoft Edge on macOS \(user-specific, default path\):</span></span>  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` <span data-ttu-id="12301-141">pode ser Canárias, dev ou beta.</span><span class="sxs-lookup"><span data-stu-id="12301-141">may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="12301-142">Para canal estável, só `Microsoft Edge` deve ser usado, `<ChannelName`>' não é necessário.</span><span class="sxs-lookup"><span data-stu-id="12301-142">For stable channel, only `Microsoft Edge` should be used, `<ChannelName`>\` is not required.</span></span>

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="12301-143">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="12301-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="12301-144">A página original foi encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="12301-144">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="12301-146">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="12301-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
