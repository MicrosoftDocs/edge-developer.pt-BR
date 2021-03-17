---
description: Saiba como exibir, editar e excluir os cookies HTTP de uma página usando o Microsoft Edge DevTools.
title: Exibir, editar e excluir cookies com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c208ca628fe91ed5922bc36566be2b9bdd20ec0b
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439679"
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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a><span data-ttu-id="49cfc-104">Exibir, editar e excluir cookies com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49cfc-104">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="49cfc-105">[Cookies HTTP][MDNHTTPCookies] são usados principalmente para gerenciar sessões de usuário, armazenar preferências de personalização do usuário e acompanhar o comportamento do usuário.</span><span class="sxs-lookup"><span data-stu-id="49cfc-105">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="49cfc-106">Cookies também são a causa de todos os irritantes que **essa página usa** os formulários de consentimento de cookies encontrados na Web.</span><span class="sxs-lookup"><span data-stu-id="49cfc-106">Cookies are also the cause of all of the annoying **this page uses cookies** consent forms that are found across the web.</span></span>  <span data-ttu-id="49cfc-107">O guia a seguir ensina como exibir, editar e excluir os cookies HTTP de uma página da Web com [o Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="49cfc-107">The following guide teaches you how to view, edit, and delete the HTTP cookies for a webpage with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-the-cookies-pane"></a><span data-ttu-id="49cfc-108">Abra o painel Cookies</span><span class="sxs-lookup"><span data-stu-id="49cfc-108">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="49cfc-109">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="49cfc-109">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="49cfc-110">Escolha a **guia Aplicativo** para abrir o **painel Aplicativo.**</span><span class="sxs-lookup"><span data-stu-id="49cfc-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="49cfc-111">O **painel Manifesto** deve abrir.</span><span class="sxs-lookup"><span data-stu-id="49cfc-111">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="49cfc-113">Figura 1: o painel Manifesto</span><span class="sxs-lookup"><span data-stu-id="49cfc-113">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="49cfc-114">Em **Armazenamento** **expanda Cookies,** selecione uma origem.</span><span class="sxs-lookup"><span data-stu-id="49cfc-114">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="O painel Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="49cfc-116">Figura 2: o painel Cookies</span><span class="sxs-lookup"><span data-stu-id="49cfc-116">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <a name="fields"></a><span data-ttu-id="49cfc-117">Campos</span><span class="sxs-lookup"><span data-stu-id="49cfc-117">Fields</span></span>  

