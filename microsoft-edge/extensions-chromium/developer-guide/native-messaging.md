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
# Sistema de mensagens nativo  

As extensões podem se comunicar com um aplicativo Win32 nativo instalado em um dispositivo de usuário usando APIs de transmissão de mensagens. O host do aplicativo nativo pode enviar e receber mensagens com extensões usando a entrada padrão e a saída padrão. As extensões que usam o recurso de mensagens nativas são instaladas no Microsoft Edge semelhantes a qualquer outra extensão. No entanto, os aplicativos nativos não são instalados ou gerenciados pelo Microsoft Edge.

Para adquirir a extensão e o host do aplicativo nativo, você pode:

1. Empacote a extensão e o host juntos. Quando os usuários instalam o pacote, a extensão e o host são instalados.
1. Instale a extensão do [repositório de Complementos do Microsoft Edge][EdgeAddons]e faça com que sua extensão solicite que os usuários instalem o host. 

Confira as etapas abaixo para configurar a extensão para enviar e receber mensagens com hosts de aplicativos nativos.

### Etapa 1: adicionar permissões ao manifesto de extensão

Adicione a permissão nativeMessaging para omanifest.jsdo ramal ** no** arquivo. Veja a seguir um exemplo de manifest.jsem:

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

### Etapa 2: criar o arquivo de manifesto do seu host de mensagens nativo
    
Aplicativos nativos devem fornecer um arquivo de manifesto de host de mensagens nativo. Esse arquivo de manifesto contém o caminho para o executável do host de mensagens nativa, o método de comunicação com a extensão e uma lista de extensões permitidas com as quais ele pode se comunicar. Os navegadores lêem e validam o manifesto do host de mensagens nativa, mas ele nunca é instalado ou gerenciado pelo navegador. O arquivo de manifesto do host deve ser um arquivo JSON válido contendo os campos a seguir.

    
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




| Nome | Descrição |  
|:--- |:--- |  
| `name` | Nome do host de mensagens nativa. Os clientes passam esta cadeia de caracteres para `runtime.connectNative` ou `runtime.sendNativeMessage` .  Esse nome deve conter apenas caracteres alfanuméricos minúsculos, sublinhados e pontos.  O nome não deve começar ou terminar com um ponto e um ponto não deve ser seguido por outro ponto. |  
| `description` | Breve descrição do aplicativo. |  
| `path` | Caminho para o binário do host de mensagens nativa. Em dispositivos Windows, você pode usar caminhos relativos para o diretório que contém o arquivo de manifesto. No macOS e no Linux, o caminho deve ser absoluto. O processo de host é iniciado com o diretório atual definido como o diretório que contém o binário do host. Por exemplo, se esse parâmetro for definido como `C:\Application\nm_host.exe` , o binário será iniciado usando o diretório atual `C:\Application\` . |  
| `type` | Tipo de interface usado para se comunicar com o host de mensagens nativa.  No momento, há apenas um valor possível para esse parâmetro: `stdio` .  Esse valor indica que o Microsoft Edge deve usar `stdin` e `stdout` para se comunicar com o host. |  
| `allowed_origins` |  Lista de extensões que podem ter acesso ao host de mensagens nativa.  Para permitir que o aplicativo identifique e se comunique com uma extensão, defina- `allowed_origins` `chrome-extension://[Microsoft-Catalog-extensionID]` o como em seu arquivo de manifesto do host de mensagens nativa. |  


Durante o desenvolvimento, você pode Sideload sua extensão para testar o recurso de mensagens nativas pelo host:
1. Navegue até `edge://extensions` e ative o botão de alternância do modo de desenvolvedor. 
1. Escolha carregar desempacotados e, em seguida, selecione o pacote de extensão para Sideload.  
1. Escolha OK.
1. Verifique se a `edge://extensions` página agora lista a extensão. 
1. Copie a chave de ID da listagem de extensão na página.

Quando estiver pronto para distribuir a extensão para os usuários, publique a extensão no repositório de Complementos do Microsoft Edge. A ID da extensão da extensão publicada pode ser diferente da ID usada durante a Sideload da extensão. Se a ID foi alterada, atualize `allowed_origins` o arquivo de manifesto host com a ID da extensão publicada. 



### Etapa 3: copiar o arquivo de manifesto do sistema de mensagens nativo para o seu sistema

A etapa final envolve copiar o arquivo de manifesto do sistema de mensagens nativo para seu computador e garantir que ele esteja configurado corretamente. Siga as etapas abaixo para garantir que o arquivo de host de mensagens nativa seja colocado no local esperado porque ele varia de acordo com a plataforma.
    
**Windows**. O arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos. O instalador do aplicativo deve criar uma chave do registro e definir o valor padrão dessa chave para o caminho completo do arquivo de manifesto. Os comandos a seguir são exemplos de chaves do registro.
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    ou  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`,  
    
Execute o seguinte comando em um prompt de comando para adicionar uma chave do registro à pasta com o arquivo de manifesto.
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
Você também pode copiar o comando a seguir para um arquivo. reg e executá-lo para adicionar a chave do registro. 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  O Microsoft Edge consulta o registro de 32 bits primeiro e, em seguida, o registro de 64 bits para identificar hosts de mensagens nativas. Se você executar o arquivo. reg acima como parte de um script em lotes, certifique-se de executá-lo usando um prompt de comando de administrador.


**MacOS**. O arquivo de manifesto deve ser armazenado da seguinte maneira:

1. Hosts de mensagens nativas de todo o sistema, que estão disponíveis para todos os usuários, são armazenados em um local fixo. Por exemplo, o arquivo de manifesto deve ser armazenado em `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. Hosts de mensagens nativas específicas do usuário, que estão disponíveis somente para o usuário atual, estão localizados no subdiretório NativeMessagingHosts no diretório de perfil do usuário. Por exemplo, o arquivo de manifesto deve ser armazenado em  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    onde `ChannelName` pode haver Canárias, dev ou beta. Não é necessário usar o canal estável `ChannelName` .


**Linux** O arquivo de manifesto deve ser armazenado da seguinte maneira:

1. Hosts de mensagens nativas de todo o sistema:  `~/.config/microsoft-edge/NativeMessagingHosts`

1. Hosts de mensagens nativas específicas do usuário:  `/etc/opt/edge/native-messaging-hosts`


> [!NOTE]
> Certifique-se de fornecer permissões de leitura no arquivo de manifesto e permissões de execução no executável do host.


> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos do Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
