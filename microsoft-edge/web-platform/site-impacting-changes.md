---
description: Fornece um resumo das alterações de alto impacto que podem afetar a compatibilidade do site
title: Compatibilidade do site – alterações que afetam o Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidade, plataforma Web
ms.openlocfilehash: 810c4e0a3e4c719987fbc374330599a58f055166
ms.sourcegitcommit: bbbf722067f1d255f59ab384e66798f8b77ef609
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2021
ms.locfileid: "11574572"
---
# <a name="site-compatibility-impacting-changes-coming-to-microsoft-edge"></a>Compatibilidade do site – alterações que afetam o Microsoft Edge  

A Plataforma Web é uma coleção de tecnologias usadas para a criação de páginas da Web.  As tecnologias incluem HTML, CSS, JavaScript e muitos outros padrões abertos.  A Plataforma Web constantemente evolui para melhorar a experiência do usuário, a segurança e a privacidade.  Em alguns casos, as alterações podem afetar a funcionalidade de páginas da Web existentes.  Para obter mais informações sobre as próximas Chromium da plataforma Web do projeto, navegue até [Chrome Platform Status Release timeline][ChromestatusFeaturesSchedule].  

Microsoft Edge adota quase todas as alterações de upstream na plataforma Web a partir do Chromium projeto.  Os motivos incluem a funcionalidade e os motivos de compatibilidade.  A Microsoft permanece no controle total do navegador Microsoft Edge e pode adiar ou rejeitar alterações.  A equipe Microsoft Edge decidir se a alteração beneficia os usuários do navegador.  Áreas de recursos Microsoft Edge planos de desvio de Chromium alterações no tempo ou no comportamento são notadas na tabela a seguir.  A tabela também destaca as alterações de alto impacto que a equipe Microsoft Edge está acompanhando.  

Revise este artigo com frequência.  A Microsoft Edge atualiza este artigo à medida que o raciocínio evolui, as linhas do tempo se solidificam e novas alterações são anunciadas.  

