---
description: Tudo sobre melhorias do Serviço de Trabalho e como usar cada um deles.
title: Melhorias do Service Worker
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, service worker, PWA
ms.openlocfilehash: 2f32155d1d28d1e65ad29abfe58a414f3e3c6ed7
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387280"
---
# <a name="service-worker-improvements"></a>Melhorias do Service Worker  

Este artigo ensina sobre melhorias nas [][MdnServiceWorkerApi] ferramentas de desenvolvedor para trabalhar com funcionários de serviço e as solicitações de rede que passam por cada uma delas.  As **melhorias dos funcionários de** serviço estão nas **ferramentas Rede,** **Aplicativo** **e Fontes.**  As melhorias simplificam as tarefas a seguir.  

*   Depuração com base nas linhas do tempo do Trabalhador do Serviço.  
    *   O início de uma solicitação e a duração da inicialização.  
    *   Atualizar para o registro do trabalhador do serviço.  
    *   O tempo de execução de uma solicitação usando o [manipulador de eventos de busca.][MdnFetchEvent]  
    *   O tempo de execução de todos os eventos de busca para carregar um cliente.  
*   Explore os detalhes do tempo de execução de manipuladores de eventos de busca, instale manipuladores de eventos e ative manipuladores de eventos.  
*   Entrar e sair do manipulador de eventos de busca com informações [de script de página.](#sources)  
    
As experiências abrangem três ferramentas de desenvolvedor diferentes.  

1.  A [ferramenta Rede.](#network)  Escolha uma solicitação de rede que seja executado por um trabalhador do serviço e acesse a linha do tempo correspondente do trabalhador do serviço na **ferramenta Timing.**  
1.  A [ferramenta Application.](#application)  Para depurar os funcionários do serviço, navegue até a **ferramenta Trabalhadores do** Serviço.  
1.  A [ferramenta Sources.](#sources)  Acessar informações de script de página ao entrar em busca de manipuladores de eventos.  
    
## <a name="network"></a>Rede  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Linha do tempo do trabalho de serviço na ferramenta Rede" lightbox="../media/sw-network-timeline.msft.png":::
   Exibição de rede  
:::image-end:::  

Para acessar os recursos de depuração de funcionários de serviço na **ferramenta Rede,** conclua uma das seguintes ações.  

*   Acesse diretamente na **ferramenta Rede.**  
*   Iniciado na ferramenta **Aplicativo.**  
    
### <a name="request-routing"></a>Roteamento de solicitação  

Para facilitar a visualização do roteamento de solicitações, os cronogramas agora exibem a start-up do serviço de trabalho e os `respondWith` eventos de busca.  Para depurar e visualizar uma solicitação de rede que passou por um funcionário do serviço, conclua as seguintes ações.  

1.  Escolha a solicitação de rede que passou por um trabalhador de serviço.  
1.  Abra a **ferramenta Timing.**  
    
### <a name="fetch-events"></a>Buscar eventos  

Para saber mais sobre os eventos de busca, escolha a seta `respondWith` listada à esquerda do `respondWith` .  Para encontrar mais detalhes sobre a **Solicitação Original** **e Resposta Recebida,** use as setas listadas correspondentes.  

## <a name="application"></a>Aplicativo  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Exibição de aplicativo" lightbox="../media/sw-application-timeline.msft.png":::
   Exibição de aplicativo  
:::image-end:::  

### <a name="service-worker-update-timeline"></a>Linha do tempo de atualização do trabalhador do serviço  

A equipe do Microsoft Edge DevTools adicionou uma linha do tempo na ferramenta **Application** para refletir o ciclo de vida da atualização do trabalhador do serviço.  Ele exibe os eventos de instalação e ativação.  Cada um dos eventos tem uma seta de menu suspenso correspondente para dar mais detalhes.  

### <a name="request-routing-and-fetch-events"></a>Solicitar eventos de roteamento e busca  

Agora você pode acessar as linhas do tempo de trabalho do serviço por meio **da ferramenta Rede** na gaveta do console.  O recurso beneficia o desempenho, minimiza a duplicação da interface do usuário e cria uma experiência de depuração mais abrangente.  

1.  Abra o serviço que você está depurando.  
1.  Escolha o **botão Rede** para abrir a experiência [de roteamento de solicitação](#network).  
1.  Use os **menus suspensos respondWith** para buscar informações de solicitação de evento e resposta.  

A **ferramenta Rede** exibe as solicitações de rede que passaram pelo trabalhador do serviço que você está depurando.  O filtro automático é uma maneira de restringir sua exploração.

## <a name="sources"></a>Fontes  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Exibição DOM" lightbox="../media/sw-sources.msft.png":::
   Exibição DOM  
:::image-end:::  

Para encontrar mais informações de pilha, de definir um ponto de quebra no manipulador de busca.  Os detalhes levam a onde o recurso é solicitado no script da página.  Quando o depurador pausa dentro de um manipulador de busca, uma informação de pilha combinada é exibida no painel à direita.  Depois disso, você pode se mover nos quadros de pilha.  

### <a name="future-work"></a>Trabalho futuro  

A equipe do Microsoft Edge DevTools planeja desenvolver ainda mais os detalhes do cache e está investigando mais maneiras de melhorar a experiência de depuração de funcionários de serviço para desenvolvedores [de Aplicativo Web Progressivo.][MdnProgressiveWebApps]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicativos Web progressivos (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de Trabalho de Serviço | MDN"  
