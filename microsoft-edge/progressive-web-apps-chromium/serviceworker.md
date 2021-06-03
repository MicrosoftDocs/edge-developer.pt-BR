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
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a><span data-ttu-id="4a379-104">Usar Os Funcionários de Serviço para gerenciar solicitações de rede e notificações por push</span><span class="sxs-lookup"><span data-stu-id="4a379-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="4a379-105">Os Trabalhadores do Serviço são um tipo especial de Web Worker com a capacidade de interceptar, modificar e responder a todas as solicitações de rede usando a `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="4a379-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="4a379-106">Os funcionários de serviço podem acessar a API e os armazenamentos de dados assíncronos do lado do cliente, como `Cache` , para armazenar `IndexedDB` recursos.</span><span class="sxs-lookup"><span data-stu-id="4a379-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <a name="registering-a-service-worker"></a><span data-ttu-id="4a379-107">Registrando um trabalhador de serviço</span><span class="sxs-lookup"><span data-stu-id="4a379-107">Registering a Service Worker</span></span>  

<span data-ttu-id="4a379-108">Semelhante a outros Trabalhadores da Web, os Trabalhadores do Serviço devem existir em um arquivo separado.</span><span class="sxs-lookup"><span data-stu-id="4a379-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="4a379-109">Você faz referência a esse arquivo ao registrar o Trabalhador do Serviço, conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a379-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="4a379-110">Os navegadores modernos oferecem diferentes níveis de suporte para Os Trabalhadores do Serviço.</span><span class="sxs-lookup"><span data-stu-id="4a379-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="4a379-111">Como tal, é uma boa prática testar a existência do objeto antes de executar qualquer código relacionado `serviceWorker` ao Trabalhador do Serviço.</span><span class="sxs-lookup"><span data-stu-id="4a379-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="4a379-112">No trecho de código acima, um Trabalhador de Serviço é registrado usando o arquivo localizado na `serviceworker.min.js` raiz do site.</span><span class="sxs-lookup"><span data-stu-id="4a379-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="4a379-113">Verifique se o arquivo JavaScript que define o Seu Trabalhador de Serviço existe no diretório de nível mais alto que você deseja que ele gerencie \(que é chamado de escopo do Service Worker\).</span><span class="sxs-lookup"><span data-stu-id="4a379-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="4a379-114">No trecho de código anterior, o arquivo é armazenado na raiz e o Trabalhador do Serviço gerencia todas as páginas no domínio.</span><span class="sxs-lookup"><span data-stu-id="4a379-114">In the previous code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="4a379-115">Se o arquivo de Trabalho de Serviço estivesse armazenado em um diretório, o escopo do Service Worker seria o `js` `js` diretório e quaisquer subdireções.</span><span class="sxs-lookup"><span data-stu-id="4a379-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="4a379-116">Como prática prática prática, coloque o arquivo de Trabalhador do Serviço na raiz do seu site, a menos que você precise reduzir o escopo do seu Serviço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="4a379-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <a name="the-service-worker-lifecycle"></a><span data-ttu-id="4a379-117">O ciclo de vida do Trabalhador do Serviço</span><span class="sxs-lookup"><span data-stu-id="4a379-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="4a379-118">O ciclo de vida de um Trabalhador de Serviço consiste em várias etapas, com cada etapa disparando um evento.</span><span class="sxs-lookup"><span data-stu-id="4a379-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="4a379-119">Você pode adicionar ouvintes a esses eventos para executar código para executar uma ação.</span><span class="sxs-lookup"><span data-stu-id="4a379-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="4a379-120">A lista a seguir apresenta uma exibição de alto nível do ciclo de vida e eventos relacionados dos funcionários do serviço.</span><span class="sxs-lookup"><span data-stu-id="4a379-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1.  <span data-ttu-id="4a379-121">Registre o Trabalhador do Serviço.</span><span class="sxs-lookup"><span data-stu-id="4a379-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="4a379-122">O navegador baixa o arquivo JavaScript, instala o Service Worker e dispara o `install` evento.</span><span class="sxs-lookup"><span data-stu-id="4a379-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="4a379-123">Você pode usar o evento para pré-armazenar em cache arquivos importantes e de longa duração, como arquivos CSS, arquivos JavaScript, imagens de logotipo, páginas offline e assim por diante em `install` seu site.</span><span class="sxs-lookup"><span data-stu-id="4a379-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="4a379-124">O Service Worker é ativado, o que dispara o `activate` evento.</span><span class="sxs-lookup"><span data-stu-id="4a379-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="4a379-125">Use esse evento para limpar caches desatualizados.</span><span class="sxs-lookup"><span data-stu-id="4a379-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="4a379-126">O Service Worker está pronto para ser executado quando a página é atualizada ou quando o usuário navega para uma nova página no site.</span><span class="sxs-lookup"><span data-stu-id="4a379-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="4a379-127">Se você quiser executar o Service Worker sem esperar, use o `self.skipWaiting()` método durante o `install` evento.</span><span class="sxs-lookup"><span data-stu-id="4a379-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="4a379-128">O Service Worker agora está em execução.</span><span class="sxs-lookup"><span data-stu-id="4a379-128">The Service Worker is now running.</span></span>     
    
