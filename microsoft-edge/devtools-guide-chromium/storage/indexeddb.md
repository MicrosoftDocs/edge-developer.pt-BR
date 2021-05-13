---
description: Como exibir e alterar dados IndexedDB com o painel de aplicativos e trechos.
title: Exibir e alterar dados IndexedDB com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b0927ab436d1278f50b0dee099ba3526e5506762
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564802"
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
# <a name="view-and-change-indexeddb-data-with-microsoft-edge-devtools"></a><span data-ttu-id="8f828-104">Exibir e alterar dados IndexedDB com Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f828-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="8f828-105">Este guia mostra como usar Microsoft Edge [DevTools][MicrosoftEdgeDevTools] para exibir e alterar [dados IndexedDB.][MDNIndexedDBAPI]</span><span class="sxs-lookup"><span data-stu-id="8f828-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="8f828-106">Ele supõe que você está familiarizado com o DevTools.</span><span class="sxs-lookup"><span data-stu-id="8f828-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="8f828-107">Ele também supõe que você está familiarizado com IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="8f828-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="8f828-108">Caso não, navegue até [Using IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="8f828-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <a name="view-indexeddb-data"></a><span data-ttu-id="8f828-109">Exibir dados IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="8f828-110">Escolha a **guia Aplicativo** para abrir a **ferramenta Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="8f828-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="8f828-111">O **painel** Manifesto geralmente é aberto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8f828-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="8f828-113">O **painel** Manifesto</span><span class="sxs-lookup"><span data-stu-id="8f828-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8f828-114">Expanda o menu **IndexedDB** para revisar quais bancos de dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8f828-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="O menu IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="8f828-116">O **menu IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="8f828-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="8f828-117">\( Ícone de banco de dados \) representa um banco de dados, onde é o nome do banco de dados e é a origem que ![ acessa o banco de ](../media/database-icon.msft.png) `notes - https://mdn.github.io` `notes` `https://mdn.github.io` dados.</span><span class="sxs-lookup"><span data-stu-id="8f828-117">\(![Database icon](../media/database-icon.msft.png)\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="8f828-118">\( ![ Ícone do Armazenamento de Objetos ](../media/object-store-icon.msft.png) \) é um armazenamento de `notes` objetos.</span><span class="sxs-lookup"><span data-stu-id="8f828-118">\(![Object Store icon](../media/object-store-icon.msft.png)\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="8f828-119">**title** e **body** são [índices][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="8f828-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8f828-120">**Limitação Conhecida**  Bancos de dados de terceiros não estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="8f828-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="8f828-121">Por exemplo, se você usar um para inserir um comercial em sua página e sua rede de comentários usar IndexedDB, os dados IndexedDB para sua rede de ad não estarão `<iframe>` visíveis.</span><span class="sxs-lookup"><span data-stu-id="8f828-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="8f828-122">Navegue [até emitir #943770][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="8f828-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="8f828-123">Escolha um banco de dados para analisar a origem e o número da versão.</span><span class="sxs-lookup"><span data-stu-id="8f828-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="O banco de dados de anotações" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="8f828-125">O **banco de dados de anotações**</span><span class="sxs-lookup"><span data-stu-id="8f828-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8f828-126">Escolha um armazenamento de objetos para revisar os pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="8f828-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8f828-127">Os dados indexedDB não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="8f828-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="8f828-128">Navegue [até Atualizar dados indexadosDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="8f828-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="O armazenamento de objetos notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="8f828-130">O **armazenamento de objetos** notes</span><span class="sxs-lookup"><span data-stu-id="8f828-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="8f828-131">**Entradas totais** é o número total de pares de valores-chave no armazenamento de objetos.</span><span class="sxs-lookup"><span data-stu-id="8f828-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="8f828-132">**O valor do gerador de** chaves é a próxima chave disponível.</span><span class="sxs-lookup"><span data-stu-id="8f828-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="8f828-133">O campo só é mostrado ao usar [geradores de chaves][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="8f828-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="8f828-134">Escolha uma célula na coluna **Valor** para expandir o valor.</span><span class="sxs-lookup"><span data-stu-id="8f828-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Exibir um valor IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="8f828-136">Exibir um **valor IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="8f828-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8f828-137">Escolha um índice, como **título** ou **corpo** na figura a seguir, para classificar o armazenamento de objetos de acordo com os valores desse índice.</span><span class="sxs-lookup"><span data-stu-id="8f828-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Classificar um armazenamento de objetos por um índice" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="8f828-139">Classificar um armazenamento de objetos por um índice</span><span class="sxs-lookup"><span data-stu-id="8f828-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <a name="refresh-indexeddb-data"></a><span data-ttu-id="8f828-140">Atualizar dados IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="8f828-141">Os valores indexadosDB na **ferramenta Application** não são atualizados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="8f828-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="8f828-142">Escolha **Atualizar** \( Atualizar \) ao exibir um armazenamento de objetos para atualizar os dados ou exibir um banco de dados e escolher Atualizar banco de dados para ![ atualizar todos os ](../media/reload-icon.msft.png) dados. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8f828-142">Choose **Refresh** \(![Refresh](../media/reload-icon.msft.png)\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Exibir um banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="8f828-144">Exibir um banco de dados</span><span class="sxs-lookup"><span data-stu-id="8f828-144">View a database</span></span>  
:::image-end:::  

