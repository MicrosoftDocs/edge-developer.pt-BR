---
description: Saiba mais sobre como você é capaz de usar mensagens nativas para que sua extensão se comunique com um aplicativo UWP parceiro.
title: Mensagens nativas | Extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor, nativo, mensagens, uwp
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9a306055b8f86b92aa5c3e7cd6de44f2386307d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399355"
---
# <a name="native-messaging-in-microsoft-edge"></a><span data-ttu-id="5251f-104">Mensagens nativas no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5251f-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a><span data-ttu-id="5251f-105">Visão geral da arquitetura de mensagens nativa</span><span class="sxs-lookup"><span data-stu-id="5251f-105">Native messaging architecture overview</span></span>  

<span data-ttu-id="5251f-106">Com a Atualização de Criadores do Windows 10, as extensões do Microsoft Edge são capazes de usar mensagens nativas para se comunicar com um aplicativo da Plataforma Universal do Windows \(UWP\).</span><span class="sxs-lookup"><span data-stu-id="5251f-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform \(UWP\) app.</span></span>  <span data-ttu-id="5251f-107">Em alto nível, as extensões do Microsoft Edge usam as mesmas APIs para mensagens nativas que as extensões Chrome e Firefox.</span><span class="sxs-lookup"><span data-stu-id="5251f-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span>  <span data-ttu-id="5251f-108">No entanto, o host de mensagens nativo precisará ser implementado usando a Plataforma Universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="5251f-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>  

