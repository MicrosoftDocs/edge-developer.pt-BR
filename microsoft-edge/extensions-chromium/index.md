---
description: Uma visão geral da criação e publicação de Extensões do Microsoft Edge (Chromium).
title: Visão geral das extensões do Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor, extensões chromium
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327523"
---
# Visão geral das extensões do Microsoft Edge (Chromium)  

Uma extensão é um pequeno programa que você \(um desenvolvedor\) usa para adicionar ou modificar recursos do Microsoft Edge \(Chromium\).  Uma extensão destina-se a melhorar a experiência de navegação diária do usuário.  Ele fornece funcionalidade de nicho que é importante para um público-alvo.  

Você pode criar uma extensão se tiver uma ideia ou produto com base em uma das condições a seguir.  

*   Um navegador da Web específico.  
*   Melhorias nos recursos de páginas da Web específicas.  
    
Exemplos de experiências acompanhantes incluem bloqueadores de ad e gerentes de senha.  

Uma extensão é estruturada de forma semelhante a um aplicativo Web normal.  No mínimo, ele deve incluir os seguintes recursos.

*   Um arquivo JSON de manifesto do aplicativo que contém informações básicas da plataforma.  
*   Um arquivo JavaScript que define a funcionalidade.  
*   Arquivos HTML e CSS que definem a interface do usuário.  

Para trabalhar diretamente com parte do navegador, como uma janela ou guia, você deve enviar solicitações de API e fazer referência freqüentemente ao navegador pelo nome.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Uma extensão do Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  Uma extensão do Microsoft Edge \(Chromium\)  
:::image-end:::  

## Diretrizes básicas  

Alguns dos navegadores mais populares para criar extensões incluem Safari, Firefox, Chrome, Opera, Safari e Microsoft Edge.  Ótimos lugares para começar seus tutoriais de desenvolvimento de extensão e pesquisa de documentação são sites hospedados pelas organizações do navegador.  A tabela a seguir não é definitiva e pode ser usada como ponto de partida.  

