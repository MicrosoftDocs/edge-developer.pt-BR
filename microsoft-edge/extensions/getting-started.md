---
description: Obtenha uma visão geral completa da jornada do início do desenvolvimento para o empacotamento de extensões do Microsoft Edge.
title: Extensões – como começar
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, extensões
ms.openlocfilehash: 5d2bf0ea2236e36b9e6205e13291ffee4118d9d7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561249"
---
# Introdução às extensões  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Seja você um novo desenvolvedor que queira se familiarizar com as extensões ou um veterano experiente com uma extensão Chrome para a qual você gostaria de portar, este guia contém todas as informações necessárias para desenvolver, testar, empacotar e publicar uma extensão para o Microsoft Edge. 

## Desenvolvendo uma extensão

A primeira etapa dessa jornada é criar uma extensão do Microsoft Edge: 
- Novo nas extensões? Confira nosso [guia sobre como criar extensões](./guides/creating-an-extension.md) para obter informações sobre como criar sua primeira extensão de navegador! 
- Já está familiarizado com as APIs de extensão? Confira nossa [documentação de suporte à API](./api-support.md) para obter as informações mais recentes sobre quais APIs têm suporte/em desenvolvimento. 
- Tem uma extensão Chrome para a qual você quer transferir o Microsoft Edge? Experimente o [Kit de ferramentas de extensão do Microsoft Edge](./guides/porting-chrome-extensions.md)!

## Carregando e Depurando

Depois que tiver uma extensão que funcione no Microsoft Edge, você desejará carregá-la para vê-la em ação. A primeira etapa para fazer isso é garantir que você tenha [recursos de desenvolvedor de extensão habilitados](./guides/adding-and-removing-extensions.md). Isso permitirá que você carregue arquivos de extensão no Microsoft Edge para poder testar a extensão durante o seu desenvolvimento. Se você tiver problemas, as ferramentas de desenvolvedor F12 permitem que você [depure os vários contextos da extensão](./guides/debugging-extensions.md) para determinar exatamente o que está acontecendo. Ainda está com problemas? Nosso [Guia de solução de problemas](./troubleshooting.md) tem soluções para várias pegadinhas comuns. 

## Relatar bugs e obter ajuda

Achou que encontrou um bug na plataforma de extensões? Se o problema for específico do Microsoft Edge, procure-o em nosso [controlador de problemas do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/issues/) para ver se ele já foi reportado. Em caso afirmativo, ótimo! Você pode pressionar o botão "+ Eu também" para votar no bug e o botão "Assista a este problema para atualizações" para ser alertado sobre qualquer alteração no problema. Se você não conseguir encontrar o problema que está executando, sinta-se à vontade para abrir um novo problema e fornecer o máximo de informações possível para que nossos desenvolvedores possam procurá-los. 

Estamos faltando uma API para a qual sua extensão precisa funcionar corretamente? Em caso afirmativo, estamos [sempre ouvindo o UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). Sinta-se à vontade para fazer uma votação na sua API se ela já existir ou para criar um novo item de feedback para que outros desenvolvedores possam fazer o mesmo voto! 

Você tem alguma dúvida de que não consegue encontrar uma resposta na documentação? É altamente recomendável que você ingresse na [comunidade de extensões do Microsoft Edge](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) no estouro de pilha e faça a pergunta lá!

## Testando sua extensão

Na atualização de aniversário do Windows, o [Microsoft WebDriver](../dev-guide/tools/webdriver.md) dá suporte ao carregamento do lado automatizado de extensões nas sessões do Microsoft Edge. Isso permitirá que você escreva testes simples para garantir que qualquer extensão que se destina a modificar uma página faz isso da maneira esperada. Você pode encontrar mais informações sobre como fazer isso em nosso [Guia de teste](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver). Além disso, fique atento às atualizações, pois planejamos adicionar mais recursos específicos de extensão ao Microsoft WebDriver no futuro.

## Adicionando os toques finais

Portanto, a extensão funciona no Microsoft Edge. O que acontece a seguir? Antes de continuar a empacotamento da extensão, recomendamos que você Confira esses guias para garantir que sua extensão esteja seguindo nossas políticas de práticas recomendadas: 
- Verifique se os ícones de extensão estão [dimensionados](./guides/design.md) e [acessíveis](./guides/accessibility.md) corretamente (ou seja, eles estão visíveis nos temas claro e escuro do Microsoft Edge, bem como no modo de alto contraste). 
- Se sua extensão precisar dar suporte a vários idiomas, certifique-se de que você tenha feito uma olhada em nosso [Guia de internacionalização](./guides/internationalization.md). 

## Empacotando uma extensão

Agora, a extensão é refinada e está pronta para ser empacotada. Não importa se você quer empacotá-lo para se preparar para envio à Microsoft Store, ou para facilitar a distribuição em suas equipes de desenvolvimento/teste, há muitos recursos disponíveis para ajudá-lo a: 

