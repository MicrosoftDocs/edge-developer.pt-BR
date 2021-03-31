---
description: Use o painel Aplicativo para inspecionar, modificar e depurar manifestos de aplicativo Web, funcionários de serviço e caches de funcionários do serviço.
title: Depurar aplicativos Web progressivos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398536"
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

# <a name="debug-progressive-web-apps"></a><span data-ttu-id="e6e4f-104">Depurar aplicativos Web progressivos</span><span class="sxs-lookup"><span data-stu-id="e6e4f-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="e6e4f-105">Use o **painel Aplicativo** para inspecionar, modificar e depurar manifestos de aplicativo Web, funcionários de serviço e caches de funcionários do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="e6e4f-106">Este guia discute apenas os recursos do Progressive Web App do **painel Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="e6e4f-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a><span data-ttu-id="e6e4f-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="e6e4f-107">Summary</span></span>  

*   <span data-ttu-id="e6e4f-108">Use o **painel Manifesto** para inspecionar o manifesto do aplicativo Web e disparar Adicionar a eventos homescreen.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="e6e4f-109">Use  o painel Funcionários do Serviço para uma ampla gama de tarefas relacionadas ao serviço de trabalho, como o registro ou atualização de um serviço, a emulação de eventos push, a offline ou a interrupção de um trabalhador de serviço.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="e6e4f-110">Exibir seu cache de funcionário de serviço no **painel Armazenamento de** Cache.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="e6e4f-111">Desaconselhe um funcionário de serviço e limpe todos os armazenamentos e caches com um único botão escolha no painel **Limpar armazenamento.**</span><span class="sxs-lookup"><span data-stu-id="e6e4f-111">Unregister a service worker and clear all storage and caches with a single button choose from the **Clear storage** pane.</span></span>  
    
## <a name="web-app-manifest"></a><span data-ttu-id="e6e4f-112">Manifesto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e6e4f-112">Web app manifest</span></span>  

<span data-ttu-id="e6e4f-113">Se você quiser que seus usuários sejam capazes de adicionar seu aplicativo às telas de tela inicial móveis, você precisa de um manifesto do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="e6e4f-114">O manifesto define como o aplicativo aparece na tela inicial, onde direcionar o usuário ao iniciar a partir da tela inicial e como o aplicativo se parece ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="e6e4f-115">Depois de configurar o manifesto, você pode usar o painel **Manifesto** do painel **Aplicativo** para inspecioná-lo.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-115">After you have your manifest set up, you may use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="O Painel de Manifesto" lightbox="../media/manifest-pane.msft.png":::
   <span data-ttu-id="e6e4f-117">O **Painel de** Manifesto</span><span class="sxs-lookup"><span data-stu-id="e6e4f-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="e6e4f-118">Para ver a fonte do manifesto, escolha o link abaixo rótulo **de Manifesto** do Aplicativo \( na `https://airhorner.com/manifest.json` figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="e6e4f-118">To look at the manifest source, choose the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="e6e4f-119">As **seções Identidade** e **Apresentação** exibem apenas campos da fonte de manifesto em uma exibição mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="e6e4f-120">A **seção Ícones** exibe todos os ícones especificados.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a><span data-ttu-id="e6e4f-121">Profissionais de serviço</span><span class="sxs-lookup"><span data-stu-id="e6e4f-121">Service workers</span></span>  

