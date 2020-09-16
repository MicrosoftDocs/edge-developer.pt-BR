---
description: Diferença entre mensagens nativas da documentação do Chrome
title: Sistema de mensagens nativo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 811468e5f92319107c60606bc9268a9f7a25e560
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015671"
---
# Sistema de mensagens nativo  

O Microsoft Edge agora permite a extensão instalada do catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \) para trocar mensagens com um aplicativo nativo usando APIs de transmissão de mensagens.  Para habilitar o recurso, você precisa se certificar dos seguintes itens ao implementar o host de mensagens nativa do seu aplicativo nativo.  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  **Host de mensagens nativa**:  
    
    Para registrar um host de mensagens nativa, o aplicativo deve instalar um arquivo de manifesto que define a configuração do host de mensagens nativa.  Veja a seguir um exemplo do arquivo de manifesto:  
    
    ```xml
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
    
O arquivo de manifesto do host de mensagens nativa deve ser um JSON válido e contém os seguintes campos:  

| Nome | Descrição |  
|:--- |:--- |  
| `name` | Nome do host de mensagens nativa. Os clientes passam esta cadeia de caracteres para `runtime.connectNative` ou `runtime.sendNativeMessage` .  Esse nome deve conter apenas caracteres alfanuméricos minúsculos, sublinhados e pontos.  O nome não deve começar ou terminar com um ponto e um ponto não deve ser seguido por outro ponto. |  
| `description` | Breve descrição do aplicativo. |  
| `path` | Caminho para o binário do host de mensagens nativa.  No Windows, o caminho pode ser relativo ao diretório no qual o arquivo de manifesto está localizado.  No macOS, o caminho deve ser absoluto.  O processo de host é iniciado com o diretório atual definido como o diretório que contém o binário do host. Por exemplo, se esse parâmetro for definido como `C:\Application\nm_host.exe` , o binário será iniciado usando o diretório atual `C:\Application\` . |  
| `type` | Tipo de interface usado para se comunicar com o host de mensagens nativa.  Atualmente, há apenas um valor possível para esse parâmetro: `stdio` .  Esse valor indica que o Chrome deve usar `stdin` e `stdout` para se comunicar com o host. |  
| `allowed_origins` |  lista de extensões que devem acessar o host de mensagens nativa.  Para habilitar o aplicativo nativo para identificar e se comunicar com o Microsoft Edge addons Extension, defina- `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` o no seu arquivo de manifesto do host de mensagens nativa. |  

1.  **Local do host de mensagens nativa**  
    
    O local do arquivo de manifesto depende da plataforma.  
    
    No Windows, o arquivo de manifesto pode estar localizado em qualquer lugar no sistema de arquivos.  O instalador do aplicativo deve criar a chave do registro  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    ou  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`,  
    
    e defina o valor padrão dessa chave para o caminho completo para o arquivo de manifesto.  Por exemplo, usando o seguinte comando:  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    ou use o seguinte arquivo. reg:  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    Quando o Microsoft Edge procura hosts de mensagens nativos, o registro de 32 bits é consultado primeiro e, em seguida, o registro de 64 bits.  

No macOS, os hosts de mensagens nativas de todo o sistema são pesquisados em um local fixo, enquanto os hosts de mensagens nativas em nível de usuário são pesquisados em um subdiretório no diretório de perfil do usuário chamado `NativeMessagingHosts` .  

Microsoft Edge no macOS \ (todo o sistema \):  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

Microsoft Edge no macOS \ (caminho padrão específico do usuário \):  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` pode ser Canárias, dev ou beta. Para canal estável, só `Microsoft Edge` deve ser usado, `<ChannelName`>' não é necessário.

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
