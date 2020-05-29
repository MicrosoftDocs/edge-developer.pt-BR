---
title: Referência de acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 7417388023612b6e1ca651deba28e099e3c8e3d8
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581570"
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





# Referência de acessibilidade   



Esta página é uma referência abrangente dos recursos de acessibilidade no Microsoft Edge DevTools.  Destina-se a desenvolvedores da Web que:  

*   Tenha noções básicas sobre o DevTools, como abri-lo.  
*   Estão familiarizados com [princípios de acessibilidade e práticas recomendadas][MDNAccessibility].  

A finalidade dessa referência é ajudar você a descobrir todas as ferramentas disponíveis no DevTools que ajudam a examinar a acessibilidade de uma página.  

Consulte [navegando no Microsoft Edge devtools com tecnologia assistencial][DevtoolsAccessibilityNavigation] se você estiver procurando ajuda sobre como navegar no devtools com uma tecnologia assistencial como um leitor de tela.  

## Visão geral dos recursos de acessibilidade no Microsoft Edge DevTools   

Esta seção explica como o DevTools se encaixa no seu kit de ferramentas de acessibilidade geral.  

Ao determinar se uma página está acessível, você precisa ter duas perguntas gerais em mente:  

1.  Você consegue navegar na página com um [leitor de tela][MDNScreenReader]ou teclado?  
1.  Os elementos da página são marcados corretamente para os leitores de tela?  

Em geral, o DevTools deve ajudá-lo a corrigir erros relacionados a perguntas #2, pois esses erros são fáceis de detectar de maneira automatizada.  Pergunta #1 é tão importante, mas infelizmente, infelizmente, o DevTools não o ajuda.  A única maneira de encontrar erros relacionados a perguntas #1 é tentar usar uma página com um leitor de tela ou teclado.  <!--See [How To Do An Accessibility Review][AccessibilityReview] to learn more.  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## Fazer auditoria da acessibilidade de uma página   

> [!NOTE]
> O painel **auditorias** fornece links para conteúdo hospedado em sites de terceiros.  A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e todos os dados que possam ser coletados.  

Em geral, use o painel auditorias para determinar se:  

*   Uma página está marcada corretamente para leitores de tela.  
*   Os elementos de texto em uma página têm taxas de contraste suficientes. Consulte também [exibir a taxa de contraste de um elemento de texto no seletor de cores](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).  

Para fazer auditoria em uma página:  

1.  Vá para a URL que você deseja auditar.  
1.  No DevTools, clique na guia **auditorias** .  O DevTools mostra várias opções de configuração.  
    
    > ##### Figura 1  
    > Configurando auditorias  
    > ![Configurando auditorias][ImageConfiguringAudits]  
    
    > [!NOTE]
    > As capturas de tela desta seção foram tiradas com a versão 79 do Microsoft Edge.  Você pode verificar qual versão está executando em `edge://version` .  A interface do usuário do painel **auditoria** tem uma aparência diferente nas versões anteriores do Microsoft Edge, mas o fluxo de trabalho geral é o mesmo.  
    
1.  Para **dispositivo**, selecione **móvel** se desejar simular um dispositivo móvel.  Essa opção muda a cadeia de caracteres do seu agente de usuário e redimensiona o visor.  Se a versão móvel da página for exibida de forma diferente da versão para área de trabalho, essa opção poderá ter um efeito significativo nos resultados da sua auditoria.  
1.  Na seção **auditorias** , certifique-se de que **acessibilidade** está ativada.  Desabilite as outras categorias se desejar excluí-las do relatório.  Deixe-os habilitados se você quiser descobrir outras maneiras de melhorar a qualidade da página.  
1.  A seção **throttling** permite que você controle a rede e a CPU, o que é útil para analisar o desempenho da carga.  Essa opção deve ser irrelevante para a pontuação de acessibilidade, portanto, você pode usar o que preferir.  
1.  A caixa de seleção **limpar armazenamento** permite limpar todo o armazenamento antes de carregar a página ou preservar o armazenamento entre as cargas da página.  Essa opção também é provavelmente irrelevante para a pontuação de acessibilidade, portanto, você pode usar o que preferir.  
1.  Clique em **executar auditorias**. Após 10 a 30 segundos, o DevTools fornece um relatório.  Seu relatório oferece várias dicas sobre como melhorar a acessibilidade da página.  
    
    > ##### Figura 2  
    > Um relatório  
    > ![Um relatório][ImageReport]  
    
