---
description: Use o painel do aplicativo para inspecionar, modificar e depurar manifestos do aplicativo Web, trabalhos de serviço e caches de trabalho do serviço.
title: Depurar aplicativos Web progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 80475ebcbbdd3fb04fd0196e993c933e0bdcf090
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125388"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="6c77a-104">Depurar aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="6c77a-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="6c77a-105">Use o painel do **aplicativo** para inspecionar, modificar e depurar manifestos do aplicativo Web, trabalhos de serviço e caches de trabalho do serviço.</span><span class="sxs-lookup"><span data-stu-id="6c77a-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="6c77a-106">Este guia apenas descreve os recursos do aplicativo Web progressivo do painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="6c77a-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <span data-ttu-id="6c77a-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="6c77a-107">Summary</span></span>  

*   <span data-ttu-id="6c77a-108">Use o painel **manifestar** para inspecionar seu manifesto do aplicativo Web e disparar adicionar a eventos tela inicial.</span><span class="sxs-lookup"><span data-stu-id="6c77a-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="6c77a-109">Use o painel **trabalhadores do serviço** para uma variedade completa de tarefas relacionadas ao trabalhador, como cancelar o registro ou a atualização de um serviço, a emulação de eventos Push, o offline ou a interrupção de um trabalhador de serviço.</span><span class="sxs-lookup"><span data-stu-id="6c77a-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="6c77a-110">Exiba o cache do serviço de trabalho no painel **armazenamento do cache** .</span><span class="sxs-lookup"><span data-stu-id="6c77a-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="6c77a-111">Cancele o registro de um trabalhador de serviço e limpe todos os armazenamentos e caches com um único clique de botão no painel **limpar armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="6c77a-111">Unregister a service worker and clear all storage and caches with a single button click from the **Clear storage** pane.</span></span>  
    
## <span data-ttu-id="6c77a-112">Manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="6c77a-112">Web app manifest</span></span>  

<span data-ttu-id="6c77a-113">Se você quiser que os usuários possam adicionar seu aplicativo à sua homescreens móvel, você precisará de um manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="6c77a-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="6c77a-114">O manifesto define como o aplicativo é exibido no tela inicial, onde direcionar o usuário ao iniciar a partir do tela inicial e como é a aparência do aplicativo durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="6c77a-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="6c77a-115">Depois de configurar o manifesto, você pode usar o painel **manifesto** do painel do **aplicativo** para inspecioná-lo.</span><span class="sxs-lookup"><span data-stu-id="6c77a-115">After you have your manifest set up, you can use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="Painel de manifesto" lightbox="./media/manifest-pane.msft.png":::
   <span data-ttu-id="6c77a-117">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="6c77a-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="6c77a-118">Para ver a origem do manifesto, clique no link abaixo do rótulo do **manifesto do aplicativo** \ ( `https://airhorner.com/manifest.json` na figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="6c77a-118">To look at the manifest source, click the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="6c77a-119">As seções de **identidade** e **apresentação** só exibem os campos da fonte de manifesto em uma tela mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="6c77a-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="6c77a-120">A seção **ícones** exibe todos os ícones que você especificou.</span><span class="sxs-lookup"><span data-stu-id="6c77a-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Painel de manifesto" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <span data-ttu-id="6c77a-121">Profissionais de serviço</span><span class="sxs-lookup"><span data-stu-id="6c77a-121">Service workers</span></span>  

