---
description: Iniciando testes para problemas de acessibilidade usando o DevTools
title: Visão geral dos testes de acessibilidade usando o DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: f6ec0652bbbb7d7e60a69877a9d44a7a2fd636a5
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624791"
---
# <a name="overview-of-accessibility-testing-using-devtools"></a>Visão geral dos testes de acessibilidade usando o DevTools

Neste artigo, abrangemos alguns dos recursos que você pode usar no DevTools para testar problemas de acessibilidade.  Passamos pelo uso de diferentes recursos do DevTools para detectar os problemas de acessibilidade em uma página de demonstração e discutimos como corrigi-los.  Abra a [página de][DevToolsA11yErrorsDemopage] demonstração em uma nova guia para testá-la você mesmo e você pode testar junto.

:::image type="complex" source="../media/a11y-testing-basics-demopage.msft.png" alt-text="A página de demonstração usada neste artigo com alguns problemas de acessibilidade" lightbox="../media/a11y-testing-basics-demopage.msft.png":::
    A página de demonstração usada neste artigo com alguns problemas de acessibilidade
:::image-end:::


## <a name="automated-testing-by-using-the-issues-tool"></a>Teste automatizado usando a ferramenta Problemas

Ao abrir a página de demonstração no navegador e abrir o DevTools, observe que alguns problemas são detectados automaticamente no contador **Problemas.**  Selecione o **contador Problemas** \( Contador de problemas \) para abrir a ferramenta ![ Problemas para exibir os problemas e mais ](../media/issues-counter-icon.msft.png) informações. [][DevToolsIssuesTool]

:::image type="complex" source="../media/a11y-testing-issues-tracker.msft.png" alt-text="O contador Problemas mostra quantos problemas há na página da Web atual e abre a ferramenta Problemas" lightbox="../media/a11y-testing-issues-tracker.msft.png":::
    O contador Problemas mostra quantos problemas há na página da Web atual e abre a ferramenta Problemas
:::image-end:::

Para este artigo, nos concentraremos na seção **Acessibilidade** da **ferramenta Problemas.**

:::image type="complex" source="../media/a11y-testing-accessibility-issues.msft.png" alt-text="Avisos de acessibilidade exibidos na ferramenta Problemas" lightbox="../media/a11y-testing-accessibility-issues.msft.png":::
    Avisos de acessibilidade exibidos na ferramenta Problemas
:::image-end:::

Para etapas passo a passo detalhadas, navegue até [Exibir a seção Acessibilidade da ferramenta Problemas.][DevToolsAccessibilityTestIssuesToolViewAccSection]


### <a name="automatically-checking-that-input-fields-have-labels"></a>Verificar automaticamente se os campos de entrada têm rótulos

O primeiro aviso exibido é `Form elements must have labels: Element has no title attribute. Element has no placeholder attribute` .  Quando você expande esta seção e selecione o link Abrir em **Elementos,** a ferramenta **Elements** será aberta, com o elemento realçado na árvore DOM.  A **guia Estilos** mostra o CSS aplicado ao elemento.

Para etapas passo a passo detalhadas, navegue até [Verificar se os campos de entrada têm rótulos][DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels].

:::image type="complex" source="../media/a11y-testing-inspect-problematic-element.msft.png" alt-text="Ferramenta Elements mostrando o HTML problemático após selecionar o link na ferramenta Problemas" lightbox="../media/a11y-testing-inspect-problematic-element.msft.png":::
    Ferramenta Elements mostrando o HTML problemático após selecionar o link na ferramenta Problemas
:::image-end:::

Nesse caso, o HTML tem `label` um elemento que não funciona.

```html
<label>Search</label>
<input type="search">
<input type="submit" value="go">
```

O uso do elemento aqui está errado, porque não há nenhuma conexão `label` entre o elemento e o `label` `input` elemento.  Um rótulo HTML válido colocaria o foco na caixa de texto de entrada de pesquisa quando você selecionasse **o rótulo de** pesquisa. 

Você pode resolver esse problema aninhando o elemento em um elemento ou adicionando um atributo que aponta para um `input` `label` atributo do `for` `id` `input` elemento.  Para exibir uma conexão correta, selecione **o outro** rótulo no formulário de doação.

Você também pode selecionar os links explicativos na **ferramenta Problemas** para obter essas informações.

:::image type="complex" source="../media/a11y-testing-more-information-links.msft.png" alt-text="Links na ferramenta Problemas apontando para informações mais detalhadas sobre o problema" lightbox="../media/a11y-testing-more-information-links.msft.png":::
    Links na ferramenta **Problemas** apontando para informações mais detalhadas sobre o problema
:::image-end:::


### <a name="automatically-checking-that-images-have-alt-text"></a>Verificar automaticamente se as imagens têm texto alt

O outro problema detectado automaticamente é que muitas das imagens na página não têm texto alternativo.  Se você expandir o `Images must have alternate text: Element has no title attribute` aviso, você obterá quatro instâncias de imagens com esse problema.

:::image type="complex" source="../media/a11y-testing-images-without-alt.msft.png" alt-text="A ferramenta Problemas, relatando imagens com texto alternativo ausente" lightbox="../media/a11y-testing-images-without-alt.msft.png":::
    A **ferramenta Problemas,** relatando imagens com texto alternativo ausente
:::image-end:::

Para etapas passo a passo detalhadas, navegue até [Verificar se as imagens têm texto alt][DevtoolsAccessibilityTestIssuesToolCheckAltText].


### <a name="automatically-checking-that-text-colors-have-enough-contrast"></a>Verificar automaticamente se as cores de texto têm contraste suficiente

A **ferramenta Issues** também relata quando dois elementos na página não têm contraste suficiente.

