---
description: Descubra novos fluxos de trabalho para exibir e alterar CSS no Microsoft Edge DevTools.
title: Referência BITS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 83edc15549b4f8e668af99a4d95966736aaa0992
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204009"
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

# Referência CSS  

Descubra novos fluxos de trabalho na seguinte referência abrangente dos recursos do Microsoft Edge DevTools relacionados à exibição e alteração da CSS.  

Confira [introdução e alterar CSS][DevToolsCSSGetStarted] para aprender as noções básicas.  

## Selecionar um elemento  

O painel **elementos** do devtools permite que você visualize ou altere a CSS de um elemento de cada vez.  O elemento selecionado é realçado na **árvore DOM**.  Os estilos do elemento são mostrados no painel **estilos** .  Consulte [Exibir o CSS de um elemento][DevToolsCSSGetStartedTutorial] para um tutorial.  

> [!NOTE]
> Na figura a seguir, o `h1` elemento que está realçado na **árvore DOM** é o elemento selecionado.  À direita, os estilos do elemento são mostrados no painel **estilos** .  À esquerda, o elemento é realçado na viewport, mas só porque o mouse está passando no momento sobre ele na **árvore DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Um exemplo de um elemento selecionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   Um exemplo de um elemento selecionado  
:::image-end:::  

Use uma das ações a seguir para selecionar um elemento.  

*   No seu visor, passe o cursor do mouse sobre o elemento, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar**.  
*   No devtools, escolha **selecionar um elemento** \ ( ![ Selecione um elemento ][ImageSelectAnElementIcon] \) ou selecionar `Control` + `Shift` + `C` \ (Windows, Linux \) ou `Command` + `Shift` + `C` \ (MacOS \) e, em seguida, escolha o elemento no visor.  
*   No DevTools, escolha o elemento na **árvore DOM**.  
*   No DevTools, execute uma consulta como `document.querySelector('p')` no **console**, passe o cursor do mouse sobre o resultado, abra o menu contextual \ (clique com o botão direito do mouse \) e escolha **revelar no painel de elementos**.  

## Exibir CSS  

### Exibir a folha de estilos externa na qual uma regra está definida  

No painel **estilos** , escolha o link ao lado de uma regra CSS para abrir a folha de estilos externa que define a regra.  