1.  Clique em uma auditoria para saber mais sobre isso.  
    
    > ##### Figura 3  
    > Mais informações sobre uma auditoria  
    > ![Mais informações sobre uma auditoria][ImageAttributes]  
    
1.  Clique em **saiba mais** para ver a documentação dessa auditoria.
    
    > ##### Figura 4  
    > Exibir a documentação de uma auditoria  
    > ![Exibir a documentação de uma auditoria][ImageAuditDocumentation]  
    
### Consulte também: extensão aXe   

Você pode preferir usar a [extensão Axe][ChromeWebStoreAxe] em vez do painel **auditorias** .  
A extensão aXe geralmente fornece as mesmas informações, já que é o mecanismo subjacente que alimenta o painel auditorias.  A extensão aXe tem uma interface do usuário diferente e descreve as auditorias de forma ligeiramente diferente.  
Uma vantagem de que a extensão aXe tem sobre o painel **auditorias** é que ele permite que você inspecione e destaque os nós com falha.  

> ##### Figura 5  
> A extensão aXe  
> ![A extensão aXe][ImageAxeExtension]  

## O painel Acessibilidade   

O painel **acessibilidade** é onde você vê a árvore de acessibilidade, atributos do Aria e propriedades de acessibilidade calculadas dos nós dom.  

Para abrir o painel de **acessibilidade** :  

1.  Clique na guia **elementos** .  
1.  Na **árvore DOM**, selecione o elemento que você deseja inspecionar.  
1.  Clique na guia **acessibilidade** .  Esta guia pode estar oculta atrás do botão **mais** guias ![ mais guias ][ImageMoreTabsIcon] .  

> ##### Figura 6  
> Inspecionar o `h1` elemento da home page do devtools no painel **acessibilidade**  
> ![Inspecionar o elemento H1 da home page do DevTools no painel Acessibilidade][ImageA11yPane]  

### Exibir a posição de um elemento na árvore de acessibilidade   

A [árvore de acessibilidade][MDNAccessibilityTree] é um subconjunto da árvore DOM.  Ele somente contém elementos da árvore DOM que são relevantes e úteis para exibir o conteúdo de uma página em um leitor de tela.  

