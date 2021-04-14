---
description: Uma referência abrangente para todos os recursos e comportamentos da interface do usuário do Console no Microsoft Edge DevTools.
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: adc3f6c33d6e1a2f6c7db8336c5ab803e76c3307
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483260"
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
# <a name="console-reference"></a><span data-ttu-id="db8df-104">Referência do console</span><span class="sxs-lookup"><span data-stu-id="db8df-104">Console reference</span></span>  

<span data-ttu-id="db8df-105">Este artigo é uma referência de recursos relacionados ao Console do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="db8df-105">This article is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="db8df-106">Ele supõe que você já esteja familiarizado com o uso do Console para exibir mensagens registradas e executar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="db8df-106">It assumes you're already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="db8df-107">Caso não seja, navegue até Começar a executar [JavaScript][DevtoolsConsoleConsoleJavascript] no Console e Começar a registrar [mensagens no Console][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="db8df-107">If not, navigate to [Get started with running JavaScript in the Console][DevtoolsConsoleConsoleJavascript] and [Get started with logging messages in the Console][DevtoolsConsoleConsoleLog].</span></span>  

<span data-ttu-id="db8df-108">Se você estiver procurando a referência da API em funções como `console.log()` , navegue até [Console API Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="db8df-108">If you're looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="db8df-109">Para fazer referência a funções como `monitorEvents()` , navegue até [Console Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="db8df-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="db8df-110">Abrir o Console</span><span class="sxs-lookup"><span data-stu-id="db8df-110">Open the Console</span></span>  

<span data-ttu-id="db8df-111">Você pode abrir **o Console** como uma ferramenta [no painel](#open-the-console-tool) superior ou como uma ferramenta [na Gaveta](#open-the-console-tool-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="db8df-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="db8df-112">Abra a ferramenta Console</span><span class="sxs-lookup"><span data-stu-id="db8df-112">Open the Console tool</span></span>  

<span data-ttu-id="db8df-113">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="db8df-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="A ferramenta Console" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="db8df-115">A **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="db8df-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-116">Para abrir a **ferramenta Console** no Menu [de Comando][DevtoolsCommandMenuIndex], digite e execute o comando Mostrar Console que tem o selo `Console` **Painel** ao lado dele. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="db8df-116">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Execute o comando para exibir a ferramenta Console" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="db8df-118">Execute o comando para exibir a **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="db8df-118">Run the command to display the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="db8df-119">Abra a ferramenta Console na Gaveta</span><span class="sxs-lookup"><span data-stu-id="db8df-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="db8df-120">Selecione `Esc` ou escolha Personalizar e controlar o **DevTools** \( \) e escolha `...` Mostrar a gaveta do **console.**</span><span class="sxs-lookup"><span data-stu-id="db8df-120">Select `Esc` or choose **Customize and control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar gaveta de console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="db8df-122">Mostrar gaveta de console</span><span class="sxs-lookup"><span data-stu-id="db8df-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="db8df-123">A Gaveta aparece na parte inferior da janela DevTools, com a **ferramenta Console** aberta.</span><span class="sxs-lookup"><span data-stu-id="db8df-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="A ferramenta Console na Gaveta" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="db8df-125">A **ferramenta Console** na **Gaveta**</span><span class="sxs-lookup"><span data-stu-id="db8df-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-126">Para abrir a **ferramenta Console** no Menu [de Comando][DevtoolsCommandMenuIndex], digite e execute o comando Mostrar Console que tem o selo `Console` **Drawer** ao lado dele. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="db8df-126">To open the **Console** tool from the [Command Menu][DevtoolsCommandMenuIndex], type `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Execute o comando para exibir a ferramenta **Console** na Gaveta" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="db8df-128">Execute o comando para exibir a **ferramenta Console** na **Gaveta**</span><span class="sxs-lookup"><span data-stu-id="db8df-128">Run the command to display the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="db8df-129">Configurações do Console Aberto</span><span class="sxs-lookup"><span data-stu-id="db8df-129">Open Console Settings</span></span>  

<span data-ttu-id="db8df-130">Escolha o **botão Configurações do** Console \( ![ Ícone de Configurações do Console ](../media/settings-button-icon.msft.png) \)</span><span class="sxs-lookup"><span data-stu-id="db8df-130">Choose the **Console Settings** \(![Console Settings icon](../media/settings-button-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configurações do Console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="db8df-132">Configurações do Console</span><span class="sxs-lookup"><span data-stu-id="db8df-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="db8df-133">Os links a seguir explicam cada configuração.</span><span class="sxs-lookup"><span data-stu-id="db8df-133">The following links explain each setting.</span></span>  

*   [<span data-ttu-id="db8df-134">Ocultar rede</span><span class="sxs-lookup"><span data-stu-id="db8df-134">Hide network</span></span>](#hide-network-messages)  
*   [<span data-ttu-id="db8df-135">Preservar log</span><span class="sxs-lookup"><span data-stu-id="db8df-135">Preserve log</span></span>](#persist-messages-across-page-loads)  
*   [<span data-ttu-id="db8df-136">Somente contexto selecionado</span><span class="sxs-lookup"><span data-stu-id="db8df-136">Selected context only</span></span>](#filter-out-messages-from-different-contexts)  
*   [<span data-ttu-id="db8df-137">Grupo semelhante</span><span class="sxs-lookup"><span data-stu-id="db8df-137">Group similar</span></span>](#turn-off-message-grouping)  
*   [<span data-ttu-id="db8df-138">Log XMLHttpRequests</span><span class="sxs-lookup"><span data-stu-id="db8df-138">Log XMLHttpRequests</span></span>](#log-xhr-and-fetch-requests)  
*   [<span data-ttu-id="db8df-139">Avaliação ávida</span><span class="sxs-lookup"><span data-stu-id="db8df-139">Eager evaluation</span></span>](#turn-off-eager-evaluation)  
*   [<span data-ttu-id="db8df-140">Preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="db8df-140">Autocomplete from history</span></span>](#turn-off-autocomplete-from-history)  
<!--*   Evaluate triggers user activation  -->  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="db8df-141">Abra a barra lateral do console</span><span class="sxs-lookup"><span data-stu-id="db8df-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="db8df-142">Para exibir a **barra lateral,** escolha **Mostrar barra lateral do console** \( Mostrar barra lateral do console ![ ](../media/show-console-sidebar-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="db8df-142">To display the **Sidebar**, choose **Show console sidebar** \(![Show console sidebar](../media/show-console-sidebar-icon.msft.png)\).</span></span>  <span data-ttu-id="db8df-143">A **barra lateral** ajuda você a filtrar.</span><span class="sxs-lookup"><span data-stu-id="db8df-143">The **Sidebar** is helps you filter.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra Lateral do Console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **<span data-ttu-id="db8df-145">Barra Lateral do Console</span><span class="sxs-lookup"><span data-stu-id="db8df-145">Console Sidebar</span></span>**  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="db8df-146">Exibir mensagens</span><span class="sxs-lookup"><span data-stu-id="db8df-146">View messages</span></span>  

<span data-ttu-id="db8df-147">Esta seção contém recursos que alteram a forma como as mensagens são apresentadas no Console.</span><span class="sxs-lookup"><span data-stu-id="db8df-147">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="db8df-148">Para um passo a passo hands-on, navegue até [Exibir mensagens][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].</span><span class="sxs-lookup"><span data-stu-id="db8df-148">For a hands-on walkthrough, navigate to [View messages][DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage].</span></span>  

### <a name="turn-off-message-grouping"></a><span data-ttu-id="db8df-149">Desativar o agrupamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="db8df-149">Turn off message grouping</span></span>  

<span data-ttu-id="db8df-150">Para desativar o comportamento padrão de agrupação de mensagens do **Console**, abra Configurações do [Console](#open-console-settings) e escolha a caixa de seleção ao lado de **Group similar**.</span><span class="sxs-lookup"><span data-stu-id="db8df-150">To turn off the default message grouping behavior of the **Console**, [open Console Settings](#open-console-settings) and choose the checkbox next to **Group similar**.</span></span>  <span data-ttu-id="db8df-151">Para obter um exemplo, navegue até [Log XHR e Buscar solicitações](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="db8df-151">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="db8df-152">Solicitações XHR e Fetch de log</span><span class="sxs-lookup"><span data-stu-id="db8df-152">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="db8df-153">Para registrar todas as solicitações no Console conforme cada uma acontece, abra Configurações do Console e escolha a caixa de seleção ao lado de `XMLHttpRequest` `Fetch` Log **XMLHttpRequests**. \*\*\*\* [](#open-console-settings)</span><span class="sxs-lookup"><span data-stu-id="db8df-153">To log all `XMLHttpRequest` and `Fetch` requests to the **Console** as each happens, [open Console Settings](#open-console-settings) and choose the checkbox next to **Log XMLHttpRequests**.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Solicitações de Log XMLHttpRequest e Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="db8df-155">Log `XMLHttpRequest` e `Fetch` solicitações</span><span class="sxs-lookup"><span data-stu-id="db8df-155">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-156">A mensagem superior na figura anterior exibe o comportamento de agrupação padrão do **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-156">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after you [turn off message grouping](#turn-off-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="db8df-157">Persistir mensagens entre cargas de página</span><span class="sxs-lookup"><span data-stu-id="db8df-157">Persist messages across page loads</span></span>  

<span data-ttu-id="db8df-158">Quando você carrega uma nova página da Web, a ação padrão limpa o **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-158">When you load a new webpage, the default action clears the **Console**.</span></span>  <span data-ttu-id="db8df-159">Para persistir mensagens entre cargas de página, [abra Configurações](#open-console-settings) do Console e escolha a caixa de seleção ao lado de **Preservar Log**.</span><span class="sxs-lookup"><span data-stu-id="db8df-159">To persist messages across page loads, [open Console Settings](#open-console-settings) and choose the checkbox next to **Preserve Log**.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="db8df-160">Ocultar mensagens de rede</span><span class="sxs-lookup"><span data-stu-id="db8df-160">Hide network messages</span></span>  

<span data-ttu-id="db8df-161">A ação padrão do Microsoft Edge é fazer logs de mensagens de rede no **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-161">The default action for Microsoft Edge is to logs network messages to the **Console**.</span></span>  <span data-ttu-id="db8df-162">Na figura a seguir, a mensagem escolhida representa um código de status HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="db8df-162">In the following figure, the chosen message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Uma mensagem 429 no Console" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="db8df-164">Uma `429` mensagem no **Console**</span><span class="sxs-lookup"><span data-stu-id="db8df-164">A `429` message in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-165">Para ocultar mensagens de rede, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="db8df-165">To hide network messages, complete the following actions.</span></span>  

1.  <span data-ttu-id="db8df-166">[Abra Configurações do Console](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="db8df-166">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="db8df-167">Escolha a caixa de seleção ao lado de **Ocultar Rede**.</span><span class="sxs-lookup"><span data-stu-id="db8df-167">Choose the checkbox next to **Hide Network**.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="db8df-168">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="db8df-168">Filter messages</span></span>  

<span data-ttu-id="db8df-169">Existem muitas maneiras de filtrar mensagens no **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-169">Many ways exist to filter out messages in the **Console**.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="db8df-170">Filtrar mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="db8df-170">Filter out browser messages</span></span>  

<span data-ttu-id="db8df-171">[Abra a Barra Lateral do Console e](#open-the-console-sidebar) escolha # mensagens de **usuário** para exibir apenas mensagens que vieram do JavaScript da página da Web.</span><span class="sxs-lookup"><span data-stu-id="db8df-171">[Open the Console Sidebar](#open-the-console-sidebar) and choose **# user messages** to only display messages that came from the JavaScript of the webpage.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Exibir mensagens de usuário" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="db8df-173">Exibir mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="db8df-173">Display user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="db8df-174">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="db8df-174">Filter by log level</span></span>  

<span data-ttu-id="db8df-175">O DevTools atribui a cada `console.*` método um dos quatro níveis de gravidade.</span><span class="sxs-lookup"><span data-stu-id="db8df-175">DevTools assigns each `console.*` method one of the four severity levels.</span></span>  

*   `Error`  
*   `Info`  
*   `Verbose`  
*   `Warning`  
    
<span data-ttu-id="db8df-176">Por exemplo, `console.log()` está no `Info` grupo, mas está no `console.error()` `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="db8df-176">For example, `console.log()` is in the `Info` group, but `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="db8df-177">A [Referência da API de Console][DevToolsConsoleApi] descreve o nível de gravidade de cada método aplicável.</span><span class="sxs-lookup"><span data-stu-id="db8df-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="db8df-178">Cada mensagem que o navegador registra no Console também tem um nível de severidade.</span><span class="sxs-lookup"><span data-stu-id="db8df-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="db8df-179">Você pode ocultar qualquer nível de mensagens que não esteja interessado.</span><span class="sxs-lookup"><span data-stu-id="db8df-179">You may hide any level of messages that you're not interested in.</span></span>  <span data-ttu-id="db8df-180">Por exemplo, se você só estiver interessado em `Error` mensagens, poderá ocultar os outros três grupos.</span><span class="sxs-lookup"><span data-stu-id="db8df-180">For example, if you're only interested in `Error` messages, you may hide the other three groups.</span></span>  

<span data-ttu-id="db8df-181">Para filtrar as mensagens, escolha o menu suspenso Níveis de **Log** e `Verbose` escolha , , ou `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="db8df-181">To filter the messages, choose the **Log Levels** dropdown and choose `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="O menu suspenso Níveis de Log" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="db8df-183">O **menu suspenso Níveis de** Log</span><span class="sxs-lookup"><span data-stu-id="db8df-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-184">Para usar o nível de log para filtrar, [abra](#open-the-console-sidebar) a Barra lateral do Console e escolha **Erros,** **Avisos,** **Informações**ou **Verbose**.</span><span class="sxs-lookup"><span data-stu-id="db8df-184">To use the log level to filter, [open the Console Sidebar](#open-the-console-sidebar) and then choose **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar a barra lateral para exibir avisos" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="db8df-186">Usar a barra lateral para exibir avisos</span><span class="sxs-lookup"><span data-stu-id="db8df-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="db8df-187">Filtrar mensagens por URL</span><span class="sxs-lookup"><span data-stu-id="db8df-187">Filter messages by URL</span></span>  

<span data-ttu-id="db8df-188">Digite `url:` seguido de uma URL para exibir apenas mensagens que vieram dessa URL.</span><span class="sxs-lookup"><span data-stu-id="db8df-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="db8df-189">Depois de digitar `url:` , o DevTools exibe todas as URLs relevantes.</span><span class="sxs-lookup"><span data-stu-id="db8df-189">After you type `url:`, DevTools displays all relevant URLs.</span></span>  <span data-ttu-id="db8df-190">Domínios também funcionam.</span><span class="sxs-lookup"><span data-stu-id="db8df-190">Domains also work.</span></span>  <span data-ttu-id="db8df-191">Por exemplo, se e estão registrando mensagens, permite que você se concentre nas mensagens `https://example.com/a.js` `https://example.com/b.js` desses dois `url:https://example.com` scripts.</span><span class="sxs-lookup"><span data-stu-id="db8df-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` allows you to focus on the messages from these two scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Um filtro DE URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="db8df-193">Um filtro DE URL</span><span class="sxs-lookup"><span data-stu-id="db8df-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-194">Para ocultar mensagens de uma URL, digite `-url:` .</span><span class="sxs-lookup"><span data-stu-id="db8df-194">To hide messages from a URL, type `-url:`.</span></span>  <span data-ttu-id="db8df-195">É um filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="db8df-195">It's a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Um filtro de URL negativo que oculta todas as mensagens que corresponderem à https://b.wal.co URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="db8df-197">Um filtro de URL negativo que oculta todas as mensagens que corresponderem à `https://b.wal.co` URL</span><span class="sxs-lookup"><span data-stu-id="db8df-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="db8df-198">Para exibir mensagens de uma única URL, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="db8df-198">To display messages from a single URL, complete the following actions.</span></span>  

1.  <span data-ttu-id="db8df-199">[Abra a barra lateral do console](#open-the-console-sidebar).</span><span class="sxs-lookup"><span data-stu-id="db8df-199">[Open the Console Sidebar](#open-the-console-sidebar).</span></span>  
1.  <span data-ttu-id="db8df-200">Expanda **a seção # mensagens do usuário.**</span><span class="sxs-lookup"><span data-stu-id="db8df-200">Expand the **# user messages** section.</span></span>  
1.  <span data-ttu-id="db8df-201">Escolha a URL do script que contém as mensagens nas quais você deseja se concentrar.</span><span class="sxs-lookup"><span data-stu-id="db8df-201">Choose the URL of the script that contains the messages on which you want to focus.</span></span>  
    
:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Exibir as mensagens que vieram de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="db8df-203">Exibir as mensagens que vieram</span><span class="sxs-lookup"><span data-stu-id="db8df-203">Display the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="db8df-204">Filtrar mensagens de diferentes contextos</span><span class="sxs-lookup"><span data-stu-id="db8df-204">Filter out messages from different contexts</span></span>  

<span data-ttu-id="db8df-205">Suponha que você tenha um anúncio \(ad\) em sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="db8df-205">Suppose that you have an advertisement \(ad\) on your webpage.</span></span>  <span data-ttu-id="db8df-206">O ad é incorporado em um `<iframe>` e gera muitas mensagens em seu **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-206">The ad is embedded in an `<iframe>` and generates many messages in your **Console**.</span></span>  <span data-ttu-id="db8df-207">Como o ad está sendo executado em um contexto [JavaScript](#choose-javascript-context)diferente, uma maneira de ocultar as mensagens é abrir Configurações do [Console](#open-console-settings) e escolher a caixa de seleção ao lado de **Somente Contexto Selecionado.**</span><span class="sxs-lookup"><span data-stu-id="db8df-207">Because the ad is running in a different [JavaScript context](#choose-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and choose the checkbox next to **Selected Context Only**.</span></span>  

### <a name="filter-out-messages-that-dont-match-a-regular-expression-pattern"></a><span data-ttu-id="db8df-208">Filtrar mensagens que não corresponderem a um padrão de expressão regular</span><span class="sxs-lookup"><span data-stu-id="db8df-208">Filter out messages that don't match a regular expression pattern</span></span>  

<span data-ttu-id="db8df-209">Digite uma expressão regular, como na caixa de texto Filtro, para filtrar todas as mensagens que não `/[gm][ta][mi]/` corresponderem a esse padrão. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="db8df-209">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** textbox to filter out any messages that don't match that pattern.</span></span>  <span data-ttu-id="db8df-210">O DevTools verifica se o padrão foi encontrado no texto da mensagem ou no script que fez com que a mensagem fosse registrada.</span><span class="sxs-lookup"><span data-stu-id="db8df-210">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar todas as mensagens que não corresponderem à expressão regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="db8df-212">Filtrar todas as mensagens que não corresponderem à `/[gm][ta][mi]/` expressão regex</span><span class="sxs-lookup"><span data-stu-id="db8df-212">Filter out any messages that don't match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="db8df-213">Executar JavaScript</span><span class="sxs-lookup"><span data-stu-id="db8df-213">Run JavaScript</span></span>  

<span data-ttu-id="db8df-214">Esta seção contém recursos relacionados à execução de JavaScript no **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-214">This section contains features related to running JavaScript in the **Console**.</span></span>  <span data-ttu-id="db8df-215">Para um passo a passo hands-on, navegue até [Executar JavaScript][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="db8df-215">For a hands-on walkthrough, navigate to [Run JavaScript][DevtoolsConsoleConsoleJavascript].</span></span>  

### <a name="rerun-expressions-from-history"></a><span data-ttu-id="db8df-216">Reprisar expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="db8df-216">Rerun expressions from history</span></span>  

<span data-ttu-id="db8df-217">Selecione `Up Arrow` para passar pelo histórico de expressões JavaScript que você executara anteriormente no **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-217">Select `Up Arrow` to cycle through the history of JavaScript expressions that you ran earlier in the **Console**.</span></span>  <span data-ttu-id="db8df-218">Selecione `Enter` para executar essa expressão novamente.</span><span class="sxs-lookup"><span data-stu-id="db8df-218">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="db8df-219">Assista ao valor de uma expressão em tempo real com expressões ao vivo</span><span class="sxs-lookup"><span data-stu-id="db8df-219">Watch the value of an expression in real time with Live Expressions</span></span>  

<span data-ttu-id="db8df-220">Se você estiver digitando a mesma expressão JavaScript no **Console** repetidamente, talvez seja mais fácil criar uma **expressão ao vivo.**</span><span class="sxs-lookup"><span data-stu-id="db8df-220">If you find yourself typing the same JavaScript expression in the **Console** repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="db8df-221">Com **Expressões Ao Vivo,** digite uma expressão uma vez e, em seguida, fixe-a na parte superior do **console.**</span><span class="sxs-lookup"><span data-stu-id="db8df-221">With **Live Expressions**, you type an expression once and then pin it to the top of your **Console**.</span></span>  <span data-ttu-id="db8df-222">O valor da expressão é atualizado quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="db8df-222">The value of the expression updates in near real time.</span></span>  <span data-ttu-id="db8df-223">Navegue [até Ver valores de expressão javascript em Real-Time com expressões ao vivo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="db8df-223">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="turn-off-eager-evaluation"></a><span data-ttu-id="db8df-224">Desativar a Avaliação Ávida</span><span class="sxs-lookup"><span data-stu-id="db8df-224">Turn off Eager Evaluation</span></span>  

<span data-ttu-id="db8df-225">**A Avaliação** Avida exibe uma visualização do valor de retorno à medida que você digita expressões JavaScript no **Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-225">**Eager Evaluation** displays a preview of the return value as you type JavaScript expressions in the **Console**.</span></span>  <span data-ttu-id="db8df-226">Para desativar as visualizações de valor de retorno, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="db8df-226">To turn off the return value previews, complete the following actions.</span></span>  

1.  <span data-ttu-id="db8df-227">[Abra Configurações do Console](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="db8df-227">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="db8df-228">Remova a caixa de seleção ao lado de **Avaliação Ávida**.</span><span class="sxs-lookup"><span data-stu-id="db8df-228">Remove the checkbox next to **Eager Evaluation**.</span></span>  
    
### <a name="turn-off-autocomplete-from-history"></a><span data-ttu-id="db8df-229">Desativar o preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="db8df-229">Turn off autocomplete from history</span></span>  

<span data-ttu-id="db8df-230">À medida que você digita uma expressão, a janela pop-up de preenchimento automático do **Console** exibe expressões que você fez anteriormente.</span><span class="sxs-lookup"><span data-stu-id="db8df-230">As you type out an expression, the autocomplete popup window for the **Console** displays expressions that you ran earlier.</span></span>  <span data-ttu-id="db8df-231">As expressões são pré-canetadas com o `>` caractere.</span><span class="sxs-lookup"><span data-stu-id="db8df-231">The expressions are pre-pended with the `>` character.</span></span>  <span data-ttu-id="db8df-232">Para parar de exibir expressões do seu histórico, [abra Configurações](#open-console-settings) do Console e remova a caixa de seleção ao lado de **Caixa** de seleção Preenchimento Automático do Histórico.</span><span class="sxs-lookup"><span data-stu-id="db8df-232">To stop displaying expressions from your history, [open Console Settings](#open-console-settings) and remove the checkbox next to **Autocomplete From History** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="db8df-233">Na figura a seguir, `document.querySelector('a')` e `document.querySelector('img')` são expressões avaliadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="db8df-233">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="O menu pop-up de preenchimento automático exibe expressões do histórico" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="db8df-235">O menu pop-up de preenchimento automático exibe expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="db8df-235">The autocomplete popup menu displays expressions from history</span></span>  
:::image-end:::  

### <a name="choose-javascript-context"></a><span data-ttu-id="db8df-236">Escolha contexto JavaScript</span><span class="sxs-lookup"><span data-stu-id="db8df-236">Choose JavaScript context</span></span>  

<span data-ttu-id="db8df-237">A opção padrão para o menu suspenso Contexto **JavaScript** é **superior**, que representa o contexto [de][MdnDocsGlossaryBrowsingContext] navegação da página da Web principal.</span><span class="sxs-lookup"><span data-stu-id="db8df-237">The default option for the **JavaScript Context** dropdown is **top**, which represents the [browsing context][MdnDocsGlossaryBrowsingContext] of the main webpage.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="O menu suspenso Contexto JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="db8df-239">O **menu suspenso Contexto JavaScript**</span><span class="sxs-lookup"><span data-stu-id="db8df-239">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="db8df-240">Suponha que você tenha um ad em sua página da Web incorporado em `<iframe>` um .</span><span class="sxs-lookup"><span data-stu-id="db8df-240">Suppose you have an ad on your webpage embedded in an `<iframe>`.</span></span>  <span data-ttu-id="db8df-241">Você deseja executar JavaScript para ajustar o DOM do ad.</span><span class="sxs-lookup"><span data-stu-id="db8df-241">You want to run JavaScript to tweak the DOM of the ad.</span></span>  <span data-ttu-id="db8df-242">Primeiro, escolha o contexto de navegação do ad no menu suspenso **Contexto JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="db8df-242">First, choose the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Escolha um contexto JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="db8df-244">Escolha um contexto JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="db8df-244">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="db8df-245">Limpar o Console</span><span class="sxs-lookup"><span data-stu-id="db8df-245">Clear the Console</span></span>  

<span data-ttu-id="db8df-246">Para limpar **o Console**, conclua qualquer um dos seguintes fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="db8df-246">To clear the **Console**, complete any of the following workflows.</span></span>  

*   <span data-ttu-id="db8df-247">Escolha o **botão Limpar Console** \( Limpar Console ![ ](../media/clear-console-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="db8df-247">Choose the **Clear Console** \(![Clear Console](../media/clear-console-button-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="db8df-248">Passe o mouse em uma mensagem, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Limpar Console**.</span><span class="sxs-lookup"><span data-stu-id="db8df-248">Hover on a message, open the contextual menu \(right-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="db8df-249">Insira `clear()` no Console **e** selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="db8df-249">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="db8df-250">Execute `console.clear()` a partir do JavaScript para sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="db8df-250">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="db8df-251">Selecione `Control` + `L` enquanto **o Console** está em foco.</span><span class="sxs-lookup"><span data-stu-id="db8df-251">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="db8df-252">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="db8df-252">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensagens na ferramenta Console | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Console como um ambiente JavaScript | Microsoft Docs"  
[DevtoolsConsoleIndex]: .index.md "Use o console | Microsoft Docs"  
[DevtoolsConsoleIndexInspectFilterInformationOnCurrentWebpage]: ./index.md#inspect-and-filter-information-on-the-current-webpage "Inspecionar e filtrar informações na página da Web atual | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Monitorar alterações no JavaScript usando expressões ao vivo | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  

[MdnDocsGlossaryBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> <span data-ttu-id="db8df-262">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db8df-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="db8df-263">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="db8df-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="db8df-265">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db8df-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