Se a folha de estilos for minified, navegue para [deixar um arquivo do minified legível][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> Na figura a seguir, depois de escolher `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` você será levado para a linha 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , onde a `.content h1:first-of-type` regra CSS é definida.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Exibir a folha de estilos onde uma regra está definida" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Exibir a folha de estilos onde uma regra está definida  
:::image-end:::  

### Exibir apenas a CSS que é realmente aplicada a um elemento  

A guia **estilos** mostra todas as regras que se aplicam a um elemento, incluindo declarações que foram substituídas.  Quando você não está interessado em declarações substituídas, use a guia **calculada** para exibir apenas a CSS que está realmente sendo aplicada a um elemento.  

1.  [Selecione um elemento](#select-an-element).  
1.  Vá para a guia **calculada** no painel **elementos** .  

> [!NOTE]
> Em uma ampla janela do DevTools, a guia **calculada** não existe.  O conteúdo da guia **calculada** é mostrado na guia **estilos** .  

As propriedades herdadas são opacas.  Marque a caixa de seleção **Mostrar tudo** para ver todos os valores herdados.  

> [!NOTE]
> Na figura a seguir, a guia **calculada** mostra as propriedades CSS aplicadas ao elemento atualmente selecionado `h1` .  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="A guia calculada" lightbox="../media/css-elements-computed-h1.msft.png":::
   A guia **calculada**  
:::image-end:::  

### Exibir as propriedades CSS em ordem alfabética  

Use a guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Exibir Propriedades CSS herdadas  

Marque a caixa de seleção **Mostrar tudo** na guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Exibir o modelo de caixa para um elemento  

Para exibir [o modelo de caixa][MDNBoxModel] de um elemento, acesse a guia **estilos** .  Se a janela do DevTools for restrita, o diagrama de **modelo de caixa** estará na parte inferior da guia.  

Escolha e edite um valor para alterar um valor.  

> [!NOTE]
> Na figura a seguir, o diagrama de **modelo de caixa** na guia **estilos** mostra o modelo de caixa do elemento atualmente selecionado `h1` .  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="O diagrama de modelo de caixa" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   O diagrama de **modelo de caixa**  
:::image-end:::  

### Pesquisar e filtrar a CSS de um elemento  

Use a caixa de texto **Filtrar** nas guias **estilos** e **calculados** para pesquisar valores ou propriedades CSS específicas.  

Para pesquisar também as propriedades herdadas na guia **calculada** , marque a caixa de seleção **Mostrar tudo** .  

> [!NOTE]
> Na figura a seguir, a guia **estilos** é filtrada para mostrar apenas as regras que incluem a consulta de pesquisa `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar a guia estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtrar a guia **estilos**  
:::image-end:::  

> [!NOTE]
> Na figura a seguir, a guia **calculada** é filtrada para mostrar somente declarações que incluam a consulta de pesquisa `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar a guia calculada" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtrar a guia **calculada**  
:::image-end:::  

### Alternar uma pseudo-classe  

Conclua as ações a seguir para alternar uma pseudoclasse como `:active` , `:focus` , `:hover` ou `:visited` .  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **elementos** , vá para a guia **estilos** .  
1.  Escolha **: Hov**.  
1.  Verifique a pseudo-classe que você deseja habilitar.  

> [!NOTE]
> Na figura a seguir, alterne a `:hover` pseudo-classe.  Na viewport, verifique se a `background-color: cornflowerblue` declaração está sendo aplicada ao elemento, mesmo que o elemento não esteja realmente sendo focalizado.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Alternar o: hover pseudo-classe" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Alternar a `:hover` pseudo-classe  
:::image-end:::  

Para obter um tutorial interativo, navegue para [Adicionar um pseudo-estado a uma classe][DevToolsCSSGetStartedAddPseudoState].  

### Exibir uma página no modo de impressão  

Conclua as ações a seguir para exibir uma página no modo de impressão.  

1.  [Abrir o menu de comandos][DevToolsCommandMenu].  
1.  Comece a digitar `Rendering` e selecione `Show Rendering` .  
1.  Para o menu suspenso **emular CSS Media** , escolha **Imprimir**.  

### Exibir CSS usado e não usado com a guia cobertura  

A guia cobertura mostra a CSS que uma página realmente usa.  

1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) enquanto o devtools estiver em foco para [abrir o menu de comando][DevToolsCommandMenu].  
1.  Comece a digitar `coverage` e escolha **Mostrar cobertura**.  A guia cobertura é exibida.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrindo a guia cobertura no menu comando" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Abrir a guia **cobertura** no **menu comando**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="A guia cobertura" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             A guia **cobertura**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Escolha **Iniciar cobertura de instrumentação e atualize a página** \ ( ![ Iniciar cobertura de instrumentação e atualizar a página ][ImageRefreshIcon] \).  A página é atualizada e a guia cobertura fornece uma visão geral de quanto o CSS \ (e JavaScript \) é usado em cada arquivo que o navegador carrega.  Verde representa a CSS usada.  Vermelho representa a CSS não usada.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Uma visão geral do quanto CSS (e JavaScript) é usado e não usado" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Uma visão geral do quanto o CSS \ (e JavaScript \) é usado e não é usado  
    :::image-end:::  

1.  Escolha um arquivo CSS para ver uma divisão linha por linha de qual CSS ele usa.  
    
    > [!NOTE]
    > Na figura a seguir, as linhas 145 a 147 e 149 a 151 de `b66bc881.site-ltr.css` não são usadas, enquanto as linhas 163 para 166 são usadas.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Uma divisão linha por linha do CSS usado e não usado" lightbox="../media/css-sources-css-coverage.msft.png":::
       Uma divisão linha por linha do CSS usado e não usado  
    :::image-end:::  
    
### Modo de visualização de impressão forçado  

Consulte [forçar devtools no modo de visualização de impressão][DevToolsCssPrintPreview].  

## Alterar CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### Adicionar uma declaração CSS a um elemento  

A ordem das declarações afeta a forma como um elemento é estilizado, use a lista a seguir para ajudá-lo a adicionar declarações de maneiras diferentes.  

*   [Adicione uma declaração embutida](#add-an-inline-declaration).  Equivalente a adicionar um `style` atributo ao HTML de um elemento.  
*   [Adicione uma declaração a uma regra de estilo](#add-a-declaration-to-a-style-rule).  

**Que fluxo de trabalho você deve usar?** Para a maioria dos cenários, você provavelmente deseja usar o fluxo de trabalho da declaração embutida.  As declarações embutidas têm uma prioridade mais alta do que as externas, portanto, o fluxo de trabalho embutido garante que as alterações entrem em vigor no elemento esperado.  Para obter mais informações sobre a específicaidade, navegue até [tipos de seletor][MDNSelectorTypes].  

Se você estiver Depurando qualquer estilo do elemento e precisar testar especificamente o que acontece quando uma declaração é definida em locais diferentes, use o outro fluxo de trabalho.  

#### Adicionar uma declaração embutida  

Conclua as ações a seguir para adicionar uma declaração embutida.  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **estilos** , escolha entre os colchetes da seção **elemento. Style** .  O cursor se concentra, permitindo que você insira texto.  
1.  Insira um nome de propriedade e selecione `Enter` .  
1.  Insira um valor válido para essa propriedade e selecione `Enter` .  Na **árvore DOM**, verifique se um `style` atributo foi adicionado ao elemento.  

> [!NOTE]
> Na figura a seguir, as `margin-top` Propriedades e foram `background-color` aplicadas ao elemento selecionado.  Na **árvore DOM** , verifique se as declarações são refletidas no `style` atributo para um elemento.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Adicionar declarações embutidas" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Adicionar declarações embutidas  
:::image-end:::  

#### Adicionar uma declaração a uma regra de estilo  

Conclua as ações a seguir para adicionar uma declaração a uma regra de estilo existente.  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **estilos** , escolha entre os colchetes da regra de estilo à qual você deseja adicionar a declaração.  O cursor se concentra, permitindo que você insira texto.  
1.  Insira um nome de propriedade e selecione `Enter` .  
1.  Insira um valor válido para essa propriedade e selecione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Adicionando uma declaração a uma regra de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Adicionar a `border-bottom-style:groove` declaração a uma regra de estilo  
:::image-end:::  

### Alterar um nome ou valor de declaração  

Escolha e edite o nome ou o valor de uma declaração para alterá-la.  Consulte [alterar valores de declaração com atalhos de teclado](#change-declaration-values-with-keyboard-shortcuts) para atalhos para incrementar ou decrementar rapidamente um valor por `0.1` ,, `1` `10` ou `100` unidades.  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Alterar o valor de uma declaração" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Alterar o valor da `border-bottom-style` declaração  
:::image-end:::  

### Alterar valores de declaração com atalhos de teclado  

Durante a edição do valor de uma declaração, você pode usar os seguintes atalhos de teclado para incrementar o valor por uma quantia específica.  

*   Selecione `Alt` + `Up` \ (Windows, Linux \) ou `Option` + `Up` \ (MacOS \) para aumentar o incremento `0.1` .  
*   Selecione `Up` para alterar o valor por `1` , ou `0.1` se o valor atual estiver entre `-1` e `1` .  
*   Selecione `Shift` + `Up` para aumentar o incremento `10` .  
*   Selecione `Shift` + `Page Up` \ (Windows, Linux \) ou `Shift` + `Command` + `Up` \ (MacOS \) para incrementar o valor por `100` .  

O decréscimo também funciona.  Basta substituir cada ocorrência de `Up` mencionado acima por `Down` .  

### Adicionar uma classe a um elemento  

Conclua as ações a seguir para adicionar uma classe a um elemento.  

1.  [Selecione o elemento](#select-an-element) na **árvore DOM**.  
1.  Choose **. CLS**.  
1.  Digite o nome da classe na caixa de texto **Adicionar nova classe** .  
1.  Selecione `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="O painel classes de elemento" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   O painel **classes de elemento**  
:::image-end:::  

### Alternar uma classe  

Conclua as ações a seguir para habilitar ou desabilitar uma classe em um elemento.  

1.  [Selecione o elemento](#select-an-element) na **árvore DOM**.  
1.  Abrir o painel **classes de elementos** .  Consulte [Adicionar uma classe a um elemento](#add-a-class-to-an-element).  Abaixo da caixa de texto **Adicionar nova classe** estão todas as classes que estão sendo aplicadas ao elemento específico.  
1.  Alternar a caixa de seleção ao lado da classe que você deseja habilitar ou desabilitar.  

### Adicionar uma regra de estilo  

Conclua as ações a seguir para adicionar uma nova regra de estilo.  

1.  [Selecione um elemento](#select-an-element).  
1.  Escolha **novo regra de estilo** \ ( ![ novo regra de estilo ][ImageNewStyleRuleIcon] \).  DevTools insere uma nova regra abaixo da regra **elemento. Style** .  

> [!NOTE]
> Na figura a seguir, o DevTools adiciona a `h1.devsite-page-title` regra de estilo depois que você escolhe **nova regra de estilo**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Adicionar uma nova regra de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Adicionar uma nova regra de estilo  
:::image-end:::  

#### Escolha em qual folha de estilos você deseja adicionar uma regra  

Ao [Adicionar uma nova regra de estilo](#add-a-style-rule), escolha e segure **nova regra de estilo** \ ( ![ nova regra de estilo ][ImageNewStyleRuleIcon] \) para escolher para qual folha de estilo adicionar a regra de estilo.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Escolher uma folha de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Escolher uma folha de estilos  
:::image-end:::  

#### Adicionar uma regra de estilo a um local específico  

Conclua as ações a seguir para adicionar uma regra de estilo a um local específico na guia **estilos** .  

1.  Passe o mouse sobre a regra de estilo que está diretamente acima de onde você deseja adicionar sua nova regra de estilo.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Escolha **Inserir regra de estilo abaixo** \ ( ![ Inserir regra de estilo abaixo do ícone ][ImageNewStyleRuleIcon] \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Inserir regra de estilo abaixo" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Inserir regra de estilo abaixo**  
:::image-end:::  

### Revelar a barra de ferramentas mais ações  

A barra de ferramentas **mais ações** permite executar as seguintes ações.  

*   Insira uma regra de estilo diretamente abaixo da que você está focalizado.  
*   Adicione uma `background-color` `color` declaração,, `box-shadow` ou `text-shadow` para a regra de estilo na qual você está focalizado.  

Conclua as ações a seguir para revelar a barra de ferramentas **mais ações** .  

1.  Na guia **estilos** , passe o mouse sobre uma regra de estilo.  **Mais ações** \ ( `...` \) são reveladas no canto inferior direito da seção de regra de estilo.  
    
    > [!NOTE]
    > Na figura a seguir, passe o mouse sobre a `.header-holder.has-default-focus` regra de estilo e **mais ações** serão reveladas no canto inferior direito da seção de regra de estilo.  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Revelar mais ações" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Revelar **mais ações** \ ( `...` \)  
    :::image-end:::  
    
1.  Passe o mouse sobre **mais ações** \ ( `...` \) para revelar as ações mencionadas acima.  
    
    > [!NOTE]
    > A ação **Inserir regra de estilo abaixo** é revelada depois de passar o mouse sobre **mais ações**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="A barra de ferramentas mais ações" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       A barra de ferramentas **mais ações**  
    :::image-end:::  
    
### Alternar uma declaração  

Conclua as ações folllwoing para alternar uma única declaração em \ (ou off \).  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **estilos** , passe o mouse sobre a regra que define a declaração.  Uma caixa de seleção é exibida ao lado de cada declaração.  
1.  Marque \ (ou desmarque \) a caixa de seleção ao lado da declaração.  Quando você desmarca uma declaração, o DevTools a risca para indicar que não está mais ativo.  

> [!NOTE]
> Na figura a seguir, a `margin-top` Propriedade do elemento selecionado no momento foi desativada.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Alternar uma declaração" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Alternar uma declaração  
:::image-end:::  

### Adicionar uma declaração de cor de plano de fundo  

Conclua as ações a seguir para adicionar uma `background-color` declaração a um elemento.  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `background-color` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Escolha **adicionar cor de plano de fundo** \ ( ![ ícone de cor da tela de fundo ][ImageAddBackgroundColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Adicionar cor de plano de fundo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Adicionar cor de plano de fundo**  
:::image-end:::  

### Adicionar uma declaração de cor  

Conclua as ações a seguir para adicionar uma `color` declaração a um elemento.  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `color` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Escolha **adicionar cor** \ ( ![ ícone Adicionar cor ][ImageAddColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Adicionar cor" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Adicionar cor**  
:::image-end:::  

### Adicionar uma declaração de caixa-sombra  

Conclua as ações a seguir para adicionar uma `box-shadow` declaração a um elemento.  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `box-shadow` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Escolha **Adicionar sombra de caixa** \ ( ![ ícone de sombra Adicionar caixa ][ImageAddBoxShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Adicionar sombra à caixa" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Adicionar sombra à caixa**  
:::image-end:::  

### Adicionar uma declaração de sombra de texto  

Conclua as ações a seguir para adicionar uma `text-shadow` declaração a um elemento.  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `text-shadow` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Escolha **Adicionar sombra de texto** \ ( ![ Adicionar ícone de sombra de texto ][ImageAddTextShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Adicionar sombra de texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Adicionar sombra de texto**  
:::image-end:::  

### Alterar as cores com o seletor de cores  

O **seletor de cores** fornece uma GUI para alteração `color` e `background-color` declarações.  

Conclua as seguintes ações para abrir o **seletor de cores**.  

1.  [Selecione um elemento](#select-an-element).  
1.  Na guia **estilos** , localize a `color` declaração, `background-color` ou semelhante, que você deseja alterar.  À esquerda do `color` `background-color` valor, ou semelhante, há um quadrado pequeno que é uma visualização da cor.  
    
    > [!NOTE]
    > Na figura a seguir, o pequeno quadrado à esquerda de `rgba(0, 0, 0, 0.7)` é uma visualização da cor.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Visualização de cores" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Visualização de cores  
    :::image-end:::  
    
1.  Escolha a visualização para abrir o **seletor de cores**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="O seletor de cores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       O **seletor de cores**  
    :::image-end:::  
    
A figura a seguir e a lista descreve de cada um dos elementos da interface do usuário do **seletor de cores**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="O seletor de cores, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   O **seletor de cores**, anotado  
:::image-end:::  

:::row:::
   :::column span="1":::
      um  
   :::column-end:::
   :::column span="1":::
      **Sombras**  
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
      **Ferramenta**  
   :::column-end:::
   :::column span="2":::
      Para obter mais informações, navegue para obter [uma amostra de cor na página com o conta-gotas](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3D  
   :::column-end:::
   :::column span="1":::
      **Copiar para área de transferência**  
   :::column-end:::
   :::column span="2":::
      Copie o **valor de exibição** para a área de transferência.  
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
      A representação RGBA, HSLA ou hexa da cor.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Paleta de cores**  
   :::column-end:::
   :::column span="2":::
      Escolha um dos quadrados para alterar a cor para esse quadrado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Matiz**  
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
      08  
   :::column-end:::
   :::column span="1":::
      **Seletor de valor de exibição**  
   :::column-end:::
   :::column span="2":::
      Alternar entre as representações de RGBA, HSLA e HexA da cor atual.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      222  
   :::column-end:::
   :::column span="1":::
      **Seletor de paleta de cores**  
   :::column-end:::
   :::column span="2":::
      Alternar entre a [paleta de design de material][MaterialDesignColorSystem], uma paleta personalizada ou uma paleta de cores de página.  O DevTools gera a paleta de cores da página com base nas cores encontradas nas suas folhas de estilos.  
   :::column-end:::
:::row-end:::  

#### Exemplo de uma cor para fora da página com o conta-gotas  

Quando você abre o **seletor de cores**, o **conta-gotas** \ ( ![ conta-gotas ][ImageEyedropperIcon] \) é ativado por padrão.  Conclua as ações a seguir para alterar a cor selecionada para outra cor na página.  

1.  Passe o mouse sobre a cor de destino no visor.  
1.  Escolha confirmar.  
    
    > [!NOTE]
    > Na figura a seguir, o **seletor de cores** mostra um valor de cor atual de `rgba(0,0,0,0.7)` , que é próximo a preto.  A cor específica deve mudar para a versão do preto que está realçada no visor depois que você a escolheu.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Usar o conta-gotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Usar o conta-gotas  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Executar comandos com o menu de comando do Microsoft Edge DevTools | Documentos da Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Adicionar um PseudoState a uma classe-introdução ao visualizar e alterar CSS | Documentos da Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Exibir o CSS de um elemento-introdução ao modo de exibição e alteração de CSS | Documentos da Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS) | Documentos da Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Torne um arquivo minified legível – referência de depuração de JavaScript | Documentos da Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "O sistema de cores-design do material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "O modelo de caixa | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de seletor-específico | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/css/reference) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  