## <a name="using-fetch-in-service-workers"></a><span data-ttu-id="4a379-129">Usando a busca em Trabalhadores do Serviço</span><span class="sxs-lookup"><span data-stu-id="4a379-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="4a379-130">O evento principal que você usa em um Service Worker é o `fetch` evento.</span><span class="sxs-lookup"><span data-stu-id="4a379-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="4a379-131">O evento é executado sempre que o navegador tenta acessar o conteúdo no `fetch` escopo do Service Worker.</span><span class="sxs-lookup"><span data-stu-id="4a379-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="4a379-132">O trecho de código a seguir mostra como adicionar um ouvinte ao evento fetch.</span><span class="sxs-lookup"><span data-stu-id="4a379-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="4a379-133">No manipulador, você pode controlar se uma solicitação vai para a rede, puxa do `fetch` cache e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4a379-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="4a379-134">A abordagem que você faz provavelmente varia de acordo com o tipo de recurso que está sendo solicitado, a frequência com que ele é atualizado e outra lógica de negócios exclusiva do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a379-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="4a379-135">Aqui estão alguns exemplos do que você pode fazer:</span><span class="sxs-lookup"><span data-stu-id="4a379-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="4a379-136">Se disponível, retorne uma resposta do cache, caso contrário, fallback para solicitar o recurso pela rede.</span><span class="sxs-lookup"><span data-stu-id="4a379-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="4a379-137">Buscar um recurso da rede, armazenar em cache uma cópia e retornar a resposta.</span><span class="sxs-lookup"><span data-stu-id="4a379-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="4a379-138">Permitir que o usuário especifique uma preferência para salvar dados.</span><span class="sxs-lookup"><span data-stu-id="4a379-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="4a379-139">Fornecer uma imagem de espaço reservado para determinadas solicitações de imagem.</span><span class="sxs-lookup"><span data-stu-id="4a379-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="4a379-140">Gere uma resposta diretamente no Service Worker.</span><span class="sxs-lookup"><span data-stu-id="4a379-140">Generate a response directly in the Service Worker.</span></span>  
    
## <a name="push-notifications"></a><span data-ttu-id="4a379-141">Notificações por push</span><span class="sxs-lookup"><span data-stu-id="4a379-141">Push Notifications</span></span>  

<span data-ttu-id="4a379-142">Os funcionários do serviço podem fazer notificações por push para os usuários.</span><span class="sxs-lookup"><span data-stu-id="4a379-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="4a379-143">As Notificações por Push são úteis para solicitar que os usuários reajam com seu aplicativo após algum tempo decorrido.</span><span class="sxs-lookup"><span data-stu-id="4a379-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="4a379-144">Para obter mais informações, navegue até [Push Notifications passo a passo e demonstração][AzurewebsitesWebpushdemo].</span><span class="sxs-lookup"><span data-stu-id="4a379-144">For more information, navigate to [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a379-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4a379-145">See also</span></span>  

<span data-ttu-id="4a379-146">Para saber mais sobre Os Trabalhadores do Serviço, navegue até a lista a seguir de tópicos relacionados.</span><span class="sxs-lookup"><span data-stu-id="4a379-146">To learn more about Service Workers, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="4a379-147">Fazendo com que os PWAs funcionem offline com os funcionários do Serviço</span><span class="sxs-lookup"><span data-stu-id="4a379-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="4a379-148">Como tornar as PWAs reativadas usando Notificações e Push</span><span class="sxs-lookup"><span data-stu-id="4a379-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web Push Notifications |  Microsoft Edge Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Fazendo com que os PWAs funcionem offline com os funcionários do Serviço - PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Como tornar as PWAs reativadas usando Notificações e Push - PWAs | MDN"  
