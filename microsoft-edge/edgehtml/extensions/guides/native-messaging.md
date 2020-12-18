---
description: Saiba como você pode usar o recurso de mensagens nativas para que sua extensão se comunique com um aplicativo UWP complementar.
title: Extensões-mensagens nativas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, nativo, mensagens, UWP
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 983ae11822edabc0f27bd6c02f9397104b082ad6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231846"
---
# <span data-ttu-id="40e03-104">Mensagens nativas no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40e03-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="40e03-105">Visão geral da arquitetura de mensagens nativa</span><span class="sxs-lookup"><span data-stu-id="40e03-105">Native messaging architecture overview</span></span>

<span data-ttu-id="40e03-106">Com a atualização do Windows 10 Creator, as extensões do Microsoft Edge podem usar o recurso de mensagens nativas para se comunicar com um aplicativo da plataforma universal do Windows (UWP) complementar.</span><span class="sxs-lookup"><span data-stu-id="40e03-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform (UWP) app.</span></span>  <span data-ttu-id="40e03-107">Em um nível alto, as extensões do Microsoft Edge usam as mesmas APIs para mensagens nativas como extensões Chrome e Firefox.</span><span class="sxs-lookup"><span data-stu-id="40e03-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span> <span data-ttu-id="40e03-108">No entanto, o host de mensagens nativa precisará ser implementado usando a plataforma universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="40e03-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>

