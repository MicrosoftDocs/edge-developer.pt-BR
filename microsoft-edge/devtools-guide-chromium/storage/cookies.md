---
title: Exibir, editar e Excluir cookies com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 084c4116cd4c9c5e70b2fe341257fa68ba2c8ae7
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612064"
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





# <span data-ttu-id="b6ad6-103">Exibir, editar e Excluir cookies com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b6ad6-103">View, Edit, And Delete Cookies With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="b6ad6-104">[Os cookies http][MDNHTTPCookies] são usados principalmente para gerenciar sessões de usuário, armazenar preferências de personalização de usuário e rastrear o comportamento do usuário.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="b6ad6-105">Eles também são a causa de todos os formulários de consentimento "Esta página usados por cookies" irritantes exibidos na Web.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-105">They are also the cause of all of those annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="b6ad6-106">Este guia ensina a exibir, editar e excluir os cookies HTTP de uma página com o [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-106">This guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="b6ad6-107">Abrir o painel cookies</span><span class="sxs-lookup"><span data-stu-id="b6ad6-107">Open the Cookies pane</span></span>   

1.  <span data-ttu-id="b6ad6-108">[Abra o devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="b6ad6-109">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="b6ad6-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="b6ad6-110">O painel de **manifesto** deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-110">The **Manifest** pane should open.</span></span>  
    
    > ##### <span data-ttu-id="b6ad6-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b6ad6-111">Figure 1</span></span>  
    > <span data-ttu-id="b6ad6-112">Painel de manifesto</span><span class="sxs-lookup"><span data-stu-id="b6ad6-112">The Manifest pane</span></span>  
    > ![Painel de manifesto][ImageManifest]  

1.  <span data-ttu-id="b6ad6-114">Em **armazenamento** expanda **cookies**, selecione uma origem.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    > ##### <span data-ttu-id="b6ad6-115">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b6ad6-115">Figure 2</span></span>  
    > <span data-ttu-id="b6ad6-116">O painel cookies</span><span class="sxs-lookup"><span data-stu-id="b6ad6-116">The Cookies pane</span></span>  
    > ![O painel cookies][ImageCookies]  

## <span data-ttu-id="b6ad6-118">Campos</span><span class="sxs-lookup"><span data-stu-id="b6ad6-118">Fields</span></span>   

<span data-ttu-id="b6ad6-119">A tabela **cookies** contém os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="b6ad6-119">The **Cookies** table contains the following fields:</span></span>  

*   <span data-ttu-id="b6ad6-120">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-120">**Name**.</span></span>  <span data-ttu-id="b6ad6-121">O nome do cookie.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-121">The name of the cookie.</span></span>  
*   <span data-ttu-id="b6ad6-122">**Valor**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-122">**Value**.</span></span>  <span data-ttu-id="b6ad6-123">O valor do cookie.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-123">The value of the cookie.</span></span>  
*   <span data-ttu-id="b6ad6-124">**Domínio**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-124">**Domain**.</span></span>  <span data-ttu-id="b6ad6-125">Os hosts que têm permissão para receber o cookie.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-125">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="b6ad6-126">Consulte [escopo de cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-126">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="b6ad6-127">**Caminho**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-127">**Path**.</span></span>  <span data-ttu-id="b6ad6-128">A URL que deve existir na URL solicitada para enviar o `Cookie` cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-128">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="b6ad6-129">Consulte [escopo de cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-129">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="b6ad6-130">**Vencimento/Max-age**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-130">**Expires / Max-Age**.</span></span>  <span data-ttu-id="b6ad6-131">A data de expiração ou a idade máxima do cookie.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-131">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="b6ad6-132">Ver [cookies permanentes][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-132">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="b6ad6-133">Para [os cookies de sessão][MDNHTTPCookiesSession] , esse valor é sempre `Session` .</span><span class="sxs-lookup"><span data-stu-id="b6ad6-133">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="b6ad6-134">**Tamanho**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-134">**Size**.</span></span>  <span data-ttu-id="b6ad6-135">O tamanho, em bytes, do cookie.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-135">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="b6ad6-136">**Http**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-136">**HTTP**.</span></span>  <span data-ttu-id="b6ad6-137">Se verdadeiro, esse campo indica que o cookie só deve ser usado por HTTP e modificação de JavaScript não é permitido.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-137">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="b6ad6-138">Consulte [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-138">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="b6ad6-139">**Seguro**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-139">**Secure**.</span></span>  <span data-ttu-id="b6ad6-140">Se verdadeiro, este campo indica que o cookie deve ser enviado para o servidor somente por meio de uma conexão HTTPS segura.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-140">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="b6ad6-141">Veja [proteger cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-141">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="b6ad6-142">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-142">**SameSite**.</span></span>  <span data-ttu-id="b6ad6-143">Contém `strict` ou `lax` se o cookie está usando o atributo experimental [SameSite][MDNHTTPCookiesSamesite] .</span><span class="sxs-lookup"><span data-stu-id="b6ad6-143">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  

## <span data-ttu-id="b6ad6-144">Filtrar cookies</span><span class="sxs-lookup"><span data-stu-id="b6ad6-144">Filter cookies</span></span>   

<span data-ttu-id="b6ad6-145">Use a caixa de texto **Filtrar** para filtrar cookies por **nome** ou **valor**.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="b6ad6-146">Não há suporte para filtragem de outros campos.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-146">Filtering by other fields is not supported.</span></span>  

> ##### <span data-ttu-id="b6ad6-147">Figura 3</span><span class="sxs-lookup"><span data-stu-id="b6ad6-147">Figure 3</span></span>  
> <span data-ttu-id="b6ad6-148">Filtragem de qualquer cookie que não contenha o texto</span><span class="sxs-lookup"><span data-stu-id="b6ad6-148">Filtering out any cookies that do not contain the text</span></span> `ID`  
> ![Filtragem de quaisquer cookies que não contenham a ID de texto][ImageCookiesFilter]  

## <span data-ttu-id="b6ad6-150">Editar um cookie</span><span class="sxs-lookup"><span data-stu-id="b6ad6-150">Edit a cookie</span></span>   

<span data-ttu-id="b6ad6-151">Os campos **nome**, **valor**, **domínio**, **caminho**e **vencimento/máx** . da idade são editáveis.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="b6ad6-152">Clique duas vezes em um campo para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-152">Double-click a field to edit it.</span></span>  

> ##### <span data-ttu-id="b6ad6-153">Figura 4</span><span class="sxs-lookup"><span data-stu-id="b6ad6-153">Figure 4</span></span>  
> <span data-ttu-id="b6ad6-154">Definindo o nome de um cookie como</span><span class="sxs-lookup"><span data-stu-id="b6ad6-154">Setting the name of a cookie to</span></span> `DEVTOOLS!`  
> ![Configurando o nome de um cookie para DEVTOOLS!][ImageEditCookie]  

## <span data-ttu-id="b6ad6-156">Excluir cookies</span><span class="sxs-lookup"><span data-stu-id="b6ad6-156">Delete cookies</span></span>   

<span data-ttu-id="b6ad6-157">Selecione um cookie e clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] para excluir um cookie.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-157">Select a cookie and then click **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete that one cookie.</span></span>  

> ##### <span data-ttu-id="b6ad6-158">Figura 5</span><span class="sxs-lookup"><span data-stu-id="b6ad6-158">Figure 5</span></span>  
> <span data-ttu-id="b6ad6-159">Excluindo um cookie específico</span><span class="sxs-lookup"><span data-stu-id="b6ad6-159">Deleting a specific cookie</span></span>  
> ![Excluindo um cookie específico][ImageDeleteCookie]  

<span data-ttu-id="b6ad6-161">Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] para excluir todos os cookies.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-161">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

> ##### <span data-ttu-id="b6ad6-162">Figura 6</span><span class="sxs-lookup"><span data-stu-id="b6ad6-162">Figure 6</span></span>  
> <span data-ttu-id="b6ad6-163">Limpar todos os cookies</span><span class="sxs-lookup"><span data-stu-id="b6ad6-163">Clearing all cookies</span></span>  
> ![Limpar todos os cookies][ImageClearAllCookies]  

<!--    -->  

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Figura 1: o painel manifestar"  
[ImageCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-selected.msft.png "Figura 2: o painel cookies"  
[ImageCookiesFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-filter-id.msft.png "Figura 3: filtragem de qualquer cookie que não contenha a ID de texto"  
[ImageEditCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-rename.msft.png "Figura 4: Configurando o nome de um cookie para DEVTOOLS!"  
[ImageDeleteCookie]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-delete-selected.msft.png "Figura 5: excluindo um cookie específico"  
[ImageClearAllCookies]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-cookies-clear-all.msft.png "Figura 6: limpeza de todos os cookies"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP-cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP-cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP-escopo de cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP-cookies seguros e HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP-cookies de sessão | MDN"  

> [!NOTE]
> <span data-ttu-id="b6ad6-179">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="b6ad6-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b6ad6-180">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b6ad6-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b6ad6-182">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b6ad6-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
