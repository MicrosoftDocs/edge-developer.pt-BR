---
description: Processo de portagem da extensão do Chrome para o Microsoft Edge
title: Fazer a portabilidade da extensão do Chrome para o Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343133"
---
# Fazer a portabilidade de sua extensão  

O Microsoft Edge permite que você porte sua extensão do Chrome com alterações mínimas.  As APIs de extensão e as chaves de manifesto compatíveis com o Chrome são compatíveis com código com o Microsoft Edge.  Para uma lista de APIs com suporte no Microsoft Edge, navegue até o suporte [à API.][ExtensionApiSupport]  

Para por a portabilidade da extensão do Chrome, conclua as etapas a seguir.  

1.  Revise as APIs de extensão do Chrome usadas em suas extensões com a lista de APIs compatíveis com as [extensões do][ExtensionApiSupport] Microsoft Edge.  
    
    > [!NOTE]
    > Se sua extensão usa APIs que não são suportadas pelo Microsoft Edge, ela pode não fazer a portabilidade diretamente.  
    
1.  No arquivo de manifesto, de definir `update_URL` o campo como `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  O valor aponta para o arquivo de sua extensão no armazenamento de Complementos do Microsoft Edge e permite que o Microsoft Edge verifique `.crx` se há atualizações de extensão.  
1.  Se for usado no nome ou na descrição da `Chrome` extensão, renomee sua extensão usando `Microsoft Edge` .  Para passar no processo de certificação, as alterações são necessárias.  
1.  Teste sua extensão para verificar se ela funciona no Microsoft Edge [ao fazer sideload da extensão.][ExtensionsGettingStartedExtensionSideloading]  
1.  Se você enfrentar problemas, poderá depurar suas extensões no Microsoft Edge usando o DevTools ou [entre em contato conosco.][mailtoExtensionMicrosoft]  
1.  Siga as [diretrizes de publicação][ExtensionsPublishPublishExtension] para publicar sua extensão na loja de Complementos do Microsoft Edge.  
    
    > [!NOTE]
    > Se sua extensão trocar mensagens com um aplicativo nativo usando, certifique-se de definir como no arquivo de manifesto do host de `chrome.runtime.connectNative` `allowed_origins` mensagens `extension://[Microsoft-Catalog-extensionID]` nativo.  A configuração permite que o aplicativo identifique sua extensão.  
    
## Próximas etapas  

Depois que o pacote de extensão estiver pronto para ser publicado na loja de Complementos do Microsoft [Edge,][ExtensionsPublishCreateDevAccount] crie uma conta de desenvolvedor e [publique sua extensão.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Suporte à API | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Fazer o sideload da extensão | Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro de desenvolvedor | Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publique sua extensão | Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamento único | Desenvolvedor do Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
