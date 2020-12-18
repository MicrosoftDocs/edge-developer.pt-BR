---
description: Como exibir e alterar dados do IndexedDB com o painel do aplicativo e Snippets.
title: Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231199"
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

# <span data-ttu-id="d75d0-104">Exibir e alterar dados do IndexedDB com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d75d0-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="d75d0-105">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir e alterar dados do [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="d75d0-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="d75d0-106">Ele pressupõe que você esteja familiarizado com o DevTools.</span><span class="sxs-lookup"><span data-stu-id="d75d0-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="d75d0-107">Ele também pressupõe que você esteja familiarizado com o IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="d75d0-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="d75d0-108">Caso contrário, navegue até [usando o IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="d75d0-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="d75d0-109">Exibir dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="d75d0-110">Escolha a guia **aplicativo** para abrir a ferramenta **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="d75d0-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="d75d0-111">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="d75d0-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="d75d0-113">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="d75d0-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d75d0-114">Expanda o menu **IndexedDB** para verificar quais bancos de dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d75d0-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="O menu IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="d75d0-116">O menu **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="d75d0-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="d75d0-117">\ ( ![ Ícone de banco de dados ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` representa um banco de dados, onde `notes` é o nome do banco de dados e `https://mdn.github.io` é a origem que acessa o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d75d0-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="d75d0-118">\ ( ![ Ícone de repositório de objetos ][ImageObjectStoreIcon] \) `notes` é um repositório de objetos.</span><span class="sxs-lookup"><span data-stu-id="d75d0-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="d75d0-119">**título** e **corpo** são [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="d75d0-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d75d0-120">**Limitação conhecida**  Os bancos de dados de terceiros não estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="d75d0-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="d75d0-121">Por exemplo, se você usar um `<iframe>` para inserir um anúncio em sua página, e sua rede de AD usar o IndexedDB, os dados do IndexedDB para a sua rede de anúncios não serão visíveis.</span><span class="sxs-lookup"><span data-stu-id="d75d0-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="d75d0-122">Navegue até o [problema #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="d75d0-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="d75d0-123">Escolha um banco de dados para revisar a origem e o número da versão.</span><span class="sxs-lookup"><span data-stu-id="d75d0-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="O banco de dados anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="d75d0-125">O banco de dados **anotações**</span><span class="sxs-lookup"><span data-stu-id="d75d0-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d75d0-126">Escolha um repositório de objetos para examinar os pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="d75d0-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d75d0-127">Os dados do IndexedDB não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="d75d0-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="d75d0-128">Navegue para [atualizar os dados do IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="d75d0-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="O repositório de objetos anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="d75d0-130">O repositório de objetos **anotações**</span><span class="sxs-lookup"><span data-stu-id="d75d0-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="d75d0-131">**Total de entradas** é o número total de pares de valores chave no repositório de objetos.</span><span class="sxs-lookup"><span data-stu-id="d75d0-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="d75d0-132">O **valor do gerador de chave** é a próxima chave disponível.</span><span class="sxs-lookup"><span data-stu-id="d75d0-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="d75d0-133">O campo só é mostrado ao usar os [geradores de chave][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="d75d0-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="d75d0-134">Escolha uma célula na coluna **valor** para expandir o valor.</span><span class="sxs-lookup"><span data-stu-id="d75d0-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Exibir um valor de IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="d75d0-136">Exibir um valor de **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="d75d0-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d75d0-137">Escolha um índice, como **título** ou **corpo** na figura a seguir, para classificar o repositório de objetos de acordo com os valores desse índice.</span><span class="sxs-lookup"><span data-stu-id="d75d0-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Classificar um repositório de objetos por um índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="d75d0-139">Classificar um repositório de objetos por um índice</span><span class="sxs-lookup"><span data-stu-id="d75d0-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d75d0-140">Atualizar dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="d75d0-141">Os valores de IndexedDB na ferramenta do **aplicativo** não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="d75d0-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="d75d0-142">Escolha **Atualizar** \ ( ![ Atualizar ][ImageReloadIcon] \) ao exibir um repositório de objetos para atualizar os dados ou exibir um banco de dados e escolha **Atualizar banco** de dados para atualizar todos os dados.</span><span class="sxs-lookup"><span data-stu-id="d75d0-142">Choose **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Exibir um banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="d75d0-144">Exibir um banco de dados</span><span class="sxs-lookup"><span data-stu-id="d75d0-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="d75d0-145">Editar dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="d75d0-146">As chaves e os valores de IndexedDB não são editáveis na ferramenta do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="d75d0-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="d75d0-147">No entanto, como o DevTools tem acesso ao contexto da página, você pode executar o código JavaScript dentro do DevTools para editar os dados do IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="d75d0-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="d75d0-148">Editar dados do IndexedDB com snippets</span><span class="sxs-lookup"><span data-stu-id="d75d0-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="d75d0-149">Os [trechos][DevtoolsJavascriptSnippets] de código são uma maneira de armazenar e executar blocos de código JavaScript dentro do devtools.</span><span class="sxs-lookup"><span data-stu-id="d75d0-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="d75d0-150">Quando você executa um snippet, o resultado é registrado no **console**.</span><span class="sxs-lookup"><span data-stu-id="d75d0-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="d75d0-151">Você pode usar um snippet para executar o código JavaScript para editar um banco de dados do IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="d75d0-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar um trecho para interagir com IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="d75d0-153">Usar um trecho para interagir com IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="d75d0-154">Excluir dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-154">Delete IndexedDB data</span></span>  

