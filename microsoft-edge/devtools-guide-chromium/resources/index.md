---
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611914"
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
    
    > ##### Figura 1  
    > A caixa de diálogo **Abrir arquivo**  
    > ![A caixa de diálogo abrir arquivo][ImageOpenFile]  
    
1.  Selecione o arquivo na lista suspensa ou comece a digitar o nome do arquivo e pressione `Enter` uma vez que o arquivo correto esteja realçado na caixa preenchimento automático.  
    
    > ##### Figura 2  
    > Digitando um nome de arquivo na caixa de diálogo **Abrir arquivo**  
    > ![Digitando um nome de arquivo na caixa de diálogo abrir arquivo][ImageFileSearch]  
    
### Recursos abertos no painel rede   

Consulte [inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].  

> ##### Figura 3  
> Inspecionar um recurso no painel de rede  
> ![Inspecionar um recurso no painel de rede][ImageNetworkResponse]  

### Revelar recursos no painel rede de outros painéis   

A seção [procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do devtools.  Se você quiser inspecionar um recurso no painel de **rede** , clique com o botão direito do mouse no recurso e selecione **revelar no painel de rede**.  

> ##### Figura 4  
> A opção **revelar no painel de rede**  
> ![Revelar no painel de rede][ImageRevealNetwork]  

## Procurar recursos   

### Procurar recursos no painel rede   

Consulte [log de atividades de rede][DevtoolsNetworkLogActivity].  

> ##### Figura 5  
> Recursos de página no log de rede  
> ![Recursos de página no log de rede][ImageNetworkLog]  

### Navegar por diretório   

Para exibir os recursos de uma página organizada por diretório:  

1.  Clique na guia **fontes** para abrir o painel **fontes** .  
1.  Clique na guia **página** para mostrar os recursos da página.  O painel da **página** é aberto.  
    
    > ##### Figura 6  
    > Painel de **página**  
    > ![Painel de página][ImagePage]  
    
    Aqui está um detalhamento dos itens não óbvios na [Figura 6](#figure-6):  
    
    | Item de página | Descrição |  
    |:--- |:--- |  
    | `top` | O contexto de [navegação][MDNInlineFrame]do documento principal. |  
    | `airhorner.com` | O domínio.  Todos os recursos aninhados nela vêm desse domínio.  Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Um diretório. |  
    | `(index)` | O documento HTML principal. |  
    | `sw.js` | Um contexto do tempo de execução do trabalho do serviço. |  
    
1.  Clique em um recurso para exibi-lo no **Editor**.  
    
    > ##### Figura 7  
    > Exibir um arquivo no **Editor**  
    > ![Exibir um arquivo no editor][ImageSourcesView]  
    
### Procurar por nome de arquivo   

Por padrão, o painel de **página** agrupa os recursos por diretório.  Para desabilitar esse agrupamento e exibir os recursos de cada domínio como uma lista plana:  

1.  Abrir o painel da **página** .  Consulte [procurar por diretório](#browse-by-directory).  
1.  Clique em **mais opções** `...` e desabilite **Agrupar por pasta**.  
    
    > ##### Figura 8  
    > A opção **Agrupar por pasta**  
    > ![A opção Agrupar por pasta][ImageGroupByFolder]  
    
    Os recursos são organizados por tipo de arquivo.  Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.  
    
    > ##### Figura 9  
    > O painel da **página** depois de desabilitar **Agrupar por pasta**  
    > ![O painel da página depois de desabilitar agrupar por pasta][ImageFileNames]  
    
### Procurar por tipo de arquivo   

Para agrupar recursos juntamente com base no tipo de arquivo:  

1.  Clique na guia **aplicativo** .  O painel **aplicativo** é aberto.  Por padrão, o painel de **manifesto** geralmente abre primeiro.  
    
    > ##### Figura 10  
    > Painel de **aplicativos**  
    > ![Painel de aplicativos][ImageApplication]  
    
1.  Role para baixo até o painel **quadros** .  
    
    > ##### Figura 11  
    > O painel **quadros**  
    > ![O painel quadros][ImageFrames]  
    
1.  Expanda as seções em que você está interessado.  
1.  Clique em um recurso para exibi-lo.  
    
    > ##### Figura 12  
    > Exibindo um recurso no painel do **aplicativo**  
    > ![Exibindo um recurso no painel do aplicativo][ImageApplicationView]  

#### Procurar arquivos por tipo no painel rede   

Consulte [Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].  

> ##### Figura 13  
> Filtragem de CSS no log de rede  
> ![Filtragem de CSS no log de rede][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Figura 1: caixa de diálogo abrir arquivo"  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Figura 2: digitando um nome de arquivo na caixa de diálogo abrir arquivo"  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Figura 3: inspecionando um recurso no painel * * Network * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Figura 4: revelar no painel de rede"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Figura 5: recursos de página no log de rede"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Figura 6: o painel da página"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Figura 7: exibindo um arquivo no editor"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Figura 8: a opção Agrupar por pasta"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Figura 9: painel da página depois de desabilitar agrupar por pasta"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Figura 10: o painel do aplicativo"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Figura 11: o painel quadros"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Figura 12: exibindo um recurso no painel do aplicativo"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Figura 13: filtragem para CSS no log de rede"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Filtrar por tipo de recurso-inspecionar atividade de rede no Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspecionar os detalhes da atividade de rede de inspeção de recursos no Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar atividades de rede-Inspecione a atividade de rede no Microsoft Edge DevTools"  

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
