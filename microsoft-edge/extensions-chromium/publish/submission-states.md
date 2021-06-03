---
description: Saiba mais sobre os diferentes estados ao enviar extensões para a loja
title: Estados de envio para extensões na loja
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 881166471ec5fabb66367ead650cb86b883cf01d
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343140"
---
# Estados de envio para extensões no Microsoft Edge de complementos  

A página de visão geral no Partner Center exibe o estado de sua extensão no fluxo geral de envio.  Este artigo descreve os diferentes estados em que sua extensão pode estar a qualquer momento durante o processo de envio e certificação.  

| # |  Estado |  Detalhes |  
|:--- |:--- |:--- |  
| 1 |  No rascunho |  Crie seu envio e salve um rascunho em sua conta.  Você não enviou o pacote de extensão e os detalhes do formulário de envio para publicar no Microsoft Edge de complementos.  Sua extensão não está disponível para os usuários neste estado.  |  
| 2|  Em revisão |  Você enviou sua extensão.  Seu pacote de extensão e seus detalhes do formulário de envio são revisados pela Microsoft.  Sua extensão não está disponível para os usuários neste estado.  |  
| 3|  Aguardando publicação |  Seu envio está nesse estado depois que sua revisão de extensão é concluída e sua extensão está sendo preparada para publicação no Microsoft Store.  Este estado é um estado intermediário entre `In review` e `In the store` .  Esse estado pode não aparecer para todos os envios.  |  
| 4|  Na loja |  A revisão agora está concluída e sua extensão é publicada no Microsoft Edge de complementos.  Sua extensão está disponível no Microsoft Store nos mercados especificados.  |  
| 5 |  Na loja.  Atualização em revisão |  Sua extensão é publicada no Microsoft Edge de complementos e você enviou uma atualização que está em análise pela Microsoft.  |  
| 6 |  Falha na revisão |  Seu envio está nesse estado se sua extensão falhar em uma revisão.  Uma revisão com falha pode ocorrer durante a revisão inicial ou durante uma atualização.  Você precisa tomar medidas corretivas e reabrir sua extensão.  |  
| 7 |  Indisponível na loja |  Há três cenários possíveis quando sua extensão exibe esse estado: Não publicado do  **armazenamento,** Removido da **loja**e **Bloqueado**.  A descrição de cada um dos três estados é especificada em 8, 9 e 10.  |  
| 8 |  Não publicado na loja |  Você não publicou sua extensão do Microsoft Edge de complementos no Partner Center.  No Partner Center, você **escolheu não publicar na** página de envio de extensão.  Depois de não publicar sua extensão, ela não estará mais disponível no armazenamento de complementos do Microsoft Edge para novos usuários baixarem, mas os usuários existentes podem continuar a usar suas cópias da extensão.  |  
| 9 |  Removido da loja |  Se a extensão for encontrada para violar os termos e condições do Microsoft Edge de complementos, a Microsoft poderá removê-la do armazenamento de Complementos de Borda e o estado muda para esse estado.  <br />  Após a remoção da extensão pela Microsoft, sua extensão não está mais disponível no armazenamento de complementos do Microsoft Edge para novos usuários baixarem, mas os usuários existentes podem continuar a usar suas cópias da extensão.  |  
| 10 |  Bloqueado |  Se sua extensão for encontrada como mal-intencionada e comprometer a segurança e a privacidade dos usuários, a Microsoft tem o direito de bloquear sua extensão do armazenamento de Complementos de Borda e o estado muda para esse estado.  Se a extensão estiver bloqueada, ela será removida do armazenamento de Complementos de Borda e de todos os dispositivos do usuário.  |  
