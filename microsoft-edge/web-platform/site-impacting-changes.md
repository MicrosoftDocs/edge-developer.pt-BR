---
description: Esta página fornece um resumo das alterações de alto impacto que podem afetar a compatibilidade do site
title: Compatibilidade do site – alterações que afetam o Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidade, plataforma da Web
ms.openlocfilehash: 6a57ffb4a2c36420d1abe4ec151342e5b77d4c7c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752189"
---
# Compatibilidade do site – alterações que afetam o Microsoft Edge  

A Web está em constante evolução para melhorar a experiência do usuário, a segurança e a privacidade.  Em alguns casos, as alterações podem ser significativas o suficiente para afetar a funcionalidade de páginas existentes.  A tabela a seguir resume as mudanças de impacto especialmente altos que a equipe do Microsoft Edge está acompanhando no momento.  Verifique com frequência; a equipe do Microsoft Edge atualiza esta página conforme a evolução, as linhas do tempo solidificam e novas alterações são anunciadas.  

| Alteração | Canal Estável | Experimentação | Informações adicionais |  
|:--- |:--- |:--- |:--- |
| Cookies padrão para `SameSite=Lax` | [Chrome ou Chrome + 1](#release-comments)  | Canárias V82, dev V82 | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pela Google, consulte a [entrada de status da plataforma Chrome][ChromePlatformStatus5088147346030592].  |  
| Política referenciadora: padrão para `strict-origin-when-cross-origin` | [Chrome ou Chrome + 1](#release-comments)  | Canárias V79, dev V79 | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pela Google, consulte a [entrada de status da plataforma Chrome][ChromePlatformStatus6251880185331712].  |  
| Não permitir XMLHttpRequest síncrono na notação de página | [Chrome + 1](#release-comments) \ (Edge v83 \) |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Chrome compatível, o Microsoft Edge oferece uma política de grupo para desabilitar essa alteração até que o Edge 88.  Para obter mais informações, incluindo a linha do tempo planejada pela Google, consulte a [entrada de status da plataforma Chrome][ChromePlatformStatus4664843055398912].  |  
| Exibir prompt sutil para solicitações de permissões de notificação |  | Canárias v83, dev v83 | Agora os usuários podem optar por aceitar solicitações de notificação em silêncio `edge://settings/content/notifications` .  Com essa configuração habilitada, o Microsoft Edge exibe um ícone de solicitação sutil na barra de endereços para os sites que solicitam o envio de usuários futuras notificações usando a `Notifications` `Push` API ou.  Este ícone sutil substitui o prompt de permissão de submenu.  Um experimento em Canárias e dev ativa esse comportamento por padrão para alguns usuários, em todos os sites que solicitam permissões de notificações.  Os usuários podem recusar-se `edge://settings/content/notifications` .  No futuro, a equipe do Microsoft Edge pode explorar a exibição do prompt de submenu em situações específicas com base em comportamentos do usuário e outras entradas.  |  
| Desabilitar TLS/1.0 e TLS/1.1 por padrão | Borda v84 |  | Para ajudar a descobrir os sites afetados, você pode definir o `edge://flags/#display-legacy-tls-warnings` sinalizador para fazer com que o Microsoft Edge exiba um aviso de "não seguro" não bloqueado ao carregar páginas que exijam protocolos TLS herdados.  A política de grupo [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] permite a reativação do TLS/1.0 e do TLS/1.1; a política permanecerá disponível até o Edge 88.  |  
| Bloquear downloads de conteúdo misto | [Chrome + 1](#release-comments) \ (Edge V85 \)  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pela Google, consulte a [entrada no blog do Google Security][GoogleBlogSecurity20200206].  O cronograma de distribuição da Microsoft em tipos de arquivo para avisar ou bloquear está planejado para um lançamento após o Chrome.  |  
| Remoção do Adobe Flash | Borda V88  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, consulte o [mapa do Adobe Flash Chromium](https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021-).  | 
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


<!-- image links -->  

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-políticas"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Não permitir sincronização XHR no navegador desliberado de página-status da plataforma Chrome"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies padrão para SameSite = LAX-status da plataforma Chrome"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Política referenciadora: padrão para status da plataforma de origem estrita-quando-entre origens – do Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protegendo os usuários contra downloads não seguros no Google Chrome-blog de segurança do Google online"  
