---
description: Saiba mais sobre algumas dicas úteis e truques sobre extensões do Microsoft Edge
title: Dicas e truques | Extensões
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desenvolvimento da Web, html, css, javascript, desenvolvedor, extensões
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a5ea19152f5524d86d17d6f978c677c45f8f3a8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399348"
---
# <a name="tips-and-tricks"></a>Dicas e truques  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Se você estiver trabalhando em uma extensão do Microsoft Edge ou já tiver publicado uma, as dicas e truques a seguir podem ser úteis.  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a>Obter um link direto para sua extensão na Microsoft Store  

No painel do Centro de Dev do Windows, você pode encontrar um link direto para sua extensão na Microsoft Store.  Esse link pode ser útil para publicidade e compartilhamento de sua extensão.  

Depois de entrar no Centro de Dev do Windows e navegar até sua extensão pelo painel, na página Identidade do aplicativo, você encontrará o link na linha de link de protocolo **da Loja:**  

![link de protocolo de armazenamento](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a>Certifique-se de que você está seguindo a Política da Microsoft Store  

Ao criar sua extensão, lembre-se de ter em mente as diretrizes para envio à Microsoft Store realçadas na [Política da Microsoft Store.](/windows/uwp/publish/store-policies)  
 
As extensões do Microsoft Edge também têm um conjunto adicional de políticas a seguir [vistas aqui](/windows/uwp/publish/store-policies#pol_10_12).  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a>Melhorar a capacidade de descoberta da extensão na Microsoft Store  

Você pode adicionar palavras-chave ao envio de extensão para melhorar sua capacidade de descoberta por meio de pesquisas.  Por exemplo, `Microsoft Edge Extensions` e `name of my extension` .  

Isso pode ser feito no Centro de Dev do Windows na seção descrição da extensão.  Essas palavras-chave precisarão ser adicionadas para cada idioma que sua extensão oferece suporte.  

![Usar palavras-chave para enviar uma resposta a uma revisão](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a>Automatizar seu envio para a Microsoft Store  

Você pode automatizar e simplificar seus envios para a Microsoft Store usando a nova API de Envio da Microsoft Store, que permite atualizar aplicativos/jogos, complementos \(compras no aplicativo\) e pacotes de pré-venda por meio de uma API REST.  Confira a [documentação e os exemplos](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) ou use a extensão [VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) da API de Envio de código aberto para começar.  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a>Usar o Hub de Feedback do Windows para coletar comentários/avaliações/solicitações de recursos  

Você pode direcionar os usuários para a subcategoria do Windows Feedback Hub para sua extensão incorporando um link que aponta para ele.  Este link precisará ser criado usando o seguinte formato:  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Você precisará substituir pelo Nome da Família de `<PFN>` Pacotes de sua extensão.  Isso pode ser encontrado na seção **Identidade do aplicativo** para sua extensão no Centro de Dev do Windows.  

## <a name="check-out-your-ratings-and-reviews"></a>Confira suas classificações e críticas  

Faça logoff regularmente para verificar as avaliações e classificações do usuário.  Embora o aplicativo UWP tenha apenas informações sobre o mercado de usuários atual, o log no Centro de Desenvolvimento do Windows exibirá a classificação média em todos os mercados.  

## <a name="respond-to-user-reviews"></a>Responder a avaliações do usuário  

Você pode responder às críticas do usuário na Microsoft Store por meio do painel do Centro de Dev do Windows.  Navegue até sua extensão e, em Análise, selecione **Avaliações**.  Um link aparecerá abaixo de cada revisão que permitirá que você responda diretamente ao cliente.  Este canal de comunicação permite que você ofereça comentários, resoluções ou envie um obrigado pela revisão!  

![Responder à revisão do usuário](./media/reviews.png)  
