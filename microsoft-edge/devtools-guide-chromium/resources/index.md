---
description: Organize recursos por quadro, domínio, tipo ou outros critérios.
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4f90927cc4044c722d9a62ab4b0427aa2753e4c5
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993587"
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





# Exibir recursos de página com o Microsoft Edge DevTools   

  

Este guia ensina a usar o Microsoft Edge DevTools para exibir os recursos de uma página da Web.  Recursos são os arquivos que uma página precisa para serem exibidos corretamente.  Exemplos de recursos incluem CSS, JavaScript e arquivos HTML, bem como imagens.  

Este guia pressupõe que você esteja familiarizado com as noções básicas de [desenvolvimento da Web][MDNLearnWebDevelopment] e do [Microsoft Edge devtools][MicrosoftEdgeDevTools].  

## Recursos abertos   

Quando você sabe o nome do recurso que deseja inspecionar, o menu de **comando** fornece uma maneira rápida de abrir o recurso.  

1.  Pressione `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \).  A caixa de diálogo **Abrir arquivo** será aberta.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="A caixa de diálogo abrir arquivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       A caixa de diálogo **Abrir arquivo**  
    :::image-end:::  
    
1.  Selecione o arquivo na lista suspensa ou comece a digitar o nome do arquivo e pressione `Enter` uma vez que o arquivo correto esteja realçado na caixa preenchimento automático.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Digite um nome de arquivo na caixa de diálogo abrir arquivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Digite um nome de arquivo na caixa de diálogo **Abrir arquivo**  
    :::image-end:::  
    
### Recursos abertos no painel rede   

Consulte [inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecionar um recurso no painel de rede" lightbox="../media/resources-network-response.msft.png":::
   Inspecionar um recurso no painel de **rede**  
:::image-end:::  

### Revelar recursos no painel rede de outros painéis   

A seção [procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do devtools.  Se você quiser inspecionar um recurso no painel de **rede** , clique com o botão direito do mouse no recurso e selecione **revelar no painel de rede**.  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Revelar no painel de rede" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Revelar no painel de rede**  
:::image-end:::  

## Procurar recursos   

### Procurar recursos no painel rede   

Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página no log de rede" lightbox="../media/resources-network-resources.msft.png":::
   Recursos de página no log de **rede**  
:::image-end:::  

### Navegar por diretório   

Para exibir os recursos de uma página organizada por diretório:  

1.  Clique na guia **fontes** para abrir o painel **fontes** .  
1.  Clique na guia **página** para mostrar os recursos da página.  O painel da **página** é aberto.  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Painel de página" lightbox="../media/resources-sources-page-empty.msft.png":::
       Painel de **página**  
    :::image-end:::  
    
    Aqui está um detalhamento dos itens não óbvios na figura anterior.  
    
    | Item de página | Descrição |  
    |:--- |:--- |  
    | `top` | O contexto de [navegação][MDNInlineFrame]do documento principal. |  
    | `airhorner.com` | O domínio.  Todos os recursos aninhados nela vêm desse domínio.  Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Um diretório. |  
    | `(index)` | O documento HTML principal. |  
    | `sw.js` | Um contexto do tempo de execução do trabalho do serviço. |  
    
1.  Clique em um recurso para exibi-lo no **Editor**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Exibir um arquivo no editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       Exibir um arquivo no **Editor**  
    :::image-end:::  
    
### Procurar por nome de arquivo   

Por padrão, o painel de **página** agrupa os recursos por diretório.  Para desabilitar esse agrupamento e exibir os recursos de cada domínio como uma lista plana:  

1.  Abrir o painel da **página** .  Consulte [procurar por diretório](#browse-by-directory).  
1.  Clique em **mais opções** `...` e desabilite **Agrupar por pasta**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="A opção Agrupar por pasta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       A opção **Agrupar por pasta**  
    :::image-end:::  
    
    Os recursos são organizados por tipo de arquivo.  Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="O painel da página depois de desabilitar agrupar por pasta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       O painel da **página** depois de desabilitar **Agrupar por pasta**  
    :::image-end:::  
    
### Procurar por tipo de arquivo   

Para agrupar recursos juntamente com base no tipo de arquivo:  

1.  Clique na guia **aplicativo** .  O painel **aplicativo** é aberto.  Por padrão, o painel de **manifesto** geralmente abre primeiro.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Painel de aplicativos" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       Painel de **aplicativos**  
    :::image-end:::  
    
1.  Role para baixo até o painel **quadros** .  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="O painel quadros" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       O painel **quadros**  
    :::image-end:::  
    
1.  Expanda as seções em que você está interessado.  
1.  Clique em um recurso para exibi-lo.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Exibir um recurso no painel do aplicativo" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Exibir um recurso no painel do **aplicativo**  
    :::image-end:::  
    
#### Procurar arquivos por tipo no painel rede   

Consulte [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtro para CSS no log de rede" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtro para CSS no log de **rede**  
:::image-end:::  

<!--  
  


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso-inspecionar atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecionar os detalhes da atividade de rede de inspeção de recursos no Microsoft Edge DevTools | Documentos da Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools | Documentos da Microsoft"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "> de<iframe: o elemento frame embutido | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprender sobre desenvolvimento na Web | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/resources/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