- Nossa solução recomendada para a criação de um pacote de extensão é acompanhar nosso [Guia de empacotamento do ManifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) , que guiará você pelas etapas de uso de uma ferramenta baseada em node. js para empacotar facilmente a extensão, independentemente da plataforma que você desenvolver. Se você quiser uma análise mais manual e profunda do nosso formato de empacotamento de extensão, consulte o nosso [Guia de criação de pacotes Appx](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder). 
- Se a extensão oferecer suporte a vários idiomas, também será necessário seguir o nosso guia sobre a [localização de pacotes de extensão](./guides/packaging/localizing-extension-packages.md) para que os idiomas que você tem na extensão sejam registrados corretamente após a compactação. 

Se você for um cliente corporativo que pretende distribuir as extensões empacotadas via canais internos, consulte o [Guia de nossas extensões para empresas](./extensions-for-enterprise.md) para ver como fazer isso.  

## Publicando na Microsoft Store

Como a plataforma de extensões ainda está em seu uso insofisticado, estamos gerenciando os envios de extensão para a Microsoft Store para que possamos nos concentrar em oferecer uma experiência de qualidade para nossos usuários e desenvolvedores. Dito isso, queremos torná-lo tão fácil quanto possível para os desenvolvedores publicarem suas extensões. Como resultado, lançamos recentemente um novo formulário de [envio de extensão](https://aka.ms/extension-request) em que os desenvolvedores podem solicitar permissão para enviar a sua extensão Appx para a Microsoft Store.
 

A primeira etapa do processo de publicação é garantir que sua extensão esteja de acordo com a [política de extensão do navegador](./microsoft-browser-extension-policy.md) , bem como a [seção extensões do Microsoft Edge das políticas da Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12). 

Depois de confirmar que sua extensão segue as políticas, você precisará se registrar para uma [conta de desenvolvedor no centro de parceiros e reservar o nome de sua extensão](./guides/packaging/extensions-in-the-windows-dev-center.md). Em seguida, você precisará enviar uma solicitação por meio do [formulário de envio de extensão](https://aka.ms/extension-request) para solicitar permissão para publicar na Microsoft Store. Se você tentar enviar seu AppX de extensão sem primeiro obter permissão, receberá o seguinte erro:

`Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.`

Depois de enviar uma solicitação, receberemos uma notificação e tentaremos acessar o seu envio o mais rápido possível. Isso pode demorar um pouco devido ao alto volume de envios que recebemos, mas vamos notificá-lo por e-mail no momento em que você está aprovado! Depois de receber o email, você poderá enviar seu AppX de extensão para a Microsoft Store via Partner Center. Observe que você não precisa assinar seu AppX antes de enviá-lo; o processo de inclusão da Microsoft Store cuidará disso para você.
 
> [!NOTE]
> O processo de publicação de uma extensão para a Microsoft Store (seja uma extensão totalmente nova ou uma atualização para uma existente) pode levar até 72 horas para ser concluído. Para acelerar esse processo, verifique se você verificou essas armadilhas comuns antes de enviá-las para evitar ter que reenviar mais tarde: 
> - Suas capturas de tela estão dimensionadas corretamente e são de sua extensão em execução no Microsoft Edge 
> - Sua descrição da extensão faz referência a "Microsoft Edge" em vez de "Edge" (essa é uma exigência legal) 
> - O ícone do 150x150 no seu pacote de extensão não [tem um plano de fundo transparente](./guides/design.md#microsoft-store-icon) (o cliente da Microsoft Store não renderiza corretamente imagens com planos de fundo transparentes) 

Além das informações acima e, se aplicável, certifique-se de que qualquer informação sobre a disponibilidade da plataforma em seu site mencione corretamente a disponibilidade da extensão no Microsoft Edge. Embora a Microsoft Store não permita uma instalação de extensão embutida com apenas um clique, você pode fazer [um link profundo para a extensão na Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) para facilitar a aquisição dos usuários. 

A Microsoft Store também permite que você [controle a visibilidade da extensão](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) no catálogo da Microsoft Store. Alguns de nossos parceiros tiraram proveito dessa funcionalidade para obter o seguinte: 
- Publicação de uma segunda versão beta da extensão como oculta na Microsoft Store.
- Publicar inicialmente a extensão como oculta para monitorar a telemetria inicial antes de alterar seu status para visível assim que um determinado nível de confiança for atingido.

## Pronto!

Se você chegou ao final deste guia, concluiu o processo de desenvolvimento de uma extensão para o Microsoft Edge! Verifique a nossa página de [dicas e truques](./tips-and-tricks.md) para ver ideias sobre como comercializar sua extensão e interagir com os usuários.
