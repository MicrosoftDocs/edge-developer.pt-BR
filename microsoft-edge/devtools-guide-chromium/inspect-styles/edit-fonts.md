---
description: Saiba como alterar estilos e configurações de fonte CSS usando o painel Estilos no Microsoft Edge DevTools.
title: Editar estilos e configurações de fonte CSS no painel Estilos no DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 928f7abb0f74839708cbe5c904ad321109ae33f0
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313091"
---
# Editar estilos e configurações de fonte CSS no painel Estilos  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

A tipografia na Web é uma parte importante da experiência do usuário.  Você deseja garantir que você conheça as diretrizes da marca corporativa e que seu conteúdo seja exibido conforme o esperado em vários dispositivos.  O texto deve ser fácil de ler usando tamanho e altura de linha.  Os usuários podem re tamanho das fontes para atender às necessidades individuais.  Para situações em que fontes específicas não estão disponíveis em um dispositivo de usuário, você deve fornecer opções de fonte de fallback.  

CSS fornece melhor suporte para tipografia nos últimos anos.  Há dezenas de unidades CSS diferentes disponíveis para definir o tamanho do texto.  Você também tem várias propriedades CSS que afetam o tamanho da fonte, o espaçamento, a altura da linha e outros recursos tipográficos.  

Para facilitar o trabalho com tipografia, um **Editor** de Fontes visual agora está **no** painel Estilos.  Você pode alterar as configurações de fonte e as alterações são renderizadas imediatamente no navegador.  Tudo sem conhecimento profundo do CSS.  

Atualmente, **a ferramenta Habilitar** nova ferramenta de editor de fontes no recurso do painel Estilos é experimental e você precisa ative-a para ferramentas de desenvolvedor do [Microsoft Edge.][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  

Qualquer CSS no painel **Estilos,** seja definições de fonte ou estilos em linha, exibe automaticamente um ícone que abre o Editor de **Fonte**visual.  Para abrir o **Editor de Fonte**visual, escolha o ícone do Editor **de** Fontes.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="O ícone no painel Estilos para editar configurações de fonte" lightbox="../media/font-editor-icon.msft.png":::
         O ícone no painel **Estilos** para editar configurações de fonte  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="O Editor de Fontes aberto na parte superior do painel Estilos" lightbox="../media/font-editor-open.msft.png":::
         O **Editor de** Fontes aberto na parte superior do painel Estilos ****  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Todos os campos no Editor de **Fonte visual** são preenchidos a partir dos valores no CSS **no** painel Estilos.  Por exemplo, a definição é definida como no painel Estilos, para que o campo de texto de altura da linha seja exibido, e a lista suspenso `line-height` `160%` de unidade é **** `160` `%` exibida.  Além disso, o controle deslizante é automaticamente definido para corresponder aos valores do campo de texto.  

O **Editor de** Fontes consiste em duas partes: o seletor de Família de Fontes e o editor de Propriedades css.  

## O seletor de Família de Fontes  

O seletor de Família de Fontes é a parte superior do Editor de **Fonte visual.**  Para escolher as fontes da regra CSS, no editor de CSS, use o **seletor de Família de** Fontes.  Você pode escolher fontes principais e de fallback para cada regra CSS.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="O Editor de Fontes aberto na parte superior do painel Estilos com o seletor da Família de Fontes realçado" lightbox="../media/font-editor-font-family.msft.png":::
   O **Editor de** Fontes aberto na parte superior do painel **Estilos** com o **seletor da Família de** Fontes realçado  
:::image-end:::  

Use o **menu suspenso Família** de Fontes para escolher em uma lista de fontes.  As fontes são organizadas em quatro grupos.  

1.  Fontes computadas, que são as fontes disponíveis na folha de estilos no **painel** Estilos.  
1.  Fontes do sistema, que são as fontes disponíveis no sistema operacional atual.  
1.  Famílias de fontes genéricas, como `serif` ou `sans-serif` .  
1.  Valores globais, como `inherit` , `initial` e `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="O editor de fontes aberto na parte superior do painel Estilos com o seletor da Família de Fontes realçado" lightbox="../media/font-editor-font-family-list.msft.png":::
   O **Editor de** Fontes aberto na parte superior do painel **Estilos** com o **seletor da Família** de Fontes realçado  
:::image-end:::  

Depois de escolher uma fonte, outro menu suspenso é exibido para você escolher fontes de fallback.  Você pode escolher até oito fontes de fallback.  Para remover uma fonte, escolha o **ícone Excluir Família de** Fontes.  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Se você escolher um valor global para a família de fontes, não obterá outro menu suspenso, pois não há fallback para ele no CSS.  

## O editor de Propriedades CSS  

You may change CSS font properties in the lower part of the visual **Font Editor**.  Você pode alterar o tamanho da fonte, a altura da linha, o peso da fonte e o espaçamento entre letras usando qualquer um dos controles da interface do usuário.  Suas alterações são aplicadas imediatamente no navegador.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="O editor de fontes aberto na parte superior do painel Estilos com as propriedades CSS realçadas" lightbox="../media/font-editor-css-properties.msft.png":::
   O **Editor de** Fontes aberto na parte superior do painel **Estilos** com as propriedades CSS realçadas  
:::image-end:::  

Você também pode converter unidades CSS usando o **Editor de Fonte visual.**  For example, you may use the tool on a CSS rule where the **Font Size** slider is initially set to `16 pixels` .  Agora, use o menu suspenso de unidade e escolha o `em` valor.  O `1 em` exibido é igual a `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Alterar o tamanho da fonte para 16 pixels" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Alterar o tamanho da fonte para `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Abrir o menu suspenso de unidade para converter em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         Abrir o menu suspenso de unidade para converter em `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

O menu suspenso de unidade fornece todas as unidades CSS numéricas disponíveis.  Tamanho da fonte, altura da linha, peso da fonte e espaçamento usam unidades diferentes.  Quando as caixas de texto têm foco, você pode selecionar as teclas e `arrow up` `arrow down` as teclas para ajustar suas configurações.  Para usar os controles deslizantes com um teclado, selecione `arrow left` as `arrow down` teclas e as teclas.  

O editor de Propriedades CSS também inclui palavras-chave predefinidas.  Para usar as palavras-chave predefinidas, no lado direito, escolha o `Toggle Input Type` ícone.  A interface do usuário muda e um menu suspenso de palavras-chave predefinidas é exibido.  Para retornar à interface do usuário com o controle deslizante e outros controles de interface do usuário, escolha o `Toggle Input Type` ícone novamente.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Abrir a interface de palavra-chave predefinida" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Abrir a interface de palavra-chave predefinida  
:::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Recursos experimentais | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Ativar recursos experimentais - recursos experimentais | Microsoft Docs"  
