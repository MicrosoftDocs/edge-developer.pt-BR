---
description: Documentação de mensagens nativas
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100249"
---
# <span data-ttu-id="15272-104">Sistema de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="15272-104">Native messaging</span></span>  

<span data-ttu-id="15272-105">As extensões se comunicam com um aplicativo Win32 nativo instalado em um dispositivo de usuário usando APIs de transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="15272-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="15272-106">O host do aplicativo nativo envia e recebe mensagens com extensões usando a entrada padrão e a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="15272-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="15272-107">As extensões que usam o recurso de mensagens nativas são instaladas no Microsoft Edge semelhantes a qualquer outra extensão.</span><span class="sxs-lookup"><span data-stu-id="15272-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="15272-108">No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="15272-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="15272-109">Para adquirir a extensão e o host de aplicativo nativo, você tem dois modelos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="15272-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="15272-110">Empacote a extensão e o host juntos.</span><span class="sxs-lookup"><span data-stu-id="15272-110">Package your extension and the host together.</span></span>  <span data-ttu-id="15272-111">Quando um usuário instala o pacote, a extensão e o host são instalados.</span><span class="sxs-lookup"><span data-stu-id="15272-111">When a user installs the package, both the extension and the host are installed.</span></span>
*   <span data-ttu-id="15272-112">Instale a extensão usando o [repositório Complementos do Microsoft Edge][EdgeAddons]e sua extensão solicitará que os usuários instalem o host.</span><span class="sxs-lookup"><span data-stu-id="15272-112">Install your extension using the [Microsoft Edge Add-ons store][EdgeAddons], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="15272-113">Para criar a extensão para enviar e receber mensagens com hosts de aplicativos nativos, consulte as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="15272-114">Etapa 1-adicionar permissões ao manifesto de extensão</span><span class="sxs-lookup"><span data-stu-id="15272-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="15272-115">Adicione a `nativeMessaging` permissão ao **manifest.jsem** arquivo da extensão.</span><span class="sxs-lookup"><span data-stu-id="15272-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="15272-116">O trecho de código a seguir é um exemplo de **manifest.js**.</span><span class="sxs-lookup"><span data-stu-id="15272-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="15272-117">Etapa 2-criar seu arquivo de manifesto do host de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="15272-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="15272-118">Aplicativos nativos devem fornecer um arquivo de manifesto de host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="15272-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="15272-119">O arquivo de manifesto contém o caminho para o tempo de execução do host de mensagens nativa, o método de comunicação com a extensão e uma lista de extensões permitidas às quais ela se comunica.</span><span class="sxs-lookup"><span data-stu-id="15272-119">The manifest file contains the path to the native messaging host runtime, the method of communication with the extension, and a list of allowed extensions to which it communicates.</span></span>  <span data-ttu-id="15272-120">O navegador lê e valida o manifesto do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="15272-120">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="15272-121">O navegador não instala ou gerencia o arquivo de manifesto de host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="15272-121">The browser does not install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="15272-122">O arquivo de manifesto host deve ser um arquivo JSON válido que contém as teclas a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-122">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="15272-123">Especifica o nome do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="15272-123">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="15272-124">Os clientes passam esta cadeia de caracteres para `runtime.connectNative` ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="15272-124">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="15272-125">Esse valor só deve conter caracteres alfanuméricos minúsculos, sublinhados e pontos.</span><span class="sxs-lookup"><span data-stu-id="15272-125">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="15272-126">Esse valor não deve começar ou terminar com um ponto e um ponto não deve ser seguido por outro ponto.</span><span class="sxs-lookup"><span data-stu-id="15272-126">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="15272-127">Descreve o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15272-127">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="15272-128">Especifica o caminho para o binário do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="15272-128">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="15272-129">Em dispositivos Windows, você pode usar caminhos relativos para o diretório que contém o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="15272-129">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="15272-130">No macOS e no Linux, o caminho deve ser absoluto.</span><span class="sxs-lookup"><span data-stu-id="15272-130">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="15272-131">O processo de host começa com o diretório atual definido para o diretório que contém o binário do host.</span><span class="sxs-lookup"><span data-stu-id="15272-131">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="15272-132">Por exemplo, \ (Windows \), se esse parâmetro for definido como `C:\Application\nm_host.exe` , o binário será iniciado usando o diretório atual \ ( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="15272-132">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="15272-133">Especifica o tipo de interface usado para se comunicar com o host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="15272-133">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="15272-134">Esse valor instrui o Microsoft Edge a usar `stdin` e `stdout` a se comunicar com o host.</span><span class="sxs-lookup"><span data-stu-id="15272-134">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="15272-135">O único valor aceitável é `stdio` .</span><span class="sxs-lookup"><span data-stu-id="15272-135">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="15272-136">Especifica a lista de extensões que têm acesso ao host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="15272-136">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="15272-137">Para permitir que o aplicativo identifique e se comunique com uma extensão, no seu arquivo de manifesto do host de mensagens nativa defina o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-137">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="15272-138">Sideload sua extensão para testar o sistema de mensagens nativa com o host.</span><span class="sxs-lookup"><span data-stu-id="15272-138">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="15272-139">Para Sideload a extensão durante o desenvolvimento e a recuperação `microsoft_catalog_extension_id` , conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-139">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="15272-140">Navegue até `edge://extensions` e, em seguida, ative o botão de alternância do modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="15272-140">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="15272-141">Escolha **carregar desempacotados**e, em seguida, selecione o pacote de extensão para Sideload.</span><span class="sxs-lookup"><span data-stu-id="15272-141">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="15272-142">Escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="15272-142">Choose **OK**.</span></span>
1.  <span data-ttu-id="15272-143">Navegue até a `edge://extensions` página e verifique se a extensão está listada.</span><span class="sxs-lookup"><span data-stu-id="15272-143">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="15272-144">Copie a chave de `microsoft_catalog_extension_id` \ (ID \) da listagem de extensão na página.</span><span class="sxs-lookup"><span data-stu-id="15272-144">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>

