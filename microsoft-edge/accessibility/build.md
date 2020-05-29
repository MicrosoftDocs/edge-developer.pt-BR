---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Mostre como as práticas recomendadas e os aplicativos sofisticados da Internet (ARIA) acessíveis podem ser juntos para criar um site acessível.
title: Acessibilidade – criar
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, Edge, desenvolvimento da Web, ARIA, desenvolvedor, UIA, automação da interface do usuário
ms.custom: seodec18
ms.openlocfilehash: 4412fef6bb78b5a393ccafd5a2cfa79aba223141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560544"
---
# Criando sites acessíveis
A Web é preenchida com sites, aplicativos e interfaces do usuário dinâmicos e complexos criados usando uma combinação de HTML, CSS e JavaScript.  No entanto, quando projetado e criado sem acessibilidade em mente, esses sites complexos são difíceis de usar por pessoas que dependem de [tecnologias adaptativas](https://webaim.org/articles/motor/assistive) para navegar na Web. A criação de sites acessíveis para pessoas com deficiências exige informações semânticas sobre a interface do usuário. Isso permite que tecnologias assistenciais, como leitores de tela, transmitam as informações necessárias para ajudar as pessoas com diversas habilidades a usar o site.

Acesse [HTML5Accessibility](https://html5accessibility.com) para obter informações sobre quais novos recursos do HTML5 são accessibly suportados pelo Microsoft Edge.

## Como funciona a acessibilidade

As tecnologias adaptativas adicionam recursos que os computadores geralmente não têm. Por exemplo, um usuário com deficiência visual pode usar o teclado em combinação com tecnologia assistencial, como um leitor de tela, em vez de usar o navegador diretamente com o mouse e a tela. Para aplicativos em plataformas Microsoft e na Web, a tecnologia assistencial interage com a [automação da interface do usuário](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)da Microsoft, um modelo de objeto específico do aplicativo, como o dom (modelo de objeto de documento) no Microsoft Edge ou uma combinação desses.

Para os desenvolvedores da Web, determinados elementos HTML são mapeados para objetos de automação da interface do usuário, portanto, ao selecionar esses elementos HTML, o desenvolvedor pode usar as propriedades e os eventos de acessibilidade incluídos nesses elementos. Ao desenvolver seu site, geralmente você só precisa se preocupar em garantir que a API seja gravada corretamente (ou que o elemento apropriado seja especificado), para que o aplicativo possa ser acessado. Consulte [o Aria e a automação da interface do usuário no Microsoft Edge](./build/ARIA-and-UI-Automation.md) para obter mais informações.  Para obter informações sobre aplicativos da plataforma universal do Windows (UWP) acessíveis, consulte o tópico [acessibilidade](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) no centro de desenvolvimento do Windows.

Muitos problemas comuns de acessibilidade com conteúdo dinâmico podem ser resolvidos por uma boa prática de codificação, e a documentação da [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) inclui muitas técnicas e práticas recomendadas para ajudá-lo a criar aplicativos Web dinâmicos mais acessíveis. Mesmo quando codificado corretamente, no entanto, o conteúdo dinâmico não está necessariamente acessível. [Aplicativos de Internet sofisticados e acessíveis (Aria)](#aria) ajudam a resolver esse problema.  

Para obter mais informações sobre acessibilidade na Web, confira a [introdução à acessibilidade da Web](https://www.w3.org/WAI/intro/accessibility.php) pela [iniciativa de acessibilidade da Web](https://www.w3.org/WAI/) (WAI).

## ARIA
A especificação do Aria ( [aplicativos sofisticados da Internet) acessível](https://www.w3.org/TR/wai-aria/) pela W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) define como uma sintaxe para tornar conteúdo dinâmico da Web e interfaces do usuário personalizadas acessíveis para todas as pessoas. O ARIA estende o HTML usando atributos adicionais (funções, propriedades e Estados) projetados para transmitir semântica personalizada. Esses atributos são usados por navegadores para passar ao longo do estado e da função dos controles para a API de acessibilidade.

### Funções, propriedades e Estados
As funções do ARIA são definidas em elementos usando o [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) atributo para fornecer tecnologias adaptativas e informações sobre APIs de acessibilidade sobre o elemento. Por exemplo, o `<li>` elemento abaixo é atribuído `role="menuitem"` para significar que se trata de um item em um menu.

``` html
<li role="menuitem">Home</li>
```

Os Estados e as propriedades do ARIA são atributos prefixados pelo Aria que fornecem informações específicas sobre um objeto para ajudar a formar a definição da natureza das funções. Propriedades são atributos essenciais para a natureza de um objeto, como [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) e [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Alterar uma propriedade afeta o significado do objeto. No exemplo abaixo, a propriedade `aria-haspopup="true"` é definida em um `<li>` item de menu para significar que ele tem um pop-up.

``` html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Os Estados não alteram a natureza do objeto, mas representam informações associadas ao objeto ou à interação do usuário com o objeto, como [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) ou [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Por exemplo, o estado `aria-checked="false"` no exemplo abaixo representa que a caixa de seleção não está marcada.

``` html
<div role="checkbox" aria-checked="false">Accept</div>
```

Vá para [o modelo de funções](https://www.w3.org/TR/wai-aria-1.1/#roles) pelo W3C para ver uma lista completa de funções, propriedades e Estados.

Para obter mais informações sobre o ARIA, consulte o ARIA na seção [Resources](#resources) .

## Recursos

### Noções básicas sobre acessibilidade
#### [O projeto A11Y](http://a11yproject.com/)
O projeto A11Y é um esforço orientado à Comunidade para facilitar a acessibilidade na Web. Confira [o site de projeto do A11Y](https://a11yproject.com/) para saber mais sobre os princípios básicos de acessibilidade, o padrão acessível e a [biblioteca](https://a11yproject.com/patterns)de widgets e seus [recursos](http://a11yproject.com/resources.html) de acessibilidade software, Blogs, livros e ferramentas.

#### [Iniciativa de acessibilidade da Web (WAI)](https://w3.org/WAI/)
A W3C's Web Accessibility Initiative (WAI) é um esforço para ajudar a melhorar a acessibilidade da Web. O site fornece uma variedade de recursos para [introdução à acessibilidade da Web](https://www.w3.org/WAI/gettingstarted/Overview.html), [design para inclusão](https://www.w3.org/WAI/users/Overview.html), [tutoriais e apresentações](https://www.w3.org/WAI/train.html)e muito mais.

### Blogs sobre acessibilidade
#### [O grupo Paciello Group](https://www.paciellogroup.com/blog/)
O grupo Paciello Group fornece soluções de consultoria e tecnologia a organizações em todo o mundo para garantir que seus clientes atinjam todas as audiências de forma eficaz e eficiente, ao mesmo tempo em que atendem aos padrões governamentais e internacionais. O blog aborda os tópicos como práticas recomendadas de acessibilidade na Web, ferramentas de acessibilidade e tendências de acessibilidade.

#### [Simplesmente acessível](http://simplyaccessible.com/articles/)
Simplesmente acessível é uma equipe de especialistas em acessibilidade que fornecem treinamento de acessibilidade, consultoria e muito mais para alterar a percepção da acessibilidade na Web. A seção de [artigos](http://simplyaccessible.com/articles/) descreve as práticas recomendadas para acessibilidade da Web, design acessível e muito mais.

#### [Grupo SSB BART (SSB)](http://www.ssbbartgroup.com/blog/)
SSB BART Group é uma empresa de acessibilidade digital que oferece suporte a seus clientes no desenvolvimento e implantação de produtos e serviços acessíveis. Seus tópicos de endereços de blog, como práticas recomendadas do ARIA, tendências de acessibilidade, webinars e muito mais.

### Exemplos acessíveis
#### [Ally. js-tutoriais](http://allyjs.io/tutorials/)
Biblioteca JavaScript para ajudar os aplicativos da Web modernos com preocupações com acessibilidade, facilitando a acessibilidade.

#### [Heydonworks-exemplos de ARIA](http://heydonworks.com/practical_aria_examples/)
Exemplos práticos do ARIA para melhorar a acessibilidade do aplicativo

#### [Exemplos de OpenAjax](http://oaa-accessibility.org/)
O website da Aliança OpenAjax é um recurso excelente para verificar as regras do WAI-ARIA e fornece vários exemplos de implementações do WAI-ARIA.

#### [Padrões](http://a11yproject.com/patterns.html)
[O projeto A11Y](http://a11yproject.com/) oferece uma biblioteca de widgets e padrões acessíveis, como menus, botões, dicas de ferramenta e muito mais.

### Técnicas de acessibilidade & ferramentas
#### [Acessibilidade: criando ícones de extensão acessíveis para o Microsoft Edge](../extensions/guides/accessibility.md)
Obtenha orientação sobre como criar ícones de extensões acessíveis para o Microsoft Edge.

#### [Nome acessível e descrição: computação e mapeamentos 1,1](https://www.w3.org/TR/accname-1.1/)
Este documento de mapeamento W3C explica como os navegadores determinam o nome e as descrições dos objetos acessíveis em linguagens de conteúdo da Web e os expõem em APIs de acessibilidade.

#### [Recursos de avaliação de acessibilidade](https://www.w3.org/WAI/eval/Overview.html)
Recursos de avaliação de acessibilidade é um recurso de várias páginas pelo W3C que descreve abordagens diferentes para a avaliação de sites para acessibilidade.

#### [Testes de compatibilidade de tecnologia assistencial](http://www.powermapper.com/tests/)
Resultados de teste mostrando como diferentes tipos de conteúdo e padrões se comportam em tecnologias assistenciais (AT), como leitores de tela.

#### [A criação de sites acessíveis ficou muito mais fácil](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)
Esta postagem de blog de ferramentas e desenvolvimento Web .NET descreve o [Verificador de acessibilidade da Web](https://go.microsoft.com/fwlink/p/?linkid=841539)de extensão do Visual Studio.

#### [Principais mapeamentos de API de acessibilidade 1,1](https://www.w3.org/TR/core-aam-1.1/)
Este documento de mapeamento W3C explica como a semântica de idiomas de conteúdo da Web é exposta a APIs de acessibilidade.  

#### [Verificações fáceis – uma primeira revisão da acessibilidade na Web](https://www.w3.org/WAI/eval/preliminary.html)
Uma série de verificações rápidas do WAI que ajudam você a Asses a acessibilidade de uma página da Web.

#### [Como se adequar à WCAG 2,0](https://www.w3.org/WAI/WCAG20/quickref/)
Uma referência rápida às diretrizes de acessibilidade de conteúdo da Web (WCAG) 2,0 requisitos (critérios de sucesso) e técnicas.

#### [Mapeamentos de API de acessibilidade em HTML 1,0](https://www.w3.org/TR/html-aam-1.0/)
Este documento de mapeamentos do W3C explica como elementos e atributos do HTML 5.1 são mapeados para APIs de acessibilidade de plataforma.


#### [Dicas rápidas](http://a11yproject.com/#Quick-tips)
Uma lista de dicas de desenvolvimento rápido na Web para acessibilidade pelo [projeto A11Y](http://a11yproject.com/).

#### [Verificação de site](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)
A ferramenta de verificação de site no centro de desenvolvimento do Microsoft Edge verifica se há bibliotecas desatualizadas, problemas de layout e problemas de acessibilidade.

#### [Técnicas para WCAG 2,0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)
Técnicas do W3C que fornecem orientação para os desenvolvedores da Web sobre como atender às [diretrizes de acessibilidade do conteúdo da Web (WCAG) 2,0](https://w3.org/TR/WCAG20/) critérios de sucesso.

#### [Dicas sobre o desenvolvimento para acessibilidade pela Web](https://w3.org/WAI/gettingstarted/tips/developing.html)
Dicas do W3C sobre como desenvolver conteúdo da Web que seja mais acessível a pessoas com deficiências.

#### [WAI-práticas de criação do ARIA 1,1](http://w3c.github.io/aria-practices/)
Um documento pelo W3C que fornece aos leitores noções básicas sobre como usar o WAI-ARIA 1,1 e recomenda abordagens para tornar widgets, navegação e comportamentos acessíveis usando funções, Estados e propriedades do WAI-ARIA.

#### [Diretrizes e técnicas do WAI](https://w3.org/WAI/guid-tech.html)
Uma série de diretrizes e normas de acessibilidade pela Web desenvolvida pela WAI.  

#### [Lista de ferramentas de avaliação da Web Accessibility](https://www.w3.org/WAI/ER/tools/index.html)
Uma lista de ferramentas de avaliação de acessibilidade da Web para ajudar a determinar se os sites atendem às diretrizes de acessibilidade.

#### [Perspectivas de acessibilidade na Web: explorar o impacto e os benefícios de todos](https://w3.org/WAI/perspectives/)
Uma série de vídeos de situação curto pelo W3C sobre o impacto da acessibilidade e os benefícios de todos.
