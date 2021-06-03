---
description: O processo de atualização ou remoção de extensões do Microsoft Edge de complementos
title: Atualizar uma listagem de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 692c534ac0586d53002e4a032197e22ae24e2863
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343154"
---
# Atualizar ou remover sua extensão  

Você pode atualizar uma extensão enviada ou remover uma listagem de extensão publicada do Microsoft Edge de complementos a qualquer momento.  

## Atualizar sua extensão no Microsoft Edge de complementos  

> [!NOTE]
> A duração do processo de certificação de uma atualização para uma extensão pode levar de algumas horas a alguns dias.  

### Atualizar uma extensão existente no Microsoft Edge de complementos  

Para atualizar sua extensão na loja, conclua as etapas a seguir.  

1.  Navegue até o [painel do desenvolvedor][MicrosoftPartnerCenter] e escolha a extensão que deseja atualizar.  
1.  Atualize o pacote de extensão ou os metadados da extensão.  Se você atualizar o pacote de extensão, certifique-se de aumentar a versão no arquivo de manifesto.  
1.  Depois de fazer as alterações, escolha **Salvar**  >  **Publicar** para atualizar sua listagem de extensão e inicie o processo de certificação.  
1.  Depois que a coluna for exibida, sua atualização de extensão estará disponível no `Status` `In the store` Microsoft Edge de complementos.  
    
### Atualizar sua extensão durante a etapa de certificação  

Embora sua extensão ainda esteja no estágio de certificação e antes de ser publicada no Microsoft Edge de complementos, você pode atualizá-la. Se sua extensão falhar no processo de certificação, talvez você também precise atualizar sua extensão.    

Para verificar o status da extensão, navegue até o painel associado à sua listagem no [Partner Center][MicrosoftPartnerCenter].  

Para editar seu envio, conclua as etapas a seguir.  

1.  Navegue até o [painel do desenvolvedor][MicrosoftPartnerCenter] e escolha a extensão que deseja atualizar.  As informações que você preencheu durante o envio anterior são exibidas.  
1.  Para abrir a seção **Visão geral da** extensão, use a barra de navegação esquerda.  Para cancelar o envio atual, escolha **Cancelar envio**.  
1.  Mova para outras seções e atualize o pacote de extensão ou os metadados da extensão.  Se você atualizar o pacote de extensão, certifique-se de aumentar a versão no arquivo de manifesto para corresponder às alterações desde a versão anterior do pacote.  
1.  Depois de fazer alterações, escolha **Salvar**  >  **Publicar**.  
    
> [!IMPORTANT]
> O processo interrompe e remove seu envio atual do pipeline de certificação Microsoft Edge extensões e uma nova revisão começa com o envio mais recente.  

### Atualizar sua extensão depois que ela falhou na certificação  

Depois que sua extensão falhou no processo de certificação, você precisa atualizar sua extensão e reabrir sua extensão que incorpora os comentários.  

Para editar sua extensão, conclua as etapas a seguir.  

1.  Navegue até o [painel do desenvolvedor][MicrosoftPartnerCenter] e escolha a extensão que falhou no processo de certificação.  
1.  Atualize o pacote de extensão ou os metadados que incorporam os comentários recebidos do processo de certificação.  Se você atualizar o pacote de extensão, certifique-se de aumentar a versão no arquivo de manifesto.  
1.  Depois de fazer alterações, escolha **Salvar**  >  **Publicar**.  
    
## Remover extensões do Microsoft Edge de complementos  

Para remover sua extensão do Microsoft Edge de complementos, conclua as etapas a seguir.  

1.  Navegue até o [painel do desenvolvedor.][MicrosoftPartnerCenter]  Na página Painel, escolha a listagem a ser removido.  
1.  Escolha **Visão geral da** extensão em sua listagem.  
1.  Escolha **Não publicar para** remover a listagem do Microsoft Edge de complementos.  
    
Sua extensão agora foi removida do Microsoft Edge de complementos.  Os usuários que já instalaram sua extensão podem continuar a usá-la, mas os novos usuários não a encontram.  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  
