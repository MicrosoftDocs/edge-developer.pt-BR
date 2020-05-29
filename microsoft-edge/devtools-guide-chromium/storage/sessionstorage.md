---
title: Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612078"
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





# <span data-ttu-id="d13e6-103">Exibir e editar o armazenamento da sessão com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d13e6-103">View And Edit Session Storage With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="d13e6-104">Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para exibir, editar e excluir [`sessionStorage`][MDNSessionStorage] pares de valores de chave.</span><span class="sxs-lookup"><span data-stu-id="d13e6-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="d13e6-105">Exibir chaves e valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="d13e6-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="d13e6-106">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="d13e6-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="d13e6-107">O painel **manifestar** é mostrado por padrão.</span><span class="sxs-lookup"><span data-stu-id="d13e6-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-108">Figura 1</span><span class="sxs-lookup"><span data-stu-id="d13e6-108">Figure 1</span></span>  
    > <span data-ttu-id="d13e6-109">Painel de manifesto</span><span class="sxs-lookup"><span data-stu-id="d13e6-109">The Manifest pane</span></span>  
    > ![Painel de manifesto][ImageManifest]  

1.  <span data-ttu-id="d13e6-111">Expanda o menu **armazenamento da sessão** .</span><span class="sxs-lookup"><span data-stu-id="d13e6-111">Expand the **Session Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="d13e6-112">Figure 2</span></span>  
    > <span data-ttu-id="d13e6-113">O menu de **armazenamento de sessão**</span><span class="sxs-lookup"><span data-stu-id="d13e6-113">The **Session Storage** Menu</span></span>  
    > ![O menu de armazenamento de sessão][ImageSessionStorageMenu]  

1.  <span data-ttu-id="d13e6-115">Selecione um domínio para ver os pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="d13e6-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-116">Figura 3</span><span class="sxs-lookup"><span data-stu-id="d13e6-116">Figure 3</span></span>  
    > <span data-ttu-id="d13e6-117">Os pares de chave-valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="d13e6-117">The sessionStorage key-value pairs</span></span>  
    > ![Os pares de chave-valor ' sessionStorage '][ImageSessionStorage]  

1.  <span data-ttu-id="d13e6-119">Selecione uma linha da tabela para exibir o valor no visualizador abaixo da tabela.</span><span class="sxs-lookup"><span data-stu-id="d13e6-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-120">Figura 4</span><span class="sxs-lookup"><span data-stu-id="d13e6-120">Figure 4</span></span>  
    > <span data-ttu-id="d13e6-121">Exibir o valor da `x-sid` chave</span><span class="sxs-lookup"><span data-stu-id="d13e6-121">Viewing the value of the `x-sid` key</span></span>  
    > ![Exibir o valor da chave x-Sid][ImageSessionStorageViewer]  

## <span data-ttu-id="d13e6-123">Criar um novo par de chave-valor sessionStorage</span><span class="sxs-lookup"><span data-stu-id="d13e6-123">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="d13e6-124">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d13e6-124">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d13e6-125">Clique duas vezes na parte vazia da tabela.</span><span class="sxs-lookup"><span data-stu-id="d13e6-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="d13e6-126">O DevTools cria uma nova linha e enfoca o cursor na coluna **chave** .</span><span class="sxs-lookup"><span data-stu-id="d13e6-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-127">Figura 5</span><span class="sxs-lookup"><span data-stu-id="d13e6-127">Figure 5</span></span>  
    > <span data-ttu-id="d13e6-128">A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave</span><span class="sxs-lookup"><span data-stu-id="d13e6-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![A parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave][ImageSessionStorageCreate]  

## <span data-ttu-id="d13e6-130">Editar chaves ou valores de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="d13e6-130">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="d13e6-131">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d13e6-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d13e6-132">Clique duas vezes em uma célula na coluna **chave** ou **valor** para editar essa chave ou valor.</span><span class="sxs-lookup"><span data-stu-id="d13e6-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-133">Figura 6</span><span class="sxs-lookup"><span data-stu-id="d13e6-133">Figure 6</span></span>  
    > <span data-ttu-id="d13e6-134">Editando uma `sessionStorage` chave</span><span class="sxs-lookup"><span data-stu-id="d13e6-134">Editing a `sessionStorage` key</span></span>  
    > ![Editando uma chave sessionStorage][ImageSessionStorageEdit]  

## <span data-ttu-id="d13e6-136">Excluir pares de chave-valor de sessionStorage</span><span class="sxs-lookup"><span data-stu-id="d13e6-136">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="d13e6-137">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d13e6-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d13e6-138">Selecione o par chave-valor que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="d13e6-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="d13e6-139">O DevTools realça tudo em azul para indicar que está selecionado.</span><span class="sxs-lookup"><span data-stu-id="d13e6-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="d13e6-140">Pressione a `Delete` tecla ou clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="d13e6-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="d13e6-141">Excluir todos os pares de chave-valor sessionStorage de um domínio</span><span class="sxs-lookup"><span data-stu-id="d13e6-141">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="d13e6-142">[Exiba os `sessionStorage` pares de valores chave de um domínio](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d13e6-142">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="d13e6-143">Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="d13e6-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="d13e6-144">Interagir com o sessionStorage a partir do console</span><span class="sxs-lookup"><span data-stu-id="d13e6-144">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="d13e6-145">Como você pode executar JavaScript no **console**e, como o **console** tem acesso aos contextos de JavaScript da página, é possível interagir com a `sessionStorage` partir do **console**.</span><span class="sxs-lookup"><span data-stu-id="d13e6-145">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="d13e6-146">Use o menu de **contextos de JavaScript** para alterar o contexto de JavaScript do **console** se desejar acessar os `sessionStorage` pares de valores chave de um domínio que não sejam a página em que você está.</span><span class="sxs-lookup"><span data-stu-id="d13e6-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-147">Figura 7</span><span class="sxs-lookup"><span data-stu-id="d13e6-147">Figure 7</span></span>  
    > <span data-ttu-id="d13e6-148">Alterando o contexto JavaScript do **console**</span><span class="sxs-lookup"><span data-stu-id="d13e6-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Alterando o contexto JavaScript do console][ImageJSContext]  

1.  <span data-ttu-id="d13e6-150">Execute suas `sessionStorage` expressões no console, da mesma forma que faria no JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d13e6-150">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="d13e6-151">Figura 8</span><span class="sxs-lookup"><span data-stu-id="d13e6-151">Figure 8</span></span>  
    > <span data-ttu-id="d13e6-152">Interagindo com `sessionStorage` o do **console**</span><span class="sxs-lookup"><span data-stu-id="d13e6-152">Interacting with `sessionStorage` from the **Console**</span></span>  
    > ![Interagindo com o sessionStorage a partir do console][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Figura 2: o menu de armazenamento da sessão"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Figura 3: os pares de chave-valor de sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Figura 4: exibindo o valor da chave x-Sid"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Figura 5: a parte vazia da tabela para clicar duas vezes para criar um novo par de valores chave"  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Figura 6: editando uma chave sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Figura 7: alterando o contexto JavaScript do console"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Figura 8: interagindo com o sessionStorage a partir do console"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="d13e6-164">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d13e6-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d13e6-165">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d13e6-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d13e6-167">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d13e6-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
