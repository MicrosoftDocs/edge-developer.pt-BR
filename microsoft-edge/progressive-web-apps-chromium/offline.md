---
title: Suporte a conectividade offline e de rede em aplicativos Web progressivos
description: Saiba como usar tecnologias de suporte para criar experiências resilientes para atender às diferentes condições da rede.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 58ffb8e9ae596dec4b99143a3061995a6598ce44
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659304"
---
# Suporte a conectividade offline e de rede em aplicativos Web progressivos

Por muitos anos, as organizações se relutam em investir muito em software baseado na Web em um software nativo porque os aplicativos da Web dependem de conexões de rede estáveis. Hoje, a plataforma da Web agora oferece opções robustas que permitem aos usuários continuarem a trabalhar, mesmo se a conexão de rede ficar instável ou ficar completamente offline.

## Usar o cache para melhorar o desempenho do PWAs

Com a introdução de [trabalhadores de serviço][MDNServiceWorker], a plataforma da Web adicionou a `Cache` API para fornecer acesso a recursos gerenciados em cache. Essa API baseada em promessa permite que os desenvolvedores armazenem e recuperem muitos recursos da Web, HTML, CSS, JavaScript, imagens, JSON e assim por diante. Geralmente, a API do cache é usada dentro do contexto de um trabalhador de serviço, mas também está disponível no thread principal do `window` objeto.

Um uso comum para a `Cache` API é armazenar previamente em cache recursos críticos quando um trabalhador de serviço é instalado, conforme mostrado no trecho de código a seguir.  

```javascript
self.addEventListener( "install", function( event ){
    event.waitUntil(
        caches.open( "static-cache" )
              .then(function( cache ){
            return cache.addAll([
                "/css/main.css",
                "/js/main.js",
                "/img/favicon.png",
                "/offline/"
            ]);
        })
    );
});
```  

Esse código, executado durante o evento ciclo de vida do trabalhador do serviço `install` , abre um cache chamado `static-cache` e, quando ele tem um ponteiro para o cache, adiciona quatro recursos a ele usando o `addAll()` método.  Geralmente, a abordagem é combinada com a recuperação do cache durante um `fetch` evento   

```javascript
self.addEventListener( "fetch", event => {
    const request = event.request,
                    url = request.url;
    
    // If we are requesting an HTML page.
    if ( request.headers.get("Accept").includes("text/html") ) {
        event.respondWith(
            // Check the cache first to see if the asset exists, and if it does, return the cached asset.
            caches.match( request )
                  .then( cached_result => {
                if ( cached_result ) {
                    return cached_result;
                }
                // If the asset is not in the cache, fallback to a network request for the asset, and proceed to cache the result.
                return fetch( request )
                       .then( response => {
                    const copy = response.clone();
                    // Wait until the response we received is added to the cache.
                    event.waitUntil(
                        caches.open( "pages" )
                              .then( cache => {
                            return cache.put( request, response );
                        });
                    );
                    return response;
                })
                // If the network is unavailable to make a request, pull the offline page out of the cache.
                .catch(() => caches.match( "/offline/" ));
            })
        ); // end respondWith
    } // end if HTML
});
```  

O trecho de código é executado no trabalho do serviço sempre que o navegador faz uma `fetch` solicitação para esse site. Nesse evento, há uma instrução condicional que é executada se a solicitação for para um arquivo HTML. O trabalhador do serviço verifica se o arquivo já existe em qualquer cache \ (usando o `match()` método \). Se a solicitação existir no cache, esse resultado será retornado em cache. Caso contrário, um novo `fetch` para esse recurso é executado, uma cópia da resposta é armazenada em cache para mais tarde, e a resposta é retornada. Se a `fetch` rede falhar porque a rede está indisponível, a página offline será retornada do cache.

Esta introdução simples mostra como usar o cache em seu aplicativo Web progressivo (PWA). Cada PWA é diferente e pode usar estratégias de cache diferentes. Seu código pode parecer diferente, e você pode usar estratégias de cache diferentes para rotas diferentes no mesmo aplicativo.

## Use o IndexedDB no seu PWA para armazenar dados estruturados

