---
description: Uma referência abrangente sobre todos os recursos e comportamentos relacionados à interface do usuário do Console no Microsoft Edge DevTools.
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399159"
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

# <a name="console-reference"></a><span data-ttu-id="20b17-104">Referência do console</span><span class="sxs-lookup"><span data-stu-id="20b17-104">Console reference</span></span>  

<span data-ttu-id="20b17-105">Esta página é uma referência de recursos relacionados ao Console do Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="20b17-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="20b17-106">Ele supõe que você já está familiarizado com o uso do Console para exibir mensagens registradas e executar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="20b17-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="20b17-107">Caso não seja, navegue até [Começar a executar JavaScript][DevToolsConsoleJavascript] no console e começar a registrar [mensagens no console.][DevToolsConsoleLog]</span><span class="sxs-lookup"><span data-stu-id="20b17-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="20b17-108">Se você estiver procurando a referência da API em funções como `console.log()` , navegue até [Referência da API do Console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="20b17-108">If you are looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="20b17-109">Para fazer referência a funções como `monitorEvents()` , navegue até [Console Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="20b17-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="20b17-110">Abrir o Console</span><span class="sxs-lookup"><span data-stu-id="20b17-110">Open the Console</span></span>  

<span data-ttu-id="20b17-111">Você pode abrir **o Console** como uma ferramenta [no painel](#open-the-console-tool) superior ou como uma ferramenta [na Gaveta](#open-the-console-tool-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="20b17-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="20b17-112">Abra a ferramenta Console</span><span class="sxs-lookup"><span data-stu-id="20b17-112">Open the Console tool</span></span>  

<span data-ttu-id="20b17-113">Selecione `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="20b17-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="A ferramenta Console" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="20b17-115">A **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="20b17-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="20b17-116">Para abrir a **ferramenta Console** no Menu [de Comando,][DevToolsCommandMenu]comece a digitar e execute o comando Mostrar Console que tem o selo `Console` **Painel** ao lado dele. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="20b17-116">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="O comando para mostrar o painel console" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="20b17-118">O comando para mostrar a **ferramenta Console**</span><span class="sxs-lookup"><span data-stu-id="20b17-118">The command to show the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="20b17-119">Abra a ferramenta Console na Gaveta</span><span class="sxs-lookup"><span data-stu-id="20b17-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="20b17-120">Selecione `Escape` ou escolha Personalizar e Controlar **DevTools** \( \) e escolha `...` Mostrar gaveta do **console**.</span><span class="sxs-lookup"><span data-stu-id="20b17-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar gaveta de console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="20b17-122">Mostrar gaveta de console</span><span class="sxs-lookup"><span data-stu-id="20b17-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="20b17-123">A Gaveta aparece na parte inferior da janela DevTools, com a **ferramenta Console** aberta.</span><span class="sxs-lookup"><span data-stu-id="20b17-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="A ferramenta Console na Gaveta" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="20b17-125">A **ferramenta Console** na **Gaveta**</span><span class="sxs-lookup"><span data-stu-id="20b17-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="20b17-126">Para abrir a **ferramenta Console** no Menu [de Comando,][DevToolsCommandMenu]comece a digitar e execute o comando Mostrar Console que tem o selo `Console` **Drawer** ao lado dele. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="20b17-126">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="O comando para mostrar a ferramenta **Console** na Gaveta" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="20b17-128">O comando para mostrar a **ferramenta Console** na **Gaveta**</span><span class="sxs-lookup"><span data-stu-id="20b17-128">The command to show the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="20b17-129">Configurações do Console Aberto</span><span class="sxs-lookup"><span data-stu-id="20b17-129">Open Console Settings</span></span>  

<span data-ttu-id="20b17-130">Escolha **Configurações do** Console \( ![ Ícone de Configurações de Console ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="20b17-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configurações do Console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="20b17-132">Configurações do Console</span><span class="sxs-lookup"><span data-stu-id="20b17-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="20b17-133">Os links abaixo explicam cada configuração:</span><span class="sxs-lookup"><span data-stu-id="20b17-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="20b17-134">Ocultar Rede</span><span class="sxs-lookup"><span data-stu-id="20b17-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="20b17-135">Preservar Log</span><span class="sxs-lookup"><span data-stu-id="20b17-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="20b17-136">Somente contexto selecionado</span><span class="sxs-lookup"><span data-stu-id="20b17-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="20b17-137">Grupo Semelhante</span><span class="sxs-lookup"><span data-stu-id="20b17-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="20b17-138">Xml de logHttpRequests</span><span class="sxs-lookup"><span data-stu-id="20b17-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="20b17-139">Avaliação avida</span><span class="sxs-lookup"><span data-stu-id="20b17-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="20b17-140">Preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="20b17-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="20b17-141">Abra a barra lateral do console</span><span class="sxs-lookup"><span data-stu-id="20b17-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="20b17-142">Escolha **Mostrar Barra Lateral do Console** \( Mostrar Barra Lateral do Console \) para mostrar a Barra ![ ][ImageShowConsoleSidebarIcon] lateral, que é útil para filtragem.</span><span class="sxs-lookup"><span data-stu-id="20b17-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra Lateral do Console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="20b17-144">**Console** Barra lateral</span><span class="sxs-lookup"><span data-stu-id="20b17-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="20b17-145">Exibir mensagens</span><span class="sxs-lookup"><span data-stu-id="20b17-145">View messages</span></span>  

<span data-ttu-id="20b17-146">Esta seção contém recursos que alteram a forma como as mensagens são apresentadas no Console.</span><span class="sxs-lookup"><span data-stu-id="20b17-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="20b17-147">Para um passo a passo hands-on, navegue até [Exibir mensagens][DevToolsConsoleViewMessages].</span><span class="sxs-lookup"><span data-stu-id="20b17-147">For a hands-on walkthrough, navigate to [View messages][DevToolsConsoleViewMessages].</span></span>  

### <a name="disable-message-grouping"></a><span data-ttu-id="20b17-148">Desabilitar o agrupamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="20b17-148">Disable message grouping</span></span>  

<span data-ttu-id="20b17-149">[Abra Configurações do Console e](#open-console-settings) **desabilite Grupo semelhante** para desabilitar o comportamento padrão de agrupação de mensagens do Console.</span><span class="sxs-lookup"><span data-stu-id="20b17-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="20b17-150">Para obter um exemplo, navegue até [Log XHR e Buscar solicitações](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="20b17-150">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="20b17-151">Solicitações XHR e Fetch de log</span><span class="sxs-lookup"><span data-stu-id="20b17-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="20b17-152">[Abra Configurações do Console e](#open-console-settings) habilita **o Log XMLHttpRequests** para registrar todas as solicitações e no `XMLHttpRequest` Console conforme elas `Fetch` ocorrem.</span><span class="sxs-lookup"><span data-stu-id="20b17-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Solicitações de Log XMLHttpRequest e Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="20b17-154">Log `XMLHttpRequest` e `Fetch` solicitações</span><span class="sxs-lookup"><span data-stu-id="20b17-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="20b17-155">A mensagem superior na figura anterior exibe o comportamento de agrupação padrão do **Console**.</span><span class="sxs-lookup"><span data-stu-id="20b17-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="20b17-156">Persistir mensagens entre cargas de página</span><span class="sxs-lookup"><span data-stu-id="20b17-156">Persist messages across page loads</span></span>  

<span data-ttu-id="20b17-157">Por padrão, o Console é limpo sempre que você carrega uma nova página.</span><span class="sxs-lookup"><span data-stu-id="20b17-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="20b17-158">Para persistir mensagens entre cargas de página, [Abra Configurações do Console](#open-console-settings) e habilita a caixa de seleção Preservar **Log.**</span><span class="sxs-lookup"><span data-stu-id="20b17-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="20b17-159">Ocultar mensagens de rede</span><span class="sxs-lookup"><span data-stu-id="20b17-159">Hide network messages</span></span>  

<span data-ttu-id="20b17-160">Por padrão, o navegador registra mensagens de rede no **Console**.</span><span class="sxs-lookup"><span data-stu-id="20b17-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="20b17-161">Na figura a seguir, a mensagem selecionada representa um código de status HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="20b17-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Uma mensagem 429 no Console" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="20b17-163">Uma `429` mensagem no **Console**</span><span class="sxs-lookup"><span data-stu-id="20b17-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="20b17-164">Para ocultar mensagens de rede:</span><span class="sxs-lookup"><span data-stu-id="20b17-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="20b17-165">[Abra Configurações do Console](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="20b17-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="20b17-166">Habilita **a caixa de seleção Ocultar Rede.**</span><span class="sxs-lookup"><span data-stu-id="20b17-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="20b17-167">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="20b17-167">Filter messages</span></span>  

<span data-ttu-id="20b17-168">Há muitas maneiras de filtrar mensagens no Console.</span><span class="sxs-lookup"><span data-stu-id="20b17-168">There are many ways to filter out messages in the Console.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="20b17-169">Filtrar mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="20b17-169">Filter out browser messages</span></span>  

<span data-ttu-id="20b17-170">[Abra a Barra Lateral do Console](#open-the-console-sidebar) e escolha Mensagens **de** Usuário para mostrar apenas mensagens que vieram do JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="20b17-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Exibir mensagens de usuário" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="20b17-172">Exibir mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="20b17-172">View user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="20b17-173">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="20b17-173">Filter by log level</span></span>  

<span data-ttu-id="20b17-174">O DevTools atribui a cada `console.*` método um nível de severidade.</span><span class="sxs-lookup"><span data-stu-id="20b17-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="20b17-175">Há 4 níveis: `Verbose` , `Info` , e `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="20b17-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="20b17-176">Por exemplo, `console.log()` está no `Info` grupo, enquanto que está no `console.error()` `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="20b17-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="20b17-177">A [Referência da API de Console][DevToolsConsoleApi] descreve o nível de gravidade de cada método aplicável.</span><span class="sxs-lookup"><span data-stu-id="20b17-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="20b17-178">Cada mensagem que o navegador registra no Console também tem um nível de severidade.</span><span class="sxs-lookup"><span data-stu-id="20b17-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="20b17-179">Você pode ocultar qualquer nível de mensagens que não esteja interessado.</span><span class="sxs-lookup"><span data-stu-id="20b17-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="20b17-180">Por exemplo, se você estiver interessado apenas em `Error` mensagens, poderá ocultar os outros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="20b17-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="20b17-181">Escolha o **menu suspenso Níveis de** Log para habilitar ou `Verbose` desabilitar , ou `Info` `Warning` `Error` mensagens.</span><span class="sxs-lookup"><span data-stu-id="20b17-181">Choose the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="O menu suspenso Níveis de Log" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="20b17-183">O **menu suspenso Níveis de** Log</span><span class="sxs-lookup"><span data-stu-id="20b17-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="20b17-184">Você também pode filtrar por nível de log abrindo a Barra lateral do [Console](#open-the-console-sidebar) e, em seguida, recoosing **Errors**, **Warnings**, **Info**ou **Verbose**.</span><span class="sxs-lookup"><span data-stu-id="20b17-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and thenchoosing **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar a barra lateral para exibir avisos" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="20b17-186">Usar a barra lateral para exibir avisos</span><span class="sxs-lookup"><span data-stu-id="20b17-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="20b17-187">Filtrar mensagens por URL</span><span class="sxs-lookup"><span data-stu-id="20b17-187">Filter messages by URL</span></span>  

<span data-ttu-id="20b17-188">Digite `url:` seguido de uma URL para exibir apenas mensagens que vieram dessa URL.</span><span class="sxs-lookup"><span data-stu-id="20b17-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="20b17-189">Depois de digitar `url:` DevTools, mostra todas as URLs relevantes.</span><span class="sxs-lookup"><span data-stu-id="20b17-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="20b17-190">Domínios também funcionam.</span><span class="sxs-lookup"><span data-stu-id="20b17-190">Domains also work.</span></span>  <span data-ttu-id="20b17-191">Por exemplo, se e estão registrando mensagens, permite que você se concentre nas mensagens `https://example.com/a.js` `https://example.com/b.js` desses dois `url:https://example.com` scripts.</span><span class="sxs-lookup"><span data-stu-id="20b17-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Um filtro DE URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="20b17-193">Um filtro DE URL</span><span class="sxs-lookup"><span data-stu-id="20b17-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="20b17-194">Digite `-url:` para ocultar mensagens dessa URL.</span><span class="sxs-lookup"><span data-stu-id="20b17-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="20b17-195">Isso é chamado de filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="20b17-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Um filtro de URL negativo que oculta todas as mensagens que corresponderem à https://b.wal.co URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="20b17-197">Um filtro de URL negativo que oculta todas as mensagens que corresponderem à `https://b.wal.co` URL</span><span class="sxs-lookup"><span data-stu-id="20b17-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="20b17-198">Você também pode mostrar mensagens de uma única URL \*\*\*\* abrindo a Barra Lateral do [Console,](#open-the-console-sidebar)expandindo a seção Mensagens do Usuário e, em seguida, ingando a URL do script que contém as mensagens nas quais você deseja se concentrar.</span><span class="sxs-lookup"><span data-stu-id="20b17-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and thenchoosing the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Exibir as mensagens que vieram de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="20b17-200">Exibir as mensagens que vieram</span><span class="sxs-lookup"><span data-stu-id="20b17-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="20b17-201">Filtrar mensagens de diferentes contextos</span><span class="sxs-lookup"><span data-stu-id="20b17-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="20b17-202">Suponha que você tenha um anúncio \(ad\) em sua página.</span><span class="sxs-lookup"><span data-stu-id="20b17-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="20b17-203">O ad é incorporado em um `<iframe>` e está gerando muitas mensagens em seu Console.</span><span class="sxs-lookup"><span data-stu-id="20b17-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="20b17-204">Como o ad está sendo executado em um contexto [JavaScript](#select-javascript-context)diferente, uma maneira de ocultar as mensagens é abrir Configurações do [Console](#open-console-settings) e ativar a caixa de seleção **Somente** contexto selecionado.</span><span class="sxs-lookup"><span data-stu-id="20b17-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and turn on the **Selected Context Only** checkbox.</span></span>  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a><span data-ttu-id="20b17-205">Filtrar mensagens que não corresponderem a um padrão de expressão regular</span><span class="sxs-lookup"><span data-stu-id="20b17-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="20b17-206">Digite uma expressão regular, como na caixa de texto Filtro, para filtrar todas as mensagens `/[gm][ta][mi]/` que não corresponderem a esse padrão. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="20b17-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="20b17-207">O DevTools verifica se o padrão foi encontrado no texto da mensagem ou no script que fez com que a mensagem fosse registrada.</span><span class="sxs-lookup"><span data-stu-id="20b17-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar todas as mensagens que não corresponderem à expressão regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="20b17-209">Filtrar todas as mensagens que não corresponderem à `/[gm][ta][mi]/` expressão regex</span><span class="sxs-lookup"><span data-stu-id="20b17-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="20b17-210">Executar JavaScript</span><span class="sxs-lookup"><span data-stu-id="20b17-210">Run JavaScript</span></span>  

<span data-ttu-id="20b17-211">Esta seção contém recursos relacionados à execução do JavaScript no Console.</span><span class="sxs-lookup"><span data-stu-id="20b17-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="20b17-212">Para um passo a passo hands-on, navegue até [Executar JavaScript][DevToolsConsoleOverviewJavascript].</span><span class="sxs-lookup"><span data-stu-id="20b17-212">For a hands-on walkthrough, navigate to [Run JavaScript][DevToolsConsoleOverviewJavascript].</span></span>  

### <a name="re-run-expressions-from-history"></a><span data-ttu-id="20b17-213">Re-executar expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="20b17-213">Re-run expressions from history</span></span>  

<span data-ttu-id="20b17-214">Selecione a `Up Arrow` chave para passar pelo histórico de expressões JavaScript que você fez anteriormente no Console.</span><span class="sxs-lookup"><span data-stu-id="20b17-214">Select the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="20b17-215">Selecione `Enter` para executar essa expressão novamente.</span><span class="sxs-lookup"><span data-stu-id="20b17-215">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="20b17-216">Assista ao valor de uma expressão em tempo real com expressões ao vivo</span><span class="sxs-lookup"><span data-stu-id="20b17-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="20b17-217">Se você estiver digitando a mesma expressão JavaScript no Console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo.**</span><span class="sxs-lookup"><span data-stu-id="20b17-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="20b17-218">Com **expressões ao vivo,** você digita uma expressão uma vez e, em seguida, fixá-la na parte superior do console.</span><span class="sxs-lookup"><span data-stu-id="20b17-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="20b17-219">O valor da expressão é atualizado quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="20b17-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="20b17-220">Navegue [até Ver valores de expressão javascript em Real-Time com expressões ao vivo][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="20b17-220">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="disable-eager-evaluation"></a><span data-ttu-id="20b17-221">Desabilitar a avaliação avida</span><span class="sxs-lookup"><span data-stu-id="20b17-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="20b17-222">Ao digitar expressões JavaScript no Console, a **Avaliação** Ávida mostra uma visualização do valor de retorno dessa expressão.</span><span class="sxs-lookup"><span data-stu-id="20b17-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="20b17-223">[Abra Configurações do Console e](#open-console-settings) desabilite a caixa de seleção **Avaliação** Ávida para desativar as visualizações de valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="20b17-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <a name="disable-autocomplete-from-history"></a><span data-ttu-id="20b17-224">Desabilitar o preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="20b17-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="20b17-225">À medida que você digita uma expressão, a janela pop-up de preenchimento automático do Console mostra expressões que você fez anteriormente.</span><span class="sxs-lookup"><span data-stu-id="20b17-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="20b17-226">Essas expressões são pré-anexadas ao `>` caractere.</span><span class="sxs-lookup"><span data-stu-id="20b17-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="20b17-227">[Abra Configurações do Console](#open-console-settings) e **desabilite** a caixa de seleção Preenchimento Automático do Histórico para parar de mostrar expressões do seu histórico.</span><span class="sxs-lookup"><span data-stu-id="20b17-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="20b17-228">Na figura a seguir, `document.querySelector('a')` e `document.querySelector('img')` são expressões avaliadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="20b17-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="O pop-up de preenchimento automático exibe expressões do histórico" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="20b17-230">O pop-up de preenchimento automático exibe expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="20b17-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <a name="select-javascript-context"></a><span data-ttu-id="20b17-231">Selecionar contexto JavaScript</span><span class="sxs-lookup"><span data-stu-id="20b17-231">Select JavaScript context</span></span>  

<span data-ttu-id="20b17-232">Por padrão, o menu suspenso **Contexto JavaScript** é definido como **superior**, o que representa o contexto [de][MDNBrowsingContext] navegação do documento principal.</span><span class="sxs-lookup"><span data-stu-id="20b17-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="O menu suspenso Contexto JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="20b17-234">O **menu suspenso Contexto JavaScript**</span><span class="sxs-lookup"><span data-stu-id="20b17-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="20b17-235">Suponha que você tenha um ad em sua página inserida em `<iframe>` um .</span><span class="sxs-lookup"><span data-stu-id="20b17-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="20b17-236">Você deseja executar JavaScript para ajustar o DOM do ad.</span><span class="sxs-lookup"><span data-stu-id="20b17-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="20b17-237">Você deve primeiro selecionar o contexto de navegação do ad no menu suspenso **Contexto JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="20b17-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Escolha um contexto JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="20b17-239">Escolha um contexto JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="20b17-239">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="20b17-240">Limpar o Console</span><span class="sxs-lookup"><span data-stu-id="20b17-240">Clear the Console</span></span>  

<span data-ttu-id="20b17-241">Você pode usar qualquer um dos seguintes fluxos de trabalho para limpar o Console:</span><span class="sxs-lookup"><span data-stu-id="20b17-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="20b17-242">Escolha **Limpar Console** \( Limpar Console ![ ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="20b17-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="20b17-243">Passe o mouse em uma mensagem, abra o menu contextual \(righ-click\) e escolha **Limpar Console**.</span><span class="sxs-lookup"><span data-stu-id="20b17-243">Hover on a message, open the contextual menu \(righ-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="20b17-244">Insira `clear()` no Console **e** selecione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="20b17-244">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="20b17-245">Execute `console.clear()` a partir do JavaScript para sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="20b17-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="20b17-246">Selecione `Control` + `L` enquanto **o Console** está em foco.</span><span class="sxs-lookup"><span data-stu-id="20b17-246">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="20b17-247">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="20b17-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Exibindo mensagens registradas - Visão geral do console | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Executando o JavaScript - Visão geral do console | Microsoft Docs"  
[DevToolsConsoleJavascript]: ./javascript.md "Começar a executar JavaScript no console | Microsoft Docs"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Assista aos valores de expressão javascript em tempo real com expressões ao | Microsoft Docs"  
[DevToolsConsoleLog]: ./log.md "Começar a registrar mensagens no console | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência da API de Utilitários de Console | Microsoft Docs"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> <span data-ttu-id="20b17-257">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20b17-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="20b17-258">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/console/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="20b17-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="20b17-260">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="20b17-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
