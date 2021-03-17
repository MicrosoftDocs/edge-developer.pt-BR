---
description: Uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.
title: Referência de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: fce6dec3883cbcc758780a9fedb4c0fb2a8d0a4c
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439251"
---
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

# <a name="accessibility-reference"></a>Referência de acessibilidade  

Esta página é uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.  Destina-se a desenvolvedores web que:  

*   Tenha uma compreensão básica do DevTools, como como abri-lo.  
*   Estão familiarizados com [princípios de acessibilidade e práticas recomendadas.][MDNAccessibility]  
    
O objetivo dessa referência é ajudá-lo a descobrir todas as ferramentas disponíveis no DevTools que o ajudam a examinar a acessibilidade de uma página.  

Se você estiver procurando ajuda para navegar no DevTools com uma tecnologia auxiliar, como um leitor de tela, navegue até Navegar pelo [Microsoft Edge DevTools][DevtoolsAccessibilityNavigation]com tecnologia assistida.  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a>Visão geral dos recursos de acessibilidade no Microsoft Edge DevTools  

Esta seção explica como o DevTools se encaixa no kit de ferramentas de acessibilidade geral.  

Ao determinar se uma página está acessível, você precisa ter duas perguntas gerais em mente:  

1.  Você é capaz de navegar na página com um teclado ou [um leitor de tela?][MDNScreenReader]  
1.  Os elementos da página estão marcados corretamente para leitores de tela?  
    
Em geral, o DevTools deve ajudá-lo a corrigir erros relacionados a perguntas #2, pois esses erros são fáceis de detectar de forma automatizada.  A #1 de perguntas é tão importante quanto, mas infelizmente o DevTools não o ajuda lá.  A única maneira de encontrar erros relacionados à #1 é tentar usar uma página com um teclado ou leitor de tela por conta própria.  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a>Auditar a acessibilidade de uma página  

> [!NOTE]
> A **ferramenta Auditorias** fornece links para conteúdo hospedado em sites de terceiros.  A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e quaisquer dados que possam ser coletados.  

Em geral, use o painel Auditorias para determinar se:  

