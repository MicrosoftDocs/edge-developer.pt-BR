---
description: O processo de distribuição da extensão por mecanismo diferente das lojas verificadas
title: Método alternativo de distribuição de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: e28a84fd75ad1ac0be2000a22c26371ca73d0293
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015692"
---
# Método alternativo de distribuição de extensão  

Se você for um desenvolvedor que deseja distribuir uma extensão como parte do processo de instalação para outro software ou um administrador de rede que queira distribuir uma extensão em toda a organização, o Microsoft Edge oferece suporte aos seguintes métodos de instalação de extensão:  

*   **Usando o registro do Windows \ (somente Windows \)**  

O Microsoft Edge suporta a instalação de uma extensão hospedada em um `update_URL` .  No Windows, o `update_URL` deve apontar para o catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \) onde a extensão deve ser hospedada.  

> [!NOTE]
> Instalação externa da extensão por meio de um arquivo JSON de preferências para o macOS <!--and Linux--> Ainda não têm suporte.  Este recurso de suporte estará disponível em breve.

## Usar o registro do Windows  

Primeiro, publique a extensão nos Complementos do Microsoft Edge ou empacote um arquivo. crx e certifique-se de que ele seja instalado com êxito.  

As etapas para instalar a extensão pelo registro no Windows são:  

*   Localize ou crie a seguinte chave no registro:  
    *   Windows de 32 bits:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   Windows de 64 bits:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   Crie uma nova chave \ (pasta \) na chave extensões com o mesmo nome que a ID da extensão \ (por exemplo, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).  
*   Na sua chave de extensão, crie uma propriedade, `update_url` e defina-a como o valor: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (isso aponta para o CRX de sua extensão nos Complementos do Microsoft Edge \). Se você quiser instalar uma extensão da loja da Web Chrome, forneça a URL de atualização do Chrome Web Store `https://clients2.google.com/service/update2/crx` .  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   Inicie o navegador e vá para `edge://extensions` ; você deve ver a extensão listada.  

## Atualização e desinstalação  

O Microsoft Edge verifica as entradas de metadados no registro toda vez que o navegador é iniciado e faz as alterações necessárias nas extensões externas instaladas.  

Para atualizar a extensão para uma nova versão, atualize o arquivo e atualize a versão no registro.  

Para desinstalar a extensão \ (por exemplo, se o seu software for desinstalado \), remova o arquivo de preferência \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) ou os metadados do registro.  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original foi encontrada [aqui](https://developer.chrome.com/apps/external_extensions).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