| Navegador da Web | Baseado no Chromium? | Página da Web de desenvolvimento de extensão |  
|:--- |:--- |:--- |  
| Safari | Não | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Não | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Sim | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Sim | [dev.opera.com/extensions][OperaDevExtensions] |  
| Mamão | Sim | Usa [a Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| novo Microsoft Edge | Sim | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Muitos dos tutoriais dos sites usam APIs específicas do navegador que podem não corresponder ao navegador para o qual você desenvolve.  Na maioria dos casos, uma extensão Chromium funciona como está em diferentes navegadores Chromium e as APIs funcionam conforme o esperado.  Apenas algumas APIs menos comuns podem ser estritamente específicas do navegador.  Para links para os tutoriais, navegue até [Ver também.](#see-also)  

## Por que o Chromium?  

Se seu objetivo for publicar sua extensão no armazenamento de extensões de cada navegador, ela deverá ser modificada para que cada versão seja segmentada e executado em cada ambiente distinto do navegador.  Por exemplo, as [extensões do Safari podem][AppleDeveloperSafariservicesAppExtensions] usar código nativo e web para se comunicar com aplicativos nativos equivalentes.  Os últimos quatro navegadores da tabela anterior usam o mesmo pacote de código e minimiza a necessidade de manter versões paralelas.  Esses navegadores são baseados no projeto [de código aberto do Chromium.][|::ref1::|Home]  

Crie uma extensão Chromium para escrever a menor quantidade de código.  Ele também visa o número máximo de armazenamentos de extensão e, por fim, o número máximo de usuários que encontram e adquirem sua extensão.  

O conteúdo a seguir se concentra principalmente em extensões do Chromium.  

## Teste de compatibilidade e extensão do navegador  

Ocasionalmente, a paridade de API não existe entre navegadores Chromium.  Por exemplo, há diferenças nas APIs de identidade e pagamento.  Para garantir que sua extensão atenda às expectativas dos clientes, revise o status da API por meio dos seguintes documentos oficiais do navegador.  

*   [Chrome APIs][ChromeDeveloperExtensionsApiIndex]  
*   [APIs de extensão com suporte no Opera][OperaDevExtensionsApis]  
*   [Fazer a portabilidade da extensão Chrome para o Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]  
    
As APIs necessárias definem as alterações que devem ser feitas para lidar com as diferenças entre cada navegador.  Isso pode significar que você deve criar pacotes de código ligeiramente diferentes com pequenas diferenças para cada loja.  

Para testar sua extensão em ambientes diferentes antes de encaminhá-la para um armazenamento do navegador, sideload-a em seu navegador enquanto você a desenvolve.  

## Publicar sua extensão nos armazenamentos do navegador  

Você pode enviar e buscar extensões do navegador nos seguintes armazenamentos de navegador.  

*   [Complementos do navegador Firefox][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Complementos de opera][OperaAddonsExtensions]  
*   [Complementos do Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Alguns armazenamentos permitem que você baixe extensões listadas de outros navegadores.  No entanto, o acesso entre navegadores não é garantido pelos armazenamentos do navegador.  Para garantir que os usuários encontrem sua extensão em navegadores diferentes, você deve manter uma listagem em cada armazenamento de extensão do navegador.  

Talvez os usuários precisem instalar sua extensão em navegadores diferentes. Nesse cenário, você pode migrar extensões existentes do Chromium de um navegador para outro.  

### Migrar uma extensão existente para o Microsoft Edge  

Se você já desenvolveu uma extensão para outro navegador Chromium, você pode encaminhá-la para a loja de Complementos do Microsoft Edge. Você não precisa reescrever sua extensão e deve verificar se ela funciona no Microsoft Edge.  Ao migrar uma extensão Chromium existente para outros navegadores Chromium, certifique-se de que as mesmas APIs ou alternativas estão disponíveis para seu navegador de destino.  

Para obter mais informações sobre como fazer a portabilidade da extensão do Chrome para o Microsoft Edge, navegue até Portar extensões do Chrome para [o Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome] Depois de fazer a portabilidade da extensão para o navegador de destino, a próxima etapa é publicá-la.  

### Publicar no site de complementos do Microsoft Edge  

Para começar [a][MicrosoftDeveloperRegistration] publicar sua extensão no Microsoft Edge, você deve se registrar em uma conta de desenvolvedor com uma conta de email MSA para enviar sua listagem de extensão para a loja.  Uma conta de email da MSA `@outlook.com` inclui e assim por `@live.com` diante.  Ao escolher um endereço de email para registrar, considere se você deve transferir ou compartilhar a propriedade da extensão com outras pessoas em sua organização.  Depois que o registro for concluído, você poderá criar um novo envio de extensão para a loja.  

Para enviar sua extensão para o armazenamento, certifique-se de fornecer os itens a seguir.  

*   Um arquivo morto \( `.zip` \) que contém seus arquivos de código.  
*   Todos os ativos visuais necessários, que incluem um logotipo e um pequeno pacote promocional.  
*   Mídia promocional opcional, como capturas de tela, blocos promocionais e uma URL de vídeo.  
*   Informações que descrevem sua extensão, como nome, breve descrição e um link de política de privacidade.  

> [!NOTE]
> Diferentes lojas podem ter requisitos de envio diferentes.  A lista acima resume os requisitos [para][ExtensionsChromiumPublish] publicar uma extensão do Microsoft Edge.  

Depois que você enviar sua extensão com êxito, sua extensão passará por um processo de revisão e passará ou falhará no processo de certificação.  Os proprietários são notificados sobre o resultado e dado as próximas etapas conforme necessário.  Se você enviar uma atualização de extensão para a loja, um novo processo de revisão será iniciado.  

## Confira também  

*   [Fazer a portabilidade de uma extensão do Google Chrome][ExtensionworkshopPorting]  
*   [Criar uma extensão do aplicativo Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Sua primeira extensão (Firefox)][MDNWebextensionsYourFirst]  
*   [Tutorial de introdução (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Começar (Opera)][OperaDevExtensionsGettingStarted]  
*   [Começar a trabalhar com extensões do Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Fazer a portabilidade da extensão Chrome para o Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Como começar a trabalhar com extensões do Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar uma extensão | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desenvolver extensões para o Microsoft Edge | Desenvolvedor da Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Desenvolvedor da Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensões do Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensões do aplicativo Safari | Apple Developer"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Criando uma extensão de aplicativo safari | Apple Developer"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "O que são extensões? | Desenvolvedor do Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "ApIs do Chrome | Desenvolvedor do Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Tutorial de Introdução | Desenvolvedor do Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portando uma extensão do Google Chrome | Workshop de extensão"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensões do Navegador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Sua primeira extensão | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensões | Complementos para Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensões | Complementos de Opera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentação de extensões | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "APIs de extensão com suporte no Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Guia de | Dev. Opera"  