:::image type="complex" source="../media/a11y-testing-contrast-issues.msft.png" alt-text="Problemas de contraste relatados na ferramenta Problemas" lightbox="../media/a11y-testing-contrast-issues.msft.png":::
    Problemas de contraste relatados na **ferramenta Problemas**
:::image-end:::

A **ferramenta Issues** fornece explicações detalhadas sobre o aviso.  Quando você faz uma sonda, você tem uma lista dos elementos que têm esse problema.  Na ferramenta **Problemas,** selecionar um link que aponta para um elemento realça esse elemento na página renderizada.

:::image type="complex" source="../media/a11y-testing-element-with-contrast-issues.msft.png" alt-text="Elemento na página realçada após selecionar o link para ele" lightbox="../media/a11y-testing-element-with-contrast-issues.msft.png":::
    Elemento na página realçada após selecionar o link para ele
:::image-end:::

Para etapas passo a passo detalhadas, navegue até Verificar se as cores do texto [têm contraste suficiente.][DevtoolsAccessibilityTestIssuesToolCheckContrast]


### <a name="verify-that-the-webpage-layout-is-usable-when-narrow"></a>Verifique se o layout da página da Web é acessível quando estreito

<!-- by design, this section doesn't have a corresponding how-to article -->

Uma parte importante da acessibilidade é garantir que seus produtos Web funcionem bem em um viewport estreito. Muitos usuários precisam ampliar a página para poder usá-la, e isso significa que não há muito espaço. Quando não houver espaço suficiente, o layout de várias colunas deve se transformar em um layout de coluna única, com o conteúdo colocado em uma ordem compreensível. Isso significa colocar o conteúdo mais importante na parte superior da página e colocar conteúdo adicional mais adiante na página.

Ao tornar a janela do navegador estreita e usar as teclas de seta para rolar a página, você pode ver que a barra de navegação superior da página de demonstração tem alguns problemas de acessibilidade.  A barra de navegação superior se sobrepõe ao formulário **de** Pesquisa, conforme mostrado na imagem anterior, e esse problema precisa ser corrigido.

Você pode simular um modo de exibição estreito ressaltando a janela do navegador, mas uma maneira melhor de testar a capacidade de resposta do seu design é usar a ferramenta **de Emulação de** Dispositivo.  Aqui estão alguns recursos da ferramenta **de Emulação de** Dispositivos que ajudam você a encontrar problemas de acessibilidade de qualquer site:

*  Sem ressizing the browser window, resize a página e teste se suas consultas de [mídia CSS][DevToolsMediaQueries] disparam uma alteração no layout.
*  Verifique se há dependências que usam um mouse. Por padrão, a emulação de dispositivo assume um dispositivo touch. Isso significa que qualquer funcionalidade do seu produto que depende da interação de foco não funcionará. 
*  Faça testes visuais simulando diferentes dispositivos, níveis de zoom e taxas de pixel.
*  Teste como seu produto se comporta em conexões não confiáveis ou quando o usuário está offline.  Mostrar as interações mais importantes para um usuário em uma conexão lenta também é uma consideração de acessibilidade.

Para saber mais sobre a **ferramenta emulação** de dispositivos, navegue até Emular dispositivos móveis [Microsoft Edge DevTools][DevToolsDeviceModeIndex].


### <a name="wavy-underlines-in-the-dom-tree-indicate-automatically-detected-issues"></a>Sublinhados ondulados na árvore DOM indicam problemas detectados automaticamente

A árvore DOM na ferramenta **Elements** sinaliza automaticamente problemas diretamente no HTML adicionando um sublinhado ondulado.  Se você tiver qualquer elemento que tenha um sublinhado `Shift` + `click` ondulado, a **ferramenta Issues** será aberta.

:::image type="complex" source="../media/a11y-testing-wavy-underlines.msft.png" alt-text="Um elemento que é mostrado com sublinhado ondulado na árvore DOM tem problemas.  Shift+clique no elemento para chegar diretamente ao problema" lightbox="../media/a11y-testing-wavy-underlines.msft.png":::
    Um elemento que é mostrado com sublinhado ondulado na árvore DOM tem problemas.  `Shift`+`click` o elemento para chegar diretamente ao problema.
:::image-end:::

Esses problemas encontrados pela ferramenta **Issues** são alguns problemas de acessibilidade relativamente óbvios que podem ser evitados.  Usar a **ferramenta Issues** e suas explicações guiadas para corrigi-los define você no caminho para um produto acessível.


## <a name="limits-of-automated-testing"></a>Limites de testes automatizados

As [ferramentas Problemas,][DevToolsIssuesTool] [Acessibilidade Insights][AccessibilityInsights]e o [Farol][Lighthouse] são ferramentas que geram automaticamente um relatório de acessibilidade para uma página da Web.  Obter um relatório automatizado dessas ferramentas é apenas o início de sua jornada de teste de acessibilidade.

A acessibilidade se trata da interação humana, pessoas com necessidades diferentes usando seus produtos em vários ambientes técnicos.  Esse teste não pode ser totalmente automatizado, mas precisa de verificação por um humano navegando o produto.  No melhor cenário, você teria acesso a testadores com necessidades de acessibilidade diferentes e testadores usando vários ambientes.  Mas você já pode fazer muito sozinho usando o teclado para navegar e inspecionando diferentes partes da página.

Na página de demonstração, há problemas adicionais que os testes automatizados não podem detectar, incluindo: 

*  Problemas que surgem depois que você interage com a página. 
*  Problemas relacionados a alterações em exibição, como tornar a janela estreita.

Um desses problemas é o formulário de doação.  Quando você usa um mouse, você pode clicar nas diferentes opções para doar dinheiro.  Mas quando você tenta usar o teclado para acessar o formulário de doação, nada acontece. Para resolver esse problema, você precisa usar a **ferramenta Inspecionar.**

