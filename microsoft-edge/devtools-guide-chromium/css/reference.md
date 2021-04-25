---
description: Descubra novos fluxos de trabalho para exibição e alteração de CSS no Microsoft Edge DevTools.
title: Referência CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: bddbf14e73f5c29bfd4757c9cd6d255f419c331f
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519328"
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

# <a name="css-reference"></a>Referência CSS  

Descubra novos fluxos de trabalho na referência abrangente a seguir dos recursos do Microsoft Edge DevTools relacionados à exibição e alteração de CSS.  

Para saber as noções básicas, navegue até [Começar a exibir e alterar CSS][DevToolsCSSGetStarted].  

## <a name="choose-an-element"></a>Escolher um elemento  

A **ferramenta Elements** do DevTools permite exibir ou alterar o CSS de um elemento de cada vez.  O elemento selecionado é realçado na árvore **DOM**.  Os estilos do elemento são mostrados no painel **Estilos.**  Para um tutorial, navegue até [Exibir o CSS para um elemento][DevToolsCSSGetStartedTutorial].  

> [!NOTE]
> Na figura a seguir, o `h1` elemento realçado na Árvore **DOM** é o elemento selecionado.  À direita, os estilos do elemento são mostrados no painel **Estilos.**  À esquerda, o elemento é realçado no viewport, mas somente porque o mouse está atualmente pairando sobre ele na **árvore DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   Um exemplo de um elemento selecionado  
:::image-end:::  

Use uma das seguintes ações para selecionar um elemento.  

*   No seu viewport, passe o mouse no elemento, abra o menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar**.  
*   No DevTools, escolha **Selecionar** um elemento \( Selecione um elemento \) ou selecione ![ ](../media/select-an-element-icon.msft.png) `Control` + `Shift` + `C` \(Windows, Linux\) `Command` + `Shift` + `C` ou \(macOS\) e escolha o elemento no viewport.  
*   Em DevTools, escolha o elemento na Árvore **DOM**.  
*   No DevTools, execute uma consulta como no Console , passe o mouse no resultado, abra o menu contextual \(clique com o botão direito do mouse\) e escolha `document.querySelector('p')` Revelar em Elementos **** **painel**.  

## <a name="view-css"></a>Exibir CSS  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a>Exibir a folha de estilos externa onde uma regra é definida  

No painel **Estilos,** escolha o link ao lado de uma regra CSS para abrir a folha de estilos externa que define a regra.  A folha de estilos é aberta no **painel Editor** da **ferramenta Sources.**  

