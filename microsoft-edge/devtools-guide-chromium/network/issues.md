---
description: Saiba como detectar problemas de rede no painel rede do Microsoft Edge DevTools.
title: Guia de Problemas de Rede
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ccd78c34a50bf235416df58aad28df9253b1b24e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993370"
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





# Guia de problemas de rede   




Este guia mostra como detectar problemas de rede ou oportunidades de otimização no painel rede do Microsoft Edge DevTools.  

Consulte [introdução][NetworkPerformance] para aprender as noções básicas do painel **rede** .  

## Solicitações em fila ou interrompidas   

**Sintomas**  

Seis solicitações estão sendo baixadas simultaneamente.  Depois disso, uma série de solicitações é enfileirada ou interrompida.  Após a conclusão de uma das primeiras seis solicitações, uma das solicitações na fila é iniciada.  

Na **cascata** na figura a seguir, as primeiras seis solicitações para o `edge-iconx1024.msft.png` ativo começam simultaneamente.  As solicitações subsequentes serão interrompidas até que uma das 6 originais seja concluída.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Um exemplo de uma série em fila ou Stallion no painel rede" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Um exemplo de uma série em fila ou Stallion no painel **rede**  
:::image-end:::  

**Causas**  

Muitas solicitações estão sendo feitas em um único domínio.  Em conexões HTTP/1.0 ou HTTP/1.1, o Microsoft Edge permite um máximo de seis conexões TCP simultâneas por host.  

**Corrige**  

*   Implemente o fragmentação de domínio se você precisar usar HTTP/1.0 ou HTTP/1.1.  
*   Use HTTP/2.  Não use o fragmentação de domínio com HTTP/2.  
*   Remova ou adie solicitações desnecessárias para que as solicitações críticas sejam baixadas anteriormente.  
    
## Tempo de demora para o primeiro byte (TTFB)   

**Sintomas**  

Uma solicitação gasta muito tempo esperando receber o primeiro byte do servidor.  

Na figura a seguir, o longo, a barra verde na **cascata** indica que a solicitação estava aguardando muito tempo.  Isso foi simulado usando um perfil para restringir a velocidade da rede e adicionar um atraso.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Um exemplo de uma solicitação com um tempo de demora para o primeiro byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Um exemplo de uma solicitação com um tempo de demora para o primeiro byte  
:::image-end:::  

**Causas**  

*   A conexão entre o cliente e o servidor está lenta.  
*   O servidor está lento para responder.  Hospede o servidor localmente para determinar se ele é a conexão ou o servidor que está lento.  Se você ainda receber um tempo lento para o primeiro byte \ (TTFB \) ao acessar um servidor local, então o servidor está lento.  
    
**Corrige**  

*   Se a conexão for lenta, considere hospedar o conteúdo em uma CDN ou alterar provedores de hospedagem.  
*   Se o servidor estiver lento, considere a otimização de consultas de banco de dados, a implementação de um cache ou a modificação da configuração do servidor.  
    
## Download de conteúdo lento   

**Sintomas**  

Uma solicitação demora muito tempo para baixar.  

Na figura a seguir, a barra azul longa na **cascata** ao lado do png significa que demorou muito tempo para baixar.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Um exemplo de uma solicitação que demora muito tempo para baixar" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Um exemplo de uma solicitação que demora muito tempo para baixar  
:::image-end:::  

**Causas**  

*   A conexão entre o cliente e o servidor está lenta.  
*   Uma grande quantidade de conteúdo está sendo baixada.  
    
**Corrige**  

*   Considere hospedar o conteúdo em uma CDN ou alterar provedores de hospedagem.  
*   Envie menos bytes otimizando suas solicitações.  
    
## Conhecimento do Contribute  

Você tem um problema de rede que deve ser adicionado a este guia?  

*   Envie um tweet para [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Selecione **enviar comentários** \ ( ![ enviar comentários ][ImageSendFeedbackIcon] \) no devtools ou pressione `Alt` + `Shift` + `I` \ (Windows \) ou `Option` + `Shift` + `I` \ (MacOS \) para fornecer comentários ou solicitações de recursos.  
*   [Abra um problema][WebFundamentalsIssue] no repositório de documentos.  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspecionar atividades de rede no Microsoft Edge DevTools | Documentos da Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Novo problema-MicrosoftDocs/Edge-Developer"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/network/issues) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \) e [Jonathan Garbee][JonathanGarbee] \ (Google Developer expert para tecnologia da Web \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