:::image type="complex" source="../media/a11y-testing-basics-donation-form-issue.msft.png" alt-text="Formulário de doação na página de demonstração é realçado" lightbox="../media/a11y-testing-basics-donation-form-issue.msft.png":::
    Formulário de doação na página de demonstração é realçado
:::image-end:::


## <a name="using-the-inspect-tool-to-detect-accessibility-issues"></a>Usando a ferramenta Inspecionar para detectar problemas de acessibilidade

Use a **ferramenta Inspecionar** para detectar problemas de acessibilidade, pairando sobre partes da página da Web.  A **ferramenta Inspecionar** \( Inspecionar ![ ](../media/inspect-icon.msft.png) \) está no canto superior esquerdo do DevTools.  Acione a ferramenta Inspecionar selecionando o botão **Inspecionar** ferramenta.

:::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Acione a ferramenta Inspecionar selecionando o botão Inspecionar ferramenta" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
    Acione a ferramenta **Inspecionar** selecionando o botão **Inspecionar** ferramenta
:::image-end:::

Depois de selecionar o **botão Inspecionar** ferramenta, você pode mover o ponteiro sobre qualquer elemento na página renderizada.  A ferramenta Inspect mostra o layout do elemento como uma sobreposição de flexbox multicolorida e mostra detalhes do elemento como uma sobreposição de informações semelhante a uma dica de ferramenta.

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Sobreposição de flexbox multicolor e sobreposição de informações ao usar a ferramenta Inspecionar" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    Sobreposição de flexbox multicolor e sobreposição de informações ao usar a **ferramenta Inspecionar**
:::image-end:::

A seção Inspecionar **Acessibilidade** da ferramenta inclui uma linha **Contraste,** quando aplicável.

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="A seção Inspecionar Acessibilidade da ferramenta inclui uma linha Contraste, quando aplicável" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    A seção Inspecionar **Acessibilidade** da ferramenta inclui uma linha **Contraste,** quando aplicável
:::image-end:::

Para etapas passo a passo detalhadas, navegue até Identificar regiões [aninhadas usando realçamento de cores][DevtoolsAccessibilityTestInspectToolColorHighlighting].
<!-- = test-inspect-tool.md##identify-nested-regions-using-color-highlighting -->

A seção superior da sobreposição de informações da ferramenta **Inspect** exibe as seguintes informações:

* Tipo de layout; se o elemento estiver posicionado usando uma flexbox ou grade, você verá um ícone apropriado \(![Ícone de layout de grade](../media/grid-icon.msft.png)\).
* O nome do elemento, como **um**, **h1**ou **div**.
* As dimensões do elemento, em pixels.
* A cor, como uma amostra de cores (um quadrado pequeno e colorido) e como um valor formatado (como `#336699` ).
* Informações de fonte (famílias de tamanho e fonte).
* Margem e preenchimento, em pixels.

A **parte Acessibilidade** da sobreposição **Inspecionar** é descrita na seção a seguir.


### <a name="checking-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a>Verificar elementos individuais para contraste de texto, texto do leitor de tela e suporte ao teclado

A **seção Acessibilidade** da sobreposição **Inspecionar** contém as seguintes linhas:

*   **Contraste** define se um elemento pode ser compreendido por pessoas com visão prejudicada.
    *   A [taxa de][W3CContrastRatio] contraste, conforme definido pelas Diretrizes do [WCAG,][WCAG] indica se há contraste suficiente entre as cores de texto e plano de fundo.  Um ícone de marca de verificação verde indica que há contraste suficiente, e um ícone de ponto de exclamação laranja indica que não há contraste suficiente.

*   **Nome** e **função** indicam qual tecnologia auxiliar de informações, como leitores de tela, relatará sobre o elemento.
    *   O **Nome** é o conteúdo de texto de um `a` elemento.  Para o elemento `<a href="/">About Us</a>` , **o nome** mostrado na ferramenta Inspecionar é "Sobre nós".
    *   A **função** do elemento.  A **função** geralmente é o nome do elemento, como `article` , , ou `img` `link` `heading` .  Os `div` elementos e são `span` representados como `generic` .

*   **O foco no teclado** indica se os usuários podem alcançar o elemento usando dispositivos de entrada diferentes de um mouse.
    *   Um ícone de marca de verificação verde indica que o elemento é focalizado no teclado.
    *   Um círculo cinza com linha diagonal indica que o elemento não é focalizado no teclado.

Para etapas passo a passo detalhadas, navegue até Verificar elementos individuais para contraste de texto, texto do leitor de tela [e suporte ao teclado.][DevtoolsAccessibilityTestInspectToolIndivElems]
<!-- = test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support -->


### <a name="using-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a>Usando a ferramenta Inspecionar para passar o mouse sobre a página da Web para realçar o DOM e CSS

Ao usar a **ferramenta Inspecionar,** selecionar um elemento na página renderizada abre a **ferramenta Elements.**  A árvore DOM mostra o HTML do elemento e **Styles** mostra as propriedades CSS que são aplicadas ao elemento.

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Detalhes sobre o elemento selecionado exibido na ferramenta Elements" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    Detalhes sobre o elemento selecionado exibido na ferramenta Elements
:::image-end:::

Ao usar a **ferramenta Inspecionar,** à medida que **** você passar o mouse sobre diferentes partes da página renderizada com Elementos abertos, você notará que a árvore DOM é atualizada automaticamente.

Para etapas passo a passo detalhadas, navegue até Usar a ferramenta Inspecionar para passar o mouse sobre a página da Web para [realçar o DOM e CSS][DevtoolsAccessibilityTestInspectToolDomCss].
<!-- = test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css -->


## <a name="verify-keyboard-support-by-using-the-tab-and-enter-keys"></a>Verificar o suporte ao teclado usando as teclas Tab e Enter

