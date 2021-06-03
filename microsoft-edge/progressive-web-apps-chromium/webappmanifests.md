---
title: Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao Sistema Operacional
description: Saiba como usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao sistema operacional.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Borda, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399096"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a>Usar o Manifesto do Aplicativo Web para integrar seu Aplicativo Web Progressivo ao Sistema Operacional

Um Manifesto do Aplicativo Web de um site rege a aparência e o comportamento do seu Aplicativo Web Progressivo \(PWA\) quando instalado em um dispositivo.  No nível mais básico, o Manifesto fornece detalhes sobre o nome do seu aplicativo, ícones a ser usado para representar seu aplicativo nos menus do sistema e as cores de tema que o sistema operacional \(OS\) usa na barra de título.  O Manifesto também permite desbloquear recursos poderosos que permitem que seu aplicativo se comporte como outros aplicativos nativos no sistema.  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a>Usar atalhos para fornecer acesso rápido aos recursos  

A maioria dos sistemas operacionais fornece acesso rápido aos principais recursos do aplicativo usando atalhos no menu de contexto conectado ao ícone do aplicativo.  Para usar atalhos em seu PWA, inclua a `shortcuts` propriedade em seu Manifesto do Aplicativo Web.  O trecho de código a seguir exibe como definir um atalho no manifesto do aplicativo Web.  

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

Quando adicionado a um Manifesto completo do Aplicativo Web, a adição do trecho de código anterior habilita dois atalhos no menu de contexto no ícone do aplicativo.  O primeiro é nomeado `Play Later` e tem um ícone personalizado.  O segundo é nomeado `Subscriptions` e não tem um ícone porque a propriedade é `icons` opcional.  A `description` propriedade também é opcional e pode ser usada para fornecer informações adicionais para fins de acessibilidade.  

## <a name="identify-your-app-as-a-share-target"></a>Identificar seu aplicativo como um Destino de Compartilhamento

Muitos sistemas operacionais permitem que os usuários compartilhem rapidamente links e arquivos com aplicativos nativos. Os Aplicativos Web Progressivos também podem participar desse recurso, usando o `share_target` membro do Manifesto do Aplicativo Web.  Usando `share_target` , você define a página `"action"` \(semelhante a um formulário\) e os parâmetros que você espera que sejam passados para ela.  O trecho de código a seguir exibe um exemplo de como usar `share_target` .

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

Quando adicionado ao Manifesto do Aplicativo Web, isso se estabelece `"/share.html"` como a página de ação de um compartilhamento. Além disso, define três parâmetros que seriam passados para essa página de ação: `"title"` , `"text"` e `"url"` .  Esses parâmetros serão armazenados nas `"name"` propriedades , e do objeto `"description"` `"link"` [ShareData.][GitHubWicgWebShareDomSharedata]  Por padrão, a página de ação recebe os parâmetros como parte de uma solicitação GET, mas você pode especificar a solicitação e codificação \(como \), assim como faria em um `method` `enctype` formulário da Web.

## <a name="see-also"></a>Consulte também  

Para saber mais sobre Manifestos de Aplicativo Web, navegue até a lista a seguir de tópicos relacionados.  

*   [Manifestos do Aplicativo Web][MDNWebAppManifests]  
*   [Destino do Compartilhamento web][GitHubWicgWebShareTarget]
*   [Web Share][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifestos do aplicativo Web | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Web Share Target API | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Dicionário ShareData - API do Web Share | WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Api do Web Share | WICG"
