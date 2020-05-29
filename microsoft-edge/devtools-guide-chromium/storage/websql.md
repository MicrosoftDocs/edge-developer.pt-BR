---
title: Exibir dados do SQL da Web com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7a1e3e47f6761cfdb23488683107ed0df6a8f4e2
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612057"
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





# <span data-ttu-id="46c9c-103">Exibir dados do SQL da Web com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="46c9c-103">View Web SQL Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="46c9c-104">A especificação SQL da Web [não está sendo mantida][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="46c9c-104">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="46c9c-105">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar dados SQL da Web.</span><span class="sxs-lookup"><span data-stu-id="46c9c-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="46c9c-106">Exibir dados do SQL Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-106">View Web SQL Data</span></span>   

1.  <span data-ttu-id="46c9c-107">Selecione a guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="46c9c-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="46c9c-108">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="46c9c-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-109">Figura 1</span><span class="sxs-lookup"><span data-stu-id="46c9c-109">Figure 1</span></span>  
    > <span data-ttu-id="46c9c-110">Painel de manifesto</span><span class="sxs-lookup"><span data-stu-id="46c9c-110">The Manifest pane</span></span>  
    > ![Painel de manifesto][ImageManifestPane]  
    
1.  <span data-ttu-id="46c9c-112">Expanda a seção **SQL Web** para exibir bancos de dados e tabelas.</span><span class="sxs-lookup"><span data-stu-id="46c9c-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="46c9c-113">Na [Figura 2](#figure-2) abaixo de **html5meetup** , um banco de dados e **salas** é uma tabela.</span><span class="sxs-lookup"><span data-stu-id="46c9c-113">In [Figure 2](#figure-2) below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-114">Figura 2</span><span class="sxs-lookup"><span data-stu-id="46c9c-114">Figure 2</span></span>  
    > <span data-ttu-id="46c9c-115">O painel SQL Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-115">The Web SQL pane</span></span>  
    > ![O painel SQL Web][ImageWebSQLPane]  

1.  <span data-ttu-id="46c9c-117">Selecione uma tabela para exibir os dados dessa tabela.</span><span class="sxs-lookup"><span data-stu-id="46c9c-117">Select a table to view the data for that table.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-118">Figura 3</span><span class="sxs-lookup"><span data-stu-id="46c9c-118">Figure 3</span></span>  
    > <span data-ttu-id="46c9c-119">Exibindo os dados da tabela SQL da Web **Rooms**</span><span class="sxs-lookup"><span data-stu-id="46c9c-119">Viewing the data of the **rooms** Web SQL table</span></span>  
    > ![Exibindo os dados de uma tabela SQL da Web][ImageWebSQLTable]  

## <span data-ttu-id="46c9c-121">Editar dados do SQL da Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-121">Edit Web SQL data</span></span>   

