---
description: Saiba mais sobre como atualizar a extensão do manifesto v2 para v3
title: Preparar-se para atualizar as extensões do manifesto v2 para v3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, desenvolvimento de extensões, extensões de borda, extensões do navegador, Complementos, desenvolvedor, manifesto v3, migrar para o manifesto v3
ms.openlocfilehash: 262a5cab54dd23f596791c93ec1238619e247333
ms.sourcegitcommit: 1ad087b00df16fd7718a5d95226de57e29b335e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117823"
---
# Preparar-se para atualizar as extensões do manifesto v2 para v3 

Este documento lista as alterações importantes que estão sendo implementadas como parte do manifesto v3, que é a próxima versão da plataforma de extensões do Chromium. Atualizaremos este documento à medida que a implementação estiver em andamento. Para obter orientações detalhadas sobre como migrar sua extensão para o manifesto v3, navegue até [migrar para o manifesto v3][Google_Migrate_to_MV3]. 

## Código hospedado remotamente  

Hoje, as extensões podem hospedar partes do código remotamente, e não incluí-las como parte do pacote de extensão durante o processo de validação. Embora isso ofereça flexibilidade para alterar o código sem reenviar a extensão à loja, o código pode ser explorado após a instalação. Para garantir que os complementos do [Microsoft Edge][EdgeAddons] listem extensões validadas, não estamos permitindo que as extensões usem código hospedado remotamente. Essa alteração torna as extensões mais seguras. Os desenvolvedores precisarão empacotar e enviar todo o código usado pela extensão para a validação. Como alternativa, os desenvolvedores podem usar a função eval () em um [ambiente em área restrita][sandboxingEval]. 

## Permissões de host em tempo de execução  

No momento da instalação, as extensões podem solicitar permissões amplas para acessar todos os sites e conteúdo. Essas permissões permitem que as extensões operem com a intervenção mínima e criem um risco para a privacidade e a segurança do usuário. Para melhorar a transparência, estamos fornecendo controles para que os usuários permitam ou restringissem o acesso a sites em tempo de execução. 

## Solicitações entre origens em scripts de conteúdo  

Os scripts de conteúdo hoje podem solicitar acesso a qualquer origem, incluindo origens que não são permitidas pelo website. Esse comportamento divide os princípios de origem cruzada. No entanto, exige-se que os scripts de conteúdo tenham as mesmas permissões que a página que eles estão injetando, fechando um Loophole de segurança potencial. Para executar solicitações entre origens, você precisará usar scripts em segundo plano para redirecionar respostas para scripts de conteúdo. Essas alterações estão disponíveis e atrás de um sinalizador. Para obter mais informações, navegue até este [documento][CORS]. 

## API de solicitação da Web  

Estamos substituindo a [API de solicitação da Web][WebRequestAPI] pela [API declarativa de solicitação de rede][DeclarativeNetRequestAPI], mas continuará a manter os recursos de observação da API de solicitação da Web. Exceto em alguns cenários específicos em que os recursos de observação da API de solicitação da Web são exigidos pela extensão, recomendamos usar apenas as APIs DNR. Acreditamos que essa alteração terá um impacto positivo nas extensões que usam recursos declarativos avançados de recursos. À medida que mais extensões se transformam em APIs do DNR, essa alteração melhorará a privacidade do usuário, que contribui para melhorar a confiança no uso de extensões.
As empresas podem continuar a usar o comportamento de bloqueio da API de solicitação da Web para extensões gerenciadas por meio de políticas corporativas. Para obter mais informações sobre as políticas de extensão, navegue até [Microsoft Edge – políticas][MicrosoftEdgePolicies]. 

## Trabalhadores de serviço em segundo plano  
 
Os funcionários de serviço estão disponíveis para teste no Canárias. Para migrar suas extensões de páginas de plano de fundo para trabalhadores do serviço, consulte [migrando de páginas de plano de fundo para trabalhadores do serviço][ServiceWorkers]. Estamos avaliando & investigando o impacto que essa alteração traz para desenvolvedores e usuários. Vamos adicionar mais detalhes sobre essa alteração para este documento no futuro. 

## Quando essas alterações estarão disponíveis no Microsoft Edge?

A implementação da API de solicitação líquida da rede atual está disponível em nossos canais estáveis e beta. Os desenvolvedores podem testar essas alterações e fornecer comentários. Vamos contribuir para os esforços de desenvolvimento e investigar outras alterações. 

| Nome do canal | Descrição |
|:--- |:--- |  
| Microsoft Edge 84 estável | A API DNR está disponível para teste |  
| Microsoft Edge 85 beta | O suporte à modificação de cabeçalho está disponível| 

Quando as alterações são feitas no Chromium, compartilhamos cronogramas para que os desenvolvedores possam atualizar seu código e republicar extensões na loja. 

Continuaremos a publicação de atualizações em nosso blog. Você pode enviar seus comentários sobre essas alterações por meio do [TechCommunity][TechCommunity].

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/ "Complementos do Microsoft Edge"  
[MicrosoftBlog]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/  
[MicrosoftEdgePolicies]: https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions 

[TechCommunity]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Comunidade técnica"  


[Google_Migrate_to_MV3]: https://developer.chrome.com/extensions/migrating_to_manifest_v3   
[SandboxingEval]: https://developer.chrome.com/apps/sandboxingEval "Usar eval em extensões Chrome. Com segurança."
[CORS]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Alterações em solicitações entre origens em scripts de conteúdo de extensão"
[WebRequestAPI]: https://developer.chrome.com/extensions/webRequest "API de solicitação da Web"  
[DeclarativeNetRequestAPI]: https://developer.chrome.com/extensions/declarativeNetRequest/ "API de solicitação de rede declarativa"
[ServiceWorkers]:  https://developers.chrome.com/extensions/migrating_to_service_workers


