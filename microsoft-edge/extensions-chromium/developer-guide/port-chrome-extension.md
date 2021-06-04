---
description: Processo de portação de extensão do Chrome para Microsoft Edge
title: Extensão porta chrome para Microsoft Edge
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
# Porta sua extensão  

Microsoft Edge permite a portabilidade da extensão do Chrome com as alterações mínimas.  As APIs de extensão e as chaves de manifesto suportadas pelo Chrome são compatíveis com código com Microsoft Edge.  Para uma lista de APIs com suporte Microsoft Edge, navegue até [SUPORTE À API][ExtensionApiSupport].  

Para portabilidade da extensão do Chrome, conclua as etapas a seguir.  

1.  Revise as APIs de extensão do Chrome usadas em suas extensões com Microsoft Edge [de APIs][ExtensionApiSupport] compatíveis.  
    
    > [!NOTE]
    > Se sua extensão usa APIs que não são suportadas por Microsoft Edge, ela pode não ser portada diretamente.  
    
1.  No arquivo de manifesto, de definir o `update_URL` campo como `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  O valor aponta para o arquivo de sua extensão no Microsoft Edge de complementos e permite Microsoft Edge verificar se há `.crx` atualizações de extensão.  
1.  Se `Chrome` for usado no nome ou na descrição da extensão, renomee sua extensão usando `Microsoft Edge` .  Para passar no processo de certificação, as alterações são necessárias.  
1.  Teste sua extensão para verificar se ela funciona Microsoft Edge [sideload da extensão][ExtensionsGettingStartedExtensionSideloading].  
1.  Se você enfrentar algum problema, poderá depurar suas extensões no Microsoft Edge usando o DevTools ou [entre em contato conosco][mailtoExtensionMicrosoft].  
1.  Siga as [diretrizes de publicação][ExtensionsPublishPublishExtension] para publicar sua extensão no Microsoft Edge de complementos.  
    
    > [!NOTE]
    > Se sua extensão trocar mensagens com um aplicativo nativo usando , certifique-se de definir como no arquivo de manifesto do host de `chrome.runtime.connectNative` `allowed_origins` mensagens `extension://[Microsoft-Catalog-extensionID]` nativo.  A configuração permite que o aplicativo identifique sua extensão.  
    
##  <a name="next-steps"></a>Próximas etapas  

Depois que o pacote de extensão estiver pronto para ser [][ExtensionsPublishCreateDevAccount] publicado no Microsoft Edge de complementos, crie uma conta de desenvolvedor e [publique sua extensão.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Suporte à API | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Fazer sideload da extensão | Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro de desenvolvedor | Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar sua extensão | Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamentos únicos | Desenvolvedor do Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
