---
description: Saiba mais sobre algumas dicas e truques úteis em relação às extensões do Microsoft Edge
title: Extensões-dicas e truques
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor, extensões
ms.openlocfilehash: db15aa49649432a6c4400b4e6830501c40485a83
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561159"
---
# Dicas e truques  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Não importa se você está trabalhando em uma extensão do Microsoft Edge ou já publicou uma, as dicas e truques a seguir podem ser úteis.

## Obter um link direto para sua extensão na Microsoft Store
No painel do centro de desenvolvimento do Windows, você pode encontrar um link direto para sua extensão na Microsoft Store. Esse link pode ser útil para publicidade e compartilhamento de sua extensão.


Depois de fazer logon no centro de desenvolvimento do Windows e navegar para sua extensão por meio do painel, na página identidade do aplicativo, você encontrará o link na linha do **link do protocolo da loja** :

![link do protocolo da loja](./media/store-link.png)
 
## Verifique se você está acompanhando a política da Microsoft Store
Ao criar sua extensão, certifique-se de ter em mente as diretrizes para enviar para a Microsoft Store realçada na [política da Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx). 
 
O Microsoft Edge Extensions também tem um conjunto de políticas adicional para acompanhar [aqui](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).

## Melhorar a capacidade de descoberta da extensão na Microsoft Store

Você pode adicionar palavras-chave ao envio de extensão para imporove sua capacidade de descoberta pelas pesquisas. Por exemplo, "extensões Microsoft Edge" e "nome da minha extensão". 

Isso pode ser feito no centro de desenvolvimento do Windows na seção Descrição da extensão. Essas palavras-chave precisarão ser adicionadas para cada idioma ao qual a extensão for compatível.

![Enviar uma resposta a uma crítica](./media/keywords.png)

## Automatizar o envio para a Microsoft Store
Você pode automatizar e simplificar seus envios para a Microsoft Store usando a nova API de envio da Microsoft Store, que permite atualizar aplicativos/jogos, Complementos (compras no aplicativo) e pacotes de pré-lançamento por meio de uma API REST. Confira a [documentação e os exemplos](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) ou use a [extensão do VSTS da API de envio](https://github.com/Microsoft/windows-dev-center-vsts-extension) do código-fonte aberto para começar.

## Usar o Hub de feedback do Windows para reunir comentários/análises/solicitações de recursos

Você pode direcionar os usuários para a subcategoria do hub de feedback do Windows para sua extensão inserindo um link que aponta para ele. Será necessário criar esse link usando o seguinte formato: 

`feedback-hub://?tabid=2&appid=<PFN>!App`

Você precisará substituir `<PFN>` pelo nome da família de pacotes pela extensão. Isso pode ser encontrado na seção **identidade do aplicativo** para sua extensão no centro de desenvolvimento do Windows.

## Confira suas classificações e avaliações
Faça logon regularmente para verificar suas análises e classificações de usuários. Embora o aplicativo UWP só tenha informações sobre o mercado atual do usuário, fazer logon no centro de desenvolvimento do Windows exibirá a classificação média em todos os mercados.

## Responder às críticas do usuário
Você pode responder às críticas do usuário na Microsoft Store por meio do painel do centro de desenvolvimento do Windows. Navegue até sua extensão e em análises selecione **análises**. Um link será exibido abaixo de cada revisão que permitirá que você responda diretamente ao cliente. Este canal de comunicação permite que você ofereça feedback, resoluções ou envie um agradecimento para a revisão!

![Enviar uma resposta a uma crítica](./media/reviews.png)
