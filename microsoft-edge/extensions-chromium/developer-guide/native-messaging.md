---
description: Documentação de mensagens nativas
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088552"
---
# <span data-ttu-id="16b46-104">Sistema de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="16b46-104">Native messaging</span></span>  

<span data-ttu-id="16b46-105">As extensões podem se comunicar com um aplicativo Win32 nativo instalado em um dispositivo de usuário usando APIs de transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="16b46-105">Extensions can communicate with a native Win32 application installed on a user’s device using message passing APIs.</span></span> <span data-ttu-id="16b46-106">O host do aplicativo nativo pode enviar e receber mensagens com extensões usando a entrada padrão e a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="16b46-106">The native application host can send and receive messages with extensions using standard input and standard output.</span></span> <span data-ttu-id="16b46-107">As extensões que usam o recurso de mensagens nativas são instaladas no Microsoft Edge semelhantes a qualquer outra extensão.</span><span class="sxs-lookup"><span data-stu-id="16b46-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span> <span data-ttu-id="16b46-108">No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="16b46-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>

<span data-ttu-id="16b46-109">Para adquirir a extensão e o host do aplicativo nativo, você pode:</span><span class="sxs-lookup"><span data-stu-id="16b46-109">To acquire the extension and native application host, you can:</span></span>

1. <span data-ttu-id="16b46-110">Empacote a extensão e o host juntos.</span><span class="sxs-lookup"><span data-stu-id="16b46-110">Package the extension and the host together.</span></span> <span data-ttu-id="16b46-111">Quando os usuários instalam o pacote, a extensão e o host são instalados.</span><span class="sxs-lookup"><span data-stu-id="16b46-111">When users install the package, both the extension and the host are installed.</span></span>
1. <span data-ttu-id="16b46-112">Instale a extensão do [repositório de Complementos do Microsoft Edge][EdgeAddons]e faça com que sua extensão solicite que os usuários instalem o host.</span><span class="sxs-lookup"><span data-stu-id="16b46-112">Install the extension from the [Microsoft Edge Add-ons store][EdgeAddons], and have your extension prompt users to install the host.</span></span> 

<span data-ttu-id="16b46-113">Confira as etapas abaixo para configurar a extensão para enviar e receber mensagens com hosts de aplicativos nativos.</span><span class="sxs-lookup"><span data-stu-id="16b46-113">Refer to the steps below to setup your extension to send and receive messages with native application hosts.</span></span>

### <span data-ttu-id="16b46-114">Etapa 1: adicionar permissões ao manifesto de extensão</span><span class="sxs-lookup"><span data-stu-id="16b46-114">Step 1: Add permissions to the extension manifest</span></span>

<span data-ttu-id="16b46-115">Adicione a permissão nativeMessaging para omanifest.jsdo ramal \*\* no\*\* arquivo.</span><span class="sxs-lookup"><span data-stu-id="16b46-115">Add the nativeMessaging permission to the extension’s **manifest.json** file.</span></span> <span data-ttu-id="16b46-116">Veja a seguir um exemplo de manifest.jsem:</span><span class="sxs-lookup"><span data-stu-id="16b46-116">Below is an example of manifest.json:</span></span>

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```

### <span data-ttu-id="16b46-117">Etapa 2: criar o arquivo de manifesto do seu host de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="16b46-117">Step 2: Create your native messaging host manifest file</span></span>
    
<span data-ttu-id="16b46-118">Aplicativos nativos devem fornecer um arquivo de manifesto de host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="16b46-118">Native applications must provide a native messaging host manifest file.</span></span> <span data-ttu-id="16b46-119">Esse arquivo de manifesto contém o caminho para o executável do host de mensagens nativa, o método de comunicação com a extensão e uma lista de extensões permitidas com as quais ele pode se comunicar.</span><span class="sxs-lookup"><span data-stu-id="16b46-119">This manifest file contains the path to the native messaging host executable, the method of communication with the extension, and a list of allowed extensions it can communicate with.</span></span> <span data-ttu-id="16b46-120">Os navegadores lêem e validam o manifesto do host de mensagens nativa, mas ele nunca é instalado ou gerenciado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="16b46-120">Browsers read and validate the native messaging host manifest, but it’s never installed or managed by the browser.</span></span> <span data-ttu-id="16b46-121">O arquivo de manifesto do host deve ser um arquivo JSON válido contendo os campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="16b46-121">The host manifest file must be a valid json file containing the following fields.</span></span>

    
```json
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




