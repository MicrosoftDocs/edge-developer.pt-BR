---
description: Saiba como usar o Microsoft Edge DevTools para exibir e alterar o CSS de uma página CSS.
title: Inspecionar Grade CSS no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 68493fae5e96ef1b2c7ed1205d67fd2b4cf67df5
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564452"
---
# <a name="inspect-css-grid"></a>Inspecionar Grade CSS  

Este artigo orienta você a identificar grades CSS em um site e depurar problemas de layout de grade usando sobreposições de grade personalizáveis.  

Os exemplos usados nos números deste artigo são tirados das páginas da Web a seguir.  

*   [Caixa de frutas][JecFyiDemoCssGridFruit]  
*   [Caixa de lanchinho][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a>Antes de começar  

CSS Grid é um paradigma de layout poderoso para a Web.  Um ótimo lugar para começar a aprender sobre CSS Grid e os muitos recursos é o [guia layout de grade css][MdnCssGridLayout] no MDN.  

## <a name="discover-css-grids"></a>Descobrir grades CSS  

Quando um elemento HTML em sua página tem ou aplicado a ele, um selo é exibido ao lado dele `display: grid` `display: inline-grid` no painel `grid` [Elementos.][DevtoolsGuideChromiumOpen]  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descobrir grade" lightbox="../media/grid-discover-grid.msft.png":::
   Descobrir grade  
:::image-end:::  

Escolha o selo para alternar a exibição de uma sobreposição de grade na página.  A sobreposição aparece sobre o elemento, definida como uma grade para exibir a posição das linhas e faixas de grade:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Selo de grade de alternância" lightbox="../media/grid-highlight-grid.msft.png":::
   Selo de grade de alternância  
:::image-end:::  

Abra o **painel Layout.**  Quando as grades são incluídas em uma página, o **painel Layout** inclui uma seção **Grid** contendo várias opções para exibir as grades.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Painel de layout" lightbox="../media/grid-layout-pane.msft.png":::
   **Painel** de layout  
:::image-end:::  

A **seção Grade** no painel **Layout** contém as duas subseções a seguir.  

*   Configurações de exibição de sobreposição  
*   Sobreposições de grade  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a>Configurações de exibição de sobreposição  

As **configurações de exibição sobreposição** consistem em duas partes a seguir.  

*   Escolha uma das opções a seguir no menu suspenso.  
    
    | Opção De linha | Detalhes |  
    |:--- |:--- |  
    | **Ocultar rótulos de linha** | Ocultar os rótulos das linhas para cada sobreposição de grade. |  
    | **Mostrar números de linha** | Exibir os números das linhas para cada sobreposição de grade \(selecionado por padrão\). |  
    | **Mostrar nomes de linha** | Exibe os nomes das linhas para cada sobreposição de grade quando os nomes são fornecidos. |  
    
*  Escolha a caixa de seleção ao lado das seguintes opções.  
    
    | Opção | Detalhes |  
    |:--- |:--- |  
    | **Mostrar tamanhos de faixa**  | Exibe \(ou ocultar\) os tamanhos das faixas. |  
    | **Mostrar nomes de área** | Exibir \(ou ocultar\) os nomes da área, quando os nomes são fornecidos. |  
    | **Estender linhas de grade** | Exibe \(ou oculta\) as extensões das dimensões de grade ao longo de cada eixo.  Por padrão, as linhas de grade só são mostradas dentro do elemento com `display: grid` ou `display: inline-grid` css definido nele. |  
    
As seções a seguir fornecem detalhes para cada uma das configurações de **exibição sobreposição.**  

### <a name="show-line-numbers"></a>Mostrar números de linha  

Por padrão, os números de linha positivos e negativos são exibidos na sobreposição de grade.  

Para obter mais informações sobre números negativos na sobreposição de grade, navegue até [Posicionamento baseado em linha com CSS Grid][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Exibir números de linha" lightbox="../media/grid-show-line-numbers.msft.png":::
   Exibir números de linha  
:::image-end:::  

### <a name="hide-line-labels"></a>Ocultar rótulos de linha  

Escolha **Ocultar rótulos de linha** para ocultar os números de linha.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ocultar rótulos de linha" lightbox="../media/grid-hide-line-labels.msft.png":::
   Ocultar rótulos de linha  
:::image-end:::  

### <a name="show-line-names"></a>Mostrar nomes de linha  

Para obter mais informações sobre nomes de linha na sobreposição de grade, navegue até [Layout usando linhas de grade nomeadas][MdnLayoutUsingNamedGridLines].  

Escolha **Mostrar nomes de linha** para exibir os nomes de linha em vez de números.  No exemplo, 4 linhas têm nomes: `left` , `middle1` , e `middle2` `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Mostrar nomes de linha" lightbox="../media/grid-show-line-names.msft.png":::
   **Mostrar nomes de linha**  
:::image-end:::  

### <a name="show-track-sizes"></a>Mostrar tamanhos de faixa  

Habilita a caixa de seleção Mostrar **tamanhos** de faixa para exibir os tamanhos de faixa da grade.  

DevTools exibe `[authored size]` e em cada rótulo de `[computed size]` linha.  

| Size | Detalhes |  
|:--- |:--- |  
| **tamanho de autoria** | O tamanho definido na folha de estilos \(omitido se não definido\). |  
| **tamanho calculado** | O tamanho real na tela. |  

Na demonstração, os `snack-box` tamanhos das colunas são definidos no `grid-template-columns:1fr 2fr;` CSS.  Portanto, os rótulos de linha de coluna exibem tamanhos de autoria e computação.  

| Tamanho da faixa | Tamanho de autoria | Tamanho calculado |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96,66px** | 1fr | 96,66px |  
| **2fr** &#x2022; **193,32px** | 2fr | 193,32px |  

Os rótulos de linha de linha exibem apenas tamanhos calculados, já que não há tamanhos de linha definidos na folha de estilos.  

| Tamanho da faixa | Tamanho de autoria | Tamanho calculado |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Mostrar tamanhos de faixa" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Mostrar tamanhos de faixa**  
:::image-end:::  

### <a name="show-area-names"></a>Mostrar nomes de área  

Para exibir os nomes de área, habilita a caixa de seleção **Mostrar nomes de** área.  No exemplo, há 3 áreas na grade: **superior**, **inferior1** e **inferior2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Mostrar nomes de área" lightbox="../media/grid-show-area-names.msft.png":::
   **Mostrar nomes de área**  
:::image-end:::  

### <a name="extend-grid-lines"></a>Estender linhas de grade  

Habilita **a caixa** de seleção Estender linhas de grade para estender as linhas de grade até a borda do viewport ao longo de cada eixo.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Estender linhas de grade" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Estender linhas de grade**  
:::image-end:::  

## <a name="grid-overlays"></a>Sobreposições de grade  

A **seção Sobreposições de** grade contém uma lista de grades presentes na página, cada uma com uma caixa de seleção, juntamente com várias opções.  

### <a name="enable-overlay-views-of-multiple-grids"></a>Habilitar exibições de sobreposição de várias grades  

Para exibir a grade de sobreposição para várias grades, escolha a caixa de seleção ao lado de cada nome da grade.  No exemplo, há duas sobreposições de grade habilitadas que são representadas com cores diferentes.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Habilitar exibições de sobreposição de várias grades" lightbox="../media/grid-grid-overlays.msft.png":::
   Habilitar exibições de sobreposição de várias grades  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a>Personalizar a cor da sobreposição de grade  

Para abrir o selador de cores e personalizar a cor da sobreposição de grade, escolha a caixa ao lado do nome da sobreposição de grade.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personalizar a cor da sobreposição de grade" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Personalizar a cor da sobreposição de grade  
:::image-end:::  

### <a name="highlight-the-grid"></a>Realça a grade  

Para realçar o elemento HTML na ferramenta **Elementos** e rolar até ele na página da Web, escolha o elemento **Mostrar** no painel Elementos \( Elemento Mostrar no ícone do painel Elementos ![ ](../media/show-element-in-element-panel-icon.msft.png) \) ícone.  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Realça a grade" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Realça a grade  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grade CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grade CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Layout de Grade CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Layout usando linhas de grade nomeadas | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Posicionamento baseado em linha com grade CSS | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/grid) e é de autoria de [Jecelyn Yeen][JecelynYeen] \ (defensora do desenvolvedor, Chrome DevTools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
