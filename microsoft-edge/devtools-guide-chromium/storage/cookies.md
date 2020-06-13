---
title: Exibir, editar e Excluir cookies com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: ecd8df7058bca4535d1f7da15ce1d500ef85aefe
ms.sourcegitcommit: a34858dd3260967ba9699842fa839c7a94775fe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/12/2020
ms.locfileid: "10710368"
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

# <span data-ttu-id="93435-103">Exibir, editar e Excluir cookies com o Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="93435-103">View, edit, and delete cookies with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="93435-104">[Os cookies http][MDNHTTPCookies] são usados principalmente para gerenciar sessões de usuário, armazenar preferências de personalização de usuário e rastrear o comportamento do usuário.</span><span class="sxs-lookup"><span data-stu-id="93435-104">[HTTP Cookies][MDNHTTPCookies] are mainly used to manage user sessions, store user personalization preferences, and track user behavior.</span></span>  <span data-ttu-id="93435-105">Os cookies também são a causa de todos os formulários de consentimento "Esta página que usa cookies" irritantes exibidos na Web.</span><span class="sxs-lookup"><span data-stu-id="93435-105">Cookies are also the cause of all of the annoying "this page uses cookies" consent forms that you see across the web.</span></span>  <span data-ttu-id="93435-106">O guia a seguir ensina a exibir, editar e excluir os cookies HTTP de uma página com o [Microsoft Edge devtools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="93435-106">The following guide teaches you how to view, edit, and delete the HTTP cookies for a page with [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="93435-107">Abrir o painel cookies</span><span class="sxs-lookup"><span data-stu-id="93435-107">Open the Cookies pane</span></span>  

