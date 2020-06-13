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

# Exibir, editar e Excluir cookies com o Microsoft Edge DevTools  

[Os cookies http][MDNHTTPCookies] são usados principalmente para gerenciar sessões de usuário, armazenar preferências de personalização de usuário e rastrear o comportamento do usuário.  Os cookies também são a causa de todos os formulários de consentimento "Esta página que usa cookies" irritantes exibidos na Web.  O guia a seguir ensina a exibir, editar e excluir os cookies HTTP de uma página com o [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Abrir o painel cookies  

1.  [Abra o devtools][DevToolsOpen].  
1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel de **manifesto** deve ser aberto.  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest-empty.msft.png":::
       Figura 1: o painel manifestar  
    :::image-end:::  

1.  Em **armazenamento** expanda **cookies**, selecione uma origem.  
    
    :::image type="complex" source="../media/storage-application-storage-cookies-selected.msft.png" alt-text="O painel cookies" lightbox="../media/storage-application-storage-cookies-selected.msft.png":::
       Figura 2: o painel cookies  
    :::image-end:::  

## Campos  

A tabela **cookies** contém os campos a seguir.  

*   **Nome**.  O nome do cookie.  
*   **Valor**.  O valor do cookie.  
*   **Domínio**.  Os hosts que têm permissão para receber o cookie.  Consulte [escopo de cookies][MDNHTTPCookiesScope].  
*   **Caminho**.  A URL que deve existir na URL solicitada para enviar o `Cookie` cabeçalho.  Consulte [escopo de cookies][MDNHTTPCookiesScope].  
*   **Vencimento/Max-age**.  A data de expiração ou a idade máxima do cookie.  Ver [cookies permanentes][MDNHTTPCookiesPermanent].  Para [os cookies de sessão][MDNHTTPCookiesSession] , esse valor é sempre `Session` .  
*   **Tamanho**.  O tamanho, em bytes, do cookie.  
*   **Http**.  Se verdadeiro, esse campo indica que o cookie só deve ser usado por HTTP e modificação de JavaScript não é permitido.  Consulte [cookies HttpOnly][MDNHTTPCookiesSecure].  
*   **Seguro**.  Se verdadeiro, este campo indica que o cookie deve ser enviado para o servidor somente por meio de uma conexão HTTPS segura.  Veja [proteger cookies][MDNHTTPCookiesSecure].  
*   **SameSite**.  Contém `strict` ou `lax` se o cookie está usando o atributo experimental [SameSite][MDNHTTPCookiesSamesite] .  
*   **Prioridade**.  Contém `low` , `medium` \ (padrão \) ou `high` se o cookie estiver usando o atributo de [prioridade de cookie][ChromiumIssue232693] preterido.

## Filtrar cookies  

Use a caixa de texto **Filtrar** para filtrar cookies por **nome** ou **valor**.  Não há suporte para filtragem de outros campos.  

:::image type="complex" source="../media/storage-application-storage-cookies-filter-id.msft.png" alt-text="Filtragem de quaisquer cookies que não contenham a ID de texto" lightbox="../media/storage-application-storage-cookies-filter-id.msft.png":::
   Figura 3: filtragem de qualquer cookie que não contenha o texto `ID`  
:::image-end:::  

## Editar um cookie  

Os campos **nome**, **valor**, **domínio**, **caminho**e **vencimento/máx** . da idade são editáveis.  
Clique duas vezes em um campo para editá-lo.  

:::image type="complex" source="../media/storage-application-storage-cookies-rename.msft.png" alt-text="Configurando o nome de um cookie para DEVTOOLS!" lightbox="../media/storage-application-storage-cookies-rename.msft.png":::
   Figura 4: definindo o nome de um cookie como `DEVTOOLS!`  
:::image-end:::  

## Excluir cookies  

Selecione um cookie e escolha **excluir selecionado** ![ excluir selecionado ][ImageDeleteIcon] para excluir o cookie específico.  

:::image type="complex" source="../media/storage-application-storage-cookies-delete-selected.msft.png" alt-text="Excluindo um cookie específico" lightbox="../media/storage-application-storage-cookies-delete-selected.msft.png":::
   Figura 5: excluindo um cookie específico  
:::image-end:::  

Selecione **limpar** tudo ![ limpar tudo ][ImageClearIcon] para excluir todos os cookies.  

:::image type="complex" source="../media/storage-application-storage-cookies-clear-all.msft.png" alt-text="Limpar todos os cookies" lightbox="../media/storage-application-storage-cookies-clear-all.msft.png":::
   Figura 6: limpeza de todos os cookies  
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
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cookies) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
