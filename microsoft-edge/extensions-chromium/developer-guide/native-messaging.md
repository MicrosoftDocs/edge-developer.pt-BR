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
# Sistema de mensagens nativo  

As extensões se comunicam com um aplicativo Win32 nativo instalado em um dispositivo de usuário usando APIs de transmissão de mensagens.  O host do aplicativo nativo envia e recebe mensagens com extensões usando a entrada padrão e a saída padrão.  As extensões que usam o recurso de mensagens nativas são instaladas no Microsoft Edge semelhantes a qualquer outra extensão.  No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.  

Para adquirir a extensão e o host de aplicativo nativo, você tem dois modelos de distribuição.  

*   Empacote a extensão e o host juntos.  Quando um usuário instala o pacote, a extensão e o host são instalados.
*   Instale a extensão usando o [repositório Complementos do Microsoft Edge][EdgeAddons]e sua extensão solicitará que os usuários instalem o host.  

Para criar a extensão para enviar e receber mensagens com hosts de aplicativos nativos, consulte as etapas a seguir.  

## Etapa 1-adicionar permissões ao manifesto de extensão  

Adicione a `nativeMessaging` permissão ao **manifest.jsem** arquivo da extensão.  O trecho de código a seguir é um exemplo de **manifest.js**.  

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

## Etapa 2-criar seu arquivo de manifesto do host de mensagens nativo  

Aplicativos nativos devem fornecer um arquivo de manifesto de host de mensagens nativo.  O arquivo de manifesto contém o caminho para o tempo de execução do host de mensagens nativa, o método de comunicação com a extensão e uma lista de extensões permitidas às quais ela se comunica.  O navegador lê e valida o manifesto do host de mensagens nativa.  O navegador não instala ou gerencia o arquivo de manifesto de host de mensagens nativa.  

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

O arquivo de manifesto host deve ser um arquivo JSON válido que contém as teclas a seguir.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Especifica o nome do host de mensagens nativa.  Os clientes passam esta cadeia de caracteres para `runtime.connectNative` ou `runtime.sendNativeMessage` .  
      
      *   Esse valor só deve conter caracteres alfanuméricos minúsculos, sublinhados e pontos.  
      *   Esse valor não deve começar ou terminar com um ponto e um ponto não deve ser seguido por outro ponto.  
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
      Especifica o caminho para o binário do host de mensagens nativa.  
      
      *   Em dispositivos Windows, você pode usar caminhos relativos para o diretório que contém o arquivo de manifesto.  
      *   No macOS e no Linux, o caminho deve ser absoluto.  
      
      O processo de host começa com o diretório atual definido para o diretório que contém o binário do host.  Por exemplo, \ (Windows \), se esse parâmetro for definido como `C:\Application\nm_host.exe` , o binário será iniciado usando o diretório atual \ ( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Especifica o tipo de interface usado para se comunicar com o host de mensagens nativa.  Esse valor instrui o Microsoft Edge a usar `stdin` e `stdout` a se comunicar com o host.  
      O único valor aceitável é `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Especifica a lista de extensões que têm acesso ao host de mensagens nativa.  Para permitir que o aplicativo identifique e se comunique com uma extensão, no seu arquivo de manifesto do host de mensagens nativa defina o valor a seguir.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Sideload sua extensão para testar o sistema de mensagens nativa com o host.  
Para Sideload a extensão durante o desenvolvimento e a recuperação `microsoft_catalog_extension_id` , conclua as etapas a seguir.  

1.  Navegue até `edge://extensions` e, em seguida, ative o botão de alternância do modo de desenvolvedor.  
1.  Escolha **carregar desempacotados**e, em seguida, selecione o pacote de extensão para Sideload.  
1.  Escolha **OK**.
1.  Navegue até a `edge://extensions` página e verifique se a extensão está listada.  
1.  Copie a chave de `microsoft_catalog_extension_id` \ (ID \) da listagem de extensão na página.

Quando estiver pronto para distribuir a extensão para os usuários, publique a extensão no repositório de Complementos do Microsoft Edge.  A ID da extensão da extensão publicada pode ser diferente da ID usada durante o Sideload da extensão.  Se a ID foi alterada, atualize `allowed_origins` o arquivo de manifesto host com a ID da extensão publicada.  

## Etapa 3-copiar o arquivo de manifesto do sistema de mensagens nativo para seu sistema  

A etapa final envolve copiar o arquivo de manifesto do sistema de mensagens nativo para seu computador e garantir que ele esteja configurado corretamente.  Para garantir que o arquivo de manifesto seja colocado no local esperado, conclua as etapas a seguir.  O local varia de acordo com a plataforma.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.  O instalador do aplicativo deve criar uma chave do registro e definir o valor padrão dessa chave para o caminho completo do arquivo de manifesto.  Os comandos a seguir são exemplos de chaves do registro.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

Para adicionar uma chave do registro ao diretório com a chave de manifesto.  

*   Comando executar no prompt de comando.    
    
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
        
    1.  Executar o `.reg` arquivo.  
    
O Microsoft Edge consulta o registro de 32 bits primeiro e, em seguida, o registro de 64 bits para identificar hosts de mensagens nativas.  Se você executar o `.reg` arquivo acima como parte de um script em lotes, certifique-se de executá-lo usando um prompt de comando de administrador.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Para armazenar o arquivo de manifesto, execute uma das seguintes ações.  

*   Hosts de mensagens nativas de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.  Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir. 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Hosts de mensagens nativas específicas do usuário, que estão disponíveis somente para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil do usuário.  Por exemplo, o arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    O  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` deve ser um dos seguintes valores.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Não é necessário usar o canal estável `{Channel_Name}` .  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Para armazenar o arquivo de manifesto, execute uma das seguintes ações.  

*   Hosts de mensagens nativas de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo.  O arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Hosts de mensagens nativas específicas do usuário, que estão disponíveis somente para o usuário atual, estão localizados no `NativeMessagingHosts` subdiretório no diretório de perfil do usuário.  O arquivo de manifesto deve ser armazenado no local a seguir.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Certifique-se de fornecer permissões de leitura no arquivo de manifesto e executar permissões no tempo de execução do host.  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