1.  <span data-ttu-id="93435-108">[Abra o devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="93435-108">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="93435-109">Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="93435-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="93435-110">O painel de **manifesto** deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="93435-110">The **Manifest** pane should open.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="93435-112">Figura 1: o painel manifestar</span><span class="sxs-lookup"><span data-stu-id="93435-112">Figure 1:  The Manifest pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="93435-113">Em **armazenamento** expanda **cookies**, selecione uma origem.</span><span class="sxs-lookup"><span data-stu-id="93435-113">Under **Storage** expand **Cookies**, then select an origin.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="O painel cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       <span data-ttu-id="93435-115">Figura 2: o painel cookies</span><span class="sxs-lookup"><span data-stu-id="93435-115">Figure 2:  The Cookies pane</span></span>  
    :::image-end:::  

## <span data-ttu-id="93435-116">Campos</span><span class="sxs-lookup"><span data-stu-id="93435-116">Fields</span></span>  

<span data-ttu-id="93435-117">A tabela **cookies** contém os campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="93435-117">The **Cookies** table contains the following fields.</span></span>  

*   <span data-ttu-id="93435-118">**Nome**.</span><span class="sxs-lookup"><span data-stu-id="93435-118">**Name**.</span></span>  <span data-ttu-id="93435-119">O nome do cookie.</span><span class="sxs-lookup"><span data-stu-id="93435-119">The name of the cookie.</span></span>  
*   <span data-ttu-id="93435-120">**Valor**.</span><span class="sxs-lookup"><span data-stu-id="93435-120">**Value**.</span></span>  <span data-ttu-id="93435-121">O valor do cookie.</span><span class="sxs-lookup"><span data-stu-id="93435-121">The value of the cookie.</span></span>  
*   <span data-ttu-id="93435-122">**Domínio**.</span><span class="sxs-lookup"><span data-stu-id="93435-122">**Domain**.</span></span>  <span data-ttu-id="93435-123">Os hosts que têm permissão para receber o cookie.</span><span class="sxs-lookup"><span data-stu-id="93435-123">The hosts that are allowed to receive the cookie.</span></span>  <span data-ttu-id="93435-124">Consulte [escopo de cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="93435-124">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="93435-125">**Caminho**.</span><span class="sxs-lookup"><span data-stu-id="93435-125">**Path**.</span></span>  <span data-ttu-id="93435-126">A URL que deve existir na URL solicitada para enviar o `Cookie` cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="93435-126">The URL that must exist in the requested URL in order to send the `Cookie` header.</span></span>  <span data-ttu-id="93435-127">Consulte [escopo de cookies][MDNHTTPCookiesScope].</span><span class="sxs-lookup"><span data-stu-id="93435-127">See [Scope of cookies][MDNHTTPCookiesScope].</span></span>  
*   <span data-ttu-id="93435-128">**Vencimento/Max-age**.</span><span class="sxs-lookup"><span data-stu-id="93435-128">**Expires / Max-Age**.</span></span>  <span data-ttu-id="93435-129">A data de expiração ou a idade máxima do cookie.</span><span class="sxs-lookup"><span data-stu-id="93435-129">The expiration date or maximum age of the cookie.</span></span>  <span data-ttu-id="93435-130">Ver [cookies permanentes][MDNHTTPCookiesPermanent].</span><span class="sxs-lookup"><span data-stu-id="93435-130">See [Permanent cookies][MDNHTTPCookiesPermanent].</span></span>  <span data-ttu-id="93435-131">Para [os cookies de sessão][MDNHTTPCookiesSession] , esse valor é sempre `Session` .</span><span class="sxs-lookup"><span data-stu-id="93435-131">For [session cookies][MDNHTTPCookiesSession] this value is always `Session`.</span></span>  
*   <span data-ttu-id="93435-132">**Tamanho**.</span><span class="sxs-lookup"><span data-stu-id="93435-132">**Size**.</span></span>  <span data-ttu-id="93435-133">O tamanho, em bytes, do cookie.</span><span class="sxs-lookup"><span data-stu-id="93435-133">The size, in bytes, of the cookie.</span></span>  
*   <span data-ttu-id="93435-134">**Http**.</span><span class="sxs-lookup"><span data-stu-id="93435-134">**HTTP**.</span></span>  <span data-ttu-id="93435-135">Se verdadeiro, esse campo indica que o cookie só deve ser usado por HTTP e modificação de JavaScript não é permitido.</span><span class="sxs-lookup"><span data-stu-id="93435-135">If true, this field indicates that the cookie should only be used over HTTP and JavaScript modification is not allowed.</span></span>  <span data-ttu-id="93435-136">Consulte [cookies HttpOnly][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="93435-136">See [HttpOnly cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="93435-137">**Seguro**.</span><span class="sxs-lookup"><span data-stu-id="93435-137">**Secure**.</span></span>  <span data-ttu-id="93435-138">Se verdadeiro, este campo indica que o cookie deve ser enviado para o servidor somente por meio de uma conexão HTTPS segura.</span><span class="sxs-lookup"><span data-stu-id="93435-138">If true, this field indicates that the cookie must be sent to the server only over a secure, HTTPS connection.</span></span>  <span data-ttu-id="93435-139">Veja [proteger cookies][MDNHTTPCookiesSecure].</span><span class="sxs-lookup"><span data-stu-id="93435-139">See [Secure cookies][MDNHTTPCookiesSecure].</span></span>  
*   <span data-ttu-id="93435-140">**SameSite**.</span><span class="sxs-lookup"><span data-stu-id="93435-140">**SameSite**.</span></span>  <span data-ttu-id="93435-141">Contém `strict` ou `lax` se o cookie está usando o atributo experimental [SameSite][MDNHTTPCookiesSamesite] .</span><span class="sxs-lookup"><span data-stu-id="93435-141">Contains `strict` or `lax` if the cookie is using the experimental [Samesite][MDNHTTPCookiesSamesite] attribute.</span></span>  
*   <span data-ttu-id="93435-142">**Prioridade**.</span><span class="sxs-lookup"><span data-stu-id="93435-142">**Priority**.</span></span>  <span data-ttu-id="93435-143">Contém `low` , `medium` \ (padrão \) ou `high` se o cookie estiver usando o atributo de [prioridade de cookie][ChromiumIssue232693] preterido.</span><span class="sxs-lookup"><span data-stu-id="93435-143">Contains `low`, `medium` \(default\), or `high` if the cookie is using the deprecated [cookie Priority][ChromiumIssue232693] attribute.</span></span>

## <span data-ttu-id="93435-144">Filtrar cookies</span><span class="sxs-lookup"><span data-stu-id="93435-144">Filter cookies</span></span>  

<span data-ttu-id="93435-145">Use a caixa de texto **Filtrar** para filtrar cookies por **nome** ou **valor**.</span><span class="sxs-lookup"><span data-stu-id="93435-145">Use the **Filter** text box to filter cookies by **Name** or **Value**.</span></span>  <span data-ttu-id="93435-146">Não há suporte para filtragem de outros campos.</span><span class="sxs-lookup"><span data-stu-id="93435-146">Filtering by other fields is not supported.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtragem de quaisquer cookies que não contenham a ID de texto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   <span data-ttu-id="93435-148">Figura 3: filtragem de qualquer cookie que não contenha o texto</span><span class="sxs-lookup"><span data-stu-id="93435-148">Figure 3:  Filtering out any cookies that do not contain the text</span></span> `ID`  
:::image-end:::  

## <span data-ttu-id="93435-149">Editar um cookie</span><span class="sxs-lookup"><span data-stu-id="93435-149">Edit a cookie</span></span>  

<span data-ttu-id="93435-150">Os campos **nome**, **valor**, **domínio**, **caminho**e **vencimento/máx** . da idade são editáveis.</span><span class="sxs-lookup"><span data-stu-id="93435-150">The **Name**, **Value**, **Domain**, **Path**, and **Expires / Max-Age** fields are editable.</span></span>  
<span data-ttu-id="93435-151">Clique duas vezes em um campo para editá-lo.</span><span class="sxs-lookup"><span data-stu-id="93435-151">Double-click a field to edit it.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Configurando o nome de um cookie para DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   <span data-ttu-id="93435-153">Figura 4: definindo o nome de um cookie como</span><span class="sxs-lookup"><span data-stu-id="93435-153">Figure 4:  Setting the name of a cookie to</span></span> `DEVTOOLS!`  
:::image-end:::  

## <span data-ttu-id="93435-154">Excluir cookies</span><span class="sxs-lookup"><span data-stu-id="93435-154">Delete cookies</span></span>  

<span data-ttu-id="93435-155">Selecione um cookie e escolha **excluir selecionado** ![ excluir selecionado ][ImageDeleteIcon] para excluir o cookie específico.</span><span class="sxs-lookup"><span data-stu-id="93435-155">Select a cookie and select **Delete Selected** ![Delete Selected][ImageDeleteIcon]  to delete the specific cookie.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Excluindo um cookie específico" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   <span data-ttu-id="93435-157">Figura 5: excluindo um cookie específico</span><span class="sxs-lookup"><span data-stu-id="93435-157">Figure 5:  Deleting a specific cookie</span></span>  
:::image-end:::  

<span data-ttu-id="93435-158">Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] para excluir todos os cookies.</span><span class="sxs-lookup"><span data-stu-id="93435-158">Select **Clear All** ![Clear All][ImageClearIcon]  to delete all cookies.</span></span>  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Limpar todos os cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   <span data-ttu-id="93435-160">Figura 6: limpeza de todos os cookies</span><span class="sxs-lookup"><span data-stu-id="93435-160">Figure 6:  Clearing all cookies</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  

[ChromiumIssue232693]: https://bugs.chromium.org/p/chromium/issues/detail?id=232693 "232693 problema do Chromium: implementando campo de prioridade para cookies | Erros de Chromium"  

[MDNHTTPCookies]: https://developer.mozilla.org/docs/Web/HTTP/Cookies "Cookies HTTP | MDN"  
[MDNHTTPCookiesPermanent]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Permanent_cookies "Cookies HTTP-cookies permanentes | MDN"  
[MDNHTTPCookiesSamesite]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#SameSite_cookies "Cookies HTTP-cookies SameSite | MDN"  
[MDNHTTPCookiesScope]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Scope_of_cookies "Cookies HTTP-escopo de cookies | MDN"  
[MDNHTTPCookiesSecure]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Secure_and_HttpOnly_cookies "Cookies HTTP-cookies seguros e HttpOnly | MDN"  
[MDNHTTPCookiesSession]: https://developer.mozilla.org/docs/Web/HTTP/Cookies#Session_cookies "Cookies HTTP-cookies de sessão | MDN"  

> [!NOTE]
> <span data-ttu-id="93435-170">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="93435-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="93435-171">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="93435-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="93435-173">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="93435-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