> [!NOTE]
> <span data-ttu-id="40e03-109">O método descrito abaixo (conectando a um aplicativo UWP via AppService) é o único mecanismo com suporte para habilitar a comunicação entre extensões do Microsoft Edge e componentes nativos.</span><span class="sxs-lookup"><span data-stu-id="40e03-109">The method outlined below (connecting to a UWP app via AppService) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span> <span data-ttu-id="40e03-110">Consulte a seção [Adicionar um componente da ponte da área de trabalho](#adding-a-desktop-bridge-component) deste guia para obter mais informações sobre como habilitar a comunicação com componentes herdados do Win32.</span><span class="sxs-lookup"><span data-stu-id="40e03-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span> 

 <span data-ttu-id="40e03-111">A arquitetura de mensagens nativas da Microsoft Edge aproveita a [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API existente como a infraestrutura de comunicação entre processos (IPC) subjacente.</span><span class="sxs-lookup"><span data-stu-id="40e03-111">Microsoft Edge's native messaging architecture leverages the existing [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API as the underlying inter-process communication (IPC) infrastructure.</span></span> <span data-ttu-id="40e03-112">Os aplicativos UWP usam a `AppService` API para se comunicar uns com os outros.</span><span class="sxs-lookup"><span data-stu-id="40e03-112">UWP apps use the `AppService` API to communicate with one another.</span></span> <span data-ttu-id="40e03-113">Por isso, as extensões do Microsoft Edge agora podem se comunicar com aplicativos UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-113">Because of this, Microsoft Edge extensions can now communicate with UWP apps.</span></span>

![arquitetura de mensagens nativa](./../media/native-messaging-architecture.png)

### <span data-ttu-id="40e03-115">Quando e quando não usar mensagens nativas</span><span class="sxs-lookup"><span data-stu-id="40e03-115">When and when not to use native messaging</span></span>

<span data-ttu-id="40e03-116">O recurso de mensagens nativas adiciona uma nova camada inteira à sua extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-116">Native messaging adds a whole new layer to your extension.</span></span> <span data-ttu-id="40e03-117">Ao implementar um aplicativo de complemento UWP para sua extensão, as seguintes possibilidades são disponibilizadas para você:</span><span class="sxs-lookup"><span data-stu-id="40e03-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>

* <span data-ttu-id="40e03-118">Sincronize dados (por exemplo, credenciais) com um aplicativo UWP complementar.</span><span class="sxs-lookup"><span data-stu-id="40e03-118">Synchronize data (e.g. credentials) with a companion UWP app.</span></span>
* <span data-ttu-id="40e03-119">Implementar algoritmos de criptografia/descriptografia mais forte não disponíveis em APIs da Web.</span><span class="sxs-lookup"><span data-stu-id="40e03-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>
* <span data-ttu-id="40e03-120">Acesse recursos que não podem ser acessados por meio de APIs da Web, por exemplo, hardware ou dispositivos USB</span><span class="sxs-lookup"><span data-stu-id="40e03-120">Access resources that are not accessible through web APIs, e.g. hardware or USB devices</span></span>

<span data-ttu-id="40e03-121">Há alguns casos em que as mensagens nativas não podem ser usadas devido a restrições de segurança ou política:</span><span class="sxs-lookup"><span data-stu-id="40e03-121">There are a few instances where native messaging can't be used due to security or policy restrictions:</span></span>

* <span data-ttu-id="40e03-122">Modificando as configurações do usuário no Microsoft Edge ou no Windows, por exemplo, alterar o navegador padrão ou o provedor de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40e03-122">Modifying user settings in either Microsoft Edge or Windows, e.g. changing the default browser or search provider.</span></span>
* <span data-ttu-id="40e03-123">Ações que violam políticas da Microsoft Store para aplicativos e extensões.</span><span class="sxs-lookup"><span data-stu-id="40e03-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>
* <span data-ttu-id="40e03-124">Transferindo dados para um ponto de extremidade remoto por meio do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="40e03-124">Transferring data to remote endpoint via native message host.</span></span>
* <span data-ttu-id="40e03-125">Permitir que outros aplicativos baixem conteúdo que altera o comportamento da extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-125">Allowing other apps to download content that changes extension behavior.</span></span>

## <span data-ttu-id="40e03-126">Demonstrações</span><span class="sxs-lookup"><span data-stu-id="40e03-126">Demos</span></span>

<span data-ttu-id="40e03-127">Para ter uma noção de qual é a aparência de uma extensão de mensagens nativas do Microsoft Edge que tenha um aplicativo UWP complementar e uma ponte da área de trabalho, confira os exemplos [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) e [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) no github.</span><span class="sxs-lookup"><span data-stu-id="40e03-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>

### <span data-ttu-id="40e03-128">Como funciona</span><span class="sxs-lookup"><span data-stu-id="40e03-128">How it works</span></span>

<span data-ttu-id="40e03-129">O componente de extensão do Microsoft Edge da amostra usa seu script de conteúdo para detectar quando um usuário está digitando informações que devem ser criptografadas.</span><span class="sxs-lookup"><span data-stu-id="40e03-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span> <span data-ttu-id="40e03-130">A extensão comunica isso ao componente da ponte da área de trabalho via mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="40e03-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span> <span data-ttu-id="40e03-131">Quando o usuário está pronto para enviar os dados, a extensão retorna um valor criptografado de volta para o site.</span><span class="sxs-lookup"><span data-stu-id="40e03-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>

> [!NOTE]
> <span data-ttu-id="40e03-132">Este exemplo só funcionará em uma página da Web que usa eventos personalizados para se comunicar com o script de conteúdo da extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-132">This sample will only work on a webpage that uses custom events to communicate with the extension's content script.</span></span> <span data-ttu-id="40e03-133">A pasta de exemplo inclui um [arquivo. html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) para testar a extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>

<span data-ttu-id="40e03-134">Neste exemplo, o aplicativo UWP é usado para passar respostas da ponte da área de trabalho para o Microsoft Edge, que, em seguida, são enviados à extensão do Microsoft Edge por meio de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="40e03-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span> <span data-ttu-id="40e03-135">Embora este exemplo tenha o host de mensagens nativa executado no aplicativo principal, ele também pode ser executado como uma tarefa em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="40e03-135">While this example has the native messaging host run in the main app, it's also able to run as a background task.</span></span> <span data-ttu-id="40e03-136">Alternar entre os dois exige a edição do script de plano de fundo da extensão, alterando a cadeia de caracteres `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` para `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="40e03-136">Switching between the two requires editing the extension's background script, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>

## <span data-ttu-id="40e03-137">Implementação do Chrome versus Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="40e03-137">Chrome vs Microsoft Edge implementation</span></span>

<span data-ttu-id="40e03-138">Embora o Chrome seja a rota de usar APIs de transmissão de mensagens para suas extensões para se comunicar com os aplicativos, o Microsoft Edge utiliza a [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API que agora permite que as extensões do Microsoft Edge e os aplicativos UWP se comuniquem.</span><span class="sxs-lookup"><span data-stu-id="40e03-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>

<span data-ttu-id="40e03-139">Esta seção detalha as diferenças entre como o Chrome e o Microsoft Edge manipulam a implementação de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="40e03-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>

### <span data-ttu-id="40e03-140">Manifesto de host e registro</span><span class="sxs-lookup"><span data-stu-id="40e03-140">Registration and host manifest</span></span>
<span data-ttu-id="40e03-141">Para que seu aplicativo seja reconhecido pela extensão como um host de mensagens nativo, ele precisará ser registrado.</span><span class="sxs-lookup"><span data-stu-id="40e03-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>

<span data-ttu-id="40e03-142">Para o registro do host de [mensagens nativas do Chrome](https://developer.chrome.com/extensions/nativeMessaging) , seu aplicativo precisa instalar um arquivo de manifesto em qualquer lugar no sistema de arquivos do Windows que define a configuração do host de mensagens nativa.</span><span class="sxs-lookup"><span data-stu-id="40e03-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>

<span data-ttu-id="40e03-143">O JSON a seguir é um exemplo de como o arquivo de configuração pode ser configurado:</span><span class="sxs-lookup"><span data-stu-id="40e03-143">The following JSON is an example of how the config file can be set up:</span></span>

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="40e03-144">Para instalar esse arquivo, o aplicativo precisa:</span><span class="sxs-lookup"><span data-stu-id="40e03-144">To install this file, the app would need to:</span></span>

1.  <span data-ttu-id="40e03-145">Registre o arquivo de manifesto em um local predefinido no registro que define a configuração do host:</span><span class="sxs-lookup"><span data-stu-id="40e03-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>
    -   ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application
        ```  
        
        <span data-ttu-id="40e03-146">ou</span><span class="sxs-lookup"><span data-stu-id="40e03-146">or</span></span>
        
    -   ```text
        HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application
        ```  
        
2.  <span data-ttu-id="40e03-147">Defina o valor padrão dessa chave para o caminho completo para o arquivo de manifesto, por exemplo,</span><span class="sxs-lookup"><span data-stu-id="40e03-147">Set the default value of that key to the full path to the manifest file, e.g.</span></span> 
    
    ```text
    [HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
<span data-ttu-id="40e03-148">Para o Microsoft Edge, a fim de registrar um [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (host de mensagens nativa), você precisará incluir o aplicativo de complemento UWP no mesmo pacote que a extensão e especificar a [extensão AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) no arquivo do seu projeto `Package.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="40e03-148">For Microsoft Edge, in order to register an [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx)(native messaging host) you'll need to include the UWP companion app in the same package as your extension and specify the [AppService extension](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in your project's `Package.appxmanifest` file.</span></span> <span data-ttu-id="40e03-149">Os `EntryPoint` `Name` atributos e podem ser configurados por você:</span><span class="sxs-lookup"><span data-stu-id="40e03-149">The `EntryPoint` and `Name` attributes can be configured by you:</span></span>

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...    
    </Application>
</Applications>
```


<span data-ttu-id="40e03-150">Você também precisará definir quais extensões têm permissão para se conectar ao serviço.</span><span class="sxs-lookup"><span data-stu-id="40e03-150">You'll also need to set which extension(s) are allowed to connect to the service.</span></span> <span data-ttu-id="40e03-151">Como o Microsoft Edge não tem uma `"allowed_origins"` propriedade de manifesto equivalente em seu AppxManifest, ela precisará ser determinada e imposta em tempo de execução pelo seu aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-151">Because Microsoft Edge doesn't have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span> <span data-ttu-id="40e03-152">Como o Microsoft Edge irá estabelecer a conexão em nome da extensão, o aplicativo pode procurar o nome da família do pacote do chamador para determinar se ele está sendo conectado pelo Microsoft Edge para controlar ou autenticar o chamador.</span><span class="sxs-lookup"><span data-stu-id="40e03-152">Since Microsoft Edge will be establishing the connection on behalf of the extension, the app can look up the caller's Package Family Name to determine if they're being connected by Microsoft Edge to control or authenticate the caller.</span></span> <span data-ttu-id="40e03-153">Ex.</span><span class="sxs-lookup"><span data-stu-id="40e03-153">E.g.</span></span> 

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```  

### <span data-ttu-id="40e03-154">Envio de mensagens</span><span class="sxs-lookup"><span data-stu-id="40e03-154">Message sending</span></span>

<span data-ttu-id="40e03-155">Para que um aplicativo e uma extensão se comuniquem uns com os outros, é preciso que as mensagens sejam enviadas para e a partir deles.</span><span class="sxs-lookup"><span data-stu-id="40e03-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>

<span data-ttu-id="40e03-156">As extensões Chrome iniciam uma mensagem usando a [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API para entregar uma mensagem ao host nativo usando um canal não persistente.</span><span class="sxs-lookup"><span data-stu-id="40e03-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span> 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="40e03-157">O primeiro parâmetro é o nome do host nativo, que parece ser exibido pelo Chrome no registro do manifesto.</span><span class="sxs-lookup"><span data-stu-id="40e03-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span> <span data-ttu-id="40e03-158">O manifesto especifica o. exe que o Chrome abrirá em uma área restrita e a mensagem será enviada usando e/s padrão.</span><span class="sxs-lookup"><span data-stu-id="40e03-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span> <span data-ttu-id="40e03-159">As extensões também podem estabelecer um canal persistente usando a `runtime.connectNative` API, que usa o nome do host nativo como o único parâmetro.</span><span class="sxs-lookup"><span data-stu-id="40e03-159">Extensions can also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span> 

<span data-ttu-id="40e03-160">O Microsoft Edge usa a mesma construção da API de mensagens nativas do Chrome para permitir que as extensões do Microsoft Edge especifiquem a qual serviço de aplicativo se conectar.</span><span class="sxs-lookup"><span data-stu-id="40e03-160">Microsoft Edge uses the same construct as Chrome's native messaging API to allow Microsoft Edge extensions to specify which app service to connect to.</span></span> <span data-ttu-id="40e03-161">O primeiro parâmetro em `runtime.sendNativeMessage` especifica o nome do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40e03-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span> <span data-ttu-id="40e03-162">Na seção [Registration and host manifest](#registration-and-host-manifest) , isso é `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="40e03-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span> <span data-ttu-id="40e03-163">A plataforma de extensão do Microsoft Edge restringe o host de mensagens nativa a ser um aplicativo UWP que é empacotado no mesmo AppX que a extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span> <span data-ttu-id="40e03-164">Isso atenua quaisquer riscos de segurança associados a ataques maliciosos que tentam conectar o Microsoft Edge com outro nome de família de pacote violando as entradas de manifesto.</span><span class="sxs-lookup"><span data-stu-id="40e03-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span> 

<span data-ttu-id="40e03-165">Isso significa que o Microsoft Edge usará o mesmo nome da família de pacotes como a extensão, além do `AppService` nome especificado na API, para identificar exclusivamente o provedor do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40e03-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="40e03-166">Isso não será facilmente convertido pelo kit de [ferramentas de extensão do Microsoft Edge](./porting-chrome-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="40e03-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span> <span data-ttu-id="40e03-167">Qualquer extensão que especifica a `"nativeMessaging"` permissão será sinalizada como exigindo conversão manual para esse componente.</span><span class="sxs-lookup"><span data-stu-id="40e03-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>

### <span data-ttu-id="40e03-168">Protocolo de comunicação</span><span class="sxs-lookup"><span data-stu-id="40e03-168">Communication protocol</span></span>

<span data-ttu-id="40e03-169">O protocolo de comunicação para mensagens nativas determina como as mensagens são formatadas antes do envio.</span><span class="sxs-lookup"><span data-stu-id="40e03-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>

<span data-ttu-id="40e03-170">O Chrome inicia cada host de mensagens nativa em um processo separado e se comunica com ele usando a entrada padrão e a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="40e03-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span> <span data-ttu-id="40e03-171">O mesmo formato é usado para enviar mensagens em ambas as direções: cada mensagem é serializada usando JSON, UTF-8 codificado e é precedido com o comprimento da mensagem de 32 bits em uma ordem de bytes nativa.</span><span class="sxs-lookup"><span data-stu-id="40e03-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>

<span data-ttu-id="40e03-172">Para o Microsoft Edge, a tarefa em segundo plano/aplicativo principal que implementa o serviço de aplicativo será iniciada pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="40e03-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span> <span data-ttu-id="40e03-173">Na inicialização, o método da tarefa em segundo plano `Run` será invocado:</span><span class="sxs-lookup"><span data-stu-id="40e03-173">On startup, the background task's `Run` method will be invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service isn't terminated.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="40e03-174">Quando a extensão envia uma mensagem para seu aplicativo UWP, o [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) evento será gerado.</span><span class="sxs-lookup"><span data-stu-id="40e03-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) event will be raised.</span></span> <span data-ttu-id="40e03-175">Essa mensagem formatada em JSON será stringifiedda no primeiro par de valores de um [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto.</span><span class="sxs-lookup"><span data-stu-id="40e03-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object.</span></span> <span data-ttu-id="40e03-176">:</span><span class="sxs-lookup"><span data-stu-id="40e03-176">:</span></span>

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="40e03-177">Quando seu aplicativo UWP envia uma resposta de volta para a extensão, a a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) será adicionada ao `ValueSet` objeto.</span><span class="sxs-lookup"><span data-stu-id="40e03-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) will be added to the `ValueSet` object.</span></span> <span data-ttu-id="40e03-178">A `Key` propriedade será ignorada pelo Microsoft Edge, mas a `Value` Propriedade conterá uma cadeia de caracteres JSON válida.</span><span class="sxs-lookup"><span data-stu-id="40e03-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>

### <span data-ttu-id="40e03-179">Retorno</span><span class="sxs-lookup"><span data-stu-id="40e03-179">Callback</span></span>

<span data-ttu-id="40e03-180">Para retornos de chamada, [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) o Chrome usa que permite uma função de retorno de chamada para manipular qualquer resposta assíncrona de enviar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="40e03-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>

<span data-ttu-id="40e03-181">O Microsoft Edge usa o [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) método do objeto [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) para permitir que o aplicativo envie um [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto de volta para a extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-181">Microsoft Edge uses the [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) object's [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) method to let the app send a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object back to the extension.</span></span>


### <span data-ttu-id="40e03-182">Limite de tamanho da mensagem</span><span class="sxs-lookup"><span data-stu-id="40e03-182">Message size limit</span></span>
<span data-ttu-id="40e03-183">As mensagens enviadas entre uma extensão e um aplicativo têm limitações de tamanho de mensagens diferentes no lugar para o Chrome e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40e03-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>

<span data-ttu-id="40e03-184">O Chrome tem as seguintes limitações de tamanho das mensagens:</span><span class="sxs-lookup"><span data-stu-id="40e03-184">Chrome has the following message size limitations:</span></span>
-   <span data-ttu-id="40e03-185">Limite de mensagem única do host de mensagens nativas: 1 MB</span><span class="sxs-lookup"><span data-stu-id="40e03-185">Single message limit from native messaging host: 1 MB</span></span>
-   <span data-ttu-id="40e03-186">Limite de mensagem única enviado para o host de mensagens nativas: 4 GB</span><span class="sxs-lookup"><span data-stu-id="40e03-186">Single message limit sent to native messaging host: 4 GB</span></span>
    
<span data-ttu-id="40e03-187">No Microsoft Edge, embora `AppService` não tenha limite quanto ao tamanho da mensagem (depende da memória), o Microsoft Edge protege-se contra aplicativos nativos inadequados por meio da imposição dos seguintes limites de tamanho de mensagem:</span><span class="sxs-lookup"><span data-stu-id="40e03-187">For Microsoft Edge, while `AppService` has no limit on message size (dependent on memory), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>
-   <span data-ttu-id="40e03-188">Limite de mensagem única do aplicativo UWP para extensão: 1 MB</span><span class="sxs-lookup"><span data-stu-id="40e03-188">Single message limit from UWP app to extension: 1 MB</span></span>
-   <span data-ttu-id="40e03-189">Limite de mensagem única da extensão para o aplicativo UWP: 100 MB</span><span class="sxs-lookup"><span data-stu-id="40e03-189">Single message limit from extension to UWP app: 100 MB</span></span>
    
### <span data-ttu-id="40e03-190">Conexões de mensagens nativas</span><span class="sxs-lookup"><span data-stu-id="40e03-190">Native messaging connections</span></span>

<span data-ttu-id="40e03-191">Há dois tipos de conexões para mensagens nativas; persistente e não persistente.</span><span class="sxs-lookup"><span data-stu-id="40e03-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>
<span data-ttu-id="40e03-192">Uma conexão **persistente** é uma conexão que é mantida em execução até que a porta seja destruída.</span><span class="sxs-lookup"><span data-stu-id="40e03-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span> <span data-ttu-id="40e03-193">Uma conexão **não persistente** é uma conexão que é aberta por uma mensagem de cada vez e é fechada após a entrega.</span><span class="sxs-lookup"><span data-stu-id="40e03-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>

#### <span data-ttu-id="40e03-194">Persistente</span><span class="sxs-lookup"><span data-stu-id="40e03-194">Persistent</span></span>

<span data-ttu-id="40e03-195">Para o Chrome, é feita uma conexão persistente criando uma porta de mensagens usando [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="40e03-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="40e03-196">Depois que a porta for feita, o Chrome iniciará um processo de host de mensagens nativo que continuará em execução até a porta que ele destruiu.</span><span class="sxs-lookup"><span data-stu-id="40e03-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>

<span data-ttu-id="40e03-197">Para o Microsoft Edge, quando uma porta de mensagens for criada usando `runtime.connectNative` , o Microsoft Edge iniciará o [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) e o manterá em execução até que a porta seja destruída.</span><span class="sxs-lookup"><span data-stu-id="40e03-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) and keeps it running until the port is destroyed.</span></span> <span data-ttu-id="40e03-198">O snippet a seguir mostra como uma conexão persistente é estabelecida de dentro de um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span> 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <span data-ttu-id="40e03-199">Não persistente</span><span class="sxs-lookup"><span data-stu-id="40e03-199">Non-persistent</span></span>

<span data-ttu-id="40e03-200">Quando uma mensagem é enviada usando o [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) Chrome, sem a criação de uma porta de mensagens, o Chrome inicia um novo processo de host de mensagens nativo para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="40e03-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span> <span data-ttu-id="40e03-201">A primeira mensagem gerada pelo processo do host é manipulada como uma resposta à solicitação original e todas as outras mensagens depois de serem ignoradas.</span><span class="sxs-lookup"><span data-stu-id="40e03-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>

<span data-ttu-id="40e03-202">O Microsoft Edge encerrará a conexão após o recebimento de todas as mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="40e03-202">Microsoft Edge will terminate the connection after every messages' response has been received.</span></span> <span data-ttu-id="40e03-203">O trecho a seguir mostra uma conexão não persistente que é estabelecida com `AppServiceConnection` isso será encerrada dentro do aplicativo UWP após uma solicitação ser recebida e armazenada como um [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .</span><span class="sxs-lookup"><span data-stu-id="40e03-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse).</span></span>

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```  

### <span data-ttu-id="40e03-204">Permissão</span><span class="sxs-lookup"><span data-stu-id="40e03-204">Permission</span></span>

<span data-ttu-id="40e03-205">Para habilitar o uso de mensagens nativas com sua extensão, para Chrome e Microsoft Edge, você precisará declarar a `"nativeMessaging"` permissão em seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="40e03-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you'll need to declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>

## <span data-ttu-id="40e03-206">Serviços de aplicativo</span><span class="sxs-lookup"><span data-stu-id="40e03-206">App services</span></span>
<span data-ttu-id="40e03-207">Esta seção detalha o impacto dos serviços do aplicativo no desempenho e na memória de mensagens nativas do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40e03-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>

### <span data-ttu-id="40e03-208">Desempenho</span><span class="sxs-lookup"><span data-stu-id="40e03-208">Performance</span></span>

<span data-ttu-id="40e03-209">Os serviços de aplicativo são "patrocinados" pelo aplicativo em primeiro plano que as chama para fins de mensagens nativas é o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40e03-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span> <span data-ttu-id="40e03-210">Isso significa que os serviços de aplicativo podem ser executados enquanto o Microsoft Edge estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="40e03-210">This means that app services can run as long as Microsoft Edge is running.</span></span>

<span data-ttu-id="40e03-211">Em relação à latência, os serviços de aplicativo usam pipes nomeados que, após a conexão inicial, permitem que dois aplicativos se comuniquem diretamente.</span><span class="sxs-lookup"><span data-stu-id="40e03-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span> <span data-ttu-id="40e03-212">Esse método de comunicação produz baixa latência.</span><span class="sxs-lookup"><span data-stu-id="40e03-212">This method of communication produces low latency.</span></span> <span data-ttu-id="40e03-213">Dispositivos com CPUs lentas terão uma latência inicial após iniciar o processo que hospeda o serviço de aplicativo (~ 80ms para iniciar a tarefa em segundo plano em alguns dispositivos).</span><span class="sxs-lookup"><span data-stu-id="40e03-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service (~80ms to startup the background task on some devices).</span></span> <span data-ttu-id="40e03-214">Após a inicialização, o desempenho em dispositivos lentos de CPU deve ser bom.</span><span class="sxs-lookup"><span data-stu-id="40e03-214">After start-up, performance on slow CPU devices should be good.</span></span> 

### <span data-ttu-id="40e03-215">Memória</span><span class="sxs-lookup"><span data-stu-id="40e03-215">Memory</span></span>
<span data-ttu-id="40e03-216">A memória atribuída a um serviço de aplicativo é retirada da cota atribuída ao Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40e03-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span> <span data-ttu-id="40e03-217">Isso significa que, se o Microsoft Edge iniciar muitos serviços de aplicativo, há uma possibilidade de que eles possam ficar sem memória.</span><span class="sxs-lookup"><span data-stu-id="40e03-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span> <span data-ttu-id="40e03-218">Os limites de memória de tarefa em segundo plano usual são aplicados em serviços de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40e03-218">The usual background task memory caps are enforced on app services.</span></span> <span data-ttu-id="40e03-219">Por exemplo, em um dispositivo de 512MB, uma tarefa em segundo plano do serviço de aplicativo não pode ter mais de 16MB.</span><span class="sxs-lookup"><span data-stu-id="40e03-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span> <span data-ttu-id="40e03-220">Esse número aumenta à medida que os dispositivos aumentam.</span><span class="sxs-lookup"><span data-stu-id="40e03-220">This number goes up as the devices scale up.</span></span>

## <span data-ttu-id="40e03-221">Criando uma extensão com mensagens nativas</span><span class="sxs-lookup"><span data-stu-id="40e03-221">Creating an extension with native messaging</span></span>

<span data-ttu-id="40e03-222">Para testar mensagens nativas, sua extensão precisa de um nome de família de pacote.</span><span class="sxs-lookup"><span data-stu-id="40e03-222">In order to test native messaging, your extension needs a Package Family Name.</span></span> <span data-ttu-id="40e03-223">O Microsoft Edge usa isso para determinar a identidade do host de mensagens nativa, o que significa que a extensão deve ser empacotada.</span><span class="sxs-lookup"><span data-stu-id="40e03-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span> 

<span data-ttu-id="40e03-224">Para criar sua extensão com mensagens nativas no Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="40e03-224">To create your extension with native messaging in Visual Studio:</span></span>

1.  <span data-ttu-id="40e03-225">Crie um projeto UWP no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="40e03-225">Create a UWP project in Visual Studio.</span></span>
2.  <span data-ttu-id="40e03-226">[Adicione `AppService` ao seu aplicativo UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="40e03-226">[Add `AppService` to your UWP app](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>
    -   <span data-ttu-id="40e03-227">Opcionalmente, você pode [Configurar `AppService` para ser hospedado no aplicativo principal](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) , em vez de como uma tarefa em segundo plano neste ponto.</span><span class="sxs-lookup"><span data-stu-id="40e03-227">You can optionally [configure `AppService` to be hosted in the main app](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>
3.  <span data-ttu-id="40e03-228">Criar e testar seu projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-228">Build and test your UWP project.</span></span>
    -   <span data-ttu-id="40e03-229">Opcionalmente, você pode adicionar um [componente da ponte da área de trabalho](#adding-a-desktop-bridge-component).</span><span class="sxs-lookup"><span data-stu-id="40e03-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>
4.  <span data-ttu-id="40e03-230">Crie uma extensão do Microsoft Edge que use o sistema de mensagens nativa para se comunicar com o aplicativo UWP associado.</span><span class="sxs-lookup"><span data-stu-id="40e03-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span> <span data-ttu-id="40e03-231">Os arquivos de extensão podem ser adicionados a uma pasta nomeada `Extension` no projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span> <span data-ttu-id="40e03-232">Todos os arquivos abaixo desta pasta, incluindo subpastas, precisam ter suas propriedades configuradas de forma que `Build Action=Content` e `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="40e03-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span> <span data-ttu-id="40e03-233">Verifique `manifest.json` também se está configurado com essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="40e03-233">Make sure `manifest.json` is also configured with these properties.</span></span>
5.  <span data-ttu-id="40e03-234">Modifique o `package.manifest.xml` arquivo no projeto para incluir metadados de extensão e convertê-los em um aplicativo sem periféricos adicionando `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="40e03-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>
    
    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>

       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```
    
6.  <span data-ttu-id="40e03-235">Use o `AppService` nome configurado para a UWP nas APIs de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="40e03-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>
7.  <span data-ttu-id="40e03-236">Criar e [implantar](#deploying) o projeto UWP (com o componente opcional da ponte da área de trabalho).</span><span class="sxs-lookup"><span data-stu-id="40e03-236">Build and [deploy](#deploying) the UWP project (with the optional Desktop Bridge component).</span></span>
8.  <span data-ttu-id="40e03-237">[Empacotar](#packaging) sua extensão de mensagens nativa quando estiver pronto para envio à loja</span><span class="sxs-lookup"><span data-stu-id="40e03-237">[Package](#packaging) your native messaging extension once it's ready for Store submission</span></span>
    
> [!NOTE]
> <span data-ttu-id="40e03-238">Consulte a seção [demos](#demos) para obter um exemplo de uma extensão de mensagens nativa completa.</span><span class="sxs-lookup"><span data-stu-id="40e03-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>

## <span data-ttu-id="40e03-239">Adicionar um componente da ponte da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="40e03-239">Adding a Desktop Bridge component</span></span> 
<span data-ttu-id="40e03-240">Se você quiser adicionar um componente da ponte da área de trabalho ao seu pacote, será necessário criar e construir seu projeto Win32 no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="40e03-240">If you want to add a Desktop Bridge component to your package, you'll need to create and build your Win32 project in Visual Studio.</span></span> <span data-ttu-id="40e03-241">Para obter informações sobre como converter seu aplicativo Win32 em UWP, consulte [portando aplicativos para o Windows 10 via desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="40e03-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span> <span data-ttu-id="40e03-242">Depois de criar o Visual Studio, você pode adicionar o executável Win32 ao pacote seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="40e03-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>

1.  <span data-ttu-id="40e03-243">Adicione o projeto Win32 à mesma solução que o projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-243">Add the Win32 project to the same solution as the UWP project.</span></span> 
2.  <span data-ttu-id="40e03-244">Defina o projeto Win32 como um projeto dependente para o projeto UWP:</span><span class="sxs-lookup"><span data-stu-id="40e03-244">Set the Win32 project as a dependent project for the UWP project:</span></span>
    
    ![configurar dependências do projeto](./../media/project-dependencies.PNG)
    
3.  <span data-ttu-id="40e03-246">Crie uma `Win32` pasta dentro do projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="40e03-246">Create a `Win32` folder within the UWP project.</span></span> <span data-ttu-id="40e03-247">Copie os binários necessários para o `Win32` projeto para essa pasta.</span><span class="sxs-lookup"><span data-stu-id="40e03-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span> <span data-ttu-id="40e03-248">Configure as propriedades de todos os binários, de forma que `Build Action=Content` e `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="40e03-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>
    
    ![pasta com arquivos de aplicativo Win32 e UWP](./../media/desktop-bridge.png)
    
4.  <span data-ttu-id="40e03-250">Modifique o arquivo de projeto UWP para copiar todos os binários necessários do `Win32` projeto para essa pasta usando o comando de evento createbuild.</span><span class="sxs-lookup"><span data-stu-id="40e03-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span> <span data-ttu-id="40e03-251">Isso garante que os binários atualizados sejam copiados para a pasta toda vez que a solução for recriada.</span><span class="sxs-lookup"><span data-stu-id="40e03-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```
    
5.  <span data-ttu-id="40e03-252">Modifique `package.manifest.xml` adicionando o `<desktop:Extension>` elemento ao `<Extensions>` elemento:</span><span class="sxs-lookup"><span data-stu-id="40e03-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```
    
## <span data-ttu-id="40e03-253">Implantando</span><span class="sxs-lookup"><span data-stu-id="40e03-253">Deploying</span></span>
<span data-ttu-id="40e03-254">Depois de configurar seu projeto UWP (e opcionalmente o projeto Win32) conforme descrito acima, você está pronto para implantar a solução usando o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="40e03-254">Once you have configured your UWP project (and optionally Win32 project) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>

![construir projeto de inprocess](../media/native-message-uwp-debug.PNG)

<span data-ttu-id="40e03-256">Depois que a solução é implantada corretamente, você deve ver sua extensão no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40e03-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>

![extensão exibida no Microsoft Edge](../media/secureextension.png)

## <span data-ttu-id="40e03-258">Embalagem</span><span class="sxs-lookup"><span data-stu-id="40e03-258">Packaging</span></span>

> [!NOTE]
> <span data-ttu-id="40e03-259">No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="40e03-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="40e03-260">Entre [em contato conosco](https://aka.ms/extension-request) com suas solicitações para fazer parte da Microsoft Store, e consideraremos você para uma atualização futura.</span><span class="sxs-lookup"><span data-stu-id="40e03-260">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>

<span data-ttu-id="40e03-261">Você pode gerar um pacote da loja para envio para o centro de desenvolvimento do Windows usando a funcionalidade interna do Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="40e03-261">You can generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>

![Criando o pacote da loja](../media/create-store-package.PNG)

## <span data-ttu-id="40e03-263">Depuração</span><span class="sxs-lookup"><span data-stu-id="40e03-263">Debugging</span></span>
<span data-ttu-id="40e03-264">As instruções para depuração variam de acordo com o componente que você deseja testar:</span><span class="sxs-lookup"><span data-stu-id="40e03-264">The instructions for debugging vary depending on which component you want to test out:</span></span>

### <span data-ttu-id="40e03-265">Depurando a extensão</span><span class="sxs-lookup"><span data-stu-id="40e03-265">Debugging the extension</span></span>
<span data-ttu-id="40e03-266">Depois que a solução for implantada, a extensão será instalada no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="40e03-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span> <span data-ttu-id="40e03-267">Confira o guia de [depuração](./debugging-extensions.md) para obter informações sobre como depurar uma extensão.</span><span class="sxs-lookup"><span data-stu-id="40e03-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>


### <span data-ttu-id="40e03-268">Depurando o aplicativo UWP</span><span class="sxs-lookup"><span data-stu-id="40e03-268">Debugging the UWP app</span></span>
<span data-ttu-id="40e03-269">O aplicativo UWP será iniciado quando a extensão tentar se conectar a ele usando [APIs de mensagens nativas](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span><span class="sxs-lookup"><span data-stu-id="40e03-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="40e03-270">Você precisará depurar o aplicativo UWP somente após o início do processo.</span><span class="sxs-lookup"><span data-stu-id="40e03-270">You'll need to debug the UWP app only once the process starts.</span></span> <span data-ttu-id="40e03-271">Isso pode ser configurado por meio da página de propriedades do projeto:</span><span class="sxs-lookup"><span data-stu-id="40e03-271">This can be configured via the project's Property page:</span></span>

1.  <span data-ttu-id="40e03-272">No Visual Studio, clique com o botão direito do mouse no seu projeto de aplicativo UWP</span><span class="sxs-lookup"><span data-stu-id="40e03-272">In Visual Studio, right click your UWP app project</span></span>
2.  <span data-ttu-id="40e03-273">Selecionar Propriedades</span><span class="sxs-lookup"><span data-stu-id="40e03-273">Select Properties</span></span>
3.  <span data-ttu-id="40e03-274">Selecionar "não iniciar, mas depurar meu código quando começar"</span><span class="sxs-lookup"><span data-stu-id="40e03-274">Check "Do not launch, but debug my code when it starts"</span></span>
    
    ![selecionando a caixa não iniciar](../media/native-message-do-not-launch.png)
    
<span data-ttu-id="40e03-276">No Visual Studio, agora você pode definir pontos de interrupção no código onde deseja depurar e, em seguida, iniciar o depurador pressionando F5.</span><span class="sxs-lookup"><span data-stu-id="40e03-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span> <span data-ttu-id="40e03-277">Depois que você interagir com a extensão para se conectar ao aplicativo UWP, o Visual Studio será automaticamente anexado ao processo.</span><span class="sxs-lookup"><span data-stu-id="40e03-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>

### <span data-ttu-id="40e03-278">Depurando a ponte da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="40e03-278">Debugging the Desktop Bridge</span></span>
<span data-ttu-id="40e03-279">Embora existam vários [métodos para depurar uma ponte da área de trabalho](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (aplicativo Win32 convertido), a única aplicável a esses cenários é a opção PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="40e03-279">Even though there are various [methods for debugging a Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (converted Win32 app), the only one applicable for this scenarios is the PLMDebug option.</span></span> <span data-ttu-id="40e03-280">Você também pode adicionar o código de depuração à função Startup para executar uma espera por um tempo específico, permitindo que você anexe o Visual Studio ao processo.</span><span class="sxs-lookup"><span data-stu-id="40e03-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>
