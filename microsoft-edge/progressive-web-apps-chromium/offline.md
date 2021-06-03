---
title: Suporte à conectividade de rede e offline em Aplicativos Web Progressivos
description: Saiba como usar tecnologias de suporte para criar experiências resilientes para atender a diferentes condições de rede.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Borda, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 6b6031aac10161c16195c83496f8d8b5b842628e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398074"
---
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a>Suporte à conectividade de rede e offline em Aplicativos Web Progressivos

Por muitos anos, as organizações estavam relutantes em investir pesadamente em software baseado na Web em software nativo porque os aplicativos Web dependiam de conexões de rede estáveis. Hoje, a plataforma Web agora oferece opções robustas que permitem que os usuários continuem trabalhando, mesmo que a conexão de rede se torne instável ou fique completamente offline.

## <a name="use-the-caching-to-improve-performance-of-pwas"></a>Usar o cache para melhorar o desempenho de PWAs

Com a introdução dos [Trabalhadores do Serviço,][MDNServiceWorker]a plataforma Web adicionou a API para `Cache` fornecer acesso a recursos em cache gerenciados. Essa API baseada em Promessa permite que os desenvolvedores armazenem e recuperem muitos recursos da Web— HTML, CSS, JavaScript, imagens, JSON e assim por diante. Normalmente, a API de Cache é usada no contexto de um Service Worker, mas também está disponível no thread principal do `window` objeto.

Um uso comum para a API é pré-armazenar em cache recursos críticos quando um Trabalhador de Serviço é instalado, conforme mostrado no `Cache` trecho de código a seguir.  

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

Esse código, que é executado durante o evento de ciclo de vida do Trabalhador do Serviço, abre um cache chamado e, quando ele tem um ponteiro para o cache, adiciona quatro recursos a ele usando `install` `static-cache` o `addAll()` método.  Geralmente, a abordagem é aliada à recuperação de cache durante um `fetch` evento   

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

O trecho de código é executado dentro do Service Worker sempre que o navegador faz uma `fetch` solicitação para este site. Dentro desse evento, há uma instrução condicional que é executado se a solicitação for para um arquivo HTML. O Trabalhador do Serviço verifica se o arquivo já existe em qualquer cache \(usando o `match()` método\). Se a solicitação existir no cache, esse resultado em cache será retornado. Caso não seja, uma nova para esse recurso é executado, uma cópia da resposta é armazenada em cache para posteriormente `fetch` e a resposta é retornada. Se o `fetch` falha porque a rede não está disponível, a página offline é retornada do cache.

Esta introdução simples mostra como usar o cache em seu aplicativo Web progressivo (PWA). Cada PWA é diferente e pode usar estratégias de cache diferentes. Seu código pode ter uma aparência diferente e você pode usar estratégias de cache diferentes para diferentes rotas dentro do mesmo aplicativo.

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a>Use IndexedDB em sua PWA para armazenar dados estruturados

`IndexedDB` é uma API para armazenar dados estruturados. Semelhante à API, ela também é assíncrona, o que significa que você pode usá-lo no thread principal ou com Os Trabalhadores da Web, como `Cache` Os Trabalhadores do Serviço. Use a API para armazenar uma quantidade significativa de dados estruturados no cliente ou dados binários, como objetos `IndexedDB` de mídia criptografados. Para obter mais informações, navegue até [MDN primer sobre como usar IndexedDB][MDNIndexeddbApiUsing].

## <a name="understand-storage-options-for-pwas"></a>Entender as opções de armazenamento para PWAs

Às vezes, talvez seja necessário armazenar pequenas quantidades de dados para oferecer uma experiência offline melhor para seus usuários. Se esse for o caso, você poderá encontrar a simplicidade do sistema de par de valores-chave do armazenamento da Web atende às suas necessidades.  

> [!IMPORTANT]
> Web Armazenamento é um processo síncrono e não está disponível para uso em threads de trabalho, como Trabalhadores do Serviço. O uso intenso pode criar problemas de desempenho para seu aplicativo. 


Há dois tipos de web Armazenamento: `localStorage` e `sessionStorage` . Cada um é mantido como um armazenamento de dados separado isolado para o domínio que o criou. `sessionStorage` persiste apenas pela duração da sessão de navegação (por exemplo, enquanto o navegador está aberto, o que inclui atualização e restaurações). `localStorage` persiste até que os dados são removidos pelo código, pelo usuário ou pelo navegador (por exemplo, quando há armazenamento limitado disponível). O trecho de código a seguir mostra como usar `localStorage` , que é semelhante a como é `sessionStorage` usado.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Este trecho de código captura metadados sobre a página atual e armazena-a em um objeto JavaScript. Em seguida, armazena esse valor como JSON no uso do método e atribui `localStorage` uma chave igual à URL `setItem()` `window.location` atual. Você pode recuperar as informações do `localStorage` uso do `getItem()` método. 

O trecho de código a seguir mostra como usar o cache para enumerar páginas armazenadas em cache e extrair metadados para executar uma tarefa, como a criação de uma `localstorage` lista de links.

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

O `insertOfflineLink()` método passa a URL da solicitação para o método para recuperar todos os `localStorage.getItem()` metadados armazenados. Os dados recuperados são verificados para ver se eles existem e, se existirem, uma ação pode ser tomada nos dados, como a criação e inserção da marcação para exibi-los.

## <a name="test-for-network-connections-in-your-pwa"></a>Testar conexões de rede em seu PWA

Além de armazenar informações para uso offline, é útil saber quando uma conexão de rede está disponível para sincronizar dados ou informar aos usuários que o status da rede foi alterado. Use as opções a seguir para testar a conectividade de rede.

### <a name="navigatoronline"></a>navigator.onLine  

A `navigator.onLine` propriedade é um booleano que permite que você saiba o status atual da rede. Se o valor for `true` , o usuário está online, caso contrário, o usuário está offline.

### <a name="online-and-offline-events"></a>Eventos online e offline  

Saber se a rede está disponível é útil, mas talvez você queira tomar medidas quando a conectividade da rede mudar. Nessa situação, talvez você queira ouvir e tomar medidas em resposta a eventos de rede. Os eventos estão disponíveis no , e elementos conforme exibido `window` no trecho de código a `document` `document.body` seguir.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a>Consulte também  

Para saber mais sobre como gerenciar cenários offline, navegue até as páginas a seguir.  

*   [Cache][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Trabalhador do Serviço][MDNServiceWorker]  
*   [Web Armazenamento][MDNWebStorageApi]  
*   [navigator.onLine][MDNNavigatoronline]  
*   [Eventos online e offline][MDNNavigatoronlineOfflineEvents]  
*   [Solicitação com Intenção: Caching estratégias na era dos PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]
    
<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Api IndexedDB | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando IndexDb - API IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "Api Armazenamento Web | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavegadorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Eventos online e offline - NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Ficar offline por Jeremy | Um livro separado"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Solicitação com intenção: Caching estratégias na era dos PWAs por | Uma lista separada"  
