---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Guias para recursos de navegador no Microsoft Edge.
title: Guia de desenvolvimento de navegador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 854b0e8ac057db3cc8b53af6205404d0841dfdb4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942038"
---
# Recursos do navegador  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## Políticas de reprodução automática  

 O Microsoft Edge fornece aos clientes a capacidade de personalizar suas preferências de navegação em sites que a mídia de reprodução automática com som para minimizar distrações na Web e conservar a largura de banda.  Os usuários podem personalizar o comportamento de mídia com os controles de reprodução automática global e por site.  Além disso, o Microsoft Edge automaticamente suprime a reprodução automática de mídia em guias de plano de fundo.  

Confira [as políticas de reprodução automática](./browser-features/autoplay-policies.md) para obter detalhes e práticas recomendadas para garantir uma boa experiência do usuário com mídia hospedada em seu site.  

## Flash  

Se o Flash for usado na sua página, mas o usuário não o tiver habilitado, o Microsoft Edge normalmente mostrará um ícone de peça de quebra-cabeça na barra de endereços.  Se você estiver adicionando dinamicamente o controle de flash após a página ser carregada, o ícone de quebra-cabeça pode não ser exibido, e nesse caso, você desejará [testar se o flash está carregado e oferecer uma experiência de fallback normal](./browser-features/flash.md) , se não estiver presente.  

## Modo de exibição de leitura.  

O Microsoft Edge fornece um [modo de exibição de leitura](./browser-features/reading-view.md) para uma experiência de leitura mais simplificada do que o livro de páginas da Web, sem a distração de conteúdo não relacionado ou outro conteúdo secundário na página.  Aqui estão dicas sobre como garantir uma excelente experiência de exibição de leitura com seu site e também instruções para optar por não usar o seu site no modo de exibição de leitura.  

## Descoberta de provedores de pesquisa  

A integração de pesquisa avançada está embutida na barra de endereços do Microsoft Edge, incluindo sugestões de pesquisa, resultados da Web, seu histórico de navegação e favoritos.  [Veja mais informações para provedores de pesquisa](./browser-features/search-provider-discovery.md) que buscam oferecer suporte para o Microsoft Edge.  