<span data-ttu-id="15272-145">Quando estiver pronto para distribuir a extensão para os usuários, publique a extensão no repositório de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="15272-145">When you are ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="15272-146">A ID da extensão da extensão publicada pode ser diferente da ID usada durante o Sideload da extensão.</span><span class="sxs-lookup"><span data-stu-id="15272-146">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="15272-147">Se a ID foi alterada, atualize `allowed_origins` o arquivo de manifesto host com a ID da extensão publicada.</span><span class="sxs-lookup"><span data-stu-id="15272-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="15272-148">Etapa 3-copiar o arquivo de manifesto do sistema de mensagens nativo para seu sistema</span><span class="sxs-lookup"><span data-stu-id="15272-148">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="15272-149">A etapa final envolve copiar o arquivo de manifesto do sistema de mensagens nativo para seu computador e garantir que ele esteja configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="15272-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it is configured correctly.</span></span>  <span data-ttu-id="15272-150">Para garantir que o arquivo de manifesto seja colocado no local esperado, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-150">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="15272-151">O local varia de acordo com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="15272-151">The location varies by platform.</span></span>  

### [<span data-ttu-id="15272-152">Windows</span><span class="sxs-lookup"><span data-stu-id="15272-152">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="15272-153">O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="15272-153">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="15272-154">O instalador do aplicativo deve criar uma chave do registro e definir o valor padrão dessa chave para o caminho completo do arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="15272-154">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="15272-155">Os comandos a seguir são exemplos de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="15272-155">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="15272-156">Para adicionar uma chave do registro ao diretório com a chave de manifesto.</span><span class="sxs-lookup"><span data-stu-id="15272-156">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="15272-157">Comando executar no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="15272-157">Run command in command prompt.</span></span>    
    
    1.  <span data-ttu-id="15272-158">Execute o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-158">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="15272-159">Crie um `.reg` arquivo e execute-o.</span><span class="sxs-lookup"><span data-stu-id="15272-159">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="15272-160">Copie o seguinte comando em um `.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="15272-160">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="15272-161">Executar o `.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="15272-161">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="15272-162">O Microsoft Edge consulta o registro de 32 bits primeiro e, em seguida, o registro de 64 bits para identificar hosts de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="15272-162">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span>  <span data-ttu-id="15272-163">Se você executar o `.reg` arquivo acima como parte de um script em lotes, certifique-se de executá-lo usando um prompt de comando de administrador.</span><span class="sxs-lookup"><span data-stu-id="15272-163">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="15272-164">macOS</span><span class="sxs-lookup"><span data-stu-id="15272-164">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="15272-165">Para armazenar o arquivo de manifesto, execute uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="15272-165">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="15272-166">Hosts de mensagens nativas de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="15272-166">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="15272-167">Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-167">For example, the manifest file must be stored in following location.</span></span> 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="15272-168">Hosts de mensagens nativas específicas do usuário, que estão disponíveis somente para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="15272-168">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="15272-169">Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-169">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="15272-170">O  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` deve ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="15272-170">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="15272-171">Canary</span><span class="sxs-lookup"><span data-stu-id="15272-171">Canary</span></span>  
    *   <span data-ttu-id="15272-172">Dev</span><span class="sxs-lookup"><span data-stu-id="15272-172">Dev</span></span>  
    *   <span data-ttu-id="15272-173">Beta</span><span class="sxs-lookup"><span data-stu-id="15272-173">Beta</span></span>  

    <span data-ttu-id="15272-174">Não é necessário usar o canal estável `{Channel_Name}` .</span><span class="sxs-lookup"><span data-stu-id="15272-174">When using the Stable channel, `{Channel_Name}` is not required.</span></span>  

### [<span data-ttu-id="15272-175">Linux</span><span class="sxs-lookup"><span data-stu-id="15272-175">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="15272-176">Para armazenar o arquivo de manifesto, execute uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="15272-176">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="15272-177">Hosts de mensagens nativas de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="15272-177">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="15272-178">O arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-178">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="15272-179">Hosts de mensagens nativas específicas do usuário, que estão disponíveis somente para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="15272-179">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="15272-180">O arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="15272-180">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="15272-181">Certifique-se de fornecer permissões de leitura no arquivo de manifesto e executar permissões no tempo de execução do host.</span><span class="sxs-lookup"><span data-stu-id="15272-181">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="15272-182">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="15272-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="15272-183">A página original foi encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="15272-183">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="15272-185">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15272-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
