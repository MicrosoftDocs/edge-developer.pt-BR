---
description: O processo de atualização da extensão na Microsoft Store.
title: Atualizar uma listagem de extensão
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de navegador, Complementos, centro de parceiros, desenvolvedor
ms.openlocfilehash: 0d4512331b4f9542921d2063c908b5e9d4251074
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015672"
---
# Atualizar uma listagem de extensão  

Atualize uma listagem existente no catálogo de Complementos do Microsoft Edge \ (Complementos do Microsoft Edge \).  Você pode alterar uma extensão publicada a qualquer momento.  Durante a atualização, você não precisa atualizar toda a extensão para fazer algumas alterações, como descrição ou logotipo de atualização.  Mas se você atualizar o pacote de extensão, lembre-se de aumentar o número da versão sempre.  

## Atualizar uma extensão já publicada  

Para atualizar sua listagem, siga estas etapas:  

1.  Acesse o [painel do desenvolvedor][MicrosoftPartnerCenter].  Na página Visão geral, clique na listagem que você deseja atualizar.  Isso traz os detalhes do formulário de envio que você preencheu durante a publicação.  
1.  Faça as alterações desejadas no pacote, na descrição, nos ativos gráficos ou em outras configurações.  Se você atualizar o arquivo do pacote, certifique-se de que a versão no manifesto seja maior do que a versão do pacote anterior.
1.  Depois de efetuar alterações, clique em salvar e publicar.
1.  Acesse o painel do desenvolvedor da [central de parceiros][MicrosoftPartnerCenter] para ver o status da sua listagem alterado de `In the store` para `In the store.  Certification in progress` .  

> [!NOTE]
> A duração do processo de publicação de atualização varia de algumas horas a alguns dias.  

Depois que a `Status` coluna `In the store` for exibida, a atualização de extensão estará disponível nos Complementos do Microsoft Edge.  

## Atualizar uma extensão durante a etapa de certificação  

Você pode editar e atualizar o envio da extensão após enviá-lo antes de entrar na etapa publicar.  Você pode verificar o status da sua extensão na página de **visão geral da extensão** associada à sua listagem no [centro de parceiros][MicrosoftPartnerCenter].  

Para editar seu envio, você pode seguir estas etapas:  

1.  Acesse o [painel do desenvolvedor][MicrosoftPartnerCenter].  Na página **visão geral** , clique na listagem que você deseja atualizar.  Isso traz os detalhes do formulário de envio que você preencheu durante a publicação.  
1.  Vá para a seção **visão geral da extensão** usando a barra de navegação à esquerda, conforme mostrado.  Cancele o envio atual clicando no botão **Cancelar envio** .  
1.  Vá para outras seções e faça as alterações desejadas no pacote, na descrição, nos ativos gráficos ou em outras configurações.  Se você atualizar o arquivo do pacote, certifique-se de que a versão no manifesto seja maior do que a versão do pacote anterior.  
1.  Depois de efetuar alterações, clique em **salvar** e **publicar**.  

> [!IMPORTANT]
> Esse processo para e remove o envio atual do nosso pipeline de certificação, e uma nova revisão começa com o envio mais recente.  

> [!NOTE]
> A duração do processo de publicação de atualização varia de algumas horas a alguns dias.  

Depois que a `Status` coluna `In the store` for exibida, a atualização de extensão estará disponível nos Complementos do Microsoft Edge.  

## Remover a extensão dos complementos do Microsoft Edge  

Para remover a extensão dos complementos do Microsoft Edge, faça o seguinte:  

1.  Acesse o [painel do desenvolvedor][MicrosoftPartnerCenter].  Na página **visão geral** , clique na listagem que você deseja remover.  
1.  Abra a página de **visão geral da extensão** da sua listagem.  
1.  Clique em **Cancelar publicação**.  Isso cancelará a publicação da listagem dos complementos do Microsoft Edge.  

Essas etapas removem a extensão dos complementos do Microsoft Edge, ou seja, os novos usuários não conseguem localizar a extensão nem instalá-la, mas os usuários que já instalaram a extensão podem continuar a usá-la.  

<!-- image links -->  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Central de parceiros"  
