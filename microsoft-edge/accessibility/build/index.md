---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Veja como as práticas recomendadas e os Aplicativos de Internet Rich (ARIA) acessíveis podem se reunir para criar um site acessível.
title: Criar | Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, borda, desenvolvimento da Web, ARIA, desenvolvedor, UIA, Automação da Interface do Usuário
ms.custom: seodec18
ms.openlocfilehash: 69f0576b39815708d01477972abad1f8bdc9486e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397885"
---
# <a name="building-accessible-websites"></a>Criando sites acessíveis

A Web é preenchida com sites dinâmicos e complexos, aplicativos e interfaces de usuário criadas usando uma combinação de HTML, CSS e JavaScript.  No entanto, quando projetados e criados sem acessibilidade em mente, esses sites complexos são difíceis de usar por pessoas que dependem de tecnologias [assisttivas](https://webaim.org/articles/motor/assistive) para navegar na Web. A criação de sites acessíveis a pessoas com deficiência requer informações semânticas sobre a interface do usuário. Isso permite que tecnologias assistenciais, como leitores de tela, transmitam as informações necessárias para ajudar as pessoas com um intervalo de habilidades a usar o site.

Visite [HTML5Accessibility para](https://html5accessibility.com) obter informações sobre quais novos recursos HTML5 têm suporte do Microsoft Edge.

## <a name="how-accessibility-works"></a>Como funciona a acessibilidade

Tecnologias assistivas adicionam recursos que os computadores geralmente não têm. Por exemplo, um usuário com deficiência visual pode usar seu teclado em combinação com tecnologias assistivas, como um leitor de tela, em vez de usar diretamente o navegador com o mouse e a tela. Para aplicativos em plataformas da Microsoft e na Web, a tecnologia auxiliar interage com a [Automação](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)da Interface do Usuário da Microsoft , um modelo de objeto específico do aplicativo, como o Modelo de Objeto de Documento (DOM) no Microsoft Edge, ou uma combinação deles.

Para desenvolvedores da Web, determinados elementos HTML são mapeados para objetos de Automação da Interface do Usuário, portanto, ao selecionar esses elementos HTML, o desenvolvedor pode usar as propriedades de acessibilidade e os eventos incorporados a esses elementos. Ao desenvolver seu site, você geralmente só precisa se preocupar em garantir que a API seja escrita corretamente (ou que o elemento apropriado seja especificado), para que o aplicativo seja acessível. Confira [ARIA e Automação da Interface do Usuário no Microsoft Edge](./ARIA-and-UI-Automation.md) para obter mais informações.  Para obter informações sobre aplicativos UWP (Plataforma Universal do Windows) acessíveis, navegue até o tópico [Acessibilidade](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) no Centro de Dev do Windows.

Muitos problemas comuns de acessibilidade com conteúdo dinâmico podem ser resolvidos por uma boa prática de codificação, e a documentação do [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) inclui muitas técnicas e práticas recomendadas para ajudá-lo a criar aplicativos Web dinâmicos mais acessíveis. Mesmo quando codificado corretamente, no entanto, o conteúdo dinâmico não é necessariamente acessível. [O ARIA (Aplicativos de Internet Rich)](#aria) acessíveis ajuda a superar esse problema.  

Para obter mais informações sobre acessibilidade da Web, confira a Introdução à [Acessibilidade da Web](https://www.w3.org/WAI/intro/accessibility.php) pela Iniciativa de Acessibilidade da Web [(ISO)](https://www.w3.org/WAI).

## <a name="aria"></a>ARIA

A [especificação ARIA (Accessible Rich Internet Applications)](https://www.w3.org/TR/wai-aria/) pela Iniciativa de Acessibilidade da [Web](https://www.w3.org/WAI/) do W3C define como uma sintaxe para tornar o conteúdo da Web dinâmico e interfaces de usuário personalizadas acessíveis a todas as pessoas. A ARIA estende HTML usando atributos adicionais (funções, propriedades e estados) projetados para transmitir semântica personalizada. Esses atributos são usados por navegadores para passar o estado e a função dos controles para a API de acessibilidade.

### <a name="roles-properties-and-states"></a>Funções, propriedades e estados

As funções do ARIA são definidas em elementos usando o atributo para dar informações de tecnologias assistivas e APIs de acessibilidade [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) sobre o elemento. Por exemplo, o elemento abaixo é atribuído para `<li>` significar que é um item em um `role="menuitem"` menu.

```html
<li role="menuitem">Home</li>
```

Estados e propriedades do ARIA são atributos prefixados por ária que fornecem informações específicas sobre um objeto para ajudar a formar a definição da natureza das funções. Propriedades são atributos essenciais à natureza de um objeto, como [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) e [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Alterar uma propriedade afeta o significado do objeto. No exemplo abaixo, a propriedade é definida em um item de menu para `aria-haspopup="true"` significar que ela tem um `<li>` pop-up.

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Os estados não alteram a natureza do objeto, mas representam informações associadas ao objeto ou à interação do usuário com o objeto, como [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) ou [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Por exemplo, o estado no exemplo abaixo representa que a caixa `aria-checked="false"` de seleção não está marcada.

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

Vá para [o Modelo de Funções](https://www.w3.org/TR/wai-aria-1.1/#roles) pelo W3C para ver uma lista completa de funções, propriedades e estados.

Para obter mais informações sobre o ARIA, navegue até ARIA na [seção Recursos.](#resources)

## <a name="assistive-technology-compatibility-testing"></a>Teste de compatibilidade de tecnologia assistida  

Verificar se o site que você está criando funciona com tecnologias auxiliares reais é a melhor maneira de garantir uma boa experiência para seus usuários com deficiências.  Como muitas tecnologias auxiliares usam o teclado, testar a acessibilidade do teclado do seu site é um bom lugar para começar.  [O teste de compatibilidade de][W3cPerspectiveVideosKeyboard] teclado valida que os usuários têm acesso a todos os controles interativos sem exigir um mouse.  O Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] é uma extensão do navegador para o Microsoft Edge e o Chrome que orienta e revela vários problemas comuns.  

Depois de ter certeza de que seu site funciona bem com um teclado, experimente-o com outras tecnologias auxiliares, como leitores de tela.  Ele descobre problemas no seguinte.

*   Seu HTML, ARIA e CSS.  
*   O nível de suporte de uma tecnologia assistida para um recurso ou técnica.  
    
Navegadores diferentes podem mapear elementos para APIs de acessibilidade de plataforma de forma diferente do Microsoft Edge.  Ao criar sua interface, é importante considerar cada diferença.  

O WebAIM realiza [][WebaimProjectsScreenreadersurvey8] pesquisas com [][WebaimProjectsLowvisionsurvey2] leitores de tela e usuários de baixa visão que ajudam você a decidir quais tecnologias e navegadores assistivos você deseja testar.  

### <a name="learning-how-to-test"></a>Aprender a testar  

Tecnologias assistivas são ferramentas sofisticadas.  Não suponha que você seja capaz de iniciar imediatamente os testes com uma tecnologia auxiliar sem primeiro saber como ela funciona.  Aprender a testar com um leitor de tela tem uma curva de aprendizado especialmente íngreme.  Um usuário leitor de tela iniciante pode supor que ocorreu um bug de leitor de tela enquanto o problema está relacionado ao uso indevido do leitor de tela.  

Para obter mais informações sobre como aprender a testar com tecnologias assistivas, navegue até [Test with Screen Readers][WebaimArticlesScreenreaderTesting] on WebAIM.  

### <a name="testing-locally"></a>Testando localmente  

A maioria dos dispositivos inclui tecnologias assistivas que são integrados ao sistema operacional.  O Microsoft Windows inclui o leitor [de tela][MicrosoftSupport22798] do Windows Narrator e a [Lupa do Windows.][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]  Tecnologias assistivas de terceiros, como [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]e [ZoomText,][FreedomscientificSoftwareZoomtext] estão disponíveis para download.  O macOS da Apple inclui o [leitor de tela VoiceOver.][AppleAccessibilityMacVision]  E todos os iOS, Android e Linux suportam uma variedade de tecnologias assistivas.  

### <a name="testing-in-virtual-machines-and-emulators"></a>Teste em Máquinas Virtuais e Emuladores  

Em macOS, se você quiser testar com uma tecnologia auxiliar disponível apenas para Windows, como o Windows Narrator ou o NVDA, crie uma máquina virtual do Windows.  Máquinas virtuais com o Microsoft Edge \(EdgeHTML\) e o IE estão disponíveis para VirtualBox e VMWare na página [de download de][MicrosoftDeveloperEdgeVms]Máquinas Virtuais.  

[O Android Studio][AndroidDeveloperSdkInstallingStudioHtml] inclui um emulador que para você testar tecnologias assistivas no [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite].  Siga as instruções para [configurar um][AndroidDeveloperDevicesManagingAvdsHtml] dispositivo virtual e iniciar o [emulador][AndroidDeveloperDevicesEmulatorHtml]e, em seguida, instalar o Pacote de Acessibilidade do [Android][GooglePlayStoreAndroidAccessibilitySuite] na loja do GooglePlay.  

> [!NOTE]
> No momento, o Simulador do iOS não inclui VoiceOver.  

### <a name="cloud-based-testing-tools"></a>Ferramentas de teste baseadas em nuvem  

Se uma tecnologia auxiliar não estiver disponível em seu sistema operacional ou você não for possível instalar uma em uma máquina virtual ou emulador, as ferramentas de teste de tecnologia assistida baseada em nuvem serão a próxima melhor opção.  

*   [O Assistiv Labs (comercial)][AssistivlabsMain] permite testar manualmente com tecnologias assistenciais por meio de qualquer navegador da Web moderno.  Escolha uma tecnologia assistida e um navegador e ele o conecta a uma máquina virtual, emulador ou dispositivo real com o qual você pode interagir.  

## <a name="resources"></a>Recursos

### <a name="accessibility-basics"></a>Noções básicas de acessibilidade

#### [<a name="the-a11y-project"></a>O projeto A11Y](http://a11yproject.com/)

O Projeto A11Y é um esforço orientado pela comunidade para facilitar a acessibilidade da Web. Confira o site do [Projeto A11Y](https://a11yproject.com/) para saber mais sobre princípios básicos de acessibilidade, seu padrão acessível e biblioteca de [widgets](https://a11yproject.com/patterns)e seus recursos em software de acessibilidade, blogs, livros e ferramentas. [](http://a11yproject.com/resources.html)

#### [<a name="web-accessibility-initiative-wai"></a>Iniciativa de Acessibilidade da Web (WAI)](https://w3.org/WAI/)

A Iniciativa de Acessibilidade da Web do W3C (WAI) é um esforço para ajudar a melhorar a acessibilidade da Web. Seu site fornece uma variedade de recursos para Introdução à Acessibilidade da [Web,](https://www.w3.org/WAI/gettingstarted/Overview.html) [Design para](https://www.w3.org/WAI/users/Overview.html)Inclusão, tutoriais e [apresentações](https://www.w3.org/WAI/train.html)e muito mais.

### <a name="accessibility-blogs"></a>Blogs de Acessibilidade

#### [<a name="the-paciello-group"></a>O Grupo Paciello](https://www.paciellogroup.com/blog/)

O Grupo Paciello fornece soluções de consultoria e tecnologia para organizações em todo o mundo para garantir que seus clientes alcancem todos os públicos de forma eficaz e eficiente, enquanto a atender aos padrões governamentais e internacionais. Seu blog aborda tópicos como práticas recomendadas de acessibilidade da Web, ferramentas de acessibilidade e tendências de acessibilidade.

#### [<a name="simply-accessible"></a>Simplesmente Acessível](http://simplyaccessible.com/articles/)

Simplesmente Acessível é uma equipe de especialistas em acessibilidade que fornece treinamento de acessibilidade, consultoria e muito mais para alterar a percepção de acessibilidade na Web. A [seção Artigos](http://simplyaccessible.com/articles/) aborda as práticas recomendadas para acessibilidade da Web, design acessível e muito mais.

#### [<a name="ssb-bart-group-ssb"></a>Grupo SSB BART (SSB)](http://www.ssbbartgroup.com/blog/)

O Grupo SSB DO BART é uma empresa de acessibilidade digital que oferece suporte a seus clientes no desenvolvimento e implantação de produtos e serviços acessíveis. Seu blog aborda tópicos como práticas recomendadas do ARIA, tendências de acessibilidade, webinars e muito mais.

### <a name="accessible-examples"></a>Exemplos acessíveis

#### [<a name="allyjs---tutorials"></a>ally.js - Tutoriais](http://allyjs.io/tutorials/)

Biblioteca JavaScript para ajudar aplicativos Web modernos com preocupações de acessibilidade tornando a acessibilidade mais simples.

#### [<a name="heydonworks---aria-examples"></a>Heydonworks - Exemplos do ARIA](http://heydonworks.com/practical_aria_examples/)

Exemplos práticos do ARIA para melhorar a acessibilidade do aplicativo

#### [<a name="openajax-examples"></a>Exemplos de OpenAjax](http://oaa-accessibility.org/)

O site da OpenAjax Alliance é um excelente recurso para verificar as regras para o WAI-ARIA e fornece vários exemplos de implementações DESAD-ARIA.

#### [<a name="patterns"></a>Padrões](http://a11yproject.com/patterns.html)

[O Projeto A11Y](http://a11yproject.com/) oferece uma biblioteca de widgets e padrões acessíveis, como menus, botões, dicas de ferramentas e muito mais.

### <a name="accessibility-techniques--tools"></a>Técnicas de acessibilidade & Ferramentas

#### [<a name="accessibility-creating-accessible-extension-icons-for-microsoft-edge"></a>Acessibilidade: criando ícones de extensão acessíveis para o Microsoft Edge](../../edgehtml/extensions/guides/accessibility.md)

Obter orientações sobre como criar ícones de extensões acessíveis para o Microsoft Edge.

#### [<a name="accessible-name-and-description-computation-and-mappings-11"></a>Nome e Descrição Acessíveis: Computação e Mapeamentos 1.1](https://www.w3.org/TR/accname-1.1/)

Este documento de mapeamento W3C explica como os navegadores determinam o nome e as descrições de objetos acessíveis de idiomas de conteúdo da Web e os expõem em APIs de acessibilidade.

#### [<a name="accessibility-evaluation-resources"></a>Recursos de Avaliação de Acessibilidade](https://www.w3.org/WAI/eval/Overview.html)

Recursos de Avaliação de Acessibilidade é um recurso de várias páginas do W3C que descreve diferentes abordagens para avaliar sites para acessibilidade.

#### [<a name="assistive-technology-compatibility-tests"></a>Testes de compatibilidade de tecnologia assistida](http://www.powermapper.com/tests/)

Resultados de teste mostrando como diferentes tipos de conteúdo e padrões se comportam em tecnologias assistivas (AT), como leitores de tela.

#### [<a name="building-accessible-websites-just-got-a-lot-easier"></a>A criação de sites acessíveis ficou muito mais fácil](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

Esta postagem do blog Desenvolvimento da Web e Ferramentas do .NET descreve o Visual Studio de extensão [da Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).

#### [<a name="core-accessibility-api-mappings-11"></a>Core Accessibility API Mappings 1.1](https://www.w3.org/TR/core-aam-1.1/)

Este documento de mapeamento W3C explica como a semântica de linguagens de conteúdo da Web são expostas a APIs de acessibilidade.  

#### [<a name="easy-checks--a-first-review-of-web-accessibility"></a>Verificações Fáceis – Uma primeira revisão da acessibilidade da Web](https://www.w3.org/WAI/eval/preliminary.html)

Uma série de verificações rápidas feitas pelo WAI que ajudam você a melhorar a acessibilidade de uma página da Web.

#### [<a name="how-to-meet-wcag-20"></a>Como atender ao WCAG 2.0](https://www.w3.org/WAI/WCAG20/quickref/)

Uma referência rápida às diretrizes de acessibilidade de conteúdo da Web (WCAG) 2.0 (critérios de sucesso) e técnicas.

#### [<a name="html-accessibility-api-mappings-10"></a>Mapeamentos de API de Acessibilidade HTML 1.0](https://www.w3.org/TR/html-aam-1.0/)

Este documento de mapeamentos W3C explica como o elemento HTML5.1 e os atributos são mapeados para APIs de acessibilidade da plataforma.

#### [<a name="quick-tips"></a>Dicas Rápidas](http://a11yproject.com/#Quick-tips)

Uma lista de dicas de desenvolvimento rápido da Web para acessibilidade [pelo Projeto A11Y.](http://a11yproject.com/)

#### [<a name="site-scan"></a>Verificação de site](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

A ferramenta Verificação de Site no Centro de Dev do Microsoft Edge verifica se há bibliotecas des atualizadas, problemas de layout e problemas de acessibilidade.

#### [<a name="techniques-for-wcag-20"></a>Técnicas do WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

Técnicas do W3C que fornecem orientações para desenvolvedores da Web sobre como atender aos critérios de sucesso do WCAG (Diretrizes de Acessibilidade de Conteúdo da [Web) 2.0.](https://w3.org/TR/WCAG20/)

#### [<a name="tips-on-developing-for-web-accessibility"></a>Dicas sobre o desenvolvimento para acessibilidade da Web](https://w3.org/WAI/gettingstarted/tips/developing.html)

Dicas do W3C sobre o desenvolvimento de conteúdo da Web mais acessível para pessoas com deficiências.

#### [<a name="wai-aria-authoring-practices-11"></a>PRÁTICAS DE Autoria 1.1 DE WAI-ARIA](http://w3c.github.io/aria-practices/)

Um documento do W3C que fornece aos leitores uma compreensão de como usar o WAI-ARIA 1.1 e recomenda abordagens para tornar widgets, navegação e comportamentos acessíveis usando funções, estados e propriedades DOAD-ARIA.

#### [<a name="wai-guidelines-and-techniques"></a>Diretrizes e técnicas DOLS](https://w3.org/WAI/guid-tech.html)

Uma série de diretrizes e padrões de acessibilidade da Web desenvolvidos pela NORMA.  

#### [<a name="web-accessibility-evaluation-tools-list"></a>Lista de Ferramentas de Avaliação de Acessibilidade da Web](https://www.w3.org/WAI/ER/tools/index.html)

Uma lista de ferramentas de avaliação de acessibilidade da Web para ajudar a determinar se os sites atendem às diretrizes de acessibilidade.

#### [<a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a>Perspectivas de acessibilidade da Web: explorar o impacto e os benefícios para todos](https://w3.org/WAI/perspectives/)

Uma série de vídeos conjunturais curtos do W3C sobre o impacto da acessibilidade e os benefícios para todos.

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Máquinas virtuais | Desenvolvedor do Microsoft Edge"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Guia completo do Narrador | Suporte da Microsoft"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Use a Lupa para tornar as coisas na tela mais fáceis de ver | Suporte da Microsoft"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Percepções de acessibilidade para web | Percepções de acessibilidade"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Criar e gerenciar dispositivos virtuais | Desenvolvedores Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Executar aplicativos no | Desenvolvedores Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Baixe o Android Studio | Desenvolvedores Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Acessibilidade para Visão - Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Laboratórios assistiv"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "JAWS® | Liberdade Científica"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Liberdade Científica"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Android Accessibility Suite | GooglePlay Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "Sobre o NVDA | NV Access"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Compatibilidade de teclado | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Pesquisa de usuários com baixa visão \#2 resultados | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Pesquisa de usuário do leitor de tela \#8 resultados | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Testes com leitores de tela | WebAIM"  
