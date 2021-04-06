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
# <a name="native-messaging"></a>Sistema de mensagens nativo  

As extensões se comunicam com um aplicativo Win32 nativo instalado no dispositivo de um usuário usando APIs de passagem de mensagens.  O host de aplicativo nativo envia e recebe mensagens com extensões usando entrada padrão e saída padrão.  Extensões usando mensagens nativas são instaladas no Microsoft Edge semelhantes a qualquer outra extensão.  No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.  

Para adquirir a extensão e o host de aplicativo nativo, você tem dois modelos de distribuição.  

*   Empacote sua extensão e o host juntos.  Quando um usuário instala o pacote, a extensão e o host são instalados.  
*   Instale sua extensão usando o Armazenamento de [Complementos do Microsoft Edge][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]e sua extensão solicita que os usuários instalem o host.  

Para criar sua extensão para enviar e receber mensagens com hosts de aplicativos nativos, conclua as etapas a seguir.  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a>Etapa 1 - Adicionar permissões ao manifesto da extensão  

Adicione a `nativeMessaging` permissão ao arquivomanifest.js** no** arquivo da extensão.  O trecho de código a seguir é um exemplo de **manifest.jsem**.  

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

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a>Etapa 2 : Criar o arquivo de manifesto do host de mensagens nativo  

Os aplicativos nativos devem fornecer um arquivo de manifesto de host de mensagens nativo.  O arquivo de manifesto contém as seguintes informações.  

*   O caminho para o tempo de execução do host de mensagens nativo.  
*   O método de comunicação com a extensão.  
*   Uma lista de extensões permitidas às quais se comunica.  
    
O navegador lê e valida o manifesto nativo do host de mensagens.  O navegador não instala ou gerencia o arquivo de manifesto do host de mensagens nativo.  

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

O arquivo de manifesto do host deve ser um arquivo JSON válido que contém as seguintes chaves.  

:::row:::
   :::column span="1":::
      **Chave**  
   :::column-end:::
   :::column span="3":::
      **Detalhes**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica o nome do host de mensagens nativo.  Os clientes passam a cadeia de `runtime.connectNative` caracteres para ou `runtime.sendNativeMessage` .  
      
      *   O valor só deve conter caracteres alfanuméricos minúsculos, sublinhados e pontos.  
      *   O valor não deve iniciar ou terminar com um ponto, e um ponto não deve ser seguido por outro ponto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Descreve o aplicativo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica o caminho para o binário de host de mensagens nativo.  
      
      *   Em dispositivos Windows, você pode usar caminhos relativos ao diretório que contém o arquivo de manifesto.  
      *   No macOS e no Linux, o caminho deve ser absoluto.  
          
      O processo de host começa com o diretório atual definido para o diretório que contém o binário do host.  Por exemplo \(Windows\), se o parâmetro for definido como , o binário será iniciado usando o `C:\App\nm_host.exe` diretório atual \( `C:\App\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica o tipo da interface usada para se comunicar com o host de mensagens nativo.  O valor instrui o Microsoft Edge a usar `stdin` e se comunicar com o `stdout` host.  
      O único valor aceitável é `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica a lista de extensões que têm acesso ao host de mensagens nativo.  Para ativar seu aplicativo para identificar e se comunicar com uma extensão, em seu arquivo de manifesto de host de mensagens nativo de definir o seguinte valor.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Fazer sideload da extensão para testar mensagens nativas com o host.  
Para fazer sideload da extensão durante o desenvolvimento e recuperar `microsoft_catalog_extension_id` , conclua as seguintes ações.  

1.  Navegue `edge://extensions` até e, em seguida, a opção Botão de alternância do modo de desenvolvedor.  
1.  Escolha **Carregar descompactado**e, em seguida, escolha o pacote de extensão para sideload.  
1.  Escolha **OK**.  
1.  Navegue `edge://extensions` até a página e verifique se sua extensão está listada.  
1.  Copie a chave `microsoft_catalog_extension_id` de \(ID\) da listagem de extensão na página.  
    
Quando estiver pronto para distribuir sua extensão aos usuários, publique sua extensão no armazenamento de Complementos do Microsoft Edge.  A ID de extensão da extensão publicada pode ser diferente da ID usada durante o sideload da extensão.  Se a ID for alterada, atualize no `allowed_origins` arquivo de manifesto do host com a ID da extensão publicada.  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a>Etapa 3 : Copiar o arquivo de manifesto do host de mensagens nativo para o sistema  

A etapa final envolve copiar o arquivo de manifesto do host de mensagens nativo para o computador e garantir que o arquivo de manifesto está configurado corretamente.  Para garantir que seu arquivo de manifesto seja colocado no local esperado, conclua as seguintes ações.  O local varia de acordo com a plataforma.

> [!NOTE]
> Verifique se você fornece permissões de leitura no arquivo de manifesto e execute permissões no tempo de execução do host.  

### [<a name="windows"></a>Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.  O instalador de aplicativo deve criar uma chave do Registro e definir o valor padrão da chave para o caminho completo do arquivo de manifesto.  Os locais a seguir são exemplos de chaves do Registro.  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

Para adicionar uma chave do Registro ao diretório com a chave de manifesto, conclua uma das seguintes ações.  

*   Execute o comando no prompt de comando.  
    
    1.  Execute o seguinte comando.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   Crie um `.reg` arquivo e execute-o.  
    
    1.  Copie o seguinte comando em um `.reg` arquivo.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Execute o `.reg` arquivo.  
        
O Microsoft Edge consulta a `HKEY_CURRENT_USER` chave raiz seguida por `HKEY_LOCAL_MACHINE` .  Em ambas as chaves, o Registro de 32 bits é pesquisado primeiro e, em seguida, o Registro de 64 bits é pesquisado para identificar hosts de mensagens nativos.  A chave do Registro especifica o local do manifesto do host de mensagens nativo.  Se as entradas do Registro do Microsoft Edge não têm o local do manifesto do host, os locais do Registro do Chromium e do Chrome serão usados como opções de fallback.  Se o Microsoft Edge encontrar a chave do Registro em qualquer um dos locais listados anteriormente, ele não consultará os locais listados no trecho de código a seguir.  Se você executar o arquivo criado como parte de um script em lotes, verifique se o executará usando um prompt `.reg` de comando do administrador.

A lista a seguir é a ordem de pesquisa para os locais do Registro.  

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
> Se você tiver extensões nos Complementos do Microsoft Edge e na Webstore do Chrome, você deverá adicionar as IDs de extensão correspondentes a ambos os repositórios no arquivo de manifesto do host porque somente o manifesto de host correspondente ao primeiro local do Registro encontrado é `allowed_origins` lido.  

### [<a name="macos"></a>macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Para armazenar o arquivo de manifesto, conclua uma das seguintes ações.  

*   Hosts de mensagens nativos em todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.  Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   Hosts de mensagens nativas específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil de usuário.  Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    O  `{Channel_Name}` in deve ser um dos seguintes `Microsoft Edge {Channel_Name}` valores.  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    Ao usar o canal Estável, ` {Channel_Name}` não é necessário.  
    
### [<a name="linux"></a>Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Para armazenar o arquivo de manifesto, conclua uma das seguintes ações.  

*   Hosts de mensagens nativos em todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.  O arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Hosts de mensagens nativas específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil de usuário.  O arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
