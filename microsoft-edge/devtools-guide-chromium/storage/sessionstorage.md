---
description: Como exibir e editar sessionStorage com o painel armazenamento da sessão e o console.
title: Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 24fca3fd3a068f3b2ffbe4ec1c23e6b80b968953
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993545"
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





# <span data-ttu-id="05d56-104">Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="05d56-104">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="05d56-105">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir, editar e excluir [`sessionStorage`][MDNSessionStorage] pares de valores de chave.</span><span class="sxs-lookup"><span data-stu-id="05d56-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="05d56-106">Exibir chaves e valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="05d56-106">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="05d56-107">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="05d56-107">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="05d56-108">O painel **manifestar** é mostrado por padrão.</span><span class="sxs-lookup"><span data-stu-id="05d56-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="05d56-110">Painel de **manifesto**</span><span class="sxs-lookup"><span data-stu-id="05d56-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="05d56-111">Expanda o menu **armazenamento da sessão** .</span><span class="sxs-lookup"><span data-stu-id="05d56-111">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="O menu de armazenamento de sessão" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="05d56-113">O menu de **armazenamento de sessão**</span><span class="sxs-lookup"><span data-stu-id="05d56-113">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="05d56-114">Selecione um domínio para ver os pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="05d56-114">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Os pares de chave-valor ' sessionStorage '" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="05d56-116">Os `sessionStorage` pares de valor chave</span><span class="sxs-lookup"><span data-stu-id="05d56-116">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="05d56-117">Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="05d56-117">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Exibir o valor da chave x-Sid" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="05d56-119">Exibir o valor da `x-sid` chave</span><span class="sxs-lookup"><span data-stu-id="05d56-119">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="05d56-120">Criar um novo par de chave-valor sessionStorage</span><span class="sxs-lookup"><span data-stu-id="05d56-120">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="05d56-121">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="05d56-121">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="05d56-122">Clique duas vezes na parte vazia da tabela.</span><span class="sxs-lookup"><span data-stu-id="05d56-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="05d56-123">O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .</span><span class="sxs-lookup"><span data-stu-id="05d56-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave" lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="05d56-125">A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave</span><span class="sxs-lookup"><span data-stu-id="05d56-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="05d56-126">Editar chaves ou valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="05d56-126">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="05d56-127">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="05d56-127">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="05d56-128">Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.</span><span class="sxs-lookup"><span data-stu-id="05d56-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Editar uma chave sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="05d56-130">Editar uma `sessionStorage` chave</span><span class="sxs-lookup"><span data-stu-id="05d56-130">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="05d56-131">Excluir pares de chave-valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="05d56-131">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="05d56-132">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="05d56-132">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="05d56-133">Selecione o par chave-valor que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="05d56-133">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="05d56-134">O DevTools realça tudo em azul para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="05d56-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="05d56-135">Pressione a `Delete` tecla ou clique em **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="05d56-135">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="05d56-136">Excluir todos os pares de chave-valor sessionStorage de um domínio</span><span class="sxs-lookup"><span data-stu-id="05d56-136">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="05d56-137">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="05d56-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="05d56-138">Selecione **limpar tudo** \ ( ![ limpar tudo ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="05d56-138">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="05d56-139">Interagir com o sessionStorage a partir do console</span><span class="sxs-lookup"><span data-stu-id="05d56-139">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="05d56-140">Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `sessionStorage` partir do **console**.</span><span class="sxs-lookup"><span data-stu-id="05d56-140">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="05d56-141">Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se desejar acessar os `sessionStorage` pares de valores chave de um domínio que não sejam a página em que você está.</span><span class="sxs-lookup"><span data-stu-id="05d56-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Alterar o contexto JavaScript do console" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="05d56-143">Alterar o contexto JavaScript do console</span><span class="sxs-lookup"><span data-stu-id="05d56-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="05d56-144">Execute suas `sessionStorage` expressões no console, da mesma forma que faria no JavaScript.</span><span class="sxs-lookup"><span data-stu-id="05d56-144">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Interagir com o sessionStorage a partir do console" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="05d56-146">Interagir com `sessionStorage` base no **console**</span><span class="sxs-lookup"><span data-stu-id="05d56-146">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="05d56-149">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="05d56-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="05d56-150">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="05d56-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="05d56-152">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="05d56-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
