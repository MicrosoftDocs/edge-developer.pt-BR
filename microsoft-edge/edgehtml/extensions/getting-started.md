---
description: Obter uma visão geral de ponta a ponta da jornada do desenvolvimento inicial para o empacotamento de extensões do Microsoft Edge.
title: Extensões - Iniciando
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 52d0aa5c1968518194a4e3b90cb0cc876d0c7f86
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439714"
---
# <a name="getting-started-with-extensions"></a>Iniciando com extensões  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Se você é um novo desenvolvedor que deseja se familiarizar com extensões ou um experiente com uma extensão do Chrome que você gostaria de portar, este guia contém todas as informações necessárias para desenvolver, testar, pacote e publicar uma extensão para o Microsoft Edge. 

## <a name="developing-an-extension"></a>Desenvolvendo uma extensão

A primeira etapa dessa jornada é criar uma extensão do Microsoft Edge: 
- Novo em extensões? Confira nosso [guia sobre como criar extensões](./guides/creating-an-extension.md) para obter informações sobre como criar sua primeira extensão do navegador! 
- Já está familiarizado com APIs de extensão? Confira nossa [documentação de suporte à API](./api-support.md) para obter as informações mais recentes sobre quais APIs são suportadas/em desenvolvimento. 
- Tem uma extensão do Chrome que você deseja porta para o Microsoft Edge? Experimente o [Microsoft Edge Extension Toolkit!](./guides/porting-chrome-extensions.md)

## <a name="loading-and-debugging"></a>Carregamento e depuração

Depois de ter uma extensão que funcione no Microsoft Edge, você vai querer carregá-la de lado para vê-la em ação. A primeira etapa a fazer isso é garantir que você tenha recursos de desenvolvedor de [extensão habilitados](./guides/adding-and-removing-extensions.md). Isso permitirá que você carregue arquivos de extensão de lado no Microsoft Edge para que você possa testar sua extensão durante o desenvolvimento. Se você executar qualquer problema, as ferramentas de desenvolvedor F12 permitem que você depure os vários [contextos](./guides/debugging-extensions.md) de sua extensão para determinar exatamente o que está acontecendo. Ainda está com problemas? Nosso [guia de solução de problemas](./troubleshooting.md) tem soluções para várias gotchas comuns. 

## <a name="reporting-bugs-and-getting-help"></a>Relatar bugs e obter ajuda

Acha que encontrou um bug em nossa plataforma de extensões? Se o problema for específico do Microsoft Edge, procure-o em nosso Rastreador de Problemas do [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/issues/) para ver se ele já foi relatado. Se tiver, ótimo! Você pode pressionar o botão "+ Eu também" para revogar o bug e o botão "Assista a esse problema para atualizações" a ser alertado para quaisquer alterações no problema. Se você não conseguir encontrar o problema que você está encontrando, esteja à vontade para abrir um novo problema e fornecer o máximo de informações possível para que nossos desenvolvedores possam dar uma olhada nele. 

