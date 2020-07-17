---
description: As etapas para criar uma conta de desenvolvedor de Complementos do Microsoft Edge no centro de parceiros.
title: Visão geral e Estados de envio de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 3bb648ee9db062bcb12f7592df752ab25d8322b5
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882643"
---
# Visão geral e Estados de envio de extensão  

A página Visão geral na central do parceiro exibe o estado de sua extensão no fluxo de envio geral.  

| # |  Estado |  Descrição/detalhes |  
|:--- |:--- |:--- |  
| um |  Em rascunho |  Depois de criar o envio e salvá-lo na sua conta, o estado muda para esse estado.  <br />  Você não enviou seu pacote de extensão e seus detalhes do formulário de envio para publicação na Microsoft Store.  <br />  Sua extensão não está disponível para os usuários neste estado.  |  
| 2|  Em revisão |  Depois de enviar a extensão, o estado muda para esse estado.  <br />  O pacote de extensão e os detalhes do formulário de envio estão em revisão pela Microsoft.  <br />  Sua extensão não está disponível para os usuários neste estado.  |  
| 3D|  Aguardando publicação |  Depois que a revisão da extensão for concluída com êxito e enquanto a extensão estiver preparada para publicação na Microsoft Store, o estado mudará para esse estado.  <br />  Esse é um estado intermediário entre `In review` e `In the store` .  <br />  Esse Estado pode não aparecer para todos os envios.  |  
| 4|  Na loja |  Após a conclusão da revisão e sua extensão ser publicada na Microsoft Store, o estado muda para esse estado.  <br />  Sua extensão está disponível na Microsoft Store em mercados que você especificou.  |  
| 5 |  Na loja.  Atualização na revisão |  Sua extensão é publicada na Microsoft Store e você enviou uma atualização em revisão pela Microsoft.  |  
| 5 |  Falha na revisão |  Se a sua extensão falha em uma crítica, o estado muda para esse estado.  <br />  Uma revisão com falha pode ocorrer durante a revisão inicial ou durante uma atualização.  <br />  Espera-se que você tome uma ação corretiva e reenvie a extensão para publicação na Microsoft Store.  |  
| 7 |  Não disponível na loja |  Há três cenários possíveis em que a extensão exibe este Estado: não **publicada da loja** , **removida da loja**e **bloqueada**.  A descrição de cada um desses três é especificada abaixo.  |  
| 08 |  Não publicado da loja |  Você não publicou sua extensão da Microsoft Store no centro de parceiros.  <br />  No centro de parceiros, na sua página de envio de extensão, você clicou no botão não publicar.  <br />  Após a cancelamento da publicação, sua extensão não está mais disponível na Microsoft Store para que novos usuários possam baixar, mas os usuários existentes podem continuar a usar suas cópias da extensão.  |  
| 222 |  Removido da loja |  Se a sua extensão for violada os termos e condições da Microsoft Store, a Microsoft poderá removê-la da Microsoft Store e o estado mudará para esse estado.  <br />  Após a remoção da sua extensão pela Microsoft, sua extensão não estará mais disponível na Microsoft Store para que novos usuários baixem, mas os usuários existentes podem continuar a usar suas cópias da extensão.  |  
| 254 |  Bloqueado |  Se a sua extensão for maliciosa e comprometer a segurança e a privacidade dos usuários, a Microsoft tem o direito de bloquear a extensão da Microsoft Store e as alterações de estado para esse estado.  <br />  Se a extensão estiver bloqueada, a extensão será removida da Microsoft Store, sua extensão também será removida dos dispositivos de usuário.  |  
