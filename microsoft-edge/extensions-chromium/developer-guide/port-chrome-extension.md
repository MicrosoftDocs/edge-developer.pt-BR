---
description: Processo de portabilidade da extensão Chrome para o Microsoft Edge.
title: Extensão Chrome de porta para Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195156"
---
# Portar a extensão  

O Microsoft Edge permite que você porte a extensão do Chrome com alterações mínimas.  As APIs de extensão e as chaves de manifesto aceitas pelo Chrome são compatíveis com o código com o Microsoft Edge.  Para obter uma lista de APIs com suporte no Microsoft Edge, navegue até [suporte à API][ExtensionApiSupport].  

Para portar sua extensão Chrome, conclua as etapas a seguir.  

1.  Examine as APIs de extensão do Chrome usadas em suas extensões com a lista de [APIs com suporte][ExtensionApiSupport] do Microsoft Edge Extensions.  
    
    > [!NOTE]
    > Se sua extensão usa APIs que não são suportadas pelo Microsoft Edge, talvez não sejam portadas diretamente.  
    
1.  Se o nome `Chrome` estiver sendo usado no nome ou na descrição da extensão, remarcando a extensão para `Microsoft Edge` .  Esta etapa é necessária para passar no processo de certificação.  
1.  Teste sua extensão para verificar se ela funciona no Microsoft Edge por meio [de Sideload na extensão][ExtensionsGettingStartedExtensionSideloading].  
1.  Se enfrentar algum problema, você pode depurar as extensões no Microsoft Edge usando o DevTools ou [entrar em contato conosco][mailtoExtensionMicrosoft].  
1.  Siga as [diretrizes de publicação][ExtensionsPublishPublishExtension] para publicar sua extensão no repositório Complementos do Microsoft Edge.  
    
    > [!NOTE]
    > Se a extensão trocar mensagens com um aplicativo nativo usando `chrome.runtime.connectNative` API, certifique-se de que você definiu `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` no seu arquivo de manifesto do seu host de mensagens nativa.  Isso permite que o aplicativo identifique a extensão.  
    
## Próximas etapas  

Depois que o pacote de extensão estiver pronto para ser publicado no repositório Complementos do Microsoft Edge, [crie uma conta de desenvolvedor][ExtensionsPublishCreateDevAccount] e [publique a extensão][ExtensionsPublishPublishExtension].  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Suporte à API | Documentos da Microsoft"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Sideload sua extensão | Documentos da Microsoft"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro do desenvolvedor | Documentos da Microsoft"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar sua extensão | Documentos da Microsoft"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamentos de uso único | Desenvolvedor Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
