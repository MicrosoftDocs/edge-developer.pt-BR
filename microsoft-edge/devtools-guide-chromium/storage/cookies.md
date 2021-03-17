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

# <a name="view-edit-and-delete-cookies-with-microsoft-edge-devtools"></a>Exibir, editar e excluir cookies com o Microsoft Edge DevTools  

[Cookies HTTP][MDNHTTPCookies] são usados principalmente para gerenciar sessões de usuário, armazenar preferências de personalização do usuário e acompanhar o comportamento do usuário.  Cookies também são a causa de todos os irritantes que **essa página usa** os formulários de consentimento de cookies encontrados na Web.  O guia a seguir ensina como exibir, editar e excluir os cookies HTTP de uma página da Web com [o Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## <a name="open-the-cookies-pane"></a>Abra o painel Cookies  

1.  [Abra DevTools][DevToolsOpen].  
1.  Escolha a **guia Aplicativo** para abrir o **painel Aplicativo.**  O **painel Manifesto** deve abrir.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Figura 1: o painel Manifesto  
    :::image-end:::  

1.  Em **Armazenamento** **expanda Cookies,** selecione uma origem.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="O painel Cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Figura 2: o painel Cookies  
    :::image-end:::  

## <a name="fields"></a>Campos  

A **tabela Cookies** contém os campos a seguir.  

*   **Nome**.  O nome do cookie.  
*   **Valor**.  O valor do cookie.  
*   **Domínio**.  Os hosts que têm permissão para receber o cookie.  Navegue [até Escopo de cookies.][MDNHTTPCookiesScope]  
*   **Caminho**.  A URL que deve existir na URL solicitada para enviar `Cookie` o header.  Navegue [até Escopo de cookies.][MDNHTTPCookiesScope]  
*   **Expira / Max-Age**.  A data de expiração ou a idade máxima do cookie.  Navegue até [Cookies permanentes][MDNHTTPCookiesPermanent].  Para [cookies de sessão,][MDNHTTPCookiesSession] esse valor é sempre `Session` .  
*   **Tamanho**.  O tamanho, em bytes, do cookie.  
*   **HTTP**.  Se for true, este campo indica que o cookie só deve ser usado em HTTP e a modificação do JavaScript não é permitida.  Navegue [até Cookies HttpOnly.][MDNHTTPCookiesSecure]  
*   **Proteger**.  Se for true, esse campo indica que o cookie deve ser enviado para o servidor somente por meio de uma conexão HTTPS segura.  Navegue até [Cookies seguros.][MDNHTTPCookiesSecure]  
*   **SameSite**.  Contém `strict` ou se o cookie está usando o atributo Experimental `lax` [Samesite.][MDNHTTPCookiesSamesite]  
*   **Prioridade**.  Contém `low` , `medium` \(default\) ou se o cookie está usando o atributo de Prioridade de `high` [cookie][ChromiumIssue232693] preterido.

## <a name="filter-cookies"></a>Cookies de filtro  

Use a **caixa de texto** Filtro para filtrar cookies por **Nome** ou **Valor**.  Não há suporte para filtragem por outros campos.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtrando cookies que não contenham a ID de texto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Figura 3: Filtrando todos os cookies que não contenham o texto `ID`  
:::image-end:::  

## <a name="edit-a-cookie"></a>Editar um cookie  

Os **campos Nome**, **Valor,** **Domínio**, **Caminho**e Expira **/ Max-Age** são editáveis.  
Clique duas vezes em um campo para editá-lo.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Definindo o nome de um cookie como DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Figura 4: Definindo o nome de um cookie como `DEVTOOLS!`  
:::image-end:::  

## <a name="delete-cookies"></a>Excluir cookies  

Escolha um cookie e escolha **Excluir Selecionado** \( Excluir ![ Selecionado ](../media/delete-icon.msft.png) \) para excluir o cookie específico.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Excluir um cookie específico" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Figura 5: Excluir um cookie específico  
:::image-end:::  

Escolha **Limpar Tudo** \( Limpar Tudo ![ ](../media/clear-icon.msft.png) \) para excluir todos os cookies.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Limpar todos os cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Figura 6: Limpar todos os cookies  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

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
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
