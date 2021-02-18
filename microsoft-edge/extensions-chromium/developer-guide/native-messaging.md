---
description: Documentação de mensagens nativas
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: d9c2370d6a4f9f7cd25001c1c58ce266423af19a
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343063"
---
# Sistema de mensagens nativo  

As extensões se comunicam com um aplicativo Win32 nativo instalado no dispositivo de um usuário usando as APIs de passagem de mensagens.  O host do aplicativo nativo envia e recebe mensagens com extensões usando entrada padrão e saída padrão.  Extensões que usam mensagens nativas são instaladas no Microsoft Edge de forma semelhante a qualquer outra extensão.  No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.  

Para adquirir a extensão e o host de aplicativo nativo, você tem dois modelos de distribuição.  

*   Empacote sua extensão e o host juntos.  Quando um usuário instala o pacote, a extensão e o host são instalados.  
*   Instale sua extensão usando o [armazenamento de Complementos] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]do Microsoft Edge e sua extensão solicitará que os usuários instalem o host.  

Para criar sua extensão para enviar e receber mensagens com hosts de aplicativo nativos, consulte as etapas a seguir.  

## Etapa 1: Adicionar permissões ao manifesto da extensão  

Adicione a `nativeMessaging` permissão aomanifest.js** no** arquivo da extensão.  O trecho de código a seguir é um exemplo ** demanifest.jsem**.  

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

## Etapa 2: criar seu arquivo de manifesto do host de mensagens nativo  

Os aplicativos nativos devem fornecer um arquivo de manifesto do host de mensagens nativo.  O arquivo de manifesto contém as informações a seguir.  

*   O caminho para o tempo de execução do host de mensagens nativo.  
*   O método de comunicação com a extensão.  
*   Uma lista de extensões permitidas com as quais se comunica.  
    
O navegador lê e valida o manifesto nativo do host de mensagens.  O navegador não instala nem gerencia o arquivo de manifesto do host de mensagens nativo.  

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

O arquivo de manifesto do host deve ser um arquivo JSON válido que contenha as chaves a seguir.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Especifica o nome do host de mensagens nativo.  Os clientes passam essa cadeia de `runtime.connectNative` caracteres para ou `runtime.sendNativeMessage` .  
      
      *   Esse valor deve conter apenas caracteres alfanuméricos minúsculos, sublinhados e pontos.  
      *   Esse valor não deve começar ou terminar com um ponto, e um ponto não deve ser seguido por outro ponto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      Descreve o aplicativo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      Especifica o caminho para o binário nativo do host de mensagens.  
      
      *   Em dispositivos Windows, você pode usar caminhos relativos para o diretório que contém o arquivo de manifesto.  
      *   No macOS e no Linux, o caminho deve ser absoluto.  
      
      O processo de host começa com o diretório atual definido como o diretório que contém o binário do host.  Por exemplo \(Windows\), se esse parâmetro for definido como , o binário será iniciado usando o `C:\Application\nm_host.exe` diretório atual \( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Especifica o tipo da interface usada para se comunicar com o host de mensagens nativo.  Esse valor instrui o Microsoft Edge a usar `stdin` e a se comunicar com o `stdout` host.  
      O único valor aceitável é `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Especifica a lista de extensões que têm acesso ao host de mensagens nativo.  Para permitir que seu aplicativo identifique e se comunique com uma extensão, em seu arquivo de manifesto de host de mensagens nativo, de definida o seguinte valor.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Realizar sideload da extensão para testar as mensagens nativas com o host.  
Para realizar o sideload da extensão durante o desenvolvimento e `microsoft_catalog_extension_id` recuperar, conclua as etapas a seguir.  

1.  Navegue até e a ligue o botão de alternância do modo `edge://extensions` desenvolvedor.  
1.  Escolha **Carregar descompactado**e selecione seu pacote de extensão para sideload.  
1.  Escolha **OK**.  
1.  Navegue `edge://extensions` até a página e verifique se sua extensão está listada.  
1.  Copie a chave de `microsoft_catalog_extension_id` \(ID\) da listagem de extensão na página.  

Quando você estiver pronto para distribuir sua extensão aos usuários, publique sua extensão no armazenamento de Complementos do Microsoft Edge.  A ID de extensão da extensão publicada pode ser diferente da ID usada durante o sideload da extensão.  Se a ID for alterada, `allowed_origins` atualize no arquivo de manifesto do host com a ID da extensão publicada.  

## Etapa 3: copiar o arquivo de manifesto do host de mensagens nativo para o sistema  

A etapa final envolve copiar o arquivo de manifesto do host de mensagens nativo para o computador e garantir que o arquivo de manifesto está configurado corretamente.  Para garantir que o arquivo de manifesto seja colocado no local esperado, conclua as etapas a seguir.  O local varia de acordo com a plataforma.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.  O instalador de aplicativo deve criar uma chave do Registro e definir o valor padrão dessa chave para o caminho completo do arquivo de manifesto.  Os comandos a seguir são exemplos de chaves do Registro.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

Para adicionar uma chave do Registro ao diretório com a chave de manifesto.  

*   Execute o comando no prompt de comando.  
    
    1.  Execute o comando a seguir.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Crie um `.reg` arquivo e execute-o.  
    
    1.  Copie o seguinte comando em um `.reg` arquivo.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Execute o `.reg` arquivo.  
    
O Microsoft Edge consulta a `HKEY_CURRENT_USER` chave raiz seguida por `HKEY_LOCAL_MACHINE` .  Em ambas as chaves, o Registro de 32 bits é pesquisado primeiro e, em seguida, o Registro de 64 bits é pesquisado para identificar hosts nativos de mensagens.  A chave do Registro especifica o local do manifesto do host de mensagens nativo.  Se o Microsoft Edge encontrar a chave do Registro em qualquer um dos locais listados anteriormente, ele não consultará os locais listados neste parágrafo.  Se você executar o arquivo acima como parte de um script em `.reg` lotes, execute-o usando um prompt de comando do administrador.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Para armazenar o arquivo de manifesto, conclua uma das ações a seguir.  

*   Hosts de mensagens nativos de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.  Por exemplo, o arquivo de manifesto deve ser armazenado no seguinte local.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Hosts de mensagens nativos específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no subdiretório no `NativeMessagingHosts` diretório de perfil do usuário.  Por exemplo, o arquivo de manifesto deve ser armazenado no seguinte local.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    O  `{Channel_Name}` in deve ser um dos valores a `Microsoft Edge {Channel_Name}` seguir.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Ao usar o canal Estável, `{Channel_Name}` não é necessário.  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Para armazenar o arquivo de manifesto, conclua uma das ações a seguir.  

*   Hosts de mensagens nativos de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.  O arquivo de manifesto deve ser armazenado no seguinte local.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Hosts de mensagens nativos específicos do usuário, que estão disponíveis apenas para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil do usuário.  O arquivo de manifesto deve ser armazenado no seguinte local.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Forneça permissões de leitura no arquivo de manifesto e execute permissões no tempo de execução do host.  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui.](https://developer.chrome.com/extensions/nativeMessaging)  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
