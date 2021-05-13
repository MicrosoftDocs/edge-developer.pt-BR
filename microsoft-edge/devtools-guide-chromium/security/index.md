---
description: Use o Painel de Segurança para garantir que uma página seja totalmente protegida por HTTPS.
title: Compreender problemas de segurança com Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 2e6aab865319e6ed7d108cddb77432f293153995
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565033"
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
# <a name="understand-security-issues-with-microsoft-edge-devtools"></a>Compreender problemas de segurança com Microsoft Edge DevTools  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a>Abra o painel Segurança  

O **painel** Segurança é o principal local no DevTools para inspecionar a segurança de uma página.  

1.  [Abra DevTools][DevToolsOpen].  
1.  Escolha a **guia Segurança** para abrir a **ferramenta Segurança.**  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="O painel Segurança" lightbox="../media/security-security-overview-secure.msft.png":::
       O **painel Segurança**  
    :::image-end:::  
    
## <a name="common-problems"></a>Problemas comuns  

### <a name="non-secure-main-origins"></a>Origens principais não seguras  

Quando a origem principal de uma página não é segura, a Visão Geral de Segurança **diz** que esta página não **é segura**.  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Uma página não segura" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Uma página não segura  
:::image-end:::  

Esse problema ocorre quando a URL que você visitou foi solicitada por HTTP.  Para torná-lo seguro, você precisa solicitá-lo por HTTPS.  Por exemplo, se você olhar para a URL na barra de endereços, provavelmente será semelhante a `http://example.com` .  Para torná-la segura, a URL deve ser `https://example.com` .  

Se você já configurou HTTPS em seu servidor, tudo o que você precisa fazer para corrigir esse problema é configurar seu servidor para redirecionar todas as solicitações HTTP para HTTPS.  

Se você não tiver definido HTTPS em seu servidor, [Vamos][LetsEncrypt] Criptografar fornece uma maneira gratuita e relativamente fácil de iniciar o processo.  Ou você pode considerar hospedar seu site em um CDN.  A maioria dos principais sites de host de CDNs em HTTPS por padrão agora.  

> [!TIP]
> A [dica Usar HTTPS][WebhintUseHttps] na [webhint][Webhint] pode ajudar a automatizar o processo de garantir que todas as solicitações HTTP sejam direcionadas para HTTPS.  

### <a name="mixed-content"></a>Conteúdo misto  

**O conteúdo** misto significa que a origem principal de uma página é segura, mas a página solicitou recursos de origens não seguras.  Páginas de conteúdo misto só são parcialmente protegidas porque o conteúdo HTTP é acessível a farejadores e vulnerável a ataques de homem no meio.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Conteúdo misto" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Conteúdo misto  
:::image-end:::  

Na figura anterior, escolha **Exibir uma** solicitação **** no painel Rede para abrir a ferramenta Rede e aplicar o filtro para que o Log de Rede mostre apenas recursos `mixed-content:displayed` não seguros. ****  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Recursos mistos no Log de Rede" lightbox="../media/security-network-filter.msft.png":::
   Recursos mistos no **Log de Rede**  
:::image-end:::  

## <a name="view-details"></a>Exibir detalhes  

### <a name="view-main-origin-certificate"></a>Exibir certificado de origem principal  

Na Visão **Geral de**Segurança, escolha **Exibir certificado** para inspecionar rapidamente o certificado para a origem principal.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Um certificado de origem principal" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Um certificado de origem principal  
:::image-end:::  

### <a name="view-origin-details"></a>Exibir detalhes de origem  

Escolha uma das entradas na nav à esquerda para exibir os detalhes da origem.  Na página de detalhes, você pode exibir informações de conexão e certificado.  As informações de transparência do certificado também são mostradas quando disponíveis.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Detalhes de origem principal" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Detalhes de origem principal  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Ferramentas de desenvolvedor | Microsoft Docs"  
[DevToolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[LetsEncrypt]: https://letsencrypt.org "Vamos criptografar - certificados SSL/TLS gratuitos"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Use HTTPS | documentação webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/security/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