Nem todas as pessoas usam dispositivos de ponteiro ou toque, e algumas pessoas podem ter baixa visão. Para atender a esses cenários, certifique-se de que as UIs funcionem com teclados.

Você pode testar usando um teclado para navegar na página, usando `Tab` ou `Shift+Tab` pulando de elemento para elemento.  Se você pressionar na página de demonstração, a primeira coisa que recebe o foco é o formulário de Pesquisa `Tab` no header da página. ****  Pressionar até permite que você envie o formulário, para que isso funcione, apesar do problema de rótulo que descobrimos anteriormente `Enter` ao usar a ferramenta **Issues.**

Para etapas passo a passo detalhadas, navegue até Verificar se há suporte ao teclado usando as [teclas Tab e Enter.](test-tab-enter-keys.md)

Quando você pressiona em vez de , o próximo elemento que obtém o foco é o primeiro link Mais na seção de conteúdo da página, conforme `Tab` indicado por um `Enter` contorno. ****

:::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navegando a página usando a tecla Tab.  O foco é mostrado em um link Mais na página." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
    Navegando a página usando a `Tab` chave.  O foco é mostrado em um link **Mais** na página.
:::image-end:::

Depois que você passa pelo último link **Mais,** a página rola para cima e não está claro qual elemento tem foco.

Se você olhar para a parte inferior esquerda da tela ou se usar um leitor de tela, poderá dizer que o link azul **Gatos** no menu de navegação da barra lateral tem foco, pois o navegador mostra a URL `#cats` .

:::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="A falta de estilo de foco torna impossível saber onde você está atualmente na página.  A única dica é a exibição do destino do link na parte inferior esquerda da janela." lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
    A falta de estilo de foco torna impossível saber onde você está atualmente na página.  A única dica é a exibição do destino do link na parte inferior esquerda da janela.
:::image-end:::

Selecionar novamente o leva à caixa de `Tab` texto de entrada do formulário de doação.  No entanto, você não pode alcançar **os 50**, **100** ou **200** botões acima da caixa de texto de entrada.  Além disso, quando o foco está na caixa de texto de entrada, a seleção `Enter` não envia o formulário.

:::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="O único elemento acessível ao teclado no formulário de doação é o campo de texto de entrada" lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
    O único elemento acessível ao teclado no formulário de doação é o campo de texto
:::image-end:::

Selecionar novamente coloca o foco na barra de navegação superior, onde você pode selecionar ir para uma seção diferente da página ou `Tab` uma página diferente do `Enter` site.  Você sabe em qual elemento você está, porque há um contorno de foco.  Para selecionar um link na barra de navegação superior, use ou coloque o foco em um `Tab` `Shift+Tab` link e selecione `Enter` .

:::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="A barra de navegação superior tem um destaque e um contorno de foco e, portanto, é acessível ao teclado" lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
    A barra de navegação superior tem um destaque e um contorno de foco e, portanto, é acessível ao teclado
:::image-end:::

Encontramos alguns problemas aqui para corrigir:

* O menu de navegação da barra lateral não mostra aos usuários onde o foco está, ao usar teclados para se mover `Tab` na página.
* No formulário de doação, os botões **50, 100, ** e **200** e a funcionalidade de envio de formulário não funcionam ao usar o teclado.
* A ordem de tabulação do teclado está incorreta. A `Tab` chave navega por todos os links **Mais** na página antes do menu de navegação da barra lateral.  Essa ordem não é útil porque a navegação na barra lateral se destina a levá-lo para as `Tab` diferentes seções dessa página. 

Vamos analisar esses problemas usando o DevTools.


## <a name="analyze-keyboard-accessibility-issues-using-devtools"></a>Analisar problemas de acessibilidade de teclado usando o DevTools


### <a name="analyzing-the-lack-of-indication-of-keyboard-focus-in-the-sidebar-menu"></a>Analisando a falta de indicação do foco do teclado no menu da barra lateral

Para descobrir por que a navegação de barra lateral não é otimizada conforme o esperado para uso com teclados, comece usando a ferramenta **Inspecionar** para realçar um link no menu de navegação da barra lateral e, em seguida, faça uma sonda na árvore DOM para o `a` elemento. 

:::image type="complex" source="../media/a11y-testing-menu-link.msft.png" alt-text="Inspecionar o código-fonte e os estilos aplicados de um link no menu de navegação da barra lateral" lightbox="../media/a11y-testing-menu-link.msft.png":::
    Inspecionar o código-fonte e os estilos aplicados de um link no menu de navegação da barra lateral
:::image-end:::

Na guia **Estilos,** você pode ver o CSS aplicado ao link e, se você selecionar o link para , o arquivo será aberto na `styles.css` ferramenta **Fontes.**

:::image type="complex" source="../media/a11y-testing-menu-link-styles.msft.png" alt-text="Os estilos que são aplicados ao link, mostrados na ferramenta Sources" lightbox="../media/a11y-testing-menu-link-styles.msft.png":::
    Os estilos que são aplicados ao link, mostrados na ferramenta Sources
:::image-end:::

No exemplo acima, os estilos da página incluem um estado no item de menu quando você usa um mouse, mas não há estado no CSS para usuários `hover` `focus` de teclado.  

Além disso, neste exemplo, os links usam `outline: none` . Esse estilo é usado para remover o contorno que é adicionado automaticamente pelos navegadores aos elementos quando eles têm foco e teclados são usados.  Para evitar esse problema, não use `outline: none` .

Para etapas passo a passo detalhadas, navegue até Analisar a falta de indicação do foco do [teclado em um menu de barra lateral](test-analyze-no-focus-indicator.md).


### <a name="analyzing-the-lack-of-keyboard-support-in-the-donation-form"></a>Analisando a falta de suporte ao teclado no formulário de doação

Os botões no formulário de doação são implementados usando o elemento, que não é reconhecido pelas ferramentas de teste automatizadas como um `div` controle em um formulário.

