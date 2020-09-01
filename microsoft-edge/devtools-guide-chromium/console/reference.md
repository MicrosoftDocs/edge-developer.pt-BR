---
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 51a85c3dad121dcb42633390de9b4e817074546e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982350"
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





# <span data-ttu-id="ef230-103">Referência do console</span><span class="sxs-lookup"><span data-stu-id="ef230-103">Console Reference</span></span>   



<span data-ttu-id="ef230-104">Esta página é uma referência de recursos relacionados ao console DevTools do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef230-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="ef230-105">Ele pressupõe que você já esteja familiarizado com o uso do console para exibir mensagens registradas e executar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ef230-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="ef230-106">Se não estiver, consulte Introdução [à execução de JavaScript no console][DevToolsConsoleJavascript] e [introdução ao registro de mensagens no console][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="ef230-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="ef230-107">Se você estiver procurando a referência de API em funções como `console.log()` consulte [referência de API do console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="ef230-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="ef230-108">Para obter a referência sobre funções como `monitorEvents()` , consulte [referência da API de utilitários de console][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="ef230-108">For the reference on functions like `monitorEvents()`, see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="ef230-109">Abrir o console</span><span class="sxs-lookup"><span data-stu-id="ef230-109">Open the Console</span></span>   

<span data-ttu-id="ef230-110">Você pode abrir o console como um [painel](#open-the-console-panel) ou uma [guia na gaveta](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="ef230-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="ef230-111">Abrir o painel de console</span><span class="sxs-lookup"><span data-stu-id="ef230-111">Open the Console panel</span></span>   

<span data-ttu-id="ef230-112">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="ef230-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Painel do console" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="ef230-114">Painel do **console**</span><span class="sxs-lookup"><span data-stu-id="ef230-114">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="ef230-115">Para abrir o painel do console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e execute o comando **show console** que tenha o selo do **painel** ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="ef230-115">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="O comando para mostrar o painel do console" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="ef230-117">O comando para mostrar o painel do **console**</span><span class="sxs-lookup"><span data-stu-id="ef230-117">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="ef230-118">Abrir a guia Console na gaveta</span><span class="sxs-lookup"><span data-stu-id="ef230-118">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="ef230-119">Pressione `Escape` ou clique em **Personalizar e controle devtools** \ ( `...` \) e selecione **Mostrar gaveta do console**.</span><span class="sxs-lookup"><span data-stu-id="ef230-119">Press `Escape` or click **Customize And Control DevTools** \(`...`\) and then select **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Mostrar gaveta do console" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="ef230-121">Mostrar gaveta do console</span><span class="sxs-lookup"><span data-stu-id="ef230-121">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="ef230-122">A gaveta é exibida na parte inferior da janela do DevTools, com a guia **console** aberta.</span><span class="sxs-lookup"><span data-stu-id="ef230-122">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="A guia Console na gaveta" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="ef230-124">A guia **console** na **gaveta**</span><span class="sxs-lookup"><span data-stu-id="ef230-124">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="ef230-125">Para abrir a guia Console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e, em seguida, execute o comando **show console** que tenha o selo de **gaveta** ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="ef230-125">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="O comando para mostrar a guia Console na gaveta" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="ef230-127">O comando para mostrar a guia **console** na **gaveta**</span><span class="sxs-lookup"><span data-stu-id="ef230-127">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="ef230-128">Abrir as configurações do console</span><span class="sxs-lookup"><span data-stu-id="ef230-128">Open Console Settings</span></span>   

<span data-ttu-id="ef230-129">Clique em **configurações do console** \ (configurações do ![ console ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ef230-129">Click **Console Settings** \(![Console Settings][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Configurações do console" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="ef230-131">Configurações do console</span><span class="sxs-lookup"><span data-stu-id="ef230-131">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="ef230-132">Os links a seguir explicam cada configuração:</span><span class="sxs-lookup"><span data-stu-id="ef230-132">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="ef230-133">Ocultar rede</span><span class="sxs-lookup"><span data-stu-id="ef230-133">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="ef230-134">Preservar log</span><span class="sxs-lookup"><span data-stu-id="ef230-134">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="ef230-135">Somente contexto selecionado</span><span class="sxs-lookup"><span data-stu-id="ef230-135">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="ef230-136">Grupo semelhante</span><span class="sxs-lookup"><span data-stu-id="ef230-136">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="ef230-137">Registros XMLHttpRequests</span><span class="sxs-lookup"><span data-stu-id="ef230-137">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="ef230-138">Avaliação rápida</span><span class="sxs-lookup"><span data-stu-id="ef230-138">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="ef230-139">Preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="ef230-139">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="ef230-140">Abrir a barra lateral do console</span><span class="sxs-lookup"><span data-stu-id="ef230-140">Open the Console Sidebar</span></span>   

<span data-ttu-id="ef230-141">Clique em **Mostrar barra lateral do console** \ ( ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] do console \) para mostrar a barra lateral, que é útil para filtragem.</span><span class="sxs-lookup"><span data-stu-id="ef230-141">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Barra lateral do console" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="ef230-143">**Console** do Nota</span><span class="sxs-lookup"><span data-stu-id="ef230-143">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="ef230-144">Exibir mensagens</span><span class="sxs-lookup"><span data-stu-id="ef230-144">View messages</span></span>   

<span data-ttu-id="ef230-145">Esta seção contém recursos que alteram o modo como as mensagens são apresentadas no console.</span><span class="sxs-lookup"><span data-stu-id="ef230-145">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="ef230-146">Consulte [Exibir mensagens][DevToolsConsoleViewMessages] para obter uma explicação prática.</span><span class="sxs-lookup"><span data-stu-id="ef230-146">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="ef230-147">Desabilitar o agrupamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="ef230-147">Disable message grouping</span></span>   

<span data-ttu-id="ef230-148">[Abra as configurações do console](#open-console-settings) e desabilite o grupo de forma **semelhante** para desabilitar o comportamento padrão de agrupamento de mensagens do console.</span><span class="sxs-lookup"><span data-stu-id="ef230-148">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="ef230-149">Consulte [log XHR e recuperar solicitações](#log-xhr-and-fetch-requests) para obter um exemplo.</span><span class="sxs-lookup"><span data-stu-id="ef230-149">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="ef230-150">Registrar solicitações de XHR e busca</span><span class="sxs-lookup"><span data-stu-id="ef230-150">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="ef230-151">[Abra as configurações do console](#open-console-settings) e habilite **XMLHttpRequests de log** para registrar todas as `XMLHttpRequest` `Fetch` solicitações e solicitações ao console à medida que elas acontecem.</span><span class="sxs-lookup"><span data-stu-id="ef230-151">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Log de solicitações XMLHttpRequest e FETCH" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="ef230-153">Log `XMLHttpRequest` e `Fetch` solicitações</span><span class="sxs-lookup"><span data-stu-id="ef230-153">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="ef230-154">A mensagem superior na figura anterior exibe o comportamento padrão de agrupamento do **console**.</span><span class="sxs-lookup"><span data-stu-id="ef230-154">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="ef230-155">Persistir mensagens em todas as cargas de página</span><span class="sxs-lookup"><span data-stu-id="ef230-155">Persist messages across page loads</span></span>   

<span data-ttu-id="ef230-156">Por padrão, o console é limpo sempre que você carrega uma nova página.</span><span class="sxs-lookup"><span data-stu-id="ef230-156">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="ef230-157">Para persistir mensagens em cargas de página, [abra as configurações do console](#open-console-settings) e, em seguida, habilite a caixa de seleção **preservar registro** .</span><span class="sxs-lookup"><span data-stu-id="ef230-157">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="ef230-158">Ocultar mensagens de rede</span><span class="sxs-lookup"><span data-stu-id="ef230-158">Hide network messages</span></span>   

<span data-ttu-id="ef230-159">Por padrão, o navegador registra as mensagens da rede no **console**.</span><span class="sxs-lookup"><span data-stu-id="ef230-159">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="ef230-160">Na figura a seguir, a mensagem selecionada representa um código de status HTTP de `429` .</span><span class="sxs-lookup"><span data-stu-id="ef230-160">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Uma mensagem do 429 no console" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="ef230-162">Uma `429` mensagem no **console**</span><span class="sxs-lookup"><span data-stu-id="ef230-162">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="ef230-163">Para ocultar as mensagens de rede:</span><span class="sxs-lookup"><span data-stu-id="ef230-163">To hide network messages:</span></span>  

1.  <span data-ttu-id="ef230-164">[Abra as configurações do console](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="ef230-164">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="ef230-165">Habilitar a caixa de seleção **ocultar rede** .</span><span class="sxs-lookup"><span data-stu-id="ef230-165">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="ef230-166">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="ef230-166">Filter messages</span></span>   

<span data-ttu-id="ef230-167">Há muitas maneiras de filtrar mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="ef230-167">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="ef230-168">Filtrar mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="ef230-168">Filter out browser messages</span></span>   

<span data-ttu-id="ef230-169">[Abra a barra lateral do console](#open-the-console-sidebar) e clique em **mensagens de usuário** para mostrar apenas as mensagens que vieram do JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="ef230-169">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Exibir mensagens de usuário" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="ef230-171">Exibir mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="ef230-171">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="ef230-172">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="ef230-172">Filter by log level</span></span>   

<span data-ttu-id="ef230-173">O DevTools atribui `console.*` um nível de severidade a cada método.</span><span class="sxs-lookup"><span data-stu-id="ef230-173">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="ef230-174">Há 4 níveis: `Verbose` ,, `Info` `Warning` e `Error` .</span><span class="sxs-lookup"><span data-stu-id="ef230-174">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="ef230-175">Por exemplo, `console.log()` é o `Info` grupo, enquanto `console.error()` está no `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="ef230-175">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="ef230-176">A [referência de API do console][DevToolsConsoleApi] descreve o nível de severidade de cada método aplicável.</span><span class="sxs-lookup"><span data-stu-id="ef230-176">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="ef230-177">Cada mensagem que o navegador registra no console também tem um nível de gravidade.</span><span class="sxs-lookup"><span data-stu-id="ef230-177">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="ef230-178">Você pode ocultar qualquer nível de mensagens em que não está interessado.</span><span class="sxs-lookup"><span data-stu-id="ef230-178">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="ef230-179">Por exemplo, se você estiver interessado apenas em `Error` mensagens, poderá ocultar os outros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="ef230-179">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="ef230-180">Clique na lista suspensa **níveis de log** para habilitar ou desabilitar `Verbose` , `Info` `Warning` ou `Error` mensagens.</span><span class="sxs-lookup"><span data-stu-id="ef230-180">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Lista suspensa níveis de log" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="ef230-182">Lista suspensa **níveis de log**</span><span class="sxs-lookup"><span data-stu-id="ef230-182">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="ef230-183">Você também pode filtrar por nível de log [abrindo a barra lateral do console](#open-the-console-sidebar) e clicando em **erros**, **avisos**, **informações**ou **detalhados**.</span><span class="sxs-lookup"><span data-stu-id="ef230-183">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Usar a barra lateral para exibir avisos" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="ef230-185">Usar a barra lateral para exibir avisos</span><span class="sxs-lookup"><span data-stu-id="ef230-185">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="ef230-186">Filtrar mensagens por URL</span><span class="sxs-lookup"><span data-stu-id="ef230-186">Filter messages by URL</span></span>   

<span data-ttu-id="ef230-187">Tipo `url:` seguido por uma URL para exibir apenas as mensagens que vieram dessa URL.</span><span class="sxs-lookup"><span data-stu-id="ef230-187">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="ef230-188">Depois que você digitar `url:` devtools, todas as URLs relevantes são exibidas.</span><span class="sxs-lookup"><span data-stu-id="ef230-188">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="ef230-189">Os domínios também funcionam.</span><span class="sxs-lookup"><span data-stu-id="ef230-189">Domains also work.</span></span>  <span data-ttu-id="ef230-190">Por exemplo, se `https://example.com/a.js` e `https://example.com/b.js` estiver registrando mensagens, o `url:https://example.com` permite que você se concentre nas mensagens desses 2 scripts.</span><span class="sxs-lookup"><span data-stu-id="ef230-190">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Um filtro de URL" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="ef230-192">Um filtro de URL</span><span class="sxs-lookup"><span data-stu-id="ef230-192">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="ef230-193">Digite `-url:` para ocultar as mensagens dessa URL.</span><span class="sxs-lookup"><span data-stu-id="ef230-193">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="ef230-194">Isso é chamado de filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="ef230-194">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Um filtro de URL negativo que oculta todas as mensagens correspondentes à https://b.wal.co URL" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="ef230-196">Um filtro de URL negativo que oculta todas as mensagens correspondentes à `https://b.wal.co` URL</span><span class="sxs-lookup"><span data-stu-id="ef230-196">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="ef230-197">Você também pode mostrar mensagens de uma única URL [abrindo a barra lateral do console](#open-the-console-sidebar), expandindo a seção **mensagens do usuário** e, em seguida, clicando na URL do script que contém as mensagens nas quais você deseja se concentrar.</span><span class="sxs-lookup"><span data-stu-id="ef230-197">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Exibir as mensagens provenientes de wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="ef230-199">Exibir as mensagens provenientes de</span><span class="sxs-lookup"><span data-stu-id="ef230-199">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="ef230-200">Filtrar mensagens de diferentes contextos</span><span class="sxs-lookup"><span data-stu-id="ef230-200">Filter out messages from different contexts</span></span>   

<span data-ttu-id="ef230-201">Suponha que você tenha um anúncio \ (AD \) na sua página.</span><span class="sxs-lookup"><span data-stu-id="ef230-201">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="ef230-202">O anúncio está incorporado em um `<iframe>` e está gerando muitas mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="ef230-202">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="ef230-203">Como o anúncio está em execução em um [contexto JavaScript](#select-javascript-context)diferente, uma maneira de ocultar as mensagens é [abrir as configurações do console](#open-console-settings) e habilitar a caixa de seleção **contexto selecionado somente** .</span><span class="sxs-lookup"><span data-stu-id="ef230-203">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="ef230-204">Filtrar mensagens que não correspondem a um padrão de expressão normal</span><span class="sxs-lookup"><span data-stu-id="ef230-204">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="ef230-205">Digite uma expressão regular como `/[gm][ta][mi]/` na caixa de texto **Filtrar** para filtrar todas as mensagens que não correspondam a esse padrão.</span><span class="sxs-lookup"><span data-stu-id="ef230-205">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="ef230-206">O DevTools verifica se o padrão é encontrado no texto da mensagem ou no script que fez com que a mensagem seja registrada.</span><span class="sxs-lookup"><span data-stu-id="ef230-206">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Filtrar todas as mensagens que não correspondam à expressão Regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="ef230-208">Filtrar todas as mensagens que não correspondam à `/[gm][ta][mi]/` expressão Regex</span><span class="sxs-lookup"><span data-stu-id="ef230-208">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="ef230-209">Executar JavaScript</span><span class="sxs-lookup"><span data-stu-id="ef230-209">Run JavaScript</span></span>   

<span data-ttu-id="ef230-210">Esta seção contém recursos relacionados à execução de JavaScript no console.</span><span class="sxs-lookup"><span data-stu-id="ef230-210">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="ef230-211">Confira [executar o JavaScript][DevToolsConsoleOverviewJavascript] para um passo a passo prático.</span><span class="sxs-lookup"><span data-stu-id="ef230-211">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="ef230-212">Executar novamente as expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="ef230-212">Re-run expressions from history</span></span>   

<span data-ttu-id="ef230-213">Pressione a `Up Arrow` tecla para percorrer o histórico de expressões JavaScript que você executou anteriormente no console.</span><span class="sxs-lookup"><span data-stu-id="ef230-213">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="ef230-214">Pressione `Enter` para executar essa expressão novamente.</span><span class="sxs-lookup"><span data-stu-id="ef230-214">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="ef230-215">Assista ao valor de uma expressão em tempo real com expressões dinâmicas</span><span class="sxs-lookup"><span data-stu-id="ef230-215">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="ef230-216">Se você estiver digitando a mesma expressão JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="ef230-216">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="ef230-217">Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.</span><span class="sxs-lookup"><span data-stu-id="ef230-217">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="ef230-218">O valor da expressão é atualizado em tempo real quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="ef230-218">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="ef230-219">Consulte [observar valores de expressão JavaScript em tempo real com expressões dinâmicas][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="ef230-219">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="ef230-220">Desabilitar a avaliação rápida</span><span class="sxs-lookup"><span data-stu-id="ef230-220">Disable Eager Evaluation</span></span>   

<span data-ttu-id="ef230-221">À medida que você digita expressões JavaScript no console, a **avaliação adiantada** mostra uma visualização do valor de retorno dessa expressão.</span><span class="sxs-lookup"><span data-stu-id="ef230-221">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="ef230-222">[Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **avaliação adiantada** para desativar as visualizações de valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ef230-222">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="ef230-223">Desabilitar o preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="ef230-223">Disable autocomplete from history</span></span>   

<span data-ttu-id="ef230-224">À medida que você digita uma expressão, a janela pop-up de preenchimento automático do console mostra as expressões que você executou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ef230-224">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="ef230-225">Essas expressões são precedidas com o `>` caractere.</span><span class="sxs-lookup"><span data-stu-id="ef230-225">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="ef230-226">[Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **AutoCompletar do histórico** para parar de mostrar as expressões do seu histórico.</span><span class="sxs-lookup"><span data-stu-id="ef230-226">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="ef230-227">Na figura a seguir, `document.querySelector('a')` e `document.querySelector('img')` são expressões que foram avaliadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ef230-227">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="O pop-up AutoCompletar exibe expressões do histórico" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="ef230-229">O pop-up AutoCompletar exibe expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="ef230-229">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="ef230-230">Selecionar contexto JavaScript</span><span class="sxs-lookup"><span data-stu-id="ef230-230">Select JavaScript context</span></span>   

<span data-ttu-id="ef230-231">Por padrão, a lista suspensa de **contexto JavaScript** é definida como **Top**, que representa o [contexto de navegação][MDNBrowsingContext] do documento principal.</span><span class="sxs-lookup"><span data-stu-id="ef230-231">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="A lista suspensa de contexto JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="ef230-233">A lista suspensa de **contexto JavaScript**</span><span class="sxs-lookup"><span data-stu-id="ef230-233">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="ef230-234">Suponha que você tenha um anúncio na sua página incorporado em um `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="ef230-234">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="ef230-235">Você deseja executar o JavaScript para ajustar o DOM do anúncio.</span><span class="sxs-lookup"><span data-stu-id="ef230-235">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="ef230-236">Primeiro, você deve selecionar o contexto de navegação do anúncio na lista suspensa de **contexto JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="ef230-236">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Selecionar um contexto JavaScript diferente" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="ef230-238">Selecionar um contexto JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="ef230-238">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="ef230-239">Limpar o console</span><span class="sxs-lookup"><span data-stu-id="ef230-239">Clear the Console</span></span>   

<span data-ttu-id="ef230-240">Você pode usar qualquer um dos fluxos de trabalho a seguir para limpar o console:</span><span class="sxs-lookup"><span data-stu-id="ef230-240">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="ef230-241">Clique em **limpar console** \ ( ![ limpar console ][ImageClearConsoleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ef230-241">Click **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="ef230-242">Clique com o botão direito do mouse em uma mensagem e selecione **limpar console**.</span><span class="sxs-lookup"><span data-stu-id="ef230-242">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="ef230-243">Digite `clear()` o console e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ef230-243">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="ef230-244">Ligue `console.clear()` do JavaScript para a sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="ef230-244">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="ef230-245">Pressione `Control` + `L` enquanto o console estiver em foco.</span><span class="sxs-lookup"><span data-stu-id="ef230-245">Press `Control`+`L` while the Console is in focus.</span></span>  
    
<!--
 

  
-->  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Exibir mensagens registradas – visão geral do console | Documentos da Microsoft"  
[DevToolsConsoleApi]: ./api.md "Referência de API de console | Documentos da Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Como executar JavaScript – visão geral do console | Documentos da Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Comece a executar o JavaScript no console | Documentos da Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas | Documentos da Microsoft"  
[DevToolsConsoleLog]: ./log.md "Introdução ao registro de mensagens no console | Documentos da Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Referência de API de utilitários de console | Documentos da Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> <span data-ttu-id="ef230-255">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="ef230-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ef230-256">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ef230-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ef230-258">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ef230-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
