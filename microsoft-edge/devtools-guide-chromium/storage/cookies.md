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





# Exibir, editar e Excluir cookies com o Microsoft Edge DevTools   

  

[Os cookies http][MDNHTTPCookies] são usados principalmente para gerenciar sessões de usuário, armazenar preferências de personalização de usuário e rastrear o comportamento do usuário.  Eles também são a causa de todos os formulários de consentimento "Esta página usados por cookies" irritantes exibidos na Web.  Este guia ensina a exibir, editar e excluir os cookies HTTP de uma página com o [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Abrir o painel cookies   

1.  [Abra o devtools][DevToolsOpen].  
1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel de **manifesto** deve ser aberto.  
    
    > ##### Figura 1  
    > Painel de manifesto  
    > ![Painel de manifesto][ImageManifest]  

1.  Em **armazenamento** expanda **cookies**, selecione uma origem.  
    
    > ##### Figura 2  
    > O painel cookies  
    > ![O painel cookies][ImageCookies]  

## Campos   

A tabela **cookies** contém os seguintes campos:  

*   **Nome**.  O nome do cookie.  
*   **Valor**.  O valor do cookie.  
*   **Domínio**.  Os hosts que têm permissão para receber o cookie.  Consulte [escopo de cookies][MDNHTTPCookiesScope].  
*   **Caminho**.  A URL que deve existir na URL solicitada para enviar o `Cookie` cabeçalho.  Consulte [escopo de cookies][MDNHTTPCookiesScope].  
*   **Vencimento/Max-age**.  A data de expiração ou a idade máxima do cookie.  Ver [cookies permanentes][MDNHTTPCookiesPermanent].  Para [os cookies de sessão][MDNHTTPCookiesSession] , esse valor é sempre `Session` .  
*   **Tamanho**.  O tamanho, em bytes, do cookie.  
*   **Http**.  Se verdadeiro, esse campo indica que o cookie só deve ser usado por HTTP e modificação de JavaScript não é permitido.  Consulte [cookies HttpOnly][MDNHTTPCookiesSecure].  
*   **Seguro**.  Se verdadeiro, este campo indica que o cookie deve ser enviado para o servidor somente por meio de uma conexão HTTPS segura.  Veja [proteger cookies][MDNHTTPCookiesSecure].  
*   **SameSite**.  Contém `strict` ou `lax` se o cookie está usando o atributo experimental [SameSite][MDNHTTPCookiesSamesite] .  

## Filtrar cookies   

Use a caixa de texto **Filtrar** para filtrar cookies por **nome** ou **valor**.  Não há suporte para filtragem de outros campos.  

> ##### Figura 3  
> Filtragem de qualquer cookie que não contenha o texto `ID`  
> ![Filtragem de quaisquer cookies que não contenham a ID de texto][ImageCookiesFilter]  

## Editar um cookie   

Os campos **nome**, **valor**, **domínio**, **caminho**e **vencimento/máx** . da idade são editáveis.  
Clique duas vezes em um campo para editá-lo.  

> ##### Figura 4  
> Definindo o nome de um cookie como `DEVTOOLS!`  
> ![Configurando o nome de um cookie para DEVTOOLS!][ImageEditCookie]  

## Excluir cookies   

Selecione um cookie e clique em **Excluir seleção selecionada** ![ selecionada ][ImageDeleteIcon] para excluir um cookie.  

> ##### Figura 5  
> Excluindo um cookie específico  
> ![Excluindo um cookie específico][ImageDeleteCookie]  

Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] para excluir todos os cookies.  

> ##### Figura 6  
> Limpar todos os cookies  
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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
