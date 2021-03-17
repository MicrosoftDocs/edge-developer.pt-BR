---
description: Como exibir e editar localStorage com o painel Armazenamento Local e o Console.
title: Exibir e editar o armazenamento local com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4eebf3108e7b1c6ecaecbfed445e8f3fe26215c4
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439672"
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

# <a name="view-and-edit-local-storage-with-microsoft-edge-devtools"></a><span data-ttu-id="67b51-104">Exibir e editar o armazenamento local com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="67b51-104">View and edit local storage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="67b51-105">Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para exibir, editar e excluir pares de valores de [chave localStorage.][MDNWindowsLocalStorage]</span><span class="sxs-lookup"><span data-stu-id="67b51-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <a name="view-localstorage-keys-and-values"></a><span data-ttu-id="67b51-106">Exibir chaves e valores localStorage</span><span class="sxs-lookup"><span data-stu-id="67b51-106">View localStorage keys and values</span></span>  

1.  <span data-ttu-id="67b51-107">Escolha a **guia Aplicativo** para abrir a **ferramenta Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="67b51-107">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="67b51-108">O **painel** Manifesto é mostrado por padrão.</span><span class="sxs-lookup"><span data-stu-id="67b51-108">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="67b51-110">O **painel** Manifesto</span><span class="sxs-lookup"><span data-stu-id="67b51-110">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="67b51-111">Expanda o menu **Armazenamento** Local.</span><span class="sxs-lookup"><span data-stu-id="67b51-111">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="O menu Armazenamento Local" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="67b51-113">O **menu Armazenamento Local**</span><span class="sxs-lookup"><span data-stu-id="67b51-113">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="67b51-114">Escolha um domínio para exibir os pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="67b51-114">Choose a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="Os pares de valores de chave localStorage para o https://www.bing.com domínio" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="67b51-116">Os `localStorage` pares de valores-chave para o `https://www.bing.com` domínio</span><span class="sxs-lookup"><span data-stu-id="67b51-116">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="67b51-117">Escolha uma linha da tabela para exibir o valor no visualizador abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="67b51-117">Choose a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Exibir o valor da tecla eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="67b51-119">Exibir o valor da `eventLogQueue_Online` chave</span><span class="sxs-lookup"><span data-stu-id="67b51-119">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <a name="create-a-new-localstorage-key-value-pair"></a><span data-ttu-id="67b51-120">Criar um novo par de valores de chave localStorage</span><span class="sxs-lookup"><span data-stu-id="67b51-120">Create a new localStorage key-value pair</span></span>  

1.  <span data-ttu-id="67b51-121">[Exibir os pares de valores de chave localStorage de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="67b51-121">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="67b51-122">Clique duas vezes na parte vazia da tabela.</span><span class="sxs-lookup"><span data-stu-id="67b51-122">Double-click the empty part of the table.</span></span>  <span data-ttu-id="67b51-123">O DevTools cria uma nova linha e concentra seu cursor na **coluna** Chave.</span><span class="sxs-lookup"><span data-stu-id="67b51-123">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="A parte vazia da tabela para clicar duas vezes para criar um novo par de valores de chave" lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="67b51-125">A parte vazia da tabela para clicar duas vezes para criar um novo par de valores de chave</span><span class="sxs-lookup"><span data-stu-id="67b51-125">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <a name="edit-localstorage-keys-or-values"></a><span data-ttu-id="67b51-126">Editar chaves ou valores localStorage</span><span class="sxs-lookup"><span data-stu-id="67b51-126">Edit localStorage keys or values</span></span>  

1.  <span data-ttu-id="67b51-127">[Exibir os pares de valores de chave localStorage de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="67b51-127">[View the localStorage key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="67b51-128">Clique duas vezes em uma célula na coluna **Chave** ou **Valor** para editar essa chave ou valor.</span><span class="sxs-lookup"><span data-stu-id="67b51-128">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Editar uma chave localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="67b51-130">Editar uma `localStorage` chave</span><span class="sxs-lookup"><span data-stu-id="67b51-130">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <a name="delete-localstorage-key-value-pairs"></a><span data-ttu-id="67b51-131">Excluir pares de valores de chave localStorage</span><span class="sxs-lookup"><span data-stu-id="67b51-131">Delete localStorage key-value pairs</span></span>  

1.  <span data-ttu-id="67b51-132">[Exibir os `localStorage` pares de valores-chave de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="67b51-132">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="67b51-133">Escolha o par de valores-chave que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="67b51-133">Choose the key-value pair that you want to delete.</span></span>  <span data-ttu-id="67b51-134">O DevTools realça o azul para indicar que ele está selecionado.</span><span class="sxs-lookup"><span data-stu-id="67b51-134">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="67b51-135">Selecione a `Delete` chave ou escolha Excluir **Selecionado** \( Excluir ![ Selecionado ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="67b51-135">Select the `Delete` key or choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-localstorage-key-value-pairs-for-a-domain"></a><span data-ttu-id="67b51-136">Excluir todos `localStorage` os pares de valores-chave para um domínio</span><span class="sxs-lookup"><span data-stu-id="67b51-136">Delete all `localStorage` key-value pairs for a domain</span></span>  

1.  <span data-ttu-id="67b51-137">[Exibir os `localStorage` pares de valores-chave de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="67b51-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="67b51-138">Escolha **Limpar Tudo** \( Limpar Tudo ![ ](../media/clear-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="67b51-138">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\).</span></span>  
    
## <a name="interact-with-localstorage-from-the-console"></a><span data-ttu-id="67b51-139">Interagir com localStorage do Console</span><span class="sxs-lookup"><span data-stu-id="67b51-139">Interact with localStorage from the Console</span></span>  

<span data-ttu-id="67b51-140">Como você é capaz de executar JavaScript no **Console**e, como o **Console** tem acesso aos contextos JavaScript da página, é possível interagir com a partir do `localStorage` **Console**.</span><span class="sxs-lookup"><span data-stu-id="67b51-140">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="67b51-141">Use o menu **de contextos JavaScript** para alterar o contexto JavaScript do **Console** se você quiser acessar os pares de valores-chave de um domínio diferente da página `localStorage` exibida.</span><span class="sxs-lookup"><span data-stu-id="67b51-141">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Alterar o contexto JavaScript do Console" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="67b51-143">Alterar o contexto JavaScript do Console</span><span class="sxs-lookup"><span data-stu-id="67b51-143">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="67b51-144">Execute suas `localStorage` expressões no Console, da mesma forma que você faz em seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="67b51-144">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Interagir com localStorage do Console" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="67b51-146">Interagir `localStorage` com a partir do **Console**</span><span class="sxs-lookup"><span data-stu-id="67b51-146">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="67b51-147">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="67b51-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window.localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="67b51-150">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="67b51-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="67b51-151">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="67b51-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="67b51-153">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="67b51-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
