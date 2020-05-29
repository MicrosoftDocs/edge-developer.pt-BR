---
title: Entender problemas de segurança com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611907"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Entender problemas de segurança com o Microsoft Edge DevTools   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Abrir o painel de segurança   

O painel de **segurança** é o local principal no devtools para inspecionar a segurança de uma página.  

1.  [Abra o devtools][DevToolsOpen].  

1.  Clique na guia **segurança** para abrir o painel **segurança** .  
    
    > ##### Figura 1  
    > O painel de segurança  
    > ![O painel de segurança][ImageSecurityPanel]  
    
## Problemas comuns   

### Origens principais não seguras   

Quando a origem principal de uma página não é segura, a **visão geral da segurança** diz que **esta página não é segura**.  

> ##### Figura 2  
> Uma página não segura  
> ![Uma página não segura][ImageNonSecurePage]  

Esse problema ocorre quando a URL que você visitou era solicitada por HTTP.  Para torná-lo seguro, você precisa solicitá-lo por HTTPS.  Por exemplo, se você olhar para a URL na barra de endereços, provavelmente ela terá uma aparência semelhante `http://example.com` .  Para torná-lo seguro, a URL deve estar `https://example.com` .  

Se você já configurou o HTTPS em seu servidor, tudo o que precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.  

Se você não configurou HTTPS em seu servidor, [vamos criptografar][LetsEncrypt] uma maneira gratuita e fácil de iniciar o processo.  Ou você pode considerar hospedar seu site em uma CDN.  A maioria dos principais sites de host do CDNs em HTTPS, por padrão, agora.  

> [!TIP]
> A dica [use HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de verificar se todas as solicitações HTTP são direcionadas para https.  

### Conteúdo misto   

**Conteúdo misto** significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.  Páginas de conteúdo misto são apenas parcialmente protegidas porque o conteúdo HTTP está acessível a farejadores e vulneráveis a ataques de Man-in-the-Middle.  

> ##### Figura 3  
> Conteúdo misto  
> ![Conteúdo misto][ImageMixedContent]  

Na [Figura 3](#figure-3), clique em **Exibir 1 solicitação no painel de rede** para abrir o painel de **rede** e aplicar o `mixed-content:displayed` filtro para que o **log de rede** mostre apenas os recursos não seguros.  

> ##### Figura 4  
> Recursos mistos no log de rede  
> ![Recursos mistos no log de rede][ImageMixedResourcesNetworkLog]  

## Exibir detalhes   

### Exibir certificado de origem principal   

Na **visão geral de segurança**, clique em **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.  

> ##### Figura 5  
> Um certificado de origem principal  
> ![Um certificado de origem principal][ImageCertificate]  

### Exibir detalhes da origem   

Clique em uma das entradas na barra de navegação à esquerda para exibir os detalhes da origem.  Na página detalhes, você pode exibir informações de conexão e certificado.  As informações sobre transparência do certificado também são mostradas quando disponíveis.  

> ##### Figura 6  
> Detalhes da origem principal  
> ![Detalhes da origem principal][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Figura 1: o painel de segurança"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Figura 2: uma página não segura"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Figura 3: conteúdo misto"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Figura 4: recursos mistos no log de rede"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Figura 5: certificado de origem principal"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Figura 6: detalhes da origem principal"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir o Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Vamos criptografar certificados SSL/TLS grátis"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Usar HTTPS | documentação do webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/security/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