<span data-ttu-id="e6e4f-122">Os funcionários de serviços são uma tecnologia fundamental na plataforma Web futura.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="e6e4f-123">Eles são scripts que o navegador executa em segundo plano, separados de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="e6e4f-124">Os scripts permitem que você acesse recursos que sem a necessidade de uma página da Web ou interação do usuário, como notificações por push, sincronização em segundo plano e experiências offline.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-124">The scripts allow you to access features that without the need of a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="e6e4f-125">O **painel Trabalhadores do** Serviço no painel **Aplicativo** é o principal local no DevTools para inspecionar e depurar os funcionários do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="O painel Trabalhadores do Serviço" lightbox="../media/service-workers-pane.msft.png":::
   <span data-ttu-id="e6e4f-127">O **painel Trabalhadores do** Serviço</span><span class="sxs-lookup"><span data-stu-id="e6e4f-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="e6e4f-128">Se um trabalhador de serviço estiver instalado na página aberta no momento, ele será listado neste painel.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-128">If a service worker is installed to the currently open page, then it is listed on this pane.</span></span>  <span data-ttu-id="e6e4f-129">Por exemplo, na figura anterior, há um trabalhador de serviço instalado para o escopo de `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="e6e4f-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="e6e4f-130">A **caixa de** seleção Offline coloca o DevTools no modo offline.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="e6e4f-131">Isso equivale ao modo offline disponível na ferramenta **Rede** ou à opção `Go offline` no Menu De [comando][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="e6e4f-131">This is equivalent to the offline mode available from the **Network** tool, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="e6e4f-132">A **caixa de seleção** Atualizar ao recarregar força o trabalhador do serviço a atualizar em cada carga de página.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="e6e4f-133">A **caixa de seleção Ignorar** para rede ignora o funcionário do serviço e força o navegador a ir para a rede para recursos solicitados.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="e6e4f-134">O **botão** Atualizar executa uma atualização única do trabalhador de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="e6e4f-135">O **botão Push** emula uma notificação por push sem uma carga \(também conhecida como uma **coceira**\).</span><span class="sxs-lookup"><span data-stu-id="e6e4f-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="e6e4f-136">O **botão Sincronizar** emula um evento de sincronização em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="e6e4f-137">O **botão Não registro** no registro do funcionário de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="e6e4f-138">Confira [Limpar o armazenamento para](#clear-storage) saber como desoperdá-lo e apagar o armazenamento e os caches com um único botão escolha.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button choose.</span></span>  
*   <span data-ttu-id="e6e4f-139">A **linha Source** informa quando o funcionário do serviço em execução foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="e6e4f-140">O link é o nome do arquivo de origem do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-140">The link is the name of the source file of the service worker.</span></span>  <span data-ttu-id="e6e4f-141">A escolha no link o envia para a origem do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-141">Choosing on the link sends you to the source of the service worker.</span></span>  
*   <span data-ttu-id="e6e4f-142">A **linha Status** informa o status do trabalhador do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="e6e4f-143">O número de ID ao lado do indicador de status verde \( na figura anterior\) é para o Trabalhador `#36` de Serviço ativo no momento.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="e6e4f-144">Ao lado do status, **um** botão iniciar \(se o  trabalhador do serviço for interrompido\) ou um botão de parada \(se o trabalhador do serviço estiver em execução\) é exibido.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-144">Next to the status, a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\) is displayed.</span></span>  <span data-ttu-id="e6e4f-145">Os funcionários do serviço são projetados para serem interrompidos e iniciados pelo navegador a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="e6e4f-146">Interromper explicitamente o trabalho de serviço usando o **botão parar** pode simular isso.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-146">Explicitly stopping your service worker using the **stop** button may simulate that.</span></span>  <span data-ttu-id="e6e4f-147">Parar o seu funcionário de serviço é uma ótima maneira de testar como seu código se comporta quando o trabalhador do serviço começa a fazer o back-up novamente.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="e6e4f-148">Ele frequentemente revela bugs devido a suposições incorretas sobre o estado global persistente.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="e6e4f-149">A **linha Clientes** informa a origem para a que o trabalhador do serviço tem escopo.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="e6e4f-150">O **botão** de foco é mais útil quando você habilita a caixa de **seleção mostrar tudo.**</span><span class="sxs-lookup"><span data-stu-id="e6e4f-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="e6e4f-151">Quando essa caixa de seleção está habilitada, todos os funcionários de serviço registrados são listados.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="e6e4f-152">Se você escolher o botão **de foco** ao lado de um trabalhador de serviço que está em execução em uma guia diferente, o Microsoft Edge se concentrará nessa guia.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-152">If you choose on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="e6e4f-153">Se o trabalhador do serviço causar erros, um novo rótulo chamado **Errors** será a aparecer.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a><span data-ttu-id="e6e4f-154">Caches de funcionários de serviço</span><span class="sxs-lookup"><span data-stu-id="e6e4f-154">Service worker caches</span></span>  

