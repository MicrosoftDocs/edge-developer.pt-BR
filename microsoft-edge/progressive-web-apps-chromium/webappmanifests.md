---
title: Usar o manifesto do aplicativo Web para integrar seu aplicativo Web progressivo ao sistema operacional
description: Saiba como usar o manifesto do aplicativo Web para integrar seu aplicativo Web progressivo ao sistema operacional.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659290"
---
# Usar o manifesto do aplicativo Web para integrar seu aplicativo Web progressivo ao sistema operacional

Um manifesto de aplicativo Web de um site rege a aparência do seu aplicativo Web progressivo \ (PWA \) e se comporta quando instalado em um dispositivo.  No nível mais básico, o manifesto fornece detalhes sobre o nome do seu aplicativo, ícones a serem usados para representar seu aplicativo em menus do sistema e as cores do tema que o sistema operacional \ (OS \) usa na barra de título.  O manifesto também permite desbloquear recursos avançados que permitem que seu aplicativo se comporte como outros aplicativos nativos no sistema.  

## Usar atalhos para fornecer acesso rápido aos recursos  

A maioria dos sistemas operacionais fornece acesso rápido aos principais recursos do aplicativo usando atalhos no menu de contexto conectado ao ícone do aplicativo.  Para usar atalhos no PWA, inclua a `shortcuts` propriedade no manifesto do seu aplicativo Web.  O trecho de código a seguir mostra como definir um atalho em seu manifesto do aplicativo Web.  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

Quando adicionado a um manifesto completo do aplicativo Web, adicionar o trecho de código anterior habilita dois atalhos no menu de contexto no ícone do aplicativo.  O primeiro é nomeado `Play Later` e tem um ícone personalizado.  O segundo é nomeado `Subscriptions` e não tem um ícone porque a `icons` propriedade é opcional.  A `description` propriedade também é opcional e pode ser usada para fornecer informações adicionais para fins de acessibilidade.  

## Identifique o aplicativo como um destino de compartilhamento

Muitos sistemas operacionais permitem que os usuários compartilhem rapidamente links e arquivos com aplicativos nativos. Aplicativos Web progressivos também podem participar desse recurso, por meio do `share_target` membro do manifesto do aplicativo Web. Usando share_target, você define a página "ação" (semelhante a um formulário) e os parâmetros que espera que sejam passados para ele. O trecho de código a seguir mostra um exemplo de como usar `share_target` .

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

Quando adicionado ao manifesto do aplicativo Web, isso estabelece "/share.html" como a página de ação para um compartilhamento. Além disso, ele define três parâmetros que seriam passados para essa página de ação: "título", "texto" e "URL". Esses parâmetros serão armazenados nas propriedades "nome", "Descrição" e "link" do objeto [ShareData](https://wicg.github.io/web-share#dom-sharedata) . Por padrão, a página de ação recebe esses parâmetros como parte de uma solicitação GET, mas você pode especificar a solicitação `method` e a codificação \ (as `enctype` \), da mesma forma que faria em um formulário da Web.

## Consulte também  

Para saber mais sobre manifestos do aplicativo Web, consulte a lista de tópicos relacionados a seguir.  

* [Manifestos do aplicativo Web][MDNWebAppManifests]  
* [Destino do compartilhamento da Web][WICGShareTarget]
* [Compartilhamento na Web][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestos do aplicativo Web | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "API de destino do compartilhamento da Web | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API de compartilhamento na Web | WICG"
