---
description: Documentação de mensagens nativas
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: e6233289794bc1c3ef235af46402c23173c09857
ms.sourcegitcommit: e6a4f73be57439149e3cc56491d7364831d0079e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "11475208"
---
# <a name="native-messaging"></a><span data-ttu-id="1e3dc-104">Sistema de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="1e3dc-104">Native messaging</span></span>  

<span data-ttu-id="1e3dc-105">As extensões se comunicam com um aplicativo Win32 nativo instalado no dispositivo de um usuário usando APIs de passagem de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-105">Extensions communicate with a native Win32 app installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="1e3dc-106">O host de aplicativo nativo envia e recebe mensagens com extensões usando entrada padrão e saída padrão.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-106">The native app host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="1e3dc-107">Extensões usando mensagens nativas são instaladas no Microsoft Edge semelhantes a qualquer outra extensão.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="1e3dc-108">No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-108">However, native apps are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="1e3dc-109">Para adquirir a extensão e o host de aplicativo nativo, você tem dois modelos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-109">To acquire the extension and native app host, you have two distribution models.</span></span>  

*   <span data-ttu-id="1e3dc-110">Empacote sua extensão e o host juntos.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-110">Package your extension and the host together.</span></span>  <span data-ttu-id="1e3dc-111">Quando um usuário instala o pacote, a extensão e o host são instalados.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="1e3dc-112">Instale sua extensão usando o Armazenamento de [Complementos do Microsoft Edge][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]e sua extensão solicita que os usuários instalem o host.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-112">Install your extension using the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="1e3dc-113">Para criar sua extensão para enviar e receber mensagens com hosts de aplicativos nativos, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-113">To create your extension to send and receive messages with native app hosts, complete the following steps.</span></span>  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a><span data-ttu-id="1e3dc-114">Etapa 1 - Adicionar permissões ao manifesto da extensão</span><span class="sxs-lookup"><span data-stu-id="1e3dc-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="1e3dc-115">Adicione a `nativeMessaging` permissão ao arquivomanifest.js\*\* no\*\* arquivo da extensão.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="1e3dc-116">O trecho de código a seguir é um exemplo de **manifest.jsem**.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-116">The following code snippet is an example of **manifest.json**.</span></span>  

```json
{
    "name": "Native Messaging Example",
    "version": "1.0",
    "manifest_version": 2, 
    "description": "Send a message to a native app.",
    "app": { 
        "launch": { 
            "local_path": "main.html" 
        } 
    }, 
    "icons": { 
        "128": "icon-128.png"
    }, 
    "permissions": ["nativeMessaging"] 
}
```  

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a><span data-ttu-id="1e3dc-117">Etapa 2 : Criar o arquivo de manifesto do host de mensagens nativo</span><span class="sxs-lookup"><span data-stu-id="1e3dc-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="1e3dc-118">Os aplicativos nativos devem fornecer um arquivo de manifesto de host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-118">Native apps must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="1e3dc-119">O arquivo de manifesto contém as seguintes informações.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="1e3dc-120">O caminho para o tempo de execução do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="1e3dc-121">O método de comunicação com a extensão.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="1e3dc-122">Uma lista de extensões permitidas às quais se comunica.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="1e3dc-123">O navegador lê e valida o manifesto nativo do host de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="1e3dc-124">O navegador não instala ou gerencia o arquivo de manifesto do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

