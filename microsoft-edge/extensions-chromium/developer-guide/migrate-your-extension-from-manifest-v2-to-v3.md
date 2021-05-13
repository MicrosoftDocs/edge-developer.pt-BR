---
description: Saiba mais sobre como atualizar sua extensão do Manifesto V2 para v3
title: Preparar para atualizar suas extensões do Manifesto V2 para a V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de borda, extensões de navegador, complementos, desenvolvedor, manifesto v3, migrar para manifesto v3
ms.openlocfilehash: 5aa1aa7446a312d581bacc4fa19ba7362c6c2a3e
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564613"
---
# <a name="prepare-to-update-your-extensions-from-manifest-v2-to-v3"></a>Preparar para atualizar suas extensões do Manifesto v2 para v3  

Este documento lista alterações importantes que estão sendo implementadas como parte do Manifesto v3, que é a próxima versão da plataforma Chromium Extensões.  A Microsoft Edge de extensões atualiza este documento à medida que a implementação progride.  Para obter orientações detalhadas sobre como migrar sua extensão para Manifesto v3, navegue até [Migrando para Manifesto V3][ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist].  

## <a name="remotely-hosted-code"></a>Código hospedado remotamente  

Atualmente, partes do código de extensões são hospedadas remotamente e não o incluem como parte do pacote de extensão durante o processo de validação.  Embora isso ofereça flexibilidade para alterar o código sem reemitir a extensão para o armazenamento, o código pode ser explorado após a instalação.  Para garantir Microsoft Edge listas de [complementos][MicrosoftMicrosoftedgeAddons] validadas, a equipe de Microsoft Edge de extensões não permite que as extensões usem código hospedado remotamente.  Essa alteração torna as extensões mais seguras.  Os desenvolvedores precisarão empacotar e enviar todo o código usado pela extensão para validação.  Como alternativa, você pode usar `eval()` a função em um ambiente em [áreas de segurança][ChromeDeveloperDocsExtensionsMv2Sandboxingeval].  

## <a name="run-time-host-permissions"></a>Permissões de host em tempo de executar  

No momento da instalação, as extensões podem solicitar permissões de proteção para acessar todos os sites e conteúdo.  Essas permissões permitem que as extensões operem com intervenção mínima e criem um risco para a privacidade e a segurança do usuário.  Para melhorar a transparência, a Microsoft Edge de extensões fornece controles para que os usuários permitam ou restrinjam o acesso a sites em tempo de execução.  

## <a name="cross-origin-requests-in-content-scripts"></a>Solicitações de origem cruzada em scripts de conteúdo  

Hoje, os scripts de conteúdo solicitam acesso a qualquer origem, incluindo origens que não são permitidas pelo site.  O comportamento quebra princípios de origem cruzada.  Em frente, a Microsoft Edge de extensões exige que os scripts de conteúdo tenham as mesmas permissões da página da Web na qual os scripts são injetados, fechando uma possível lacuna de segurança.  Para executar solicitações de origem cruzada, você precisa usar scripts em segundo plano para retransmitir respostas de volta aos scripts de conteúdo.  Essas alterações estão disponíveis e atrás de um sinalizador.  Para obter mais informações, navegue até este [documento][ChromiumHomeChromiumSecurityExtensionContentScriptFetches].  

## <a name="web-request-api"></a>API de Solicitação da Web  

A Microsoft Edge de extensões substitui a API de Solicitação da Web pela [API][ChromeDeveloperDocsExtensionsReferenceWebrequest] de Solicitação [Líquida][ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]Declarativa , mas continua a manter os recursos observacionais da API de Solicitação da Web.  Exceto em alguns cenários específicos em que os recursos observacionais da API de Solicitação da Web são necessários pela extensão, a equipe de extensões Microsoft Edge recomenda usar apenas as APIs DNR.  A Microsoft Edge de extensões acredita que essa alteração terá impacto positivo em extensões que usam recursos declarativos avançados.  À medida que mais extensões são transições para as APIs DNR, essa alteração melhorará a privacidade do usuário, o que contribui para aumentar a confiança no uso de extensões.  
As empresas podem continuar a usar o comportamento de bloqueio da API de Solicitação da Web para extensões gerenciadas por meio de políticas corporativas.  Para obter mais informações sobre políticas de extensão, navegue [até Microsoft Edge – Políticas][DeployedgeMicrosoftEdgePoliciesExtensions].  

## <a name="background-service-workers"></a>Funcionários de serviço em segundo plano  
 
Os funcionários do serviço estão disponíveis para teste no Canary.  Para migrar suas extensões de páginas em segundo plano para os funcionários do serviço, consulte [Migrating from Background Pages to Service Workers][ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers].  A Microsoft Edge de extensões está avaliando e investigando o impacto que essa alteração traz para desenvolvedores e usuários.  A Microsoft Edge de extensões adiciona detalhes adicionais sobre a alteração a este documento no futuro.  

## <a name="when-are-these-changes-available-in-microsoft-edge"></a>Quando essas alterações estão disponíveis no Microsoft Edge  

A implementação da API de solicitação líquida declarativa atual está disponível em nossos canais Estável e Beta.  Teste as alterações e forneça comentários.  A Microsoft Edge de extensões contribui para os esforços de desenvolvimento e investiga outras alterações.  

| Nome do canal | Detalhes |  
|:--- |:--- |  
| Microsoft Edge estável 84 | A API DNR está disponível para teste |  
| Microsoft Edge 85 Beta | O suporte à modificação do header está disponível|  

Quando as alterações são feitas no Chromium, a equipe de Microsoft Edge extensões compartilha linhas do tempo para que você possa atualizar seu código e republicar extensões na loja.  

A Microsoft Edge de extensões continua publicando atualizações no blog.  Você pode fornecer seus comentários sobre as alterações por meio [do Tech Community][MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254].

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesExtensions]: /deployedge/microsoft-edge-policies#extensions "Extensões - Microsoft Edge - Políticas | Microsoft Docs"  

[MicrosoftMicrosoftedgeAddons]: https://microsoftedge.microsoft.com/addons "Microsoft Edge Complementos"  

[MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "As alterações do Manifesto V3 agora estão disponíveis no Microsoft Edge | Microsoft Tech Community"  

[ChromeDeveloperDocsExtensionsMv2Sandboxingeval]: https://developer.chrome.com/docs/extensions/mv2/sandboxingEval "Usando a avaliação em extensões do Chrome | Desenvolvedores do Chrome"  
[ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers]:  https://developer.chrome.com/docs/extensions/mv3/migrating_to_service_workers "Migrando de páginas em segundo plano para funcionários de serviço | Desenvolvedores do Chrome"  
[ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist]: https://developer.chrome.com/docs/extensions/mv3/mv3-migration-checklist "Lista de verificação de migração de manifesto V3 | Desenvolvedores do Chrome"    

[ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]: https://developer.chrome.com/docs/extensions/reference/declarativeNetRequest "chrome.declarativeNetRequest | Desenvolvedores do Chrome"  
[ChromeDeveloperDocsExtensionsReferenceWebrequest]: https://developer.chrome.com/docs/extensions/reference/webRequest "chrome.webRequest | Desenvolvedores do Chrome"  

[ChromiumHomeChromiumSecurityExtensionContentScriptFetches]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Alterações nas solicitações de origem cruzada em scripts de conteúdo de extensão do Chrome | Os Chromium projetos"  
