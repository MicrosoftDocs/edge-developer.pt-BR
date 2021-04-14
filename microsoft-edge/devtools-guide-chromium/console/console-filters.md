---
description: Saiba como filtrar mensagens de console
title: Começar a filtrar mensagens no Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: b493bb790b48bc1c4dca0e6802d2f638099b7644
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483305"
---
# <a name="filter-console-messages"></a>Filtrar mensagens de Console  

Ao navegar na Web, você pode encontrar que **o Console** está inundado com todos os tipos de informações.  Muitas vezes, as informações não são relevantes para você.  Como informações sobre o projeto ao vivo que outro desenvolvedor registrou enquanto você depura.  Ou mais informações sobre violações e avisos sobre o desempenho do site atual que você não pode alterar.  Faz sentido usar as opções de filtro do **Console** para reduzir o ruído.  

## <a name="filter-by-log-level"></a>Filtrar por nível de log  

Cada método do `console` objeto tem um nível de gravidade anexado a ele.  Os níveis de gravidade `Verbose` são , , ou `Info` `Warning` `Error` .  Exibe os níveis de severidade na documentação [da API][DevtoolsConsoleApi].  Por exemplo, `console.log()` é uma mensagem de `Info` nível, mas é uma mensagem `console.error()` de `Error` nível.  

Para filtrar mensagens no **Console,** use o menu suspenso **Nível** de Log.  Você pode alternar o estado de cada nível.  Para desativar cada nível, remova a marca de seleção ao lado de cada um.  

:::image type="complex" source="../media/console-filter-dropdown.msft.png" alt-text="O menu suspenso filtra mensagens de console usando o nível de log" lightbox="../media/console-filter-dropdown.msft.png":::
    O menu suspenso filtra mensagens **de console** usando o nível de log  
:::image-end:::  

Como nenhum filtro é aplicado, a figura a seguir exibe dezenas de mensagens.  Em seguida, reduza e gerencie o número de mensagens.  

:::image type="complex" source="../media/console-filter-displays-all.msft.png" alt-text="Nenhum conjunto de filtros significa que você pode exibir muitas mensagens de console" lightbox="../media/console-filter-displays-all.msft.png":::
    Nenhum conjunto de filtros significa que você pode exibir muitas mensagens de console  
:::image-end:::  

Escolha ocultar todas as mensagens de nível de aviso para reduzir o ruído.  Navegue até o **menu suspenso Níveis** de Log e desmarque o `Warnings` nível.  

:::image type="complex" source="../media/console-filter-hide-warning.msft.png" alt-text="Ocultar todas as mensagens de nível de aviso no Console para filtrar grande parte do ruído" lightbox="../media/console-filter-hide-warning.msft.png":::
    Ocultar todas as mensagens de nível de aviso no **Console** para filtrar grande parte do ruído  
:::image-end:::  

## <a name="filter-by-text"></a>Filtrar por texto  

Se você quiser revisar mais detalhes, para filtrar mensagens usando texto, digite uma cadeia de caracteres na **caixa de** texto Filtro.  Por exemplo, digite na caixa para exibir apenas suas mensagens `block` sobre o navegador bloqueando o carregamento de recursos.

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Exibe as mensagens que contêm o bloco de palavras" lightbox="../media/console-filter-text.msft.png":::
    Exibe as mensagens que contêm a palavra `block`  
:::image-end:::  

## <a name="filter-by-regular-expression"></a>Filtrar por expressão regular

[Expressões regulares][MdnDocsWebJavascriptGuideRegularExpressions] são uma maneira poderosa de filtrar mensagens.  Por exemplo, digite na caixa de texto Filtro para exibir apenas `/^Tracking/` mensagens que começam com o termo **** `Tracking` .  Se você não estiver familiarizado com expressões regulares, [RegExr][|::ref1::|Main] é um ótimo recurso para aprender sobre como usar expressões regulares.

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Exibe as mensagens que começam com o filtro de palavras usando uma expressão regular na caixa de texto Filtro" lightbox="../media/console-filter-regex.msft.png":::
    Exibe as mensagens que começam com a palavra usando uma expressão regular na caixa de texto `filter` **Filtro**  
:::image-end:::  

## <a name="filter-by-message-source"></a>Filtrar por fonte de mensagem  

Você também pode definir que tipo de mensagens deseja exibir e onde cada uma delas foi originada usando a **Barra lateral** do **Console**.  Para fazer isso, escolha o botão **Mostrar barra lateral do console.**  

:::image type="complex" source="../media/console-filter-sidebar-icon.msft.png" alt-text="Para abrir a barra lateral, escolha o ícone barra lateral" lightbox="../media/console-filter-sidebar-icon.msft.png":::
    Para abrir a **barra lateral,** escolha o botão **Mostrar barra lateral do console**  
:::image-end:::  

Quando a **Barra lateral** estiver aberta, você poderá exibir o número geral de mensagens e onde cada uma delas se originou.  As opções são `All messages` , , , , e `User Messages` `Errors` `Warnings` `Info` `Verbose` .  

:::image type="complex" source="../media/console-filter-sidebar-open.msft.png" alt-text="A Barra Lateral do Console exibe as diferentes mensagens de origem de fontes" lightbox="../media/console-filter-sidebar-open.msft.png":::
    A **Barra Lateral do Console** exibe as diferentes mensagens de origem de fontes  
:::image-end:::  

Escolha qualquer uma das opções para exibir apenas as mensagens desse tipo.  Por exemplo, para exibir mensagens de usuário, escolha a opção mensagens de usuário para exibir menos ruído.

:::image type="complex" source="../media/console-filter-select-user-messages.msft.png" alt-text="Escolha exibir apenas mensagens de usuário no Console usando o filtro na barra lateral" lightbox="../media/console-filter-select-user-messages.msft.png":::
    Escolha exibir apenas mensagens de usuário no **Console** usando o filtro na **barra lateral**  
:::image-end:::  

Para filtrar mais e expandir a opção, escolha o ícone de triângulo ao lado dele.  Dessa forma, você tem mais opções para exibir apenas mensagens que se originam de uma fonte específica.  

:::image type="complex" source="../media/console-filter-sidebar-open-arrow.msft.png" alt-text="Escolha o ícone de seta expande cada uma das seções" lightbox="../media/console-filter-sidebar-open-arrow.msft.png":::
    Escolha o ícone de seta expande cada uma das seções  
:::image-end:::  

:::image type="complex" source="../media/console-filter-user-message-by-source.msft.png" alt-text="Escolha qualquer uma das novas opções para filtrar usando tipo e fonte" lightbox="../media/console-filter-user-message-by-source.msft.png":::
    Escolha qualquer uma das novas opções para filtrar usando tipo e fonte  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referência da API de console | Microsoft Docs"  

[MdnDocsWebJavascriptGuideRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expressões regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  