<span data-ttu-id="e6e4f-155">O **painel Armazenamento de** Cache fornece uma lista somente leitura de recursos que foram armazenados em cache usando a API de Cache \(service worker\) [Cache][MDNWebCacheAPI].</span><span class="sxs-lookup"><span data-stu-id="e6e4f-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="O Painel de Armazenamento de Cache" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="e6e4f-157">O **Painel de Armazenamento de** Cache</span><span class="sxs-lookup"><span data-stu-id="e6e4f-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e6e4f-158">Na primeira vez que você abrir um cache e adicionar um recurso a ele, o DevTools pode não detectar a alteração.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-158">The first time you open a cache and add a resource to it, DevTools may not detect the change.</span></span>  <span data-ttu-id="e6e4f-159">Atualize a página e para exibir o cache.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-159">Refresh the page and to display the cache.</span></span>  

<span data-ttu-id="e6e4f-160">Se você tiver dois ou mais caches abertos, os caches serão exibidos no menu suspenso Armazenamento **de Cache** a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-160">If you have two or more caches open, the caches display under the following **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="O menu suspenso Armazenamento de Cache" lightbox="../media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="e6e4f-162">O **menu suspenso Armazenamento de** Cache</span><span class="sxs-lookup"><span data-stu-id="e6e4f-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <a name="quota-usage"></a><span data-ttu-id="e6e4f-163">Uso de cota</span><span class="sxs-lookup"><span data-stu-id="e6e4f-163">Quota usage</span></span>  

<span data-ttu-id="e6e4f-164">Algumas respostas no painel Armazenamento **de Cache** podem ser sinalizadas como "opacas".</span><span class="sxs-lookup"><span data-stu-id="e6e4f-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="e6e4f-165">Isso se refere a uma resposta recuperada de uma origem diferente, como de **uma CDN** ou API remota, quando [o CORS][FetchHttpCorsProtocol] não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="e6e4f-166">Para evitar vazamento de informações entre domínios, preenchimento significativo é adicionado ao tamanho de uma resposta opaca usada para calcular os limites de cota de armazenamento \(por exemplo, se uma exceção é lançada\) e relatada pela `QuotaExceeded` `navigator.storage` API.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-166">In order to avoid leakage of cross-domain information, significant padding is added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="e6e4f-167">Os detalhes desse preenchimento variam de navegador para navegador, mas  para o Microsoft Edge, isso significa que o tamanho mínimo que qualquer resposta opaca em cache único contribui para o uso geral do armazenamento é de aproximadamente [7 megabytes][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="e6e4f-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="e6e4f-168">Lembre-se do preenchimento ao determinar quantas respostas opacas você deseja armazenar em cache, já que você pode exceder facilmente as limitações de cota de armazenamento muito antes do esperado com base no tamanho real dos recursos opacos.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-168">Remember the padding when determining how many opaque responses you want to cache, since you may easily exceed storage quota limitations much sooner than you otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="e6e4f-169">Guias relacionados:</span><span class="sxs-lookup"><span data-stu-id="e6e4f-169">Related Guides:</span></span>  

*   [<span data-ttu-id="e6e4f-170">Stack Overflow: Quais limitações se aplicam às respostas opacas?</span><span class="sxs-lookup"><span data-stu-id="e6e4f-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a><span data-ttu-id="e6e4f-171">Limpar o armazenamento</span><span class="sxs-lookup"><span data-stu-id="e6e4f-171">Clear storage</span></span>  

<span data-ttu-id="e6e4f-172">O **painel Armazenamento Limpo** é um recurso muito útil ao desenvolver aplicativos Web progressivos.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="e6e4f-173">Esse painel permite que você desaconselhe os funcionários do serviço e desimpe todos os caches e armazenamento com um único botão escolha.</span><span class="sxs-lookup"><span data-stu-id="e6e4f-173">This pane lets you unregister service workers and clear all caches and storage with a single button choose.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e6e4f-174">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e6e4f-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Execute comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Problema Chromium 796060: o valor de armazenamento em cache aumenta em cada atualização quando o código do Analytics está no html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Cache - APIs da Web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow: Quais limitações se aplicam às respostas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="e6e4f-179">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e6e4f-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e6e4f-180">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="e6e4f-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e6e4f-182">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e6e4f-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