| Alterar | Canal Estável | Experimentação | Informações adicionais |  
|:--- |:--- |:--- |:--- |
| Cookies padrão `SameSite=Lax` para e `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada Status da Plataforma [Chrome.][ChromestatusFeature5088147346030592]  |  
| Política do Referrer: Padrão para `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada Status da Plataforma [Chrome.][ChromestatusFeature6251880185331712]  |  
| Não permitir síncrono na `XmlHttpRequest` demissão de página | [Chrome+1](#release-comments) \(Edge v83\) |  | Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Correspondente ao Chrome, Microsoft Edge oferece uma Política de Grupo para desativar essa alteração até o Edge v88.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada Status da Plataforma [Chrome.][ChromestatusFeature4664843055398912]  |  
| Exibir prompt sutil para solicitações de permissões de notificação | Edge v84 |  | As solicitações de notificação silenciosa exibem um ícone de solicitação sutil na barra de endereços para permissões de notificação de site solicitadas usando a API ou a API, substituindo a interface do usuário do prompt de sublinhado de permissão completa ou `Notifications` `Push` padrão.  Esse recurso está habilitado no momento para todos os usuários.  Para não fazer solicitações de notificação silenciosa, navegue até `edge://settings/content/notifications` .  No futuro, a equipe de Microsoft Edge pode explorar a rehabilitação do prompt de notificação de sublagem completa em alguns cenários.  |  
| Desativar o TLS/1.0 e o TLS/1.1 por padrão | Edge v84 |  | A [Política de Grupo SSLMinVersion][DeployedgeMicrosoftEdgePoliciesSslversionmin] permite a rehabilitação de TLS/1.0 e TLS/1.1; a política permanece disponível até Edge v90.  |  
| Bloquear downloads de conteúdo misto | [Chrome+1](#release-comments) \(Edge v86\)  |  | Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Para obter mais informações, incluindo a linha do tempo planejada pelo Google para essa alteração, navegue até a entrada do [blog de segurança do Google.][GoogleBlogSecurity20200206]  A agenda de lançamento da Microsoft em tipos de arquivo para avisar ou bloquear é planejada para uma versão após o Chrome.  |  
| Deprecate AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Para obter mais informações, navegue até a [documentação webDev][WebDevAppCacheRemoval].  O cronograma de lançamento da Microsoft para o deprecamento está planejado para uma versão após o Chrome.  Solicitar um [Token AppCache OriginTrial][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permite que os sites continuem a usar a API preterida até o Edge v90.  |  
| Remoção do Adobe Flash | Edge v88  |  | Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Para obter mais informações, navegue até o Mapa do [Adobe Flash Chromium][ChromiumFlashRoadmapSupportRemoved].  | 
| Desativar e remover FTP | Edge v88  | Edge Beta v87 | No Edge Beta v87, o suporte a FTP é desligado por padrão; no Edge Stable v87, ele permanece habilitado.  No Edge v88, o suporte a FTP é totalmente removido.  Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia.  Para obter mais informações, navegue até a Entrada de [Status da Plataforma Chrome.][ChromestatusFeature6246151319715840]  As empresas que têm sites que ainda exigem suporte a FTP podem continuar a usar o FTP configurando o site para usar o [modo IE][DeployedgeEdgeIeMode].  | 
| Atualizar automaticamente imagens de conteúdo misto | Edge v88  |  | Referências não seguras \(HTTP\) às imagens são atualizadas automaticamente para HTTPS; se a imagem não estiver disponível em HTTPS, o download da imagem falhará. Uma [Política de][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] Grupo está disponível para controlar esse recurso. Essa alteração está ocorrendo no projeto Chromium, no qual Microsoft Edge se baseia. Para obter mais informações, navegue até a entrada [Status da Plataforma Chrome.][ChromestatusFeature4926989725073408]  | 
| Autenticação HTTP não permitido quando cookies de terceiros são bloqueados  | Edge v87  |  | A partir do Edge v87, quando os cookies são bloqueados para solicitações de terceiros, usando a política [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] ou por meio da página Configurações Edge, a autenticação HTTP também é vetada. Essa alteração pode afetar Enterprise [downloads][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] da Lista de Sites do Modo para o Modo Internet Explorer se o ponto de extremidade que hospeda a lista exigir o uso da autenticação HTTP.  Para permitir o uso de cookies e autenticação HTTP para downloads Enterprise Lista de Sites do Modo, adicione um padrão de URL correspondente à [política CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |   

##### <a name="release-comments"></a>Comentários de versão  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      Com base nos comentários do usuário e do desenvolvedor, o recurso indicado ou a alteração envia uma versão após o Chrome.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome ou Chrome+1  
   :::column-end:::
   :::column span="2":::
      Com base nos comentários do usuário e do desenvolvedor, o recurso indicado ou a alteração é lançado ao mesmo tempo ou uma versão após o Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Sobre o modo IE | Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configurar usando a política usar a política de lista de site do IE do modo Enterprise - Configurar políticas de modo IE | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Políticas | Microsoft Docs"  

[ChromestatusFeaturesSchedule]: https://www.chromestatus.com/features/schedule "Linha do tempo de lançamento | Status da plataforma Chrome"  
[ChromestatusFeature4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Não permitir a sincronização XHR no JavaScript de página | Status da plataforma Chrome"  
[ChromestatusFeature4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Autoupgrade Image Mixed Content | Status da plataforma Chrome"  
[ChromestatusFeature5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Cookies padrão para SameSite=Lax | Status da plataforma Chrome"  
[ChromestatusFeature6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Deprecate o suporte a FTP | Status da plataforma Chrome"  
[ChromestatusFeature6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Política de referência: Padrão para estrito-origin-when-cross-origin | Status da plataforma Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Suporte a Flash Removido do Chromium (Destino: Chrome 88+ - Jan 2021) - Mapa do Flash | Chromium Projects"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Token AppCache OriginTrial | Desenvolvedores do Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protegendo os usuários contra downloads inseguros no Google Chrome - Blog de Segurança do Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Preparando-se para a remoção do AppCache | web.dev"  

<!--todo:  cleanup links  -->  
