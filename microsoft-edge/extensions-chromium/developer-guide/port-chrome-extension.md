---
description: Processo de portabilidade da extensão Chrome para o Microsoft Edge.
title: Extensão do Chrome de porta para a Microsoft (Chromium) Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 794e8806a95ce0a70069c65c306c30131b01e24d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561312"
---
# Extensão Chrome de porta para a Microsoft \ (Chromium \) Edge  

O processo de portabilidade de uma extensão do Chrome para o Microsoft Edge é muito simples.  Extensões escritas para Chromium, na maioria dos casos, são executadas no Microsoft Edge com alterações mínimas.  As APIs de extensão e as chaves de manifesto aceitas pelo Chrome são compatíveis com o código com o Microsoft Edge.  No entanto, o Microsoft Edge não é compatível com as seguintes APIs de extensão:  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> O usuário deve estar conectado ao Microsoft Edge usando uma conta do MSA ou AAD para usar a `chrome.identity.getProfileUserInfo` API.  Se o usuário estiver conectado ao Microsoft Edge usando o **anúncio local**, a API retornará `null` para os valores de email e ID.  

> [!IMPORTANT]
> **Pagamentos**: o Microsoft Edge não oferece suporte direto a uma extensão que use [pagamentos da loja da Web Chrome][ChromeDeveloperWebStorePayments] devido à necessidade de usar a `identity.getAuthtoken` solicitação para obter o token para que os usuários conectados enviem a solicitação de API de licenciamento baseado em REST.  O Microsoft Edge não é compatível com a `getAuthtoken` solicitação, portanto, esse fluxo não funciona.  

Para portar a sua extensão Chrome, siga estas etapas:  

1.  Examine as APIs de extensão do Chrome usadas nas extensões.  Se você estiver usando recursos ou APIs que não são compatíveis com o Microsoft Edge, talvez não seja possível portar a extensão.  
    
    > [!NOTE]
    > A `getAuthToken` API não funciona com o Microsoft Edge, mas você pode usar `launchWebAuthFlow` para buscar um token OAuth2 para autenticar usuários.  
    
1.  Se você estiver usando `Chrome` no nome ou na descrição da extensão, remarcando a extensão para `Microsoft Edge` .  Você deve passar no processo de certificação.  
    
1.  Teste sua extensão para verificar se ela funciona no Microsoft Edge.  A primeira etapa para fazer isso é garantir que você tenha recursos de desenvolvedor de extensão ativados.  Isso permite que você carregue arquivos de extensão no Microsoft Edge para poder testar a extensão durante o seu desenvolvimento.  
    
1.  Se tiver problemas, depure as extensões no Microsoft Edge usando o DevTools ou [entre em contato conosco][mailtoExtensionPartnerOpsMicrosoft].  
    
1.  Agora, a extensão é refinada e está pronta para ser empacotada.  Se você quiser se preparar para enviar para o catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \), não será necessário empacotar a extensão.  Além disso, siga nossas [diretrizes de publicação][ExtensionsPublishExtension] para publicar sua extensão em Complementos do Microsoft Edge.  
    
    > [!NOTE]
    > Se sua extensão trocar mensagens com um aplicativo nativo usando `chrome.runtime.connectNative` API, certifique-se de que você definiu `allowedorigins` para " `extension://[Microsoft-Catalog-extensionID]` " em seu arquivo de manifesto do seu host de mensagens nativa.  Isso permite que o aplicativo identifique a extensão.  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Publicar uma extensão"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagamentos unidirecionais-Google Chrome"  