Para investigar isso, você pode usar a **ferramenta Inspecionar** para passar o mouse sobre os botões do formulário de doação.  O resultado é que nenhum deles é acessível ao teclado, **** conforme indicado pelo anel cinza na linha de foco do teclado da sobreposição de informações.  Conforme mostrado nas **** linhas **Nome** e Função da sobreposição de informações, os botões do formulário de doação também não têm nome e têm uma função de (representando ou elementos), o que significa que eles não estão acessíveis à tecnologia `generic` `div` `span` assistiva.

:::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Inspecionar os botões do formulário mostra que eles não são acessíveis ao teclado" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
    Inspecionar os botões do formulário mostra que eles não são acessíveis ao teclado
:::image-end:::

Para etapas passo a passo detalhadas, navegue até Analisar a [falta de suporte ao teclado em um formulário](test-analyze-no-keyboard-support.md).

Se você selecionar o **botão Doar,** a ferramenta **Inspecionar** o leva para a ferramenta **Elementos** e mostra o HTML do formulário.

```HTML
<div class="donationrow">
    <div class="donationbutton">50</div>
    <div class="donationbutton">100</div>
    <div class="donationbutton">200</div>
</div>
<div class="donationrow">
    <label for="freedonation">Other</label>
    <input id="freedonation" class="smallinput">
</div>
<div class="donationrow">
    <div class="submitbutton">Donate</div>
</div>
```

O uso dos `label` elementos e são válidos, o que resulta no rótulo funcionando conforme o pretendido e a caixa de texto é acessível `input` `input` ao teclado.  O restante do formulário usa elementos, que são fáceis `div` de usar, mas não têm significado semântico.

Em seguida, vamos analisar a funcionalidade JavaScript do formulário. Em **Elementos,** selecione a guia **Ouvintes de** Eventos para analisar o JavaScript do formulário.

:::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="A guia Ouvintes de Eventos, com um link para o JavaScript para o formulário" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
    A **guia Ouvintes de** Eventos, com um link para o JavaScript para o formulário
:::image-end:::

Na guia **Ouvintes de** Eventos, selecione o link para abrir a ferramenta Fontes e inspecione o JavaScript responsável pela `buttons.js:18` funcionalidade do formulário. ****

:::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="O JavaScript responsável pela funcionalidade do formulário de doação, mostrado na ferramenta Sources" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
    O JavaScript responsável pela funcionalidade do formulário de doação, mostrado na ferramenta **Sources**
:::image-end:::

O `click` uso de eventos com botões é recomendado porque os eventos funcionam com `click` ponteiros do mouse e teclados.  No entanto, como um elemento não é acessível ao teclado e o botão Doar é implementado como um elemento, esse JavaScript só é executado `div` quando um mouse é **** `div` usado.

Usar um botão como um é um exemplo clássico em que JavaScript extra é necessário para `div` criar a funcionalidade que os elementos `button` fornecem. Como resultado, isso leva a uma experiência inacessível.


### <a name="checking-the-accessibility-tree-for-keyboard-and-screen-reader-support"></a>Verificando a Árvore de Acessibilidade para suporte a teclado e leitor de tela

Usar a **ferramenta Inspecionar** para verificar individualmente cada elemento na página é demorado.  Em vez disso, use a guia **Acessibilidade** para navegar na Árvore de Acessibilidade **da página.**  A Árvore de Acessibilidade indica quais informações a página fornece para tecnologias assistivas, como leitores de tela.

:::image type="complex" source="../media/a11y-testing-accessibility-tree.msft.png" alt-text="Botão Formulário de doação na Árvore de Acessibilidade" lightbox="../media/a11y-testing-accessibility-tree.msft.png":::
    Botão Formulário de doação na Árvore **de Acessibilidade**
:::image-end:::

Qualquer elemento na árvore que não tenha um nome ou que tenha uma função de , é um problema, porque esse elemento não estará disponível para usuários de teclado ou para pessoas que usam tecnologia `generic` assistida.

Para etapas passo a passo detalhadas, navegue até Verificar a Árvore de Acessibilidade para suporte a teclado e [leitor de tela.](test-accessibility-tree.md)


### <a name="analyzing-the-order-of-keyboard-access-to-sections-of-the-page"></a>Analisando a ordem de acesso do teclado às seções da página

Outro problema é a ordem de tabulação não clara na página.  Os usuários de teclado só chegam ao menu de navegação da barra lateral depois de fazer a tabulação de todos os links **Mais** em toda a página.  Neste exemplo, o menu de navegação da barra lateral destina-se a ser um atalho para diferentes seções dessa página.  Essa ordem de tabulação leva a uma experiência de usuário ruim. 

O motivo da ordem `Tab` confusa é que ela é determinada pela ordem de origem do documento.  A ordem de tabulação também pode ser modificada usando o atributo em um elemento que tira esse elemento `tabindex` da ordem de origem padrão.

No código-fonte do documento, o menu de navegação da barra lateral é exibido após o conteúdo principal da página.  O menu de navegação da barra lateral aparece acima do conteúdo principal da página apenas porque o menu de navegação da barra lateral foi posicionado usando CSS.

A ordem de origem de um documento é importante para a tecnologia assistida e pode ser diferente da ordem na qual os elementos aparecem na página renderizada.  Usando CSS, você pode re-ordenar elementos de página de forma visual, mas isso não significa que tecnologias assistivas, como leitores de tela, representariam elementos de página na mesma ordem que o CSS.

Você pode testar a ordem dos elementos de página usando o Visualizador de Ordem **de Origem** na guia **Acessibilidade.**  Role para baixo todo o caminho e selecione a caixa de seleção **Mostrar Ordem** de Origem.  Agora, quando você navega pela árvore DOM na ferramenta **Elementos,** como selecionar o elemento, sobreposições numéricas são exibidas em seções da página renderizada que representam a `header` ordem de origem. 

