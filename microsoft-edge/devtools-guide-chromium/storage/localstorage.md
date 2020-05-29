---
title: Exibir e editar armazenamento local com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612008"
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





# <span data-ttu-id="e94ff-103">Exibir e editar armazenamento local com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e94ff-103">View And Edit Local Storage With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="e94ff-104">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir, editar e excluir [`localStorage`][MDNWindowsLocalStorage] pares de valores de chave.</span><span class="sxs-lookup"><span data-stu-id="e94ff-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`localStorage`][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="e94ff-105">Exibir chaves e valores de localStorage</span><span class="sxs-lookup"><span data-stu-id="e94ff-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="e94ff-106">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="e94ff-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="e94ff-107">O painel **manifestar** é mostrado por padrão.</span><span class="sxs-lookup"><span data-stu-id="e94ff-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-108">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e94ff-108">Figure 1</span></span>  
    > <span data-ttu-id="e94ff-109">Painel de manifesto</span><span class="sxs-lookup"><span data-stu-id="e94ff-109">The Manifest pane</span></span>  
    > ![Painel de manifesto][ImageManifest]  

1.  <span data-ttu-id="e94ff-111">Expanda o menu **armazenamento local** .</span><span class="sxs-lookup"><span data-stu-id="e94ff-111">Expand the **Local Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e94ff-112">Figure 2</span></span>  
    > <span data-ttu-id="e94ff-113">O menu **armazenamento local** mostra dois domínios: `https://business.bing.com` e</span><span class="sxs-lookup"><span data-stu-id="e94ff-113">The **Local Storage** menu shows two domains: `https://business.bing.com` and</span></span> `https://www.bing.com`  
    > ![O menu armazenamento local][ImageLocalStorageMenu]  

1.  <span data-ttu-id="e94ff-115">Selecione um domínio para ver os pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="e94ff-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-116">Figura 3</span><span class="sxs-lookup"><span data-stu-id="e94ff-116">Figure 3</span></span>  
    > <span data-ttu-id="e94ff-117">Os `localStorage` pares de valor chave do `https://www.bing.com` domínio</span><span class="sxs-lookup"><span data-stu-id="e94ff-117">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    > ![Os pares de chave-valor de localStorage para o https://www.bing.com domínio][ImageLocalStorage]  

1.  <span data-ttu-id="e94ff-119">Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="e94ff-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-120">Figura 4</span><span class="sxs-lookup"><span data-stu-id="e94ff-120">Figure 4</span></span>  
    > <span data-ttu-id="e94ff-121">Exibir o valor da `eventLogQueue_Online` chave</span><span class="sxs-lookup"><span data-stu-id="e94ff-121">Viewing the value of the `eventLogQueue_Online` key</span></span>  
    > ![Exibir o valor da chave eventLogQueue_Online][ImageLocalStorageViewer]  

## <span data-ttu-id="e94ff-123">Criar um novo `localStorage` par chave-valor</span><span class="sxs-lookup"><span data-stu-id="e94ff-123">Create a new `localStorage` key-value pair</span></span>   

1.  <span data-ttu-id="e94ff-124">[Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="e94ff-124">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="e94ff-125">Clique duas vezes na parte vazia da tabela.</span><span class="sxs-lookup"><span data-stu-id="e94ff-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="e94ff-126">O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .</span><span class="sxs-lookup"><span data-stu-id="e94ff-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-127">Figura 5</span><span class="sxs-lookup"><span data-stu-id="e94ff-127">Figure 5</span></span>  
    > <span data-ttu-id="e94ff-128">A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave</span><span class="sxs-lookup"><span data-stu-id="e94ff-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave][ImageLocalStorageCreate]  

## <span data-ttu-id="e94ff-130">Editar `localStorage` chaves ou valores</span><span class="sxs-lookup"><span data-stu-id="e94ff-130">Edit `localStorage` keys or values</span></span>   

1.  <span data-ttu-id="e94ff-131">[Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="e94ff-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="e94ff-132">Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.</span><span class="sxs-lookup"><span data-stu-id="e94ff-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-133">Figura 6</span><span class="sxs-lookup"><span data-stu-id="e94ff-133">Figure 6</span></span>  
    > <span data-ttu-id="e94ff-134">Editando uma `localStorage` chave</span><span class="sxs-lookup"><span data-stu-id="e94ff-134">Editing a `localStorage` key</span></span>  
    > ![Editando uma chave localStorage][ImageLocalStorageEdit]  

## <span data-ttu-id="e94ff-136">Excluir `localStorage` pares de chave-valor</span><span class="sxs-lookup"><span data-stu-id="e94ff-136">Delete `localStorage` key-value pairs</span></span>   

1.  <span data-ttu-id="e94ff-137">[Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="e94ff-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="e94ff-138">Selecione o par chave-valor que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="e94ff-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="e94ff-139">O DevTools realça tudo em azul para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="e94ff-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="e94ff-140">Pressione a `Delete` tecla ou clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="e94ff-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="e94ff-141">Excluir todos os `localStorage` pares de valores chave de um domínio</span><span class="sxs-lookup"><span data-stu-id="e94ff-141">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="e94ff-142">[Exiba os `localStorage` pares de valores chave de um domínio](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="e94ff-142">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="e94ff-143">Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="e94ff-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="e94ff-144">Interagir com `localStorage` base no console</span><span class="sxs-lookup"><span data-stu-id="e94ff-144">Interact with `localStorage` from the Console</span></span>   

<span data-ttu-id="e94ff-145">Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `localStorage` partir do **console**.</span><span class="sxs-lookup"><span data-stu-id="e94ff-145">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="e94ff-146">Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se você quiser acessar os `localStorage` pares de valores chave de um domínio que não sejam a página exibida.</span><span class="sxs-lookup"><span data-stu-id="e94ff-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-147">Figura 7</span><span class="sxs-lookup"><span data-stu-id="e94ff-147">Figure 7</span></span>  
    > <span data-ttu-id="e94ff-148">Alterando o contexto JavaScript do **console**</span><span class="sxs-lookup"><span data-stu-id="e94ff-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Alterando o contexto JavaScript do console][ImageJSContext]  

1.  <span data-ttu-id="e94ff-150">Execute suas `localStorage` expressões no console, o mesmo que você faz em seu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e94ff-150">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="e94ff-151">Figura 8</span><span class="sxs-lookup"><span data-stu-id="e94ff-151">Figure 8</span></span>  
    > <span data-ttu-id="e94ff-152">Interagindo com `localStorage` o do **console**</span><span class="sxs-lookup"><span data-stu-id="e94ff-152">Interacting with `localStorage` from the **Console**</span></span>  
    > ![Interagindo com o localStorage a partir do console][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Figura 2: o menu armazenamento local"  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Figura 3: os pares de chave-valor de localStorage para o https://www.bing.com domínio"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Figura 4: exibindo o valor da tecla eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Figura 5: a parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave"  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Figura 6: editando uma chave localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Figura 7: alterando o contexto JavaScript do console"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Figura 8: interagindo com o localStorage a partir do console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="e94ff-164">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="e94ff-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e94ff-165">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e94ff-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e94ff-167">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e94ff-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
