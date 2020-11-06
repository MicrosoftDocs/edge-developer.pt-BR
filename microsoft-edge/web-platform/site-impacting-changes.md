---
description: Fornece um resumo das alterações de alto impacto que podem afetar a compatibilidade do site
title: Compatibilidade do site – alterações que afetam o Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web
ms.openlocfilehash: bb4d67bf1ab6274a10a83ee750fa9db52ab85464
ms.sourcegitcommit: 4497b399a6ddfa34163b7d3db4f76423d4da3c12
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/05/2020
ms.locfileid: "11156345"
---
# Compatibilidade do site – alterações que afetam o Microsoft Edge  

A Web está em constante evolução para melhorar a experiência do usuário, a segurança e a privacidade.  Em alguns casos, as alterações podem ser significativas o suficiente para afetar a funcionalidade de páginas existentes.  A tabela a seguir resume as alterações de impacto especialmente alto impacto que a equipe do Microsoft Edge está acompanhando no momento.  Leia este artigo com frequência; a equipe do Microsoft Edge atualiza a seguinte página conforme o raciocínio evolui, as linhas do tempo solidificam e novas alterações são anunciadas.  

| Alteração | Canal Estável | Experimentação | Informações adicionais |  
|:--- |:--- |:--- |:--- |
| Cookies padrão para `SameSite=Lax` e `SameSite=None-requires-Secure` | [Chrome + 1](#release-comments) \ (Edge v86 \)  | Canárias V82, dev V82 | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pela Google para essa alteração, navegue até a [entrada de status da plataforma Chrome][ChromePlatformStatus5088147346030592].  |  
| Política referenciadora: padrão para `strict-origin-when-cross-origin` | [Chrome + 1](#release-comments) \ (Edge v86 \)  | Canárias V79, dev V79 | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pela Google para essa alteração, navegue até a [entrada de status da plataforma Chrome][ChromePlatformStatus6251880185331712].  |  
| Não permitir síncrono `XmlHttpRequest` na destransmissão de página | [Chrome + 1](#release-comments) \ (Edge v83 \) |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Chrome compatível, o Microsoft Edge oferece uma política de grupo para desativar essa alteração até que o Edge V88.  Para obter mais informações, incluindo a linha do tempo planejada pela Google para essa alteração, navegue até a [entrada de status da plataforma Chrome][ChromePlatformStatus4664843055398912].  |  
| Exibir prompt sutil para solicitações de permissões de notificação | Borda v84 |  | Solicitações de notificação silenciosas exibem um ícone de solicitação sutil na barra de endereços para permissões de notificação de site solicitadas usando a `Notifications` `Push` API ou, substituindo a interface do usuário do prompt do submenu de permissão completa ou padrão.  Este recurso está habilitado no momento para todos os usuários.  Para recusar solicitações de notificação silenciosa, navegue até `edge://settings/content/notifications` .  No futuro, a equipe do Microsoft Edge pode explorar a reativação do prompt de notificação do submenu completo em alguns cenários.  |  
| Desativar TLS/1.0 e TLS/1.1 por padrão | Borda v84 |  | A política de grupo [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] permite a reativação do TLS/1.0 e do TLS/1.1; a política permanecerá disponível até o Edge V90.  |  
| Bloquear downloads de conteúdo misto | [Chrome + 1](#release-comments) \ (Edge v86 \)  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pela Google para essa alteração, navegue até a [entrada de blog do Google Security][GoogleBlogSecurity20200206].  O cronograma de distribuição da Microsoft em tipos de arquivo para avisar ou bloquear está planejado para um lançamento após o Chrome.  |  
| Substituir AppCache | [Chrome + 1](#release-comments) \ (Edge v86 \)  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, acesse a [documentação do webdev][WebDevAppCacheRemoval].  O cronograma de distribuição da Microsoft para substituição está planejado para um lançamento após o Chrome.  Solicitar um [token AppCache OriginTrial][AppCacheOriginTrial] permite que os sites continuem a usar a API substituída até que o Edge V90.  |  
| Remoção do Adobe Flash | Borda V88  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, navegue até o [mapa do Adobe Flash Chromium][ChromiumFlashRoadmapSupportRemoved].  | 
| Desativar e remover FTP | Borda V88  | Edge beta v87 | No v87 Edge beta, o suporte para FTP está desativado por padrão; em Edge stable v87 ele permanecerá habilitado.  No Edge V88, o suporte para FTP é totalmente removido.  Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, navegue até a [entrada de status da plataforma Chrome][ChromePlatformStatus6246151319715840].  As empresas que têm sites que ainda exigem suporte a FTP podem continuar a usar o FTP Configurando o site para usar o [modo IE](https://docs.microsoft.com/deployedge/edge-ie-mode).  |   

##### Comentários de versão  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      Com base nos comentários dos usuários e do desenvolvedor, o recurso ou a alteração indicadas envia uma versão após o Chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome ou Chrome + 1
   :::column-end:::
   :::column span="2":::
      Com base nos comentários do usuário e do desenvolvedor, o recurso ou a alteração indicada é enviado ao mesmo tempo ou um lançamento após o Chrome.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-Policies | Documentos da Microsoft"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Não permitir sincronização XHR no JavaScript descartar de página | Status da plataforma Chrome"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies padrão para SameSite = LAX | Status da plataforma Chrome"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Política referenciadora: padrão para a origem estrita-quando-entre origens | Status da plataforma Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Substituir suporte a FTP | Status da plataforma Chrome"

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Suporte a flash removido da Chromium (destino: Chrome 88 +-Jan 2021)-mapa de flash | Projetos Chromium"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protegendo os usuários contra downloads não seguros no Google Chrome-blog de segurança do Google online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal/ "Remoção de AppCache"
[AppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Token OriginTrial AppCache"

<!--todo:  cleanup links  -->  
