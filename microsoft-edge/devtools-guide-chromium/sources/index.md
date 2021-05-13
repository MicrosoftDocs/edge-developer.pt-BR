---
description: Use a ferramenta Sources para exibir, modificar e depurar JavaScript retornado pelo servidor e inspecionar os recursos que comem a página da Web atual.  Para usar a ferramenta Sources como um ambiente de desenvolvimento, adicione arquivos de origem a um Workspace.
title: Visão geral da ferramenta Fontes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: d3ef49bf986d8827216bd0bc183e45806aa0a2c3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564711"
---
# <a name="sources-tool-overview"></a>Visão geral da ferramenta Fontes  

Use a **ferramenta Sources** para exibir, modificar e depurar código JavaScript front-end e inspecionar os recursos que comem a página da Web atual.  A **ferramenta Sources** tem três painéis:  

| Painel | Ações |  
|:--- |:--- |  
| **Painel navegador** | Navegue entre os recursos retornados do servidor para construir a página da Web atual.  Selecione arquivos, imagens e outros recursos e veja seus caminhos.  Opcionalmente, configurar um Espaço de Trabalho local para salvar alterações diretamente nos arquivos de origem.  |  
| **Painel editor** | Exibir JavaScript, HTML, CSS e outros arquivos retornados do servidor.  Faça edições experimentais em JavaScript ou CSS.  Suas alterações serão preservadas até que você atualize a página ou seja preservada após a atualização da página se você salvar em um arquivo local com Espaços de Trabalho.  Ao usar Espaços de Trabalho ou Substituições, você também pode editar arquivos HTML.  |  
| **Painel de depurador** | Use o Depurador JavaScript para definir pontos de interrupção, pausar a execução do JavaScript e passar pelo código, incluindo todas as edições feitas, enquanto observa quaisquer expressões JavaScript que você especificar.  Assista e altere manualmente os valores das variáveis que estão no escopo da linha de código atual.  |  

A figura a seguir mostra o painel **Navegador** realçado com uma caixa vermelha no canto superior esquerdo do DevTools, o painel **Editor** realçado na parte superior direita e o painel **Depurador** realçado na parte inferior.  No lado esquerdo, está a parte principal da janela do navegador, mostrando a página da Web renderizada acinzenada porque o depurador é pausado em um ponto de interrupção:

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Os painéis da ferramenta Sources, em layout estreito" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   Os painéis da ferramenta Sources, em layout estreito  
:::image-end:::  

Quando o DevTools é largo, o painel **Depurador** é colocado à direita e inclui **Escopo** e **Assistir**:  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Navegar, exibir, editar e depurar JavaScript retornado pelo servidor" lightbox="../media/sources-panes-wide-layout.msft.png":::
   Navegar, exibir, editar e depurar JavaScript retornado pelo servidor  
:::image-end:::  

Para maximizar o tamanho da ferramenta Sources, desfaça DevTools em uma janela separada e, opcionalmente, mova a janela DevTools para um monitor separado.  Consulte [Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Encaixar para baixo, Doca para a esquerda)][DevToolsCustomizePlacement].

