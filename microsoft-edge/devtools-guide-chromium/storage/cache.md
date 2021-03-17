---
description: Como exibir dados de cache do painel Aplicativo do Microsoft Edge DevTools.
title: Exibir dados de cache com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 0ce4dbbf2456579abe84fca48bca8106384995dd
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439314"
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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a>Exibir dados de cache com o Microsoft Edge DevTools  

Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspecionar [dados de cache.][MDNCache]  

Se você estiver tentando inspecionar dados [de cache HTTP,][MDNHTTPCaching] esse não é o guia que você deseja.  Procure as informações na coluna **Tamanho** do **Log de Rede.**  Navegue até [Log network activity][DevtoolsNetworkLogActivity].  

## <a name="view-cache-data"></a>Exibir dados de cache  

1.  Escolha a **guia Aplicativo** para abrir o **painel Aplicativo.**  O **painel** Manifesto geralmente é aberto por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       O **painel** Manifesto  
    :::image-end:::  
    
1.  Expanda a **seção Armazenamento de Cache** para exibir caches disponíveis.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponíveis" lightbox="../media/storage-application-cache-storage.msft.png":::
       Caches disponíveis  
    :::image-end:::  
    
1.  Escolha um cache para exibir o conteúdo.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Exibir o conteúdo de um cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Exibir o conteúdo de um cache  
    :::image-end:::  
    
1.  Escolha um recurso para exibir os cabeçalhos HTTP na seção abaixo da tabela.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Exibir os cabeçalhos HTTP de um recurso" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Exibir os cabeçalhos HTTP de um recurso  
    :::image-end:::  
    
1.  Escolha **Visualizar** para exibir o conteúdo de um recurso.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Exibir o conteúdo de um recurso" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Exibir o conteúdo de um recurso  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a>Atualizar um recurso  

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Escolha o recurso que você deseja atualizar.  O DevTools realça-o para indicar que ele está selecionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Escolher um recurso para atualizar" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Escolher um recurso para atualizar  
    :::image-end:::  
    
1.  Escolha **Atualizar** \( ![ Atualizar ](../media/refresh-icon.msft.png) \).  
    
## <a name="filter-resources"></a>Filtrar recursos  

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Use a **caixa de texto Filtrar** por Caminho para filtrar todos os recursos que não corresponderem ao caminho que você fornece.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrar recursos que não corresponderem ao caminho especificado" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtrar recursos que não corresponderem ao caminho especificado  
    :::image-end:::  
    
## <a name="delete-a-resource"></a>Excluir um recurso  

1.  [Exibir os dados de um cache](#view-cache-data).  
1.  Escolha o recurso que você deseja excluir.  O DevTools realça-o para indicar que ele está selecionado.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Escolher um recurso a ser excluído" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Escolher um recurso a ser excluído  
    :::image-end:::  
    
1.  Escolha **Excluir Selecionado** \( Excluir Selecionado ![ ](../media/delete-icon.msft.png) \).  
    
## <a name="delete-all-cache-data"></a>Excluir todos os dados de cache  

1.  Abra **o Armazenamento**Limpo do  >  **Aplicativo**.  
1.  Verifique se a caixa de **seleção Armazenamento de Cache** está habilitada.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="A caixa de seleção Armazenamento de Cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       A **caixa de seleção Armazenamento de** Cache  
    :::image-end:::  
    
1.  Escolha **Limpar dados do site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="O botão Limpar Dados do Site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       O **botão Limpar Dados do Site**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Log network activity | Microsoft Docs"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Armazenamento em cache HTTP | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/cache) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
