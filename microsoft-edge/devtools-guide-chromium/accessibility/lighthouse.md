---
description: Testando a acessibilidade usando o Farol de dentro do DevTools.
title: Testar a acessibilidade usando o Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: bb158085eb516c8d4ce37a22f6b612784db51461
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597234"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a>Testar a acessibilidade usando o Lighthouse

Você pode usar o Farol de dentro do DevTools para auditar a acessibilidade de uma página e gerar um relatório. Você pode usar a ferramenta Doleiro para determinar:

*   Se uma página está marcada corretamente para leitores de tela.  
*   Se os elementos de texto em uma página têm taxas de contraste suficientes usando o Selador de Cores. Para obter mais informações, navegue [até Testar contraste de cor de texto usando o Selador de Cores](color-picker.md).   

> [!NOTE]
> A **ferramenta Lighthouse** fornece links para conteúdo hospedado em sites de terceiros.  A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e quaisquer dados que possam ser coletados.  

Para auditar uma página usando a ferramenta Lighthouse, execute as etapas a seguir.

1.  Navegue até a URL que você deseja auditar.
1.  Em DevTools, selecione a **ferramenta DevTools.**  As opções de configuração são exibidas.
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Opções de configuração do Farol" lightbox="../media/accessibility-lighthouse.msft.png":::
       Opções de configuração do Farol
    :::image-end:::  
    
1.  Para **Dispositivo**, selecione **Móvel** se quiser simular um dispositivo móvel.  Essa opção altera a cadeia de caracteres do agente do usuário e resize o viewport.  Essa opção pode afetar os resultados da auditoria.
1.  Na seção **Categorias,** selecione **Acessibilidade**.
1.  Selecione **Gerar relatório**. Após 10 a 30 segundos, o DevTools exibe um relatório.  O relatório fornece dicas sobre como melhorar a acessibilidade da página.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Um relatório do Farol para a categoria Acessibilidade" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       Um relatório do Farol para a **categoria Acessibilidade**
    :::image-end:::  
    
1.  Selecione um item no relatório para saber mais sobre ele.  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Um problema expandido em um relatório do Farol" lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       Um problema expandido em um relatório do Farol
    :::image-end:::  
    
1.  Selecione o link **Saber mais** para exibir a documentação do problema.
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Exibir a documentação de um problema" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Exibir a documentação de um problema
    :::image-end:::  

1.  Para retornar às opções de configuração, em DevTools, selecione **Executar uma auditoria** ( `+` ).    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Teste de Acessibilidade da Web - Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
