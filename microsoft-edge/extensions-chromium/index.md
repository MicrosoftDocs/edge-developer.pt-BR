---
description: A visão geral das extensões do Microsoft Edge (Chromium), bem como a criação e a publicação de extensões do navegador em geral.
title: Extensões Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento de extensões, extensões de navegador, Complementos, central de parceiros, desenvolvedor, extensões de Chromium
ms.openlocfilehash: 04b9ffb7ec175bad4f980310819ea6d3551ef9f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230940"
---
# Visão geral das extensões do Microsoft Edge (Chromium) 

Uma extensão é um pequeno programa que você \ (o desenvolvedor \) pode usar para adicionar novos recursos ao Microsoft Edge \ (Chromium \) ou modificar a funcionalidade existente.  Uma extensão destina-se a melhorar a experiência de navegação diária de um usuário fornecendo funcionalidades de nicho que são importantes para os públicos-alvo.  

Você pode criar extensões se sua ideia ou produto depende da disponibilidade de um navegador da Web específico ou aumenta a experiência de navegação onde a funcionalidade que você deseja fornecer estende os sites existentes.  Exemplos de experiências complementares incluem adblockers e gerentes de senha.  

Uma extensão é estruturada de forma semelhante a um aplicativo Web regular.  No mínimo, ele inclui um arquivo JSON de manifesto do aplicativo que contém informações básicas sobre a plataforma, um arquivo JavaScript para definir funcionalidades e um arquivo HTML e CSS para determinar a aparência da interface do usuário \ (conforme obrigatório \).  Para trabalhar diretamente com parte do navegador, como uma janela ou guia, você deve enviar solicitações de API e, muitas vezes, referenciar o navegador pelo nome.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Uma extensão Microsoft Edge (Chromium)":::
  Uma extensão \ (Chromium \) do Microsoft Edge  
:::image-end:::  

## Orientação básica  

Alguns dos navegadores mais populares a serem criados são o Safari, o Firefox, o Chrome, o Opera, o Brave e o Microsoft Edge.  Locais incríveis para começar seus tutoriais de desenvolvimento de extensão e pesquisa de documentação são sites hospedados pelas organizações do navegador.  A tabela a seguir não é definitiva, por favor, use-a como ponto de partida útil.  

