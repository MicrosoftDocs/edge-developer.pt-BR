---
title: Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 890e20f65c3b70193a38783f3c9ca5d879d5ac48
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983713"
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





# <span data-ttu-id="35628-103">Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="35628-103">View and change IndexedDB data with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="35628-104">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir e alterar dados do [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="35628-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="35628-105">Ele pressupõe que você esteja familiarizado com o DevTools.</span><span class="sxs-lookup"><span data-stu-id="35628-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="35628-106">Ele também pressupõe que você esteja familiarizado com o IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="35628-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="35628-107">Caso contrário, consulte [usando o IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="35628-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="35628-108">Exibir dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="35628-109">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="35628-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="35628-110">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="35628-110">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="35628-112">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="35628-112">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35628-113">Expanda o menu **IndexedDB** para ver quais bancos de dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35628-113">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="O menu IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="35628-115">O menu **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="35628-115">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="35628-116">\ ( ![ Ícone de banco de dados ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` representa um banco de dados, onde `notes` é o nome do banco de dados e `https://mdn.github.io` é a origem que acessa o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="35628-116">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="35628-117">\ ( ![ Ícone de repositório de objetos ][ImageObjectStoreIcon] \) `notes` é um repositório de objetos.</span><span class="sxs-lookup"><span data-stu-id="35628-117">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="35628-118">**título** e **corpo** são [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="35628-118">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="35628-119">**Limitação conhecida**  Os bancos de dados de terceiros não estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="35628-119">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="35628-120">Por exemplo, se você usar um `<iframe>` para inserir um anúncio em sua página, e sua rede de AD usar o IndexedDB, os dados do IndexedDB para a sua rede de anúncios não serão visíveis.</span><span class="sxs-lookup"><span data-stu-id="35628-120">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="35628-121">Veja o [problema #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="35628-121">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="35628-122">Selecione um banco de dados para ver a origem e o número da versão.</span><span class="sxs-lookup"><span data-stu-id="35628-122">Select a database to see the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="O banco de dados anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="35628-124">O banco de dados **anotações**</span><span class="sxs-lookup"><span data-stu-id="35628-124">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35628-125">Selecione um repositório de objetos para ver os pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="35628-125">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="35628-126">Os dados do IndexedDB não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="35628-126">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="35628-127">Consulte [atualizar dados do IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="35628-127">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="O repositório de objetos anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="35628-129">O repositório de objetos **anotações**</span><span class="sxs-lookup"><span data-stu-id="35628-129">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="35628-130">**Total de entradas** é o número total de pares de valores chave no repositório de objetos.</span><span class="sxs-lookup"><span data-stu-id="35628-130">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="35628-131">O **valor do gerador de chave** é a próxima chave disponível.</span><span class="sxs-lookup"><span data-stu-id="35628-131">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="35628-132">Este campo é mostrado apenas ao usar [geradores de chaves][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="35628-132">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="35628-133">Selecione uma célula na coluna **valor** para expandir esse valor.</span><span class="sxs-lookup"><span data-stu-id="35628-133">Select a cell in the **Value** column to expand that value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Exibir um valor de IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="35628-135">Exibir um valor de **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="35628-135">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35628-136">Selecione um índice, como **título** ou **corpo** na figura a seguir, para classificar o repositório de objetos de acordo com os valores desse índice.</span><span class="sxs-lookup"><span data-stu-id="35628-136">Select an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Classificar um repositório de objetos por um índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="35628-138">Classificar um repositório de objetos por um índice</span><span class="sxs-lookup"><span data-stu-id="35628-138">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="35628-139">Atualizar dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-139">Refresh IndexedDB data</span></span>   

<span data-ttu-id="35628-140">Os valores de IndexedDB no painel do **aplicativo** não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="35628-140">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="35628-141">Selecione **Atualizar** \ ( ![ Atualizar ][ImageReloadIcon] \) ao exibir um repositório de objetos para atualizar os dados ou exibir um banco de dados e clique em **Atualizar banco** de dados para atualizar todos os dados.</span><span class="sxs-lookup"><span data-stu-id="35628-141">Select **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Exibir um banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="35628-143">Exibir um banco de dados</span><span class="sxs-lookup"><span data-stu-id="35628-143">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="35628-144">Editar dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-144">Edit IndexedDB data</span></span>   

<span data-ttu-id="35628-145">As chaves e os valores do IndexedDB não podem ser editados no painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="35628-145">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="35628-146">No entanto, como o DevTools tem acesso ao contexto da página, você pode executar o código JavaScript dentro do DevTools para editar os dados do IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="35628-146">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="35628-147">Editar dados do IndexedDB com snippets</span><span class="sxs-lookup"><span data-stu-id="35628-147">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="35628-148">Os [trechos][DevtoolsJavascriptSnippets] de código são uma maneira de armazenar e executar blocos de código JavaScript dentro do devtools.</span><span class="sxs-lookup"><span data-stu-id="35628-148">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="35628-149">Quando você executa um snippet, o resultado é registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="35628-149">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="35628-150">Você pode usar um snippet para executar o código JavaScript para editar um banco de dados do IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="35628-150">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar um trecho para interagir com IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="35628-152">Usar um trecho para interagir com IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-152">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="35628-153">Excluir dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-153">Delete IndexedDB data</span></span>   

### <span data-ttu-id="35628-154">Excluir um par de valor-chave IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-154">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="35628-155">[Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="35628-155">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="35628-156">Selecione o par chave-valor que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="35628-156">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="35628-157">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="35628-157">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Selecionar um par de valor chave para excluí-lo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="35628-159">Selecionar um par de valor chave para excluí-lo</span><span class="sxs-lookup"><span data-stu-id="35628-159">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35628-160">Pressione a `Delete` tecla ou clique em **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="35628-160">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Como a loja de objetos se parece após o par de valor chave ter sido excluído" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="35628-162">Como a loja de objetos se parece após o par de valor chave ter sido excluído</span><span class="sxs-lookup"><span data-stu-id="35628-162">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="35628-163">Excluir todos os pares de valores chave em um repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="35628-163">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="35628-164">[Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="35628-164">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Exibir um repositório de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="35628-166">Exibir um repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="35628-166">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="35628-167">Selecione **limpar repositório de objetos** \ ( ![ limpar repositório de objetos ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="35628-167">Select **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="35628-168">Excluir um banco de dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-168">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="35628-169">[Exiba o banco de dados do IndexedDB](#view-indexeddb-data) que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="35628-169">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="35628-170">Selecione **excluir banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="35628-170">Select **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="O botão excluir banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="35628-172">O botão **excluir banco de dados**</span><span class="sxs-lookup"><span data-stu-id="35628-172">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="35628-173">Excluir todo o armazenamento do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="35628-173">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="35628-174">Abrir o painel **limpar armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="35628-174">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="35628-175">Verifique se a caixa de seleção **IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="35628-175">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="35628-176">Selecione **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="35628-176">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="O painel limpar armazenamento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="35628-178">O painel **limpar armazenamento**</span><span class="sxs-lookup"><span data-stu-id="35628-178">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools | Documentos da Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: show iframe IndexedDB bancos de dados-Chromium-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de chave-conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando o IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice-usando IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="35628-186">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="35628-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="35628-187">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="35628-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="35628-189">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="35628-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
