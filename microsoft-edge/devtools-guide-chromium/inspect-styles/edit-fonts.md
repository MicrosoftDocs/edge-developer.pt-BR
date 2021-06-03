---
description: Saiba como alterar estilos de fonte CSS e configurações usando o painel Estilos em Microsoft Edge DevTools.
title: Editar estilos de fonte CSS e configurações no painel Estilos no DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439490"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a>Editar estilos de fonte CSS e configurações no painel Estilos  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

Tipografia na Web é uma parte importante da experiência do usuário.  Você deseja garantir que você conheça as diretrizes de marca corporativa e que seu conteúdo seja exibido conforme o esperado em vários dispositivos.  O texto deve ser fácil de ler usando tamanho e altura de linha.  Os usuários podem resizer fontes para atender às necessidades individuais.  Para situações em que fontes específicas não estão disponíveis em um dispositivo de usuário, você deve fornecer opções de fonte de fallback.  

CSS oferece melhor suporte para tipografia nos últimos anos.  Dezenas de unidades CSS diferentes estão disponíveis para definir o tamanho do texto.  Você também tem várias propriedades CSS que afetam o tamanho da fonte, o espaçamento, a altura da linha e outros recursos tipográficos.  

Para facilitar o trabalho com tipografia, um Editor de **Fonte** visual agora está no painel **Estilos.**  Você pode alterar suas configurações de fonte e as alterações são renderizadas imediatamente no navegador.  Tudo isso sem conhecimento aprofundado de CSS.  

Atualmente, o **Enable new font editor tool within the Styles pane** recurso é experimental e você precisa austá-lo para Microsoft Edge Ferramentas de [Desenvolvedor.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  

Qualquer CSS no painel **Estilos,** definições de fonte ou estilos em linha, exibe automaticamente um ícone que abre o Editor de **Fontes visual**.  Para abrir o Editor **de Fonte visual,** escolha o **ícone editor de** fontes.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="O ícone no painel Estilos para editar configurações de fonte" lightbox="../media/font-editor-icon.msft.png":::
         O ícone no painel **Estilos** para editar configurações de fonte  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O Editor de Fontes aberto em cima do painel Estilos" lightbox="../media/font-editor-open.msft.png":::
         O **Editor de Fontes** aberto em cima do painel **Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Todos os campos no Editor de **Fontes visuais** são preenchidos a partir dos valores no CSS no painel **Estilos.**  Por exemplo, a definição é definida como no painel `line-height` `160%` **Estilos,** para que o campo de texto de altura da linha seja exibido e a lista suspenso da unidade `160` exibe `%` .  Além disso, o controle deslizante é definido automaticamente para corresponder aos valores do campo de texto.  

O **Editor de Fontes** consiste em duas partes: o seletor família de fontes e o editor de Propriedades CSS.  

## <a name="the-font-family-selector"></a>O seletor família de fontes  

O seletor família de fontes é a parte superior do Editor de **Fontes visual.**  Para escolher as fontes da regra CSS, no editor CSS, use o **seletor Família de** Fontes.  Você pode escolher fontes principais e fallback para cada regra CSS.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="O Editor de Fontes aberto em cima do painel Estilos com o seletor família de fontes realçada" lightbox="../media/font-editor-font-family.msft.png":::
   O **Editor de Fontes** aberto em cima do painel **Estilos** com o seletor **família** de fontes realçada  
:::image-end:::  

Use o menu **suspenso Família** de Fontes para escolher de uma lista de fontes.  As fontes são organizadas em quatro grupos.  

1.  Fontes computadas, que são as fontes disponíveis na folha de estilos no painel **Estilos.**  
1.  Fontes do sistema, que são as fontes disponíveis no sistema operacional atual.  
1.  Famílias de fontes genéricas, como `serif` ou `sans-serif` .  
1.  Valores globais, como `inherit` , `initial` e `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="O editor de fontes aberto em cima do painel Estilos com o seletor família de fontes realçada" lightbox="../media/font-editor-font-family-list.msft.png":::
   O **Editor de Fontes** aberto em cima do painel **Estilos** com o seletor **família** de fontes realçada  
:::image-end:::  

Depois de escolher uma fonte, outro menu suspenso é exibido para você escolher fontes de fallback.  Você pode escolher até oito fontes de fallback.  Para remover uma fonte, escolha o **ícone Excluir Família de** Fontes.  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Se você escolher um valor global para a família de fontes, não obterá outro menu suspenso, pois não há fallback para ele em CSS.  

## <a name="the-css-properties-editor"></a>O editor de Propriedades CSS  

Você pode alterar propriedades de fonte CSS na parte inferior do Editor de **Fontes visual**.  Você pode alterar o tamanho da fonte, a altura da linha, o peso da fonte e o espaçamento de carta usando qualquer um dos controles da interface do usuário.  Suas alterações são aplicadas imediatamente no navegador.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="O editor de fontes aberto em cima do painel Estilos com as propriedades CSS realçadas" lightbox="../media/font-editor-css-properties.msft.png":::
   O **Editor de Fontes** aberto em cima do painel **Estilos** com as propriedades CSS realçadas  
:::image-end:::  

Você também pode converter unidades CSS usando o Editor de **Fonte visual**.  Por exemplo, você pode usar a ferramenta em uma regra CSS em que o controle deslizante **Tamanho** da Fonte é definido inicialmente como `16 pixels` .  Agora, use o menu suspenso da unidade e escolha o valor `em` .  O `1 em` exibido é igual a `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Alterar o tamanho da fonte para 16 pixels" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Alterar o tamanho da fonte para `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Abra o menu suspenso da unidade para converter em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         Abra o menu suspenso da unidade para converter em `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

O menu suspenso da unidade fornece todas as unidades CSS numéricas disponíveis.  O tamanho da fonte, a altura da linha, o peso da fonte e o espaçamento usam unidades diferentes.  Quando as caixas de texto têm foco, você pode selecionar as `arrow up` teclas e `arrow down` ajustar as configurações.  Para usar os controles deslizantes com um teclado, selecione `arrow left` as `arrow down` teclas e.  

O editor de Propriedades CSS também inclui palavras-chave predefinidas.  Para usar as palavras-chave predefinidas, no lado direito, escolha o `Toggle Input Type` ícone.  As alterações da interface do usuário e um menu suspenso de palavras-chave predefinidas são exibidos.  Para retornar à interface do usuário com o controle deslizante e outros controles de interface do usuário, escolha `Toggle Input Type` o ícone novamente.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Abra a interface de palavra-chave predefinida" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Abra a interface de palavra-chave predefinida  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - Recursos experimentais | Microsoft Docs"  
