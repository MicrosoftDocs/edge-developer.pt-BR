---
description: Use o painel de segurança para garantir que uma página seja totalmente protegida por HTTPS.
title: Entender problemas de segurança com o Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 09f7e641ddd8da74c361980b9ce61b212a8477fe
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125381"
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
1.  Escolha a guia **segurança** para abrir o painel de **segurança** .  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-secure.msft.png":::
       O painel de **segurança**  
    :::image-end:::  
    
## Problemas comuns  

### Origens principais não seguras  

Quando a origem principal de uma página não é segura, a **visão geral da segurança** diz que **esta página não é segura**.  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Uma página não segura  
:::image-end:::  

Esse problema ocorre quando a URL que você visitou era solicitada por HTTP.  Para torná-lo seguro, você precisa solicitá-lo por HTTPS.  Por exemplo, se você olhar para a URL na barra de endereços, provavelmente ela terá uma aparência semelhante `http://example.com` .  Para torná-lo seguro, a URL deve estar `https://example.com` .  

Se você já configurou o HTTPS em seu servidor, tudo o que precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.  

Se você não configurou HTTPS em seu servidor, [vamos criptografar][LetsEncrypt] uma maneira gratuita e fácil de iniciar o processo.  Ou você pode considerar hospedar seu site em uma CDN.  A maioria dos principais sites de host do CDNs em HTTPS, por padrão, agora.  

> [!TIP]
> A dica [use HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de verificar se todas as solicitações HTTP são direcionadas para https.  

### Conteúdo misto  

**Conteúdo misto** significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.  Páginas de conteúdo misto são apenas parcialmente protegidas porque o conteúdo HTTP está acessível a farejadores e vulneráveis a ataques de Man-in-the-Middle.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Conteúdo misto  
:::image-end:::  

Na figura anterior, escolha **exibir uma solicitação no painel de rede** para abrir o painel de **rede** e aplicar o `mixed-content:displayed` filtro para que o **log de rede** mostre apenas os recursos não seguros.  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="O painel de segurança" lightbox="../media/security-network-filter.msft.png":::
   Recursos mistos no **log de rede**  
:::image-end:::  

## Exibir detalhes  

### Exibir certificado de origem principal  

Na **visão geral de segurança**, escolha **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Um certificado de origem principal  
:::image-end:::  

### Exibir detalhes da origem  

Clique em uma das entradas na barra de navegação à esquerda para exibir os detalhes da origem.  Na página detalhes, você pode exibir informações de conexão e certificado.  As informações sobre transparência do certificado também são mostradas quando disponíveis.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="O painel de segurança" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Detalhes da origem principal  
:::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  
[DevToolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  
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
