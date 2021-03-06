---
description: Saiba mais sobre como você pode empacotá-la.
title: Extensões - Empacotamento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398494"
---
# <a name="packaging-microsoft-edge-extensions"></a>Empacotando extensões do Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Portanto, você finalmente concluiu sua extensão e está pronto para empacotá-la. Você pode estar se perguntando quais são as próximas etapas para obter isso nas mãos de usuários em potencial. Este guia destina-se a ensinar como fazer exatamente isso.  

O guia de empacotamento de extensão é abrangente, já que aborda tudo o que você gostaria de saber sobre empacotamento, mesmo os detalhes mais finos e abrangentes. Se você não quiser saber tudo o que há para saber sobre como empacotar sua extensão, você está com sorte. Adicionamos suporte para extensões ao ManifoldJS, uma ferramenta de Node.js de código aberto que tira a maioria dos problemas de empacotamento.  

> [!NOTE]
> No momento, enviar uma extensão do Microsoft Edge à Microsoft Store é um recurso restrito. [Entre em contato conosco com](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) suas solicitações para fazer parte da Microsoft Store e consideraremos você para uma atualização futura.  

Use o contorno do processo abaixo para mapear sua aventura de empacotamento!  

## [<a name="extensions-in-the-windows-dev-center"></a>Extensões no Centro de Desenvolvimento do Windows](./packaging/extensions-in-the-windows-dev-center.md)  

Independentemente de qual rota de criação de pacote você escolher, manual ou ManifoldJS, a primeira etapa é registrar uma conta do Desenvolvedor do Windows e reservar os nomes da extensão.  

Depois de fazer isso, você pode [](./packaging/creating-and-testing-extension-packages.md) ir para Criar e testar pacotes de extensão para saber como os AppXs são criados e empacotar manualmente sua extensão, ou ir para a rota mais fácil e ir para [Usando ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)para extensões de pacote.  

> [!NOTE]
> Depois de entrar em contato conosco e ter sido aprovado para ter sua extensão na Microsoft Store, confira a lista de verificação de [envio de aplicativos](https://docs.microsoft.com/windows/uwp/publish/app-submissions).  


## [<a name="creating-and-testing-extension-packages"></a>Criar e testar pacotes de extensão](./packaging/creating-and-testing-extension-packages.md)  

Esta seção do guia percorre a criação manual do pacote de extensão depois que você configurar sua conta do Desenvolvedor do Windows e reservou seus nomes [de extensão.](./packaging/extensions-in-the-windows-Dev-Center.md) Se você estiver curioso sobre os detalhes mais finos de empacotamento de uma extensão, leia isso.  

Também estão incluídas informações sobre como testar [e desempacotar uma extensão empacotada.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) Essas informações são relevantes mesmo que você tenha feito a rota de empacotamento ManifoldJS.  

## [<a name="localizing-extension-packages"></a>Localizando pacotes de extensão](./packaging/localizing-extension-packages.md)  

A etapa de localização do pacote se enquadra entre a criação do arquivo appxmanifest.xml e a execução do comando final para empacotar sua extensão.  
Isso permite que você indique quais idiomas suas extensões suportam na listagem da Microsoft Store e qual idioma o nome da sua extensão aparece no Windows.  

Você pode ir [para Localização de nome](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) e descrição para a Microsoft Store nesta seção do guia se sua extensão não dá suporte a vários idiomas.  

## [<a name="using-manifoldjs-to-package-extensions"></a>Usar ManifoldJS para extensões de pacote](./packaging/using-ManifoldJS-to-package-extensions.md)  

A rota da ferramenta para empacotar sua extensão, ManifoldJS empacota sua extensão em um snap com o mínimo esforço em sua extremidade. Forneça alguns ativos da Windows/Microsoft Store depois de preencher algumas propriedades do AppXManifest e sua extensão será empacotada em pouco tempo.  

Depois que sua extensão for [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) empacotada, consulte a seção de teste de Criação e teste da extensão do Microsoft Edge para saber como fazer sideload ou desempacotar.  

## [<a name="running-the-windows-app-certification-kit"></a>Executar o Kit de Certificação de Aplicativos Windows](./packaging/running-the-windows-app-certification-kit.md)  

Depois de ter uma extensão empacotada, você pode, em seguida, execute-a por meio do Kit de Certificação de Aplicativos do Windows. Isso executará vários testes no pacote de extensão para garantir que ele esteja pronto para a Microsoft Store.  