*   Uma página é marcada corretamente para leitores de tela.  
*   Os elementos de texto em uma página têm taxas de contraste suficientes.  Navegue [até Exibir a taxa de contraste de um elemento de texto no Selador de Cores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

Para auditar uma página:  

1.  Navegue até a URL que você deseja auditar.  
1.  No DevTools, escolha a **ferramenta Auditorias.**  O DevTools mostra várias opções de configuração.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Configurar auditorias" lightbox="../media/accessibility-audits-pane.msft.png":::
       Configurar auditorias  
    :::image-end:::  
    
    > [!NOTE]
    > As capturas de tela nesta seção foram feitas com o Microsoft Edge versão 79.  Você pode verificar qual versão está executando em `edge://version` .  A **interface do usuário da** ferramenta Auditorias parece diferente em versões anteriores do Microsoft Edge, mas o fluxo de trabalho geral é o mesmo.  
    
1.  Para **Dispositivo**, escolha **Móvel** se quiser simular um dispositivo móvel.  Essa opção altera a cadeia de caracteres do agente do usuário e resize o viewport.  Se a versão móvel da página for exibida de forma diferente da versão da área de trabalho, essa opção poderá ter um efeito significativo nos resultados da auditoria.  
1.  Na seção **Auditorias,** certifique-se de **que a Acessibilidade** está habilitada.  Desabilite as outras categorias se quiser exclui-las do relatório.  Deixe-os habilitados se você quiser descobrir outras maneiras de melhorar a qualidade da sua página.  
1.  A **seção Throttling** permite que você reduza a rede e a CPU, o que é útil ao analisar o desempenho da carga.  Essa opção deve ser irrelevante para sua pontuação de acessibilidade, portanto, você pode usar o que preferir.  
1.  A **caixa de seleção** Limpar Armazenamento permite limpar todo o armazenamento antes de carregar a página ou preservar o armazenamento entre cargas de página.  Essa opção também provavelmente é irrelevante para sua pontuação de acessibilidade, portanto, você pode usar o que preferir.  
1.  Escolha **Executar Auditorias**. Após 10 a 30 segundos, o DevTools fornece um relatório.  Seu relatório fornece várias dicas sobre como melhorar a acessibilidade da página.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Um relatório" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Um relatório  
    :::image-end:::  
    
1.  Escolha uma auditoria para saber mais sobre ela.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Mais informações sobre uma auditoria" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Mais informações sobre uma auditoria  
    :::image-end:::  
    
1.  Escolha **Saber mais** para exibir a documentação dessa auditoria.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Exibir a documentação de uma auditoria" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Exibir a documentação de uma auditoria  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a>Consulte também: extensão aXe  

Você pode preferir usar a extensão [aXe em][ChromeWebStoreAxe] vez da **ferramenta Auditorias.**  
A extensão aXe geralmente fornece as mesmas informações, já que é o mecanismo subjacente que alimenta o painel auditorias.  A extensão aXe tem uma interface do usuário diferente e descreve as auditorias um pouco diferente.  
Uma vantagem que a extensão aXe tem sobre a ferramenta **Auditorias** é que ela permite inspecionar e realçar nós com falha.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="A extensão aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   A extensão aXe  
:::image-end:::  

## <a name="the-accessibility-panel"></a>O painel Acessibilidade  

O **painel Acessibilidade** é onde você visualiza a árvore de acessibilidade, os atributos do ARIA e as propriedades de acessibilidade calculadas dos nós DOM.  

Para abrir o **painel Acessibilidade:**  

1.  Escolha a **ferramenta Elementos.**  
1.  Na Árvore **DOM,** selecione o elemento que você deseja inspecionar.  
1.  Escolha o **painel Acessibilidade.**  Esse painel pode estar oculto atrás do **botão Mais Guias** \( Mais Guias ![ ](../media/more-tabs-icon.msft.png) \).  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Inspecione o elemento h1 da homepage DevTools no painel Acessibilidade" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Inspecionar o `h1` elemento da homepage DevTools no painel **Acessibilidade**  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Exibir a posição de um elemento na árvore de acessibilidade  

A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.  Ele contém apenas elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.  

Inspecione a posição de um elemento na árvore de acessibilidade do painel [Acessibilidade.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="A seção Árvore de Acessibilidade" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   A **seção Árvore de** Acessibilidade  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a>Exibir os atributos ARIA de um elemento  

Os atributos do ARIA garantem que os leitores de tela tenham todas as informações necessárias para representar corretamente o conteúdo de uma página.  

Exibir os atributos ARIA de um elemento no [painel Acessibilidade.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="A seção Atributos do ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   A **seção Atributos do ARIA**  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a>Exibir as propriedades de acessibilidade calculadas de um elemento  

> [!NOTE]
> Se você estiver procurando propriedades CSS calculadas, navegue até [Painel Computado.][DevtoolsCssReferenceViewActuallyAppliedElements]  

Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.  Essas propriedades são exibidas na seção **Propriedades Computadas** do painel **Acessibilidade.**  

Exibir as propriedades de acessibilidade calculadas de um elemento no painel [Acessibilidade.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="A seção Propriedades Computadas do painel Acessibilidade" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   A **seção Propriedades Computadas** do painel **Acessibilidade**  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a>Exibir a taxa de contraste de um elemento de texto no Selador de Cores  

Algumas pessoas com baixa visão não veem áreas muito claras ou muito escuras.  Tudo tende a aparecer com o mesmo brilho, o que dificulta a distinção de contornos e bordas.  

A taxa de contraste mede a diferença no brilho entre o primeiro plano e o plano de fundo do texto.  Se o texto tiver uma taxa de contraste baixa, esses usuários de baixa visão poderão literalmente experimentar seu site como uma tela em branco.  

O Selador de Cores ajuda você a verificar se seu texto atende aos níveis de taxa de contraste recomendados:  

1.  Escolha a **ferramenta Elementos.**  
1.  Na Árvore **DOM,** selecione o elemento de texto que você deseja inspecionar.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Inspecionar um parágrafo na árvore DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Inspecionar um parágrafo na árvore **DOM**  
    :::image-end:::  
    
1.  No painel **Estilos,** escolha o quadrado de cores ao lado `color` do valor do elemento.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="A propriedade color do elemento" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       A `color` propriedade do elemento  
    :::image-end:::  
    
1.  Verifique a **seção Taxa de** Contraste do Selador de Cores.  Uma marca de seleção significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].  Dois indicadores de verificação significam que ele atende [à recomendação aprimorada][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="A seção Taxa de Contraste do Se picker de cores mostra 2 marcas de seleção e um valor de 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       A **seção Taxa** de Contraste do Selador de Cores mostra 2 marcas de seleção e um valor de `13.97`  
    :::image-end:::  
    
1.  Para obter mais informações, escolha a seção **Taxa de Contraste.**  Uma linha aparece no se picker visual na parte superior do Selador de Cores.  Se a cor atual atender às recomendações, qualquer coisa do mesmo lado da linha também atende às recomendações.  Se a cor atual não atender às recomendações, qualquer coisa do mesmo lado também não atenderá às recomendações.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="A Linha de Taxa de Contraste no selador visual" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       A **Linha de Taxa** de Contraste no selador visual  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegue pelo Microsoft Edge DevTools com tecnologia | Microsoft Docs"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exibir apenas o CSS que é realmente aplicado a um elemento - Referência CSS | Microsoft Docs"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe - Teste de Acessibilidade da Web - Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Acessibilidade | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Leitor de tela | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Nível AAA de contraste (aprimorado) | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Nível AA de contraste (mínimo) | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