### <span data-ttu-id="d75d0-155">Excluir um par de valor-chave IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="d75d0-156">[Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="d75d0-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="d75d0-157">Selecione o par chave-valor que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="d75d0-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="d75d0-158">O DevTools a destaca para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="d75d0-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Selecionar um par de valor chave para excluí-lo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="d75d0-160">Selecionar um par de valor chave para excluí-lo</span><span class="sxs-lookup"><span data-stu-id="d75d0-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d75d0-161">Pressione a `Delete` tecla ou escolha **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d75d0-161">Press the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Como a loja de objetos se parece após o par de valor chave ter sido excluído" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="d75d0-163">Como a loja de objetos se parece após o par de valor chave ter sido excluído</span><span class="sxs-lookup"><span data-stu-id="d75d0-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="d75d0-164">Excluir todos os pares de valores chave em um repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="d75d0-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="d75d0-165">[Exibir um repositório de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="d75d0-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Exibir um repositório de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="d75d0-167">Exibir um repositório de objetos</span><span class="sxs-lookup"><span data-stu-id="d75d0-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d75d0-168">Escolha **limpar repositório de objetos** \ ( ![ limpar repositório de objetos ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d75d0-168">Choose **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="d75d0-169">Excluir um banco de dados do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="d75d0-170">[Exiba o banco de dados do IndexedDB](#view-indexeddb-data) que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="d75d0-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="d75d0-171">Escolha **excluir banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="d75d0-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="O botão excluir banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="d75d0-173">O botão **excluir banco de dados**</span><span class="sxs-lookup"><span data-stu-id="d75d0-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="d75d0-174">Excluir todo o armazenamento do IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d75d0-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="d75d0-175">Abrir o painel **limpar armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="d75d0-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="d75d0-176">Verifique se a caixa de seleção **IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d75d0-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="d75d0-177">Escolha **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="d75d0-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="O painel limpar armazenamento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="d75d0-179">O painel **limpar armazenamento**</span><span class="sxs-lookup"><span data-stu-id="d75d0-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d75d0-180">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d75d0-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Executar trechos de JavaScript em qualquer página com o Microsoft Edge DevTools | Documentos da Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: show iframe IndexedDB bancos de dados-Chromium-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de chave-conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando o IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice-usando IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="d75d0-188">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d75d0-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d75d0-189">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d75d0-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d75d0-191">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d75d0-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
