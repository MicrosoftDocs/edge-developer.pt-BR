---
description: Teste sua extensão sideloading-lo no navegador
title: Fazer sideload da extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104767"
---
# Fazer sideload para uma extensão

Durante o desenvolvimento, você pode usar o navegador Microsoft Edge \(Chromium\) para executar e depurar sua extensão com segurança. Ao fazer sideload da extensão localmente no navegador, você pode executar e testar sua extensão. Este artigo explica como fazer sideload de extensões em Microsoft Edge.

Para fazer sideload da extensão, siga estas etapas.

1.  Abra a página escolhendo os três pontos na parte superior do navegador e `edge://extensions` selecionando **Extensões**.

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abra a página edge://extensions página":::
          Abra a página edge://extensions página :::image-end:::

1.  Na página gerenciamento de extensão em , a opção Modo desenvolvedor `edge://extensions` usando a alternância na parte inferior esquerda da página. ****

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Ativar o modo de desenvolvedor":::
          Ativar o modo de desenvolvedor :::image-end:::

1.  Ao instalar sua extensão pela primeira vez, escolha **Carregar Desempacotar**.  Você será solicitado a solicitar o diretório com seus arquivos de origem de extensão.  Sua extensão é instalada no navegador, semelhante às extensões instaladas na loja.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Página extensões instaladas mostrando uma extensão com sideload":::
          Página extensões instaladas mostrando uma extensão com sideload :::image-end:::

Durante o desenvolvimento, talvez você também precise executar as seguintes tarefas.
* Atualize a extensão. Navegue `edge://extensions` até e selecione Recarregar **para** atualizar sua extensão.  
* Remova a extensão do navegador. Navegue `edge://extensions` até e selecione em sua `Remove` extensão.