| Navegador da Web | Baseado em Chromium? | Home Page de desenvolvimento de extensão |  
|:--- |:--- |:--- |  
| Safari | Não | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Não | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Sim | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Sim | [dev.opera.com/extensions][OperaDevExtensions] |  
| Brave | Sim | Usa o [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| novo Microsoft Edge | Sim | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Muitos dos tutoriais dos sites usam APIs específicas do navegador que podem não corresponder ao navegador para o qual você está desenvolvendo.  Na maioria dos casos, uma extensão Chromium funciona como está em diferentes navegadores Chromium e as APIs funcionam como esperado.  Apenas algumas APIs menos comuns podem ser estritamente específicas do navegador.  Para obter links para os tutoriais, consulte [Consulte também](#see-also).  

## Por que Chromium?

Se a sua meta é publicar sua extensão para o maior número possível de extensões do navegador, ele deve ser modificado para várias versões para direcionar e executar em cada ambiente de navegador distinto.  [As extensões do Safari][AppleDeveloperSafariservicesAppExtensions], ao contrário de outros tipos de extensão, podem aproveitar o código nativo e Web para se comunicar com os aplicativos nativos da contraparte.  [As extensões do Firefox][MDNWebextensions] compartilham mais em comum com os outros tipos de extensão, mas também há algumas [diferenças][ExtensionworkshopPorting] a serem consideradas.  No entanto, há algumas boas notícias; os últimos quatro navegadores do gráfico podem aproveitar o mesmo pacote de código e minimizar a necessidade de alterar e manter versões paralelas.  Isso ocorre porque os navegadores se baseiam no [projeto de código-fonte aberto Chromium][|::ref1::|Home].  

A criação de uma extensão Chromium permite que você escreva a quantidade mínima de código para maximizar o número de repositórios de extensão que você está direcionando e, basicamente, o número de usuários que podem encontrar e adquirir sua extensão.  

O conteúdo a seguir se concentra principalmente em extensões Chromium.  

## Compatibilidade de navegador e testes de extensão  

Ocasionalmente, a paridade da API não existe entre os navegadores da Chromium.  Por exemplo, existem diferenças nas APIs de identidade e pagamento.  Para garantir que sua extensão atenda às expectativas do cliente, revise o status da API por meio da documentação oficial do navegador, como [APIs do Chrome][ChromeDeveloperExtensionsApiIndex], [APIs de extensão com suporte no Opera][OperaDevExtensionsApis]e [extensão Chrome da portabilidade para a Microsoft (Chromium) Edge][ExtensionsChromiumDeveloperGuidePortChrome].  

Dependendo das APIs que você precisa, essas diferenças podem significar que você deve criar pacotes de código ligeiramente diferentes com pequenas diferenças no código para cada loja.  

Ao desenvolver a extensão, você pode Sideload-la em seu navegador para testá-la em ambientes diferentes antes de enviar a extensão para os repositórios do navegador.  

## Publicar sua extensão em repositórios do navegador  

Você pode enviar e buscar extensões do navegador nos seguintes repositórios do navegador.  

*   [Complementos do navegador Firefox][MozillaAddonsFirefoxExtensions]  
*   [Loja da Web Chrome][GoogleChromeWebstoreCategoryExtensions]  
*   [Complementos do Opera][OperaAddonsExtensions]  
*   [Complementos do Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Algumas lojas permitem baixar extensões listadas de outros navegadores.  O download a partir de outro navegador pode salvar o empenho de \ (o desenvolvedor \) na frente e remover a necessidade de envio para outras lojas se os usuários puderem navegar até as listagens da loja existente em diferentes navegadores.  No entanto, o acesso entre navegadores não é garantido por lojas de navegador.  Para garantir que os usuários possam encontrar a extensão em diferentes navegadores, você deve manter uma listagem em cada repositório de extensão do navegador.  

Uma extensão pode ter públicos sobrepostos que muitas vezes usam vários navegadores, ou você pode descobrir que deve estar direcionando a um público-alvo que ainda não o fez.  Para que isso aconteça, as extensões Chromium existentes podem ser migradas de um navegador para outro.  

### Migrar uma extensão existente para o Microsoft Edge  

Se você já tiver desenvolvido uma extensão para outro Chromium navegador e desejar oferecer e garantir que ele funcione pelo Microsoft Edge, você não precisará regravar a extensão.  Migrar extensões do Chromium existentes para outros navegadores do Chromium é simples, desde que as APIs que você usa estiverem disponíveis em diferentes navegadores, ou há outras APIs que fornecem a funcionalidade necessária.  

Para obter mais informações sobre como fazer a portabilidade de sua extensão Chrome, consulte [borda do Chrome de portabilidade para a Microsoft (Chromium) Edge][ExtensionsChromiumDeveloperGuidePortChrome].  Depois de transferir a extensão para o navegador de destino, a próxima etapa é publicá-la.  

### Publicação no site de Complementos do Microsoft Edge  

Para começar a publicar sua extensão no Microsoft Edge, você deve [se registrar para uma conta de desenvolvedor][MicrosoftDeveloperRegistration] com uma conta de email do MSA \ (@outlook. com, @live. com e assim por diante \) para enviar sua listagem de extensão na loja.  Ao escolher um endereço de email para se registrar, considere se você deve transferir ou compartilhar a posse da extensão com outras pessoas em sua organização.  Após a conclusão do registro, você pode criar um novo envio de extensão para a loja.  

Para enviar sua extensão para a loja, você deve atender aos seguintes requisitos.  

*   Um arquivo morto \ (. zip \) que contém os arquivos de código.  
*   Todos os ativos visuais necessários, que incluem um logotipo e um bloco promocional pequeno.  
*   Mídia promocional opcional, como capturas de tela, blocos promocionais maiores, uma URL ou qualquer combinação de vídeos da extensão.  
*   Informações que descrevem sua extensão, como o nome, a descrição curta, a descrição longa e um link para a política de privacidade.  

> [!NOTE]
> Diferentes lojas podem ter requisitos de envio diferentes.  A lista acima resume os [requisitos][ExtensionsChromiumPublish] para publicar uma extensão para o Microsoft Edge.  

Depois de concluir o processo de envio, a extensão será analisada e o processo de certificação será revisado, e ele passará ou falhará.  Os proprietários são notificados sobre o resultado e são dadas as próximas etapas necessárias.  Se você enviar uma extensão atualizada à loja, incluindo atualizações para os detalhes da listagem da extensão, um novo processo de revisão será iniciado.  

## Consulte também  

*   [Portando uma extensão Google Chrome][ExtensionworkshopPorting]  
*   [Criando uma extensão de aplicativo do Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Sua primeira extensão (Firefox)][MDNWebextensionsYourFirst]  
*   [Tutorial de introdução (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Introdução (Opera)][OperaDevExtensionsGettingStarted]  
*   [Introdução às extensões do Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Extensão Chrome de porta para Microsoft (Chromium) Edge | Documentos da Microsoft"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Introdução às extensões do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar uma extensão | Documentos da Microsoft"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desenvolver extensões para o Microsoft Edge | Desenvolvedor da Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Centro de parcerias | Desenvolvedor da Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensões para Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensões do aplicativo Safari | Desenvolvedor da Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Criando uma extensão do aplicativo Safari | Desenvolvedor da Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "O que são extensões? | Desenvolvedor Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "APIs do Chrome | Desenvolvedor Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Tutorial de introdução | Desenvolvedor Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portabilidade de uma extensão Google Chrome | Workshop de extensão"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Loja da Web Chrome"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensões do navegador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Sua primeira extensão | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensões | Complementos do Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensões | Complementos do Opera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentação de extensões | Dev. opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "APIs de extensão com suporte no Opera | Dev. opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Introdução | Dev. opera"  