Para carregar a página da Web de demonstração de depuração mostrada acima, consulte A abordagem básica para usar um [depurador](#the-basic-approach-to-using-a-debugger), abaixo.

## <a name="using-the-navigator-pane-to-select-files"></a>Usando o painel Navegador para selecionar arquivos

Use o **painel** Navegador \(à esquerda\) para navegar entre os recursos retornados do servidor para construir a página da Web atual.  Selecione arquivos, imagens e outros recursos e veja seus caminhos.  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="O painel Navegador" lightbox="../media/navigator-pane.msft.png":::
   O **painel Navegador**
:::image-end:::  

Para acessar quaisquer guias ocultas do painel Navegador, selecione ![ Mais guias ](../media/more-tabs-icon.msft.png) \( Mais**guias**\).

As subseções a seguir abrangem o painel Navegador:  

*   [Usando a guia Página para explorar recursos que constroem a página da Web atual](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)  
*   [Usando a guia Sistema de Arquivos para definir um Espaço de Trabalho local](#using-the-filesystem-tab-to-define-a-local-workspace)  
*   [Usando a guia Substituições para substituir arquivos de servidor com arquivos locais](#using-the-overrides-tab-to-override-server-files-with-local-files)  
*   [Usando a guia Scripts de conteúdo para Microsoft Edge extensões](#using-the-content-scripts-tab-for-microsoft-edge-extensions)  
*   [Usando a guia Trechos de Código para executar trechos de código JavaScript em qualquer página](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)  
*   [Usando o Menu de Comando para abrir arquivos](#using-the-command-menu-to-open-files)  
    
### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a>Usando a guia Página para explorar recursos que constroem a página da Web atual

Use a **guia Página** do painel **Navegador** para explorar o sistema de arquivos retornado do servidor para construir a página da Web atual.  Selecione um arquivo JavaScript para exibi-lo, editá-lo e depurá-lo.  A **guia Página** lista todos os recursos carregados pela página.

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="A guia Página no painel Navegador da ferramenta Sources" lightbox="../media/sources-page-tab.msft.png":::
   A **guia Página** no painel **Navegador** da ferramenta **Sources**
:::image-end:::  

Para exibir um arquivo no painel **Editor,** selecione um arquivo **na** guia Página.  Para uma imagem, uma visualização da imagem é exibida.  
Para exibir a URL ou o caminho de um recurso, passe o mouse sobre o recurso.  
Para carregar um arquivo em uma nova guia do navegador ou para exibir outras ações, clique com o botão direito do mouse no nome do arquivo.  

#### <a name="icons-in-the-page-tab"></a>Ícones na guia Página

A **guia Página** usa os seguintes ícones:  

*   O **ícone** da janela, juntamente com o rótulo `top` , representa o quadro principal do documento, que é um [quadro HTML][W3CHtml4Frames].  
*   O **ícone de** nuvem representa uma [origem][WhatwgHtmlSpecMulitpageOriginHtmlOrigin].  
*   O **ícone de** pasta representa um diretório.  
*   O **ícone** da página representa um recurso.  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a>Arquivos de grupo por pasta ou como uma lista simples

A **guia Página** exibe arquivos ou recursos agrupados por servidor e diretório ou como uma lista simples.

Para alterar como os recursos são agrupados:

1.  Ao lado das guias no painel Navegador \(à esquerda\), selecione **o botão ...** \( Mais**opções**\).  Um menu é exibido.  
1.  Selecione ou deslele **a opção Grupo por** pasta.  
    
### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a>Usando a guia Sistema de Arquivos para definir um Espaço de Trabalho local

Use a guia **Sistema** de Arquivos do painel **Navegador** para adicionar arquivos a um Espaço de Trabalho, para que as alterações feitas no DevTools são salvas no sistema de arquivos local.  
Um arquivo que está em um Espaço de Trabalho é indicado por um ponto verde ao lado do nome do arquivo, em todo o DevTools.  

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="A guia Sistema de Arquivos, para um Espaço de Trabalho" lightbox="../media/sources-filesystem-tab.msft.png":::
   A **guia Sistema de** Arquivos, para um Espaço de Trabalho
:::image-end:::  

Por padrão, quando você edita um arquivo na ferramenta **Fontes,** suas alterações são descartadas quando você atualize a página da Web.  A **ferramenta Sources** funciona com uma cópia dos recursos front-end retornados pelo servidor Web.  Quando você modifica esses arquivos front-end retornados pelo servidor, as alterações não persistem, pois você não alterou os arquivos de origem.  Você também precisa aplicar suas edições no código-fonte real e, em seguida, implantar no servidor.  
Por outro lado, quando você usa um Workspace, as alterações feitas no código front-end são preservadas quando você atualize a página da Web.  Com um Workspace, quando você edita o código front-end retornado pelo servidor, a ferramenta Sources também aplica suas edições ao código-fonte local.  Em seguida, para que outros usuários vejam suas alterações, você só precisa reimplantar seus arquivos de origem alterados para o servidor.  
Os espaços de trabalho funcionam bem quando o código JavaScript retornado pelo servidor é o mesmo que o código-fonte JavaScript local.  Os espaços de trabalho não funcionam tão bem quando seu fluxo de trabalho envolve transformações em seu código-fonte, como a minificação ou a [compilação TypeScript.][TypescriptlangMain]  

Para obter mais informações, consulte o tutorial [Editar arquivos com espaços de trabalho][DevtoolsGuideChromiumWorkspacesIndex].

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a>Usando a guia Substituições para substituir arquivos de servidor com arquivos locais

Use a **guia Substituições** do painel **Navegador** para substituir ativos de página \(como imagens\) com arquivos de uma pasta local.  
Os itens nesta guia substituem o que o servidor envia para o navegador, mesmo depois que o servidor envia os ativos.  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="A guia Substituições do painel Navegador" lightbox="../media/overrides-tab.msft.png":::
   A **guia Substituições** do painel **Navegador**
:::image-end:::  

O **recurso Substituições** é semelhante a Workspaces.  Use Substituições quando quiser experimentar alterações em uma página da Web e você precisa manter as alterações depois de atualizar a página da Web, mas não se importa em mapear suas alterações no código-fonte da página da Web.  

Um arquivo que substitui um arquivo retornado pelo servidor é indicado por um ponto roxo ao lado do nome do arquivo, em todo o DevTools.

#### <a name="see-also"></a>Ver também

*   [Substituir recursos de página da Web com cópias locais usando Microsoft Edge DevTools][DevtoolsJavascriptOverrides]  
*   [Mapear código pré-processador para código-fonte][DevToolsJavaScriptSourceMaps]  
    
### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a>Usando a guia Scripts de conteúdo para Microsoft Edge extensões

Use a **guia Scripts de** conteúdo do painel **Navegador** para exibir quaisquer scripts de conteúdo carregados por uma extensão Microsoft Edge que você instalou.  

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="A guia Scripts de conteúdo do painel Navegador" lightbox="../media/content-scripts-tab.msft.png":::
   A **guia Scripts de** conteúdo do painel **Navegador**
:::image-end:::  

Quando o depurador entra no código que você não reconhece, talvez você queira marcar esse código como código biblioteca, para evitar entrar nesse código.  Consulte [Marcar scripts de conteúdo como código biblioteca][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].

#### <a name="see-also"></a>Ver também

*   [Scripts de conteúdo][MdnAddOnsWebextensionsContentScripts]  
*   [Criar um tutorial para extensão Parte 2][ExtensionsChromiumGetstartPart2ContentScripts]  
    
### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a>Usando a guia Trechos de Código para executar trechos de código JavaScript em qualquer página da Web

Use a **guia Trechos** de Código do painel **Navegador** para criar e salvar trechos de código JavaScript, para que você possa executar facilmente esses trechos em qualquer página da Web.

:::image type="complex" source="../media/snippet.msft.png" alt-text="Um trecho que insere a biblioteca jQuery em uma página da Web" lightbox="../media/snippet.msft.png":::
   Um trecho que insere a biblioteca jQuery em uma página da Web  
:::image-end:::  

Por exemplo, suponha que você insira com frequência o seguinte código no **Console**, para inserir a biblioteca jQuery em uma página para que você possa executar comandos jQuery no **Console**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Em vez disso, você pode salvar esse código em **um trecho de código** e, em seguida, execute-o facilmente sempre que precisar.  Quando você seleciona `Ctrl` + `S` \(Windows/Linux\) ou `Command` + `S` \(macOS\), o DevTools **** salva o trecho em seu sistema de arquivos.  

Há várias maneiras de executar um trecho de código:  

*   No painel **Navegador,** selecione a guia **Trechos** de Código e selecione o arquivo de trechos para abri-lo.  Em seguida, na parte inferior do painel Editor, selecione **Executar** \( ![ O botão Executar ](../media/run-snippet-icon.msft.png) \).  
*   Quando DevTools tiver foco, selecione `Ctrl` + `P` \(Windows/Linux\) ou `Command` + `P` [][DevToolsCommandMenuIndex]\(macOS\) `!` para abrir o Menu de Comando e digite .  
    
Trechos de código são semelhantes aos indicadores.

#### <a name="see-also"></a>Ver também

*   [Executar trechos de código do JavaScript em qualquer página da Web com Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptSnippets]  
    
### <a name="using-the-command-menu-to-open-files"></a>Usando o Menu de Comando para abrir arquivos

Para abrir um arquivo, além de usar o painel **Navegador** na ferramenta **Fontes,** você pode usar o Menu de Comando de qualquer lugar no DevTools.

*   Em qualquer lugar no DevTools, selecione `Ctrl` + `P` em Windows/Linux `Command` + `P` ou no macOS.  O Menu de Comando é exibido e lista todos os recursos que estão nas guias do painel **Navegador** da **ferramenta Sources.**  
*   Ou, ao lado das guias do painel **** **Navegador** na ferramenta Fontes, selecione **o botão ...** \( Mais**opções**\) e selecione **Abrir Arquivo**.  

Para exibir e escolher de uma lista de todos os arquivos .js, digite `.js` .

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Abrir um arquivo usando o Menu de Comando" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   Abrir um arquivo usando o Menu de Comando
:::image-end:::

Se você digitar `?` , o Menu de Comando mostrará vários comandos, incluindo **...  Abrir arquivo**.  Se você selecionar `Backspace` para limpar o Menu de Comando, uma lista de arquivos será mostrada.

Para obter mais informações, [consulte Executar comandos com o menu de comando Microsoft Edge DevTools][DevToolsCommandMenuIndex].

## <a name="using-the-editor-pane-to-view-or-edit-files"></a>Usando o painel Editor para exibir ou editar arquivos

Use o **painel Editor** para exibir os arquivos front-end retornados do servidor para compor a página da Web atual, incluindo JavaScript, HTML, CSS e arquivos de imagem.  Quando você edita os arquivos front-end no **painel Editor,** o DevTools atualiza a página da Web para executar o código modificado.  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="O painel Editor na ferramenta Fontes" lightbox="../media/editor-pane.msft.png":::
   O **painel Editor** na ferramenta **Fontes**  
:::image-end:::

O **painel Editor** tem o seguinte nível de suporte para vários tipos de arquivo:  

| Tipo de arquivo | Ações com suporte |  
|:--- |:--- |  
| JavaScript | Exibir, editar e depurar.  |  
| CSS | Exibir e editar.  |  
| HTML | Exibir e editar.  |  
| Images | Exibir.  |  

Por padrão, as edições são descartadas quando você atualize a página da Web.  Para obter informações sobre como salvar as alterações no sistema de arquivos, consulte [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), above.

As subseções a seguir abrangem o painel Editor:  

*   [Editando um arquivo JavaScript](#editing-a-javascript-file)  
*   [Reformatar um arquivo JavaScript minificado com impressão bastante impressa](#reformatting-a-minified-javascript-file-with-pretty-print)  
*   [Mapeamento de código minificado para seu código-fonte para mostrar código acessível](#mapping-minified-code-to-your-source-code-to-show-readable-code)  
*   [Transformações do código-fonte para o código front-end compilado](#transformations-from-source-code-to-compiled-front-end-code)  
*   [Editando um arquivo CSS](#editing-a-css-file)  
*   [Editar um arquivo HTML](#editing-an-html-file)  
*   [Indo para um número de linha ou função](#going-to-a-line-number-or-function)  
*   [Exibindo arquivos de origem ao usar uma ferramenta diferente](#displaying-source-files-when-using-a-different-tool)  
    
### <a name="editing-a-javascript-file"></a>Editando um arquivo JavaScript

Para editar um arquivo JavaScript no DevTools, use o **painel Editor,** na **ferramenta Sources.**

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Editando JavaScript no painel Editor" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   Editando JavaScript no **painel Editor**  
:::image-end:::

Para carregar um arquivo no painel Editor, use a guia **Página** no painel **Navegador** \(à esquerda\).  Ou use o **Menu de**Comando , da seguinte forma: no canto superior direito do DevTools, selecione Personalizar e controlar **DevTools** \( \) e selecione `...` Abrir **Arquivo**.

#### <a name="save-and-undo"></a>Salvar e Desfazer

Para que as alterações do JavaScript entre em vigor, selecione `Ctrl` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\).  

Se você alterar um arquivo, um asterisco será exibido ao lado do nome do arquivo.  

*   Para salvar alterações, selecione `Ctrl` + `S` em Windows/Linux `Command` + `S` ou no macOS.  
*   Para desfazer uma alteração, selecione `Ctrl` + `Z` em Windows/Linux ou `Command` + `Z` no macOS.  
    
Por padrão, suas edições são descartadas quando você atualize a página da Web.  Para obter mais informações sobre como salvar as alterações no sistema de arquivos local, consulte [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].

#### <a name="find-and-replace"></a>Encontrar e substituir

Para encontrar texto no arquivo atual, selecione o painel **Editor** para dar foco a ele e selecione em `Ctrl` + `F` Windows/Linux ou `Command` + `F` no macOS.  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Encontrar e substituir, no painel Editor da ferramenta Fontes" lightbox="../media/find-replace.msft.png":::
   **Encontrar** e **substituir**, no **painel Editor** da **ferramenta Sources**
:::image-end:::

Para encontrar e substituir texto, selecione o botão **Substituir** \(**A-\>B**\) à esquerda da caixa **de** texto Encontrar.  O **botão** Substituir \(**A-\>B**\) é exibido ao exibir um arquivo editável.

#### <a name="showing-the-changes-you-made"></a>Mostrando as alterações feitas

Para revisar as alterações feitas em um arquivo, clique com o botão direito do mouse no painel **Editor** e selecione **Modificações Locais.**

A **Gaveta** é aberta na parte inferior do DevTools, mostrando suas alterações na **guia Alterações.**

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Mostrando modificações locais, na guia Alterações da Gaveta" lightbox="../media/local-modifications.msft.png":::
   Mostrando **modificações locais**, na guia **Alterações** da **Gaveta**
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a>Alterações dentro de uma função entrarão em vigor

O DevTools não executará um script de novo, portanto, as únicas alterações do JavaScript que têm efeito são as alterações feitas em funções.  Por exemplo, na figura a seguir, adicionamos o seguinte código ao JavaScript retornado pelo servidor:  
*   Adicionamos a instrução `console.log('A')` fora de qualquer função.  
*   Adicionamos a instrução `console.log('B')` dentro de uma `onClick` função.  
Salvamos as alterações, os números inseridos no formulário e selecionamos o botão de formulário para enviar o formulário.  

Depois de enviar o formulário, , que está no escopo global, não é executado, mas , dentro de uma função, é executado, saída `console.log('A')` `console.log('B')` para o `onClick` `B` Console:

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript de escopo global não é executado de acordo com o escopo global" lightbox="../media/edit-js.msft.png":::
   JavaScript de escopo global não é executado de acordo com o escopo global  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a>Reformatar um arquivo JavaScript minificado com impressão bastante impressa

Para usar a impressão bastante impressa para reformatar um **** arquivo para torná-lo acessível, selecione o botão De impressão bonito \( Format \), que é mostrado como chaves, na parte inferior do ![ painel ](../media/format-icon.msft.png) Editor.  Ou, se um **botão Pretty-print** aparecer na parte superior do painel Editor, você poderá selecionar esse botão.

:::image type="complex" source="../media/minified.msft.png" alt-text="O botão de impressão Pretty" lightbox="../media/minified.msft.png":::
   O **botão de impressão** Pretty  
:::image-end:::  

O arquivo reformatado aparece em uma nova guia, com `:formatted` anexado ao nome do arquivo.  O código reformatado é somente leitura.  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Um arquivo JavaScript bastante impresso (reformatado)" lightbox="../media/pretty-printed.msft.png":::
   Um arquivo JavaScript bastante impresso \(reformatted\)  
:::image-end:::  

Para fazer o arquivo reformatado rolar para o código selecionado no arquivo minificado:  

1.  Se a guia arquivo reformatado estiver aberta, feche-a.  
1.  Selecione algum código no arquivo minificado no painel Editor.
1.  Selecione o **botão De impressão** bonito.  
     
O código formatado aparece em uma nova guia, rolada para o código selecionado.

Para obter mais informações, [consulte Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a>Mapeamento de código minificado para seu código-fonte para mostrar código acessível

Mapas de origem de pré-processadores fazem com que o DevTools carregue seus arquivos de origem JavaScript originais, além de seus arquivos JavaScript minificados e transformados que são retornados pelo servidor.  Em seguida, você exibirá seus arquivos de origem originais enquanto definir pontos de interrupção e passar o código.  Enquanto isso, Microsoft Edge está executando seu código minificado.  

No painel **Editor,** se você clicar com o botão direito do mouse em um arquivo JavaScript e, em seguida, selecionar Adicionar mapa de origem **,** uma caixa pop-up será exibida, com uma caixa de texto **URL** de mapa de origem e um **botão Adicionar.**

A abordagem de mapeamento de origem mantém seu código front-end acessível e depurável mesmo depois de combiná-lo, minificá-lo ou compilá-lo.
Para obter mais informações, consulte [Map preprocessado code to source code][DevToolsJavaScriptSourceMaps].

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a>Transformações do código-fonte para o código front-end compilado

Se você usar uma estrutura que transforme seus arquivos JavaScript, como React, sua fonte local JavaScript pode ser diferente do JavaScript front-end retornado pelo servidor.  Não há suporte para espaços de trabalho nesse cenário, mas há suporte para mapeamento de código-fonte nesse cenário.  

Em um ambiente de desenvolvimento, seu servidor pode incluir seus mapas de origem e seus arquivos originais `.ts` `.jsx` ou React.  A **ferramenta Sources** exibe esses arquivos, mas não permite que você edite esses arquivos.  Quando você definir pontos de interrupção e usar o depurador, o DevTools exibe seus arquivos originais ou, na verdade, passo a passo pela versão minificada de seus `.ts` `.jsx` arquivos JavaScript.

Nesse cenário, a **ferramenta Sources** é útil para inspecionar e examinar o JavaScript de front-end transformado que é retornado do servidor.  Use o depurador para definir expressões de Watch e use o Console para inserir expressões JavaScript para manipular dados que estão no escopo.

### <a name="editing-a-css-file"></a>Editando um arquivo CSS

Há duas maneiras de editar CSS no DevTools:  

*   Na ferramenta **Elementos,** você trabalha com uma configuração CSS por vez, por meio de controles de interface do usuário.  Essa abordagem é recomendada na maioria dos casos.  Para obter mais informações, [consulte Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].  
*   Na ferramenta **Fontes,** você usa um editor de texto.  
    
A ferramenta Sources dá suporte à edição direta de um arquivo CSS.  Por exemplo, se você editar o arquivo CSS do tutorial Editar arquivos com [espaços][DevtoolsGuideChromiumWorkspacesIndex] de trabalho para corresponder à regra de estilo abaixo, o elemento no canto superior esquerdo da página da Web renderizada muda `H1` para verde:

```css
h1 {
  color: green;
}  
```  

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS no painel Editor para alterar a cor do texto do título H1 para verde" lightbox="../media/edit-css.msft.png":::
   Editar CSS no **painel Editor** para alterar a cor do texto do título `H1` para verde  
:::image-end:::  

As alterações CSS vigoram imediatamente; você não precisa salvar manualmente as alterações.

#### <a name="see-also"></a>Ver também  

*   [Editar estilos de fonte CSS e configurações no painel Estilos][DevToolsInspectStylesEditFonts]  
*   [DevTools para iniciantes: Introdução ao CSS][DevToolsBeginnersCss] - tutorial  
    
### <a name="editing-an-html-file"></a>Editar um arquivo HTML

Há duas maneiras de editar HTML no DevTools:  

*   Na ferramenta **Elementos,** você trabalha com um elemento HTML por vez, por meio de controles de interface do usuário.  
*   Na ferramenta **Fontes,** você usa um editor de texto.  
    
:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="O editor HTML da ferramenta Sources" lightbox="../media/sources-html-editor.msft.png":::
   O editor HTML da **ferramenta Sources**
:::image-end:::  

Ao contrário de um arquivo JavaScript ou CSS, um arquivo HTML retornado pelo servidor Web não pode ser editado diretamente na ferramenta Sources.  Para editar um arquivo HTML usando o Editor da ferramenta Fontes, o arquivo HTML deve estar em um Espaço de Trabalho ou na guia **Substituições.**  Consulte estas subseções do artigo atual:  

*   [Usando a guia Sistema de Arquivos para definir um Espaço de Trabalho local](#using-the-filesystem-tab-to-define-a-local-workspace)  
*   [Usando a guia Substituições para substituir arquivos de servidor com arquivos locais](#using-the-overrides-tab-to-override-server-files-with-local-files)  
   
Para salvar alterações, selecione `Ctrl` + `S` em Windows/Linux `Command` + `S` ou no macOS.  Um arquivo editado é marcado por um asterisco.  
Para encontrar texto, selecione `Ctrl` + `F` em Windows/Linux ou `Command` + `F` no macOS.  
Para desfazer uma edição, selecione `Ctrl` + `Z` em Windows/Linux `Command` + `Z` ou no macOS.  
Para exibir outros comandos durante a edição de um arquivo HTML, no painel Editor, clique com o botão direito do mouse no arquivo HTML.  
Você também pode editar HTML usando um editor HTML, em vez de DevTools.  Por exemplo, o artigo [DevTools para iniciantes:][DevToolsBeginnersHtml] Começar com HTML e o DOM usa um site que habilita a edição HTML na página da Web.  

### <a name="going-to-a-line-number-or-function"></a>Indo para um número de linha ou função

Para ir para um número de linha ou símbolo \(como um nome de função\) no arquivo que está aberto no painel Editor, você pode usar o Menu de Comando, em vez de rolar pelo arquivo.

1.  No painel **Navegador,** selecione as releições \( `...` \) \(**Mais opções**\) e selecione **Abrir Arquivo**.  O Menu de Comando é exibido.  
1.  Digite um dos seguintes caracteres:  
     
| Character | Nome do comando | Finalidade |  
|:--- |:--- |:--- |  
| \: | **Ir para a linha** | Vá para um número de linha.  |  
| \@ | **Ir para o símbolo** | Vá para uma função.  Quando você digita , o Menu de Comando lista as funções encontradas no arquivo JavaScript que está `@` aberto no painel Editor.  |  
   
Para obter mais informações, [consulte Executar comandos com o menu de comando Microsoft Edge DevTools][DevToolsCommandMenuIndex].

### <a name="displaying-source-files-when-using-a-different-tool"></a>Exibindo arquivos de origem ao usar uma ferramenta diferente

O principal local para exibir arquivos de origem no DevTools está na **ferramenta Sources.**  Mas, às vezes, você precisa acessar outras ferramentas, como **Elementos** ou **Console**, durante a exibição ou edição de seus arquivos de origem.  Use a **ferramenta Fontes Rápidas** na [Gaveta][DevtoolsCustomizeIndexDrawer].  

1.  Selecione uma ferramenta diferente da **ferramenta Sources,** como a **ferramenta Elements.**  
1.  Selecione `Ctrl` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).  O Menu de Comando é aberto.  
1.  Digite `Quick Source` e selecione Mostrar Fonte **Rápida**.  Na parte inferior da janela DevTools, a Gaveta é exibida, com o **painel De origem** rápida selecionado.  O **painel Fonte Rápida** contém o último arquivo editado na ferramenta **Fontes,** dentro de uma versão compacta do editor de código DevTools.  
1.  Selecione `Ctrl` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\) para abrir a **caixa de diálogo Abrir Arquivo.**  
    
## <a name="using-the-debugger-pane-to-debug-javascript-code"></a>Usando o painel Depurador para depurar código JavaScript

Use o depurador JavaScript para passar pelo código JavaScript retornado pelo servidor.  
O depurador inclui o painel **Depurador,** juntamente com pontos de interrupção que você definir em linhas de código no **painel Editor.**

Com o depurador, você passa pelo código enquanto observa as expressões JavaScript especificadas.  Assista e altere manualmente os valores de variável e mostre automaticamente quais variáveis estão no escopo da instrução atual.

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="O painel Depurador da ferramenta Sources  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   O **painel Depurador** da **ferramenta Sources**  
:::image-end:::  

O depurador dá suporte a ações padrão de depuração, como:  

*   Definindo pontos de interrupção, para pausar código.  
*   Passando pelo código.  
*   Exibindo e editando propriedades e variáveis.  
*   Observando os valores das expressões JavaScript.  
*   Exibindo a pilha de chamadas\ (a sequência de chamadas de função até o momento\).  
    
O depurador no DevTools foi projetado para parecer, parecer e trabalhar como o [depurador][VisualStudioCodeDocsEditorDebugging] no Visual Studio Code e o [depurador em Visual Studio][VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].

As subseções a seguir abrangem a depuração:  

*   [A abordagem básica para usar um depurador](#the-basic-approach-to-using-a-debugger)  
*   [Vantagens do Watch and Scope do depurador sobre console.log](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)  
*   [Depurar do Visual Studio Code diretamente](#debug-from-visual-studio-code-directly)  
*   [Artigos sobre depuração](#articles-about-debugging)  
    
### <a name="the-basic-approach-to-using-a-debugger"></a>A abordagem básica para usar um depurador

Para solucionar problemas de código JavaScript, você pode inserir `console.log()` instruções no **painel Editor.**  Outra abordagem mais poderosa é usar o depurador de Microsoft Edge DevTools.  O uso de um depurador pode ser mais simples do que , depois que você estiver familiarizado com a `console.log()` abordagem do depurador.

Para usar um depurador em uma página da Web, você normalmente definirá um ponto de interrupção e enviará um formulário da página da Web, da seguinte maneira:

1.  Abra a página da Web em uma nova guia do navegador.  Por exemplo, abra essa página da Web de formulário em uma nova guia: [Demonstração: Introdução Depuração javaScript com Microsoft Edge (Chromium) DevTools][GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted].  
1.  Selecione `F12` para abrir a janela **DevTools** e selecione a **guia Fontes.**  
1.  No painel **Navegador** \(à esquerda\), **** selecione a guia Página e selecione o arquivo JavaScript, como `get-started.js` .  
1.  No painel **Editor,** selecione um número de linha perto de uma linha de código suspeita para definir um ponto de interrupção nessa linha.  Na figura abaixo, um ponto de interrupção é definido na linha `var sum = addend1 + addend2;` .  
1.  Na página da Web, insira valores e envie o formulário.  Por exemplo, insira números, como e , em seguida, selecione o `5` botão Adicionar Número `1` **1 e Número 2**.  
    
    O depurador executa o código JavaScript e pausa no ponto de interrupção.  O depurador agora está no modo Pausado, para que você possa inspecionar os valores das propriedades que estão no escopo e passar pelo código.  
    
    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Inserindo o modo pausado do depurador" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        Inserindo o modo pausado do depurador  
    :::image-end:::  
    
    Na figura acima, adicionamos as expressões watch e , e pisou `sum` duas linhas além do ponto de `typeof sum` interrupção.  
    
1.  Examine os valores no painel **Escopo,** que mostra todas as variáveis ou propriedades que estão no escopo do ponto de interrupção atual e seus valores.  Ou adicione expressões no painel **de** relógio.  Essas expressões são as mesmas expressões que você escreveria em uma `console.log` instrução para depurar seu código.  Para executar comandos JavaScript para manipular dados no contexto atual, use **o Console**.  Para abrir o console, selecione `Esc` .  
1.  Passo a passo pelo código usando os controles na parte superior do painel **Depurador,** como **Etapa** \( `F9` \).
    
#### <a name="see-also"></a>Ver também

*   [Introdução à depuração][DevtoolsGuideChromiumJavascriptIndex] do JavaScript - um tutorial usando uma página da Web existente e simples que contém alguns controles de formulário.
    
### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a>Vantagens do Depurador\'s Watch and Scope sobre console\.log  

Essas três abordagens são equivalentes:

*   Adicionando temporariamente `console.log(sum)` as instruções e no `console.log(typeof sum)` código, onde está no `sum` escopo.  
*   Emitando as instruções e no painel Console do `sum` `console.log(typeof sum)` **** DevTools, quando o depurador é pausado onde `sum` está no escopo.  
*   Definindo **as expressões** do `sum` Relógio e no painel `typeof sum` **Depurador.**  
    
Quando a variável está no escopo, e seu valor é mostrado automaticamente na seção Escopo do `sum` `sum` painel **Depurador,** **** e também são sobreposição no painel Editor onde é `sum` calculado.  Portanto, você provavelmente não precisaria definir uma expressão watch para `sum` .

O depurador oferece uma exibição mais rica e flexível e um ambiente do que uma `console.log` instrução.  Por exemplo, no depurador, conforme você passa pelo código, você pode exibir e alterar os valores de todas as propriedades e variáveis definidas no momento.  Você também pode emitir instruções JavaScript no **Console**, como para alterar valores em uma matriz que está no escopo.  \(Para exibir o Console, selecione **Esc**.\)

As expressões Breakpoints e Watch são preservadas quando você atualize a página da Web.

### <a name="debug-from-visual-studio-code-directly"></a>Depurar do Visual Studio Code diretamente

Para usar o depurador mais completo do Visual Studio Code em vez do depurador DevTools, use o Microsoft Edge Ferramentas para extensão **VS Code** para Visual Studio Code.

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="As Microsoft Edge ferramentas para VS Code de Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   O **Microsoft Edge ferramentas para VS Code** de Visual Studio Code  
:::image-end:::  

Essa extensão fornece acesso **** às ferramentas **Elementos** e Rede do Microsoft Edge DevTools, de dentro Microsoft Visual Studio Code.  

Para obter mais informações, [consulte Visual Studio Code visão][VisualStudioCodeIndex] geral e a página GitHub Readme, Microsoft Edge Ferramentas de Desenvolvedor para [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].

### <a name="articles-about-debugging"></a>Artigos sobre depuração

Os artigos a seguir abrangem o painel **de depurador** e pontos de interrupção:

*   [Introdução à depuração do JavaScript no Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - Um tutorial \(com capturas de tela\), usando um projeto simples e existente.  
*   Use os recursos [de depurador][DevToolsJavaScriptReference] - Como usar o depurador para definir pontos de interrupção, passar pelo código, exibir e modificar valores variáveis, assistir expressões JavaScript e exibir a pilha de chamada.  
*   [Pause seu código com pontos de][DevToolsJavaScriptBreakpoints] interrupção - Como definir pontos de interrupção básicos e especializados no depurador.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools para iniciantes: Começar a trabalhar em CSS | Microsoft Docs"  
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools para iniciantes: começar com HTML e o dom | Microsoft Docs"  
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Executar comandos com o Menu de Comandos do Microsoft Edge DevTools | Microsoft Docs"   
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Gaveta - Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Alterar Microsoft Edge posicionamento do DevTools (Desfazer, Doca para baixo, Doca para a esquerda) | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Começar a depurar JavaScript no Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Execute trechos de código do JavaScript em qualquer página da Web com Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar arquivos com espaços de trabalho | Microsoft Docs"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos de fonte CSS e configurações no painel Estilos | Microsoft Docs"  
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Pause seu código com pontos de interrupção | Microsoft Docs"  
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Marcar scripts de conteúdo como código biblioteca | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Substituir recursos de página da Web por cópias locais usando Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Use os recursos de depurador | Microsoft Docs"  
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformata um arquivo JavaScript minificado com impressão bastante impressa - Use os recursos de depurador | Microsoft Docs"  
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Mapear código pré-processador para código-fonte | Microsoft Docs"  
[VisualStudioCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code visão geral | Microsoft Docs"  
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Criar um tutorial de extensão Parte 2 | Microsoft Docs"  

[VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Navegue pelo código com o Visual Studio depurador | Microsoft Docs"  

[VisualStudioCodeDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Depuração | Visual Studio Code"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Ferramentas de desenvolvedor para Visual Studio Code | GitHub"  

[GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demonstração: Introdução Depuração javaScript com Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[WhatwgHtmlSpecMulitpageOriginHtmlOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origem | HTML Standard"  

[MdnAddOnsWebextensionsContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de conteúdo | MDN"  

[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Quadros | W3C"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/sources) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

<!--todo: needs an accessibility review to replace "view", "see", and "look" with "display", exception is "see also" headings -->  

<!--todo: need a consistency review to replace all UI interactions with "choose" and all keyboard interactions with "select" -->  
