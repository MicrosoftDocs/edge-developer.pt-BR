---
description: Documentação de mensagens nativas
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 2d629762d4c7c75832905cfbf8c2d5311191092d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327698"
---
# <span data-ttu-id="2668b-104">Sistema de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="2668b-104">Native messaging</span></span>  

<span data-ttu-id="2668b-105">As extensões se comunicam com um aplicativo Win32 nativo instalado no dispositivo de um usuário usando as APIs de passagem de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2668b-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="2668b-106">O host do aplicativo nativo envia e recebe mensagens com extensões usando entrada padrão e saída padrão.</span><span class="sxs-lookup"><span data-stu-id="2668b-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="2668b-107">Extensões que usam mensagens nativas são instaladas no Microsoft Edge de forma semelhante a qualquer outra extensão.</span><span class="sxs-lookup"><span data-stu-id="2668b-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="2668b-108">No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2668b-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="2668b-109">Para adquirir a extensão e o host de aplicativo nativo, você tem dois modelos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="2668b-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="2668b-110">Empacote sua extensão e o host juntos.</span><span class="sxs-lookup"><span data-stu-id="2668b-110">Package your extension and the host together.</span></span>  <span data-ttu-id="2668b-111">Quando um usuário instala o pacote, a extensão e o host são instalados.</span><span class="sxs-lookup"><span data-stu-id="2668b-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="2668b-112">Instale sua extensão usando o [armazenamento de Complementos] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]do Microsoft Edge e sua extensão solicitará que os usuários instalem o host.</span><span class="sxs-lookup"><span data-stu-id="2668b-112">Install your extension using the [Microsoft Edge Add-ons store] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="2668b-113">Para criar sua extensão para enviar e receber mensagens com hosts de aplicativo nativos, consulte as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="2668b-114">Etapa 1: adicionar permissões ao manifesto da extensão</span><span class="sxs-lookup"><span data-stu-id="2668b-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="2668b-115">Adicione a `nativeMessaging` permissão aomanifest.js\*\* no\*\* arquivo da extensão.</span><span class="sxs-lookup"><span data-stu-id="2668b-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="2668b-116">O trecho de código a seguir é um exemplo \*\* demanifest.jsem\*\*.</span><span class="sxs-lookup"><span data-stu-id="2668b-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="2668b-117">Etapa 2: criar seu arquivo de manifesto do host de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="2668b-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="2668b-118">Os aplicativos nativos devem fornecer um arquivo de manifesto do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="2668b-119">O arquivo de manifesto contém as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="2668b-120">O caminho para o tempo de execução do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="2668b-121">O método de comunicação com a extensão.</span><span class="sxs-lookup"><span data-stu-id="2668b-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="2668b-122">Uma lista de extensões permitidas com as quais se comunica.</span><span class="sxs-lookup"><span data-stu-id="2668b-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="2668b-123">O navegador lê e valida o manifesto do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="2668b-124">O navegador não instala nem gerencia o arquivo de manifesto do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="2668b-125">O arquivo de manifesto do host deve ser um arquivo JSON válido que contenha as chaves a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2668b-126">Especifica o nome do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-126">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="2668b-127">Os clientes passam essa cadeia de `runtime.connectNative` caracteres para ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="2668b-127">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="2668b-128">Esse valor deve conter apenas caracteres alfanuméricos minúsculos, sublinhados e pontos.</span><span class="sxs-lookup"><span data-stu-id="2668b-128">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="2668b-129">Esse valor não deve começar ou terminar com um ponto, e um ponto não deve ser seguido por outro ponto.</span><span class="sxs-lookup"><span data-stu-id="2668b-129">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2668b-130">Descreve o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-130">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2668b-131">Especifica o caminho para o binário nativo do host de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2668b-131">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="2668b-132">Em dispositivos Windows, você pode usar caminhos relativos para o diretório que contém o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="2668b-132">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="2668b-133">No macOS e no Linux, o caminho deve ser absoluto.</span><span class="sxs-lookup"><span data-stu-id="2668b-133">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="2668b-134">O processo de host começa com o diretório atual definido como o diretório que contém o binário do host.</span><span class="sxs-lookup"><span data-stu-id="2668b-134">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="2668b-135">Por exemplo \(Windows\), se esse parâmetro for definido como , o binário será iniciado usando o `C:\Application\nm_host.exe` diretório atual \( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="2668b-135">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2668b-136">Especifica o tipo da interface usada para se comunicar com o host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-136">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="2668b-137">Esse valor instrui o Microsoft Edge a usar `stdin` e a se comunicar com o `stdout` host.</span><span class="sxs-lookup"><span data-stu-id="2668b-137">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="2668b-138">O único valor aceitável é `stdio` .</span><span class="sxs-lookup"><span data-stu-id="2668b-138">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="2668b-139">Especifica a lista de extensões que têm acesso ao host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-139">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="2668b-140">Para permitir que seu aplicativo identifique e se comunique com uma extensão, em seu arquivo de manifesto de host de mensagens nativo, de definida o seguinte valor.</span><span class="sxs-lookup"><span data-stu-id="2668b-140">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="2668b-141">Realizar sideload da extensão para testar as mensagens nativas com o host.</span><span class="sxs-lookup"><span data-stu-id="2668b-141">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="2668b-142">Para realizar o sideload da extensão durante o desenvolvimento e `microsoft_catalog_extension_id` recuperar, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-142">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="2668b-143">Navegue `edge://extensions` até e, em seguida, a a turn on the Developer mode toggle button.</span><span class="sxs-lookup"><span data-stu-id="2668b-143">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="2668b-144">Escolha **Carregar descompactado**e selecione seu pacote de extensão para sideload.</span><span class="sxs-lookup"><span data-stu-id="2668b-144">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="2668b-145">Escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="2668b-145">Choose **OK**.</span></span>  
1.  <span data-ttu-id="2668b-146">Navegue `edge://extensions` até a página e verifique se sua extensão está listada.</span><span class="sxs-lookup"><span data-stu-id="2668b-146">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="2668b-147">Copie a chave de `microsoft_catalog_extension_id` \(ID\) da listagem de extensão na página.</span><span class="sxs-lookup"><span data-stu-id="2668b-147">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  

<span data-ttu-id="2668b-148">Quando você estiver pronto para distribuir sua extensão aos usuários, publique sua extensão no armazenamento de complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2668b-148">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="2668b-149">A ID de extensão da extensão publicada pode ser diferente da ID usada durante o sideload da extensão.</span><span class="sxs-lookup"><span data-stu-id="2668b-149">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="2668b-150">Se a ID for alterada, `allowed_origins` atualize no arquivo de manifesto do host com a ID da extensão publicada.</span><span class="sxs-lookup"><span data-stu-id="2668b-150">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="2668b-151">Etapa 3: copiar o arquivo de manifesto do host de mensagens nativo para o sistema</span><span class="sxs-lookup"><span data-stu-id="2668b-151">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="2668b-152">A etapa final envolve copiar o arquivo de manifesto do host de mensagens nativo para seu computador e garantir que o arquivo de manifesto está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="2668b-152">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="2668b-153">Para garantir que o arquivo de manifesto seja colocado no local esperado, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-153">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="2668b-154">O local varia de acordo com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="2668b-154">The location varies by platform.</span></span>  

### [<span data-ttu-id="2668b-155">Windows</span><span class="sxs-lookup"><span data-stu-id="2668b-155">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="2668b-156">O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2668b-156">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="2668b-157">O instalador de aplicativo deve criar uma chave do Registro e definir o valor padrão dessa chave para o caminho completo do arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="2668b-157">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="2668b-158">Os comandos a seguir são exemplos de chaves do Registro.</span><span class="sxs-lookup"><span data-stu-id="2668b-158">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="2668b-159">Para adicionar uma chave do Registro ao diretório com a chave de manifesto.</span><span class="sxs-lookup"><span data-stu-id="2668b-159">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="2668b-160">Execute o comando no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="2668b-160">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="2668b-161">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="2668b-161">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="2668b-162">Crie um `.reg` arquivo e execute-o.</span><span class="sxs-lookup"><span data-stu-id="2668b-162">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="2668b-163">Copie o comando a seguir em um `.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="2668b-163">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="2668b-164">Execute o `.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="2668b-164">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="2668b-165">O Microsoft Edge consulta a `HKEY_CURRENT_USER` chave raiz seguida por `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="2668b-165">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="2668b-166">Em ambas as chaves, o Registro de 32 bits é pesquisado primeiro e, em seguida, o Registro de 64 bits é pesquisado para identificar hosts nativos de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2668b-166">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="2668b-167">A chave do Registro especifica o local do manifesto do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="2668b-167">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="2668b-168">Se o Microsoft Edge encontrar a chave do Registro em qualquer um dos locais listados anteriormente, ele não consultará os locais listados neste parágrafo.</span><span class="sxs-lookup"><span data-stu-id="2668b-168">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in this paragraph.</span></span>  <span data-ttu-id="2668b-169">Se você executar o arquivo acima como parte de um script em `.reg` lotes, execute-o usando um prompt de comando do administrador.</span><span class="sxs-lookup"><span data-stu-id="2668b-169">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="2668b-170">macOS</span><span class="sxs-lookup"><span data-stu-id="2668b-170">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="2668b-171">Para armazenar o arquivo de manifesto, conclua uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-171">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="2668b-172">Hosts de mensagens nativos de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="2668b-172">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="2668b-173">Por exemplo, o arquivo de manifesto deve ser armazenado no seguinte local.</span><span class="sxs-lookup"><span data-stu-id="2668b-173">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="2668b-174">Hosts de mensagens nativos específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no subdiretório no `NativeMessagingHosts` diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="2668b-174">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="2668b-175">Por exemplo, o arquivo de manifesto deve ser armazenado no seguinte local.</span><span class="sxs-lookup"><span data-stu-id="2668b-175">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="2668b-176">O  `{Channel_Name}` in deve ser um dos valores a `Microsoft Edge {Channel_Name}` seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-176">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="2668b-177">Canary</span><span class="sxs-lookup"><span data-stu-id="2668b-177">Canary</span></span>  
    *   <span data-ttu-id="2668b-178">Dev</span><span class="sxs-lookup"><span data-stu-id="2668b-178">Dev</span></span>  
    *   <span data-ttu-id="2668b-179">Beta</span><span class="sxs-lookup"><span data-stu-id="2668b-179">Beta</span></span>  

    <span data-ttu-id="2668b-180">Ao usar o canal Estável, `{Channel_Name}` não é necessário.</span><span class="sxs-lookup"><span data-stu-id="2668b-180">When using the Stable channel, `{Channel_Name}` isn't required.</span></span>  

### [<span data-ttu-id="2668b-181">Linux</span><span class="sxs-lookup"><span data-stu-id="2668b-181">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="2668b-182">Para armazenar o arquivo de manifesto, conclua uma das ações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2668b-182">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="2668b-183">Hosts de mensagens nativos de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="2668b-183">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="2668b-184">O arquivo de manifesto deve ser armazenado no seguinte local.</span><span class="sxs-lookup"><span data-stu-id="2668b-184">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="2668b-185">Hosts de mensagens nativos específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no subdiretório no `NativeMessagingHosts` diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="2668b-185">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="2668b-186">O arquivo de manifesto deve ser armazenado no seguinte local.</span><span class="sxs-lookup"><span data-stu-id="2668b-186">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="2668b-187">Forneça permissões de leitura no arquivo de manifesto e execute permissões no tempo de execução do host.</span><span class="sxs-lookup"><span data-stu-id="2668b-187">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="2668b-189">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2668b-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2668b-190">A página original é encontrada [aqui.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="2668b-190">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2668b-192">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2668b-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
