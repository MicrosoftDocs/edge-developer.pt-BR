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
# Estados de envio para extensões no armazenamento de Complementos do Microsoft Edge  

A página de visão geral no Partner Center exibe o estado de sua extensão no fluxo geral de envio.  Este artigo descreve os diferentes estados em que sua extensão pode estar a qualquer momento durante o processo de envio e certificação.  

| # |  Estado |  Detalhes |  
|:--- |:--- |:--- |  
| 1 |  Em rascunho |  Você cria seu envio e salva um rascunho na sua conta.  Você não enviou o pacote de extensão e os detalhes do formulário de envio para publicar no armazenamento de Complementos do Microsoft Edge.  Sua extensão não está disponível para os usuários nesse estado.  |  
| 2|  Em revisão |  Você enviou sua extensão.  O pacote de extensão e os detalhes do formulário de envio são analisados pela Microsoft.  Sua extensão não está disponível para os usuários nesse estado.  |  
| 3|  Aguardando publicação |  Seu envio está nesse estado após a conclusão da revisão da extensão e sua extensão está sendo preparada para publicação na Microsoft Store.  Esse estado é um estado intermediário entre `In review` e `In the store` .  Esse estado pode não aparecer para todos os envios.  |  
| 4|  Na loja |  A revisão agora está concluída e sua extensão foi publicada na loja de Complementos do Microsoft Edge.  Sua extensão está disponível na Microsoft Store nos mercados que você especificou.  |  
| 5 |  Na loja.  Atualizar em revisão |  Sua extensão foi publicada na loja de Complementos do Microsoft Edge e você enviou uma atualização que está sendo analisada pela Microsoft.  |  
| 6 |  Falha na revisão |  Seu envio está nesse estado se a extensão falhar em uma revisão.  Uma revisão com falha pode ocorrer durante a revisão inicial ou durante uma atualização.  Você precisa tomar uma ação corretiva e resubmitir sua extensão.  |  
| 7 |  Indisponível na loja |  Há três cenários possíveis quando sua extensão exibe esse estado: Não publicado do **armazenamento,** removido do **armazenamento**e **Bloqueado.**  A descrição de cada um dos três estados é especificada em 8, 9 e 10.  |  
| 8 |  Não publicado na loja |  Você não publicou sua extensão na loja de Complementos do Microsoft Edge no Partner Center.  No Partner Center, você escolheu **não publicar na** página de envio de extensão.  Depois de desinstaar sua extensão, ela não estará mais disponível no armazenamento de Complementos do Microsoft Edge para que novos usuários baixem, mas os usuários existentes poderão continuar a usar suas cópias da extensão.  |  
| 9 |  Removido do armazenamento |  Se a extensão for encontrada violando os termos e condições do armazenamento de Complementos do Microsoft Edge, a Microsoft poderá removê-la do armazenamento de Complementos do Edge e o estado mudar para esse estado.  <br />  Após a remoção da extensão pela Microsoft, sua extensão não estará mais disponível no armazenamento de Complementos do Microsoft Edge para que novos usuários baixem, mas os usuários existentes poderão continuar a usar suas cópias da extensão.  |  
| 10 |  Bloqueado |  Se sua extensão for mal-intencionada e comprometer a segurança e a privacidade dos usuários, a Microsoft tem o direito de bloquear sua extensão do armazenamento de Complementos de Borda e o estado muda para esse estado.  Se sua extensão estiver bloqueada, ela será removida da loja de Complementos de Borda e de todos os dispositivos do usuário.  |  