| <span data-ttu-id="16b46-122">Nome</span><span class="sxs-lookup"><span data-stu-id="16b46-122">Name</span></span> | <span data-ttu-id="16b46-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="16b46-123">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="16b46-124">Nome do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="16b46-124">Name of the native messaging host.</span></span> <span data-ttu-id="16b46-125">Os clientes passam esta cadeia de caracteres para `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="16b46-125">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="16b46-126">Esse nome deve conter apenas caracteres alfanuméricos minúsculos, sublinhados e pontos.</span><span class="sxs-lookup"><span data-stu-id="16b46-126">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="16b46-127">O nome não deve começar ou terminar com um ponto e um ponto não deve ser seguido por outro ponto.</span><span class="sxs-lookup"><span data-stu-id="16b46-127">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="16b46-128">Breve descrição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16b46-128">Brief description of the application.</span></span> |  
| `path` | <span data-ttu-id="16b46-129">Caminho para o binário do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="16b46-129">Path to the native messaging host binary.</span></span> <span data-ttu-id="16b46-130">Em dispositivos Windows, você pode usar caminhos relativos para o diretório que contém o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="16b46-130">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span> <span data-ttu-id="16b46-131">No macOS e no Linux, o caminho deve ser absoluto.</span><span class="sxs-lookup"><span data-stu-id="16b46-131">On macOS and Linux, the path must be absolute.</span></span> <span data-ttu-id="16b46-132">O processo de host é iniciado com o diretório atual definido como o diretório que contém o binário do host.</span><span class="sxs-lookup"><span data-stu-id="16b46-132">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="16b46-133">Por exemplo, se esse parâmetro for definido como `C:\Application\nm_host.exe` , o binário será iniciado usando o diretório atual `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="16b46-133">For example, if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="16b46-134">Tipo de interface usado para se comunicar com o host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="16b46-134">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="16b46-135">No momento, há apenas um valor possível para esse parâmetro: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="16b46-135">Currently there's only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="16b46-136">Esse valor indica que o Microsoft Edge deve usar `stdin` e `stdout` para se comunicar com o host.</span><span class="sxs-lookup"><span data-stu-id="16b46-136">This value indicates that Microsoft Edge should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="16b46-137">Lista de extensões que podem ter acesso ao host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="16b46-137">List of extensions that may have access to the native messaging host.</span></span>  <span data-ttu-id="16b46-138">Para permitir que o aplicativo identifique e se comunique com uma extensão, defina- `allowed_origins` `chrome-extension://[Microsoft-Catalog-extensionID]` o como em seu arquivo de manifesto do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="16b46-138">To enable your application to identify and communicate with an extension, set `allowed_origins` to `chrome-extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  


<span data-ttu-id="16b46-139">Durante o desenvolvimento, você pode Sideload sua extensão para testar o recurso de mensagens nativas pelo host:</span><span class="sxs-lookup"><span data-stu-id="16b46-139">While developing, you can sideload your extension to test native messaging with the host by:</span></span>
1. <span data-ttu-id="16b46-140">Navegue até `edge://extensions` e ative o botão de alternância do modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="16b46-140">Navigating to `edge://extensions`, and then turning on the Developer mode toggle button.</span></span> 
1. <span data-ttu-id="16b46-141">Escolha carregar desempacotados e, em seguida, selecione o pacote de extensão para Sideload.</span><span class="sxs-lookup"><span data-stu-id="16b46-141">Choose Load unpacked, and then select your extension package to sideload.</span></span>  
1. <span data-ttu-id="16b46-142">Escolha OK.</span><span class="sxs-lookup"><span data-stu-id="16b46-142">Choose OK.</span></span>
1. <span data-ttu-id="16b46-143">Verifique se a `edge://extensions` página agora lista a extensão.</span><span class="sxs-lookup"><span data-stu-id="16b46-143">Verify the `edge://extensions` page now lists your extension.</span></span> 
1. <span data-ttu-id="16b46-144">Copie a chave de ID da listagem de extensão na página.</span><span class="sxs-lookup"><span data-stu-id="16b46-144">Copy the key from ID from the extension listing on the page.</span></span>

<span data-ttu-id="16b46-145">Quando estiver pronto para distribuir a extensão para os usuários, publique a extensão no repositório de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="16b46-145">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="16b46-146">A ID da extensão da extensão publicada pode ser diferente da ID usada durante a Sideload da extensão.</span><span class="sxs-lookup"><span data-stu-id="16b46-146">The extension ID of the published extension may be different to the ID used while sideloading your extension.</span></span> <span data-ttu-id="16b46-147">Se a ID foi alterada, atualize `allowed_origins` o arquivo de manifesto host com a ID da extensão publicada.</span><span class="sxs-lookup"><span data-stu-id="16b46-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span> 



### <span data-ttu-id="16b46-148">Etapa 3: copiar o arquivo de manifesto do sistema de mensagens nativo para o seu sistema</span><span class="sxs-lookup"><span data-stu-id="16b46-148">Step 3: Copy the native messaging host manifest file to your system</span></span>

<span data-ttu-id="16b46-149">A etapa final envolve copiar o arquivo de manifesto do sistema de mensagens nativo para seu computador e garantir que ele esteja configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="16b46-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it’s configured correctly.</span></span> <span data-ttu-id="16b46-150">Siga as etapas abaixo para garantir que o arquivo de host de mensagens nativa seja colocado no local esperado porque ele varia de acordo com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="16b46-150">Follow the steps below to ensure the native messaging host file is placed in the expected location because it varies by platform.</span></span>
    
