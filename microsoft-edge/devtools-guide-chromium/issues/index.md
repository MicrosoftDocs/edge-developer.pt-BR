---
description: Use a ferramenta problemas para localizar e corrigir problemas com o website.
title: Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 4691db9542ecff93d1b59e243844109e0c730d23
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124723"
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

# Localizar e corrigir problemas com a ferramenta problemas do DevTools Microsoft Edge  

A ferramenta **problemas** no Microsoft Edge devtools reduz a notificação cansativo e resíduos do **console**.  Use-o para encontrar soluções para problemas detectados pelo navegador, como problemas com cookies e conteúdo misto.  

> [!NOTE]
> No Microsoft Edge 84, a ferramenta **problemas** dá suporte a três tipos de problemas:  
> *   [Problemas com cookies][MDNSameSiteCookies]  
> *   [Conteúdo misto][MDNMixedContent]  
> *   [Problemas com o COEP][W3CCOEPSpec]
> 
> O Microsoft Edge DevTools Team Plan para dar suporte a mais tipos de problemas em versões futuras do Microsoft Edge.  

## Abrir a ferramenta problemas na gaveta do DevTools  

1.  Acesse uma página, como [SameSite-sandbox.Glitch.me][GlitchSamesiteSandbox], que contém problemas para corrigir.  
1.  [Abra o devtools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Selecione o botão **ir para problemas** na barra de aviso amarela.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-open-issues-tab.msft.png":::
             O botão **ir para problemas** na barra de aviso amarela quando problemas são detectados.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Ou, se preferir, escolha **problemas** no menu **mais ferramentas** .  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media//issues-more-tools-menu.msft.png":::
             Ferramenta **problemas** no menu **mais ferramentas**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Selecione o botão **recarregar página** , se necessário.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-before-refresh.msft.png":::
       Ferramenta **problemas** na gaveta devtools com o botão **recarregar página**  
    :::image-end:::  

    Os problemas relatados no **console** são muito difíceis de entender, como os avisos de cookies na imagem a seguir.  Com base nos problemas relatados, talvez não seja claro o que você deve fazer.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-after-refresh.msft.png":::
       Ferramenta **problemas** na gaveta devtools com três problemas de cookies  
    :::image-end:::  
    
## Exibir itens na ferramenta problemas  

A ferramenta **problemas** na gaveta do devtools apresenta avisos em uma maneira estruturada, agregada e acionável.  

1.  Selecione um item na ferramenta **problemas** para obter orientação sobre como corrigir o problema e localizar os recursos afetados.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Marcar cookies entre sites como** um problema seguro aberto na ferramenta **problemas**  
    :::image-end:::  
    
    Cada item tem quatro componentes:  
    
    *   Uma manchete descrevendo o problema.  
    *   Uma descrição que fornece o contexto e a solução.  
    *   Uma seção de **recursos afetados** que se vincula aos recursos dentro do contexto devtools apropriado, como o painel rede.  
    *   Links para outras diretrizes.  
    
1.  Selecione itens em **recursos afetados** para exibir detalhes.  No exemplo a seguir, a **marca cookies entre sites como** um problema seguro afeta um cookie e duas solicitações.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Recursos afetados abertos na ferramenta **problemas** na gaveta do devtools  
    :::image-end:::  
    
## Exibir problemas no contexto  

1.  Selecione um link de recurso para exibir o item no contexto apropriado no DevTools.  No exemplo a seguir, selecione `samesite-sandbox.glitch.me` em **solicitações** para mostrar os cookies anexados a essa solicitação.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-view-request.msft.png":::
       Exibir o cookie afetado no painel de **rede** do devtools  
    :::image-end:::  

1.  Role para ver o item com um problema: para o exemplo a seguir, o `ck02` Cookie.  Passe o mouse sobre a coluna **SameSite** para ver o `None` valor detectado pelo problema.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Botão ir para problemas na barra de aviso amarela quando problemas são detectados" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` valor na coluna **SameSite** para o `ck02` cookie no painel de **rede** devtools  
    :::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open.md "Abrir o Microsoft Edge DevTools | Documentos da Microsoft"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Testes de cookies SameSite | Problema"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "SameSite cookies | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Conteúdo misto | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Política incorporada de origem cruzada | Grupo da Comunidade Incubator da Web"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/issues/index) e é criada por [Samuel Dutton][SamDutton] \ (defensora do desenvolvedor \).  
[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
