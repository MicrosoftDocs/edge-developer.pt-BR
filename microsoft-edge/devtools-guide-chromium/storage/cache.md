---
description: Como exibir dados de cache no painel de aplicativos do Microsoft Edge DevTools.
title: Exibir dados de cache com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 5ab5fd0b3b504443e495f1d5108907a4551e6ac6
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125437"
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

# Exibir dados de cache com o Microsoft Edge DevTools  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar dados de [cache][MDNCache] .  

Se você estiver tentando inspecionar dados de [cache http][MDNHTTPCaching] , este não é o guia desejado.  Procure as informações na coluna **tamanho** do **log de rede**.  Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].  

## Exibir dados do cache  

1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel de **manifesto** geralmente abre por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       Painel de **manifesto**  
    :::image-end:::  
    
1.  Expanda a seção **armazenamento do cache** para ver os caches disponíveis.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage.msft.png":::
       Caches disponíveis  
    :::image-end:::  
    
1.  Selecione um cache para exibir o conteúdo.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Exibir o conteúdo de um cache  
    :::image-end:::  
    
1.  Selecione um recurso para exibir os cabeçalhos HTTP na seção abaixo da tabela.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Exibir os cabeçalhos HTTP de um recurso  
    :::image-end:::  
    
1.  Escolha **Visualizar** para exibir o conteúdo de um recurso.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Exibir o conteúdo de um recurso  
    :::image-end:::  
    
## Atualizar um recurso  

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Selecione o recurso que você deseja atualizar.  O DevTools a destaca para indicar que está selecionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Selecionar um recurso para atualizar  
    :::image-end:::  
    
1.  Escolha **Atualizar** \ ( ![ Atualizar ][ImageRefreshIcon] \).  
    
## Filtrar recursos  

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Use a caixa de texto **Filtrar por caminho** para filtrar os recursos que não correspondem ao caminho fornecido.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtrar recursos que não correspondam ao caminho especificado  
    :::image-end:::  
    
## Excluir um recurso  

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Selecione o recurso que você deseja excluir.  O DevTools a destaca para indicar que está selecionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Selecionar um recurso para excluir  
    :::image-end:::  
    
1.  Escolha **excluir selecionado** \ ( ![ excluir selecionado ][ImageDeleteIcon] \).  
    
## Excluir todos os dados do cache  

1.  Abrir **Application**  >  **armazenamento limpo**do aplicativo.  
1.  Verifique se a caixa de seleção **armazenamento do cache** está habilitada.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       A caixa de seleção **armazenamento do cache**  
    :::image-end:::  
    
1.  Escolha **limpar dados do site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       O botão **limpar dados do site**  
    :::image-end:::  
    
## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Registrar atividades da rede | Documentos da Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Cache HTTP | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/cache) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