> [!NOTE]
> <span data-ttu-id="5251f-109">O método descrito abaixo \(conectando-se a um aplicativo UWP via AppService\) é o único mecanismo com suporte para habilitá-lo entre extensões do Microsoft Edge e componentes nativos.</span><span class="sxs-lookup"><span data-stu-id="5251f-109">The method outlined below \(connecting to a UWP app via AppService\) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span>  <span data-ttu-id="5251f-110">Confira a seção [Adicionando um](#adding-a-desktop-bridge-component) componente da Ponte de Desktop deste guia para obter mais informações sobre como habilitar a comunicação com componentes Win32 herdados.</span><span class="sxs-lookup"><span data-stu-id="5251f-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span>  

<span data-ttu-id="5251f-111">A arquitetura de mensagens nativa no Microsoft Edge aproveita a API existente como a infraestrutura subjacente de comunicação entre processos [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\).</span><span class="sxs-lookup"><span data-stu-id="5251f-111">The native messaging architecture in Microsoft Edge leverages the existing [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API as the underlying inter-process communication \(IPC\) infrastructure.</span></span>  <span data-ttu-id="5251f-112">Os aplicativos UWP usam `AppService` a API para se comunicarem entre si.</span><span class="sxs-lookup"><span data-stu-id="5251f-112">UWP apps use the `AppService` API to communicate with one another.</span></span>  <span data-ttu-id="5251f-113">Por isso, as extensões do Microsoft Edge agora podem se comunicar com aplicativos UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-113">Because of this, Microsoft Edge extensions are now able to communicate with UWP apps.</span></span>  

![arquitetura de mensagens nativa](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a><span data-ttu-id="5251f-115">Quando e quando não usar mensagens nativas</span><span class="sxs-lookup"><span data-stu-id="5251f-115">When and when not to use native messaging</span></span>  

<span data-ttu-id="5251f-116">A mensagem nativa adiciona uma nova camada inteira à sua extensão.</span><span class="sxs-lookup"><span data-stu-id="5251f-116">Native messaging adds a whole new layer to your extension.</span></span>  <span data-ttu-id="5251f-117">Ao implementar um aplicativo de parceiro UWP para sua extensão, as seguintes possibilidades ficam disponíveis para você:</span><span class="sxs-lookup"><span data-stu-id="5251f-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>  

*   <span data-ttu-id="5251f-118">Sincronizar dados \(por exemplo, credenciais\) com um aplicativo UWP parceiro.</span><span class="sxs-lookup"><span data-stu-id="5251f-118">Synchronize data \(for example credentials\) with a companion UWP app.</span></span>  
*   <span data-ttu-id="5251f-119">Implemente algoritmos de criptografia/descriptografia mais fortes não disponíveis em APIs da Web.</span><span class="sxs-lookup"><span data-stu-id="5251f-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>  
*   <span data-ttu-id="5251f-120">Acessar recursos que não são acessíveis por meio de APIs da Web, por exemplo, hardware ou dispositivos USB</span><span class="sxs-lookup"><span data-stu-id="5251f-120">Access resources that are not accessible through web APIs, for example hardware or USB devices</span></span>  

<span data-ttu-id="5251f-121">Há algumas instâncias em que as mensagens nativas não devem ser usadas devido a restrições de segurança ou política:</span><span class="sxs-lookup"><span data-stu-id="5251f-121">There are a few instances where native messaging should not be used due to security or policy restrictions:</span></span>  

*   <span data-ttu-id="5251f-122">Modificando as configurações do usuário no Microsoft Edge ou no Windows, por exemplo, alterando o navegador padrão ou o provedor de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="5251f-122">Modifying user settings in either Microsoft Edge or Windows, for example changing the default browser or search provider.</span></span>  
*   <span data-ttu-id="5251f-123">Ações que violam políticas da Microsoft Store para aplicativos e extensões.</span><span class="sxs-lookup"><span data-stu-id="5251f-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>  
*   <span data-ttu-id="5251f-124">Transferindo dados para o ponto de extremidade remoto por meio do host de mensagem nativo.</span><span class="sxs-lookup"><span data-stu-id="5251f-124">Transferring data to remote endpoint via native message host.</span></span>  
*   <span data-ttu-id="5251f-125">Permitindo que outros aplicativos baixem conteúdo que altera o comportamento da extensão.</span><span class="sxs-lookup"><span data-stu-id="5251f-125">Allowing other apps to download content that changes extension behavior.</span></span>  

## <a name="demos"></a><span data-ttu-id="5251f-126">Demonstrações</span><span class="sxs-lookup"><span data-stu-id="5251f-126">Demos</span></span>  

<span data-ttu-id="5251f-127">Para ter uma ideia de como é uma extensão de mensagens nativa do Microsoft Edge que tem um aplicativo UWP e uma Ponte de Área de Trabalho, confira os exemplos [secureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) e [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) no GitHub.</span><span class="sxs-lookup"><span data-stu-id="5251f-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>  

### <a name="how-it-works"></a><span data-ttu-id="5251f-128">Como funciona</span><span class="sxs-lookup"><span data-stu-id="5251f-128">How it works</span></span>  

<span data-ttu-id="5251f-129">O componente de extensão do Microsoft Edge do exemplo usa seu script de conteúdo para detectar quando um usuário digita informações que devem ser criptografadas.</span><span class="sxs-lookup"><span data-stu-id="5251f-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span>  <span data-ttu-id="5251f-130">A extensão comunica isso ao componente ponte de desktop por meio de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="5251f-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span>  <span data-ttu-id="5251f-131">Quando o usuário estiver pronto para enviar os dados, a extensão retornará um valor criptografado de volta ao site.</span><span class="sxs-lookup"><span data-stu-id="5251f-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>  

> [!NOTE]
> <span data-ttu-id="5251f-132">Este exemplo funcionará apenas em uma página da Web que usa eventos personalizados para se comunicar com o script de conteúdo da extensão.</span><span class="sxs-lookup"><span data-stu-id="5251f-132">This sample will only work on a webpage that uses custom events to communicate with the content script of the extension.</span></span>  <span data-ttu-id="5251f-133">A pasta de exemplo inclui um [arquivo .html para](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) testar a extensão com.</span><span class="sxs-lookup"><span data-stu-id="5251f-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>  

<span data-ttu-id="5251f-134">Neste exemplo, o aplicativo UWP é usado para passar respostas da Ponte da Área de Trabalho para o Microsoft Edge, que, em seguida, é enviado para a extensão do Microsoft Edge por meio de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5251f-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span>  <span data-ttu-id="5251f-135">Embora este exemplo tenha o host de mensagens nativo executado no aplicativo principal, ele também é capaz de ser executado como uma tarefa em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5251f-135">While this example has the native messaging host run in the main app, it is also able to run as a background task.</span></span>  <span data-ttu-id="5251f-136">Alternar entre os dois requer a edição do script em segundo plano da extensão, alterando a cadeia de caracteres `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` para `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="5251f-136">Switching between the two requires editing the background script of the extension, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>  

## <a name="chrome-vs-microsoft-edge-implementation"></a><span data-ttu-id="5251f-137">Implementação do Chrome vs Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5251f-137">Chrome vs Microsoft Edge implementation</span></span>  

<span data-ttu-id="5251f-138">Enquanto o Chrome segue a rota de usar APIs de passagem de mensagens para suas extensões se comunicarem com aplicativos, o Microsoft Edge utiliza a API que agora permite que extensões do Microsoft Edge e [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) aplicativos UWP se comuniquem.</span><span class="sxs-lookup"><span data-stu-id="5251f-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>  

<span data-ttu-id="5251f-139">Esta seção detalha as diferenças entre como o Chrome e o Microsoft Edge lidam com a implementação de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="5251f-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>  

### <a name="registration-and-host-manifest"></a><span data-ttu-id="5251f-140">Registro e manifesto de host</span><span class="sxs-lookup"><span data-stu-id="5251f-140">Registration and host manifest</span></span>  

<span data-ttu-id="5251f-141">Para que seu aplicativo seja reconhecido pela extensão como um host de mensagens nativo, ele precisará ser registrado.</span><span class="sxs-lookup"><span data-stu-id="5251f-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>  

<span data-ttu-id="5251f-142">Para o registro de host de mensagens nativas do [Chrome,](https://developer.chrome.com/extensions/nativeMessaging) seu aplicativo precisa instalar um arquivo de manifesto em qualquer lugar no sistema de arquivos do Windows que define a configuração nativa do host de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5251f-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>  

<span data-ttu-id="5251f-143">O JSON a seguir é um exemplo de configurações para o arquivo config:</span><span class="sxs-lookup"><span data-stu-id="5251f-143">The following JSON is an example of settings for the config file:</span></span>  

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

<span data-ttu-id="5251f-144">Para instalar esse arquivo, o aplicativo precisaria:</span><span class="sxs-lookup"><span data-stu-id="5251f-144">To install this file, the app would need to:</span></span>  

1.  <span data-ttu-id="5251f-145">Registre o arquivo de manifesto em um local predefinido no Registro que define a configuração do host:</span><span class="sxs-lookup"><span data-stu-id="5251f-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        <span data-ttu-id="5251f-146">or</span><span class="sxs-lookup"><span data-stu-id="5251f-146">or</span></span>  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  <span data-ttu-id="5251f-147">Definir o valor padrão dessa chave para o caminho completo para o arquivo de manifesto, por exemplo</span><span class="sxs-lookup"><span data-stu-id="5251f-147">Set the default value of that key to the full path to the manifest file, for example</span></span> `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

<span data-ttu-id="5251f-148">Para o Microsoft Edge, para registrar um \(host de mensagens nativo\) você deve incluir o aplicativo de parceiro UWP no mesmo pacote que sua extensão e especificar a extensão AppService no arquivo do seu [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) `Package.appxmanifest` projeto.</span><span class="sxs-lookup"><span data-stu-id="5251f-148">For Microsoft Edge, in order to register an [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(native messaging host\) you must include the UWP companion app in the same package as your extension and specify the [AppService extension](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in the `Package.appxmanifest` file of your project.</span></span>  <span data-ttu-id="5251f-149">Os `EntryPoint` atributos e podem ser `Name` configurados por você:</span><span class="sxs-lookup"><span data-stu-id="5251f-149">The `EntryPoint` and `Name` attributes may be configured by you:</span></span>  

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

<span data-ttu-id="5251f-150">Você também precisa definir quais extensões têm permissão para se conectar ao serviço.</span><span class="sxs-lookup"><span data-stu-id="5251f-150">You also need to set which extensions are allowed to connect to the service.</span></span>  <span data-ttu-id="5251f-151">Como o Microsoft Edge não tem uma propriedade de manifesto equivalente em seu AppxManifest, isso precisará ser determinado e imposto em tempo de execução pelo `"allowed_origins"` seu aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-151">Because Microsoft Edge does not have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span>  <span data-ttu-id="5251f-152">Como o Microsoft Edge estabelece a conexão em nome da extensão, o aplicativo procura o Nome da Família de Pacotes do chamador para determinar se a extensão está sendo conectada pelo Microsoft Edge para controlar ou autenticar o chamador.</span><span class="sxs-lookup"><span data-stu-id="5251f-152">Since Microsoft Edge establishes the connection on behalf of the extension, the app looks up the Package Family Name of the caller to determine if extension is being connected by Microsoft Edge to control or authenticate the caller.</span></span>  <span data-ttu-id="5251f-153">Por exemplo</span><span class="sxs-lookup"><span data-stu-id="5251f-153">For example</span></span>   

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

### <a name="message-sending"></a><span data-ttu-id="5251f-154">Envio de mensagens</span><span class="sxs-lookup"><span data-stu-id="5251f-154">Message sending</span></span>  

<span data-ttu-id="5251f-155">Para que um aplicativo e uma extensão se comuniquem entre si, as mensagens precisam ser enviadas para e para elas.</span><span class="sxs-lookup"><span data-stu-id="5251f-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>  

<span data-ttu-id="5251f-156">As extensões do Chrome iniciam uma mensagem usando a API para entregar uma mensagem ao [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) host nativo usando um canal não persistente.</span><span class="sxs-lookup"><span data-stu-id="5251f-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span>  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="5251f-157">O primeiro parâmetro é o nome do host nativo, que o Chrome procura no registro do manifesto.</span><span class="sxs-lookup"><span data-stu-id="5251f-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span>  <span data-ttu-id="5251f-158">O manifesto especifica o .exe que o Chrome iniciará em uma área de ressalva e a mensagem é enviada usando std e/s.</span><span class="sxs-lookup"><span data-stu-id="5251f-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span>  
<span data-ttu-id="5251f-159">As extensões também estabelecem um canal persistente usando a API, que usa o nome do `runtime.connectNative` host nativo como o único parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5251f-159">Extensions also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span>  

<span data-ttu-id="5251f-160">O Microsoft Edge usa a mesma construção que a API de mensagens nativa no Chrome para permitir que extensões do Microsoft Edge especifiquem a qual serviço de aplicativo se conectar.</span><span class="sxs-lookup"><span data-stu-id="5251f-160">Microsoft Edge uses the same construct as the native messaging API in Chrome to allow Microsoft Edge extensions to specify which app service to connect to.</span></span>  <span data-ttu-id="5251f-161">O primeiro parâmetro em `runtime.sendNativeMessage` especifica o nome do serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5251f-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span>  <span data-ttu-id="5251f-162">Na seção [Registro e manifesto do host,](#registration-and-host-manifest) este é `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="5251f-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span>  <span data-ttu-id="5251f-163">A plataforma de extensão do Microsoft Edge restringe o host de mensagens nativo a ser um aplicativo UWP empacotado no mesmo AppX que a extensão.</span><span class="sxs-lookup"><span data-stu-id="5251f-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span>  <span data-ttu-id="5251f-164">Isso reduz os riscos de segurança associados a ataques mal-intencionados que tentam conectar o Microsoft Edge a outro Nome da Família de Pacotes violando entradas de manifesto.</span><span class="sxs-lookup"><span data-stu-id="5251f-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span>  

<span data-ttu-id="5251f-165">Isso significa que o Microsoft Edge usará o mesmo Nome da Família de Pacotes que a extensão, além do nome especificado na API, para identificar exclusivamente o provedor do serviço `AppService` de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5251f-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="5251f-166">Isso não será facilmente convertido pelo [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5251f-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span>  <span data-ttu-id="5251f-167">Todas as extensões que especificam a permissão serão sinalizadas como `"nativeMessaging"` exigindo a conversão manual para este componente.</span><span class="sxs-lookup"><span data-stu-id="5251f-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>  

### <a name="communication-protocol"></a><span data-ttu-id="5251f-168">Protocolo de comunicação</span><span class="sxs-lookup"><span data-stu-id="5251f-168">Communication protocol</span></span>  

<span data-ttu-id="5251f-169">O protocolo de comunicação para mensagens nativas determina como as mensagens são formatadas antes do envio.</span><span class="sxs-lookup"><span data-stu-id="5251f-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>  

<span data-ttu-id="5251f-170">O Chrome inicia cada host de mensagens nativa em um processo separado e se comunica com ele usando entrada padrão e saída padrão.</span><span class="sxs-lookup"><span data-stu-id="5251f-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span>  <span data-ttu-id="5251f-171">O mesmo formato é usado para enviar mensagens em ambas as direções: cada mensagem é serializada usando JSON, UTF-8 codificado e precedido com comprimento de mensagem de 32 bits na ordem de byte nativo.</span><span class="sxs-lookup"><span data-stu-id="5251f-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>  

<span data-ttu-id="5251f-172">Para o Microsoft Edge, o aplicativo principal/tarefa em segundo plano que implementa o serviço de aplicativo será iniciado pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="5251f-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span>  <span data-ttu-id="5251f-173">Na inicialização, `Run` o método da tarefa em segundo plano é invocado:</span><span class="sxs-lookup"><span data-stu-id="5251f-173">On startup, the `Run` method of the background task is invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service is not stopped and ended.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="5251f-174">Quando sua extensão envia uma mensagem para seu aplicativo UWP, [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) o evento será gerado.</span><span class="sxs-lookup"><span data-stu-id="5251f-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) event will be raised.</span></span>  <span data-ttu-id="5251f-175">Esta mensagem formatada JSON será então stringified no primeiro par KeyValue de um [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) objeto.</span><span class="sxs-lookup"><span data-stu-id="5251f-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object.</span></span>  <span data-ttu-id="5251f-176">:</span><span class="sxs-lookup"><span data-stu-id="5251f-176">:</span></span>  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="5251f-177">Quando seu aplicativo UWP envia uma resposta de volta à sua extensão, um [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) será adicionado ao `ValueSet` objeto.</span><span class="sxs-lookup"><span data-stu-id="5251f-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) will be added to the `ValueSet` object.</span></span>  <span data-ttu-id="5251f-178">A `Key` propriedade será ignorada pelo Microsoft Edge, mas `Value` a propriedade conterá uma cadeia de caracteres JSON válida.</span><span class="sxs-lookup"><span data-stu-id="5251f-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>  

### <a name="callback"></a><span data-ttu-id="5251f-179">Retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="5251f-179">Callback</span></span>  

<span data-ttu-id="5251f-180">Para retornos de chamada, o Chrome usa o que permite que uma função de retorno de chamada manipular qualquer [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) resposta assíncrona do envio de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5251f-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>  

<span data-ttu-id="5251f-181">O Microsoft Edge usa [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) o método do objeto para permitir que o aplicativo envie um objeto de volta para a [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) extensão.</span><span class="sxs-lookup"><span data-stu-id="5251f-181">Microsoft Edge uses the [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) method  of the [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) object to let the app send a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object back to the extension.</span></span>  

### <a name="message-size-limit"></a><span data-ttu-id="5251f-182">Limite de tamanho da mensagem</span><span class="sxs-lookup"><span data-stu-id="5251f-182">Message size limit</span></span>  

<span data-ttu-id="5251f-183">As mensagens enviadas de um lado para o outro entre uma extensão e um aplicativo têm limitações de tamanho de mensagem diferentes para o Chrome e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5251f-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>  

<span data-ttu-id="5251f-184">O Chrome tem as seguintes limitações de tamanho de mensagem:</span><span class="sxs-lookup"><span data-stu-id="5251f-184">Chrome has the following message size limitations:</span></span>  

*   <span data-ttu-id="5251f-185">Limite de mensagem única do host de mensagens nativa: 1 MB</span><span class="sxs-lookup"><span data-stu-id="5251f-185">Single message limit from native messaging host:  1 MB</span></span>  
*   <span data-ttu-id="5251f-186">Limite de mensagem único enviado para o host de mensagens nativo: 4 GB</span><span class="sxs-lookup"><span data-stu-id="5251f-186">Single message limit sent to native messaging host:  4 GB</span></span>  

<span data-ttu-id="5251f-187">Para o Microsoft Edge, embora não tenha limite para o tamanho da mensagem \(dependente da memória\), o Microsoft Edge protege a si mesmo contra o comportamento errado de aplicativos nativos, impondo os seguintes limites de tamanho da `AppService` mensagem:</span><span class="sxs-lookup"><span data-stu-id="5251f-187">For Microsoft Edge, while `AppService` has no limit on message size \(dependent on memory\), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>  

*   <span data-ttu-id="5251f-188">Limite de mensagem única do aplicativo UWP para a extensão: 1 MB</span><span class="sxs-lookup"><span data-stu-id="5251f-188">Single message limit from UWP app to extension: 1 MB</span></span>  
*   <span data-ttu-id="5251f-189">Limite de mensagem única da extensão para o aplicativo UWP: 100 MB</span><span class="sxs-lookup"><span data-stu-id="5251f-189">Single message limit from extension to UWP app: 100 MB</span></span>  

### <a name="native-messaging-connections"></a><span data-ttu-id="5251f-190">Conexões de mensagens nativas</span><span class="sxs-lookup"><span data-stu-id="5251f-190">Native messaging connections</span></span>  

<span data-ttu-id="5251f-191">Há dois tipos de conexões para mensagens nativas; persistente e não persistente.</span><span class="sxs-lookup"><span data-stu-id="5251f-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>  
<span data-ttu-id="5251f-192">Uma **conexão** persistente é uma conexão que é mantida em execução até que a porta seja destruída.</span><span class="sxs-lookup"><span data-stu-id="5251f-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span>  <span data-ttu-id="5251f-193">Uma **conexão não persistente** é uma conexão que é aberta para uma mensagem de cada vez e fecha após a entrega.</span><span class="sxs-lookup"><span data-stu-id="5251f-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>  

#### <a name="persistent"></a><span data-ttu-id="5251f-194">Persistente</span><span class="sxs-lookup"><span data-stu-id="5251f-194">Persistent</span></span>  

<span data-ttu-id="5251f-195">Para o Chrome, uma conexão persistente é feita criando uma porta de mensagens usando [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="5251f-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="5251f-196">Depois que a porta é feita, o Chrome inicia um processo de host de mensagens nativo que permanece em execução até que a porta seja destruída.</span><span class="sxs-lookup"><span data-stu-id="5251f-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>  

<span data-ttu-id="5251f-197">Para o Microsoft Edge, depois que uma porta de mensagens é criada usando , o Microsoft Edge inicia e a mantém em execução até que a `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) porta seja destruída.</span><span class="sxs-lookup"><span data-stu-id="5251f-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) and keeps it running until the port is destroyed.</span></span>  <span data-ttu-id="5251f-198">O trecho a seguir mostra como uma conexão persistente é estabelecida de dentro de um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span>  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a><span data-ttu-id="5251f-199">Não persistente</span><span class="sxs-lookup"><span data-stu-id="5251f-199">Non-persistent</span></span>  

<span data-ttu-id="5251f-200">Quando uma mensagem é enviada usando no Chrome, sem criar uma porta de mensagens, o Chrome inicia um novo processo de host de [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) mensagens nativa para cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="5251f-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span>  <span data-ttu-id="5251f-201">A primeira mensagem gerada pelo processo de host é tratada como uma resposta à solicitação original e todas as outras mensagens depois de ignoradas.</span><span class="sxs-lookup"><span data-stu-id="5251f-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>  

<span data-ttu-id="5251f-202">O Microsoft Edge interrompe e encerra a conexão depois que todas as respostas a cada mensagem são recebidas.</span><span class="sxs-lookup"><span data-stu-id="5251f-202">Microsoft Edge stops and ends the connection after every response to each message has been received.</span></span>  <span data-ttu-id="5251f-203">O trecho a seguir mostra uma conexão não persistente estabelecida com ela que será encerrada no aplicativo UWP após uma solicitação ter sido recebida e armazenada como `AppServiceConnection` [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) um .</span><span class="sxs-lookup"><span data-stu-id="5251f-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true).</span></span>  

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

### <a name="permission"></a><span data-ttu-id="5251f-204">Permissão</span><span class="sxs-lookup"><span data-stu-id="5251f-204">Permission</span></span>  

<span data-ttu-id="5251f-205">Para habilitar o uso de mensagens nativas com sua extensão, para o Chrome e o Microsoft Edge, você deve declarar a `"nativeMessaging"` permissão em seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="5251f-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you must declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>  

## <a name="app-services"></a><span data-ttu-id="5251f-206">Serviços de aplicativo</span><span class="sxs-lookup"><span data-stu-id="5251f-206">App services</span></span>  

<span data-ttu-id="5251f-207">Esta seção detalha o impacto que os serviços de aplicativos têm no desempenho e na memória de mensagens nativas do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5251f-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>  

### <a name="performance"></a><span data-ttu-id="5251f-208">Desempenho</span><span class="sxs-lookup"><span data-stu-id="5251f-208">Performance</span></span>  

<span data-ttu-id="5251f-209">Os serviços de aplicativo são "patrocinados" pelo aplicativo em primeiro plano que os chama, que para fins de mensagens nativas é o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5251f-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span>  <span data-ttu-id="5251f-210">Isso significa que os serviços de aplicativo podem ser executados enquanto o Microsoft Edge está em execução.</span><span class="sxs-lookup"><span data-stu-id="5251f-210">This means that app services can run as long as Microsoft Edge is running.</span></span>  

<span data-ttu-id="5251f-211">Em relação à latência, os serviços de aplicativo usam pipes nomeados que, após a conexão inicial, permitem que dois aplicativos se comuniquem diretamente.</span><span class="sxs-lookup"><span data-stu-id="5251f-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span>  <span data-ttu-id="5251f-212">Esse método de comunicação produz baixa latência.</span><span class="sxs-lookup"><span data-stu-id="5251f-212">This method of communication produces low latency.</span></span>  <span data-ttu-id="5251f-213">Dispositivos com CPUs lentas experimentarão alguma latência inicial após iniciar o processo que hospeda o serviço de aplicativo \(~80ms) para iniciar a tarefa em segundo plano em alguns dispositivos\).</span><span class="sxs-lookup"><span data-stu-id="5251f-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service \(~80ms to startup the background task on some devices\).</span></span>  <span data-ttu-id="5251f-214">Após a start-up, o desempenho em dispositivos de CPU lentos deve ser bom.</span><span class="sxs-lookup"><span data-stu-id="5251f-214">After start-up, performance on slow CPU devices should be good.</span></span>  

### <a name="memory"></a><span data-ttu-id="5251f-215">Memória</span><span class="sxs-lookup"><span data-stu-id="5251f-215">Memory</span></span>  

<span data-ttu-id="5251f-216">A memória alocada a um serviço de aplicativo é retirada da cota alocada para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5251f-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span>  <span data-ttu-id="5251f-217">Isso significa que, se o Microsoft Edge iniciar muitos serviços de aplicativo, há a possibilidade de que eles podem ficar sem memória.</span><span class="sxs-lookup"><span data-stu-id="5251f-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span>  <span data-ttu-id="5251f-218">Os caps de memória da tarefa em segundo plano comuns são imposto nos serviços de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5251f-218">The usual background task memory caps are enforced on app services.</span></span>  <span data-ttu-id="5251f-219">Por exemplo, em um dispositivo de 512 MB, uma tarefa em segundo plano do serviço de aplicativo não pode ser maior do que 16 MB.</span><span class="sxs-lookup"><span data-stu-id="5251f-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span>  <span data-ttu-id="5251f-220">Esse número sobe conforme os dispositivos são dimensionados.</span><span class="sxs-lookup"><span data-stu-id="5251f-220">This number goes up as the devices scale up.</span></span>  

## <a name="creating-an-extension-with-native-messaging"></a><span data-ttu-id="5251f-221">Criando uma extensão com mensagens nativas</span><span class="sxs-lookup"><span data-stu-id="5251f-221">Creating an extension with native messaging</span></span>  

<span data-ttu-id="5251f-222">Para testar a mensagem nativa, sua extensão precisa de um Nome da Família de Pacotes.</span><span class="sxs-lookup"><span data-stu-id="5251f-222">In order to test native messaging, your extension needs a Package Family Name.</span></span>  <span data-ttu-id="5251f-223">O Microsoft Edge usa isso para determinar a identidade nativa do host de mensagens, o que significa que sua extensão deve ser empacotada.</span><span class="sxs-lookup"><span data-stu-id="5251f-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span>  

<span data-ttu-id="5251f-224">Para criar sua extensão com mensagens nativas em Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="5251f-224">To create your extension with native messaging in Visual Studio:</span></span>  

1.  <span data-ttu-id="5251f-225">Crie um projeto UWP em Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5251f-225">Create a UWP project in Visual Studio.</span></span>  
1.  <span data-ttu-id="5251f-226">[Adicione `AppService` ao seu aplicativo UWP](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="5251f-226">[Add `AppService` to your UWP app](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>  
    *   <span data-ttu-id="5251f-227">Opcionalmente, você pode configurar para ser hospedado no aplicativo [ `AppService` principal,](/windows/uwp/launch-resume/convert-app-service-in-process) em vez de como uma tarefa em segundo plano neste ponto.</span><span class="sxs-lookup"><span data-stu-id="5251f-227">You can optionally [configure `AppService` to be hosted in the main app](/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>  
1.  <span data-ttu-id="5251f-228">Crie e teste seu projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-228">Build and test your UWP project.</span></span>  
    *   <span data-ttu-id="5251f-229">Opcionalmente, você pode adicionar um componente [da Ponte de Desktop.](#adding-a-desktop-bridge-component)</span><span class="sxs-lookup"><span data-stu-id="5251f-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>  
1.  <span data-ttu-id="5251f-230">Crie uma extensão do Microsoft Edge que usa mensagens nativas para se comunicar com o aplicativo da UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span>  <span data-ttu-id="5251f-231">Os arquivos de extensão podem ser adicionados a uma pasta `Extension` chamada no projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span>  <span data-ttu-id="5251f-232">Todos os arquivos abaixo dessa pasta, incluindo subpastas, precisam ter suas propriedades configuradas de forma que `Build Action=Content` e `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="5251f-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  <span data-ttu-id="5251f-233">`manifest.json`Certifique-se de que também está configurado com essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5251f-233">Make sure `manifest.json` is also configured with these properties.</span></span>  
1.  <span data-ttu-id="5251f-234">Modifique o arquivo no projeto para incluir metadados de extensão e `package.manifest.xml` converta-o em um aplicativo sem cabeça adicionando `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="5251f-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>  
    
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
    
1.  <span data-ttu-id="5251f-235">Use o `AppService` nome configurado para a UWP nas APIs de mensagens nativas.</span><span class="sxs-lookup"><span data-stu-id="5251f-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>  
1.  <span data-ttu-id="5251f-236">Build and [deploy](#deploying) the UWP project \(with the optional Desktop Bridge component\).</span><span class="sxs-lookup"><span data-stu-id="5251f-236">Build and [deploy](#deploying) the UWP project \(with the optional Desktop Bridge component\).</span></span>  
1.  <span data-ttu-id="5251f-237">[Empacote](#packaging) sua extensão de mensagens nativa quando estiver pronta para envio da Loja</span><span class="sxs-lookup"><span data-stu-id="5251f-237">[Package](#packaging) your native messaging extension once it is ready for Store submission</span></span>  
    
> [!NOTE]
> <span data-ttu-id="5251f-238">Consulte a [seção Demos](#demos) para um exemplo de uma extensão de mensagens nativa completa.</span><span class="sxs-lookup"><span data-stu-id="5251f-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>  

## <a name="adding-a-desktop-bridge-component"></a><span data-ttu-id="5251f-239">Adicionando um componente da Ponte de Desktop</span><span class="sxs-lookup"><span data-stu-id="5251f-239">Adding a Desktop Bridge component</span></span>  

<span data-ttu-id="5251f-240">Se quiser adicionar um componente da Ponte de Desktop ao pacote, crie e crie seu projeto Win32 em Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5251f-240">If you want to add a Desktop Bridge component to your package, you must create and build your Win32 project in Visual Studio.</span></span>  <span data-ttu-id="5251f-241">Para obter informações sobre como converter seu aplicativo win32 em UWP, consulte [Portando aplicativos para Windows 10 via Ponte de Desktop](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="5251f-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span>  <span data-ttu-id="5251f-242">Depois de Visual Studio, você pode adicionar o executável Win32 ao pacote executando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5251f-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>  

1.  <span data-ttu-id="5251f-243">Adicione o projeto Win32 à mesma solução do projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-243">Add the Win32 project to the same solution as the UWP project.</span></span>  
1.  <span data-ttu-id="5251f-244">De definir o projeto Win32 como um projeto dependente para o projeto UWP:</span><span class="sxs-lookup"><span data-stu-id="5251f-244">Set the Win32 project as a dependent project for the UWP project:</span></span>  
    
    ![configurando dependências do projeto](../media/project-dependencies.png)  
    
1.  <span data-ttu-id="5251f-246">Crie uma `Win32` pasta dentro do projeto UWP.</span><span class="sxs-lookup"><span data-stu-id="5251f-246">Create a `Win32` folder within the UWP project.</span></span>  <span data-ttu-id="5251f-247">Copie os binários necessários para `Win32` o projeto para esta pasta.</span><span class="sxs-lookup"><span data-stu-id="5251f-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span>  <span data-ttu-id="5251f-248">Configure as propriedades de todos os binários como `Build Action=Content` esse e `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="5251f-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  
    
    ![folder with win32 and UWP app files in it](../media/desktop-bridge.png)  
    
1.  <span data-ttu-id="5251f-250">Modifique o arquivo de projeto UWP para copiar todos os binários necessários para o projeto nesta pasta usando o comando de evento `Win32` PostBuild.</span><span class="sxs-lookup"><span data-stu-id="5251f-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span>  <span data-ttu-id="5251f-251">Isso garante que os binários atualizados sejam copiados para a pasta sempre que a solução for reconstruída.</span><span class="sxs-lookup"><span data-stu-id="5251f-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  <span data-ttu-id="5251f-252">Modifique `package.manifest.xml` adicionando `<desktop:Extension>` o elemento ao `<Extensions>` elemento:</span><span class="sxs-lookup"><span data-stu-id="5251f-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a><span data-ttu-id="5251f-253">Implantando</span><span class="sxs-lookup"><span data-stu-id="5251f-253">Deploying</span></span>  

<span data-ttu-id="5251f-254">Depois de configurar o projeto UWP \(e, opcionalmente, o projeto Win32\) conforme descrito acima, você está pronto para implantar a solução usando Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5251f-254">Once you have configured your UWP project \(and optionally Win32 project\) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>  

![build inprocess project](../media/native-message-uwp-debug.png)  

<span data-ttu-id="5251f-256">Depois que a solução for implantada corretamente, você deverá ver sua extensão no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5251f-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>  

![exibição de extensão no Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a><span data-ttu-id="5251f-258">Embalagem</span><span class="sxs-lookup"><span data-stu-id="5251f-258">Packaging</span></span>  

> [!NOTE]
> <span data-ttu-id="5251f-259">No momento, enviar uma extensão do Microsoft Edge à Microsoft Store é um recurso restrito.</span><span class="sxs-lookup"><span data-stu-id="5251f-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="5251f-260">[Envie uma solicitação](https://developer.microsoft.com/microsoft-edge/extensions/requests/) para fazer parte da Microsoft Store e seja considerada para atualizações futuras.</span><span class="sxs-lookup"><span data-stu-id="5251f-260">[Send a request](https://developer.microsoft.com/microsoft-edge/extensions/requests/) to be a part of the Microsoft Store, and be considered for future updates.</span></span>  

<span data-ttu-id="5251f-261">Você pode gerar um pacote da Store para envio para o Centro de Dev do Windows usando a funcionalidade Visual Studio local:</span><span class="sxs-lookup"><span data-stu-id="5251f-261">You may generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>  

![Criando pacote da Loja](../media/create-store-package.png)  

## <a name="debugging"></a><span data-ttu-id="5251f-263">Depuração</span><span class="sxs-lookup"><span data-stu-id="5251f-263">Debugging</span></span>  

<span data-ttu-id="5251f-264">As instruções para depuração variam dependendo de qual componente você deseja testar:</span><span class="sxs-lookup"><span data-stu-id="5251f-264">The instructions for debugging vary depending on which component you want to test out:</span></span>  

### <a name="debugging-the-extension"></a><span data-ttu-id="5251f-265">Depurando a extensão</span><span class="sxs-lookup"><span data-stu-id="5251f-265">Debugging the extension</span></span>  

<span data-ttu-id="5251f-266">Depois que a solução for implantada, a extensão será instalada no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5251f-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span>  <span data-ttu-id="5251f-267">Confira o guia [Depuração](./debugging-extensions.md) para obter informações sobre como depurar uma extensão.</span><span class="sxs-lookup"><span data-stu-id="5251f-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>  

### <a name="debugging-the-uwp-app"></a><span data-ttu-id="5251f-268">Depuração do aplicativo UWP</span><span class="sxs-lookup"><span data-stu-id="5251f-268">Debugging the UWP app</span></span>  

<span data-ttu-id="5251f-269">O aplicativo UWP será lançado quando a extensão tentar se conectar a ele usando [APIs de mensagens nativas.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)</span><span class="sxs-lookup"><span data-stu-id="5251f-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="5251f-270">Você deve depurar o aplicativo UWP somente depois que o processo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5251f-270">You must debug the UWP app only once the process starts.</span></span>  <span data-ttu-id="5251f-271">Isso pode ser configurado usando a página Propriedade do projeto:</span><span class="sxs-lookup"><span data-stu-id="5251f-271">This may be configured using the Property page of the project:</span></span>  

1.  <span data-ttu-id="5251f-272">Em Visual Studio, passe o mouse no projeto de aplicativo UWP e abra o menu contextual \(clique com o botão direito do mouse\)</span><span class="sxs-lookup"><span data-stu-id="5251f-272">In Visual Studio, hover on your UWP app project and open the contextual menu \(right-click\)</span></span>  
1.  <span data-ttu-id="5251f-273">Selecionar **Propriedades**</span><span class="sxs-lookup"><span data-stu-id="5251f-273">Select **Properties**</span></span>  
1.  <span data-ttu-id="5251f-274">Verificar **Não iniciar, mas depurar meu código quando ele for iniciado**</span><span class="sxs-lookup"><span data-stu-id="5251f-274">Check **Do not launch, but debug my code when it starts**</span></span>  
    
    ![selecionar não iniciar caixa](../media/native-message-do-not-launch.png)  
    
<span data-ttu-id="5251f-276">No Visual Studio agora você pode definir pontos de interrupção no código onde deseja depurar e, em seguida, iniciar o depurador pressionando F5.</span><span class="sxs-lookup"><span data-stu-id="5251f-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span>  <span data-ttu-id="5251f-277">Depois de interagir com a extensão para se conectar ao aplicativo UWP, Visual Studio anexar automaticamente ao processo.</span><span class="sxs-lookup"><span data-stu-id="5251f-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>  

### <a name="debugging-the-desktop-bridge"></a><span data-ttu-id="5251f-278">Depurando a ponte da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="5251f-278">Debugging the Desktop Bridge</span></span>  

<span data-ttu-id="5251f-279">Mesmo que haja vários métodos para [depurar](/windows/msix/desktop/desktop-to-uwp-debug) uma Ponte de Desktop \(aplicativo Win32 convertido\), o único aplicável a esses cenários é a opção PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="5251f-279">Even though there are various [methods for debugging a Desktop Bridge](/windows/msix/desktop/desktop-to-uwp-debug) \(converted Win32 app\), the only one applicable for this scenarios is the PLMDebug option.</span></span>  <span data-ttu-id="5251f-280">Você também pode adicionar código de depuração à função de inicialização para executar uma espera por um horário específico, permitindo que você anexe Visual Studio ao processo.</span><span class="sxs-lookup"><span data-stu-id="5251f-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>  
