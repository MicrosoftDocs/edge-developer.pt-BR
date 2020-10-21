---
description: Como exibir dados do SQL da Web no painel de aplicativos do Microsoft Edge DevTools.
title: Exibir dados do SQL da Web com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0396a00ec354fdd707bc4d484242d4cf844db5f9
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125465"
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

# <span data-ttu-id="a64e8-104">Exibir dados do SQL da Web com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a64e8-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="a64e8-105">A especificação SQL da Web [não está sendo mantida][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="a64e8-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="a64e8-106">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar dados SQL da Web.</span><span class="sxs-lookup"><span data-stu-id="a64e8-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="a64e8-107">Exibir dados do SQL Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="a64e8-108">Selecione a guia **fontes** para abrir o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="a64e8-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="a64e8-109">O painel de **manifesto** geralmente abre por padrão.</span><span class="sxs-lookup"><span data-stu-id="a64e8-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="a64e8-111">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="a64e8-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a64e8-112">Expanda a seção **SQL Web** para exibir bancos de dados e tabelas.</span><span class="sxs-lookup"><span data-stu-id="a64e8-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="a64e8-113">Na figura a seguir, abaixo de **html5meetup** é um banco de dados e **salas** é uma tabela.</span><span class="sxs-lookup"><span data-stu-id="a64e8-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="a64e8-115">O painel **SQL Web**</span><span class="sxs-lookup"><span data-stu-id="a64e8-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a64e8-116">Selecione uma tabela para exibir os dados dessa tabela.</span><span class="sxs-lookup"><span data-stu-id="a64e8-116">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="a64e8-118">Exibir os dados de uma tabela SQL da Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a64e8-119">Editar dados do SQL da Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-119">Edit Web SQL data</span></span>  

<span data-ttu-id="a64e8-120">Você não pode editar dados SQL da Web ao exibir uma tabela SQL da Web, como na **Figura 3** acima.</span><span class="sxs-lookup"><span data-stu-id="a64e8-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="a64e8-121">Mas você pode executar instruções a partir do console SQL Web que edita ou exclui tabelas.</span><span class="sxs-lookup"><span data-stu-id="a64e8-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="a64e8-122">Consulte [executar consultas do SQL Web](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="a64e8-122">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="a64e8-123">Executar consultas do SQL da Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="a64e8-124">Selecione um banco de dados para abrir um console para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a64e8-124">Select a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="a64e8-125">Digite uma instrução SQL da Web e selecione `Enter` para executá-la.</span><span class="sxs-lookup"><span data-stu-id="a64e8-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="a64e8-127">Usar o console do SQL Web para excluir uma linha de uma tabela</span><span class="sxs-lookup"><span data-stu-id="a64e8-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a64e8-128">Atualizar uma tabela SQL da Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="a64e8-129">O DevTools não atualiza tabelas em tempo real.</span><span class="sxs-lookup"><span data-stu-id="a64e8-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="a64e8-130">Para atualizar os dados em uma tabela:</span><span class="sxs-lookup"><span data-stu-id="a64e8-130">To update the data in a table:</span></span>  

1.  <span data-ttu-id="a64e8-131">[Exiba os dados em uma tabela SQL da Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="a64e8-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="a64e8-132">Escolha **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="a64e8-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="a64e8-133">Filtrar colunas em uma tabela SQL da Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="a64e8-134">[Exiba os dados em uma tabela SQL da Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="a64e8-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="a64e8-135">Use a caixa de texto **colunas visíveis** para especificar quais colunas você deseja mostrar.</span><span class="sxs-lookup"><span data-stu-id="a64e8-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="a64e8-136">Forneça os nomes de coluna como uma lista de CSV.</span><span class="sxs-lookup"><span data-stu-id="a64e8-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="a64e8-138">Use a caixa de texto **colunas visíveis** para reduzir o número de colunas exibidas</span><span class="sxs-lookup"><span data-stu-id="a64e8-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a64e8-139">Excluir todos os dados SQL da Web</span><span class="sxs-lookup"><span data-stu-id="a64e8-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="a64e8-140">Abrir o painel **limpar armazenamento** .</span><span class="sxs-lookup"><span data-stu-id="a64e8-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="a64e8-141">Verifique se a caixa de seleção **SQL da Web** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a64e8-141">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="a64e8-143">A caixa de seleção **SQL da Web**</span><span class="sxs-lookup"><span data-stu-id="a64e8-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a64e8-144">Escolha **limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="a64e8-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="a64e8-146">O botão **limpar dados do site**</span><span class="sxs-lookup"><span data-stu-id="a64e8-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="a64e8-147">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a64e8-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Banco de dados SQL Web | W3C"  

> [!NOTE]
> <span data-ttu-id="a64e8-150">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="a64e8-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a64e8-151">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/websql) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a64e8-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a64e8-153">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a64e8-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
