---
description: Fornece um resumo das alterações de alto impacto que podem afetar a compatibilidade do site
title: Compatibilidade do site – alterações que afetam o Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web
ms.openlocfilehash: 64cdb417e6bd0aa648c7e1225bb6dc522f3873ce
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327502"
---
# Compatibilidade do site – alterações que afetam o Microsoft Edge  

A Web está em constante evolução para melhorar a experiência do usuário, a segurança e a privacidade.  Em alguns casos, as alterações podem ser significativas o suficiente para afetar a funcionalidade das páginas existentes.  A tabela a seguir resume as alterações particularmente de alto impacto que a equipe do Microsoft Edge está acompanhando no momento.  Revise este artigo com frequência; a equipe do Microsoft Edge atualiza a página a seguir à medida que pensa em evolução, as linhas do tempo se solidificam e novas alterações são anunciadas.  

| Alteração | Canal Estável | Experimentação | Informações adicionais |  
|:--- |:--- |:--- |:--- |
| Cookies padrão para `SameSite=Lax` e `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada [de Status da Plataforma Chrome.][ChromePlatformStatus5088147346030592]  |  
| Política de Referência: Padrão para `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada [de Status da Plataforma Chrome.][ChromePlatformStatus6251880185331712]  |  
| Não permitir síncrono no `XmlHttpRequest` dismissal de página | [Chrome+1](#release-comments) \(Edge v83\) |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Correspondente ao Chrome, o Microsoft Edge oferece uma Política de Grupo para desativar essa alteração até o Edge v88.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada [de Status da Plataforma Chrome.][ChromePlatformStatus4664843055398912]  |  
| Exibir prompt sutil para solicitações de permissões de notificação | Edge v84 |  | As solicitações de notificação silenciosa exibem um ícone de solicitação sutil na barra de endereços para permissões de notificação do site solicitadas usando a API ou a API, substituindo a interface do usuário do prompt de sub-menu de permissão completo ou `Notifications` `Push` padrão.  No momento, esse recurso está habilitado para todos os usuários.  Para não receber solicitações de notificação silenciosas, navegue até `edge://settings/content/notifications` .  No futuro, a equipe do Microsoft Edge poderá explorar a rehabilitação do prompt de notificação do sub-sub-limite completo em alguns cenários.  |  
| Desativar TLS/1.0 e TLS/1.1 por padrão | Edge v84 |  | A [Política de Grupo SSLMinVersion][DeployedgeMicrosoftEdgePoliciesSslversionmin] permite a rehabilitação de TLS/1.0 e TLS/1.1; a política permanece disponível até o Edge v90.  |  
| Bloquear downloads de conteúdo misto | [Chrome+1](#release-comments) \(Edge v86\)  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada do blog de [segurança do Google.][GoogleBlogSecurity20200206]  O cronograma de lançamento da Microsoft sobre tipos de arquivo para avisar ou bloquear está planejado para uma versão após o Chrome.  |  
| Preterir AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, navegue até a [documentação webDev][WebDevAppCacheRemoval].  O cronograma de lançamento da Microsoft para preterição está planejado para uma versão após o Chrome.  Solicitar um [Token OriginTrial appCache][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permite que os sites continuem a usar a API preterida até o Edge v90.  |  
| Remoção do Adobe Flash | Edge v88  |  | Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, navegue até o [mapa do Adobe Flash Chromium.][ChromiumFlashRoadmapSupportRemoved]  | 
| Desativar e remover FTP | Edge v88  | Edge Beta v87 | Na Borda Beta v87, o suporte a FTP está desligado por padrão; no Edge Stable v87, ele permanece habilitado.  No Edge v88, o suporte a FTP foi completamente removido.  Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado.  Para obter mais informações, navegue até a entrada de [status da plataforma Chrome.][ChromePlatformStatus6246151319715840]  As empresas que têm sites que ainda exigem suporte a FTP podem continuar a usar FTP configurando o site para usar o [modo IE.][DeployedgeEdgeIeMode]  | 
| Atualizar automaticamente imagens de conteúdo misto | Edge v88  |  | Referências \(HTTP\) não seguras para imagens são atualizadas automaticamente para HTTPS; se a imagem não estiver disponível em HTTPS, o download da imagem falhará. Uma [Política de][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] Grupo está disponível para controlar esse recurso. Essa alteração está acontecendo no projeto Chromium, no qual o Microsoft Edge é baseado. Para obter mais informações, navegue até a entrada [de Status da Plataforma Chrome.][ChromePlatformStatus4926989725073408]  | 
| Autenticação HTTP não permitido quando cookies de terceiros são bloqueados  | Edge v87  |  | A partir do Edge v87, quando os cookies são bloqueados para solicitações de terceiros, usando a política [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] ou por meio da página Configurações de Borda, a autenticação HTTP também não é permitido. Essa alteração poderá afetar os [downloads][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] da Lista de Sites do Modo Empresarial para o modo Internet Explorer se o ponto de extremidade que hospeda a lista exigir o uso da autenticação HTTP.  Para permitir o uso de cookies e autenticação HTTP para downloads de Lista de Sites do Modo Empresarial, adicione um padrão de URL correspondente à [política CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |   

##### Comentários de versão  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      Com base nos comentários dos usuários e desenvolvedores, o recurso indicado ou a alteração é lançado uma versão após o Chrome.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome ou Chrome+1  
   :::column-end:::
   :::column span="2":::
      Com base nos comentários dos usuários e desenvolvedores, o recurso indicado ou a alteração é lançado ao mesmo tempo ou em uma versão após o Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Sobre o modo IE | Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configurar usando a política usar a lista de site do IE do modo Empresarial - Configurar políticas do modo IE | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Políticas | Microsoft Docs"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Não permitir o XHR de sincronização no JavaScript de página | Status da plataforma Chrome"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Autoupgrade Image Mixed Content | Status da plataforma Chrome"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Cookies padrão para SameSite=| Status da plataforma Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Desaprecatar o suporte a FTP | Status da plataforma Chrome"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Política de referência: padrão para o formato strict-origin-when-cross-origin | Status da plataforma Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Suporte a flash removido do Chromium (destino: Chrome 88+ - janeiro de 2021) - mapa do Flash | Projetos Chromium"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Token AppCache OriginTrial | Desenvolvedores do Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protegendo os usuários contra downloads inseguros no Google Chrome - Blog de Segurança do Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Preparação para a remoção do AppCache | web.dev"  

<!--todo:  cleanup links  -->  
