---
description: Use a ferramenta Problemas para encontrar e corrigir problemas com seu site.
title: Encontre e corrige problemas com a ferramenta Microsoft Edge Problemas do DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 64954d632416f7d1353269d04c1550ca7a0652b7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564179"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a>Encontre e corrige problemas com a ferramenta Microsoft Edge Problemas do DevTools  

A **ferramenta Problemas** no Microsoft Edge DevTools reduz a fatiga de notificação e a desordem do **Console**.  Use-o para encontrar soluções para problemas detectados pelo navegador, como problemas de cookie e conteúdo misto.  

> [!NOTE]
> No Microsoft Edge 84, a **ferramenta Issues** dá suporte a três tipos de problema:  
> *   [Problemas de cookie][MDNSameSiteCookies]  
> *   [Conteúdo misto][MDNMixedContent]  
> *   [Problemas de COEP][W3CCOEPSpec]
> 
> A Microsoft Edge equipe do DevTools planeja dar suporte a mais tipos de problemas em versões futuras Microsoft Edge.  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a>Abra a ferramenta Problemas na gaveta DevTools  

1.  Navegue até uma página da Web, como [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], que contém problemas para corrigir.  
1.  [Abra DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Escolha o **botão Ir para Problemas** na barra de aviso amarelo.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Vá para o botão Problemas na barra de aviso amarelo quando Os problemas são detectados" lightbox="../media/issues-open-issues-tab.msft.png":::
             O **botão Ir para Problemas** na barra de aviso amarelo quando Problemas são detectados.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Como alternativa, escolha **Problemas** no menu **Mais ferramentas.**  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Ferramenta Problemas no menu Mais ferramentas" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Ferramenta Problemas** no menu **Mais ferramentas**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Escolha o **botão Recarregar página,** se necessário.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Ferramenta Problemas no botão DevTools Drawer with Reload page" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Ferramenta Problemas** no botão DevTools Drawer with **Reload page**  
    :::image-end:::  

    Os problemas relatados no **Console** são difíceis de entender, como os avisos de cookie na imagem a seguir.  Com base nos problemas relatados, pode não estar claro o que você deve fazer.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Ferramenta Problemas na Gaveta de DevTools com três problemas de cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Ferramenta Problemas** na Gaveta de DevTools com três problemas de cookie  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a>Exibir itens na ferramenta Problemas  

A **ferramenta Problemas** na Gaveta de DevTools apresenta avisos de forma estruturada, agregada e a ação.  

1.  Escolha um item na ferramenta **Problemas** para obter orientações sobre como corrigir o problema e encontrar recursos afetados.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Marcar cookies entre sites como problema seguro aberto na ferramenta Problemas" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Marcar cookies entre sites como problema** seguro aberto na ferramenta **Problemas**  
    :::image-end:::  
    
    Cada item tem quatro componentes:  
    
    *   Uma título que descreve o problema.  
    *   Uma descrição que fornece o contexto e a solução.  
    *   Uma **seção RECURSOS AFETADOs** que se vincula aos recursos no contexto apropriado do DevTools, como o painel Rede.  
    *   Links para mais orientações.  
    
1.  Escolha itens em **RECURSOS AFETADOs** para exibir detalhes.  No exemplo a seguir, o **mark cross-site cookies as Secure** issue afeta um cookie e duas solicitações.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Recursos afetados abertos na ferramenta Problemas" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Recursos afetados abertos na **ferramenta Problemas** na Gaveta de DevTools  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a>Exibir problemas no contexto  

1.  Escolha um link de recurso para exibir o item no contexto apropriado no DevTools.  No exemplo a seguir, escolha `samesite-sandbox.glitch.me` em **Solicitações** para mostrar os cookies anexados a essa solicitação.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Exibir o cookie afetado na ferramenta Rede de DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       Exibir o cookie afetado na **** ferramenta Rede de DevTools  
    :::image-end:::  

1.  Role para exibir o item com um problema: para o exemplo a seguir, o `ck02` cookie.  Passe o mouse na **coluna SameSite** para revisar `None` o valor detectado pelo problema.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Nenhum valor na coluna SameSite para o cookie ck02 na ferramenta Rede DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` na coluna **SameSite** para o `ck02` cookie na **** ferramenta Rede DevTools  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Testes de cookie sameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Cookies sameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Conteúdo misto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Política de embedder entre origens | Grupo Community Web Incubator"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é de autoria de [Sam Dutton][SamDutton] \(Developer Advocate\).  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[SamDutton]: https://developers.google.com/web/resources/contributors#sam-dutton  