<span data-ttu-id="46c9c-122">Você não pode editar dados SQL da Web ao exibir uma tabela SQL da Web, como na **Figura 3** acima.</span><span class="sxs-lookup"><span data-stu-id="46c9c-122">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="46c9c-123">Mas você pode executar instruções a partir do console SQL Web que edita ou exclui tabelas.</span><span class="sxs-lookup"><span data-stu-id="46c9c-123">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="46c9c-124">Consulte [executar consultas do SQL Web](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="46c9c-124">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="46c9c-125">Executar consultas do SQL da Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-125">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="46c9c-126">Selecione um banco de dados para abrir um console para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="46c9c-126">Select a database to open a console for that database.</span></span>  

1.  <span data-ttu-id="46c9c-127">Digite uma instrução SQL da Web e pressione `Enter` para executá-la.</span><span class="sxs-lookup"><span data-stu-id="46c9c-127">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-128">Figura 4</span><span class="sxs-lookup"><span data-stu-id="46c9c-128">Figure 4</span></span>  
    > <span data-ttu-id="46c9c-129">Usar o console do SQL Web para excluir uma linha da tabela **salas**</span><span class="sxs-lookup"><span data-stu-id="46c9c-129">Using the Web SQL Console to delete a row from the **rooms** table</span></span>  
    > ![Usar o console do SQL Web para excluir uma linha de uma tabela][ImageWebSQLEdit]  

## <span data-ttu-id="46c9c-131">Atualizar uma tabela SQL da Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-131">Refresh a Web SQL table</span></span>   

<span data-ttu-id="46c9c-132">O DevTools não atualiza tabelas em tempo real.</span><span class="sxs-lookup"><span data-stu-id="46c9c-132">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="46c9c-133">Para atualizar os dados em uma tabela:</span><span class="sxs-lookup"><span data-stu-id="46c9c-133">To update the data in a table:</span></span>  

1.  <span data-ttu-id="46c9c-134">[Exiba os dados em uma tabela SQL da Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="46c9c-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="46c9c-135">Selecione **Atualizar** ![ atualização ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="46c9c-135">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="46c9c-136">Filtrar colunas em uma tabela SQL da Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-136">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="46c9c-137">[Exiba os dados em uma tabela SQL da Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="46c9c-137">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="46c9c-138">Use a caixa de texto **colunas visíveis** para especificar quais colunas você deseja mostrar.</span><span class="sxs-lookup"><span data-stu-id="46c9c-138">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="46c9c-139">Forneça os nomes de coluna como uma lista de CSV.</span><span class="sxs-lookup"><span data-stu-id="46c9c-139">Provide the column names as a CSV list.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-140">Figura 5</span><span class="sxs-lookup"><span data-stu-id="46c9c-140">Figure 5</span></span>  
    > <span data-ttu-id="46c9c-141">Usar a caixa de texto **colunas visíveis** para mostrar apenas `room_name` as `last_updated` colunas e</span><span class="sxs-lookup"><span data-stu-id="46c9c-141">Using the **Visible Columns** text box to only show the `room_name` and `last_updated` columns</span></span>  
    > ![Usar a caixa de texto colunas visíveis para reduzir o número de colunas exibidas][ImageWebSQLFilter]  

## <span data-ttu-id="46c9c-143">Excluir todos os dados SQL da Web</span><span class="sxs-lookup"><span data-stu-id="46c9c-143">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="46c9c-144">Abrir o painel **limpar armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="46c9c-144">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="46c9c-145">Verifique se a caixa de seleção **SQL da Web** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46c9c-145">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-146">Figura 6</span><span class="sxs-lookup"><span data-stu-id="46c9c-146">Figure 6</span></span>  
    > <span data-ttu-id="46c9c-147">A caixa de seleção **SQL da Web**</span><span class="sxs-lookup"><span data-stu-id="46c9c-147">The **Web SQL** checkbox</span></span>  
    > ![A caixa de seleção SQL da Web][ImageWebSQLCheckbox]  

1.  <span data-ttu-id="46c9c-149">Selecione **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="46c9c-149">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="46c9c-150">Figura 7</span><span class="sxs-lookup"><span data-stu-id="46c9c-150">Figure 7</span></span>  
    > <span data-ttu-id="46c9c-151">O botão **limpar dados do site**</span><span class="sxs-lookup"><span data-stu-id="46c9c-151">The **Clear Site Data** button</span></span>  
    > ![O botão limpar dados do site][ImageClearWebSQL]  

 



<!-- image links -->  

[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageWebSQLPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql.msft.png "Figura 2: painel SQL Web"  
[ImageWebSQLTable]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png "Figura 3: exibindo os dados de uma tabela SQL Web"  
[ImageWebSQLEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-commands.msft.png "Figura 4: usar o console do SQL Web para excluir uma linha de uma tabela"  
[ImageWebSQLFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png "Figura 5: usar a caixa de texto colunas visíveis para reduzir o número de colunas exibidas"  
[ImageWebSQLCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-web-sql.msft.png "Figura 6: caixa de seleção SQL da Web"  
[ImageClearWebSQL]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-clear-site-data-button.msft.png "Figura 7: botão limpar dados do site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Banco de dados SQL Web | W3C"  

> [!NOTE]
> <span data-ttu-id="46c9c-162">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="46c9c-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="46c9c-163">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/websql) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="46c9c-163">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="46c9c-165">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46c9c-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
