---
description: Usar o painel armazenamento para inspecionar o armazenamento da Web, IndexedDB, cookies e caches de solicitação/resposta
title: DevTools-armazenamento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, armazenamento na Web, armazenamento local, armazenamento de sessão, IndexedDB, cookies, trabalho do serviço, cache
ms.custom: seodec18
ms.openlocfilehash: 8de6e1f90f86fa09b116646918c6be1d8cfb0a72
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561387"
---
# <span data-ttu-id="95bba-104">Armazenamento</span><span class="sxs-lookup"><span data-stu-id="95bba-104">Storage</span></span>

<span data-ttu-id="95bba-105">Use o painel **armazenamento** para inspecionar e gerenciar vários dados armazenados em cache localmente, incluindo:</span><span class="sxs-lookup"><span data-stu-id="95bba-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>

 - <span data-ttu-id="95bba-106">Pares de chave/valores de [armazenamento na Web](#local-and-session-storage-managers) (armazenamento*local* e de *sessão* )</span><span class="sxs-lookup"><span data-stu-id="95bba-106">[Web storage](#local-and-session-storage-managers) (*Local* and *Session* storage) key/values pairs</span></span>
 - <span data-ttu-id="95bba-107">Dados estruturados do [BD indexado](#indexeddb-manager)</span><span class="sxs-lookup"><span data-stu-id="95bba-107">[Indexed DB](#indexeddb-manager) structured data</span></span>
 - <span data-ttu-id="95bba-108">[Cookies](#cookies-list) para o domínio</span><span class="sxs-lookup"><span data-stu-id="95bba-108">[Cookies](#cookies-list) for the domain</span></span>
 - <span data-ttu-id="95bba-109">[Cache](#cache-manager) (pares de solicitação/resposta) para depuração do trabalho do serviço</span><span class="sxs-lookup"><span data-stu-id="95bba-109">[Cache](#cache-manager) (request/response pairs) for service worker debugging</span></span>

<span data-ttu-id="95bba-110">Expanda qualquer uma dessas categorias e clique em uma entrada de filho para abrir a guia do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="95bba-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>

## <span data-ttu-id="95bba-111">Gerentes de armazenamento local e de sessão</span><span class="sxs-lookup"><span data-stu-id="95bba-111">Local and Session storage managers</span></span>

<span data-ttu-id="95bba-112">Use o *Gerenciador de armazenamento local* e o *Gerenciador de armazenamento de sessão* para inspecionar e gerenciar o armazenamento na Web da sua página.</span><span class="sxs-lookup"><span data-stu-id="95bba-112">Use the *Local Storage manager* and *Session Storage manager* to inspect and manage the web storage for  your page.</span></span> 

<span data-ttu-id="95bba-113">As pastas armazenamento **local** e **sessão de armazenamento de sessão** dentro do [*seletor de recursos*](./debugger.md#resource-picker) do painel de armazenamento exibem uma lista de origens para a página.</span><span class="sxs-lookup"><span data-stu-id="95bba-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [*Resource picker*](./debugger.md#resource-picker) display a list of origins for the page.</span></span> <span data-ttu-id="95bba-114">Selecionar um desses quadros abre uma tabela editável dos pares de chave/valor atuais definidos por meio de [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivamente (e/ou definido diretamente da [lista armazenamento](#storage-list)devtools).</span><span class="sxs-lookup"><span data-stu-id="95bba-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively (and/or set directly from the  DevTools [Storage list](#storage-list)).</span></span>

![Gerenciador de cookies DevTools](./media/storage_web_storage.png)

<span data-ttu-id="95bba-116">Nas guias *armazenamento local* e *armazenamento de sessão* , você pode:</span><span class="sxs-lookup"><span data-stu-id="95bba-116">From the *Local Storage* and *Session Storage* tabs you can:</span></span>

 - <span data-ttu-id="95bba-117">**Refresh** ( `Ctrl+F5` ) a [lista de armazenamento](#cookies-list) para ver o conjunto atual de pares de chave/valores para o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="95bba-117">**Refresh** (`Ctrl+F5`) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span> <span data-ttu-id="95bba-118">(A lista não é atualizada automaticamente após as atualizações de script.)</span><span class="sxs-lookup"><span data-stu-id="95bba-118">(The list does not auto-refresh upon script updates.)</span></span>
 - <span data-ttu-id="95bba-119">**Simule alcançar o limite de armazenamento para o** armazenamento na Web do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="95bba-119">**Simulate reaching the storage limit** for Microsoft Edge web storage.</span></span> <span data-ttu-id="95bba-120">Cada domínio e subdomínio tem sua própria área de armazenamento, no entanto, há um limite combinado:</span><span class="sxs-lookup"><span data-stu-id="95bba-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>
    - <span data-ttu-id="95bba-121">**Subdomínios:** até 5 MBS de espaço</span><span class="sxs-lookup"><span data-stu-id="95bba-121">**Subdomains:** up to 5 MBs of space</span></span>
    - <span data-ttu-id="95bba-122">**Domínios:** até 10 MBs de espaço</span><span class="sxs-lookup"><span data-stu-id="95bba-122">**Domains:** up to 10 MBs of space</span></span>
    - <span data-ttu-id="95bba-123">**Total para todos os domínios:** até 50 MBS de espaço</span><span class="sxs-lookup"><span data-stu-id="95bba-123">**Total for all domains:** up to 50 MBs of space</span></span>

   <span data-ttu-id="95bba-124">O armazenamento da sessão é limpo assim que a última guia do navegador que faz referência à sua origem é fechada.</span><span class="sxs-lookup"><span data-stu-id="95bba-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span> <span data-ttu-id="95bba-125">As entradas de armazenamento local persistem indefinidamente até serem desmarcadas de forma programática pela página ou manualmente pelo usuário:</span><span class="sxs-lookup"><span data-stu-id="95bba-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>

   <span data-ttu-id="95bba-126">**Configurações**  >  de **Limpar dados**  >  de navegação **Cookies e dados de sites salvos**</span><span class="sxs-lookup"><span data-stu-id="95bba-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

![Limpar dados de navegação do painel configurações do Microsoft Edge](./media/settings_clear_browsing_data.png)

### <span data-ttu-id="95bba-128">Lista de armazenamento</span><span class="sxs-lookup"><span data-stu-id="95bba-128">Storage list</span></span>

<span data-ttu-id="95bba-129">Na tabela de *lista de armazenamento* , você pode:</span><span class="sxs-lookup"><span data-stu-id="95bba-129">From the *Storage list* table you can:</span></span>

 - <span data-ttu-id="95bba-130">**Inspecione e classifique** os pares de chave/valor clicando em um dos nomes de coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="95bba-130">**Inspect and sort** your key/value pairs by clicking on either column name in the table.</span></span>
 - <span data-ttu-id="95bba-131">**Edite** a *chave* e o *valor* de uma entrada existente clicando na célula.</span><span class="sxs-lookup"><span data-stu-id="95bba-131">**Edit** the *Key* and *Value* of an existing entry by clicking in the cell.</span></span>
 - <span data-ttu-id="95bba-132">**Delete** ( `Del` ) uma entrada da opção de menu de contexto clique com o botão direito do mouse em *Excluir item*.</span><span class="sxs-lookup"><span data-stu-id="95bba-132">**Delete** (`Del`) an entry from the right-click context menu option, *Delete item*.</span></span>
 - <span data-ttu-id="95bba-133">**Adicione** um novo par de chave/valor clicando na linha vazia na parte inferior da tabela.</span><span class="sxs-lookup"><span data-stu-id="95bba-133">**Add** a new key/value pair by clicking on the empty row at the bottom of the table.</span></span>


### <span data-ttu-id="95bba-134">Teclado</span><span class="sxs-lookup"><span data-stu-id="95bba-134">Shortcuts</span></span>

| <span data-ttu-id="95bba-135">Ação</span><span class="sxs-lookup"><span data-stu-id="95bba-135">Action</span></span>              | <span data-ttu-id="95bba-136">Atalho</span><span class="sxs-lookup"><span data-stu-id="95bba-136">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="95bba-137">Atualizar</span><span class="sxs-lookup"><span data-stu-id="95bba-137">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="95bba-138">Excluir item</span><span class="sxs-lookup"><span data-stu-id="95bba-138">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="95bba-139">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="95bba-139">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="95bba-140">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="95bba-140">Select all</span></span>          | `Ctrl` + `A`  |


## <span data-ttu-id="95bba-141">IndexedDB Manager</span><span class="sxs-lookup"><span data-stu-id="95bba-141">IndexedDB manager</span></span>

<span data-ttu-id="95bba-142">Use a guia **IndexedDB** para inspecionar e gerenciar os dados estruturados armazenados localmente em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="95bba-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span> <span data-ttu-id="95bba-143">Especificamente, você pode inspecionar/classificar e atualizar os repositórios de objetos e índices e também excluir entradas de valores chave individuais.</span><span class="sxs-lookup"><span data-stu-id="95bba-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>

> [!TIP]
> <span data-ttu-id="95bba-144">Você pode usar a demonstração do [mixer de áudio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) para testar a unidade do *IndexedDB Manager* no Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="95bba-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>

<span data-ttu-id="95bba-145">Para excluir todos os dados do IndexedDB armazenados para o usuário atual no Microsoft Edge, use o menu *configurações* do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="95bba-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge *Settings* menu:</span></span>

<span data-ttu-id="95bba-146">**...** >  **Configurações**  >  de **Limpar dados**  >  de navegação **Cookies e dados de sites salvos**</span><span class="sxs-lookup"><span data-stu-id="95bba-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

<span data-ttu-id="95bba-147">A pasta **IndexedDB** dentro do [*seletor de recursos*](./debugger.md#resource-picker) do depurador exibe uma lista de origens dos recursos carregados pela página.</span><span class="sxs-lookup"><span data-stu-id="95bba-147">The **IndexedDB** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="95bba-148">Qualquer banco de dados IndexedDB (IDB) estará listado na origem, juntamente com seus armazenamentos de objetos.</span><span class="sxs-lookup"><span data-stu-id="95bba-148">Any IndexedDB (IDB) databases will be listed under the origin, along with their object stores.</span></span> 

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)

### <span data-ttu-id="95bba-150">Barra de ferramentas IndexedDB</span><span class="sxs-lookup"><span data-stu-id="95bba-150">IndexedDB Toolbar</span></span>

<span data-ttu-id="95bba-151">Na barra de ferramentas do *IndexedDB* , você pode:</span><span class="sxs-lookup"><span data-stu-id="95bba-151">From the *IndexedDB* toolbar you can:</span></span>

 - <span data-ttu-id="95bba-152">**Refresh** ( `Ctrl+F5` ) para ver as entradas atuais no repositório de objetos ou índice do seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="95bba-152">**Refresh** (`Ctrl+F5`) to see the current entries in the object store or index of your database.</span></span> <span data-ttu-id="95bba-153">O Gerenciador de IndexedDB não é atualizado automaticamente quando são feitas alterações em seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="95bba-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>

### <span data-ttu-id="95bba-154">Lista de entradas do repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="95bba-154">Object store entries list</span></span>

<span data-ttu-id="95bba-155">No *repositório de objetos* ou na tabela de *índice* , você pode:</span><span class="sxs-lookup"><span data-stu-id="95bba-155">From the *Object store* or *Index* table you can:</span></span>

 - <span data-ttu-id="95bba-156">**Inspecione e classifique** os pares de valor chave clicando em qualquer nome de coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="95bba-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="95bba-157">**Refresh** ( `Ctrl+F5` )</span><span class="sxs-lookup"><span data-stu-id="95bba-157">**Refresh** (`Ctrl+F5`)</span></span>
 - <span data-ttu-id="95bba-158">**Excluir item** ( `Del` ) para remover a entrada selecionada em seu repositório de objetos ou índice.</span><span class="sxs-lookup"><span data-stu-id="95bba-158">**Delete item** (`Del`) to remove the selected entry in your object store or index.</span></span> <span data-ttu-id="95bba-159">Você também pode fazer isso a partir da opção de [menu de contexto](#context-menu) clique com o botão direito do mouse em *Excluir item*.</span><span class="sxs-lookup"><span data-stu-id="95bba-159">You can also do this from the right-click [context menu](#context-menu) option, *Delete item*.</span></span>
 - <span data-ttu-id="95bba-160">**Copiar itens selecionados** ( `Ctrl+C` ) para copiar o item selecionado para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="95bba-160">**Copy selected items** (`Ctrl+C`) to copy the selected item to your clipboard.</span></span> <span data-ttu-id="95bba-161">Você também pode fazer isso a partir da opção de [menu de contexto](#context-menu) clique com o botão direito do mouse, *Copiar item selecionado*.</span><span class="sxs-lookup"><span data-stu-id="95bba-161">You can also do this from the right-click [context menu](#context-menu) option, *Copy selected item*.</span></span>
 - <span data-ttu-id="95bba-162">**Selecionar tudo** ( `Ctrl+A` ) para selecionar todas as entradas no repositório de objetos ou índice.</span><span class="sxs-lookup"><span data-stu-id="95bba-162">**Select all** (`Ctrl+A`) to select all the entries in your object store or index.</span></span> <span data-ttu-id="95bba-163">Você também pode fazer isso a partir da opção de [menu de contexto](#context-menu) clique com o botão direito do mouse, *Selecione todos*.</span><span class="sxs-lookup"><span data-stu-id="95bba-163">You can also do this from the right-click [context menu](#context-menu) option, *Select all*.</span></span>

<span data-ttu-id="95bba-164">As colunas do *repositório de objetos* ou da tabela de *índice* são classificável:</span><span class="sxs-lookup"><span data-stu-id="95bba-164">The columns of the *Object store* or *Index* table are sortable:</span></span>

<span data-ttu-id="95bba-165">Coluna</span><span class="sxs-lookup"><span data-stu-id="95bba-165">Column</span></span> | <span data-ttu-id="95bba-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="95bba-166">Description</span></span>
:------------ | :-------------
<span data-ttu-id="95bba-167">Chave</span><span class="sxs-lookup"><span data-stu-id="95bba-167">Key</span></span> | <span data-ttu-id="95bba-168">Nome do par chave-valor (igual à *chave primária*) ao iterar em um repositório de objetos; Nome da chave de índice (chave atual do cursor) ao iterar em um índice</span><span class="sxs-lookup"><span data-stu-id="95bba-168">Name of the key-value pair (same as *Primary Key*) when iterating over an object store; Name of the index key (cursor's current key) when iterating over an index</span></span>
<span data-ttu-id="95bba-169">Chave primária</span><span class="sxs-lookup"><span data-stu-id="95bba-169">Primary Key</span></span> | <span data-ttu-id="95bba-170">Nome do par chave-valor (consulte *documentos da Web do MDN* para obter mais informações sobre [chaves](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)idb)</span><span class="sxs-lookup"><span data-stu-id="95bba-170">Name of the key-value pair (see *MDN web docs* for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database))</span></span>
<span data-ttu-id="95bba-171">Value</span><span class="sxs-lookup"><span data-stu-id="95bba-171">Value</span></span> | <span data-ttu-id="95bba-172">Valor do par chave-valor</span><span class="sxs-lookup"><span data-stu-id="95bba-172">Value of the key-value pair</span></span>

<span data-ttu-id="95bba-173">Confira os *documentos da Web do MDN* para saber mais sobre os [conceitos e uso do IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span><span class="sxs-lookup"><span data-stu-id="95bba-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>

### <span data-ttu-id="95bba-174">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="95bba-174">Context menu</span></span>

<span data-ttu-id="95bba-175">Além da barra de [ferramentas *IndexedDB* ](#indexeddb-toolbar), você também pode gerenciar seus dados em repositórios de objetos ou índices no menu de **contexto** de clique com o botão direito do mouse e/ou nos [atalhos](#shortcuts)de teclado.</span><span class="sxs-lookup"><span data-stu-id="95bba-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="95bba-176">Teclado</span><span class="sxs-lookup"><span data-stu-id="95bba-176">Shortcuts</span></span>

<span data-ttu-id="95bba-177">Ação</span><span class="sxs-lookup"><span data-stu-id="95bba-177">Action</span></span> | <span data-ttu-id="95bba-178">Atalho</span><span class="sxs-lookup"><span data-stu-id="95bba-178">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="95bba-179">Atualizar</span><span class="sxs-lookup"><span data-stu-id="95bba-179">Refresh</span></span> | `Ctrl` + `F5`
<span data-ttu-id="95bba-180">Excluir par chave-valor</span><span class="sxs-lookup"><span data-stu-id="95bba-180">Delete key-value pair</span></span> | `Del`
<span data-ttu-id="95bba-181">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="95bba-181">Copy selected items</span></span> | `Ctrl` + `C`
<span data-ttu-id="95bba-182">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="95bba-182">Select all</span></span> | `Ctrl` + `A`

## <span data-ttu-id="95bba-183">Gerenciador de cookies</span><span class="sxs-lookup"><span data-stu-id="95bba-183">Cookies manager</span></span>

<span data-ttu-id="95bba-184">Use o *Gerenciador de cookies* para inspecionar e gerenciar os cookies para o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="95bba-184">Use the *Cookies manager* to inspect and manage the cookies for the given domain.</span></span> 

<span data-ttu-id="95bba-185">A pasta **cookies** dentro do [*seletor de recursos*](./debugger.md#resource-picker) do depurador exibe uma lista de origens dos recursos carregados pela página.</span><span class="sxs-lookup"><span data-stu-id="95bba-185">The **Cookies** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="95bba-186">Selecionar um desses quadros abre uma tabela que representa os cookies atuais definidos por um cabeçalho [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou por meio de um script com [Document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="95bba-186">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>

![Gerenciador de cookies DevTools](./media/storage_cookies.png)

<span data-ttu-id="95bba-188">Na barra de ferramentas da guia *cookies* , você pode:</span><span class="sxs-lookup"><span data-stu-id="95bba-188">From the *Cookies* tab toolbar you can:</span></span>

 - <span data-ttu-id="95bba-189">**Refresh** ( `Ctrl+F5` ) a [lista de cookies](#cookies-list) para ver o conjunto atual de cookies para o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="95bba-189">**Refresh** (`Ctrl+F5`) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span> <span data-ttu-id="95bba-190">(A lista não é atualizada automaticamente.)</span><span class="sxs-lookup"><span data-stu-id="95bba-190">(The list does not auto-refresh.)</span></span>
 - <span data-ttu-id="95bba-191">**Exclua todos os cookies** ( `Ctrl+Shift+Del` ) (sessão e permanentes) para o caminho da página atual.</span><span class="sxs-lookup"><span data-stu-id="95bba-191">**Delete all cookies** (`Ctrl+Shift+Del`) (session and permanent) for the path of the current page.</span></span>
 - <span data-ttu-id="95bba-192">**Exclua todos os cookies de sessão** ( `Ctrl+Del` ) para o caminho da página atual.</span><span class="sxs-lookup"><span data-stu-id="95bba-192">**Delete all session cookies** (`Ctrl+Del`) for the path of the current page.</span></span>

<span data-ttu-id="95bba-193">Para limpar completamente a *lista de cookies*, talvez seja necessário **limpar todos os cookies do domínio** da barra de ferramentas painel de [**rede**](./network.md#toolbar) .</span><span class="sxs-lookup"><span data-stu-id="95bba-193">To completely clear your *Cookies list*, you might need to **Clear all cookies for the domain** from the [**Network**](./network.md#toolbar) panel toolbar.</span></span>

### <span data-ttu-id="95bba-194">Lista de cookies</span><span class="sxs-lookup"><span data-stu-id="95bba-194">Cookies list</span></span>

<span data-ttu-id="95bba-195">Na tabela *lista de cookies* , você pode:</span><span class="sxs-lookup"><span data-stu-id="95bba-195">From the *Cookies list* table you can:</span></span>

 - <span data-ttu-id="95bba-196">**Inspecione e classifique** seus cookies clicando em qualquer nome de coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="95bba-196">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="95bba-197">**Edite** o *nome* e o *valor* de um cookie existente clicando na célula.</span><span class="sxs-lookup"><span data-stu-id="95bba-197">**Edit** the *Name* and *Value* of an existing cookie by clicking in the cell.</span></span>
 - <span data-ttu-id="95bba-198">**Delete** ( `Del` ) um cookie da opção de menu de [contexto](#context-menu) clique com o botão direito do mouse em *excluir cookie*.</span><span class="sxs-lookup"><span data-stu-id="95bba-198">**Delete** (`Del`) a cookie from the right-click [context menu](#context-menu) option, *Delete cookie*.</span></span>
 - <span data-ttu-id="95bba-199">**Adicione** um novo cookie de sessão para o *domínio/caminho* fornecido clicando na linha vazia na parte inferior da tabela.</span><span class="sxs-lookup"><span data-stu-id="95bba-199">**Add** a new session cookie for the given *Domain/Path* by clicking on the empty row at the bottom of the table.</span></span> <span data-ttu-id="95bba-200">Isso só funciona com cookies de sessão; os cookies permanentes (com datas de vencimento específicas) devem ser definidos com métodos tradicionais.</span><span class="sxs-lookup"><span data-stu-id="95bba-200">This only works for session cookies; permanent cookies (with specific expiry dates) must be set with traditional methods.</span></span> <span data-ttu-id="95bba-201">Os valores de *domínio* e de *caminho* são preenchidos automaticamente de acordo com o local da página.</span><span class="sxs-lookup"><span data-stu-id="95bba-201">The *Domain* and *Path* values are auto-filled according to the location of the page.</span></span>

<span data-ttu-id="95bba-202">As colunas da *lista de cookies* são classificável:</span><span class="sxs-lookup"><span data-stu-id="95bba-202">The columns of the *Cookies list* are sortable:</span></span>

<span data-ttu-id="95bba-203">Coluna</span><span class="sxs-lookup"><span data-stu-id="95bba-203">Column</span></span> | <span data-ttu-id="95bba-204">Descrição</span><span class="sxs-lookup"><span data-stu-id="95bba-204">Description</span></span>
:------------ | :-------------
<span data-ttu-id="95bba-205">Name</span><span class="sxs-lookup"><span data-stu-id="95bba-205">Name</span></span> | <span data-ttu-id="95bba-206">Nome do cookie</span><span class="sxs-lookup"><span data-stu-id="95bba-206">Name of the cookie</span></span>
<span data-ttu-id="95bba-207">Value</span><span class="sxs-lookup"><span data-stu-id="95bba-207">Value</span></span> | <span data-ttu-id="95bba-208">Valor do cookie</span><span class="sxs-lookup"><span data-stu-id="95bba-208">Value of the cookie</span></span>
<span data-ttu-id="95bba-209">Domínio</span><span class="sxs-lookup"><span data-stu-id="95bba-209">Domain</span></span> | <span data-ttu-id="95bba-210">Nome do host do cookie (pode estar vazio)</span><span class="sxs-lookup"><span data-stu-id="95bba-210">Host name of the cookie (may be empty)</span></span>
<span data-ttu-id="95bba-211">Caminho</span><span class="sxs-lookup"><span data-stu-id="95bba-211">Path</span></span> | <span data-ttu-id="95bba-212">Caminho da URL para o cookie (pode estar vazio)</span><span class="sxs-lookup"><span data-stu-id="95bba-212">URL path for the cookie (may be empty)</span></span>
<span data-ttu-id="95bba-213">Expira</span><span class="sxs-lookup"><span data-stu-id="95bba-213">Expires</span></span> | <span data-ttu-id="95bba-214">Tempo de vida máximo do cookie como um carimbo de data/hora HTTP.</span><span class="sxs-lookup"><span data-stu-id="95bba-214">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span> <span data-ttu-id="95bba-215">Se não `Expires` `Max-Age` for definido, a entrada será considerada um cookie de *sessão* .</span><span class="sxs-lookup"><span data-stu-id="95bba-215">If no `Expires` or `Max-Age` was set, the entry is considered a *Session* cookie.</span></span>
<span data-ttu-id="95bba-216">Somente HTTP</span><span class="sxs-lookup"><span data-stu-id="95bba-216">HTTP only</span></span> | <span data-ttu-id="95bba-217">Indica se o cookie foi definido com a `HttpOnly` diretiva, indicando que ele não está acessível a partir de JavaScript</span><span class="sxs-lookup"><span data-stu-id="95bba-217">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span>
<span data-ttu-id="95bba-218">Proteja</span><span class="sxs-lookup"><span data-stu-id="95bba-218">Secure</span></span> | <span data-ttu-id="95bba-219">Indica se o cookie foi definido com a `Secure` diretiva, indicando que ele só será enviado para o servidor a partir de uma solicitação usando SSL e o protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="95bba-219">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>

<span data-ttu-id="95bba-220">Consulte a referência do **MDN Web docs** [Set-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) para ver mais detalhes sobre as propriedades do cookie.</span><span class="sxs-lookup"><span data-stu-id="95bba-220">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>

### <span data-ttu-id="95bba-221">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="95bba-221">Context menu</span></span>

<span data-ttu-id="95bba-222">Além da [barra de ferramentas](#cookies-manager)da guia *cookies* , você também pode gerenciar seus cookies do **menu de contexto** de clique com o botão direito do mouse e/ou os [atalhos](#shortcuts)de teclado.</span><span class="sxs-lookup"><span data-stu-id="95bba-222">In addition to the *Cookies* tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="95bba-223">Teclado</span><span class="sxs-lookup"><span data-stu-id="95bba-223">Shortcuts</span></span>

| <span data-ttu-id="95bba-224">Ação</span><span class="sxs-lookup"><span data-stu-id="95bba-224">Action</span></span>                     | <span data-ttu-id="95bba-225">Atalho</span><span class="sxs-lookup"><span data-stu-id="95bba-225">Shortcut</span></span>                 |
|:---------------------------|:-------------------------|
| <span data-ttu-id="95bba-226">Atualizar</span><span class="sxs-lookup"><span data-stu-id="95bba-226">Refresh</span></span>                    | `Ctrl` + `F5`            |
| <span data-ttu-id="95bba-227">Excluir cookie</span><span class="sxs-lookup"><span data-stu-id="95bba-227">Delete cookie</span></span>              | `Del`                    |
| <span data-ttu-id="95bba-228">Excluir todos os cookies</span><span class="sxs-lookup"><span data-stu-id="95bba-228">Delete all cookies</span></span>         | `Ctrl` + `Shift` + `Del` |
| <span data-ttu-id="95bba-229">Excluir todos os cookies de sessão</span><span class="sxs-lookup"><span data-stu-id="95bba-229">Delete all session cookies</span></span> | `Ctrl` + `Del`           |
| <span data-ttu-id="95bba-230">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="95bba-230">Copy selected items</span></span>        | `Ctrl` + `C`             |
| <span data-ttu-id="95bba-231">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="95bba-231">Select all</span></span>                 | `Ctrl` + `A`             |

### <span data-ttu-id="95bba-232">Gerenciador de cache</span><span class="sxs-lookup"><span data-stu-id="95bba-232">Cache manager</span></span>

<span data-ttu-id="95bba-233">Clicar em uma entrada de cache específica abrirá o Gerenciador de **cache** do trabalho do serviço, onde você pode inspecionar e, opcionalmente, excluir entradas de cache (pares de*solicitação* e *resposta* /valor):</span><span class="sxs-lookup"><span data-stu-id="95bba-233">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs):</span></span>

![Gerenciador de cache](./media/storage_cache.png)

### <span data-ttu-id="95bba-235">Teclado</span><span class="sxs-lookup"><span data-stu-id="95bba-235">Shortcuts</span></span>

#### <span data-ttu-id="95bba-236">Gerenciador de cache</span><span class="sxs-lookup"><span data-stu-id="95bba-236">Cache manager</span></span>

| <span data-ttu-id="95bba-237">Ação</span><span class="sxs-lookup"><span data-stu-id="95bba-237">Action</span></span>              | <span data-ttu-id="95bba-238">Atalho</span><span class="sxs-lookup"><span data-stu-id="95bba-238">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="95bba-239">Atualizar</span><span class="sxs-lookup"><span data-stu-id="95bba-239">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="95bba-240">Excluir item</span><span class="sxs-lookup"><span data-stu-id="95bba-240">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="95bba-241">Copiar itens selecionados</span><span class="sxs-lookup"><span data-stu-id="95bba-241">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="95bba-242">Selecionar tudo</span><span class="sxs-lookup"><span data-stu-id="95bba-242">Select all</span></span>          | `Ctrl` + `A`  |
