---
description: Hospedar e publicar extensões na empresa para o Microsoft Edge (Chromium).
title: Publicar e atualizar extensões no armazenamento de Complementos do Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 91fdd5c2f625890653085e8999da3e513b072348
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327684"
---
# Publicar e atualizar extensões no armazenamento de Complementos do Microsoft Edge  

A maioria das extensões são [publicadas no armazenamento de Complementos][MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions] do Microsoft Edge para proteger os usuários contra extensões mal-intencionadas.  

## Opções de publicação para extensões  

Todas as extensões são distribuídas aos usuários como um arquivo morto especial \( `.zip` \) com `.crx` um sufixo.  As extensões publicadas no armazenamento de Complementos do Microsoft Edge são carregadas como `.zip` arquivos.  O processo de publicação converte automaticamente `.zip` o arquivo em um `.crx` arquivo.  

Os dois cenários a seguir não exigem que você publique sua extensão no armazenamento de Complementos do Microsoft Edge.  

*   Extensões distribuídas usando a política Enterprise.  
*   Usar diretórios de extensão não descompactados em um computador local quando o Microsoft Edge está no modo de desenvolvedor.  

## Atualizações para extensões

O navegador Microsoft Edge verifica periodicamente se há novas versões de extensões instaladas e atualiza cada uma sem a intervenção do usuário.  

<!-- links -->  

[MicrosoftMicrosoftedgeInsiderAddonsEdgeextensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Extensões - Complementos do Microsoft Edge Insider | Microsoft"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui.](https://developer.chrome.com/extensions/hosting)  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
