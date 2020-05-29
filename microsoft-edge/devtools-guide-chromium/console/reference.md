---
title: Referência do console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601780"
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





# <span data-ttu-id="05f67-103">Referência do console</span><span class="sxs-lookup"><span data-stu-id="05f67-103">Console Reference</span></span>   



<span data-ttu-id="05f67-104">Esta página é uma referência de recursos relacionados ao console DevTools do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="05f67-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="05f67-105">Ele pressupõe que você já esteja familiarizado com o uso do console para exibir mensagens registradas e executar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="05f67-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="05f67-106">Se não estiver, consulte Introdução [à execução de JavaScript no console][DevToolsConsoleJavascript] e [introdução ao registro de mensagens no console][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="05f67-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="05f67-107">Se você estiver procurando a referência de API em funções como `console.log()` consulte [referência de API do console][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="05f67-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="05f67-108">Para a referência em funções como `monitorEvents()` consulte [referência da API de utilitários de console][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="05f67-108">For the reference on functions like `monitorEvents()` see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="05f67-109">Abrir o console</span><span class="sxs-lookup"><span data-stu-id="05f67-109">Open the Console</span></span>   

<span data-ttu-id="05f67-110">Você pode abrir o console como um [painel](#open-the-console-panel) ou uma [guia na gaveta](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="05f67-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="05f67-111">Abrir o painel de console</span><span class="sxs-lookup"><span data-stu-id="05f67-111">Open the Console panel</span></span>   

<span data-ttu-id="05f67-112">Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="05f67-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

> ##### <span data-ttu-id="05f67-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="05f67-113">Figure 1</span></span>  
> <span data-ttu-id="05f67-114">Painel do console</span><span class="sxs-lookup"><span data-stu-id="05f67-114">The Console panel</span></span>  
> ![Painel do console][ImageConsolePanel]  

<span data-ttu-id="05f67-116">Para abrir o painel do console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e execute o comando **show console** que tenha o selo do **painel** ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="05f67-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

> ##### <span data-ttu-id="05f67-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="05f67-117">Figure 2</span></span>  
> <span data-ttu-id="05f67-118">O comando para mostrar o painel do console</span><span class="sxs-lookup"><span data-stu-id="05f67-118">The command for showing the Console panel</span></span>  
> ![O comando para mostrar o painel do console][ImageCommandShowConsole]  

### <span data-ttu-id="05f67-120">Abrir a guia Console na gaveta</span><span class="sxs-lookup"><span data-stu-id="05f67-120">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="05f67-121">Pressione `Escape` ou clique em **Personalizar e controle devtools** `...` e selecione **Mostrar gaveta do console**.</span><span class="sxs-lookup"><span data-stu-id="05f67-121">Press `Escape` or click **Customize And Control DevTools** `...` and then select **Show console drawer**.</span></span>  

> ##### <span data-ttu-id="05f67-122">Figura 3</span><span class="sxs-lookup"><span data-stu-id="05f67-122">Figure 3</span></span>  
> <span data-ttu-id="05f67-123">Mostrar gaveta do console</span><span class="sxs-lookup"><span data-stu-id="05f67-123">Show console drawer</span></span>  
> ![Mostrar gaveta do console][ImageShowConsoleDrawer]  

<span data-ttu-id="05f67-125">A gaveta é exibida na parte inferior da janela do DevTools, com a guia **console** aberta.</span><span class="sxs-lookup"><span data-stu-id="05f67-125">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

> ##### <span data-ttu-id="05f67-126">Figura 4</span><span class="sxs-lookup"><span data-stu-id="05f67-126">Figure 4</span></span>  
> <span data-ttu-id="05f67-127">A guia Console na gaveta</span><span class="sxs-lookup"><span data-stu-id="05f67-127">The Console tab in the Drawer</span></span>  
> ![A guia Console na gaveta][ImageDrawerConsole]  

<span data-ttu-id="05f67-129">Para abrir a guia Console no [menu de comando][DevToolsCommandMenu], comece a digitar `Console` e, em seguida, execute o comando **show console** que tenha o selo de **gaveta** ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="05f67-129">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

> ##### <span data-ttu-id="05f67-130">Figura 5</span><span class="sxs-lookup"><span data-stu-id="05f67-130">Figure 5</span></span>  
> <span data-ttu-id="05f67-131">O comando para mostrar a guia Console na gaveta</span><span class="sxs-lookup"><span data-stu-id="05f67-131">The command for showing the Console tab in the Drawer</span></span>  
> ![O comando para mostrar a guia Console na gaveta][ImageShowDrawerCommand]  

### <span data-ttu-id="05f67-133">Abrir as configurações do console</span><span class="sxs-lookup"><span data-stu-id="05f67-133">Open Console Settings</span></span>   

<span data-ttu-id="05f67-134">Clique em configurações do console configurações **do console** ![ ][ImageSettingsButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="05f67-134">Click **Console Settings** ![Console Settings][ImageSettingsButtonIcon].</span></span>  

> ##### <span data-ttu-id="05f67-135">Figura 6</span><span class="sxs-lookup"><span data-stu-id="05f67-135">Figure 6</span></span>  
> <span data-ttu-id="05f67-136">Configurações do console</span><span class="sxs-lookup"><span data-stu-id="05f67-136">Console Settings</span></span>  
> ![Configurações do console][ImageConsoleSettings]  

<span data-ttu-id="05f67-138">Os links a seguir explicam cada configuração:</span><span class="sxs-lookup"><span data-stu-id="05f67-138">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="05f67-139">Ocultar rede</span><span class="sxs-lookup"><span data-stu-id="05f67-139">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="05f67-140">Preservar log</span><span class="sxs-lookup"><span data-stu-id="05f67-140">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="05f67-141">Somente contexto selecionado</span><span class="sxs-lookup"><span data-stu-id="05f67-141">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="05f67-142">Grupo semelhante</span><span class="sxs-lookup"><span data-stu-id="05f67-142">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="05f67-143">Registros XMLHttpRequests</span><span class="sxs-lookup"><span data-stu-id="05f67-143">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="05f67-144">Avaliação rápida</span><span class="sxs-lookup"><span data-stu-id="05f67-144">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="05f67-145">Preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="05f67-145">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  

### <span data-ttu-id="05f67-146">Abrir a barra lateral do console</span><span class="sxs-lookup"><span data-stu-id="05f67-146">Open the Console Sidebar</span></span>   

<span data-ttu-id="05f67-147">Clique em **Mostrar barra lateral do console** ![ Mostrar barra lateral ][ImageShowConsoleSidebarIcon] do console para mostrar a barra lateral, que é útil para filtragem.</span><span class="sxs-lookup"><span data-stu-id="05f67-147">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon] to show the Sidebar, which is useful for filtering.</span></span>  

> ##### <span data-ttu-id="05f67-148">Figura 7</span><span class="sxs-lookup"><span data-stu-id="05f67-148">Figure 7</span></span>  
> <span data-ttu-id="05f67-149">Barra lateral do console</span><span class="sxs-lookup"><span data-stu-id="05f67-149">Console Sidebar</span></span>  
> ![Barra lateral do console][ImageConsoleSidebar]  

## <span data-ttu-id="05f67-151">Exibir mensagens</span><span class="sxs-lookup"><span data-stu-id="05f67-151">View messages</span></span>   

<span data-ttu-id="05f67-152">Esta seção contém recursos que alteram o modo como as mensagens são apresentadas no console.</span><span class="sxs-lookup"><span data-stu-id="05f67-152">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="05f67-153">Consulte [Exibir mensagens][DevToolsConsoleViewMessages] para obter uma explicação prática.</span><span class="sxs-lookup"><span data-stu-id="05f67-153">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="05f67-154">Desabilitar o agrupamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="05f67-154">Disable message grouping</span></span>   

<span data-ttu-id="05f67-155">[Abra as configurações do console](#open-console-settings) e desabilite o grupo de forma **semelhante** para desabilitar o comportamento padrão de agrupamento de mensagens do console.</span><span class="sxs-lookup"><span data-stu-id="05f67-155">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="05f67-156">Consulte [log XHR e recuperar solicitações](#log-xhr-and-fetch-requests) para obter um exemplo.</span><span class="sxs-lookup"><span data-stu-id="05f67-156">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="05f67-157">Registrar solicitações de XHR e busca</span><span class="sxs-lookup"><span data-stu-id="05f67-157">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="05f67-158">[Abra as configurações do console](#open-console-settings) e habilite **XMLHttpRequests de log** para registrar todas as `XMLHttpRequest` `Fetch` solicitações e solicitações ao console à medida que elas acontecem.</span><span class="sxs-lookup"><span data-stu-id="05f67-158">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

> ##### <span data-ttu-id="05f67-159">Figura 8</span><span class="sxs-lookup"><span data-stu-id="05f67-159">Figure 8</span></span>  
> <span data-ttu-id="05f67-160">Registro `XMLHttpRequest` em log e `Fetch` solicitações</span><span class="sxs-lookup"><span data-stu-id="05f67-160">Logging `XMLHttpRequest` and `Fetch` requests</span></span>  
> ![Registrando solicitações XMLHttpRequest e busca][ImageXhrGrouped]  

<span data-ttu-id="05f67-162">A mensagem superior na [Figura 8](#figure-8) mostra o comportamento padrão de agrupamento do console.</span><span class="sxs-lookup"><span data-stu-id="05f67-162">The top message in [Figure 8](#figure-8) shows the default grouping behavior of the Console.</span></span>  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="05f67-163">Persistir mensagens em todas as cargas de página</span><span class="sxs-lookup"><span data-stu-id="05f67-163">Persist messages across page loads</span></span>   

<span data-ttu-id="05f67-164">Por padrão, o console é limpo sempre que você carrega uma nova página.</span><span class="sxs-lookup"><span data-stu-id="05f67-164">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="05f67-165">Para persistir mensagens em cargas de página, [abra as configurações do console](#open-console-settings) e, em seguida, habilite a caixa de seleção **preservar registro** .</span><span class="sxs-lookup"><span data-stu-id="05f67-165">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="05f67-166">Ocultar mensagens de rede</span><span class="sxs-lookup"><span data-stu-id="05f67-166">Hide network messages</span></span>   

<span data-ttu-id="05f67-167">Por padrão, o navegador registra as mensagens da rede no **console**.</span><span class="sxs-lookup"><span data-stu-id="05f67-167">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="05f67-168">Por exemplo, a mensagem selecionada na [Figura 9](#figure-9) representa um código de status de `429` .</span><span class="sxs-lookup"><span data-stu-id="05f67-168">For example, the selected message in [Figure 9](#figure-9) represents a status code of `429`.</span></span>  

> ##### <span data-ttu-id="05f67-169">Figura 9</span><span class="sxs-lookup"><span data-stu-id="05f67-169">Figure 9</span></span>  
> <span data-ttu-id="05f67-170">Uma mensagem do 429 no console</span><span class="sxs-lookup"><span data-stu-id="05f67-170">A 429 message in the Console</span></span>  
> <span data-ttu-id="05f67-171">! [Uma mensagem do 429 no console] [Image429Message]</span><span class="sxs-lookup"><span data-stu-id="05f67-171">![A 429 message in the Console][Image429Message]</span></span>  

<span data-ttu-id="05f67-172">Para ocultar as mensagens de rede:</span><span class="sxs-lookup"><span data-stu-id="05f67-172">To hide network messages:</span></span>  

1.  <span data-ttu-id="05f67-173">[Abra as configurações do console](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="05f67-173">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="05f67-174">Habilitar a caixa de seleção **ocultar rede** .</span><span class="sxs-lookup"><span data-stu-id="05f67-174">Enable the **Hide Network** checkbox.</span></span>  

## <span data-ttu-id="05f67-175">Filtrar mensagens</span><span class="sxs-lookup"><span data-stu-id="05f67-175">Filter messages</span></span>   

<span data-ttu-id="05f67-176">Há muitas maneiras de filtrar mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="05f67-176">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="05f67-177">Filtrar mensagens do navegador</span><span class="sxs-lookup"><span data-stu-id="05f67-177">Filter out browser messages</span></span>   

<span data-ttu-id="05f67-178">[Abra a barra lateral do console](#open-the-console-sidebar) e clique em **mensagens de usuário** para mostrar apenas as mensagens que vieram do JavaScript da página.</span><span class="sxs-lookup"><span data-stu-id="05f67-178">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

> ##### <span data-ttu-id="05f67-179">Figura 10</span><span class="sxs-lookup"><span data-stu-id="05f67-179">Figure 10</span></span>  
> <span data-ttu-id="05f67-180">Exibindo mensagens de usuário</span><span class="sxs-lookup"><span data-stu-id="05f67-180">Viewing user messages</span></span>  
> <span data-ttu-id="05f67-181">! [Exibindo mensagens de usuário] [ImageUserMessages]</span><span class="sxs-lookup"><span data-stu-id="05f67-181">![Viewing user messages][ImageUserMessages]</span></span>  

### <span data-ttu-id="05f67-182">Filtrar por nível de log</span><span class="sxs-lookup"><span data-stu-id="05f67-182">Filter by log level</span></span>   

<span data-ttu-id="05f67-183">O DevTools atribui `console.*` um nível de severidade a cada método.</span><span class="sxs-lookup"><span data-stu-id="05f67-183">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="05f67-184">Há 4 níveis: `Verbose` ,, `Info` `Warning` e `Error` .</span><span class="sxs-lookup"><span data-stu-id="05f67-184">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="05f67-185">Por exemplo, `console.log()` é o `Info` grupo, enquanto `console.error()` está no `Error` grupo.</span><span class="sxs-lookup"><span data-stu-id="05f67-185">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="05f67-186">A [referência de API do console][DevToolsConsoleApi] descreve o nível de severidade de cada método aplicável.</span><span class="sxs-lookup"><span data-stu-id="05f67-186">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="05f67-187">Cada mensagem que o navegador registra no console também tem um nível de gravidade.</span><span class="sxs-lookup"><span data-stu-id="05f67-187">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="05f67-188">Você pode ocultar qualquer nível de mensagens em que não está interessado.</span><span class="sxs-lookup"><span data-stu-id="05f67-188">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="05f67-189">Por exemplo, se você estiver interessado apenas em `Error` mensagens, poderá ocultar os outros 3 grupos.</span><span class="sxs-lookup"><span data-stu-id="05f67-189">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="05f67-190">Clique na lista suspensa **níveis de log** para habilitar ou desabilitar `Verbose` , `Info` `Warning` ou `Error` mensagens.</span><span class="sxs-lookup"><span data-stu-id="05f67-190">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

> ##### <span data-ttu-id="05f67-191">Figura 11</span><span class="sxs-lookup"><span data-stu-id="05f67-191">Figure 11</span></span>  
> <span data-ttu-id="05f67-192">Lista suspensa **níveis de log**</span><span class="sxs-lookup"><span data-stu-id="05f67-192">The **Log Levels** dropdown</span></span>  
> <span data-ttu-id="05f67-193">! [A lista suspensa níveis de log] [ImageLogLevels]</span><span class="sxs-lookup"><span data-stu-id="05f67-193">![The Log Levels dropdown][ImageLogLevels]</span></span>  

<span data-ttu-id="05f67-194">Você também pode filtrar por nível de log [abrindo a barra lateral do console](#open-the-console-sidebar) e clicando em **erros**, **avisos**, **informações**ou **detalhados**.</span><span class="sxs-lookup"><span data-stu-id="05f67-194">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

> ##### <span data-ttu-id="05f67-195">Figura 12</span><span class="sxs-lookup"><span data-stu-id="05f67-195">Figure 12</span></span>  
> <span data-ttu-id="05f67-196">Usar a barra lateral para exibir avisos</span><span class="sxs-lookup"><span data-stu-id="05f67-196">Using the Sidebar to view warnings</span></span>  
> <span data-ttu-id="05f67-197">! [Usando a barra lateral para exibir avisos] [ImageSidebarWarnings]</span><span class="sxs-lookup"><span data-stu-id="05f67-197">![Using the Sidebar to view warnings][ImageSidebarWarnings]</span></span>  

### <span data-ttu-id="05f67-198">Filtrar mensagens por URL</span><span class="sxs-lookup"><span data-stu-id="05f67-198">Filter messages by URL</span></span>   

<span data-ttu-id="05f67-199">Tipo `url:` seguido por uma URL para exibir apenas as mensagens que vieram dessa URL.</span><span class="sxs-lookup"><span data-stu-id="05f67-199">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="05f67-200">Depois que você digitar `url:` devtools, todas as URLs relevantes são exibidas.</span><span class="sxs-lookup"><span data-stu-id="05f67-200">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="05f67-201">Os domínios também funcionam.</span><span class="sxs-lookup"><span data-stu-id="05f67-201">Domains also work.</span></span>  <span data-ttu-id="05f67-202">Por exemplo, se `https://example.com/a.js` e `https://example.com/b.js` estiver registrando mensagens, o `url:https://example.com` permite que você se concentre nas mensagens desses 2 scripts.</span><span class="sxs-lookup"><span data-stu-id="05f67-202">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

> ##### <span data-ttu-id="05f67-203">Figura 13</span><span class="sxs-lookup"><span data-stu-id="05f67-203">Figure 13</span></span>  
> <span data-ttu-id="05f67-204">Um filtro de URL</span><span class="sxs-lookup"><span data-stu-id="05f67-204">A URL filter</span></span>  
> <span data-ttu-id="05f67-205">! [Um filtro de URL] [ImageUrlFilter]</span><span class="sxs-lookup"><span data-stu-id="05f67-205">![A URL filter][ImageUrlFilter]</span></span>  

<span data-ttu-id="05f67-206">Digite `-url:` para ocultar as mensagens dessa URL.</span><span class="sxs-lookup"><span data-stu-id="05f67-206">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="05f67-207">Isso é chamado de filtro de URL negativo.</span><span class="sxs-lookup"><span data-stu-id="05f67-207">This is called a negative URL filter.</span></span>  

> ##### <span data-ttu-id="05f67-208">Figura 14</span><span class="sxs-lookup"><span data-stu-id="05f67-208">Figure 14</span></span>  
> <span data-ttu-id="05f67-209">Um filtro de URL negativo que oculta todas as mensagens que correspondem à URL</span><span class="sxs-lookup"><span data-stu-id="05f67-209">A negative URL filter that hides all messages matching the URL</span></span> `https://b.wal.co`  
> <span data-ttu-id="05f67-210">! [Um filtro de URL negativo que oculta todas as mensagens correspondentes à URL https://b.wal.co ] [ImageNegativeUrlFilter1]</span><span class="sxs-lookup"><span data-stu-id="05f67-210">![A negative URL filter that hides all messages matching the URL https://b.wal.co][ImageNegativeUrlFilter1]</span></span>  

<span data-ttu-id="05f67-211">Você também pode mostrar mensagens de uma única URL [abrindo a barra lateral do console](#open-the-console-sidebar), expandindo a seção **mensagens do usuário** e, em seguida, clicando na URL do script que contém as mensagens nas quais você deseja se concentrar.</span><span class="sxs-lookup"><span data-stu-id="05f67-211">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

> ##### <span data-ttu-id="05f67-212">Figura 15</span><span class="sxs-lookup"><span data-stu-id="05f67-212">Figure 15</span></span>  
> <span data-ttu-id="05f67-213">Exibindo as mensagens provenientes de</span><span class="sxs-lookup"><span data-stu-id="05f67-213">Viewing the messages that came from</span></span> `wp-ad.min.js`  
> <span data-ttu-id="05f67-214">! [Exibindo as mensagens que vieram do WP-AD. min. js] [ImageNegativeUrlFilter2]</span><span class="sxs-lookup"><span data-stu-id="05f67-214">![Viewing the messages that came from wp-ad.min.js][ImageNegativeUrlFilter2]</span></span>  

### <span data-ttu-id="05f67-215">Filtrar mensagens de diferentes contextos</span><span class="sxs-lookup"><span data-stu-id="05f67-215">Filter out messages from different contexts</span></span>   

<span data-ttu-id="05f67-216">Suponha que você tenha um anúncio \ (AD \) na sua página.</span><span class="sxs-lookup"><span data-stu-id="05f67-216">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="05f67-217">O anúncio está incorporado em um `<iframe>` e está gerando muitas mensagens no console.</span><span class="sxs-lookup"><span data-stu-id="05f67-217">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="05f67-218">Como o anúncio está em execução em um [contexto JavaScript](#select-javascript-context)diferente, uma maneira de ocultar as mensagens é [abrir as configurações do console](#open-console-settings) e habilitar a caixa de seleção **contexto selecionado somente** .</span><span class="sxs-lookup"><span data-stu-id="05f67-218">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="05f67-219">Filtrar mensagens que não correspondem a um padrão de expressão normal</span><span class="sxs-lookup"><span data-stu-id="05f67-219">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="05f67-220">Digite uma expressão regular como `/[gm][ta][mi]/` na caixa de texto **Filtrar** para filtrar todas as mensagens que não correspondam a esse padrão.</span><span class="sxs-lookup"><span data-stu-id="05f67-220">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="05f67-221">O DevTools verifica se o padrão é encontrado no texto da mensagem ou no script que fez com que a mensagem seja registrada.</span><span class="sxs-lookup"><span data-stu-id="05f67-221">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

> ##### <span data-ttu-id="05f67-222">Figura 16</span><span class="sxs-lookup"><span data-stu-id="05f67-222">Figure 16</span></span>  
> <span data-ttu-id="05f67-223">Filtragem de mensagens que não correspondem</span><span class="sxs-lookup"><span data-stu-id="05f67-223">Filtering out any messages that do not match</span></span> `/[gm][ta][mi]/`  
> <span data-ttu-id="05f67-224">! [Filtrar todas as mensagens que não correspondam à expressão Regex] [ImageRegExFilter]</span><span class="sxs-lookup"><span data-stu-id="05f67-224">![Filtering out any messages that do not match regex expression][ImageRegExFilter]</span></span>  

## <span data-ttu-id="05f67-225">Executar JavaScript</span><span class="sxs-lookup"><span data-stu-id="05f67-225">Run JavaScript</span></span>   

<span data-ttu-id="05f67-226">Esta seção contém recursos relacionados à execução de JavaScript no console.</span><span class="sxs-lookup"><span data-stu-id="05f67-226">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="05f67-227">Confira [executar o JavaScript][DevToolsConsoleOverviewJavascript] para um passo a passo prático.</span><span class="sxs-lookup"><span data-stu-id="05f67-227">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="05f67-228">Executar novamente as expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="05f67-228">Re-run expressions from history</span></span>   

<span data-ttu-id="05f67-229">Pressione a `Up Arrow` tecla para percorrer o histórico de expressões JavaScript que você executou anteriormente no console.</span><span class="sxs-lookup"><span data-stu-id="05f67-229">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="05f67-230">Pressione `Enter` para executar essa expressão novamente.</span><span class="sxs-lookup"><span data-stu-id="05f67-230">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="05f67-231">Assista ao valor de uma expressão em tempo real com expressões dinâmicas</span><span class="sxs-lookup"><span data-stu-id="05f67-231">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="05f67-232">Se você estiver digitando a mesma expressão JavaScript no console repetidamente, talvez seja mais fácil criar uma **expressão ao vivo**.</span><span class="sxs-lookup"><span data-stu-id="05f67-232">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="05f67-233">Com **expressões ao vivo** , você digita uma expressão uma vez e a fixa na parte superior do console.</span><span class="sxs-lookup"><span data-stu-id="05f67-233">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="05f67-234">O valor da expressão é atualizado em tempo real quase em tempo real.</span><span class="sxs-lookup"><span data-stu-id="05f67-234">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="05f67-235">Consulte [observar valores de expressão JavaScript em tempo real com expressões dinâmicas][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="05f67-235">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="05f67-236">Desabilitar a avaliação rápida</span><span class="sxs-lookup"><span data-stu-id="05f67-236">Disable Eager Evaluation</span></span>   

<span data-ttu-id="05f67-237">À medida que você digita expressões JavaScript no console, a **avaliação adiantada** mostra uma visualização do valor de retorno dessa expressão.</span><span class="sxs-lookup"><span data-stu-id="05f67-237">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="05f67-238">[Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **avaliação adiantada** para desativar as visualizações de valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="05f67-238">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="05f67-239">Desabilitar o preenchimento automático do histórico</span><span class="sxs-lookup"><span data-stu-id="05f67-239">Disable autocomplete from history</span></span>   

<span data-ttu-id="05f67-240">À medida que você digita uma expressão, a janela pop-up de preenchimento automático do console mostra as expressões que você executou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05f67-240">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="05f67-241">Essas expressões são precedidas com o `>` caractere.</span><span class="sxs-lookup"><span data-stu-id="05f67-241">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="05f67-242">[Abra as configurações do console](#open-console-settings) e desabilite a caixa de seleção **AutoCompletar do histórico** para parar de mostrar as expressões do seu histórico.</span><span class="sxs-lookup"><span data-stu-id="05f67-242">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="05f67-243">Na [Figura 17](#figure-17), `document.querySelector('a')` e `document.querySelector('img')` são expressões que foram avaliadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05f67-243">In [Figure 17](#figure-17), `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

> ##### <span data-ttu-id="05f67-244">Figura 17</span><span class="sxs-lookup"><span data-stu-id="05f67-244">Figure 17</span></span>  
> <span data-ttu-id="05f67-245">O pop-up de preenchimento automático mostrando expressões do histórico</span><span class="sxs-lookup"><span data-stu-id="05f67-245">The autocomplete popup showing expressions from history</span></span>  
> <span data-ttu-id="05f67-246">! [O pop-up AutoCompletar mostrando expressões do histórico] [ImageHistoryAutocomplete]</span><span class="sxs-lookup"><span data-stu-id="05f67-246">![The autocomplete popup showing expressions from history][ImageHistoryAutocomplete]</span></span>  

### <span data-ttu-id="05f67-247">Selecionar contexto JavaScript</span><span class="sxs-lookup"><span data-stu-id="05f67-247">Select JavaScript context</span></span>   

<span data-ttu-id="05f67-248">Por padrão, a lista suspensa de **contexto JavaScript** é definida como **Top**, que representa o [contexto de navegação][MDNBrowsingContext] do documento principal.</span><span class="sxs-lookup"><span data-stu-id="05f67-248">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

> ##### <span data-ttu-id="05f67-249">Figura 18</span><span class="sxs-lookup"><span data-stu-id="05f67-249">Figure 18</span></span>  
> <span data-ttu-id="05f67-250">A lista suspensa de **contexto JavaScript**</span><span class="sxs-lookup"><span data-stu-id="05f67-250">The **JavaScript Context** dropdown</span></span>  
> <span data-ttu-id="05f67-251">! [A lista suspensa contexto JavaScript] [ImageJavascriptContext]</span><span class="sxs-lookup"><span data-stu-id="05f67-251">![The JavaScript Context dropdown][ImageJavascriptContext]</span></span>  

<span data-ttu-id="05f67-252">Suponha que você tenha um anúncio na sua página incorporado em um `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="05f67-252">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="05f67-253">Você deseja executar o JavaScript para ajustar o DOM do anúncio.</span><span class="sxs-lookup"><span data-stu-id="05f67-253">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="05f67-254">Primeiro, você deve selecionar o contexto de navegação do anúncio na lista suspensa de **contexto JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="05f67-254">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

> ##### <span data-ttu-id="05f67-255">Figura 19</span><span class="sxs-lookup"><span data-stu-id="05f67-255">Figure 19</span></span>  
> <span data-ttu-id="05f67-256">Selecionando um contexto JavaScript diferente</span><span class="sxs-lookup"><span data-stu-id="05f67-256">Selecting a different JavaScript context</span></span>  
> <span data-ttu-id="05f67-257">! [Selecionando um contexto JavaScript diferente] [ImageSelectContext]</span><span class="sxs-lookup"><span data-stu-id="05f67-257">![Selecting a different JavaScript context][ImageSelectContext]</span></span>  

## <span data-ttu-id="05f67-258">Limpar o console</span><span class="sxs-lookup"><span data-stu-id="05f67-258">Clear the Console</span></span>   

<span data-ttu-id="05f67-259">Você pode usar qualquer um dos fluxos de trabalho a seguir para limpar o console:</span><span class="sxs-lookup"><span data-stu-id="05f67-259">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="05f67-260">Clique em **limpar** console ![ limpar console ][ImageClearConsoleIcon] .</span><span class="sxs-lookup"><span data-stu-id="05f67-260">Click **Clear Console** ![Clear Console][ImageClearConsoleIcon].</span></span>  
*   <span data-ttu-id="05f67-261">Clique com o botão direito do mouse em uma mensagem e selecione **limpar console**.</span><span class="sxs-lookup"><span data-stu-id="05f67-261">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="05f67-262">Digite `clear()` o console e pressione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="05f67-262">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="05f67-263">Ligue `console.clear()` do JavaScript para a sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="05f67-263">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="05f67-264">Pressione `Control` + `L` enquanto o console estiver em foco.</span><span class="sxs-lookup"><span data-stu-id="05f67-264">Press `Control`+`L` while the Console is in focus.</span></span>  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Figura 1: painel do console"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figura 2: o comando para mostrar o painel do console"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Figura 3: mostrar a gaveta do console"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Figura 4: guia Console na gaveta"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Figura 5: o comando para mostrar a guia Console na gaveta"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Figura 6: configurações do console"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Figura 7: barra lateral do console"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Figura 8: registro em log de solicitações XMLHttpRequest e FETCH"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Show-Network.msft.png "Figura 9: uma mensagem do 429 no console"  
[ImageUserMessages]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-Drawer-User-messages.msft.png "Figura 10: exibindo mensagens de usuário"  
[ImageLogLevels]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-log-Level-default-Levels.msft.png "Figura 11: a lista suspensa de níveis de log"  
[ImageSidebarWarnings]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Sidebar-Warnings.msft.png "Figura 12: usar a barra lateral para exibir avisos"  
[ImageUrlFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Text.msft.png "Figura 13: um filtro de URL"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Negative-Filter-Text.msft.png "Figura 14: um filtro de URL negativo que oculta todas as mensagens correspondentes à URL https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Text-specified.msft.png "Figura 15: exibindo as mensagens provenientes de wp-AD. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Regex.msft.png "Figura 16: filtrar todas as mensagens que não correspondam à expressão Regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-Filter-Text-AutoFilter-History.msft.png "figura 17: pop-up de preenchimento automático mostrando expressões do histórico"  
[ImageJavascriptContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-dom-Level-Top.msft.png "Figura 18: a lista suspensa de contexto JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/devtools-Guide-Chromium/Media/console-dom-Level-Multiple.msft.png "Figura 19: selecionando um contexto JavaScript diferente"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Exibir mensagens registradas – visão geral do console"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referência de API do console"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Visão geral do console em JavaScript"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Começar a executar o JavaScript no console"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Assista aos valores de expressão JavaScript em tempo real com expressões dinâmicas"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introdução ao registro de mensagens no console"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referência de API de utilitários de console"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Contexto de navegação | MDN"  

> [!NOTE]
> <span data-ttu-id="05f67-293">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="05f67-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="05f67-294">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/console/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="05f67-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="05f67-296">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="05f67-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
