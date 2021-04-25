---
description: Organize recursos por quadro, domínio, tipo ou outros critérios.
title: Exibir recursos de página com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 818b93c1c07a93baa8972a530871d20446fd687f
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519440"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a>Exibir recursos de página com o Microsoft Edge DevTools  

Este guia ensina como usar o Microsoft Edge DevTools para exibir os recursos de uma página da Web.  Recursos são os arquivos que uma página precisa para exibir corretamente.  Exemplos de recursos incluem arquivos CSS, JavaScript e HTML, bem como imagens.  

Este guia supõe que você está familiarizado com os conceitos básicos de [desenvolvimento da Web][MDNLearnWebDevelopment] e Microsoft Edge [DevTools.][MicrosoftEdgeDevTools]  

## <a name="open-resources"></a>Abrir recursos  

Quando você sabe o nome do recurso que deseja inspecionar, o **Menu de Comando** fornece uma maneira rápida de abrir o recurso.  

1.  Selecione `Control` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\).  A **caixa de diálogo** Abrir Arquivo é aberta.  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="A caixa de diálogo Abrir Arquivo" lightbox="../media/resources-command-menu-empty.msft.png":::
       A **caixa de diálogo Abrir Arquivo**  
    :::image-end:::  
    
1.  Escolha o arquivo no menu suspenso ou comece a digitar o nome do arquivo e selecione quando o arquivo correto for realçado na caixa de preenchimento `Enter` automático.  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Digite um nome de arquivo na caixa de diálogo Abrir Arquivo" lightbox="../media/resources-command-menu-file-search.msft.png":::
       Digite um nome de arquivo na caixa **de diálogo Abrir Arquivo**  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a>Abrir recursos na ferramenta Rede  

Navegue [até Inspecionar os detalhes de um recurso][DevtoolsNetworkInspectDetailsResource].  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Inspecionar um recurso na ferramenta Rede" lightbox="../media/resources-network-response.msft.png":::
   Inspecionar um recurso na **ferramenta Rede**  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a>Revelar recursos na ferramenta Rede de outros painéis  

A [seção Procurar recursos](#browse-resources) abaixo mostra como exibir recursos de várias partes da interface do usuário do DevTools.  Se você quiser inspecionar um **** recurso na ferramenta Rede, passe o mouse no recurso, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Revelar no painel Rede.**  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Revelação no painel Rede" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **Revelação no painel Rede**  
:::image-end:::  

## <a name="browse-resources"></a>Procurar recursos  

### <a name="browse-resources-in-the-network-panel"></a>Procurar recursos no painel Rede  

Navegue até [Log network activity][DevtoolsNetworkLogActivity].  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Recursos de página no Log de Rede" lightbox="../media/resources-network-resources.msft.png":::
   Recursos de página no Log **de** Rede  
:::image-end:::  

### <a name="browse-by-directory"></a>Procurar por diretório  

Para exibir os recursos de uma página da Web organizada pelo diretório:  

1.  Abra DevTools.
1.  Escolha a **ferramenta Fontes** e, no painel **Navegador,** no canto superior esquerdo, escolha a **guia** Página.
1.  Escolha o **botão Mais opções** (...) à direita da guia **Página** e escolha Grupo **por pasta**.
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="A guia Página no painel Navegador da ferramenta Sources" lightbox="../media/resources-sources-page-empty.msft.png":::
       A **guia Página** no painel **Navegador** da ferramenta **Sources**  
    :::image-end:::  
    
    Aqui está uma divisão dos itens não óbvios na figura anterior.  
    
    | Item de página | Descrição |  
    |:--- |:--- |  
    | `top` | O contexto principal [de navegação do documento.][MDNInlineFrame] |  
    | `airhorner.com` | O domínio.  Todos os recursos aninhados sob ele vêm desse domínio.  Por exemplo, a URL completa do `comlink.global.j` arquivo é provavelmente `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Um diretório. |  
    | `(index)` | O documento HTML principal. |  
    | `sw.js` | Um contexto de tempo de execução do trabalhador de serviço. |  
    
1.  Escolha um recurso para exibi-lo no **Editor**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Exibir um arquivo no Editor" lightbox="../media/resources-sources-page-resource.msft.png":::
       Exibir um arquivo no **Editor**  
    :::image-end:::  
    
### <a name="browse-by-filename"></a>Procurar por nome de arquivo  

Por padrão, a guia **Página** grupos recursos por diretório.  Para exibir os recursos de cada domínio como uma lista simples, em vez de a agrupar por diretório:

1.  Navegue até a **ferramenta Sources.**  
1.  No painel **Navegador** (à esquerda), escolha a **guia** Página.  
1.  Escolha **Mais opções** e `...` desmarca a marca de seleção ao lado de **Grupo por pasta**.  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="A opção Grupo por pasta" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       A **opção Grupo por** pasta  
    :::image-end:::  
    
    Os recursos são organizados por tipo de arquivo.  Em cada tipo de arquivo, os recursos são organizados em ordem alfabética.  

    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="A guia Página após limpar a marca de seleção Grupo por pasta" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       A **guia Página** após limpar a marca de seleção Grupo **por** pasta  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a>Procurar por tipo de arquivo  

Para agrupar recursos com base no tipo de arquivo:  

1.  Escolha a **guia Aplicativo.**  A **ferramenta Application** é aberta.  Por padrão, **o** painel Manifesto geralmente é aberto primeiro.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="A ferramenta Application" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       A **ferramenta Application**  
    :::image-end:::  
    
1.  Role para baixo até o painel **Quadros.**  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="O painel Quadros" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       O **painel Quadros**  
    :::image-end:::  
    
1.  Expanda as seções nas quais você está interessado.  
1.  Escolha um recurso para exibi-lo.  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Exibir um recurso no painel Aplicativo" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       Exibir um recurso no painel **Aplicativo**  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a>Procurar arquivos por tipo no painel Rede  

Navegue [até Filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Filtrar para CSS no Log de Rede" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   Filtrar para CSS no **Log de** Rede  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Filtrar por tipo de recurso - Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Inspecionar os detalhes do recurso - Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Atividade de rede de log - Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: o elemento Frame em linha | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Saiba mais sobre desenvolvimento da Web | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/resources/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