:::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="A ação do Visualizador de Ordem de Origem mostra a ordem dos elementos no código-fonte como sobreposições numéricas na página" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
    A ação do **Visualizador** de Ordem de Origem mostra a ordem dos elementos no código-fonte como sobreposições numéricas na página
:::image-end:::

Para obter etapas passo a passo detalhadas, navegue até Testar o suporte ao [teclado usando o Visualizador de Ordem de Origem](test-tab-key-source-order-viewer.md).


## <a name="testing-contrast-of-text-colors-in-various-states"></a>Testar contraste de cores de texto em vários estados

A **ferramenta Inspecionar** relata problemas de acessibilidade para um estado de cada vez.  Primeiro, descreveremos a limitação de uso da ferramenta Inspecionar para exibir apenas o estado estático de um elemento page.  Em seguida, explicaremos como inspecionar outros estados de um elemento de página selecionando **\:hov (Estado** do Elemento Toggle) na guia **Estilos.**

### <a name="checking-text-color-contrast-in-the-default-state"></a>Verificando o contraste de cor do texto no estado padrão

Além dos testes automáticos de contraste de cor na ferramenta **Problemas,** você também pode usar a ferramenta **Inspecionar** para verificar se elementos de página individuais têm contraste suficiente.  Se as informações de contraste estão disponíveis, a sobreposição **Inspecionar** mostra a taxa de contraste e um item de caixa de seleção.  Um ícone de marca de verificação verde indica que há contraste suficiente, e um ícone de alerta amarelo indica que não há contraste suficiente.

Por exemplo, os links no menu de navegação da barra lateral têm contraste suficiente, mas o item de lista verde **Cachorros** na seção **Status** de Doação não.  Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição **Inspecionar.**

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Os links no menu de navegação da barra lateral têm contraste suficiente, conforme mostrado na sobreposição Inspecionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Os links no menu de navegação da barra lateral têm contraste suficiente, conforme mostrado na sobreposição **Inspecionar** :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição Inspecionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Um elemento que não tem contraste suficiente é sinalizado por um aviso na sobreposição **Inspecionar** :::image-end:::
    :::column-end:::
:::row-end:::

Usar a **ferramenta Inspecionar** dessa forma não testa totalmente seus elementos. Os elementos na página podem ter estados diferentes, todos eles precisam ser testados. Por exemplo, se você passar o mouse sobre o menu de navegação da barra lateral, observe a animação que altera a cor dos links.

:::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="O item de menu mostrando cores diferentes quando o ponteiro do mouse está sobre ele" lightbox="../media/a11y-testing-hover.msft.png":::
    O item de menu mostrando cores diferentes quando o ponteiro do mouse está sobre ele
:::image-end:::

### <a name="verify-accessibility-of-all-states-of-elements-such-as-the-contrast-on-hover"></a>Verificar a acessibilidade de todos os estados de elementos, como o contraste no foco

Ao usar o DevTools, você precisará simular todos os estados do elemento, pois a ferramenta **Inspecionar** não exibe informações para todos os estados ao mesmo tempo. Neste exemplo, ao usar a ferramenta **Inspecionar,** você não pode alcançar o estado do link Gatos no menu de navegação da barra lateral para analisar a taxa de contraste em um estado, porque o estado em seus estilos não é `hover` **** `hover` `hover` disparado.  Em vez disso, você precisa simular o estado do item de menu **Gatos,** usando a simulação de estado na **guia Estilos.**

Para etapas passo a passo detalhadas, navegue até [Verificar a acessibilidade de todos os estados de elementos](test-inspect-states.md).

Acione a **ferramenta Inspecionar** e, na página renderizada, selecione o link **azul Gatos** no menu de navegação da barra lateral.  A **ferramenta Elements** é aberta, com o elemento selecionado na árvore `a` DOM.  Se necessário, na árvore DOM, navegue até o elemento que tem um `hover` estado no CSS.  Nesse caso, o `a` elemento tem um `hover` estado.

:::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspecionar o elemento que tem um estado de foco na ferramenta Elements" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
    Inspecionar o elemento que tem um estado de foco na ferramenta Elements
:::image-end:::

Na guia **Estilos,** selecione **o botão \:hov (Estado do Elemento Toggle).**  Em **seguida,** use as caixas de seleção estado do elemento Force para escolher qual estado simular.

:::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="O recurso de simulação de estado mostrando todas as opções" lightbox="../media/a11y-testing-state-simulation.msft.png":::
    O recurso de simulação de estado mostrando todas as opções
:::image-end:::

Selecione a **caixa de seleção \:hover.**  Um ponto amarelo agora aparece ao lado do elemento DOM, indicando que o elemento DOM tem um estado simulado.  Além disso, o link **Gatos** no menu de navegação da barra lateral agora é realçado na página, como se o ponteiro do mouse estivesse pairando sobre ele.

:::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulando um estado de foco" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
    DevTools simulando um estado de foco
:::image-end:::

Depois que o estado simulado for aplicado, você poderá usar a ferramenta **Inspecionar** novamente para verificar o contraste do elemento quando o usuário passar o mouse sobre ele.  Nesse caso, o contraste não é alto o suficiente.

:::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Testar o contraste de um elemento em um estado de foco simulado" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
    Testar o contraste de um elemento em um estado de foco simulado
:::image-end:::

A simulação de estado também é uma boa maneira de verificar se você considera diferentes necessidades do usuário.  Para o menu de navegação da barra lateral, você pode detectar que o `:focus` estado tem um problema de contraste.


## <a name="use-the-rendering-tool-to-test-accessibility-for-visual-impairment"></a>Use a ferramenta Rendering para testar a acessibilidade para deficiência visual

