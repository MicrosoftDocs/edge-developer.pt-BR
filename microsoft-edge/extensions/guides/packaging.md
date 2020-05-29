---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Saiba como você pode usar o recurso de mensagens nativas para que sua extensão se comunique com um aplicativo UWP complementar.
title: Extensões-pacotes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 23c97f366db527cae2672d6ad46fa666583f6398
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561191"
---
# Empacotando extensões do Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Por fim, você concluiu a extensão e está pronto para empacotá-la. Você pode estar se perguntando quais são as próximas etapas para obter isso em mãos de usuários em potencial. Este guia destina-se a ensinar como fazer exatamente isso.

O guia de empacotamento de extensão é abrangente, pois ele abrange tudo o que você gostaria de saber sobre empacotamento, até mesmo os detalhes detalhados. Se você não quiser aprender tudo que precisa saber sobre o empacotamento da extensão, você está com sorte. Adicionamos suporte para extensões ao ManifoldJS, uma ferramenta de nó de código-fonte Open. js que usa a maioria do seu pacote de Woes ausente.

> [!NOTE]
> No momento, o envio de uma extensão do Microsoft Edge para a Microsoft Store é um recurso restrito. Entre [em contato conosco](https://aka.ms/extension-request) com suas solicitações para fazer parte da Microsoft Store, e consideraremos você para uma atualização futura.


Use a estrutura de tópicos do processo abaixo para mapear sua aventura de embalagem!


## [Extensões no centro de desenvolvimento do Windows](./packaging/extensions-in-the-windows-dev-center.md)

Não importa qual rota de criação de pacotes você escolhe, manual ou ManifoldJS, a primeira etapa é registrar-se para uma conta de desenvolvedor do Windows e reservar o (s) nome (s) de sua extensão.

Depois de fazer isso, você pode se mover para [criar e testar pacotes de extensão](./packaging/creating-and-testing-extension-packages.md) para saber como o AppXs é criado e empacotar manualmente a extensão ou ir para a rota mais fácil e ir para [usar o ManifoldJS para extensões de pacote](./packaging/using-ManifoldJS-to-package-extensions.md).

> [!NOTE]
> Depois que tiver chegado para nós e tiver sido aprovado para ter sua extensão na Microsoft Store, confira a lista de [verificação de envio de aplicativo](https://docs.microsoft.com/windows/uwp/publish/app-submissions).


## [Criando e testando pacotes de extensão](./packaging/creating-and-testing-extension-packages.md)

Esta seção do guia percorre a criação manual do pacote de extensão após a [configuração da sua conta de desenvolvedor do Windows e reservava o nome (s) da extensão](./packaging/extensions-in-the-windows-Dev-Center.md). Se você está curioso para ver os detalhes mais finos do empacotamento de uma extensão, faça uma leitura.

Também está incluída informações sobre como [testar e descompactar uma extensão empacotada](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package). Essas informações são relevantes mesmo que você tenha saído da rota de embalagem do ManifoldJS.

## [Localizando pacotes de extensão](./packaging/localizing-extension-packages.md)
A etapa de localização do pacote cai entre a criação do arquivo appxmanifest. xml e a execução do comando final para empacotar a extensão.
Isso permite que você indique quais idiomas são compatíveis com as suas extensões na listagem da Microsoft Store e em qual idioma o nome da extensão é exibido no Windows.

Você pode ir para [localizar o nome e a descrição da Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) nesta seção do guia se a extensão não oferecer suporte a vários idiomas.

## [Usar o ManifoldJS para extensões de pacote](./packaging/using-ManifoldJS-to-package-extensions.md)

A rota da ferramenta para empacotar sua extensão, o ManifoldJS irá empacotar a extensão em um encaixe com o mínimo de esforço no seu fim. Forneça alguns ativos Windows/Microsoft Store após preencher algumas propriedades de AppXManifest, e sua extensão será empacotada em qualquer momento.

Depois que sua extensão estiver empacotada, consulte a seção [teste](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de como criar e testar a extensão do Microsoft Edge para saber como Sideload-la ou desempacotá-la.


## [Executando o kit de certificação de aplicativos Windows](./packaging/running-the-windows-app-certification-kit.md)

Depois que você tiver uma extensão empacotada, poderá executá-la por meio do kit de certificação de aplicativos Windows. Isso fará com que vários testes sejam executados em seu pacote de extensão para garantir que ele esteja pronto para a Microsoft Store.
