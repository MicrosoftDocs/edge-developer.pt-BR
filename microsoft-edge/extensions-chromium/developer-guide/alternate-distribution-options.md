---
description: Saiba como distribuir extensões usando métodos alternativos que não usam armazenamentos verificados
title: Método alternativo para distribuir extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 3b2c72e13488632e2fadea2a7e8eb95888f67170
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343146"
---
# Métodos alternativos de distribuição de extensão  

Geralmente, as extensões são distribuídas por meio do Microsoft Edge de complementos. Há alguns cenários em que os desenvolvedores podem precisar distribuir extensões usando métodos alternativos. Por exemplo:

1.  A extensão está associada a outro software e deve ser instalada junto com o restante do software empacotado.   
1.  Os administradores de rede querem distribuir uma extensão em toda a organização.   

Extensões que não são carregadas do armazenamento de Complementos de Borda são conhecidas como extensões instaladas externamente. A lista a seguir fornece métodos alternativos de distribuição de extensões instaladas externamente. 

*   Use o Windows (somente Windows).  
*   Use um arquivo JSON de preferências (macOS e Linux).  
    
## Antes de começar  

Certifique-se de publicar sua extensão no Microsoft Edge de complementos ou empacote um arquivo e certifique-se de que ele seja instalado com êxito `.crx` no computador.  Se você instalar o `.crx` arquivo usando o , certifique-se de poder navegar até sua extensão nessa `update_URL` URL.  

Além disso, verifique se você tem as seguintes informações.    

1.  O caminho do arquivo `.crx` ou a `update_URL` extensão.
1.  A versão da extensão.  As informações de versão estão disponíveis no arquivo de manifesto ou Microsoft Edge depois de `edge://extensions` carregar a extensão empacotada.   
1.  A ID da extensão.  As informações de ID estão disponíveis Microsoft Edge depois `edge://extensions` de carregar a extensão empacotada.  

> [!NOTE] 
> Os exemplos a seguir `1.0` usam como a versão e para a `aaaaaaaaaabbbbbbbbbbcccccccccc` ID.  

## Use o Windows (somente Windows)  

Para distribuir sua extensão usando o Windows registro, execute as etapas a seguir.

1.  Encontre ou crie a seguinte chave no Registro:  
    *   32 bits Windows: `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .  
    *   64 bits Windows: `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .  
1.  Crie uma nova chave ou pasta em **Extensões** com o mesmo nome que a ID da extensão. Por exemplo, crie a chave com o nome `aaaaaaaaaabbbbbbbbbbcccccccccc` .  
1.  Na chave **Extensões,** crie a `update_url` propriedade e de definir o valor como `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  A `update_url` propriedade aponta para o arquivo de sua extensão no Microsoft Edge de `.crx` complementos.  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > Se você quiser instalar uma extensão do Chrome Web Store, de definir o valor `update_url` de `https://clients2.google.com/service/update2/crx` como .  
  
1.  Verifique se sua extensão está listada no Microsoft Edge navegando para `edge://extensions` .  

## Usar um arquivo JSON de preferências (macOS e Linux)  

Para distribuir sua extensão usando um arquivo JSON de preferências, execute as etapas a seguir.

1.  Ao usar o Linux, verifique se o arquivo de extensão está disponível no computador em que a extensão `.crx` será instalada. Copie o arquivo de extensão para um diretório local ou use um compartilhamento de rede que `.crx` seja acessível do computador. 
1.  Crie um arquivo JSON em que o nome do arquivo corresponde à ID da extensão. Por exemplo, crie um arquivo JSON com o nome de arquivo `aaaaaaaaaabbbbbbbbbbcccccccccc.json` .  
1.  Dependendo do sistema operacional, salve o arquivo JSON em uma das seguintes pastas.   
    *   **macOS**  
        *   Específico do usuário: `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   Todos os usuários: `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        Para impedir que usuários não autorizados instalem extensões para todos os usuários, verifique se o arquivo de extensão é somente leitura. Além disso, certifique-se de que as seguintes condições sejam atendidas:
        
        *   Cada diretório no caminho pertence à raiz do usuário.  
        *   Cada diretório no caminho é atribuído ao `admin` grupo `wheel` ou.  
        *   Todos os diretórios no caminho não podem ser escritos no mundo.  
        *   O caminho também deve estar livre de links simbólicos.  
        
    *   **Linux**  
        *   Específico do usuário: `~/.config/microsoft-edge/External Extensions/`  
        *   Todos os usuários: `/usr/share/microsoft-edge/extensions/`  
1.  Dependendo do cenário, copie o código apropriado que segue para o arquivo JSON. 
    *   Aplica-se somente ao Linux. Se você instalar de um arquivo, especifique o local e a versão usando `external_crx` e `external_version` .  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   Aplica-se ao macOS e ao Linux. Se você instalar de um `update_URL` , especifique a URL de atualização usando `external_update_url` . 
        
        Copie o código a seguir para o arquivo JSON ao instalar apenas arquivos locais `.crx` no Linux.  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  Copie o código a seguir para o arquivo JSON ao instalar a partir do Microsoft Edge de complementos em macOS e Linux.
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  Para instalar extensões para localidades específicas, liste as localidades com suporte usando `supported_locale` .  Você também pode especificar localidades pai para instalar sua extensão para todas as localidades de idioma que usam esse pai. Por exemplo, ao usar a localidade pai, sua extensão é instalada para todas as localidades em inglês, como `en` , e assim por `en-US` `en-GB` diante.  Quando os usuários alteram sua localidade em seu navegador, as extensões instaladas externamente são desinstaladas.  Para instalar sua extensão para qualquer localidade, não use `supported_locales` .  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  Verifique se sua extensão está instalada no Microsoft Edge navegando para `edge://extensions` .  

## Atualizar e desinstalar extensões instaladas externamente

Microsoft Edge verifica as entradas de metadados no Registro sempre que o navegador é iniciado e faz alterações nas extensões instaladas externamente.  

Para atualizar sua extensão para uma nova versão, atualize a versão no arquivo de manifesto e atualize a versão no Registro.  

Talvez seja necessário desinstalar extensões instaladas externamente, que foram instaladas como parte de um pacote de software que foi instalado anteriormente no computador.  Para desinstalar sua extensão, remova seu arquivo JSON de preferências ou remova a chave do Registro.   

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  A página original é encontrada [aqui](https://developer.chrome.com/apps/external_extensions).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