### <a name="check-contrast-issues-with-dark-theme-and-light-themes"></a>Verificar problemas de contraste com temas escuros e claros

Outra consideração quando se trata de acessibilidade de cores é que pode haver temas diferentes que você precisa testar para problemas de contraste.  A maioria dos sistemas operacionais tem um modo escuro e um modo claro.  Sua página da Web pode reagir a essas configurações diferentes usando consultas de mídia CSS.

Esta página de demonstração tem um tema claro e escuro.  Você pode testar os dois temas sem alterar seu sistema operacional usando [a][DevToolsColorSchemeSimulation] simulação de esquema de cores escuro ou claro na ferramenta **Rendering.**  Até o momento, este artigo analisou a página de demonstração com um sistema operacional usando uma configuração de tema escuro.  Se simularmos um esquema de luz e atualizarmos a página, a ferramenta **Issues** mostrará seis problemas de contraste de cor em vez de dois.

Para etapas passo a passo detalhadas, navegue até Verificar se há problemas de contraste com [tema escuro e tema claro.](test-dark-mode.md)


Ao alternar para um tema claro na ferramenta **Rendering,** observe os itens a seguir.

*  Novos problemas de contraste são detectados devido à alteração do tema claro.
*  Toda a **seção Status** da Doação da página é ilegível no modo claro.

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png" alt-text="Novos problemas de contraste detectados devido à alteração para tema claro" lightbox="../media/a11y-testing-new-contrast-issues-in-light-mode.msft.png":::
            Novos problemas de contraste detectados devido à alteração para tema claro :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-donation-state-light-contrast.msft.png" alt-text="Os itens de status de doação sinalizados como problemas de contraste quando no modo claro" lightbox="../media/a11y-testing-donation-state-light-contrast.msft.png":::
            Os itens de status de doação sinalizados como problemas de contraste quando no modo claro :::image-end:::
    :::column-end:::
:::row-end:::


### <a name="verify-that-the-webpage-is-usable-by-people-with-color-blindness"></a>Verifique se a página da Web pode ser usável por pessoas com falta de cor

Os diferentes estados de doações usam cor (vermelho, verde, amarelo) como o único meio de diferenciar entre os estados de financiamento.  No entanto, não é possível esperar que todos os usuários experimentem essas cores conforme o pretendido.  Se você usar o recurso de [emulação][DevToolsVisionDeficiencies] de deficiências de visão do DevTools, poderá descobrir que isso não é bom o suficiente, simulando como as pessoas com visão diferente perceberiam seu design.
Para etapas passo a passo detalhadas, navegue até Verificar se a página pode ser [usável por pessoas com visão de cor](test-color-blindness.md).
:::image type="complex" source="../media/a11y-testing-simulating-protanopia.msft.png" alt-text="Mostrar a página como alguém com protanopia (cegueira de cor vermelha) a verá" lightbox="../media/a11y-testing-simulating-protanopia.msft.png":::
    Mostrando a página como se alguém com protanopia (cegueira de cor vermelha) a veja
:::image-end:::



### <a name="verify-that-the-webpage-is-usable-with-blurred-vision"></a>Verifique se a página da Web é usável com visão desfocado

Outro recurso interessante da ferramenta **Rendering** é que você pode simular a visão desfocado.  Se escolhermos **** a opção de **** visão desfocado na lista lista suspenso Deficiências de visão emular, podemos ver que a sombra de soltar no texto no menu superior dificulta a leitura dos itens do menu.
Para etapas passo a passo detalhadas, navegue até Verificar se a [página pode ser usável com visão desfocado](test-blurred-vision.md).

:::image type="complex" source="../media/a11y-testing-simulating-blur.msft.png" alt-text="Simular uma página desfocado pode revelar problemas de acessibilidade" lightbox="../media/a11y-testing-simulating-blur.msft.png":::
    Simular uma página desfocado pode revelar problemas de acessibilidade
:::image-end:::


### <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off-reduced-motion"></a>Verifique se a página pode ser usável com a animação da interface do usuário desligada (movimento reduzido)

Outra configuração que os sistemas operacionais vêm com esses dias é uma maneira de desativar animações.  As animações podem ajudar a usabilidade de um produto, mas também podem causar muitos problemas, desde confusão até enjoo. É por isso que seus produtos não devem mostrar animações aos usuários que as desligaram no sistema operacional.  Usando uma consulta de mídia CSS, você pode verificar se o usuário deseja ver animações e a desativar de acordo.  E, assim como no modo escuro e claro, há uma maneira de simular o movimento [reduzido usando DevTools][DevToolsReducedMotion].

Na página de demonstração aqui, desligar animações interromperá a rolagem suave da página quando você selecionar diferentes partes do menu de navegação da barra lateral.  Isso é obtido envolvendo a configuração de rolagem suave em CSS em uma consulta de mídia:

:::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulando o movimento reduzido e o CSS que garante que a rolagem suave só acontece quando o usuário o deseja" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
    Simulando o movimento reduzido e o CSS que garante que a rolagem suave só acontece quando o usuário o deseja
:::image-end:::

```css
@media (prefers-reduced-motion: no-preference) {
  html {
    scroll-behavior: smooth;
  }
}
```

Esta consulta de mídia CSS executa condicionalmente a animação "rolagem suave".  Mas a animação da barra de navegação superior, o menu de navegação na barra lateral e mais **links** ainda são executados, mesmo quando o usuário não deseja ver animações. Essas outras animações precisam ser executados condicionalmente, como adicionando consultas de mídia adicionais.

Para etapas passo a passo detalhadas, navegue até Verificar se a página pode ser usável com a [animação da interface do usuário desligada](test-reduced-ui-motion.md).


## <a name="what-to-do-next"></a>O que fazer em seguida?