<!--Are we missing an API that your extension needs to work properly? If so, [we're always listening on UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). Feel free to upvote your API if it already exists, or to create a new feedback item so that other developers can upvote it too! -->  

Você tem uma pergunta que não pode encontrar uma resposta na documentação? É recomendável que você participe da [comunidade extensões](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) do Microsoft Edge no Stack Overflow e pergunte-o lá!

## <a name="testing-your-extension"></a>Testando sua extensão

A partir da Atualização de Aniversário do Windows, o [Microsoft WebDriver](../webdriver/index.md) dá suporte ao carregamento automático de extensões em sessões do Microsoft Edge. Isso permitirá que você escreva testes simples para garantir que qualquer extensão destinada a modificar uma página faça isso da maneira esperada. Você pode encontrar mais informações sobre como fazer isso em nosso guia [de teste.](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver) Além disso, fique atento às atualizações enquanto planejamos adicionar mais recursos específicos de extensão ao Microsoft WebDriver no futuro.

## <a name="adding-the-final-touches"></a>Adicionando os toques finais

Portanto, sua extensão funciona no Microsoft Edge. O que acontece a seguir? Antes de continuar empacotando sua extensão, recomendamos que você confira estes guias para garantir que sua extensão siga nossas políticas de práticas: 
- Certifique-se de que [](./guides/design.md) seus ícones de extensão sejam dimensionado corretamente e acessíveis [(o](./guides/accessibility.md) que significa que eles estão visíveis em temas claros e escuros do Microsoft Edge, bem como no modo de alto contraste). 
- Se sua extensão precisar dar suporte a vários idiomas, verifique se você já viu nosso guia [de internacionalização.](./guides/internationalization.md) 

## <a name="packaging-an-extension"></a>Empacotando uma extensão

Agora sua extensão está finalmente polida e pronta para ser empacotada. Se você deseja empacotá-lo para se preparar para envio para a Microsoft Store ou para facilitar a distribuição em suas equipes de desenvolvimento/teste, há muitos recursos disponíveis para ajudá-lo: 

- Nossa solução recomendada para criar um pacote de extensão é seguir nosso guia de empacotamento [ManifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) que o guiará pelas etapas de uso de uma ferramenta baseada em Node.js para empacotar facilmente sua extensão, independentemente da plataforma em que você se desenvolva. Se você quiser uma pesquisa mais manual e detalhada em nosso formato de empacotamento de extensão, consulte nosso guia de criação de [pacote AppX.](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder) 
- Se sua extensão for compatível com vários idiomas, [](./guides/packaging/localizing-extension-packages.md) você também precisará seguir nosso guia sobre como localização de pacotes de extensão para que os idiomas que você tem em sua extensão sejam registrados corretamente após a empacotamento. 

Se você é um cliente corporativo que procura distribuir suas extensões [](./extensions-for-enterprise.md) empacotada por canais internos, confira nossas extensões para o guia empresarial para ver como fazer isso.  

## <a name="publishing-to-the-microsoft-store"></a>Publicação na Microsoft Store

Como nossa plataforma de extensões ainda está em sua infância, estamos gerenciando propositalmente os envios de extensão para a Microsoft Store para que possamos nos concentrar em oferecer uma experiência de qualidade para nossos usuários e desenvolvedores. Dito isso, queremos tornar mais fácil para os desenvolvedores publicarem suas extensões. Como resultado, iniciamos recentemente um [](https://aka.ms/extension-request) novo formulário de envio de extensão onde os desenvolvedores podem solicitar permissão para enviar sua extensão AppX para a Microsoft Store.
 
A primeira etapa do processo de publicação é garantir **** que sua extensão esteja em conformidade com nossa política de extensão do navegador, bem como com a seção extensões do Microsoft Edge das Políticas [da Microsoft Store.](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12)  

<!--  The first step of the publishing process is to make sure your extension conforms to our [browser extension policy](./microsoft-browser-extension-policy.md) as well as the [Microsoft Edge extensions section of the Microsoft Store Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).  -->  

Depois de confirmar que sua extensão segue as políticas, você precisará se registrar em uma conta de desenvolvedor no Partner Center e reservar o nome [da extensão](./guides/packaging/extensions-in-the-windows-dev-center.md). Em seguida, você precisará enviar uma solicitação por meio do nosso formulário de envio de [extensão](https://aka.ms/extension-request) para solicitar permissão para publicar na Microsoft Store. Se você tentar enviar sua extensão AppX sem obter primeiro a permissão, receberá o seguinte erro:

```text
Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.
```  

Depois de enviar uma solicitação, receberemos uma notificação e tentaremos chegar ao envio assim que possível. Isso pode demorar um pouco devido ao alto volume de envios que recebemos, mas notificaremos você por email no momento em que você for aprovado! Depois de receber o email, você poderá enviar sua extensão AppX para a Microsoft Store por meio do Partner Center. Observe que você não precisa assinar seu AppX antes de enviar; o processo de ingestão da Microsoft Store tratará disso para você!
 
> [!NOTE]
> O processo de publicação de uma extensão para a Microsoft Store (seja uma extensão nova ou uma atualização para uma existente) pode levar até 72 horas para ser concluída. Para agilizar esse processo, verifique se você verificou essas gotchas comuns antes de enviar para evitar ter que reabrir mais tarde: 
> - Suas capturas de tela são dimensionada corretamente e são de sua extensão em execução no Microsoft Edge 
> - Sua descrição de extensão faz referência ao "Microsoft Edge" em vez de "Edge" (isso é um requisito legal) 
> - Seu ícone 150x150 no pacote de extensão não tem um plano de fundo transparente [(o](./guides/design.md#microsoft-store-icon) cliente da Microsoft Store não renderiza corretamente imagens com plano de fundo transparente) 

Além do acima e, se aplicável, certifique-se de que qualquer informação de disponibilidade da plataforma em seu site mencione corretamente a disponibilidade da extensão no Microsoft Edge. Embora a Microsoft Store não permita instalação de extensão em linha de um clique, você pode vincular profundamente sua extensão na [Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) para facilitar a aquisição dos usuários. 

A Microsoft Store também permite controlar a [visibilidade da extensão](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) no catálogo da Microsoft Store. Alguns de nossos parceiros aproveitaram essa funcionalidade para alcançar o seguinte: 
- Publicar uma segunda versão beta de sua extensão como oculto na Microsoft Store.
- Publicando inicialmente sua extensão como oculta para monitorar a telemetria inicial antes de, eventualmente, alterar seu status para visível quando um determinado nível de confiança for atingido.

## <a name="thats-it"></a>Pronto!

Se você atingiu a parte inferior deste guia, concluiu o processo de desenvolvimento de uma extensão para o Microsoft Edge! Confira nossa página [](./tips-and-tricks.md) dicas e truques para saber mais sobre como comercializar sua extensão e interagir com seus usuários.
