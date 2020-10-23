---
description: Saiba como usar o Microsoft Edge DevTools para exibir e alterar a CSS de uma página CSS.
title: Inspecionar a grade CSS no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 150aea57aa676580b554cc74292671ed567a0a2c
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133917"
---
# Inspecionar grade CSS  

Este artigo orienta você na identificação de grades CSS em um site e na depuração de problemas de layout de grade usando sobreposições de grade personalizáveis.  

Os exemplos usados nos números deste artigo são retirados das páginas da Web a seguir.  

*   [Caixa de frutas][JecFyiDemoCssGridFruit]  
*   [Caixa de lanche][JecFyiDemoCssGridSnack]  

## Antes de começar  

A grade CSS é um poderoso paradigma de layout para a Web.  Um ótimo lugar para começar a aprender sobre a grade CSS e os muitos recursos é o [Guia de layout de grade CSS][MdnCssGridLayout] em MDN.  

## Descobrir grades CSS  

Quando um elemento HTML na sua página tiver `display: grid` ou `display: inline-grid` aplicado a ele, um `grid` emblema será exibido ao lado dele no painel de [elementos][DevtoolsGuideChromiumOpen] .  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-discover-grid.msft.png":::
   Descobrir grade  
:::image-end:::  

Selecione o selo para alternar a exibição de uma sobreposição de grade na página.  A sobreposição aparece sobre o elemento, disposta como uma grade para exibir a posição das linhas de grade e as faixas:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-highlight-grid.msft.png":::
   Alternar o selo da grade  
:::image-end:::  

Abrir o painel de **layout** .  Quando as grades são incluídas em uma página, o painel de **layout** inclui uma seção de **grade** contendo várias opções para exibir as grades.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-layout-pane.msft.png":::
   Painel de **layout**  
:::image-end:::  

A seção **grade** no painel **layout** contém as 2 subseções a seguir.  

*   Configurações de exibição de sobreposição  
*   Sobreposições de grade  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## Configurações de exibição de sobreposição  

As **configurações de exibição de sobreposição** consistem nas duas partes a seguir.  

*   Escolha uma das opções a seguir no menu suspenso.  
    
    | Opção de linha | Detalhes |  
    |:--- |:--- |  
    | **Ocultar rótulos de linha** | Ocultar os rótulos das linhas para cada sobreposição de grade. |  
    | **Mostrar números de linha** | Exiba os números das linhas para cada sobreposição de grade \ (selecionada por padrão \). |  
    | **Mostrar nomes de linha** | Exiba os nomes das linhas para cada sobreposição de grade quando os nomes forem fornecidos. |  
    
*  Selecione a caixa de seleção ao lado das opções a seguir.  
    
    | Opção | Detalhes |  
    |:--- |:--- |  
    | **Mostrar tamanhos de faixas**  | Exibir \ (ou ocultar \) os tamanhos das faixas. |  
    | **Mostrar nomes de área** | Exiba \ (ou oculte \) os nomes da área, quando os nomes são fornecidos. |  
    | **Estender linhas de grade** | Exibe \ (ou oculta \) as extensões das dimensões da grade ao longo de cada eixo.  Por padrão, as linhas de grade são mostradas apenas dentro do elemento com `display: grid` ou `display: inline-grid` CSS definidas nela. |  
    
As seções a seguir fornecem detalhes para cada uma das **configurações de exibição de sobreposição**.  

### Mostrar números de linha  

Por padrão, os números de linha positivos e negativos são exibidos na sobreposição de grade.  

Para obter mais informações sobre números negativos na sobreposição de grade, navegue até [posicionamento baseado em linha com grade CSS][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-show-line-numbers.msft.png":::
   Exibir números de linha  
:::image-end:::  

### Ocultar rótulos de linha  

Selecione **ocultar rótulos de linha** para ocultar os números de linha.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-hide-line-labels.msft.png":::
   Ocultar rótulos de linha  
:::image-end:::  

### Mostrar nomes de linha  

<!--todo: @rachel verify the link and text for line name -->  
Para obter mais informações sobre nomes de linha na sobreposição de grade, navegue até [layout usando linhas de grade nomeadas][MdnLayoutUsingNamedGridLines].  

Selecione **Mostrar nomes de linha** para exibir os nomes das linhas em vez de números.  No exemplo, 4 linhas têm nomes: `left` ,, `middle1` `middle2` e `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-show-line-names.msft.png":::
   **Mostrar nomes de linha**  
:::image-end:::  

### Mostrar tamanhos de faixas  

Habilite a caixa de seleção **Mostrar tamanhos de faixas** para exibir os tamanhos de faixa da grade.  

DevTools exibe `[authored size]` e `[computed size]` em cada rótulo de linha.  

| Size | Detalhes |  
|:--- |:--- |  
| **tamanho da criação** | O tamanho definido em stylesheet \ (omitido se não definido \). |  
| **tamanho calculado** | O tamanho real na tela. |  

Na demonstração, os `snack-box` tamanhos das colunas são definidos no `grid-template-columns:1fr 2fr;` CSS.  Portanto, os rótulos de linha da coluna exibem os tamanhos criados e calculados.  

| Tamanho da faixa | Tamanho da criação | Tamanho calculado |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96.66 PX** | 1fr | 96.66 px |  
| **2fr** &#x2022; **193.32 px** | 2fr | 193.32 px |  

Os rótulos de linha de linha exibem apenas os tamanhos calculados, pois não há tamanhos de linha definidos na folha de estilos.  

| Tamanho da faixa | Tamanho da criação | Tamanho calculado |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Mostrar tamanhos de faixas**  
:::image-end:::  

### Mostrar nomes de área  

Para exibir os nomes das áreas, habilite a caixa de seleção **Mostrar nomes de área** .  No exemplo, há três áreas na grade: **superior**, **bottom1** e **bottom2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-show-area-names.msft.png":::
   **Mostrar nomes de área**  
:::image-end:::  

### Estender linhas de grade  

Habilite a caixa de seleção **estender linhas de grade** para estender as linhas de grade para a borda da viewport ao longo de cada eixo.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Estender linhas de grade**  
:::image-end:::  

## Sobreposições de grade  

A seção **sobreposições de grade** contém uma lista de grades que estão presentes na página, cada uma com uma caixa de seleção, juntamente com várias opções.  

### Habilitar modos de exibição de sobreposição de várias grades  

<!--todo: @zoher verify and provide updates -->  

Para exibir a grade de sobreposição para várias grades, escolha a caixa de seleção ao lado de cada nome da grade.  No exemplo, há duas sobreposições de grade habilitadas que são representadas com cores diferentes.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-grid-overlays.msft.png":::
   Habilitar modos de exibição de sobreposição de várias grades  
:::image-end:::  

### Personalizar a cor da sobreposição de grade  

Para abrir o seletor de cores e personalizar a cor da sobreposição de grade, escolha a caixa ao lado do nome da sobreposição de grade.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Personalizar a cor da sobreposição de grade  
:::image-end:::  

### Realçar a grade  

Para realçar o elemento HTML no painel **elementos** e rolar para ele na página da Web, escolha o **elemento Mostrar no painel elementos** \ ( ![ Mostrar elemento no ícone do painel elementos ][ImageShowElementInElementsPanelIcon] \) ícone.  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Realçar a grade  
:::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grade CSS | JEC. FYI"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grade CSS | JEC. FYI"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Layout de grade CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout usando linhas de grade nomeadas | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Posicionamento baseado em linhas com grade CSS | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/grid) e é criada por [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
