---
title: Usar Os Funcionários de Serviço para gerenciar solicitações de rede e notificações por push
description: Os Trabalhadores do Serviço são Web Workers que ajudam a melhorar o desempenho, responder a diferentes condições de rede e aumentar a conectividade com seu aplicativo Web.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Borda, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 314acbbd5a2f423c274f92e815b2be4329ace9b8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399131"
---
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a>Usar Os Funcionários de Serviço para gerenciar solicitações de rede e notificações por push

Os Trabalhadores do Serviço são um tipo especial de Web Worker com a capacidade de interceptar, modificar e responder a todas as solicitações de rede usando a `Fetch` API.  Os funcionários de serviço podem acessar a API e os armazenamentos de dados assíncronos do lado do cliente, como `Cache` , para armazenar `IndexedDB` recursos.  

## <a name="registering-a-service-worker"></a>Registrando um trabalhador de serviço  

Semelhante a outros Trabalhadores da Web, os Trabalhadores do Serviço devem existir em um arquivo separado. Você faz referência a esse arquivo ao registrar o Trabalhador do Serviço, conforme mostrado no trecho de código a seguir.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Os navegadores modernos oferecem diferentes níveis de suporte para Os Trabalhadores do Serviço. Como tal, é uma boa prática testar a existência do objeto antes de executar qualquer código relacionado `serviceWorker` ao Trabalhador do Serviço. No trecho de código acima, um Trabalhador de Serviço é registrado usando o arquivo localizado na `serviceworker.min.js` raiz do site. Verifique se o arquivo JavaScript que define o Seu Trabalhador de Serviço existe no diretório de nível mais alto que você deseja que ele gerencie \(que é chamado de escopo do Service Worker\).  No trecho de código anterior, o arquivo é armazenado na raiz e o Trabalhador do Serviço gerencia todas as páginas no domínio. Se o arquivo de Trabalho de Serviço estivesse armazenado em um diretório, o escopo do Service Worker seria o `js` `js` diretório e quaisquer subdireções.  Como prática prática prática, coloque o arquivo de Trabalhador do Serviço na raiz do seu site, a menos que você precise reduzir o escopo do seu Serviço de Trabalho.  

## <a name="the-service-worker-lifecycle"></a>O ciclo de vida do Trabalhador do Serviço  

O ciclo de vida de um Trabalhador de Serviço consiste em várias etapas, com cada etapa disparando um evento. Você pode adicionar ouvintes a esses eventos para executar código para executar uma ação. A lista a seguir apresenta uma exibição de alto nível do ciclo de vida e eventos relacionados dos funcionários do serviço. 

1.  Registre o Trabalhador do Serviço.  
1.  O navegador baixa o arquivo JavaScript, instala o Service Worker e dispara o `install` evento. Você pode usar o evento para pré-armazenar em cache arquivos importantes e de longa duração, como arquivos CSS, arquivos JavaScript, imagens de logotipo, páginas offline e assim por diante em `install` seu site.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  O Service Worker é ativado, o que dispara o `activate` evento.  Use esse evento para limpar caches desatualizados.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  O Service Worker está pronto para ser executado quando a página é atualizada ou quando o usuário navega para uma nova página no site. Se você quiser executar o Service Worker sem esperar, use o `self.skipWaiting()` método durante o `install` evento.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  O Service Worker agora está em execução.     
    
## <a name="using-fetch-in-service-workers"></a>Usando a busca em Trabalhadores do Serviço  

O evento principal que você usa em um Service Worker é o `fetch` evento.  O evento é executado sempre que o navegador tenta acessar o conteúdo no `fetch` escopo do Service Worker. O trecho de código a seguir mostra como adicionar um ouvinte ao evento fetch.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

No manipulador, você pode controlar se uma solicitação vai para a rede, puxa do `fetch` cache e assim por diante.  A abordagem que você faz provavelmente varia de acordo com o tipo de recurso que está sendo solicitado, a frequência com que ele é atualizado e outra lógica de negócios exclusiva do seu aplicativo.  Aqui estão alguns exemplos do que você pode fazer:  

*   Se disponível, retorne uma resposta do cache, caso contrário, fallback para solicitar o recurso pela rede.  
*   Buscar um recurso da rede, armazenar em cache uma cópia e retornar a resposta.
*   Permitir que o usuário especifique uma preferência para salvar dados. 
*   Fornecer uma imagem de espaço reservado para determinadas solicitações de imagem.  
*   Gere uma resposta diretamente no Service Worker.  
    
## <a name="push-notifications"></a>Notificações por push  

Os funcionários do serviço podem fazer notificações por push para os usuários. As Notificações por Push são úteis para solicitar que os usuários reajam com seu aplicativo após algum tempo decorrido. Para obter mais informações, navegue até [Push Notifications passo a passo e demonstração][AzurewebsitesWebpushdemo].  

## <a name="see-also"></a>Veja também  

Para saber mais sobre Os Trabalhadores do Serviço, navegue até a lista a seguir de tópicos relacionados.  

*   [Fazendo com que os PWAs funcionem offline com os funcionários do Serviço][MDNPwasMakingOfflineServiceWorkers]  
*   [Como tornar as PWAs reativadas usando Notificações e Push][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web Push Notifications |  Demonstrações do Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Fazendo com que os PWAs funcionem offline com os funcionários do Serviço - PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Como tornar as PWAs reativadas usando Notificações e Push - PWAs | MDN"  
