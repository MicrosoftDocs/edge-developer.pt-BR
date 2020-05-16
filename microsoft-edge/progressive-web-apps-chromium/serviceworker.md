---
title: Usar trabalhadores de serviço para gerenciar solicitações de rede e notificações por push
description: Trabalhadores de serviço são funcionários da Web que ajudam a melhorar o desempenho, responder a variáveis de rede variáveis e aumentar a conectividade com o aplicativo Web.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicativos Web progressivos, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 9bf573b668ade351716b69965f653e05857c32ec
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659297"
---
# Usar trabalhadores de serviço para gerenciar solicitações de rede e notificações por push

Os funcionários de serviço são um tipo especial de Web Worker com a capacidade de interceptar, modificar e responder a todas as solicitações de rede usando a `Fetch` API.  Os funcionários do serviço podem acessar a `Cache` API e repositórios de dados assíncronos do lado do cliente, como `IndexedDB` , para armazenar recursos.  

## Registrando um trabalhador de serviço  

Semelhante a outros funcionários da Web, os funcionários do serviço devem existir em um arquivo separado. Você faz referência a esse arquivo ao registrar o trabalhador do serviço, conforme mostrado no trecho de código a seguir.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Navegadores modernos fornecem níveis diferentes de suporte para trabalhadores de serviço. Assim, é uma prática recomendada testar a existência do `serviceWorker` objeto antes de executar qualquer código relacionado ao trabalhador do serviço. No trecho de código acima, um trabalhador de serviço é registrado usando o `serviceworker.min.js` arquivo localizado na raiz do site. Verifique se o arquivo JavaScript que define seu trabalho de serviço existe no diretório de nível mais alto que você deseja que ele gerencie \ (que é conhecido como o escopo do trabalho do serviço \).  No trecho de código acima, o arquivo é armazenado na raiz e o trabalhador do serviço gerencia todas as páginas do domínio. Se o arquivo de trabalho do serviço foi armazenado em um `js` diretório, o escopo do trabalho do serviço seria o `js` diretório e todos os subdiretórios.  Como prática recomendada, coloque o arquivo de trabalho do serviço na raiz do seu site, a menos que você precise reduzir o escopo do trabalho do serviço.  

## O ciclo de vida do trabalho do serviço  

O ciclo de vida de um trabalhador de serviço consiste em várias etapas, com cada etapa disparando um evento. Você pode adicionar ouvintes a esses eventos para executar o código para executar uma ação. A lista a seguir apresenta uma exibição de alto nível do ciclo de vida e os eventos relacionados de trabalhadores de serviço. 

1. Registrar o trabalhador do serviço.  
1.  O navegador baixa o arquivo JavaScript, instala o trabalhador do serviço e dispara o `install` evento. Você pode usar o `install` evento para armazenar em cache todos os arquivos importantes e de longa duração, como arquivos CSS, arquivos JavaScript, imagens de logotipo, páginas offline e assim por diante do seu site.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  O trabalhador do serviço é ativado, o que dispara o `activate` evento.  Use este evento para limpar caches desatualizados.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  O trabalhador do serviço está pronto para ser executado quando a página é atualizada ou quando o usuário navega para uma nova página no site. Se você quiser executar o trabalhador do serviço sem espera, use o `self.skipWaiting()` método durante o `install` evento.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  O trabalho do serviço agora está em execução.     
    
## Usando a busca em funcionários do serviço  

O evento principal que você usa em um trabalho de serviço é o `fetch` evento.  O `fetch` evento é executado toda vez que o navegador tenta acessar o conteúdo dentro do escopo do trabalho do serviço. O trecho de código a seguir mostra como adicionar um ouvinte para o evento de busca.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Dentro do `fetch` manipulador, você pode controlar se uma solicitação vai para a rede, puxa do cache e assim por diante.  A abordagem que você pode fazer varia de acordo com o tipo de recurso que está sendo solicitado, com que frequência ele é atualizado e outras lógicas comerciais exclusivas do seu aplicativo.  Aqui estão alguns exemplos do que você pode fazer:  

*   Se disponível, retorne uma resposta do cache, caso contrário, faça fallback para solicitar o recurso pela rede.  
*   Busque um recurso da rede, armazene uma cópia em cache e retorne a resposta.
*   Permitir que o usuário especifique uma preferência para salvar os dados. 
*   Forneça uma imagem de espaço reservado para determinadas solicitações de imagem.  
*   Gerar uma resposta diretamente no trabalhador do serviço.  

## Notificações por push  

Os funcionários de serviço podem enviar notificações por push aos usuários. As notificações por push são úteis para solicitar que os usuários voltem ao seu aplicativo após algum tempo ter decorrido. Para obter mais informações, consulte [instruções passo a passo e demonstração de notificações por push][AzurewebsitesWebpushdemo].  

## Consulte também  

Para saber mais sobre trabalhadores de serviço, confira a seguinte lista de tópicos relacionados.  

*   [Como tornar o PWAs trabalhar offline com trabalhadores de serviço][MDNPwasMakingOfflineServiceWorkers]  
*   [Como fazer o PWAs ser reutilizado usando notificações e envio][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notificações por push da Web |  Demonstrações do Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Como tornar o PWAs trabalhar offline com funcionários de serviço-PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Como fazer o PWAs ser reutilizado usando notificações e PWAs | MDN"  
