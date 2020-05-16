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
# <span data-ttu-id="f1a8d-104">Usar trabalhadores de serviço para gerenciar solicitações de rede e notificações por push</span><span class="sxs-lookup"><span data-stu-id="f1a8d-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="f1a8d-105">Os funcionários de serviço são um tipo especial de Web Worker com a capacidade de interceptar, modificar e responder a todas as solicitações de rede usando a `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="f1a8d-106">Os funcionários do serviço podem acessar a `Cache` API e repositórios de dados assíncronos do lado do cliente, como `IndexedDB` , para armazenar recursos.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <span data-ttu-id="f1a8d-107">Registrando um trabalhador de serviço</span><span class="sxs-lookup"><span data-stu-id="f1a8d-107">Registering a Service Worker</span></span>  

<span data-ttu-id="f1a8d-108">Semelhante a outros funcionários da Web, os funcionários do serviço devem existir em um arquivo separado.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="f1a8d-109">Você faz referência a esse arquivo ao registrar o trabalhador do serviço, conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="f1a8d-110">Navegadores modernos fornecem níveis diferentes de suporte para trabalhadores de serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="f1a8d-111">Assim, é uma prática recomendada testar a existência do `serviceWorker` objeto antes de executar qualquer código relacionado ao trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="f1a8d-112">No trecho de código acima, um trabalhador de serviço é registrado usando o `serviceworker.min.js` arquivo localizado na raiz do site.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="f1a8d-113">Verifique se o arquivo JavaScript que define seu trabalho de serviço existe no diretório de nível mais alto que você deseja que ele gerencie \ (que é conhecido como o escopo do trabalho do serviço \).</span><span class="sxs-lookup"><span data-stu-id="f1a8d-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="f1a8d-114">No trecho de código acima, o arquivo é armazenado na raiz e o trabalhador do serviço gerencia todas as páginas do domínio.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-114">In the above code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="f1a8d-115">Se o arquivo de trabalho do serviço foi armazenado em um `js` diretório, o escopo do trabalho do serviço seria o `js` diretório e todos os subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="f1a8d-116">Como prática recomendada, coloque o arquivo de trabalho do serviço na raiz do seu site, a menos que você precise reduzir o escopo do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <span data-ttu-id="f1a8d-117">O ciclo de vida do trabalho do serviço</span><span class="sxs-lookup"><span data-stu-id="f1a8d-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="f1a8d-118">O ciclo de vida de um trabalhador de serviço consiste em várias etapas, com cada etapa disparando um evento.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="f1a8d-119">Você pode adicionar ouvintes a esses eventos para executar o código para executar uma ação.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="f1a8d-120">A lista a seguir apresenta uma exibição de alto nível do ciclo de vida e os eventos relacionados de trabalhadores de serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1. <span data-ttu-id="f1a8d-121">Registrar o trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="f1a8d-122">O navegador baixa o arquivo JavaScript, instala o trabalhador do serviço e dispara o `install` evento.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="f1a8d-123">Você pode usar o `install` evento para armazenar em cache todos os arquivos importantes e de longa duração, como arquivos CSS, arquivos JavaScript, imagens de logotipo, páginas offline e assim por diante do seu site.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="f1a8d-124">O trabalhador do serviço é ativado, o que dispara o `activate` evento.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="f1a8d-125">Use este evento para limpar caches desatualizados.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="f1a8d-126">O trabalhador do serviço está pronto para ser executado quando a página é atualizada ou quando o usuário navega para uma nova página no site.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="f1a8d-127">Se você quiser executar o trabalhador do serviço sem espera, use o `self.skipWaiting()` método durante o `install` evento.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="f1a8d-128">O trabalho do serviço agora está em execução.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-128">The Service Worker is now running.</span></span>     
    
## <span data-ttu-id="f1a8d-129">Usando a busca em funcionários do serviço</span><span class="sxs-lookup"><span data-stu-id="f1a8d-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="f1a8d-130">O evento principal que você usa em um trabalho de serviço é o `fetch` evento.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="f1a8d-131">O `fetch` evento é executado toda vez que o navegador tenta acessar o conteúdo dentro do escopo do trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="f1a8d-132">O trecho de código a seguir mostra como adicionar um ouvinte para o evento de busca.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="f1a8d-133">Dentro do `fetch` manipulador, você pode controlar se uma solicitação vai para a rede, puxa do cache e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="f1a8d-134">A abordagem que você pode fazer varia de acordo com o tipo de recurso que está sendo solicitado, com que frequência ele é atualizado e outras lógicas comerciais exclusivas do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="f1a8d-135">Aqui estão alguns exemplos do que você pode fazer:</span><span class="sxs-lookup"><span data-stu-id="f1a8d-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="f1a8d-136">Se disponível, retorne uma resposta do cache, caso contrário, faça fallback para solicitar o recurso pela rede.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="f1a8d-137">Busque um recurso da rede, armazene uma cópia em cache e retorne a resposta.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="f1a8d-138">Permitir que o usuário especifique uma preferência para salvar os dados.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="f1a8d-139">Forneça uma imagem de espaço reservado para determinadas solicitações de imagem.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="f1a8d-140">Gerar uma resposta diretamente no trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-140">Generate a response directly in the Service Worker.</span></span>  

## <span data-ttu-id="f1a8d-141">Notificações por push</span><span class="sxs-lookup"><span data-stu-id="f1a8d-141">Push Notifications</span></span>  

<span data-ttu-id="f1a8d-142">Os funcionários de serviço podem enviar notificações por push aos usuários.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="f1a8d-143">As notificações por push são úteis para solicitar que os usuários voltem ao seu aplicativo após algum tempo ter decorrido.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="f1a8d-144">Para obter mais informações, consulte [instruções passo a passo e demonstração de notificações por push][AzurewebsitesWebpushdemo].</span><span class="sxs-lookup"><span data-stu-id="f1a8d-144">For more information, see [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <span data-ttu-id="f1a8d-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f1a8d-145">See also</span></span>  

<span data-ttu-id="f1a8d-146">Para saber mais sobre trabalhadores de serviço, confira a seguinte lista de tópicos relacionados.</span><span class="sxs-lookup"><span data-stu-id="f1a8d-146">To learn more about Service Workers, see the following list of related topics.</span></span>  

*   [<span data-ttu-id="f1a8d-147">Como tornar o PWAs trabalhar offline com trabalhadores de serviço</span><span class="sxs-lookup"><span data-stu-id="f1a8d-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="f1a8d-148">Como fazer o PWAs ser reutilizado usando notificações e envio</span><span class="sxs-lookup"><span data-stu-id="f1a8d-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notificações por push da Web |  Demonstrações do Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Como tornar o PWAs trabalhar offline com funcionários de serviço-PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Como fazer o PWAs ser reutilizado usando notificações e PWAs | MDN"  