```json
{
    "name": "com.my_company.my_app",
    "description": "My App",
    "path": "C:\\Program Files\\My App\\chrome_native_messaging_host.exe",
    "type": "stdio",
    "allowed_origins": [
        "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="1e3dc-125">O arquivo de manifesto do host deve ser um arquivo JSON válido que contém as seguintes chaves.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="1e3dc-126">Chave</span><span class="sxs-lookup"><span data-stu-id="1e3dc-126">Key</span></span>**  
   :::column-end:::
   :::column span="3":::
      **<span data-ttu-id="1e3dc-127">Detalhes</span><span class="sxs-lookup"><span data-stu-id="1e3dc-127">Details</span></span>**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="1e3dc-128">Especifica o nome do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-128">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="1e3dc-129">Os clientes passam a cadeia de `runtime.connectNative` caracteres para ou `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="1e3dc-129">Clients pass the string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="1e3dc-130">O valor só deve conter caracteres alfanuméricos minúsculos, sublinhados e pontos.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-130">The value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="1e3dc-131">O valor não deve iniciar ou terminar com um ponto, e um ponto não deve ser seguido por outro ponto.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-131">The value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="1e3dc-132">Descreve o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-132">Describes the app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="1e3dc-133">Especifica o caminho para o binário de host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-133">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="1e3dc-134">Em dispositivos Windows, você pode usar caminhos relativos ao diretório que contém o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-134">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="1e3dc-135">No macOS e no Linux, o caminho deve ser absoluto.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-135">On macOS and Linux, the path must be absolute.</span></span>  
          
      <span data-ttu-id="1e3dc-136">O processo de host começa com o diretório atual definido para o diretório que contém o binário do host.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-136">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="1e3dc-137">Por exemplo \(Windows\), se o parâmetro for definido como , o binário será iniciado usando o `C:\App\nm_host.exe` diretório atual \( `C:\App\` \).</span><span class="sxs-lookup"><span data-stu-id="1e3dc-137">For example \(Windows\), if the parameter is set to `C:\App\nm_host.exe`, the binary is started using the current directory \(`C:\App\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="1e3dc-138">Especifica o tipo da interface usada para se comunicar com o host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-138">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="1e3dc-139">O valor instrui o Microsoft Edge a usar `stdin` e se comunicar com o `stdout` host.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-139">The value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="1e3dc-140">O único valor aceitável é `stdio` .</span><span class="sxs-lookup"><span data-stu-id="1e3dc-140">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="1e3dc-141">Especifica a lista de extensões que têm acesso ao host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-141">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="1e3dc-142">Para ativar seu aplicativo para identificar e se comunicar com uma extensão, em seu arquivo de manifesto de host de mensagens nativo de definir o seguinte valor.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-142">To turn on your app to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="1e3dc-143">Fazer sideload da extensão para testar mensagens nativas com o host.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-143">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="1e3dc-144">Para fazer sideload da extensão durante o desenvolvimento e recuperar `microsoft_catalog_extension_id` , conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-144">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following actions.</span></span>  

1.  <span data-ttu-id="1e3dc-145">Navegue `edge://extensions` até e, em seguida, a opção Botão de alternância do modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-145">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="1e3dc-146">Escolha **Carregar descompactado**e, em seguida, escolha o pacote de extensão para sideload.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-146">Choose **Load unpacked**, and then choose your extension package to sideload.</span></span>  
1.  <span data-ttu-id="1e3dc-147">Escolha **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-147">Choose **OK**.</span></span>  
1.  <span data-ttu-id="1e3dc-148">Navegue `edge://extensions` até a página e verifique se sua extensão está listada.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-148">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="1e3dc-149">Copie a chave `microsoft_catalog_extension_id` de \(ID\) da listagem de extensão na página.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-149">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  
    
<span data-ttu-id="1e3dc-150">Quando estiver pronto para distribuir sua extensão aos usuários, publique sua extensão no armazenamento de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-150">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="1e3dc-151">A ID de extensão da extensão publicada pode ser diferente da ID usada durante o sideload da extensão.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-151">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="1e3dc-152">Se a ID for alterada, atualize no `allowed_origins` arquivo de manifesto do host com a ID da extensão publicada.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-152">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a><span data-ttu-id="1e3dc-153">Etapa 3 : Copiar o arquivo de manifesto do host de mensagens nativo para o sistema</span><span class="sxs-lookup"><span data-stu-id="1e3dc-153">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="1e3dc-154">A etapa final envolve copiar o arquivo de manifesto do host de mensagens nativo para o computador e garantir que o arquivo de manifesto está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-154">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="1e3dc-155">Para garantir que seu arquivo de manifesto seja colocado no local esperado, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-155">To ensure your manifest file is placed in the expected location, complete the following the actions.</span></span>  <span data-ttu-id="1e3dc-156">O local varia de acordo com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-156">The location varies by platform.</span></span>

> [!NOTE]
> <span data-ttu-id="1e3dc-157">Verifique se você fornece permissões de leitura no arquivo de manifesto e execute permissões no tempo de execução do host.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-157">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

### [<a name="windows"></a><span data-ttu-id="1e3dc-158">Windows</span><span class="sxs-lookup"><span data-stu-id="1e3dc-158">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="1e3dc-159">O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-159">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="1e3dc-160">O instalador de aplicativo deve criar uma chave do Registro e definir o valor padrão da chave para o caminho completo do arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-160">The app installer must create a registry key and set the default value of the key to the full path of the manifest file.</span></span>  <span data-ttu-id="1e3dc-161">Os locais a seguir são exemplos de chaves do Registro.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-161">The following locations are examples of registry keys.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