<span data-ttu-id="49cfc-118">A **tabela Cookies** contém os campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="49cfc-118">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="49cfc-119">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-119">**Name**.</span></span>  <span data-ttu-id="49cfc-120">O nome do cookie.</span><span class="sxs-lookup"><span data-stu-id="49cfc-120">The name of the cookie.</span></span>  
*   <span data-ttu-id="49cfc-121">**Valor**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-121">**Value**.</span></span>  <span data-ttu-id="49cfc-122">O valor do cookie.</span><span class="sxs-lookup"><span data-stu-id="49cfc-122">The value of the cookie.</span></span>  
*   <span data-ttu-id="49cfc-123">**Domínio**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-123">**Domain**.</span></span>  <span data-ttu-id="49cfc-124">Os hosts que têm permissão para receber o cookie.</span><span class="sxs-lookup"><span data-stu-id="49cfc-124">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="49cfc-125">Navegue [até Escopo de cookies.][MDNHTTPCookiesScope]</span><span class="sxs-lookup"><span data-stu-id="49cfc-125">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="49cfc-126">**Caminho**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-126">**Path**.</span></span>  <span data-ttu-id="49cfc-127">A URL que deve existir na URL solicitada para enviar `Cookie` o header.</span><span class="sxs-lookup"><span data-stu-id="49cfc-127">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="49cfc-128">Navegue [até Escopo de cookies.][MDNHTTPCookiesScope]</span><span class="sxs-lookup"><span data-stu-id="49cfc-128">Navigate to [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="49cfc-129">**Expira / Max-Age**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-129">**Expires / Max-Age**.</span></span>  <span data-ttu-id="49cfc-130">A data de expiração ou a idade máxima do cookie.</span><span class="sxs-lookup"><span data-stu-id="49cfc-130">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="49cfc-131">Navegue até [Cookies permanentes][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="49cfc-131">Navigate to [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="49cfc-132">Para [cookies de sessão,][MDNHTTPCookiesSession] esse valor é sempre `Session` .</span><span class="sxs-lookup"><span data-stu-id="49cfc-132">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="49cfc-133">**Tamanho**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-133">**Size**.</span></span>  <span data-ttu-id="49cfc-134">O tamanho, em bytes, do cookie.</span><span class="sxs-lookup"><span data-stu-id="49cfc-134">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="49cfc-135">**HTTP**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-135">**HTTP**.</span></span>  <span data-ttu-id="49cfc-136">Se for true, este campo indica que o cookie só deve ser usado em HTTP e a modificação do JavaScript não é permitida.</span><span class="sxs-lookup"><span data-stu-id="49cfc-136">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="49cfc-137">Navegue [até Cookies HttpOnly.][MDNHTTPCookiesSecure]</span><span class="sxs-lookup"><span data-stu-id="49cfc-137">Navigate to [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="49cfc-138">**Proteger**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-138">**Secure**.</span></span>  <span data-ttu-id="49cfc-139">Se for true, esse campo indica que o cookie deve ser enviado para o servidor somente por meio de uma conexão HTTPS segura.</span><span class="sxs-lookup"><span data-stu-id="49cfc-139">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="49cfc-140">Navegue até [Cookies seguros.][MDNHTTPCookiesSecure]</span><span class="sxs-lookup"><span data-stu-id="49cfc-140">Navigate to [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="49cfc-141">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-141">**SameSite**.</span></span>  <span data-ttu-id="49cfc-142">Contém `strict` ou se o cookie está usando o atributo Experimental `lax` [Samesite.][MDNHTTPCookiesSamesite]</span><span class="sxs-lookup"><span data-stu-id="49cfc-142">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="49cfc-143">**Prioridade**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-143">**Priority**.</span></span>  <span data-ttu-id="49cfc-144">Contém `low` , `medium` \(default\) ou se o cookie está usando o atributo de Prioridade de `high` [cookie][ChromiumIssue232693] preterido.</span><span class="sxs-lookup"><span data-stu-id="49cfc-144">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <a name="filter-cookies"></a><span data-ttu-id="49cfc-145">Cookies de filtro</span><span class="sxs-lookup"><span data-stu-id="49cfc-145">Filter cookies</span></span>  

<span data-ttu-id="49cfc-146">Use a **caixa de texto** Filtro para filtrar cookies por **Nome** ou **Valor**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-146">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="49cfc-147">Não há suporte para filtragem por outros campos.</span><span class="sxs-lookup"><span data-stu-id="49cfc-147">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrando cookies que não contenham a ID de texto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="49cfc-149">Figura 3: Filtrando todos os cookies que não contenham o texto</span><span class="sxs-lookup"><span data-stu-id="49cfc-149">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a><span data-ttu-id="49cfc-150">Editar um cookie</span><span class="sxs-lookup"><span data-stu-id="49cfc-150">Edit a cookie</span></span>  

<span data-ttu-id="49cfc-151">Os **campos Nome**, **Valor,** **Domínio**, **Caminho**e Expira **/ Max-Age** são editáveis.</span><span class="sxs-lookup"><span data-stu-id="49cfc-151">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="49cfc-152">Clique duas vezes em um campo para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="49cfc-152">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Definindo o nome de um cookie como DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="49cfc-154">Figura 4: Definindo o nome de um cookie como</span><span class="sxs-lookup"><span data-stu-id="49cfc-154">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a><span data-ttu-id="49cfc-155">Excluir cookies</span><span class="sxs-lookup"><span data-stu-id="49cfc-155">Delete cookies</span></span>  

<span data-ttu-id="49cfc-156">Escolha um cookie e escolha **Excluir Selecionado** \( Excluir ![ Selecionado ](../media/delete-icon.msft.png) \) para excluir o cookie específico.</span><span class="sxs-lookup"><span data-stu-id="49cfc-156">Choose a cookie and choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\) to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Excluir um cookie específico" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="49cfc-158">Figura 5: Excluir um cookie específico</span><span class="sxs-lookup"><span data-stu-id="49cfc-158">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="49cfc-159">Escolha **Limpar Tudo** \( Limpar Tudo ![ ](../media/clear-icon.msft.png) \) para excluir todos os cookies.</span><span class="sxs-lookup"><span data-stu-id="49cfc-159">Choose **Clear All** \(![Clear All](../media/clear-icon.msft.png)\) to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Limpar todos os cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="49cfc-161">Figura 6: Limpar todos os cookies</span><span class="sxs-lookup"><span data-stu-id="49cfc-161">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="49cfc-162">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49cfc-162">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abra o Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "Problema Chromium 232693: Implementando o campo de prioridade para cookies | Bugs de cromo"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP - Cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP - Cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP - Escopo de cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP - Cookies Seguros e HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP - Cookies de sessão | MDN"  

> [!NOTE]
> <span data-ttu-id="49cfc-172">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49cfc-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49cfc-173">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="49cfc-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="49cfc-175">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49cfc-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
