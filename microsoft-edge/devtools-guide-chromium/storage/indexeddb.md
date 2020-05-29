---
title: Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612085"
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





# <span data-ttu-id="5b253-103">Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5b253-103">View And Change IndexedDB Data With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="5b253-104">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir e alterar dados do [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="5b253-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="5b253-105">Ele pressupõe que você esteja familiarizado com o DevTools.</span><span class="sxs-lookup"><span data-stu-id="5b253-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="5b253-106">Ele também pressupõe que você esteja familiarizado com o IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="5b253-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="5b253-107">Caso contrário, consulte [usando o IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="5b253-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="5b253-108">Exibir dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="5b253-109">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="5b253-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="5b253-110">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="5b253-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="5b253-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="5b253-111">Figure 1</span></span>  
    > <span data-ttu-id="5b253-112">Painel de manifesto</span><span class="sxs-lookup"><span data-stu-id="5b253-112">The Manifest pane</span></span>  
    > ![Painel de manifesto][ImageManifest]  

1.  <span data-ttu-id="5b253-114">Expanda o menu **IndexedDB** para ver quais bancos de dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5b253-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    > ##### <span data-ttu-id="5b253-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="5b253-115">Figure 2</span></span>  
    > <span data-ttu-id="5b253-116">O menu **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="5b253-116">The **IndexedDB** menu</span></span>  
    > ![O menu IndexedDB][ImageIndexedDBMenu]  
    
    *   ![<span data-ttu-id="5b253-118">Ícone de banco de dados ][ImageDatabaseIcon] `notes - https://mdn.github.io` representa um banco de dados, onde `notes` é o nome do banco de dados e `https://mdn.github.io` é a origem que acessa o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5b253-118">Database icon][ImageDatabaseIcon] `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   ![<span data-ttu-id="5b253-119">][ImageObjectStoreIcon] `notes` O ícone de repositório de objetos é um repositório de objetos.</span><span class="sxs-lookup"><span data-stu-id="5b253-119">Object Store icon][ImageObjectStoreIcon] `notes` is an object store.</span></span>  
    *   <span data-ttu-id="5b253-120">**título** e **corpo** são [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="5b253-120">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b253-121">**Limitação conhecida**  Os bancos de dados de terceiros não estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="5b253-121">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="5b253-122">Por exemplo, se você usar um `<iframe>` para inserir um anúncio em sua página, e sua rede de AD usar o IndexedDB, os dados do IndexedDB para a sua rede de anúncios não serão visíveis.</span><span class="sxs-lookup"><span data-stu-id="5b253-122">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="5b253-123">Veja o [problema #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="5b253-123">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="5b253-124">Selecione um banco de dados para ver a origem e o número da versão.</span><span class="sxs-lookup"><span data-stu-id="5b253-124">Select a database to see the origin and version number.</span></span>  
    
    > ##### <span data-ttu-id="5b253-125">Figura 3</span><span class="sxs-lookup"><span data-stu-id="5b253-125">Figure 3</span></span>  
    > <span data-ttu-id="5b253-126">O banco de dados **anotações**</span><span class="sxs-lookup"><span data-stu-id="5b253-126">The **notes** database</span></span>  
    > ![O banco de dados anotações][ImageIndexedDBDatabase]  
    
1.  <span data-ttu-id="5b253-128">Selecione um repositório de objetos para ver os pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="5b253-128">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b253-129">Os dados do IndexedDB não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="5b253-129">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="5b253-130">Consulte [atualizar dados do IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="5b253-130">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="5b253-131">Figura 4</span><span class="sxs-lookup"><span data-stu-id="5b253-131">Figure 4</span></span>  
    > <span data-ttu-id="5b253-132">O repositório de objetos **anotações**</span><span class="sxs-lookup"><span data-stu-id="5b253-132">The **notes** object store</span></span>  
    > ![O repositório de objetos anotações][ImageIndexedDBObjectStore]  

    *   <span data-ttu-id="5b253-134">**Total de entradas** é o número total de pares de valores chave no repositório de objetos.</span><span class="sxs-lookup"><span data-stu-id="5b253-134">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="5b253-135">O **valor do gerador de chave** é a próxima chave disponível.</span><span class="sxs-lookup"><span data-stu-id="5b253-135">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="5b253-136">Este campo é mostrado apenas ao usar [geradores de chaves][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="5b253-136">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  

1.  <span data-ttu-id="5b253-137">Selecione uma célula na coluna **valor** para expandir esse valor.</span><span class="sxs-lookup"><span data-stu-id="5b253-137">Select a cell in the **Value** column to expand that value.</span></span>  
    
    > ##### <span data-ttu-id="5b253-138">Figura 5</span><span class="sxs-lookup"><span data-stu-id="5b253-138">Figure 5</span></span>  
    > <span data-ttu-id="5b253-139">Exibindo um valor de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-139">Viewing an IndexedDB value</span></span>  
    > ![Exibindo um valor de IndexedDB][ImageIndexedBDValue]  
    
1.  <span data-ttu-id="5b253-141">Selecione um índice, como **título** ou **corpo** na [Figura 6](#figure-6), para classificar o repositório de objetos de acordo com os valores desse índice.</span><span class="sxs-lookup"><span data-stu-id="5b253-141">Select an index, such as **title** or **body** in [Figure 6](#figure-6), to sort the object store according to the values of that index.</span></span>  
   
    > ##### <span data-ttu-id="5b253-142">Figura 6</span><span class="sxs-lookup"><span data-stu-id="5b253-142">Figure 6</span></span>  
    > <span data-ttu-id="5b253-143">Um repositório de objetos que é classificado em ordem alfabética de acordo com a chave de **título**</span><span class="sxs-lookup"><span data-stu-id="5b253-143">An object store that is sorted alphabetically according to the **title** key</span></span>  
    > ![Classificando um repositório de objetos por um índice][ImageIndexedDBIndex]  

## <span data-ttu-id="5b253-145">Atualizar dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-145">Refresh IndexedDB data</span></span>   

<span data-ttu-id="5b253-146">Os valores de IndexedDB no painel do **aplicativo** não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="5b253-146">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="5b253-147">Selecione **Atualizar** ![ atualização ][ImageReloadIcon] ao exibir um repositório de objetos para atualizar os dados ou exibir um banco de dados e clique em **Atualizar banco** de dados para atualizar todos os dados.</span><span class="sxs-lookup"><span data-stu-id="5b253-147">Select **Refresh** ![Refresh][ImageReloadIcon] when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

> ##### <span data-ttu-id="5b253-148">Figura 7</span><span class="sxs-lookup"><span data-stu-id="5b253-148">Figure 7</span></span>  
> <span data-ttu-id="5b253-149">Exibir um banco de dados</span><span class="sxs-lookup"><span data-stu-id="5b253-149">Viewing a database</span></span>  
> ![Exibir um banco de dados][ImageIndexedDBDatabase2]  

## <span data-ttu-id="5b253-151">Editar dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-151">Edit IndexedDB data</span></span>   

<span data-ttu-id="5b253-152">As chaves e os valores do IndexedDB não podem ser editados no painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="5b253-152">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="5b253-153">No entanto, como o DevTools tem acesso ao contexto da página, você pode executar o código JavaScript dentro do DevTools para editar os dados do IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="5b253-153">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="5b253-154">Editar dados do IndexedDB com snippets</span><span class="sxs-lookup"><span data-stu-id="5b253-154">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="5b253-155">Os [trechos][DevtoolsJavascriptSnippets] de código são uma maneira de armazenar e executar blocos de código JavaScript dentro do devtools.</span><span class="sxs-lookup"><span data-stu-id="5b253-155">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="5b253-156">Quando você executa um snippet, o resultado é registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="5b253-156">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="5b253-157">Você pode usar um snippet para executar o código JavaScript para editar um banco de dados do IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="5b253-157">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

> ##### <span data-ttu-id="5b253-158">Figura 8</span><span class="sxs-lookup"><span data-stu-id="5b253-158">Figure 8</span></span>  
> <span data-ttu-id="5b253-159">Usando um trecho para interagir com IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-159">Using a Snippet to interact with IndexedDB</span></span>  
> ![Usando um trecho para interagir com IndexedDB][ImageIndexedDBSnippet]  

## <span data-ttu-id="5b253-161">Excluir dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-161">Delete IndexedDB data</span></span>   

### <span data-ttu-id="5b253-162">Excluir um par de valor-chave IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-162">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="5b253-163">[Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="5b253-163">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="5b253-164">Selecione o par chave-valor que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="5b253-164">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="5b253-165">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="5b253-165">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="5b253-166">Figura 9</span><span class="sxs-lookup"><span data-stu-id="5b253-166">Figure 9</span></span>  
    > <span data-ttu-id="5b253-167">Selecionando um par de valores chave para excluí-lo</span><span class="sxs-lookup"><span data-stu-id="5b253-167">Selecting a key-value pair in order to delete it</span></span>  
    > ![Selecionando um par de valores chave para excluí-lo][ImageIndexedDBKeyValuePair]  

1.  <span data-ttu-id="5b253-169">Pressione a `Delete` tecla ou clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b253-169">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  
    
    > ##### <span data-ttu-id="5b253-170">Figura 10</span><span class="sxs-lookup"><span data-stu-id="5b253-170">Figure 10</span></span>  
    > <span data-ttu-id="5b253-171">Como a loja de objetos se parece após o par de valor chave ter sido excluído</span><span class="sxs-lookup"><span data-stu-id="5b253-171">How the object store looks after the key-value pair has been deleted</span></span>  
    > ![Como a loja de objetos se parece após o par de valor chave ter sido excluído][ImageIndexedDBKeyValuePairDeleted]  

### <span data-ttu-id="5b253-173">Excluir todos os pares de valores chave em um repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="5b253-173">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="5b253-174">[Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="5b253-174">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="5b253-175">Figura 11</span><span class="sxs-lookup"><span data-stu-id="5b253-175">Figure 11</span></span>  
    > <span data-ttu-id="5b253-176">Exibir um repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="5b253-176">Viewing an object store</span></span>  
    > ![Exibir um repositório de objetos][ImageIndexedDBObjectStore]  

1.  <span data-ttu-id="5b253-178">Selecione **limpar repositório de objetos** ![ limpar repositório de objetos ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b253-178">Select **Clear object store** ![Clear object store][ImageClearIcon].</span></span>  

### <span data-ttu-id="5b253-179">Excluir um banco de dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-179">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="5b253-180">[Exiba o banco de dados do IndexedDB](#view-indexeddb-data) que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="5b253-180">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="5b253-181">Selecione **excluir banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="5b253-181">Select **Delete database**.</span></span>  
    
    > ##### <span data-ttu-id="5b253-182">Figura 12</span><span class="sxs-lookup"><span data-stu-id="5b253-182">Figure 12</span></span>  
    > <span data-ttu-id="5b253-183">O botão **excluir banco de dados**</span><span class="sxs-lookup"><span data-stu-id="5b253-183">The **Delete database** button</span></span>  
    > ![O botão excluir banco de dados][ImageIndexedDBDatabase]  

### <span data-ttu-id="5b253-185">Excluir todo o armazenamento do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5b253-185">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="5b253-186">Abrir o painel **limpar armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="5b253-186">Open the **Clear storage** pane.</span></span>  

1.  <span data-ttu-id="5b253-187">Verifique se a caixa de seleção **IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="5b253-187">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  

1.  <span data-ttu-id="5b253-188">Selecione **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="5b253-188">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="5b253-189">Figura 13</span><span class="sxs-lookup"><span data-stu-id="5b253-189">Figure 13</span></span>  
    > <span data-ttu-id="5b253-190">O painel **limpar armazenamento** ![ o painel limpar armazenamento][ImageIndexedDBClearStorage]</span><span class="sxs-lookup"><span data-stu-id="5b253-190">The **Clear storage** pane ![The Clear storage pane][ImageIndexedDBClearStorage]</span></span>  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Figura 1: o painel manifestar"  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Figura 2: o menu IndexedDB"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Figura 3: o banco de dados do notes_db"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Figura 4: o repositório de objetos notes_os"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Figura 5: exibindo um valor de IndexedDB"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Figura 6: classificando um repositório de objetos por um índice"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Figura 7: exibindo um banco de dados"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Figura 8: usando um snippet para interagir com IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Figura 9: selecionando um par de valor chave para excluí-lo"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Figura 10: qual a aparência do repositório de objetos após o par de valor chave ter sido excluído"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Figura 11: exibindo um repositório de objetos"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Figura 12: botão excluir banco de dados"  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Figura 13: o painel limpar armazenamento"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: show iframe IndexedDB bancos de dados-Chromium-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de chave-conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando o IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice-usando IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="5b253-211">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="5b253-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5b253-212">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5b253-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5b253-214">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b253-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