<span data-ttu-id="1e3dc-162">Para adicionar uma chave do Registro ao diretório com a chave de manifesto, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-162">To add a registry key to the directory with the manifest key, complete one of the following actions.</span></span>  

*   <span data-ttu-id="1e3dc-163">Execute o comando no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-163">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="1e3dc-164">Execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-164">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   <span data-ttu-id="1e3dc-165">Crie um `.reg` arquivo e execute-o.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-165">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="1e3dc-166">Copie o seguinte comando em um `.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-166">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="1e3dc-167">Execute o `.reg` arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-167">Run the `.reg` file.</span></span>  
        
<span data-ttu-id="1e3dc-168">O Microsoft Edge consulta a `HKEY_CURRENT_USER` chave raiz seguida por `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="1e3dc-168">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="1e3dc-169">Em ambas as chaves, o Registro de 32 bits é pesquisado primeiro e, em seguida, o Registro de 64 bits é pesquisado para identificar hosts de mensagens nativos.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-169">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="1e3dc-170">A chave do Registro especifica o local do manifesto do host de mensagens nativo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-170">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="1e3dc-171">Se as entradas do Registro do Microsoft Edge não têm o local do manifesto do host, os locais do Registro do Chromium e do Chrome serão usados como opções de fallback.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-171">If the registry entries for Microsoft Edge don't have the location of the host manifest, the Chromium and Chrome registry locations are used as fallback options.</span></span>  <span data-ttu-id="1e3dc-172">Se o Microsoft Edge encontrar a chave do Registro em qualquer um dos locais listados anteriormente, ele não consultará os locais listados no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-172">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in the following code snippet.</span></span>  <span data-ttu-id="1e3dc-173">Se você executar o arquivo criado como parte de um script em lotes, verifique se o executará usando um prompt `.reg` de comando do administrador.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-173">If you run your created `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>

<span data-ttu-id="1e3dc-174">A lista a seguir é a ordem de pesquisa para os locais do Registro.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-174">The following list is the search order for the registry locations.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\

HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\
```  
 
> [!NOTE] 
> <span data-ttu-id="1e3dc-175">Se você tiver extensões nos Complementos do Microsoft Edge e na Webstore do Chrome, você deverá adicionar as IDs de extensão correspondentes a ambos os repositórios no arquivo de manifesto do host porque somente o manifesto de host correspondente ao primeiro local do Registro encontrado é `allowed_origins` lido.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-175">If you have extensions on the Microsoft Edge Add-ons and the Chrome Webstore, you must add the extension IDs corresponding to both the stores in the `allowed_origins` of the host manifest file because only the host manifest corresponding to the first registry location found is read.</span></span>  

### [<a name="macos"></a><span data-ttu-id="1e3dc-176">macOS</span><span class="sxs-lookup"><span data-stu-id="1e3dc-176">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="1e3dc-177">Para armazenar o arquivo de manifesto, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-177">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="1e3dc-178">Hosts de mensagens nativos em todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-178">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="1e3dc-179">Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-179">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   <span data-ttu-id="1e3dc-180">Hosts de mensagens nativas específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-180">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="1e3dc-181">Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-181">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    <span data-ttu-id="1e3dc-182">O  `{Channel_Name}` in deve ser um dos seguintes `Microsoft Edge {Channel_Name}` valores.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-182">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    <span data-ttu-id="1e3dc-183">Ao usar o canal Estável, ` {Channel_Name}` não é necessário.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-183">When using the Stable channel, ` {Channel_Name}` isn't required.</span></span>  
    
### [<a name="linux"></a><span data-ttu-id="1e3dc-184">Linux</span><span class="sxs-lookup"><span data-stu-id="1e3dc-184">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="1e3dc-185">Para armazenar o arquivo de manifesto, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-185">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="1e3dc-186">Hosts de mensagens nativos em todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-186">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="1e3dc-187">O arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-187">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="1e3dc-188">Hosts de mensagens nativas específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-188">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="1e3dc-189">O arquivo de manifesto deve ser armazenado no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e3dc-189">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="1e3dc-191">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e3dc-191">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1e3dc-192">A página original é encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="1e3dc-192">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1e3dc-194">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1e3dc-194">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
