---
description: Saiba como você pode usar o recurso de mensagens nativas para que sua extensão se comunique com um aplicativo UWP complementar.
title: Extensões-mensagens nativas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, nativo, mensagens, UWP
ms.openlocfilehash: 83f80e112180317c38763225c1cdd015da4238b0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561209"
---
# Mensagens nativas no Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Visão geral da arquitetura de mensagens nativa

Com a atualização do Windows 10 Creator, as extensões do Microsoft Edge podem usar o recurso de mensagens nativas para se comunicar com um aplicativo da plataforma universal do Windows (UWP) complementar.  Em um nível alto, as extensões do Microsoft Edge usam as mesmas APIs para mensagens nativas como extensões Chrome e Firefox. No entanto, o host de mensagens nativa precisará ser implementado usando a plataforma universal do Windows.

> [!NOTE]
> O método descrito abaixo (conectando a um aplicativo UWP via AppService) é o único mecanismo com suporte para habilitar a comunicação entre extensões do Microsoft Edge e componentes nativos. Consulte a seção [Adicionar um componente da ponte da área de trabalho](#adding-a-desktop-bridge-component) deste guia para obter mais informações sobre como habilitar a comunicação com componentes herdados do Win32. 

 A arquitetura de mensagens nativas da Microsoft Edge aproveita a [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API existente como a infraestrutura de comunicação entre processos (IPC) subjacente. Os aplicativos UWP usam a `AppService` API para se comunicar uns com os outros. Por isso, as extensões do Microsoft Edge agora podem se comunicar com aplicativos UWP.

![arquitetura de mensagens nativa](./../media/native-messaging-architecture.png)


### Quando e quando não usar mensagens nativas

O recurso de mensagens nativas adiciona uma nova camada inteira à sua extensão. Ao implementar um aplicativo de complemento UWP para sua extensão, as seguintes possibilidades são disponibilizadas para você:

* Sincronize dados (por exemplo, credenciais) com um aplicativo UWP complementar.
* Implementar algoritmos de criptografia/descriptografia mais forte não disponíveis em APIs da Web.
* Acesse recursos que não podem ser acessados por meio de APIs da Web, por exemplo, hardware ou dispositivos USB

Há alguns casos em que as mensagens nativas não podem ser usadas devido a restrições de segurança ou política:

* Modificando as configurações do usuário no Microsoft Edge ou no Windows, por exemplo, alterar o navegador padrão ou o provedor de pesquisa.
* Ações que violam políticas da Microsoft Store para aplicativos e extensões.
* Transferindo dados para um ponto de extremidade remoto por meio do host de mensagens nativa.
* Permitir que outros aplicativos baixem conteúdo que altera o comportamento da extensão.

## Demonstrações

Para ter uma noção de qual é a aparência de uma extensão de mensagens nativas do Microsoft Edge que tenha um aplicativo UWP complementar e uma ponte da área de trabalho, confira os exemplos [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) e [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) no github.

### Como funciona

O componente de extensão do Microsoft Edge da amostra usa seu script de conteúdo para detectar quando um usuário está digitando informações que devem ser criptografadas. A extensão comunica isso ao componente da ponte da área de trabalho via mensagens nativas. Quando o usuário está pronto para enviar os dados, a extensão retorna um valor criptografado de volta para o site.

> [!NOTE]
> Este exemplo só funcionará em uma página da Web que usa eventos personalizados para se comunicar com o script de conteúdo da extensão. A pasta de exemplo inclui um [arquivo. html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) para testar a extensão.

Neste exemplo, o aplicativo UWP é usado para passar respostas da ponte da área de trabalho para o Microsoft Edge, que, em seguida, são enviados à extensão do Microsoft Edge por meio de retorno de chamada. Embora este exemplo tenha o host de mensagens nativa executado no aplicativo principal, ele também pode ser executado como uma tarefa em segundo plano. Alternar entre os dois exige a edição do script de plano de fundo da extensão, alterando a cadeia de caracteres `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` para `"NativeMessagingHostOutOfProcess"` .

## Implementação do Chrome versus Microsoft Edge

Embora o Chrome seja a rota de usar APIs de transmissão de mensagens para suas extensões para se comunicar com os aplicativos, o Microsoft Edge utiliza a [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API que agora permite que as extensões do Microsoft Edge e os aplicativos UWP se comuniquem.

Esta seção detalha as diferenças entre como o Chrome e o Microsoft Edge manipulam a implementação de mensagens nativas.

### Manifesto de host e registro
Para que seu aplicativo seja reconhecido pela extensão como um host de mensagens nativo, ele precisará ser registrado.


Para o registro do host de [mensagens nativas do Chrome](https://developer.chrome.com/extensions/nativeMessaging) , seu aplicativo precisa instalar um arquivo de manifesto em qualquer lugar no sistema de arquivos do Windows que define a configuração do host de mensagens nativa.

O JSON a seguir é um exemplo de como o arquivo de configuração pode ser configurado:

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

Para instalar esse arquivo, o aplicativo precisa:

1. Registre o arquivo de manifesto em um local predefinido no registro que define a configuração do host:
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     ou
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. Defina o valor padrão dessa chave para o caminho completo para o arquivo de manifesto, por exemplo,  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




Para o Microsoft Edge, a fim de registrar um [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (host de mensagens nativa), você precisará incluir o aplicativo de complemento UWP no mesmo pacote que a extensão e especificar a [extensão AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) no arquivo do seu projeto `Package.appxmanifest` . Os `EntryPoint` `Name` atributos e podem ser configurados por você:

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


Você também precisará definir quais extensões têm permissão para se conectar ao serviço. Como o Microsoft Edge não tem uma `"allowed_origins"` propriedade de manifesto equivalente em seu AppxManifest, ela precisará ser determinada e imposta em tempo de execução pelo seu aplicativo UWP. Como o Microsoft Edge irá estabelecer a conexão em nome da extensão, o aplicativo pode procurar o nome da família do pacote do chamador para determinar se ele está sendo conectado pelo Microsoft Edge para controlar ou autenticar o chamador. Ex. 

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



### Envio de mensagens

Para que um aplicativo e uma extensão se comuniquem uns com os outros, é preciso que as mensagens sejam enviadas para e a partir deles.

As extensões Chrome iniciam uma mensagem usando a [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API para entregar uma mensagem ao host nativo usando um canal não persistente. 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

O primeiro parâmetro é o nome do host nativo, que parece ser exibido pelo Chrome no registro do manifesto. O manifesto especifica o. exe que o Chrome abrirá em uma área restrita e a mensagem será enviada usando e/s padrão. As extensões também podem estabelecer um canal persistente usando a `runtime.connectNative` API, que usa o nome do host nativo como o único parâmetro. 

O Microsoft Edge usa a mesma construção da API de mensagens nativas do Chrome para permitir que as extensões do Microsoft Edge especifiquem a qual serviço de aplicativo se conectar. O primeiro parâmetro em `runtime.sendNativeMessage` especifica o nome do serviço de aplicativo. Na seção [Registration and host manifest](#registration-and-host-manifest) , isso é `"com.microsoft.inventory"` . A plataforma de extensão do Microsoft Edge restringe o host de mensagens nativa a ser um aplicativo UWP que é empacotado no mesmo AppX que a extensão. Isso atenua quaisquer riscos de segurança associados a ataques maliciosos que tentam conectar o Microsoft Edge com outro nome de família de pacote violando as entradas de manifesto. 

Isso significa que o Microsoft Edge usará o mesmo nome da família de pacotes como a extensão, além do `AppService` nome especificado na API, para identificar exclusivamente o provedor do serviço de aplicativo.  

> [!NOTE]
> Isso não será facilmente convertido pelo kit de [ferramentas de extensão do Microsoft Edge](./porting-chrome-extensions.md). Qualquer extensão que especifica a `"nativeMessaging"` permissão será sinalizada como exigindo conversão manual para esse componente.





### Protocolo de comunicação

O protocolo de comunicação para mensagens nativas determina como as mensagens são formatadas antes do envio.

O Chrome inicia cada host de mensagens nativa em um processo separado e se comunica com ele usando a entrada padrão e a saída padrão. O mesmo formato é usado para enviar mensagens em ambas as direções: cada mensagem é serializada usando JSON, UTF-8 codificado e é precedido com o comprimento da mensagem de 32 bits em uma ordem de bytes nativa.


Para o Microsoft Edge, a tarefa em segundo plano/aplicativo principal que implementa o serviço de aplicativo será iniciada pela plataforma. Na inicialização, o método da tarefa em segundo plano `Run` será invocado:  

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

Quando a extensão envia uma mensagem para seu aplicativo UWP, o [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) evento será gerado. Essa mensagem formatada em JSON será stringifiedda no primeiro par de valores de um [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto. :

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

Quando seu aplicativo UWP envia uma resposta de volta para a extensão, a a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) será adicionada ao `ValueSet` objeto. A `Key` propriedade será ignorada pelo Microsoft Edge, mas a `Value` Propriedade conterá uma cadeia de caracteres JSON válida.

### Retorno

Para retornos de chamada, [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) o Chrome usa que permite uma função de retorno de chamada para manipular qualquer resposta assíncrona de enviar uma mensagem.

O Microsoft Edge usa o [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) método do objeto [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) para permitir que o aplicativo envie um [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto de volta para a extensão.


### Limite de tamanho da mensagem
As mensagens enviadas entre uma extensão e um aplicativo têm limitações de tamanho de mensagens diferentes no lugar para o Chrome e o Microsoft Edge.

O Chrome tem as seguintes limitações de tamanho das mensagens:
- Limite de mensagem única do host de mensagens nativas: 1 MB
- Limite de mensagem única enviado para o host de mensagens nativas: 4 GB

No Microsoft Edge, embora `AppService` não tenha limite quanto ao tamanho da mensagem (depende da memória), o Microsoft Edge protege-se contra aplicativos nativos inadequados por meio da imposição dos seguintes limites de tamanho de mensagem:
- Limite de mensagem única do aplicativo UWP para extensão: 1 MB
- Limite de mensagem única da extensão para o aplicativo UWP: 100 MB



### Conexões de mensagens nativas

Há dois tipos de conexões para mensagens nativas; persistente e não persistente.
Uma conexão **persistente** é uma conexão que é mantida em execução até que a porta seja destruída. Uma conexão **não persistente** é uma conexão que é aberta por uma mensagem de cada vez e é fechada após a entrega.

#### Persistente

Para o Chrome, é feita uma conexão persistente criando uma porta de mensagens usando [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) . Depois que a porta for feita, o Chrome iniciará um processo de host de mensagens nativo que continuará em execução até a porta que ele destruiu.

Para o Microsoft Edge, quando uma porta de mensagens for criada usando `runtime.connectNative` , o Microsoft Edge iniciará o [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) e o manterá em execução até que a porta seja destruída. O snippet a seguir mostra como uma conexão persistente é estabelecida de dentro de um aplicativo UWP. 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### Não persistente

Quando uma mensagem é enviada usando o [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) Chrome, sem a criação de uma porta de mensagens, o Chrome inicia um novo processo de host de mensagens nativo para cada mensagem. A primeira mensagem gerada pelo processo do host é manipulada como uma resposta à solicitação original e todas as outras mensagens depois de serem ignoradas.

O Microsoft Edge encerrará a conexão após o recebimento de todas as mensagens de resposta. O trecho a seguir mostra uma conexão não persistente que é estabelecida com `AppServiceConnection` isso será encerrada dentro do aplicativo UWP após uma solicitação ser recebida e armazenada como um [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .

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

### Permissão

Para habilitar o uso de mensagens nativas com sua extensão, para Chrome e Microsoft Edge, você precisará declarar a `"nativeMessaging"` permissão em seu `manifest.json` arquivo.


## Serviços de aplicativo
Esta seção detalha o impacto dos serviços do aplicativo no desempenho e na memória de mensagens nativas do Microsoft Edge.

### Desempenho

Os serviços de aplicativo são "patrocinados" pelo aplicativo em primeiro plano que as chama para fins de mensagens nativas é o Microsoft Edge. Isso significa que os serviços de aplicativo podem ser executados enquanto o Microsoft Edge estiver em execução.

Em relação à latência, os serviços de aplicativo usam pipes nomeados que, após a conexão inicial, permitem que dois aplicativos se comuniquem diretamente. Esse método de comunicação produz baixa latência. Dispositivos com CPUs lentas terão uma latência inicial após iniciar o processo que hospeda o serviço de aplicativo (~ 80ms para iniciar a tarefa em segundo plano em alguns dispositivos). Após a inicialização, o desempenho em dispositivos lentos de CPU deve ser bom. 


### Memória
A memória atribuída a um serviço de aplicativo é retirada da cota atribuída ao Microsoft Edge. Isso significa que, se o Microsoft Edge iniciar muitos serviços de aplicativo, há uma possibilidade de que eles possam ficar sem memória. Os limites de memória de tarefa em segundo plano usual são aplicados em serviços de aplicativo. Por exemplo, em um dispositivo de 512MB, uma tarefa em segundo plano do serviço de aplicativo não pode ter mais de 16MB. Esse número aumenta à medida que os dispositivos aumentam.


## Criando uma extensão com mensagens nativas

Para testar mensagens nativas, sua extensão precisa de um nome de família de pacote. O Microsoft Edge usa isso para determinar a identidade do host de mensagens nativa, o que significa que a extensão deve ser empacotada. 


Para criar sua extensão com mensagens nativas no Visual Studio:

1. Crie um projeto UWP no Visual Studio.
2. [Adicione `AppService` ao seu aplicativo UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).
   - Opcionalmente, você pode [Configurar `AppService` para ser hospedado no aplicativo principal](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) , em vez de como uma tarefa em segundo plano neste ponto.
3. Criar e testar seu projeto UWP.
   - Opcionalmente, você pode adicionar um [componente da ponte da área de trabalho](#adding-a-desktop-bridge-component).
4. Crie uma extensão do Microsoft Edge que use o sistema de mensagens nativa para se comunicar com o aplicativo UWP associado. Os arquivos de extensão podem ser adicionados a uma pasta nomeada `Extension` no projeto UWP. Todos os arquivos abaixo desta pasta, incluindo subpastas, precisam ter suas propriedades configuradas de forma que `Build Action=Content` e `Copy to Output Directory=Copy Always` . Verifique `manifest.json` também se está configurado com essas propriedades.
5. Modifique o `package.manifest.xml` arquivo no projeto para incluir metadados de extensão e convertê-los em um aplicativo sem periféricos adicionando `AppListEntry="none"` :

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

6. Use o `AppService` nome configurado para a UWP nas APIs de mensagens nativas.
7. Criar e [implantar](#deploying) o projeto UWP (com o componente opcional da ponte da área de trabalho).
8. [Empacotar](#packaging) sua extensão de mensagens nativa quando estiver pronto para envio à loja

> [!NOTE]
> Consulte a seção [demos](#demos) para obter um exemplo de uma extensão de mensagens nativa completa.


## Adicionar um componente da ponte da área de trabalho 
Se você quiser adicionar um componente da ponte da área de trabalho ao seu pacote, será necessário criar e construir seu projeto Win32 no Visual Studio. Para obter informações sobre como converter seu aplicativo Win32 em UWP, consulte [portando aplicativos para o Windows 10 via desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root). Depois de criar o Visual Studio, você pode adicionar o executável Win32 ao pacote seguindo estas etapas:

1. Adicione o projeto Win32 à mesma solução que o projeto UWP. 

2. Defina o projeto Win32 como um projeto dependente para o projeto UWP:

    ![configurar dependências do projeto](./../media/project-dependencies.PNG)

3. Crie uma `Win32` pasta dentro do projeto UWP. Copie os binários necessários para o `Win32` projeto para essa pasta. Configure as propriedades de todos os binários, de forma que `Build Action=Content` e `Copy to Output Directory=Copy Always` .

    ![pasta com arquivos de aplicativo Win32 e UWP](./../media/desktop-bridge.png)

4. Modifique o arquivo de projeto UWP para copiar todos os binários necessários do `Win32` projeto para essa pasta usando o comando de evento createbuild. Isso garante que os binários atualizados sejam copiados para a pasta toda vez que a solução for recriada.

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. Modifique `package.manifest.xml` adicionando o `<desktop:Extension>` elemento ao `<Extensions>` elemento:

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## Implantando
Depois de configurar seu projeto UWP (e opcionalmente o projeto Win32) conforme descrito acima, você está pronto para implantar a solução usando o Visual Studio.

![construir projeto de inprocess](../media/native-message-uwp-debug.PNG)

Depois que a solução é implantada corretamente, você deve ver sua extensão no Microsoft Edge.

![extensão exibida no Microsoft Edge](../media/secureextension.png)

## Empacotamento

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito. Entre [em contato conosco](https://aka.ms/extension-request) com suas solicitações para fazer parte da Microsoft Store, e consideraremos você para uma atualização futura.


Você pode gerar um pacote da loja para envio para o centro de desenvolvimento do Windows usando a funcionalidade interna do Visual Studio:


![Criando o pacote da loja](../media/create-store-package.PNG)

## Depuração
As instruções para depuração variam de acordo com o componente que você deseja testar:

### Depurando a extensão
Depois que a solução for implantada, a extensão será instalada no Microsoft Edge. Confira o guia de [depuração](./debugging-extensions.md) para obter informações sobre como depurar uma extensão.


### Depurando o aplicativo UWP
O aplicativo UWP será iniciado quando a extensão tentar se conectar a ele usando [APIs de mensagens nativas](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative). Você precisará depurar o aplicativo UWP somente após o início do processo. Isso pode ser configurado por meio da página de propriedades do projeto:

1.  No Visual Studio, clique com o botão direito do mouse no seu projeto de aplicativo UWP
2.  Selecionar Propriedades
3.  Selecionar "não iniciar, mas depurar meu código quando começar"

    ![selecionando a caixa não iniciar](../media/native-message-do-not-launch.png)

No Visual Studio, agora você pode definir pontos de interrupção no código onde deseja depurar e, em seguida, iniciar o depurador pressionando F5. Depois que você interagir com a extensão para se conectar ao aplicativo UWP, o Visual Studio será automaticamente anexado ao processo.


### Depurando a ponte da área de trabalho
Embora existam vários [métodos para depurar uma ponte da área de trabalho](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (aplicativo Win32 convertido), a única aplicável a esses cenários é a opção PLMDebug. Você também pode adicionar o código de depuração à função Startup para executar uma espera por um tempo específico, permitindo que você anexe o Visual Studio ao processo.