Inspecione a posição de um elemento na árvore de acessibilidade no [painel Acessibilidade](#the-accessibility-pane).  

> ##### Figura 7  
> A seção de árvore de acessibilidade  
> ![A seção de árvore de acessibilidade][ImageAllyTree]  

### Exibir os atributos do ARIA de um elemento   

Os atributos do ARIA garantem que os leitores de tela tenham todas as informações necessárias para representar adequadamente o conteúdo de uma página.  

Exiba os atributos do ARIA de um elemento no [painel Acessibilidade](#the-accessibility-pane).  

> ##### Figura 8  
> A seção de atributos do ARIA  
> ![A seção de atributos do ARIA][ImageAriaAttributesSection]  

### Exibir as propriedades de acessibilidade calculadas de um elemento   

> [!NOTE]
> Se você estiver procurando propriedades CSS calculadas, consulte a [guia calculada][DevtoolsCssReferenceViewActuallyAppliedElements].  

Algumas propriedades de acessibilidade são calculadas dinamicamente pelo navegador.  Essas propriedades são exibidas na seção **Propriedades calculadas** do painel **acessibilidade** .  

Exiba as propriedades de acessibilidade calculadas de um elemento no [painel Acessibilidade](#the-accessibility-pane).  

> ##### Figura 9  
> A seção Propriedades calculadas (acessibilidade)  
> ![A seção Propriedades calculadas (acessibilidade)][ImageComputedA11yPropertiesSection]  

## Exibir a taxa de contraste de um elemento de texto no seletor de cores   

Algumas pessoas com visão subnormal não veem áreas como muito brilhantes ou muito escuras.  Tudo tem a aparência da mesma forma de brilho, o que torna difícil distinguir estruturas de tópicos e bordas.  
A taxa de contraste mede a diferença de brilho entre o primeiro e o plano de fundo do texto.  Se o texto tiver uma taxa de contraste baixa, esses usuários com deficiência visual poderão ter literalmente o seu site como uma tela em branco.  

O seletor de cores ajuda a verificar se o texto atende aos níveis de taxa de contraste recomendados:  

1.  Clique na guia **elementos** .  
1.  Na **árvore DOM**, selecione o elemento de texto que você deseja inspecionar.  
    
    > ##### Figura 10  
    > Inspecionar um parágrafo na árvore DOM  
    > ![Inspecionar um parágrafo na árvore DOM][ImageInspectDomTree]  
    
1.  No painel **estilos** , clique no quadrado colorido ao lado do `color` valor do elemento.  
    
    > ##### Figura 11  
    > A `color` Propriedade do elemento  
    > ![A Propriedade Color do elemento][ImageColorElement]  
    
1.  Marque a seção **taxa de contraste** do seletor de cores.  Uma marca de opção significa que o elemento atende à [recomendação mínima][W3CContrastMinimum].  Duas marcas de opção significa que ela atende à [recomendação aprimorada][W3CContrastEnhanced].
    
    > ##### Figura 12  
    > A seção taxa de contraste do seletor de cores mostra 2 marcas de seleção e um valor de `13.97`  
    > ![A seção taxa de contraste do seletor de cores mostra duas marcas de seleção e um valor de 13,97][ImageColorPickerContrastRatio]  
    
1.  Clique na seção **taxa de contraste** para ver mais informações.  Uma linha aparece no seletor Visual na parte superior do seletor de cores.  Se a cor atual atender às recomendações, qualquer coisa no mesmo lado da linha também atenderá às recomendações.  Se a cor atual não atender às recomendações, qualquer coisa no mesmo lado também não atende às recomendações.  
    
    > ##### Figura 13  
    > A linha de taxa de contraste no seletor Visual  
    > ![A linha de taxa de contraste no seletor Visual][ImageContrastRatioLine]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  

[ImageConfiguringAudits]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-pane.msft.png "Figura 1: Configurando auditorias"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result.msft.png "Figura 2: uma figura"  
[ImageAttributes]: /microsoft-edge/devtools-guide-chromium/media/accessibility-audits-run-audits-result-issues-expanded.msft.png "Figura 3: mais informações sobre uma auditoria"  
[ImageAuditDocumentation]: /microsoft-edge/devtools-guide-chromium/media/accessibility-web-dev-accessibility-audits-learn-more.msft.png "Figura 4: exibindo a documentação de uma auditoria"  
[ImageAxeExtension]: /microsoft-edge/devtools-guide-chromium/media/accessibility-devtools-extension-axe-panel.msft.png "Figura 5: a extensão aXe"  
[ImageA11yPane]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility.msft.png "Figura 6: inspecionando o elemento H1 da página inicial do DevTools no painel de acessibilidade"  
[ImageAllyTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-tree.msft.png "Figura 7: seção de árvore de acessibilidade"  
[ImageAriaAttributesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-aria-attributes.msft.png "Figura 8: seção atributos do ARIA"  
[ImageComputedA11yPropertiesSection]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-accessibility-computed-properties.msft.png "Figura 9: seção de propriedades calculadas (acessibilidade)"  
[ImageInspectDomTree]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-paragraph-highlight.msft.png "Figura 10: inspecionar um parágrafo na árvore DOM"  
[ImageColorElement]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color.msft.png "Figura 11: a Propriedade Color do elemento"  
[ImageColorPickerContrastRatio]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png "Figura 12: a seção índice de contraste do seletor de cores mostra 2 marcas de seleção e um valor de 13,97"  
[ImageContrastRatioLine]: /microsoft-edge/devtools-guide-chromium/media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png "Figura 13: linha de proporção de contraste no seletor Visual"  
<!-- links -->  

[DevtoolsAccessibilityNavigation]: navigation.md "Navegar no Microsoft Edge DevTools com tecnologia assistencial"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Exibir somente a CSS que realmente é aplicada a um elemento-referência de elemento CSS"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "Axe-teste de acessibilidade na Web-Web Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Árvore de acessibilidade (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Acessibilidade | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Leitor de tela | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contraste (aprimorado) nível AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Contraste (mínimo) nível AA | W3C"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
