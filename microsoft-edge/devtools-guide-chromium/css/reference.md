---
title: Referência BITS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 4f0370b83d8c939476a1ed378dbdf750101c9527
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843961"
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







# Referência BITS   



Descubra novos fluxos de trabalho nesta referência abrangente do Microsoft Edge DevTools recursos relacionados à exibição e alteração da CSS.  

Confira [introdução e alterar CSS][DevToolsCSSGetStarted] para aprender as noções básicas.  

## Selecionar um elemento   

O painel **elementos** do devtools permite que você visualize ou altere a CSS de um elemento de cada vez.  O elemento selecionado é realçado na **árvore DOM**.  Os estilos do elemento são mostrados no painel **estilos** .  Consulte [Exibir o CSS de um elemento][DevToolsCSSGetStartedTutorial] para um tutorial.  

> [!NOTE]
> Na [Figura 1](#figure-1), o `h1` elemento que está realçado na **árvore DOM** é o elemento selecionado.  À direita, os estilos do elemento são mostrados no painel **estilos** .  À esquerda, o elemento é realçado na viewport, mas só porque o mouse está passando no momento sobre ele na **árvore DOM**.  

> ##### Figura 1  
> Um exemplo de um elemento selecionado  
> ![Um exemplo de um elemento selecionado][ImageSelectedElement]  

Há muitas maneiras de selecionar um elemento:  

*   No seu visor, clique com o botão direito do mouse no elemento e selecione **inspecionar**.  
*   No devtools, clique em **selecionar um elemento** , ![ Selecione um elemento ][ImageSelectAnElementIcon] ou pressione `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Shift` + `C` \ (MacOS \) e, em seguida, clique no elemento no visor.  
*   No DevTools, clique no elemento na **árvore DOM**.  
*   No DevTools, execute uma consulta como `document.querySelector('p')` no **console**, clique com o botão direito do mouse no resultado e selecione **revelar no painel de elementos**.  

## Exibir CSS   

### Exibir a folha de estilos externa na qual uma regra está definida   

No painel **estilos** , clique no link ao lado de uma regra CSS para abrir a folha de estilos externa que define a regra.  

Se a folha de estilos for minified, consulte [torne um arquivo do minified legível][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> Na [Figura 2](#figure-2), clicar `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` leva você até a linha 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , onde a `.content h1:first-of-type` regra CSS é definida.  

> ##### Figura 2  
> Exibir a folha de estilos onde uma regra está definida  
> ![Exibir a folha de estilos onde uma regra está definida][ImageViewRuleStylesheet]  

### Exibir apenas a CSS que é realmente aplicada a um elemento   

A guia **estilos** mostra todas as regras que se aplicam a um elemento, incluindo declarações que foram substituídas.  Quando você não está interessado em declarações substituídas, use a guia **calculada** para exibir apenas a CSS que está realmente sendo aplicada a um elemento.  

1.  [Selecione um elemento](#select-an-element).  
1.  Vá para a guia **calculada** no painel **elementos** .  

> [!NOTE]
> Em uma ampla janela do DevTools, a guia **calculada** não existe.  O conteúdo da guia **calculada** é mostrado na guia **estilos** .  

As propriedades herdadas são opacas.  Marque a caixa de seleção **Mostrar tudo** para ver todos os valores herdados.  

> [!NOTE]
> Na [Figura 3](#figure-3), a guia **calculada** mostra as propriedades CSS aplicadas ao elemento atualmente selecionado `h1` .  

> ##### Figura 3  
> A guia **calculada**  
> ![A guia calculada][ImageComputedTab]  

### Exibir as propriedades CSS em ordem alfabética   

Use a guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Exibir Propriedades CSS herdadas   

Marque a caixa de seleção **Mostrar tudo** na guia **calculada** .  Consulte [exibir apenas a CSS que é realmente aplicada a um elemento](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Exibir o modelo de caixa para um elemento   

Para exibir [o modelo de caixa][MDNBoxModel] de um elemento, acesse a guia **estilos** .  Se a janela do DevTools for restrita, o diagrama de **modelo de caixa** estará na parte inferior da guia.  

Para alterar um valor, clique duas vezes nele.  

> [!NOTE]
> Na [Figura 4](#figure-4), o diagrama de **modelo de caixa** na guia **estilos** mostra o modelo de caixa do elemento atualmente selecionado `h1` .  

> ##### Figura 4  
> O diagrama de **modelo de caixa**  
> ![O diagrama de modelo de caixa][ImageBoxModel]  

### Pesquisar e filtrar a CSS de um elemento   

Use a caixa de texto **Filtrar** nas guias **estilos** e **calculados** para pesquisar valores ou propriedades CSS específicas.  

Para pesquisar também as propriedades herdadas na guia **calculada** , marque a caixa de seleção **Mostrar tudo** .  

> [!NOTE]
> Na [Figura 5](#figure-5), a guia **estilos** é filtrada para mostrar apenas as regras que incluem a consulta de pesquisa `color` .  

> ##### Figura 5  
> Filtrando a guia **estilos**  
> ![Filtrando a guia estilos][ImageStylesFilter]  

> [!NOTE]
> Na [Figura 6](#figure-6), a guia **calculada** é filtrada para mostrar somente declarações que incluam a consulta de pesquisa `100%` .  

> ##### Figura 6  
> Filtrando a guia **calculada**  
> ![Filtrando a guia calculada][ImageComputerFilter]  

### Alternar uma pseudo-classe   

Para alternar entre uma pseudoclasse, como `:active` , `:focus` `:hover` ou `:visited` :  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **elementos** , vá para a guia **estilos** .  
1.  Clique em **: Hov**.  
1.  Verifique a pseudo-classe que você deseja habilitar.  

> [!NOTE]
> Na [Figura 7](#figure-7), alterne a `:hover` pseudo-classe.  Na viewport, verifique se a `background-color: cornflowerblue` declaração está sendo aplicada ao elemento, mesmo que o elemento não esteja realmente sendo focalizado.  

> ##### Figura 7  
> Como alternar a `:hover` pseudo-classe  
> ![Alternando o: hover pseudo-classe][ImagePseudoClass]  

Consulte [Adicionar um pseudo-estado a uma classe][DevToolsCSSGetStartedAddPseudoState] para um tutorial interativo. 

### Exibir uma página no modo de impressão   

Para exibir uma página no modo de impressão:  
1.  [Abrir o menu de comandos][DevToolsCommandMenu].  
1.  Comece a digitar `Rendering` e selecione `Show Rendering` .  
1.  Para a lista suspensa **emular mídia CSS** , selecione **Imprimir**.  

### Exibir CSS usado e não usado com a guia cobertura   

A guia cobertura mostra a CSS que uma página realmente usa.  

1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) enquanto o devtools estiver em foco para abrir o menu de comando.  
1.  Comece a digitar `coverage` e selecione **Mostrar cobertura**.  A guia cobertura é exibida.  
    
    > ##### Figura 8  
    > Abrindo a guia cobertura no menu comando  
    > ![Abrindo a guia cobertura no menu comando][ImageCommandMenu]  
    
    > ##### Figura 9  
    > A guia cobertura  
    > ![A guia cobertura][ImageCoverageEmpty]  
    
1.  Clique em **Iniciar cobertura de instrumentação e atualize a cobertura de** ![ Instrumentação de início de página e atualize a página ][ImageRefreshIcon] .  A página é atualizada e a guia cobertura fornece uma visão geral de quanto o CSS \ (e JavaScript \) é usado em cada arquivo que o navegador carrega.  Verde representa a CSS usada.  Vermelho representa a CSS não usada.  
    
    > ##### Figura 10  
    > Uma visão geral do quanto CSS (e JavaScript) é usado e não usado  
    > ![Uma visão geral do quanto CSS (e JavaScript) é usado e não usado][ImageCoverageOverview]  

1.  Clique em um arquivo CSS para ver uma divisão linha por linha de qual CSS ele usa.  
    
    > [!NOTE]
    > Na [Figura 11](#figure-11), as linhas 145 a 147 e 149 a 151 não `b66bc881.site-ltr.css` são usadas, enquanto as linhas 163 para 166 são usadas.  
    
    > ##### Figura 11  
    > Uma divisão linha por linha do CSS usado e não usado  
    > ![Uma divisão linha por linha do CSS usado e não usado][ImageCoverageDetail]  
    
### Modo de visualização de impressão forçado   

Consulte [forçar devtools no modo de visualização de impressão][DevToolsCssPrintPreview].  

## Alterar CSS   

<!-- todo s/CSS declaration/declaration/ -->  

### Adicionar uma declaração CSS a um elemento   

Como a ordem das declarações afeta a forma como um elemento é estilizado, você pode adicionar declarações de maneiras diferentes:  

*   [Adicione uma declaração embutida](#add-an-inline-declaration).  Equivalente a adicionar um `style` atributo ao HTML de um elemento.  
*   [Adicione uma declaração a uma regra de estilo](#add-a-declaration-to-a-style-rule).  

**Que fluxo de trabalho você deve usar?** Para a maioria dos cenários, você provavelmente deseja usar o fluxo de trabalho da declaração embutida.  As declarações embutidas têm uma prioridade mais alta do que as externas, portanto, o fluxo de trabalho embutido garante que as alterações entrem em vigor no elemento como você esperaria.  Consulte [tipos de seletores][MDNSelectorTypes] para obter mais informações sobre a específica.  

Se você estiver Depurando qualquer estilo do elemento e precisar testar especificamente o que acontece quando uma declaração é definida em locais diferentes, use o outro fluxo de trabalho.  

#### Adicionar uma declaração embutida   

Para adicionar uma declaração embutida:  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **estilos** , clique entre os colchetes da seção **elemento. Style** .  O cursor se concentra, permitindo que você insira texto.  
1.  Insira um nome de propriedade e pressione `Enter` .  
1.  Insira um valor válido para essa propriedade e pressione `Enter` .  Na **árvore DOM**, verifique se um `style` atributo foi adicionado ao elemento.  

> [!NOTE]
> Na [Figura 12](#figure-12), as `margin-top` Propriedades e foram `background-color` aplicadas ao elemento selecionado.  Na **árvore DOM** , verifique se as declarações são refletidas no `style` atributo para um elemento.  

> ##### Figura 12  
> Adicionando declarações embutidas  
> ![Adicionando declarações embutidas][ImageInlineDeclarations]  

#### Adicionar uma declaração a uma regra de estilo   

Para adicionar uma declaração a uma regra de estilo existente:  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **estilos** , clique entre os colchetes da regra de estilo à qual você deseja adicionar a declaração.  O cursor se concentra, permitindo que você insira texto.  
1.  Insira um nome de propriedade e pressione `Enter` .  
1.  Insira um valor válido para essa propriedade e pressione `Enter` .  

> ##### Figura 13  
> Adicionando a `border-bottom-style:groove` declaração a uma regra de estilo  
> ![Adicionando uma declaração a uma regra de estilo][ImageAddDeclarationExistingRule]  

### Alterar um nome ou valor de declaração   

Clique duas vezes no nome ou valor de uma declaração para alterá-la.  Consulte [alterar valores de declaração com atalhos de teclado](#change-declaration-values-with-keyboard-shortcuts) para atalhos para incrementar ou decrementar rapidamente um valor por `0.1` ,, `1` `10` ou `100` unidades.  

> ##### Figura 14  
> Alterar o valor da `border-bottom-style`  
> ![Alterar o valor de uma declaração][ImageAddDeclarationExistingRule2]  

### Alterar valores de declaração com atalhos de teclado   

Durante a edição do valor de uma declaração, você pode usar os seguintes atalhos de teclado para incrementar o valor por um valor fixo:  

*   Pressione `Alt` + `Up` \ (Windows \) ou `Option` + `Up` \ (MacOS \) para incrementar `0.1` .  
*   Pressione `Up` para alterar o valor por `1` , ou `0.1` se o valor atual estiver entre `-1` e `1` .  
*   Pressione `Shift` + `Up` para incrementar `10` .  
*   Pressione `Shift` + `Page Up` \ (Windows \) ou `Shift` + `Command` + `Up` \ (MacOS \) para incrementar o valor por `100` .  

O decréscimo também funciona.  Basta substituir cada ocorrência de `Up` mencionado acima por `Down` .  

### Adicionar uma classe a um elemento   

Para adicionar uma classe a um elemento:  

1.  [Selecione o elemento](#select-an-element) na **árvore DOM**.  
1.  Clique em **. CLS**.  
1.  Digite o nome da classe na caixa de texto **Adicionar nova classe** .  
1.  Pressione `Enter` .  

> ##### Figura 15  
> O painel **classes de elemento**  
> ![O painel classes de elemento][ImageElementClasses]  

### Alternar uma classe   

Para habilitar ou desabilitar uma classe em um elemento:  

1.  [Selecione o elemento](#select-an-element) na **árvore DOM**.  
1.  Abrir o painel **classes de elementos** .  Consulte [Adicionar uma classe a um elemento](#add-a-class-to-an-element).  Abaixo da caixa de texto **Adicionar nova classe** estão todas as classes que estão sendo aplicadas a esse elemento.  
1.  Alternar a caixa de seleção ao lado da classe que você deseja habilitar ou desabilitar.  

### Adicionar uma regra de estilo   

Para adicionar uma nova regra de estilo:  

1.  [Selecione um elemento](#select-an-element).  
1.  Clique em nova regra de **estilo** ![ nova regra de estilo ][ImageNewStyleRuleIcon] .  DevTools insere uma nova regra abaixo da regra **elemento. Style** .  

> [!NOTE]
> Na [Figura 16](#figure-16), devtools adiciona a `h1.devsite-page-title` regra de estilo depois de clicar em **nova regra de estilo**.  

> ##### Figura 16  
> Adicionando uma nova regra de estilo  
> ![Adicionando uma nova regra de estilo][ImageStyleRule]  

#### Escolha em qual folha de estilos você deseja adicionar uma regra   

Ao [Adicionar uma nova regra de estilo](#add-a-style-rule), clique e **mantenha nova regra de estilo** ![ nova regra ][ImageNewStyleRuleIcon] de estilo para escolher em qual folha de estilos adicionar a regra de estilo.  

> ##### Figura 17  
> Escolhendo uma folha de estilos  
> ![Escolhendo uma folha de estilos][ImageChooseStylesheet]  

#### Adicionar uma regra de estilo a um local específico   

Para adicionar uma regra de estilo a um local específico na guia **estilos** :  

1.  Passe o mouse sobre a regra de estilo que está diretamente acima de onde você deseja adicionar sua nova regra de estilo.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Clique em **Inserir regra de estilo abaixo** ![ Inserir regra de estilo abaixo ][ImageNewStyleRuleIcon] .  

> ##### Figura 18  
> **Inserir regra de estilo abaixo**  
> ![Inserir regra de estilo abaixo][ImageInsertStyleRuleBelow]  

### Revelar a barra de ferramentas mais ações   

A barra de ferramentas **mais ações** permite que você:  

*   Insira uma regra de estilo diretamente abaixo da que você está focalizado.  
*   Adicione uma `background-color` `color` declaração,, `box-shadow` ou `text-shadow` para a regra de estilo na qual você está focalizado.  

Para revelar a barra de ferramentas **mais ações** :  

1.  Na guia **estilos** , passe o mouse sobre uma regra de estilo.  **Mais ações** `...` é revelado no canto inferior direito da seção de regra de estilo.  
    
    > [!NOTE]
    > Na [Figura 19](#figure-19), passe o mouse sobre a `.header-holder.has-default-focus` regra de estilo e **mais ações** são reveladas no canto inferior direito da seção de regra de estilo.  
    
    > ##### Figura 19  
    > Revelando **mais ações**  
    > ![Revelando mais ações][ImageRevealMore]  
    
1.  Passe o mouse sobre **mais ações** `...` para revelar as ações mencionadas acima.  
    
    > [!NOTE]
    > A ação **Inserir regra de estilo abaixo** é revelada depois de passar o mouse sobre **mais ações**.  
    
    > ##### Figura 20  
    > A barra de ferramentas **mais ações**  
    > ![A barra de ferramentas mais ações][ImageInsertStyleRuleBelow2]  
    
### Alternar uma declaração   

Para ativar ou desativar uma única declaração:  

1.  [Selecione um elemento](#select-an-element).  
1.  No painel **estilos** , passe o mouse sobre a regra que define a declaração.  As caixas de seleção aparecem ao lado de cada declaração.  
1.  Marque ou desmarque a caixa de seleção ao lado da declaração.  Quando você desmarca uma declaração, o DevTools a risca para indicar que não está mais ativo.  

> [!NOTE]
> Na [Figura 21](#figure-21), a `margin-top` Propriedade do elemento selecionado no momento foi desativada.  

> ##### Figura 21  
> Como alternar uma declaração  
> ![Como alternar uma declaração][ImageToggleDeclaration]  

### Adicionar uma declaração de cor de plano de fundo   

Para adicionar uma `background-color` declaração a um elemento:  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `background-color` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Clique em **adicionar cor de plano de fundo** ![ adicionar cor de plano de fundo ][ImageAddBackgroundColorIcon] .  

> ##### Figura 22  
> **Adicionar cor de plano de fundo**  
> ![Adicionar cor de plano de fundo][ImageAddBackgroundColor]  

### Adicionar uma declaração de cor   

Para adicionar uma `color` declaração a um elemento:  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `color` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Clique em **adicionar cor** ![ adicionar cor ][ImageAddColorIcon] .  

> ##### Figura 23  
> **Adicionar cor**  
> ![Adicionar cor][ImageAddColor]  

### Adicionar uma declaração de caixa-sombra   

Para adicionar uma `box-shadow` declaração a um elemento:  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `box-shadow` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Clique em **Adicionar caixa** ![ Adicionar à caixa Adicionar sombra ][ImageAddBoxShadowIcon] .  

> ##### Figura 24  
> **Adicionar sombra à caixa**  
> ![Adicionar sombra à caixa][ImageAddBoxShadow]  

### Adicionar uma declaração de sombra de texto   

Para adicionar uma `text-shadow` declaração a um elemento:  

1.  Passe o mouse sobre a regra de estilo à qual você deseja adicionar a `text-shadow` declaração.  
1.  [Revelar a barra de ferramentas **mais ações** ](#reveal-the-more-actions-toolbar).  
1.  Clique em **Adicionar sombra de texto** ![ Adicionar sombra de texto ][ImageAddTextShadowIcon] .  

> ##### Figura 25  
> **Adicionar sombra de texto**  
> ![Adicionar sombra de texto][ImageAddTextShadow]  

### Alterar as cores com o seletor de cores   

O **seletor de cores** fornece uma GUI para alteração `color` e `background-color` declarações.  

Para abrir o **seletor de cores**:  

1.  [Selecione um elemento](#select-an-element).  
1.  Na guia **estilos** , localize a `color` declaração, `background-color` ou semelhante, que você deseja alterar.  À esquerda do `color` `background-color` valor, ou semelhante, há um quadrado pequeno que é uma visualização da cor.  
    
    > [!NOTE]
    > Na [Figura 26](#figure-26), o pequeno quadrado à esquerda de `rgba(0, 0, 0, 0.7)` é uma visualização da cor.  
    
    > ##### Figura 26  
    > Visualização de cores  
    > ![Visualização de cores][ImageColorPreview]  
    
1.  Clique na visualização para abrir o **seletor de cores**.  
    
    > ##### Figura 27  
    > O **seletor de cores**  
    > ![O seletor de cores][ImageColorPicker]  
    
Aqui está uma descrição de cada um dos elementos de interface do usuário do **seletor de cores**:  

> ##### Figura 28  
> O seletor de cores, anotado  
> ![O seletor de cores, anotado][ImageColorPickerAnnotated]  

1.  **Sombras**.  
1.  **Conta-gotas**.  Consulte [obter uma amostra de uma cor na página com o conta-gotas](#sample-a-color-off-the-page-with-the-eyedropper).  
1.  **Copiar para a área de transferência**.  Copie o **valor de exibição** para a área de transferência.  
1.  **Valor de exibição**.  A representação RGBA, HSLA ou hexa da cor.  
1.  **Paleta de cores**.  Clique em um desses quadrados para alterar a cor para esse quadrado.  
1.  **Matiz**.  
1.  **Opacidade**.  
1.  **Seletor de valor de exibição**.  Alternar entre as representações de RGBA, HSLA e HexA da cor atual.  
1.  **Interruptor de paleta de cores**.  Alternar entre a [paleta de design de material][MaterialDesignColorSystem], uma paleta personalizada ou uma paleta de cores de página.  O DevTools gera a paleta de cores da página com base nas cores encontradas nas suas folhas de estilos.  

#### Exemplo de uma cor para fora da página com o conta-gotas   

Quando você abre o **seletor de cores**, o conta-gotas do **conta** -gotas ![ ][ImageEyedropperIcon] está ativado por padrão.  Para alterar a cor selecionada para outra cor na página:  

1.  Passe o mouse sobre a cor de destino no visor.  
1.  Clique em para confirmar.  
    
    > [!NOTE]
    > Na [Figura 29](#figure-29), o **seletor de cores** mostra um valor de cor atual de `rgba(0,0,0,0.7)` , que é próximo a preto.  Essa cor deve mudar para o preto que está realçado no visor quando o preto foi clicado.  
    
    > ##### Figura 29  
    > Usar o conta-gotas  
    > ![Usar o conta-gotas][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Figura 1: um exemplo de um elemento selecionado"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Figura 2: exibir a folha de estilos na qual uma regra está definida"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Figura 3: a guia calculada"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Figura 4: o diagrama de modelo de caixa"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Figura 5: filtrando a guia estilos"  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Figura 6: filtrando a guia calculada"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Figura 7: alternando o: hover pseudo-classe"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Figura 8: abrindo a guia cobertura no menu de comando"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Figura 9: a guia cobertura"  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Figura 10: uma visão geral do quanto CSS (e JavaScript) é usado e não usado"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Figura 11: divisão linha por linha de CSS usada e não usada"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Figura 12: adicionando declarações embutidas"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Figura 13: adicionando uma declaração a uma regra de estilo"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Figura 14: alterando o valor de uma declaração"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Figura 15: painel classes de elemento"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Figura 16: adicionando uma nova regra de estilo"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Figura 17: escolhendo uma folha de estilos"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Figura 18: inserir regra de estilo abaixo"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Figura 19: revelando mais ações"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Figura 20: a barra de ferramentas mais ações"  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Figura 21: alternando uma declaração"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Figura 22: adicionar cor de plano de fundo"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Figura 23: adicionar cor"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Figura 24: Adicionar sombra à caixa"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Figura 25: Adicionar sombra de texto"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Figura 26: visualização de cores"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Figura 27: o seletor de cores"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Figura 28: o seletor de cores, anotado"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Figura 29: usando o conta-gotas"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Adicionar um PseudoState a uma classe-introdução ao exibir e alterar CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Exibir o CSS para um elemento-introdução à exibição e alteração de CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Forçar o Microsoft Edge DevTools no modo de visualização de impressão (tipo de mídia de impressão CSS)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Torne um arquivo minified legível – referência de depuração de JavaScript"  

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