## <a name="edit-indexeddb-data"></a><span data-ttu-id="8f828-145">Editar dados IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="8f828-146">As teclas indexadasDB e os valores não podem ser editáveis na **ferramenta Application.**</span><span class="sxs-lookup"><span data-stu-id="8f828-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="8f828-147">Como o DevTools tem acesso ao contexto da página, no entanto, você pode executar código JavaScript no DevTools para editar dados indexadosDB.</span><span class="sxs-lookup"><span data-stu-id="8f828-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <a name="edit-indexeddb-data-with-snippets"></a><span data-ttu-id="8f828-148">Editar dados indexadosdb com trechos</span><span class="sxs-lookup"><span data-stu-id="8f828-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="8f828-149">[Trechos de código][DevtoolsJavascriptSnippets] são uma maneira de armazenar e executar blocos de código JavaScript no DevTools.</span><span class="sxs-lookup"><span data-stu-id="8f828-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="8f828-150">Quando você executar um trecho de código, o resultado será registrado no **Console**.</span><span class="sxs-lookup"><span data-stu-id="8f828-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="8f828-151">Você pode usar um trecho para executar código JavaScript para editar um banco de dados IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="8f828-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Usar um trecho de código para interagir com IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="8f828-153">Usar um trecho de código para interagir com IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <a name="delete-indexeddb-data"></a><span data-ttu-id="8f828-154">Excluir dados IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-154">Delete IndexedDB data</span></span>  

### <a name="delete-an-indexeddb-key-value-pair"></a><span data-ttu-id="8f828-155">Excluir um par de valores de chave IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="8f828-156">[Exibir um armazenamento de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="8f828-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="8f828-157">Escolha o par de valores-chave que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="8f828-157">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="8f828-158">O DevTools realça-o para indicar que ele está selecionado.</span><span class="sxs-lookup"><span data-stu-id="8f828-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Escolha um par de valores-chave para excluí-lo" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="8f828-160">Escolha um par de valores-chave para excluí-lo</span><span class="sxs-lookup"><span data-stu-id="8f828-160">Choose a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8f828-161">Selecione a `Delete` chave ou escolha Excluir **Selecionado** \( Excluir ![ Selecionado ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="8f828-161">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Como o armazenamento de objetos se parece após a exclusão do par de valores-chave" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="8f828-163">Como o armazenamento de objetos se parece após a exclusão do par de valores-chave</span><span class="sxs-lookup"><span data-stu-id="8f828-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <a name="delete-all-key-value-pairs-in-an-object-store"></a><span data-ttu-id="8f828-164">Excluir todos os pares de valores-chave em um armazenamento de objetos</span><span class="sxs-lookup"><span data-stu-id="8f828-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="8f828-165">[Exibir um armazenamento de objetos IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="8f828-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Exibir um armazenamento de objetos" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="8f828-167">Exibir um armazenamento de objetos</span><span class="sxs-lookup"><span data-stu-id="8f828-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8f828-168">Escolha **Limpar o armazenamento de objetos** \( Limpar o armazenamento de objetos ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="8f828-168">Choose **Clear object store** \(![Clear object store](../media/clear-icon.msft.png)\).</span></span>  
    
### <a name="delete-an-indexeddb-database"></a><span data-ttu-id="8f828-169">Excluir um banco de dados IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="8f828-170">[Exibir o banco de dados IndexedDB](#view-indexeddb-data) que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="8f828-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="8f828-171">Escolha **Excluir banco de dados**.</span><span class="sxs-lookup"><span data-stu-id="8f828-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="O botão Excluir banco de dados" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="8f828-173">O **botão Excluir banco de dados**</span><span class="sxs-lookup"><span data-stu-id="8f828-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <a name="delete-all-indexeddb-storage"></a><span data-ttu-id="8f828-174">Excluir todo o armazenamento IndexedDB</span><span class="sxs-lookup"><span data-stu-id="8f828-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="8f828-175">Abra o **painel Limpar armazenamento.**</span><span class="sxs-lookup"><span data-stu-id="8f828-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="8f828-176">Verifique se a **caixa de seleção IndexedDB** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="8f828-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="8f828-177">Escolha **Limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="8f828-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="O painel Limpar armazenamento" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="8f828-179">O **painel Limpar armazenamento**</span><span class="sxs-lookup"><span data-stu-id="8f828-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8f828-180">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8f828-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página com Microsoft Edge DevTools | Microsoft Docs"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770 - DevTools: Mostrar bancos de dados indexadosdb iframe - chromium - Monotrilho"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Gerador de Chaves - Conceitos básicos | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Api IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Usando IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Usando um índice - Usando indexadoDB | MDN"  

> [!NOTE]
> <span data-ttu-id="8f828-188">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f828-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8f828-189">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8f828-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8f828-191">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8f828-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
