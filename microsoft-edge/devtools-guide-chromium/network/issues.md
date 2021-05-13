---
description: Saiba como detectar problemas de rede no painel Rede do Microsoft Edge DevTools.
title: Guia de problemas de rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c99f43872abe04800880c63ee4126bfcdd633edb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564977"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="network-issues-guide"></a>Guia de problemas de rede  

Este guia mostra como detectar problemas de rede ou oportunidades de otimização no painel Rede do Microsoft Edge DevTools.  

Para saber os conceitos básicos da **ferramenta Rede,** navegue até [Introdução][NetworkPerformance].  

## <a name="queued-or-stalled-requests"></a>Solicitações em fila ou paralisadas  

**Sintomas**  

Seis solicitações estão sendo baixadas simultaneamente.  Depois disso, uma série de solicitações são enluadas ou paralisadas.  Quando uma das seis primeiras solicitações é final, uma das solicitações na fila é iniciada.  

Na **Cascata,** na figura a seguir, as seis primeiras solicitações para `edge-iconx1024.msft.png` o ativo começam simultaneamente.  As solicitações subsequentes são paralisadas até que uma das seis terminações originais.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Um exemplo de uma série em fila ou paralisada no painel Rede" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Um exemplo de uma série em fila ou paralisada na **ferramenta Rede**  
:::image-end:::  

**Causas**  

Muitas solicitações estão sendo feitas em um único domínio.  Em conexões HTTP/1.0 ou HTTP/1.1, Microsoft Edge permite no máximo seis conexões TCP simultâneas por host.  

**Correções**  

*   Implemente o fragmento de domínio se você deve usar HTTP/1.0 ou HTTP/1.1.  
*   Use HTTP/2.  Não use o fragmento de domínio com HTTP/2.  
*   Remover ou adiar solicitações desnecessárias para que solicitações críticas baixem anteriormente.  
    
## <a name="slow-time-to-first-byte-ttfb"></a>Tempo lento para primeiro byte (TTFB)  

**Sintomas**  

Uma solicitação passa muito tempo esperando para receber o primeiro byte do servidor.  

Na figura a seguir, a barra longa e verde na **Cascata** indica que a solicitação estava aguardando muito tempo.  Isso foi simulado usando um perfil para restringir a velocidade da rede e adicionar um atraso.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Um exemplo de uma solicitação com um tempo lento para o primeiro byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Um exemplo de uma solicitação com um tempo lento para o primeiro byte  
:::image-end:::  

**Causas**  

*   A conexão entre o cliente e o servidor é lenta.  
*   O servidor é lento para responder.  Hospede o servidor localmente para determinar se é a conexão ou o servidor que está lento.  Se você ainda tiver um tempo lento para o primeiro byte \(TTFB\) ao acessar um servidor local, o servidor será lento.  
    
**Correções**  

*   Se a conexão for lenta, considere hospedar seu conteúdo em um CDN ou alterar provedores de hospedagem.  
*   Se o servidor for lento, considere otimizar consultas de banco de dados, implementar um cache ou modificar a configuração do servidor.  
    
## <a name="slow-content-download"></a>Download de conteúdo lento  

**Sintomas**  

Uma solicitação leva muito tempo para ser baixada.  

Na figura a seguir, a barra longa e azul na **Cascata** ao lado do png significa que demorou muito para ser baixado.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Um exemplo de uma solicitação que leva muito tempo para ser baixada" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Um exemplo de uma solicitação que leva muito tempo para ser baixada  
:::image-end:::  

**Causas**  

*   A conexão entre o cliente e o servidor é lenta.  
*   Muito conteúdo está sendo baixado.  
    
**Correções**  

*   Considere hospedar seu conteúdo em um CDN ou alterar provedores de hospedagem.  
*   Envie menos bytes otimizando suas solicitações.  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspecionar a atividade de rede no Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Novo problema - MicrosoftDocs/desenvolvedor de borda"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/network/issues) é encontrada aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) e [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors#jonathan-garbee
