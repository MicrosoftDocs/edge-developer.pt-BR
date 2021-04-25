---
description: Como exibir dados de Cache de Aplicativo no painel Aplicativo do Microsoft Edge DevTools.
title: Exibir dados de cache de aplicativos com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: cbe6623aa3132db4d01cd6b440702eb157525eed
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519139"
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

# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a>Exibir dados de cache de aplicativo com o Microsoft Edge DevTools  

> [!WARNING]
> A API de Cache de Aplicativo [está sendo removida da plataforma Web][HTMLStandardOfflineWebApplications].  

Este guia mostra como usar o [Microsoft Edge DevTools][MicrosoftEdgeDevTools] para inspecionar recursos [de Cache de][MDNWebAPIsWindowApplicationCache] Aplicativos.  

## <a name="view-application-cache-data"></a>Exibir dados do Cache do Aplicativo  

1.  Na parte superior do DevTools, escolha a **ferramenta Application.**  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="O painel Manifesto" lightbox="../media/storage-application-manifest.msft.png":::
       O **painel** Manifesto  
    :::image-end:::  

1.  Expanda a **seção Cache** do Aplicativo e escolha um cache para exibir os recursos.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="O painel Cache de Aplicativos" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       O **painel Cache** de Aplicativos  
    :::image-end:::  

Cada linha da tabela representa um recurso em cache.  

A **coluna Tipo** representa a categoria do [recurso][MDNHTMLResourcesInAnApplicationCache].  

| Categoria | Detalhes |  
|:--- |:--- |  
| `Explicit` | Esse recurso foi explicitamente listado no manifesto. |  
| `Fallback` | A URL é um fallback para outro recurso.  A URL do outro recurso não está listada no DevTools. |  
| `Master` | O `manifest` atributo no recurso indica que o cache é o pai do recurso. |  
| `Network` | O manifesto especificou que o recurso deve vir da rede. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

Na parte inferior da tabela, há ícones de status indicando sua conexão de rede e o status do **Cache do Aplicativo.**  O **Cache de Aplicativo** pode ter os seguintes estados.  

| Estado | Detalhes |  
|:--- |:--- |  
| `CHECKING` | O manifesto está sendo buscado e verificado se há atualizações. |  
| `DOWNLOADING` | Recursos estão sendo adicionados ao cache. |  
| `IDLE` | O cache não tem novas alterações. |  
| `OBSOLETE` | O cache está sendo excluído. |  
| `UPDATEREADY` |  Uma nova versão do cache está disponível. |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Aplicativos Web offline - Html Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Recursos em um cache de aplicativo | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache - APIs da Web | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
