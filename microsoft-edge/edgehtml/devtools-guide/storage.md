---
description: Use o painel De armazenamento para inspecionar o armazenamento da Web, IndexedDB, cookies e caches de solicitação/resposta
title: Armazenamento | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, armazenamento da Web, armazenamento local, armazenamento de sessão, indexadodb, cookies, serviço de trabalho, cache
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398893"
---
# <a name="storage"></a><span data-ttu-id="0f98c-104">Storage</span><span class="sxs-lookup"><span data-stu-id="0f98c-104">Storage</span></span>

<span data-ttu-id="0f98c-105">Use o **painel De** armazenamento para inspecionar e gerenciar vários dados armazenados em cache localmente, incluindo:</span><span class="sxs-lookup"><span data-stu-id="0f98c-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>  

*   <span data-ttu-id="0f98c-106">[Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs</span><span class="sxs-lookup"><span data-stu-id="0f98c-106">[Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs</span></span>  
*   <span data-ttu-id="0f98c-107">[Dados estruturados de DB](#indexeddb-manager) indexados</span><span class="sxs-lookup"><span data-stu-id="0f98c-107">[Indexed DB](#indexeddb-manager) structured data</span></span>  
*   <span data-ttu-id="0f98c-108">[Cookies](#cookies-list) para o domínio</span><span class="sxs-lookup"><span data-stu-id="0f98c-108">[Cookies](#cookies-list) for the domain</span></span>  
*   <span data-ttu-id="0f98c-109">[Cache](#cache-manager) \(pares de solicitação/resposta\) para depuração de funcionários de serviço</span><span class="sxs-lookup"><span data-stu-id="0f98c-109">[Cache](#cache-manager) \(request/response pairs\) for service worker debugging</span></span>  

<span data-ttu-id="0f98c-110">Expanda qualquer uma dessas categorias e clique em uma entrada filha para abrir sua guia gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f98c-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>  

## <a name="local-and-session-storage-managers"></a><span data-ttu-id="0f98c-111">Gerentes de armazenamento local e de sessão</span><span class="sxs-lookup"><span data-stu-id="0f98c-111">Local and Session storage managers</span></span>  

<span data-ttu-id="0f98c-112">Use o Gerenciador de Armazenamento Local e o Gerenciador de Armazenamento de Sessão para inspecionar e gerenciar o armazenamento da Web para sua página.</span><span class="sxs-lookup"><span data-stu-id="0f98c-112">Use the Local Storage manager and Session Storage manager to inspect and manage the web storage for your page.</span></span>  

<span data-ttu-id="0f98c-113">As **pastas Armazenamento Local** e Armazenamento de **Sessão** dentro do Se [picker](./debugger.md#resource-picker) de Recursos do painel de armazenamento exibem uma lista de origens para a página.</span><span class="sxs-lookup"><span data-stu-id="0f98c-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [Resource picker](./debugger.md#resource-picker) display a list of origins for the page.</span></span>  <span data-ttu-id="0f98c-114">Selecionar um desses quadros abre uma tabela editável dos pares de chave/valor atuais definidos por meio de [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente \(and/or set directly from the DevTools [Storage list](#storage-list)\).</span><span class="sxs-lookup"><span data-stu-id="0f98c-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively \(and/or set directly from the  DevTools [Storage list](#storage-list)\).</span></span>  

![Gerente de Armazenamento do DevTools](./media/storage_web_storage.png)  

<span data-ttu-id="0f98c-116">Nas guias Armazenamento Local e Armazenamento de Sessão, você pode:</span><span class="sxs-lookup"><span data-stu-id="0f98c-116">From the Local Storage and Session Storage tabs you can:</span></span>  

*   <span data-ttu-id="0f98c-117">**Atualize** \( \) a lista de armazenamento para ver o conjunto atual de pares de `Ctrl+F5` chave/valores para o domínio determinado. [](#cookies-list)</span><span class="sxs-lookup"><span data-stu-id="0f98c-117">**Refresh** \(`Ctrl+F5`\) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span>  <span data-ttu-id="0f98c-118">\(A lista não atualiza automaticamente após atualizações de script.\)</span><span class="sxs-lookup"><span data-stu-id="0f98c-118">\(The list does not auto-refresh upon script updates.\)</span></span>  
*   <span data-ttu-id="0f98c-119">**Simular atingir o limite de armazenamento**  para o armazenamento web do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f98c-119">**Simulate reaching the storage limit**  for Microsoft Edge web storage.</span></span>  <span data-ttu-id="0f98c-120">Cada domínio e subdomínio tem sua própria área de armazenamento, no entanto, há um limite combinado:</span><span class="sxs-lookup"><span data-stu-id="0f98c-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>  
    *   <span data-ttu-id="0f98c-121">**Subdomas**: até 5 MBs de espaço</span><span class="sxs-lookup"><span data-stu-id="0f98c-121">**Subdomains**:  up to 5 MBs of space</span></span>  
    *   <span data-ttu-id="0f98c-122">**Domínios**: até 10 MBs de espaço</span><span class="sxs-lookup"><span data-stu-id="0f98c-122">**Domains**:  up to 10 MBs of space</span></span>  
    *   <span data-ttu-id="0f98c-123">**Total para todos os domínios**: até 50 MBs de espaço</span><span class="sxs-lookup"><span data-stu-id="0f98c-123">**Total for all domains**:  up to 50 MBs of space</span></span>  

   <span data-ttu-id="0f98c-124">O armazenamento de sessão é limpo assim que a última guia do navegador fazendo referência à sua origem é fechada.</span><span class="sxs-lookup"><span data-stu-id="0f98c-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span>  <span data-ttu-id="0f98c-125">As entradas de armazenamento local persistem indefinidamente até serem desempuradas programaticamente pela página ou manualmente pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="0f98c-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>  

   <span data-ttu-id="0f98c-126">**Configurações**  >  **Limpar dados de navegação**  >  **Cookies e dados de site salvos**</span><span class="sxs-lookup"><span data-stu-id="0f98c-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

![Limpar dados de navegação do painel Configurações do Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a><span data-ttu-id="0f98c-128">Lista de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0f98c-128">Storage list</span></span>  

<span data-ttu-id="0f98c-129">Na tabela De armazenamento, você pode:</span><span class="sxs-lookup"><span data-stu-id="0f98c-129">From the Storage list table you can:</span></span>  

*   <span data-ttu-id="0f98c-130">**Inspecione** e `key/value` classificar seus pares clicando em qualquer nome de coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="0f98c-130">**Inspect and sort** your `key/value` pairs by clicking on either column name in the table.</span></span>  
*   <span data-ttu-id="0f98c-131">**Edite** `Key` e de uma entrada existente `Value` clicando na célula.</span><span class="sxs-lookup"><span data-stu-id="0f98c-131">**Edit** the `Key` and `Value` of an existing entry by clicking in the cell.</span></span>  
*   <span data-ttu-id="0f98c-132">**Excluir** \( \) uma entrada da opção de menu de contexto de clique com o botão direito `Del` do mouse, **Excluir item**.</span><span class="sxs-lookup"><span data-stu-id="0f98c-132">**Delete** \(`Del`\) an entry from the right-click context menu option, **Delete item**.</span></span>  
*   <span data-ttu-id="0f98c-133">**Adicione** um novo `key/value` par clicando na linha vazia na parte inferior da tabela.</span><span class="sxs-lookup"><span data-stu-id="0f98c-133">**Add** a new `key/value` pair by clicking on the empty row at the bottom of the table.</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="0f98c-134">Atalhos</span><span class="sxs-lookup"><span data-stu-id="0f98c-134">Shortcuts</span></span>

| <span data-ttu-id="0f98c-135">Ação</span><span class="sxs-lookup"><span data-stu-id="0f98c-135">Action</span></span> | <span data-ttu-id="0f98c-136">Atalho</span><span class="sxs-lookup"><span data-stu-id="0f98c-136">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0f98c-137">Atualizar</span><span class="sxs-lookup"><span data-stu-id="0f98c-137">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="0f98c-138">Excluir item</span><span class="sxs-lookup"><span data-stu-id="0f98c-138">Delete item</span></span> | `Del` |  
| <span data-ttu-id="0f98c-139">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="0f98c-139">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="0f98c-140">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="0f98c-140">Select all</span></span> | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a><span data-ttu-id="0f98c-141">Gerente indexedDB</span><span class="sxs-lookup"><span data-stu-id="0f98c-141">IndexedDB manager</span></span>  

<span data-ttu-id="0f98c-142">Use a **guia IndexedDB** para inspecionar e gerenciar os dados estruturados armazenados localmente em uma máquina cliente.</span><span class="sxs-lookup"><span data-stu-id="0f98c-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span>  <span data-ttu-id="0f98c-143">Especificamente, você pode inspecionar/classificar e atualizar seus índices e armazenamentos de objetos e também excluir entradas de valor de chave individuais.</span><span class="sxs-lookup"><span data-stu-id="0f98c-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>  

> [!TIP]
> <span data-ttu-id="0f98c-144">Você pode usar nossa [demonstração do Mixador](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) de Áudio para testar o *gerenciador IndexedDB* no Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="0f98c-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="0f98c-145">Para excluir todos os dados IndexedDB armazenados para o usuário atual no Microsoft Edge, use o menu Configurações **do** Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="0f98c-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge **Settings** menu:</span></span>  

<span data-ttu-id="0f98c-146">**...** >  **Configurações**  >  **Limpar dados de navegação**  >  **Cookies e dados de site salvos**</span><span class="sxs-lookup"><span data-stu-id="0f98c-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

<span data-ttu-id="0f98c-147">A pasta dentro do Seletor de Recursos do Depurador exibe uma lista de origens dos recursos `IndexedDB` carregados pela [](./debugger.md#resource-picker) página.</span><span class="sxs-lookup"><span data-stu-id="0f98c-147">The `IndexedDB` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="0f98c-148">Todos os bancos de dados IndexedDB \(IDB\) serão listados na origem, juntamente com seus armazenamentos de objetos.</span><span class="sxs-lookup"><span data-stu-id="0f98c-148">Any IndexedDB \(IDB\) databases will be listed under the origin, along with their object stores.</span></span>  

![Gerente IndexedDB do DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a><span data-ttu-id="0f98c-150">Barra de ferramentas IndexedDB</span><span class="sxs-lookup"><span data-stu-id="0f98c-150">IndexedDB Toolbar</span></span>  

<span data-ttu-id="0f98c-151">Na barra de ferramentas IndexedDB, você pode:</span><span class="sxs-lookup"><span data-stu-id="0f98c-151">From the IndexedDB toolbar you can:</span></span>  

*   <span data-ttu-id="0f98c-152">**Atualize** \( \) para ver as entradas atuais no armazenamento de objetos `Ctrl` + `F5` ou no índice do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f98c-152">**Refresh** \(`Ctrl`+`F5`\) to see the current entries in the object store or index of your database.</span></span>  <span data-ttu-id="0f98c-153">O gerente IndexedDB não atualize automaticamente quando as alterações são feitas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f98c-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>  

### <a name="object-store-entries-list"></a><span data-ttu-id="0f98c-154">Lista de entradas do armazenamento de objetos</span><span class="sxs-lookup"><span data-stu-id="0f98c-154">Object store entries list</span></span>  

<span data-ttu-id="0f98c-155">No armazenamento de objetos ou na tabela Índice, você pode:</span><span class="sxs-lookup"><span data-stu-id="0f98c-155">From the Object store or Index table you can:</span></span>  

*   <span data-ttu-id="0f98c-156">**Inspecione** e classificar seus pares de valores-chave clicando em qualquer nome de coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="0f98c-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="0f98c-157">**Atualizar** \( `Ctrl` + `F5` \)</span><span class="sxs-lookup"><span data-stu-id="0f98c-157">**Refresh** \(`Ctrl`+`F5`\)</span></span>  
*   <span data-ttu-id="0f98c-158">**Excluir item** \( `Del` \) para remover a entrada selecionada no seu armazenamento de objetos ou índice.</span><span class="sxs-lookup"><span data-stu-id="0f98c-158">**Delete item** \(`Del`\) to remove the selected entry in your object store or index.</span></span>  <span data-ttu-id="0f98c-159">Você também pode fazer isso na opção menu de contexto com o botão direito [do](#context-menu) mouse, **Excluir item**.</span><span class="sxs-lookup"><span data-stu-id="0f98c-159">You can also do this from the right-click [context menu](#context-menu) option, **Delete item**.</span></span>  
*   <span data-ttu-id="0f98c-160">**Copie itens selecionados** \( `Ctrl` + `C` \) para copiar o item selecionado para sua área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0f98c-160">**Copy selected items** \(`Ctrl`+`C`\) to copy the selected item to your clipboard.</span></span>  <span data-ttu-id="0f98c-161">Você também pode fazer isso na opção menu de contexto com o botão direito [do](#context-menu) **mouse, Copiar item selecionado**.</span><span class="sxs-lookup"><span data-stu-id="0f98c-161">You can also do this from the right-click [context menu](#context-menu) option, **Copy selected item**.</span></span>  
*   <span data-ttu-id="0f98c-162">**Selecione todos** \( `Ctrl` + `A` \) para selecionar todas as entradas no seu armazenamento de objetos ou índice.</span><span class="sxs-lookup"><span data-stu-id="0f98c-162">**Select all** \(`Ctrl`+`A`\) to select all the entries in your object store or index.</span></span>  <span data-ttu-id="0f98c-163">Você também pode fazer isso na opção menu de contexto com o botão [direito](#context-menu) do mouse, **Selecione tudo**.</span><span class="sxs-lookup"><span data-stu-id="0f98c-163">You can also do this from the right-click [context menu](#context-menu) option, **Select all**.</span></span>  

<span data-ttu-id="0f98c-164">As colunas do armazenamento de objetos ou da tabela Index podem ser classificação:</span><span class="sxs-lookup"><span data-stu-id="0f98c-164">The columns of the Object store or Index table are sortable:</span></span>  

| <span data-ttu-id="0f98c-165">Coluna</span><span class="sxs-lookup"><span data-stu-id="0f98c-165">Column</span></span> | <span data-ttu-id="0f98c-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f98c-166">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0f98c-167">Chave</span><span class="sxs-lookup"><span data-stu-id="0f98c-167">Key</span></span> | <span data-ttu-id="0f98c-168">Nome do par de valores-chave \(mesmo que **Chave Primária**\) ao iterar sobre um armazenamento de objetos; Nome da chave de índice \(chave atual do cursor\) ao iterar sobre um índice</span><span class="sxs-lookup"><span data-stu-id="0f98c-168">Name of the key-value pair \(same as **Primary Key**\) when iterating over an object store; Name of the index key \(cursor's current key\) when iterating over an index</span></span> |  
| <span data-ttu-id="0f98c-169">Chave Primária</span><span class="sxs-lookup"><span data-stu-id="0f98c-169">Primary Key</span></span> | <span data-ttu-id="0f98c-170">Nome do par de valores-chave \(consulte **Documentos da Web MDN** para obter mais informações sobre chaves [do](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)BID \)</span><span class="sxs-lookup"><span data-stu-id="0f98c-170">Name of the key-value pair \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span></span> |  
| <span data-ttu-id="0f98c-171">Value</span><span class="sxs-lookup"><span data-stu-id="0f98c-171">Value</span></span> | <span data-ttu-id="0f98c-172">Valor do par de valores-chave</span><span class="sxs-lookup"><span data-stu-id="0f98c-172">Value of the key-value pair</span></span> |  

<span data-ttu-id="0f98c-173">Confira documentos *da Web MDN para* saber mais sobre conceitos e uso [indexadosDB.](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)</span><span class="sxs-lookup"><span data-stu-id="0f98c-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>  

### <a name="context-menu"></a><span data-ttu-id="0f98c-174">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="0f98c-174">Context menu</span></span>  

<span data-ttu-id="0f98c-175">Além da barra de ferramentas [ *IndexedDB,* ](#indexeddb-toolbar)você também pode gerenciar seus dados em armazenamentos de objetos ou índices no **menu** Contexto com o botão direito do mouse e/ou [atalhos de teclado.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="0f98c-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="0f98c-176">Atalhos</span><span class="sxs-lookup"><span data-stu-id="0f98c-176">Shortcuts</span></span>

| <span data-ttu-id="0f98c-177">Ação</span><span class="sxs-lookup"><span data-stu-id="0f98c-177">Action</span></span> | <span data-ttu-id="0f98c-178">Atalho</span><span class="sxs-lookup"><span data-stu-id="0f98c-178">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0f98c-179">Atualizar</span><span class="sxs-lookup"><span data-stu-id="0f98c-179">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="0f98c-180">Excluir par de valores-chave</span><span class="sxs-lookup"><span data-stu-id="0f98c-180">Delete key-value pair</span></span> | `Del` |  
| <span data-ttu-id="0f98c-181">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="0f98c-181">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="0f98c-182">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="0f98c-182">Select all</span></span> | `Ctrl +`<span data-ttu-id="0f98c-183">A'</span><span class="sxs-lookup"><span data-stu-id="0f98c-183">A\`</span></span> |  

## <a name="cookies-manager"></a><span data-ttu-id="0f98c-184">Gerenciador de cookies</span><span class="sxs-lookup"><span data-stu-id="0f98c-184">Cookies manager</span></span>  

<span data-ttu-id="0f98c-185">Use o Gerenciador de Cookies para inspecionar e gerenciar os cookies para o domínio determinado.</span><span class="sxs-lookup"><span data-stu-id="0f98c-185">Use the Cookies manager to inspect and manage the cookies for the given domain.</span></span>  

<span data-ttu-id="0f98c-186">A pasta dentro do Seletor de Recursos do Depurador exibe uma lista de origens dos recursos `Cookies` carregados pela [](./debugger.md#resource-picker) página.</span><span class="sxs-lookup"><span data-stu-id="0f98c-186">The `Cookies` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="0f98c-187">Selecionar um desses quadros abre uma tabela que representa os cookies atuais definidos pelo cabeçalho [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou por script com [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="0f98c-187">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>  

![Gerenciador de Cookies do DevTools](./media/storage_cookies.png)  

<span data-ttu-id="0f98c-189">Na barra de ferramentas da guia Cookies, você pode:</span><span class="sxs-lookup"><span data-stu-id="0f98c-189">From the Cookies tab toolbar you can:</span></span>  

*   <span data-ttu-id="0f98c-190">**Atualize** \( `Ctrl` + `F5` \) a [lista Cookies](#cookies-list) para ver o conjunto atual de cookies para o domínio determinado.</span><span class="sxs-lookup"><span data-stu-id="0f98c-190">**Refresh** \(`Ctrl`+`F5`\) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span>  <span data-ttu-id="0f98c-191">\(A lista não atualize automaticamente.\)</span><span class="sxs-lookup"><span data-stu-id="0f98c-191">\(The list does not auto-refresh.\)</span></span>  
*   <span data-ttu-id="0f98c-192">**Exclua** todos os cookies `Ctrl` + `Shift` + `Del` \( \) \(session e permanent\) para o caminho da página atual.</span><span class="sxs-lookup"><span data-stu-id="0f98c-192">**Delete all cookies** \(`Ctrl`+`Shift`+`Del`\) \(session and permanent\) for the path of the current page.</span></span>  
*   <span data-ttu-id="0f98c-193">**Exclua todos os cookies** `Ctrl` + `Del` de sessão \( \) para o caminho da página atual.</span><span class="sxs-lookup"><span data-stu-id="0f98c-193">**Delete all session cookies** \(`Ctrl`+`Del`\) for the path of the current page.</span></span>  

<span data-ttu-id="0f98c-194">Para limpar completamente sua lista de Cookies, talvez seja necessário limpar todos **os cookies** para o domínio na barra de ferramentas [do](./network.md#toolbar) painel de rede.</span><span class="sxs-lookup"><span data-stu-id="0f98c-194">To completely clear your Cookies list, you might need to **Clear all cookies for the domain** from the [Network](./network.md#toolbar) panel toolbar.</span></span>  

### <a name="cookies-list"></a><span data-ttu-id="0f98c-195">Lista de cookies</span><span class="sxs-lookup"><span data-stu-id="0f98c-195">Cookies list</span></span>  

<span data-ttu-id="0f98c-196">Na tabela de lista Cookies, você pode:</span><span class="sxs-lookup"><span data-stu-id="0f98c-196">From the Cookies list table you can:</span></span>  

*   <span data-ttu-id="0f98c-197">**Inspecionar e classificar** seus cookies clicando em qualquer nome de coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="0f98c-197">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="0f98c-198">**Edite** `Name` e de um cookie existente `Value` clicando na célula.</span><span class="sxs-lookup"><span data-stu-id="0f98c-198">**Edit** the `Name` and `Value` of an existing cookie by clicking in the cell.</span></span>  
*   <span data-ttu-id="0f98c-199">**Exclua** \( \) um cookie da opção de menu de contexto com o botão `Del` direito do mouse, [](#context-menu) `Delete cookie` .</span><span class="sxs-lookup"><span data-stu-id="0f98c-199">**Delete** \(`Del`\) a cookie from the right-click [context menu](#context-menu) option, `Delete cookie`.</span></span>  
*   <span data-ttu-id="0f98c-200">**Adicione** um novo cookie de sessão para o dado clicando na linha `Domain/Path` vazia na parte inferior da tabela.</span><span class="sxs-lookup"><span data-stu-id="0f98c-200">**Add** a new session cookie for the given `Domain/Path` by clicking on the empty row at the bottom of the table.</span></span>  <span data-ttu-id="0f98c-201">Isso só funciona para cookies de sessão; cookies permanentes \(com datas de expiração específicas\) devem ser definidos com métodos tradicionais.</span><span class="sxs-lookup"><span data-stu-id="0f98c-201">This only works for session cookies; permanent cookies \(with specific expiry dates\) must be set with traditional methods.</span></span>  <span data-ttu-id="0f98c-202">Os `Domain` valores e são `Path` preenchidos automaticamente de acordo com o local da página.</span><span class="sxs-lookup"><span data-stu-id="0f98c-202">The `Domain` and `Path` values are auto-filled according to the location of the page.</span></span>  

<span data-ttu-id="0f98c-203">As colunas da lista Cookies são sortíveis:</span><span class="sxs-lookup"><span data-stu-id="0f98c-203">The columns of the Cookies list are sortable:</span></span>

| <span data-ttu-id="0f98c-204">Coluna</span><span class="sxs-lookup"><span data-stu-id="0f98c-204">Column</span></span> | <span data-ttu-id="0f98c-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f98c-205">Description</span></span> |  
| :--- | :--- |  
| <span data-ttu-id="0f98c-206">Name</span><span class="sxs-lookup"><span data-stu-id="0f98c-206">Name</span></span> | <span data-ttu-id="0f98c-207">Nome do cookie</span><span class="sxs-lookup"><span data-stu-id="0f98c-207">Name of the cookie</span></span> |  
| <span data-ttu-id="0f98c-208">Value</span><span class="sxs-lookup"><span data-stu-id="0f98c-208">Value</span></span> | <span data-ttu-id="0f98c-209">Valor do cookie</span><span class="sxs-lookup"><span data-stu-id="0f98c-209">Value of the cookie</span></span> |  
| <span data-ttu-id="0f98c-210">Domínio</span><span class="sxs-lookup"><span data-stu-id="0f98c-210">Domain</span></span> | <span data-ttu-id="0f98c-211">Nome do host do cookie \(pode estar vazio\)</span><span class="sxs-lookup"><span data-stu-id="0f98c-211">Host name of the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="0f98c-212">Caminho</span><span class="sxs-lookup"><span data-stu-id="0f98c-212">Path</span></span> | <span data-ttu-id="0f98c-213">Caminho da URL para o cookie \(pode estar vazio\)</span><span class="sxs-lookup"><span data-stu-id="0f98c-213">URL path for the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="0f98c-214">Expira</span><span class="sxs-lookup"><span data-stu-id="0f98c-214">Expires</span></span> | <span data-ttu-id="0f98c-215">Duração máxima do cookie como um data/hora HTTP.</span><span class="sxs-lookup"><span data-stu-id="0f98c-215">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span>  <span data-ttu-id="0f98c-216">Se não `Expires` tiver `Max-Age` sido definido, a entrada será considerada um cookie de sessão.</span><span class="sxs-lookup"><span data-stu-id="0f98c-216">If no `Expires` or `Max-Age` was set, the entry is considered a Session cookie.</span></span>  |  
| <span data-ttu-id="0f98c-217">Somente HTTP</span><span class="sxs-lookup"><span data-stu-id="0f98c-217">HTTP only</span></span> | <span data-ttu-id="0f98c-218">Indica se o cookie foi definido com `HttpOnly` diretiva, indicando que ele está inacessível do JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f98c-218">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span> |  
| <span data-ttu-id="0f98c-219">Proteja</span><span class="sxs-lookup"><span data-stu-id="0f98c-219">Secure</span></span> | <span data-ttu-id="0f98c-220">Indica se o cookie foi definido com a diretiva, indicando que ele só será enviado para o servidor a partir de uma solicitação usando `Secure` SSL e o protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0f98c-220">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>  |  

<span data-ttu-id="0f98c-221">Consulte a referência [set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) de documentos da **Web MDN** para obter mais detalhes sobre propriedades de cookie.</span><span class="sxs-lookup"><span data-stu-id="0f98c-221">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>  

### <a name="context-menu"></a><span data-ttu-id="0f98c-222">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="0f98c-222">Context menu</span></span>  

<span data-ttu-id="0f98c-223">Além da barra de ferramentas da guia [Cookies,](#cookies-manager)você também pode gerenciar seus cookies no **menu** Contexto com o botão direito do mouse e/ou os [atalhos de teclado.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="0f98c-223">In addition to the Cookies tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="0f98c-224">Atalhos</span><span class="sxs-lookup"><span data-stu-id="0f98c-224">Shortcuts</span></span>  

| <span data-ttu-id="0f98c-225">Ação</span><span class="sxs-lookup"><span data-stu-id="0f98c-225">Action</span></span> | <span data-ttu-id="0f98c-226">Atalho</span><span class="sxs-lookup"><span data-stu-id="0f98c-226">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0f98c-227">Atualizar</span><span class="sxs-lookup"><span data-stu-id="0f98c-227">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="0f98c-228">Excluir cookie</span><span class="sxs-lookup"><span data-stu-id="0f98c-228">Delete cookie</span></span> | `Del` |  
| <span data-ttu-id="0f98c-229">Excluir todos os cookies</span><span class="sxs-lookup"><span data-stu-id="0f98c-229">Delete all cookies</span></span> | `Ctrl`+`Shift`+`Del` |  
| <span data-ttu-id="0f98c-230">Excluir todos os cookies de sessão</span><span class="sxs-lookup"><span data-stu-id="0f98c-230">Delete all session cookies</span></span> | `Ctrl`+`Del` |  
| <span data-ttu-id="0f98c-231">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="0f98c-231">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="0f98c-232">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="0f98c-232">Select all</span></span> | `Ctrl`+`A` |  

### <a name="cache-manager"></a><span data-ttu-id="0f98c-233">Gerenciador de cache</span><span class="sxs-lookup"><span data-stu-id="0f98c-233">Cache manager</span></span>  

<span data-ttu-id="0f98c-234">Clicar em uma entrada de cache específica abrirá o Gerenciador de **Cache** de funcionários do serviço, onde você pode inspecionar e, opcionalmente, excluir entradas de cache \( e pares de `Request` `Response` chave/valor\):</span><span class="sxs-lookup"><span data-stu-id="0f98c-234">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries \(`Request` and `Response` key/value pairs\):</span></span>  

![Gerenciador de cache](./media/storage_cache.png)  

### <a name="shortcuts"></a><span data-ttu-id="0f98c-236">Atalhos</span><span class="sxs-lookup"><span data-stu-id="0f98c-236">Shortcuts</span></span>  

#### <a name="cache-manager"></a><span data-ttu-id="0f98c-237">Gerenciador de cache</span><span class="sxs-lookup"><span data-stu-id="0f98c-237">Cache manager</span></span>  

| <span data-ttu-id="0f98c-238">Ação</span><span class="sxs-lookup"><span data-stu-id="0f98c-238">Action</span></span> | <span data-ttu-id="0f98c-239">Atalho</span><span class="sxs-lookup"><span data-stu-id="0f98c-239">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0f98c-240">Atualizar</span><span class="sxs-lookup"><span data-stu-id="0f98c-240">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="0f98c-241">Excluir item</span><span class="sxs-lookup"><span data-stu-id="0f98c-241">Delete item</span></span> | `Del` |  
| <span data-ttu-id="0f98c-242">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="0f98c-242">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="0f98c-243">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="0f98c-243">Select all</span></span> | `Ctrl`+`A` |  
