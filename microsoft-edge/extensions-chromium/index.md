---
description: Uma visão geral da criação e publicação Microsoft Edge (Chromium) Extensões.
title: Visão geral Microsoft Edge extensões (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, desenvolvimento de extensões, extensões de navegador, addons, partner center, desenvolvedor, extensões de cromo
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327523"
---
# Visão geral Microsoft Edge extensões (Chromium)  

Uma extensão é um pequeno programa que você \(um desenvolvedor\) usa para adicionar ou modificar recursos para Microsoft Edge \(Chromium\).  Uma extensão destina-se a melhorar a experiência de navegação diária de um usuário.  Ele fornece funcionalidade de nicho que é importante para um público-alvo.  

Você pode criar uma extensão se tiver uma ideia ou produto que se baseia em uma das seguintes condições.  

*   Um navegador da Web específico.  
*   Melhorias nos recursos de páginas da Web específicas.  
    
Exemplos de experiências de parceiro incluem bloqueadores de ad e gerentes de senha.  

Uma extensão é estruturada de forma semelhante a um aplicativo Web regular.  No mínimo, ele deve incluir os seguintes recursos.

*   Um arquivo JSON de manifesto de aplicativo que contém informações básicas da plataforma.  
*   Um arquivo JavaScript que define a funcionalidade.  
*   Arquivos HTML e CSS que definem a interface do usuário.  

Para trabalhar diretamente com parte do navegador, como uma janela ou guia, você deve enviar solicitações de API e frequentemente fazer referência ao navegador pelo nome.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Uma extensão Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  Uma Microsoft Edge \(Chromium\)  
:::image-end:::  

##  <a name="basic-guidance"></a>Diretrizes básicas  

Alguns dos navegadores mais populares para criar extensões incluem Safari, Firefox, Chrome, Opera, Brave e Microsoft Edge.  Ótimos locais para começar os tutoriais de desenvolvimento de extensão e a pesquisa de documentação são sites hospedados pelas organizações do navegador.  A tabela a seguir não é definitiva e pode ser usada como ponto de partida.  

| Navegador da Web | Chromium baseado? | Página da Web de desenvolvimento de extensão |  
|:--- |:--- |:--- |  
| Safari | Não | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | Não | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Sim | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Sim | [dev.opera.com/extensions][OperaDevExtensions] |  
| Bálsam | Sim | Usa [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| novo Microsoft Edge | Sim | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Muitos dos tutoriais dos sites usam APIs específicas do navegador que podem não corresponder ao navegador para o qual você desenvolve.  Na maioria dos casos, uma extensão Chromium funciona como está em diferentes Chromium e as APIs funcionam conforme o esperado.  Somente algumas APIs menos comuns podem ser estritamente específicas do navegador.  Para links para os tutoriais, navegue até [Ver também](#see-also).  

##  <a name="why-chromium"></a>Por Chromium?  

Se seu objetivo é publicar sua extensão no armazenamento de extensões para cada navegador, ela deve ser modificada para cada versão para direcionar e executar em cada ambiente de navegador distinto.  Por exemplo, [as extensões do Safari][AppleDeveloperSafariservicesAppExtensions] podem usar a Web e o código nativo para se comunicar com aplicativos nativos equivalentes.  Os últimos quatro navegadores da tabela anterior usam o mesmo pacote de código e minimizam o requisito de manter versões paralelas.  Esses navegadores se baseiam no Chromium [de código aberto.][|::ref1::|Home]  

Crie uma Chromium para gravar a menor quantidade de código.  Ele também direciona o número máximo de armazenamentos de extensão e, por fim, o número máximo de usuários que encontram e adquirem sua extensão.  

O conteúdo a seguir se concentra principalmente em Chromium extensões.  

##  <a name="browser-compatibility-and-extension-testing"></a>Teste de compatibilidade e extensão do navegador  

Ocasionalmente, a paridade da API não existe entre Chromium navegadores.  Por exemplo, há diferenças nas APIs de identidade e pagamento.  Para garantir que sua extensão atenda às expectativas do cliente, revise o status da API por meio dos seguintes documentos oficiais do navegador.  

*   [Chrome APIs][ChromeDeveloperExtensionsApiIndex]  
*   [APIs de extensão com suporte no Opera][OperaDevExtensionsApis]  
*   [Extensão porta chrome para Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]  
    
As APIs necessárias definem as alterações que devem ser feitas para resolver as diferenças entre cada navegador.  Isso pode significar que você deve criar pacotes de código ligeiramente diferentes com pequenas diferenças para cada loja.  

Para testar sua extensão em ambientes diferentes antes de enviar para um armazenamento do navegador, armazene-a no navegador enquanto a desenvolve.  

##  <a name="publish-your-extension-to-browser-stores"></a>Publicar sua extensão nos armazenamentos do navegador  

Você pode enviar e buscar extensões de navegador nos seguintes armazenamentos de navegador.  

*   [Complementos do navegador Firefox][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Addons de opera][OperaAddonsExtensions]  
*   [Microsoft Edge Complementos][MicrosoftEdgeAddonsCategoryExtensions]  

Alguns armazenamentos permitem baixar extensões listadas de outros navegadores.  No entanto, o acesso entre navegadores não é garantido pelos armazenamentos do navegador.  Para garantir que seus usuários encontrem sua extensão em navegadores diferentes, você deve manter uma listagem em cada armazenamento de extensão do navegador.  

Os usuários podem precisar instalar sua extensão em navegadores diferentes. Nesse cenário, você pode migrar extensões Chromium existentes de um navegador para outro.  

###  <a name="migrate-an-existing-extension-to-microsoft-edge"></a>Migrar uma extensão existente para Microsoft Edge  

Se você já tiver desenvolvido uma extensão para outro navegador Chromium, você poderá enviar para o Microsoft Edge de complementos. Você não precisa reescrever sua extensão e deve verificar se ela funciona Microsoft Edge.  Ao migrar uma extensão Chromium para outros navegadores Chromium, verifique se as mesmas APIs ou alternativas estão disponíveis para o navegador de destino.  

Para obter mais informações sobre como portar sua extensão do Chrome para Microsoft Edge, navegue até [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]. Após a portabilidade da extensão para o navegador de destino, a próxima etapa é publicá-la.  

###  <a name="publish-to-the-microsoft-edge-add-ons-website"></a>Publicar no site complementos do Microsoft Edge site  

Para começar [a][MicrosoftDeveloperRegistration] publicar sua extensão no Microsoft Edge, você deve se registrar em uma conta de desenvolvedor com uma conta de email MSA para enviar sua listagem de extensão para o armazenamento.  Uma conta de email MSA inclui `@outlook.com` , e assim por `@live.com` diante.  Ao escolher um endereço de email para registrar, considere se você deve transferir ou compartilhar a propriedade da extensão com outras pessoas em sua organização.  Depois que o registro for concluído, você poderá criar um novo envio de extensão para o armazenamento.  

Para enviar sua extensão para o armazenamento, certifique-se de fornecer os itens a seguir.  

*   Um arquivo morto \( `.zip` \) que contém seus arquivos de código.  
*   Todos os ativos visuais necessários, que incluem um logotipo e um pequeno azulejo promocional.  
*   Mídia promocional opcional, como capturas de tela, blocos promocionais e uma URL de vídeo.  
*   Informações que descrevem sua extensão, como o nome, a descrição curta e um link de política de privacidade.  

> [!NOTE]
> Os diferentes armazenamentos podem ter requisitos de envio diferentes.  A lista acima resume os requisitos [para][ExtensionsChromiumPublish] publicar uma extensão para Microsoft Edge.  

Depois de enviar sua extensão com êxito, sua extensão passa por um processo de revisão e passa ou falha no processo de certificação.  Os proprietários são notificados do resultado e dado as próximas etapas conforme necessário.  Se você enviar uma atualização de extensão para o armazenamento, um novo processo de revisão será iniciado.  

##  <a name="see-also"></a>Consulte também  

*   [Porta uma extensão do Google Chrome][ExtensionworkshopPorting]  
*   [Criar uma extensão do Aplicativo Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Sua primeira extensão (Firefox)][MDNWebextensionsYourFirst]  
*   [Tutorial introdução (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Começar (Opera)][OperaDevExtensionsGettingStarted]  
*   [Começar com extensões Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Port Chrome Extension To Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Iniciando com extensões Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar uma extensão | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desenvolver extensões para Microsoft Edge | Desenvolvedor da Microsoft"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Partner Center | Desenvolvedor da Microsoft"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensões para Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensões de aplicativo safari | Desenvolvedor apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Criando uma extensão do aplicativo Safari | Desenvolvedor apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "O que são extensões? | Desenvolvedor do Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "APIs do Chrome | Desenvolvedor do Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Introdução ao Tutorial | Desenvolvedor do Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Portando uma extensão do Google Chrome | Workshop de Extensão"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensões | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensões do navegador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Sua primeira extensão | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensões | Complementos para Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensões | Opera Addons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentação de extensões | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "APIs de extensão com suporte no Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Iniciando | Dev. Opera"  