<span data-ttu-id="16b46-151">**Windows**.</span><span class="sxs-lookup"><span data-stu-id="16b46-151">**Windows**.</span></span> <span data-ttu-id="16b46-152">O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="16b46-152">The manifest file may be located anywhere in the file system.</span></span> <span data-ttu-id="16b46-153">O instalador do aplicativo deve criar uma chave do registro e definir o valor padrão dessa chave para o caminho completo do arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="16b46-153">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span> <span data-ttu-id="16b46-154">Os comandos a seguir são exemplos de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="16b46-154">The following commands are examples of registry keys.</span></span>
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="16b46-155">ou</span><span class="sxs-lookup"><span data-stu-id="16b46-155">or</span></span>  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="16b46-156">,</span><span class="sxs-lookup"><span data-stu-id="16b46-156">,</span></span>  
    
<span data-ttu-id="16b46-157">Execute o seguinte comando em um prompt de comando para adicionar uma chave do registro à pasta com o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="16b46-157">Run the following command at a command prompt to add a registry key to the folder with the manifest file.</span></span>
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
<span data-ttu-id="16b46-158">Você também pode copiar o comando a seguir para um arquivo. reg e executá-lo para adicionar a chave do registro.</span><span class="sxs-lookup"><span data-stu-id="16b46-158">Alternatively, copy the following command to a .reg file and run it to add the registry key.</span></span> 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  <span data-ttu-id="16b46-159">O Microsoft Edge consulta o registro de 32 bits primeiro e, em seguida, o registro de 64 bits para identificar hosts de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="16b46-159">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span> <span data-ttu-id="16b46-160">Se você executar o arquivo. reg acima como parte de um script em lotes, certifique-se de executá-lo usando um prompt de comando de administrador.</span><span class="sxs-lookup"><span data-stu-id="16b46-160">If you run the above .reg file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>


<span data-ttu-id="16b46-161">**MacOS**.</span><span class="sxs-lookup"><span data-stu-id="16b46-161">**macOS**.</span></span> <span data-ttu-id="16b46-162">O arquivo de manifesto deve ser armazenado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="16b46-162">The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="16b46-163">Hosts de mensagens nativas de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="16b46-163">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span> <span data-ttu-id="16b46-164">Por exemplo, o arquivo de manifesto deve ser armazenado em</span><span class="sxs-lookup"><span data-stu-id="16b46-164">For example, the manifest file must be stored in</span></span> `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. <span data-ttu-id="16b46-165">Hosts de mensagens nativas específicas do usuário, que estão disponíveis somente para o usuário atual, estão localizados no subdiretório NativeMessagingHosts no diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="16b46-165">User-specific native messaging hosts, which are available to the current user only, are located in the NativeMessagingHosts  subdirectory in the user profile directory.</span></span> <span data-ttu-id="16b46-166">Por exemplo, o arquivo de manifesto deve ser armazenado em</span><span class="sxs-lookup"><span data-stu-id="16b46-166">For example, the manifest file must be stored in</span></span>  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    <span data-ttu-id="16b46-167">onde `ChannelName` pode haver Canárias, dev ou beta.</span><span class="sxs-lookup"><span data-stu-id="16b46-167">where `ChannelName` may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="16b46-168">Não é necessário usar o canal estável `ChannelName` .</span><span class="sxs-lookup"><span data-stu-id="16b46-168">When using the Stable channel, `ChannelName` isn't required.</span></span>


<span data-ttu-id="16b46-169">**Linux** O arquivo de manifesto deve ser armazenado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="16b46-169">**Linux** The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="16b46-170">Hosts de mensagens nativas de todo o sistema:  `~/.config/microsoft-edge/NativeMessagingHosts`</span><span class="sxs-lookup"><span data-stu-id="16b46-170">System-wide native messaging hosts:  `~/.config/microsoft-edge/NativeMessagingHosts`</span></span>

1. <span data-ttu-id="16b46-171">Hosts de mensagens nativas específicas do usuário:  `/etc/opt/edge/native-messaging-hosts`</span><span class="sxs-lookup"><span data-stu-id="16b46-171">User-specific native messaging hosts:  `/etc/opt/edge/native-messaging-hosts`</span></span>


> [!NOTE]
> <span data-ttu-id="16b46-172">Certifique-se de fornecer permissões de leitura no arquivo de manifesto e permissões de execução no executável do host.</span><span class="sxs-lookup"><span data-stu-id="16b46-172">Ensure that you provide read permissions on the manifest file, and execute permissions on the host executable.</span></span>


> [!NOTE]
> <span data-ttu-id="16b46-173">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="16b46-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="16b46-174">A página original foi encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="16b46-174">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="16b46-176">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="16b46-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
