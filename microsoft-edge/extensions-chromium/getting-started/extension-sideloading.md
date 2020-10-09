---
description: Testar a extensão por meio de Sideload no navegador
title: Sideload sua extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento da Web, HTML, CSS, JavaScript, Developer, extensões
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104767"
---
# Sideload uma extensão

Durante o desenvolvimento, você pode usar o navegador Microsoft Edge \ (Chromium \) para executar e depurar a extensão com segurança. Ao fazer o Sideload da sua extensão localmente no seu navegador, você pode executar e testar a extensão. Este artigo explica como Sideload extensões para o Microsoft Edge.

Para Sideload a extensão, siga estas etapas.

1.  Para abrir a `edge://extensions` página, escolha os três pontos na parte superior do seu navegador e, em seguida, selecione **extensões**.

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abrir a página edge://extensions":::
          Abrir a página edge://extensions :::image-end:::

1.  Na página Gerenciamento de extensão `edge://extensions` , ative o **modo de desenvolvedor** usando o botão de alternância na parte inferior esquerda da página.

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Abrir a página edge://extensions":::
          Ativar o modo de desenvolvedor :::image-end:::

1.  Ao instalar a extensão pela primeira vez, escolha **carregar desempacotada**.  Você será solicitado a fornecer o diretório com seus arquivos de origem de extensão.  Sua extensão é instalada em seu navegador, semelhante às extensões instaladas a partir da loja.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Abrir a página edge://extensions":::
          Página de extensões instaladas mostrando uma extensão Sideload :::image-end:::

Durante o desenvolvimento, você também pode precisar executar as seguintes tarefas.
* Atualize a extensão. Navegue até `edge://extensions` e, em seguida, selecione **recarregar** para atualizar a extensão.  
* Remova a extensão do seu navegador. Navegue até `edge://extensions` e selecione `Remove` na extensão.