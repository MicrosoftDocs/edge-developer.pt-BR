---
description: Como exibir dados SQL Web no painel Aplicativo do Microsoft Edge DevTools.
title: Exibir dados SQL Web com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 9f684aabf3592220079e6a8595d91cfea6785769
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439595"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a><span data-ttu-id="5a9ba-104">Exibir dados SQL Web com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5a9ba-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="5a9ba-105">A especificação SQL Web [não está sendo mantida.][W3CWebSQLStatus]</span><span class="sxs-lookup"><span data-stu-id="5a9ba-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="5a9ba-106">Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspecionar dados SQL Web.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <a name="view-web-sql-data"></a><span data-ttu-id="5a9ba-107">Exibir dados SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="5a9ba-108">Escolha a **ferramenta Fontes** para abrir a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="5a9ba-108">Choose the **Sources** tool to open the **Sources** tool.</span></span>  <span data-ttu-id="5a9ba-109">O **painel** Manifesto geralmente é aberto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="5a9ba-111">O **painel** Manifesto</span><span class="sxs-lookup"><span data-stu-id="5a9ba-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5a9ba-112">Expanda a **seção SQL** Web para exibir bancos de dados e tabelas.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="5a9ba-113">Na figura a seguir, abaixo **html5meetup** está um banco de dados e **salas** é uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="O painel SQL Web" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="5a9ba-115">O **painel SQL** Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5a9ba-116">Escolha uma tabela para exibir os dados dessa tabela.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-116">Choose a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Exibir os dados de uma tabela de SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="5a9ba-118">Exibir os dados de uma tabela de SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a><span data-ttu-id="5a9ba-119">Editar dados SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-119">Edit Web SQL data</span></span>  

<span data-ttu-id="5a9ba-120">Você não é capaz de editar dados SQL Web ao exibir uma tabela SQL Web, como na anterior acima.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="5a9ba-121">Mas você pode executar instruções do Console web SQL que editam ou excluem tabelas.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="5a9ba-122">Navegue [até Executar consultas SQL Web.](#run-web-sql-queries)</span><span class="sxs-lookup"><span data-stu-id="5a9ba-122">Navigate to [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <a name="run-web-sql-queries"></a><span data-ttu-id="5a9ba-123">Executar consultas SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="5a9ba-124">Escolha um banco de dados para abrir um console para esse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="5a9ba-125">Digite uma instrução SQL Web e selecione `Enter` para executar.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Usar o Console SQL Web para excluir uma linha de uma tabela" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="5a9ba-127">Usar o Console SQL Web para excluir uma linha de uma tabela</span><span class="sxs-lookup"><span data-stu-id="5a9ba-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a><span data-ttu-id="5a9ba-128">Atualizar uma tabela SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="5a9ba-129">O DevTools não atualiza tabelas em tempo real.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="5a9ba-130">Para atualizar os dados em uma tabela, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="5a9ba-131">[Exibir os dados em uma tabela SQL Web.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="5a9ba-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5a9ba-132">Escolha **Atualizar** \( ![ Atualizar ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5a9ba-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a><span data-ttu-id="5a9ba-133">Filtrar colunas em uma tabela SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="5a9ba-134">[Exibir os dados em uma tabela SQL Web.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="5a9ba-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5a9ba-135">Use a **caixa de texto Colunas** Visíveis para especificar quais colunas você deseja mostrar.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="5a9ba-136">Forneça os nomes das colunas como uma lista CSV.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Use a caixa de texto Colunas Visíveis para reduzir o número de colunas mostradas" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="5a9ba-138">Use a **caixa de texto Colunas** Visíveis para reduzir o número de colunas mostradas</span><span class="sxs-lookup"><span data-stu-id="5a9ba-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a><span data-ttu-id="5a9ba-139">Excluir todos os dados SQL Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="5a9ba-140">Abra o **painel Limpar Armazenamento.**</span><span class="sxs-lookup"><span data-stu-id="5a9ba-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="5a9ba-141">Verifique se a caixa de **SQL** Web está 100% 100% 2000.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Caixa de SQL Web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="5a9ba-143">Caixa **de SQL** Web</span><span class="sxs-lookup"><span data-stu-id="5a9ba-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5a9ba-144">Escolha **Limpar dados do site**.</span><span class="sxs-lookup"><span data-stu-id="5a9ba-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="O botão Limpar Dados do Site" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="5a9ba-146">O **botão Limpar Dados do Site**</span><span class="sxs-lookup"><span data-stu-id="5a9ba-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5a9ba-147">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5a9ba-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Web SQL banco de dados | W3C"  

> [!NOTE]
> <span data-ttu-id="5a9ba-150">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5a9ba-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5a9ba-151">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/websql) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5a9ba-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5a9ba-153">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5a9ba-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
