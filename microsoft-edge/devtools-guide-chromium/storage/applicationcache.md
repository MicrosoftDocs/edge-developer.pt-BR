---
description: Como exibir dados de cache do aplicativo no painel de aplicativos do Microsoft Edge DevTools.
title: Exibir dados de cache do aplicativo com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3d73047a8332e4d6cae5f7411f968a7dfe4c3738
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230779"
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

# Exibir dados de cache do aplicativo com o Microsoft Edge DevTools  

> [!WARNING]
> A API de cache do aplicativo está [sendo removida da plataforma da Web][HTMLStandardOfflineWebApplications].  

Este guia mostra como usar [o Microsoft Edge devtools][MicrosoftEdgeDevTools] para inspecionar os recursos de [cache do aplicativo][MDNWebAPIsWindowApplicationCache] .  

## Exibir dados de cache do aplicativo  

1.  Selecione a guia **fontes** para abrir o painel **fontes** .  O painel de **manifesto** geralmente abre por padrão.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Painel de manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       Painel de **manifesto**  
    :::image-end:::  

1.  Expanda a seção **cache do aplicativo** e escolha um cache para ver os recursos.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Painel de cache do aplicativo" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Painel de **cache do aplicativo**  
    :::image-end:::  

Cada linha da tabela representa um recurso armazenado em cache.  

A coluna **tipo** representa a [categoria do recurso][MDNHTMLResourcesInAnApplicationCache].  

| Categoria | Detalhes |  
|:--- |:--- |  
| `Explicit` | Este recurso foi explicitamente listado no manifesto. |  
| `Fallback` | A URL é um fallback para outro recurso.  A URL do outro recurso não está listada no DevTools. |  
| `Master` | O `manifest` atributo no recurso indica que o cache é o pai do recurso. |  
| `Network` | O manifesto especificou que o recurso deve vir da rede. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

Na parte inferior da tabela há ícones de status que indicam a conexão de rede e o status do **cache do aplicativo**.  O **cache do aplicativo** pode ter os seguintes Estados.  

| Estado | Detalhes |  
|:--- |:--- |  
| `CHECKING` | O manifesto está sendo buscado e verificou se há atualizações. |  
| `DOWNLOADING` | Os recursos estão sendo adicionados ao cache. |  
| `IDLE` | O cache não tem novas alterações. |  
| `OBSOLETE` | O cache está sendo excluído. |  
| `UPDATEREADY` |  Uma nova versão do cache está disponível. |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicativos Web offline-padrão HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos em um cache de aplicativos | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-APIs da Web | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