Abordamos algumas ferramentas que você pode usar para garantir que você pegue problemas de acessibilidade em seus produtos.  Essas ferramentas variam de verificações automatizadas e verificações de detalhes manuais até a simulação de diferentes estados e ambientes.  Essas ferramentas são resumidas nos recursos [de teste de acessibilidade no DevTools](reference.md).  As ferramentas automatizadas não conseguem encontrar todos os problemas em um produto, pois muitas das barreiras de acessibilidade aparecem somente durante o uso interativo.

Nenhuma dessas ferramentas pode substituir uma rodada adequada de teste de seus produtos por pessoas que usam tecnologias assistivas e seguir um plano para verificar todos os testes necessários. Você também pode usar o [recurso Avaliações][AccessibilityInsightsAssessment] de [Acessibilidade Insights][AccessibilityInsights].  Talvez seja necessário executar verificações adicionais, como:

* Teste quando ampliado.
* Teste com leitores de tela.
* Teste com reconhecimento de voz.
* Teste no modo de alto contraste.

Outra maneira de descobrir o que fazer para melhorar seu produto Web é usar a extensão [webhint para][WebhintForCode]Visual Studio Code .  Essa extensão sinaliza os problemas de acessibilidade detectáveis prontamente em seu código-fonte e fornece informações sobre como corrigi-los.

:::image type="complex" source="../media/a11y-testing-webhint-in-vs-code.msft.png" alt-text="Webhint no Visual Studio Code, mostrando um problema de acessibilidade sublinhando o elemento HTML e mostrando uma explicação do problema" lightbox="../media/a11y-testing-webhint-in-vs-code.msft.png":::
    Webhint no Visual Studio Code, mostrando um problema de acessibilidade sublinhando o elemento HTML e mostrando uma explicação do problema
:::image-end:::

Estamos constantemente trabalhando em novos recursos de acessibilidade para o DevTools.  Se você estiver faltando algo, envie uma mensagem e nos diga o que podemos fazer.


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]


<!-- links -->
[DevToolsMediaQueries]: ../device-mode/index.md#show-media-queries "Mostrar consultas de mídia - Emular dispositivos móveis Microsoft Edge DevTools | Microsoft Docs"
[DevToolsDeviceModeIndex]: ../device-mode/index.md "Emular dispositivos móveis no Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsAccessibilityReference]: reference.md "Recursos de teste de acessibilidade no DevTools | Microsoft Docs"
[DevToolsColorSchemeSimulation]: ./preferred-color-scheme-simulation.md "Simulação de esquema de cores escuro ou claro | Microsoft Docs"
[DevToolsIssuesTool]: ../issues/index.md "Encontre e corrige problemas usando a ferramenta Problemas | Microsoft Docs"
[DevToolsReducedMotion]: ./reduced-motion-simulation.md "Simulação de movimento reduzida | Microsoft Docs"
[DevToolsVisionDeficiencies]: ./emulate-vision-deficiencies.md "Emular deficiências de visão | Microsoft Docs"
<!-- links into test-issues-tool.md -->
[DevToolsAccessibilityTestIssuesToolViewAccSection]: test-issues-tool.md#view-the-accessibility-section-of-the-issues-tool "Exibir a seção Acessibilidade da ferramenta Problemas - Testar automaticamente uma página da Web para problemas de acessibilidade | Microsoft Docs"
[DevtoolsAccessibilityTestIssuesToolCheckFieldsLabels]: test-issues-tool.md#verify-that-input-fields-have-labels "Verifique se os campos de entrada têm rótulos - Teste automaticamente uma página da Web para problemas de acessibilidade | Microsoft Docs" 
[DevtoolsAccessibilityTestIssuesToolCheckAltText]: test-issues-tool.md#verify-that-images-have-alt-text "Verifique se as imagens têm texto alt - Teste automaticamente uma página da Web para problemas de acessibilidade | Microsoft Docs "
[DevtoolsAccessibilityTestIssuesToolCheckContrast]: test-issues-tool.md#verify-that-text-colors-have-enough-contrast "Verifique se as cores de texto têm contraste suficiente - Teste automaticamente uma página da Web para problemas de acessibilidade | Microsoft Docs"
<!-- links into test-inspect-tool.md -->
[DevtoolsAccessibilityTestInspectToolColorHighlighting]: test-inspect-tool.md#identify-nested-regions-using-color-highlighting "Identificar regiões aninhadas usando realçamento de cores - Use a ferramenta Inspecionar para detectar problemas de acessibilidade, pairando sobre a página da Web | Microsoft Docs"
[DevtoolsAccessibilityTestInspectToolIndivElems]: test-inspect-tool.md#check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support "Verificar elementos individuais para contraste de texto, texto do leitor de tela e suporte ao teclado - Use a ferramenta Inspecionar para detectar problemas de acessibilidade, passe o mouse sobre a página da Web | Microsoft Docs"
[DevtoolsAccessibilityTestInspectToolDomCss]: test-inspect-tool.md#use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css "Use a ferramenta Inspecionar para passar o mouse sobre a página da Web para realçar o DOM e CSS - Use a ferramenta Inspecionar para detectar problemas de acessibilidade, pairando sobre a página da Web | Microsoft Docs"
<!-- external links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Webpage de demonstração de teste de acessibilidade | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "taxa de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Diretrizes de acessibilidade de conteúdo da Web | W3C"
[AccessibilityInsightsAssessment]: https://accessibilityinsights.io/docs/en/web/getstarted/assessment/ "Avaliação em Acessibilidade Insights para web | Acessibilidade Insights"
[AccessibilityInsights]: https://accessibilityinsights.io "Acessibilidade Insights"
[Lighthouse]: https://developers.google.com/web/tools/lighthouse/ "| Google"
[WebhintForCode]:https://aka.ms/webhint4code "webhint | Visual Studio Marketplace"
