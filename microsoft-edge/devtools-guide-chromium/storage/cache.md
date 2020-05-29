---
title: Exibir dados de cache com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612065"
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

Se você estiver tentando inspecionar dados de [cache http][MDNHTTPCaching] , este não é o guia desejado.  
Procure as informações na coluna **tamanho** do **log de rede**.  Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].  

## Exibir dados do cache   

1.  Selecione a guia **aplicativo** para abrir o painel do **aplicativo** .  O painel de **manifesto** geralmente abre por padrão.  
    
    > ##### Figura 1  
    > Painel de manifesto  
    > ![Painel de manifesto][ImageManifestPane]  

1.  Expanda a seção **armazenamento do cache** para ver os caches disponíveis.  
    
    > ##### Figura 2  
    > Caches disponíveis  
    > ![Caches disponíveis][ImageCache]  

1.  Selecione um cache para exibir o conteúdo.  
    
    > ##### Figura 3  
    > Exibir o conteúdo de um cache  
    > ![Exibir o conteúdo de um cache][ImageCacheView]  

1.  Selecione um recurso para exibir os cabeçalhos HTTP na seção abaixo da tabela.  
    
    > ##### Figura 4  
    > Visualizando os cabeçalhos HTTP de um recurso  
    > ![Visualizando os cabeçalhos HTTP de um recurso][ImageViewCacheResource]  

1.  Selecione **Visualizar** para exibir o conteúdo de um recurso.  
    
    > ##### Figura 5  
    > Exibindo o conteúdo de um recurso  
    > ![Exibindo o conteúdo de um recurso][ImageCacheContent]  

## Atualizar um recurso   

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Selecione o recurso que você deseja atualizar.  O DevTools a destaca para indicar que está selecionado.  
    
    > ##### Figura 6  
    > Selecionando um recurso  
    > ![Selecionando um recurso][ImageCacheSelected]  

1.  Selecione **Atualizar** ![ atualização ][ImageRefreshIcon] .  

## Filtrar recursos   

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Use a caixa de texto **Filtrar por caminho** para filtrar os recursos que não correspondem ao caminho fornecido.  
    
    > ##### Figura 7  
    > Filtrar recursos que não correspondem ao caminho especificado  
    > ![Filtrar recursos que não correspondem ao caminho especificado][ImageCacheFilter]  

## Excluir um recurso   

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Selecione o recurso que você deseja excluir.  O DevTools a destaca para indicar que está selecionado.  
    
    > ##### Figura 8  
    > Selecionando um recurso  
    > ![Selecionando um recurso][ImageCacheSelected2]  

1.  Selecione **excluir** selecionado ![ excluir selecionado ][ImageDeleteIcon] .  

## Excluir todos os dados do cache   

1.  Abrir **Application**  >  **armazenamento limpo**do aplicativo.  
1.  Verifique se a caixa de seleção **armazenamento do cache** está habilitada.  
    
    > ##### Figura 9  
    > A caixa de seleção **armazenamento do cache**  
    > ![A caixa de seleção armazenamento do cache][ImageCacheCheckbox]  

1.  Selecione **limpar dados do site**.  
    
    > ##### Figura 10  
    > O botão **limpar dados do site**  
    > ![O botão limpar dados do site][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figura 1: o painel manifestar"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Figura 2: caches disponíveis"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Figura 3: exibindo o conteúdo de um cache"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Figura 4: exibindo os cabeçalhos HTTP de um recurso"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Figura 5: exibindo o conteúdo de um recurso"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Figura 6: selecionando um recurso"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Figura 7: filtrando recursos que não correspondem ao caminho especificado"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Figura 8: selecionando um recurso"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Figura 9: caixa de seleção armazenamento do cache"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Figura 10: o botão limpar dados do site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Registrar atividades de rede"  

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