<span data-ttu-id="6c77a-122">Os funcionários de serviço são uma tecnologia fundamental na próxima plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="6c77a-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="6c77a-123">Eles são scripts que o navegador executa em segundo plano, separado de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="6c77a-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="6c77a-124">Esses scripts permitem que você acesse recursos que não precisam de uma página da Web ou interação do usuário, como notificações por push, sincronização em segundo plano e experiências offline.</span><span class="sxs-lookup"><span data-stu-id="6c77a-124">These scripts enable you to access features that don't need a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="6c77a-125">O painel de **trabalhadores de serviço** no painel de **aplicativos** é o local principal no devtools para inspecionar e depurar trabalhadores de serviço.</span><span class="sxs-lookup"><span data-stu-id="6c77a-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="Painel de manifesto" lightbox="./media/service-workers-pane.msft.png":::
   <span data-ttu-id="6c77a-127">O painel **funcionários do serviço**</span><span class="sxs-lookup"><span data-stu-id="6c77a-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="6c77a-128">Se um trabalhador do serviço estiver instalado na página atualmente aberta, você verá-o listado nesse painel.</span><span class="sxs-lookup"><span data-stu-id="6c77a-128">If a service worker is installed to the currently open page, then you'll see it listed on this pane.</span></span>  <span data-ttu-id="6c77a-129">Por exemplo, na figura anterior, há um trabalho de serviço instalado para o escopo de `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="6c77a-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="6c77a-130">A caixa de seleção **offline** coloca devtools no modo offline.</span><span class="sxs-lookup"><span data-stu-id="6c77a-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="6c77a-131">Isso equivale ao modo offline disponível no painel **rede** ou na `Go offline` opção no [menu de comando][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="6c77a-131">This is equivalent to the offline mode available from the **Network** panel, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="6c77a-132">A caixa de seleção **Atualizar na recarga** força o trabalhador do serviço a atualizar em cada carregamento de página.</span><span class="sxs-lookup"><span data-stu-id="6c77a-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="6c77a-133">A caixa **de seleção Ignorar para rede** ignora o trabalhador do serviço e força o navegador a ir para a rede para obter os recursos solicitados.</span><span class="sxs-lookup"><span data-stu-id="6c77a-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="6c77a-134">O botão **Atualizar** executa uma atualização única do trabalho de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="6c77a-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="6c77a-135">O botão de **ação** emula uma notificação por push sem uma carga \ (também conhecida como **Tickle**\).</span><span class="sxs-lookup"><span data-stu-id="6c77a-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="6c77a-136">O botão **sincronizar** emula um evento de sincronização em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6c77a-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="6c77a-137">O botão **Cancelar registro** cancela o registro do trabalho de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="6c77a-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="6c77a-138">Confira o [armazenamento claro](#clear-storage) para obter uma maneira de cancelar o registro de um trabalhador de serviço e revelar armazenamento e caches com um único clique de botão.</span><span class="sxs-lookup"><span data-stu-id="6c77a-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button click.</span></span>  
*   <span data-ttu-id="6c77a-139">A linha de **origem** informa quando o trabalho de serviço atualmente em execução foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6c77a-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="6c77a-140">O link é o nome do arquivo de origem do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="6c77a-140">The link is the name of the service worker's source file.</span></span>  <span data-ttu-id="6c77a-141">Clicar no link envia você para a fonte do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="6c77a-141">Clicking on the link sends you to the service worker's source.</span></span>  
*   <span data-ttu-id="6c77a-142">A linha **status** informa o status do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="6c77a-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="6c77a-143">O número de identificação ao lado do indicador de status verde \ ( `#36` na figura anterior \) é para o trabalhador de serviço ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="6c77a-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="6c77a-144">Ao lado do status, você verá um botão **Iniciar** \ (se o trabalhador do serviço estiver parado \) ou um botão **parar** \ (se o trabalhador do serviço estiver em execução \).</span><span class="sxs-lookup"><span data-stu-id="6c77a-144">Next to the status you'll see a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\).</span></span>  <span data-ttu-id="6c77a-145">Os funcionários de serviço são projetados para serem interrompidos e iniciados pelo navegador a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="6c77a-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="6c77a-146">Parar explicitamente seu trabalho de serviço usando o botão **parar** pode simular isso.</span><span class="sxs-lookup"><span data-stu-id="6c77a-146">Explicitly stopping your service worker using the **stop** button can simulate that.</span></span>  <span data-ttu-id="6c77a-147">Parar seu trabalho de serviço é uma ótima maneira de testar como o seu código se comporta quando o trabalho do serviço começa a fazer backup novamente.</span><span class="sxs-lookup"><span data-stu-id="6c77a-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="6c77a-148">Freqüentemente, ele revela bugs devido a suposições defeituosas sobre o estado global persistente.</span><span class="sxs-lookup"><span data-stu-id="6c77a-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="6c77a-149">A linha **clientes** informa a origem para a qual o trabalhador do serviço tem escopo.</span><span class="sxs-lookup"><span data-stu-id="6c77a-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="6c77a-150">O botão **foco** é principalmente útil quando você habilita a caixa de seleção **Mostrar tudo** .</span><span class="sxs-lookup"><span data-stu-id="6c77a-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="6c77a-151">Quando essa caixa de seleção estiver habilitada, todos os trabalhos de serviço registrados serão listados.</span><span class="sxs-lookup"><span data-stu-id="6c77a-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="6c77a-152">Se você clicar no botão **foco** ao lado de um trabalhador de serviço que está sendo executado em uma guia diferente, o Microsoft Edge será focalizado nessa guia.</span><span class="sxs-lookup"><span data-stu-id="6c77a-152">If you click on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="6c77a-153">Se o trabalhador do serviço causar algum erro, um novo rótulo chamado **erros** aparecerá.</span><span class="sxs-lookup"><span data-stu-id="6c77a-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Painel de manifesto" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <span data-ttu-id="6c77a-154">Caches de funcionários do serviço</span><span class="sxs-lookup"><span data-stu-id="6c77a-154">Service worker caches</span></span>  

<span data-ttu-id="6c77a-155">O painel **armazenamento de cache** fornece uma lista somente leitura de recursos que foram armazenados em cache usando a API de [cache][MDNWebCacheAPI]\ (serviço de trabalho \).</span><span class="sxs-lookup"><span data-stu-id="6c77a-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Painel de manifesto" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="6c77a-157">Painel **armazenamento do cache**</span><span class="sxs-lookup"><span data-stu-id="6c77a-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6c77a-158">Na primeira vez que você abre um cache e adiciona um recurso a ele, a DevTools pode não detectar a alteração.</span><span class="sxs-lookup"><span data-stu-id="6c77a-158">The first time you open a cache and add a resource to it, DevTools might not detect the change.</span></span>  <span data-ttu-id="6c77a-159">Recarregue a página e você deve ver o cache.</span><span class="sxs-lookup"><span data-stu-id="6c77a-159">Reload the page and you should see the cache.</span></span>  

<span data-ttu-id="6c77a-160">Se você tiver dois ou mais caches abertos, verá-os listados abaixo do menu suspenso **armazenamento em cache** .</span><span class="sxs-lookup"><span data-stu-id="6c77a-160">If you have two or more caches open, you'll see them listed below the **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Painel de manifesto" lightbox="./media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="6c77a-162">O menu suspenso **armazenamento do cache**</span><span class="sxs-lookup"><span data-stu-id="6c77a-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <span data-ttu-id="6c77a-163">Uso da cota</span><span class="sxs-lookup"><span data-stu-id="6c77a-163">Quota usage</span></span>  

<span data-ttu-id="6c77a-164">Algumas respostas dentro do painel **armazenamento do cache** podem ser sinalizadas como "opaco".</span><span class="sxs-lookup"><span data-stu-id="6c77a-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="6c77a-165">Isso se refere a uma resposta recuperada de uma origem diferente, como de uma **CDN** ou API remota, quando o [CORS][FetchHttpCorsProtocol] não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6c77a-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="6c77a-166">Para evitar o vazamento de informações entre domínios, há um preenchimento significativo adicionado ao tamanho de uma resposta opaca usada para calcular limites de cotas de armazenamento \ (por exemplo, se uma `QuotaExceeded` exceção é acionada \) e reportada pela `navigator.storage` API.</span><span class="sxs-lookup"><span data-stu-id="6c77a-166">In order to avoid leakage of cross-domain information, there's significant padding added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="6c77a-167">Os detalhes desse preenchimento variam do navegador para o navegador, mas para o Microsoft Edge, isso significa que o **tamanho mínimo** que qualquer resposta opaca em cache única contribui para o uso geral do armazenamento é de [aproximadamente 7 megabytes][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="6c77a-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="6c77a-168">Você deve ter isso em mente ao determinar quantas respostas opacas você deseja armazenar em cache, pois você pode ter facilmente excedido as limitações de cotas de armazenamento muito antes do que você esperaria com base no tamanho real dos recursos opacos.</span><span class="sxs-lookup"><span data-stu-id="6c77a-168">You should keep this in mind when determining how many opaque responses you want to cache, since you could easily exceeded storage quota limitations much sooner than you'd otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="6c77a-169">Guias relacionados:</span><span class="sxs-lookup"><span data-stu-id="6c77a-169">Related Guides:</span></span>  

*   [<span data-ttu-id="6c77a-170">Estouro de pilha: quais limitações se aplicam às respostas opacas?</span><span class="sxs-lookup"><span data-stu-id="6c77a-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <span data-ttu-id="6c77a-171">Limpar armazenamento</span><span class="sxs-lookup"><span data-stu-id="6c77a-171">Clear storage</span></span>  

<span data-ttu-id="6c77a-172">O painel **limpar armazenamento** é um recurso muito útil ao desenvolver aplicativos Web progressivos.</span><span class="sxs-lookup"><span data-stu-id="6c77a-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="6c77a-173">Esse painel permite cancelar o registro de trabalhadores do serviço e limpar todos os caches e armazenamento com um único clique de botão.</span><span class="sxs-lookup"><span data-stu-id="6c77a-173">This pane lets you unregister service workers and clear all caches and storage with a single button click.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <span data-ttu-id="6c77a-174">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6c77a-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "796060 problema de Chromium: o valor de armazenamento em cache aumenta em cada atualização quando o código analítico está em HTML"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "APIs da Web em cache | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Estouro de pilha: quais limitações se aplicam às respostas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="6c77a-179">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="6c77a-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6c77a-180">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6c77a-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6c77a-182">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6c77a-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