Se a folha de estilos for minificada, escolha o botão **Formatar** \( ![ Formatar ](../media/format-icon.msft.png) \) na parte inferior do **painel Editor.**  Para obter mais informações, navegue até [Reformat a minified JavaScript file with pretty-print][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> Na figura a seguir, depois de escolher, você é levado para a `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` linha 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` de , onde a regra CSS é `.content h1:first-of-type` definida.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Exibindo a folha de estilos em que uma regra é definida" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Exibindo a folha de estilos em que uma regra é definida  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a>Exibir apenas o CSS que é realmente aplicado a um elemento  

O **painel Estilos** mostra todas as regras que se aplicam a um elemento, incluindo declarações que foram substituídos.  Quando você não estiver interessado em declarações substituidas, use o painel **Computed** para exibir apenas o CSS que está realmente sendo aplicado a um elemento.  

1.  [Selecione um elemento](#choose-an-element).  
1.  Navegue até **o painel Computed** na **ferramenta Elements.**  

> [!NOTE]
> Em uma janela ampla do DevTools, o painel **Computed** não existe.  O conteúdo do painel **Computed** é mostrado no painel **Estilos.**  

As propriedades herdadas são opacas.  Para exibir todos os valores herdados, selecione a **caixa de seleção Mostrar Tudo.**  

> [!NOTE]
> Na figura a seguir, o **painel Computed** mostra as propriedades CSS que estão sendo aplicadas ao elemento selecionado `h1` no momento.  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="O painel Computed" lightbox="../media/css-elements-computed-h1.msft.png":::
   O **painel Computed**  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a>Exibir propriedades CSS em ordem alfabética  

Use o **painel Computed.**  Navegue [até Exibir somente o CSS que é realmente aplicado a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### <a name="view-inherited-css-properties"></a>Exibir propriedades CSS herdadas  

Marque a **caixa de seleção** Mostrar Tudo no painel **Computado.**  Navegue [até Exibir somente o CSS que é realmente aplicado a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### <a name="view-the-box-model-for-an-element"></a>Exibir o modelo de caixa de um elemento  

Para exibir [o modelo de caixa][MDNBoxModel] de um elemento, navegue até o painel **Estilos.**  Se sua janela DevTools for estreita, o diagrama **do Modelo** de Caixa será na parte inferior do painel.  

Escolha e edite em um valor para alterar um valor.  

> [!NOTE]
> Na figura a seguir, o diagrama **Modelo** de Caixa no painel **Estilos** mostra o modelo de caixa do elemento selecionado `h1` no momento.  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="O diagrama do modelo de caixa" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   O **diagrama do modelo de** caixa  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a>Pesquisar e filtrar o CSS de um elemento  

Use a **caixa de** texto Filtrar nos **painéis Estilos** e **Computados** para pesquisar propriedades ou valores CSS específicos.  

Para também pesquisar propriedades herdadas no **painel Computed,** marque a caixa de seleção **Mostrar Tudo.**  

> [!NOTE]
> Na figura a seguir, o painel **Estilos** é filtrado para mostrar apenas regras que incluem a consulta de pesquisa `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar o painel Estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtrar o **painel Estilos**  
:::image-end:::  

> [!NOTE]
> Na figura a seguir, o **painel Computed** é filtrado para mostrar apenas declarações que incluem a consulta de pesquisa `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar o painel Computed" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtrar o **painel Computed**  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a>Alternar uma pseudo-classe  

Conclua as seguintes ações para alternar uma pseudo-classe `:active` como , , ou `:focus` `:hover` `:visited` .  

1.  [Selecione um elemento](#choose-an-element).  
1.  Na ferramenta **Elementos,** navegue até o **painel Estilos.**  
1.  Escolha **:hov**.  
1.  Verifique a pseudo-classe que você deseja habilitar.  

> [!NOTE]
> Na figura a seguir, alterne a `:hover` pseudo-classe.  No viewport, verifique se a declaração está sendo aplicada ao elemento, mesmo que o elemento não está realmente sendo `background-color: cornflowerblue` pairado sobre.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Alternar a pseudo-classe :hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Alternar a `:hover` pseudo-classe  
:::image-end:::  

Para um tutorial interativo, navegue até [Adicionar um pseudostate a uma classe][DevToolsCSSGetStartedAddPseudoState].  

### <a name="view-a-page-in-print-mode"></a>Exibir uma página no modo de impressão  

Conclua as seguintes ações para exibir uma página no modo de impressão.  

1.  [Abra o Menu de Comando][DevToolsCommandMenu].  
1.  Comece a digitar `Rendering` e selecione `Show Rendering` .  
1.  Para o **menu suspenso Emular Mídia CSS,** escolha **imprimir**.  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a>Exibir CSS usado e não usado com a ferramenta Coverage  

A **ferramenta Coverage** mostra qual CSS uma página realmente usa.  

1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) enquanto o [][DevToolsCommandMenu]DevTools está em foco para abrir o Menu de Comando .  
1.  Comece a digitar `coverage` e escolha Mostrar **Cobertura**.  A **ferramenta Coverage** é exibida.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrindo a ferramenta Cobertura no Menu de Comando" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Abra a **ferramenta Cobertura** no Menu **de Comando**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="A ferramenta Coverage" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             A **ferramenta Coverage**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Escolha **Iniciar a cobertura de instrumentação e atualize a página** \( Inicie a cobertura de ![ instrumentação e atualize a ](../media/refresh-icon.msft.png) página \).  A página atualiza e a ferramenta **Coverage** fornece uma visão geral de quanto CSS \(e JavaScript\) é usado a partir de cada arquivo que o navegador carrega.  Verde representa CSS usado.  Vermelho representa CSS nãousado.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Uma visão geral de quanto CSS (e JavaScript) é usado e não usado" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Uma visão geral de quanto CSS \(e JavaScript\) é usado e não usado  
    :::image-end:::  

1.  Para exibir uma divisão linha a linha do que CSS é usado, escolha um arquivo CSS.  
    
    > [!NOTE]
    > Na figura a seguir, as linhas 145 a 147 e 149 a 151 de não são usadas, enquanto as linhas `b66bc881.site-ltr.css` 163 a 166 são usadas.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Uma divisão linha a linha de CSS usada e não utilizada" lightbox="../media/css-sources-css-coverage.msft.png":::
       Uma divisão linha a linha de CSS usada e não utilizada  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a>Forçar o modo de visualização de impressão  

Navegue [até Forçar DevTools no modo Visualização de Impressão.][DevToolsCssPrintPreview]  

## <a name="change-css"></a>Alterar CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a>Adicionar uma declaração CSS a um elemento  

A ordem das declarações afeta a forma como um elemento é estilado, use a lista a seguir para ajudá-lo a adicionar declarações de maneiras diferentes.  

*   [Adicione uma declaração em linha](#add-an-inline-declaration).  Equivalente a adicionar `style` um atributo ao HTML de um elemento.  
*   [Adicione uma declaração a uma regra de estilo.](#add-a-declaration-to-a-style-rule)  

**Qual fluxo de trabalho você deve usar?** Para a maioria dos cenários, você provavelmente deseja usar o fluxo de trabalho de declaração em linha.  As declarações em linha têm maior especificidade do que as externas, portanto, o fluxo de trabalho em linha garante que as alterações tenham efeito no elemento esperado.  Para obter mais informações sobre a especificidade, navegue até [Tipos de Seletor][MDNSelectorTypes].  

Se você estiver depurando quaisquer estilos do elemento e precisar testar especificamente o que acontece quando uma declaração é definida em locais diferentes, use o outro fluxo de trabalho.  

#### <a name="add-an-inline-declaration"></a>Adicionar uma declaração em linha  

Conclua as seguintes ações para adicionar uma declaração em linha.  

1.  [Selecione um elemento](#choose-an-element).  
1.  No painel **Estilos,** escolha entre os colchetes da **seção element.style.**  O cursor se concentra, permitindo que você insira texto.  
1.  Insira um nome de propriedade e selecione `Enter` .  
1.  Insira um valor válido para essa propriedade e selecione `Enter` .  Na Árvore **DOM,** verifique se um `style` atributo foi adicionado ao elemento.  

> [!NOTE]
> Na figura a seguir, `margin-top` as propriedades e foram `background-color` aplicadas ao elemento selecionado.  Na Árvore **DOM,** verifique se as declarações são refletidas no `style` atributo de um elemento.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Adicionar declarações em linha" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Adicionar declarações em linha  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a>Adicionar uma declaração a uma regra de estilo  

Conclua as seguintes ações para adicionar uma declaração a uma regra de estilo existente.  

1.  [Selecione um elemento](#choose-an-element).  
1.  No painel **Estilos,** escolha entre os colchetes da regra de estilo à qual você deseja adicionar a declaração.  O cursor se concentra, permitindo que você insira texto.  
1.  Insira um nome de propriedade e selecione `Enter` .  
1.  Insira um valor válido para essa propriedade e selecione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Adicionar uma declaração a uma regra de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Adicionar a `border-bottom-style:groove` declaração a uma regra de estilo  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a>Alterar um nome ou valor de declaração  

Escolha e edite o nome ou o valor de uma declaração para alterá-la.  Para atalhos para incrementar ou decrementar rapidamente um valor por , , ou unidades, navegue até Alterar valores de declaração `0.1` `1` com `10` `100` [atalhos de teclado](#change-declaration-values-with-keyboard-shortcuts).  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Alterando o valor de uma declaração" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Alterar o valor da `border-bottom-style` declaração  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a>Alterar valores de declaração com atalhos de teclado  

Ao editar o valor de uma declaração, você pode usar os atalhos de teclado a seguir para incrementar o valor por uma quantidade específica.  

*   Selecione `Alt` + `Up` \(Windows, Linux\) `Option` + `Up` ou \(macOS\) para incrementar `0.1` por .  
*   Selecione `Up` para alterar o valor por , ou se o valor atual estiver entre e `1` `0.1` `-1` `1` .  
*   Selecione `Shift` + `Up` para incrementar `10` por .  
*   Selecione `Shift` + `Page Up` \(Windows, Linux\) `Shift` + `Command` + `Up` ou \(macOS\) para incrementar o valor em `100` .  

A decrementação também funciona.  Basta substituir cada instância mencionada `Up` acima por `Down` .  

### <a name="add-a-class-to-an-element"></a>Adicionar uma classe a um elemento  

Conclua as seguintes ações para adicionar uma classe a um elemento.  

1.  [Selecione o elemento](#choose-an-element) na Árvore **DOM**.  
1.  Escolha **.cls**.  
1.  Insira o nome da classe na caixa **de texto Adicionar Nova** Classe.  
1.  Selecione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="O painel Classes de Elemento" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   O **painel Classes de** Elemento  
:::image-end:::  

### <a name="toggle-a-class"></a>Alternar uma classe  

Conclua as seguintes ações para habilitar ou desabilitar uma classe em um elemento.  

1.  [Selecione o elemento](#choose-an-element) na Árvore **DOM**.  
1.  Abra o **painel Classes de** Elemento.  Navegue [até Adicionar uma classe a um elemento](#add-a-class-to-an-element).  Abaixo da **caixa de texto** Adicionar Nova Classe estão todas as classes aplicadas ao elemento específico.  
1.  Alterne a caixa de seleção ao lado da classe que você deseja ativar ou desativar.  

### <a name="add-a-style-rule"></a>Adicionar uma regra de estilo  

Conclua as seguintes ações para adicionar uma nova regra de estilo.  

1.  [Selecione um elemento](#choose-an-element).  
1.  Escolha **Nova Regra de Estilo** \( Nova Regra de Estilo ![ ](../media/new-style-rule-icon.msft.png) \).  O DevTools insere uma nova regra abaixo da **regra element.style.**  

> [!NOTE]
> Na figura a seguir, DevTools adiciona a regra de estilo `h1.devsite-page-title` depois de escolher Nova Regra de **Estilo**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Adicionar uma nova regra de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Adicionar uma nova regra de estilo  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a>Escolha a qual folha de estilos adicionar uma regra  

Ao [adicionar uma nova regra de](#add-a-style-rule)estilo, escolha e segure New Style **Rule** \( New Style Rule \) para escolher qual folha de estilos adicionar a regra ![ de ](../media/new-style-rule-icon.msft.png) estilo.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Escolha uma folha de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Escolha uma folha de estilos  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a>Adicionar uma regra de estilo a um local específico  

Conclua as seguintes ações para adicionar uma regra de estilo a um local específico no painel **Estilos.**  

1.  Passe o mouse na regra de estilo que está diretamente acima de onde você deseja adicionar sua nova regra de estilo.  
1.  [Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)  
1.  Escolha **Inserir Regra de Estilo abaixo** \( Inserir Regra de Estilo abaixo ícone ![ ](../media/new-style-rule-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Inserir regra de estilo abaixo" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Inserir regra de estilo abaixo**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a>Revelar a barra de ferramentas Mais Ações  

A **barra de ferramentas** Mais Ações permite executar as seguintes ações.  

*   Insira uma regra de estilo diretamente abaixo da que você está focado.  
*   Adicione uma `background-color` , , ou declaração à regra de estilo em que você está `color` `box-shadow` `text-shadow` focado.  

Conclua as seguintes ações para revelar a barra **de ferramentas Mais** Ações.  

1.  No painel **Estilos,** passe o mouse em uma regra de estilo.  **Mais Ações** \( \) é revelado na parte inferior `...` direita da seção de regra de estilo.  
    
    > [!NOTE]
    > Na figura a seguir, passe o mouse na regra de estilo e Mais Ações será revelada no canto inferior direito `.header-holder.has-default-focus` da seção de regra de estilo. ****  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Revelar mais ações" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Revelar **mais ações** \( `...` \)  
    :::image-end:::  
    
1.  Passe o **mouse sobre Mais Ações** `...` \( \) para revelar as ações mencionadas acima.  
    
    > [!NOTE]
    > A **ação Inserir Regra de Estilo Abaixo** é revelada após passar o mouse sobre Mais **Ações**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="A barra de ferramentas Mais Ações" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       A **barra de ferramentas Mais** Ações  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a>Alternar uma declaração  

Conclua as ações folllwoing para alternar uma única declaração em \(ou off\).  

1.  [Selecione um elemento](#choose-an-element).  
1.  No painel **Estilos,** passe o mouse na regra que define a declaração.  Uma caixa de seleção é exibida ao lado de cada declaração.  
1.  Marque \(ou desmarcar\) a caixa de seleção ao lado da declaração.  Quando você desmarca uma declaração, o DevTools a cruza para indicar que ela não está mais ativa.  

> [!NOTE]
> Na figura a seguir, a propriedade do elemento selecionado no momento `margin-top` foi alternada.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Alternar uma declaração" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Alternar uma declaração  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a>Adicionar uma declaração de cor de plano de fundo  

Conclua as seguintes ações para adicionar `background-color` uma declaração a um elemento.  

1.  Passe o mouse na regra de estilo à que você deseja `background-color` adicionar a declaração.  
1.  [Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)  
1.  Escolha **Adicionar Cor do Plano de** Fundo \( Adicionar ícone de cor de plano de fundo ![ ](../media/add-background-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Adicionar cor de plano de fundo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Adicionar cor de plano de fundo**  
:::image-end:::  

### <a name="add-a-color-declaration"></a>Adicionar uma declaração de cor  

Conclua as seguintes ações para adicionar `color` uma declaração a um elemento.  

1.  Passe o mouse na regra de estilo à que você deseja `color` adicionar a declaração.  
1.  [Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)  
1.  Escolha **Adicionar Cor** \( Adicionar ícone de cor ![ ](../media/add-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Adicionar Cor" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Adicionar Cor**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a>Adicionar uma declaração de sombra de caixa  

Conclua as seguintes ações para adicionar `box-shadow` uma declaração a um elemento.  

1.  Passe o mouse na regra de estilo à que você deseja `box-shadow` adicionar a declaração.  
1.  [Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)  
1.  Escolha **Adicionar Sombra de Caixa** \( Adicionar ícone sombra de caixa ![ ](../media/add-box-shadow-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Adicionar Sombra de Caixa" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Adicionar Sombra de Caixa**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a>Adicionar uma declaração de sombra de texto  

Conclua as seguintes ações para adicionar `text-shadow` uma declaração a um elemento.  

1.  Passe o mouse na regra de estilo à que você deseja `text-shadow` adicionar a declaração.  
1.  [Revelar a **barra de ferramentas Mais Ações.** ](#reveal-the-more-actions-toolbar)  
1.  Escolha **Adicionar Sombra de Texto** \( Adicionar ícone sombra de texto ![ ](../media/add-text-shadow-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Adicionar Sombra de Texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Adicionar Sombra de Texto**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a>Alterar cores com o Selador de Cores  

O **Selador de** Cores fornece uma GUI para alterações `color` e `background-color` declarações.  

Conclua as seguintes ações para abrir o **Selador de Cores**.  

1.  [Selecione um elemento](#choose-an-element).  
1.  No painel **Estilos,** encontre `color` a declaração , ou semelhante que você deseja `background-color` alterar.  À esquerda do valor , ou semelhante, há um pequeno `color` quadrado que é uma `background-color` visualização da cor.  
    
    > [!NOTE]
    > Na figura a seguir, o pequeno quadrado à esquerda `rgba(0, 0, 0, 0.7)` é uma visualização dessa cor.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Visualização de cores" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Visualização de cores  
    :::image-end:::  
    
1.  Escolha a visualização para abrir o **Selador de Cores**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="O Se picker de cores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       O **Se picker de cores**  
    :::image-end:::  
    
A figura a seguir e os descries de lista de cada um dos elementos da interface do usuário do **Selador de Cores**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="O Seletor de Cores, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   O **Seletor de**Cores , anotado  
:::image-end:::  

:::row:::
   :::column span="1":::
      1  
   :::column-end:::
   :::column span="1":::
      **Sombreos**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      2  
   :::column-end:::
   :::column span="1":::
      **Conta-gotas**  
   :::column-end:::
   :::column span="2":::
      Para obter mais informações, navegue até Amostra de uma cor da [página com o Conta-gotas](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3  
   :::column-end:::
   :::column span="1":::
      **Copiar para área de transferência**  
   :::column-end:::
   :::column span="2":::
      Copie o **Valor de Exibição** para sua área de transferência.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      4  
   :::column-end:::
   :::column span="1":::
      **Valor de exibição**  
   :::column-end:::
   :::column span="2":::
      A representação RGBA, HSLA ou Hex da cor.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Paleta de Cores**  
   :::column-end:::
   :::column span="2":::
      Escolha um dos quadrados para alterar a cor para esse quadrado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
   :::column-end:::
   :::column span="1":::
      **Hue**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      7  
   :::column-end:::
   :::column span="1":::
      **Opacidade**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      8  
   :::column-end:::
   :::column span="1":::
      **Alternador de valor de exibição**  
   :::column-end:::
   :::column span="2":::
      Alterne entre as representações RGBA, HSLA e Hex da cor atual.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      9  
   :::column-end:::
   :::column span="1":::
      **Alternador de Paleta de Cores**  
   :::column-end:::
   :::column span="2":::
      Alterne entre a paleta [Design de Material,][MaterialDesignColorSystem]uma paleta personalizada ou uma paleta de cores de página.  O DevTools gera a paleta de cores da página com base nas cores que ele encontra em suas folhas de estilo.  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a>Amostra de uma cor da página com o Conta-gotas  

Quando você abre o **Selador de**Cores, **o** Conta-gotas \( Conta-gotas ![ ](../media/eyedropper-icon.msft.png) \) está em uso por padrão.  Conclua as seguintes ações para alterar a cor selecionada para outra cor na página.  

1.  Passe o mouse sobre a cor de destino no viewport.  
1.  Escolha confirmar.  
    
    > [!NOTE]
    > Na figura a seguir, o **Selador** de Cores mostra um valor de cor atual `rgba(0,0,0,0.7)` de , que está próximo ao preto.  A cor específica deve mudar para a versão do preto que está realçada no viewport depois que você a escolheu.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Usando o Conta-gotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Usando o Conta-gotas  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Adicionar um pseudostate a uma classe - Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Exibir o CSS para um elemento - Começar a exibir e alterar o css | Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformata um arquivo JavaScript minificado com impressão bastante impressa - Use o depurador | Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "O sistema de cores - Design de Material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "O modelo de caixa | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de seletor - Especificidade | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/css/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  