`IndexedDB` é uma API para armazenar dados estruturados. Semelhante à `Cache` API, ele também é assíncrono, o que significa que você pode usá-lo no thread principal ou em funcionários da Web, como funcionários de serviço. Use a `IndexedDB` API para armazenar uma quantidade significativa de dados estruturados no cliente ou dados binários, como objetos de mídia criptografados. Para obter mais informações, consulte [MDN Primer on using IndexedDB][MDNIndexeddbApiUsing].

## Entender as opções de armazenamento para PWAs

Às vezes, você pode precisar armazenar pequenas quantidades de dados para fornecer uma melhor experiência offline para seus usuários. Se esse for o caso, você pode encontrar a simplicidade do sistema de par de valor chave do armazenamento na Web para atender às suas necessidades.  

> [!IMPORTANT]
> O armazenamento da Web é um processo síncrono e não está disponível para uso em threads de trabalho, como funcionários de serviço. Uso pesado pode criar problemas de desempenho para seu aplicativo. 


Há dois tipos de armazenamento na Web: `localStorage` e `sessionStorage` . Cada um é mantido como um repositório de dados separado isolado para o domínio que o criou. `sessionStorage` persiste apenas pela duração da sessão de navegação (por exemplo, enquanto o navegador está aberto, o que inclui atualização e restaurações). `localStorage` persiste até que os dados sejam removidos pelo código, pelo usuário ou pelo navegador (por exemplo, quando houver armazenamento limitado disponível). O trecho de código a seguir mostra como usar `localStorage` , o que é semelhante ao `sessionStorage` usado.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Este trecho de código captura metadados sobre a página atual e armazena-os em um objeto JavaScript. Em seguida, ele armazena esse valor como JSON em `localStorage` uso do `setItem()` método e atribui uma chave igual à `window.location` URL atual. Você pode recuperar as informações `localStorage` usando o `getItem()` método. 

O trecho de código a seguir mostra como usar o armazenamento em cache `localstorage` para enumerar páginas armazenadas em cache e extrair metadados para executar uma tarefa, como criar uma lista de links.

```javascript
caches.open( "pages" )
      .then( cache => {
    cache.keys()
         .then( keys => {
        if ( keys.length )
        {
            keys.forEach( insertOfflineLink );
        }
    })
});

function insertOfflineLink( request ) {
    var data = JSON.parse( localStorage.getItem( request.url ) );
    // If data exists and this page is not an offline page, assuming that offline pages have the word offline in the URL.
    if ( data && request.url.indexOf('offline') < 0  )
    {
        // Build a link and insert it into the page.
    }
}
```  

O `insertOfflineLink()` método passa a URL da solicitação para o `localStorage.getItem()` método para recuperar os metadados armazenados. Os dados recuperados são verificados para ver se ele existe e, em caso afirmativo, uma ação pode ser tomada nos dados, como a criação e a inserção da marcação para exibi-la.

## Testar conexões de rede no PWA

Além de armazenar informações para uso offline, é útil saber quando uma conexão de rede está disponível para sincronizar dados ou informar aos usuários que o status da rede foi alterado. Use as opções a seguir para testar a conectividade de rede.

### Navigator. onLine  

A `navigator.onLine` propriedade é um booliano que permite que você saiba o status atual da rede. Se o valor for `true` , o usuário estará online, caso contrário, o usuário estará offline.

### Eventos online e offline  

Saber se a rede está disponível é útil, mas você pode querer fazer uma ação quando a conectividade da rede mudar. Nessa situação, talvez você queira ouvir e executar ações em resposta a eventos de rede. Os eventos estão disponíveis nos `window` elementos, `document` e `document.body` como exibidos no trecho de código a seguir.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## Consulte também  

Para saber mais sobre como gerenciar cenários offline, consulte as páginas a seguir.  

*   [Cache][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Trabalhador do serviço][MDNServiceWorker]  
*   [Armazenamento na Web][MDNWebStorageApi]  
*   [Navigator. onLine][MDNNavigatoronline]  
*   [Eventos online e offline][MDNNavigatoronlineOfflineEvents]  
*   [Solicitação com intuito: estratégias de cache na época de PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]

<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando a API IndexDb-IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "Serviço de serviço | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "API de armazenamento da Web | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Eventos online e offline-NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Como ficar offline por Jeremy Keith | Um livro distante"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Solicitação com intuito: estratégias de cache na época de PWAs por Aaron Gustafson | Uma lista separada"  
