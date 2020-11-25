---
description: Tudo sobre os aprimoramentos do trabalho do serviço e como usar cada um deles.
title: Melhorias do trabalho do serviço
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, trabalhador do serviço, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190019"
---
# Melhorias do trabalho do serviço  

Este artigo ensina melhorias para os [funcionários do serviço][MdnServiceWorkerApi] e as solicitações de rede que passam por cada um deles.  As **melhorias de trabalho do serviço** estão nas ferramentas de **rede**, **aplicativo**e **fontes** .  Os aprimoramentos incluem as seguintes tarefas.  

*   Depuração com base em cronogramas do trabalhador do serviço.  
    *   O início de uma solicitação e duração da inicialização.  
    *   Atualize para o registro de trabalhador do serviço.  
    *   O tempo de execução de uma solicitação usando o manipulador de [eventos FETCH][MdnFetchEvent] .  
    *   O tempo de execução de todos os eventos de busca para carregar um cliente.  
*   Explore os detalhes do tempo de execução de busca de manipuladores de eventos, instale manipuladores de eventos e ative manipuladores de eventos.  
*   Depuração dentro e fora do manipulador de eventos FETCH com [informações de script de página](#sources).  

As experiências se estendem por três ferramentas de desenvolvedor diferentes.  

1.  A ferramenta [rede](#network) .  Escolha uma solicitação de rede que seja executada por meio de um trabalhador de serviço e acesse a linha do tempo correspondente do trabalho de serviço na ferramenta de **intervalo** .  
1.  A ferramenta do [aplicativo](#application) .  Para depurar os trabalhadores do serviço, navegue até a ferramenta **trabalhadores do serviço** .  
1.  A ferramenta [fontes](#sources) .  Acessar informações de script de página ao entrar em busca de manipuladores de eventos de busca.  

## Rede  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Linha do tempo de trabalho do serviço na ferramenta de rede" lightbox="../media/sw-network-timeline.msft.png":::
   Tela de rede  
:::image-end:::  

Para acessar os recursos de depuração de trabalho do serviço na ferramenta **rede** , execute uma das seguintes ações.  

*   Acesse diretamente na ferramenta **rede** .  
*   Iniciou na ferramenta do **aplicativo** .  
    
### Roteamento de solicitação  

Para facilitar a visualização do roteamento de solicitação, os cronogramas agora exibem os eventos de início e busca do trabalho do serviço `respondWith` .  Para depurar e visualizar uma solicitação de rede transmitida por meio de um trabalhador de serviço, conclua as ações a seguir.  

1.  Escolha a solicitação de rede que passou por um trabalhador do serviço.  
1.  Abrir a ferramenta de **intervalo** .  
    
### Buscar eventos  

Para saber mais sobre os `respondWith` eventos de busca, escolha a seta suspensa à esquerda do `respondWith` .  Para saber mais detalhes sobre a **solicitação** e a **resposta originais recebidas**, use as setas suspensas correspondentes.  

## Aplicativo  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Visualização do aplicativo" lightbox="../media/sw-application-timeline.msft.png":::
   Visualização do aplicativo  
:::image-end:::  

### Linha do tempo de atualização de trabalho do serviço  

A equipe do Microsoft Edge DevTools adicionou uma linha do tempo na ferramenta do **aplicativo** para refletir o ciclo de vida de atualização do trabalhador do serviço.  Ele exibe os eventos de instalação e ativação.  Cada um dos eventos tem uma seta suspensa correspondente para fornecer mais detalhes.  

### Eventos de roteamento e busca de solicitação  

Agora você pode acessar o cronograma do trabalhador do serviço por meio da ferramenta **rede** na gaveta do console.  O recurso beneficia o desempenho, minimiza a duplicação da interface do usuário e cria uma experiência de depuração mais abrangente.  

1.  Abra o trabalhador do serviço que você está depurando.  
1.  Escolha o botão **rede** para abrir a [experiência de roteamento de solicitações](#network).  
1.  Use os dropdowns **respondWith** para obter informações de solicitação e resposta de eventos.  

A ferramenta **rede** exibe as solicitações de rede que passaram pelo trabalhador do serviço que você está depurando.  O filtro automático é uma maneira de restringir a exploração.

## Fontes  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Modo de exibição DOM" lightbox="../media/sw-sources.msft.png":::
   Modo de exibição DOM  
:::image-end:::  

Para encontrar mais informações sobre pilha, defina um ponto de interrupção no manipulador de busca.  Os detalhes resultam no local em que o recurso é solicitado no script de página.  Quando o depurador pausar dentro de um manipulador de busca, as informações de pilha combinadas serão exibidas no painel à direita.  Depois disso, você pode percorrer os quadros de pilha.  

### Trabalho futuro  

A equipe Microsoft Edge DevTools planeja mais desenvolver o detalhe do cache e está investigando mais maneiras de melhorar a experiência de depuração do trabalho do serviço para desenvolvedores de [aplicativos Web progressivos][MdnProgressiveWebApps] .  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicativos Web progressivos (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabalho do serviço | MDN"  
