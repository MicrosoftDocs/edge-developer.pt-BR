---
description: Saiba como salvar as alterações feitas no DevTools no disco.
title: Editar arquivos com o Workspaces
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 640bb80e01f776c763af053cf8354ce90cf52e93
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564662"
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
# <a name="edit-files-with-workspaces"></a>Editar arquivos com o Workspaces  

Este tutorial fornece prática na configuração e no uso de um Espaço de Trabalho.  Depois de adicionar arquivos a um Espaço de Trabalho, as alterações feitas no código-fonte no DevTools são salvas no computador local e são preservadas após a atualização da página da Web.  

> [!IMPORTANT]
> **Pré-requisitos**: Antes de começar este tutorial, você deve saber como executar as seguintes ações.  
> 
> *   [Usar html, CSS e JavaScript para criar uma página da Web][MDNWebGettingStarted]  
> *   [Usar o DevTools para fazer alterações básicas no CSS][DevToolsCssIndex]  
> *   [Executar um servidor Web HTTP local][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a>Visão geral  

Os espaços de trabalho permitem salvar uma alteração que você faz no Devtools em uma cópia local do mesmo arquivo em seu computador.  Para este tutorial, você deve ter as seguintes configurações em seu computador.  

*   Você tem o código-fonte do seu site na área de trabalho.  
*   Você está executando um servidor Web local no diretório de código-fonte, para que o site seja acessível em `localhost:8080` .  
*   Você abriu `localhost:8080` no Microsoft Edge e está usando o DevTools para alterar o CSS do site.  

Com espaços de trabalho habilitados, as alterações CSS feitas no DevTools são salvas no código-fonte da área de trabalho.  

## <a name="limitations"></a>Limitações  

Se você estiver usando uma estrutura moderna, provavelmente transformará seu código-fonte de um formato fácil de manter em um formato otimizado para ser executado o mais rápido possível.  

Os espaços de trabalho geralmente são capazes de mapear o código otimizado de volta para o código-fonte original com a ajuda de mapas [de origem.][TreehouseBlogSourceMaps]  Mas há uma grande variação entre estruturas sobre como cada estrutura usa mapas de origem.  Os Devtools não suportam todas as variações.  

Os espaços de trabalho são conhecidos por não funcionarem com a estrutura a seguir.  

*   Criar React App  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a>Recurso relacionado: substituições locais  

**Substituições Locais** é outro recurso DevTools semelhante a Workspaces.  Use Substituições Locais quando quiser experimentar alterações em uma página da Web e você precisa exibir as alterações em cargas de página da Web, mas não se importa em mapear suas alterações no código-fonte da página da Web.  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a>Etapa 1: Configurar  

Conclua as seguintes ações, para obter experiência prática com Espaços de Trabalho.  

### <a name="set-up-the-demo"></a>Configurar a demonstração  

1.  [Abra a demonstração][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Um projeto Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Um projeto Glitch  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Crie um `app` diretório em sua área de trabalho.  Salve cópias dos arquivos do `workspaces-demo` diretório para o `app` diretório.  Para o restante do tutorial, o diretório é chamado de `~/Desktop/app` .  
1.  Inicie um servidor Web local em `~/Desktop/app` .  Abaixo está um código de exemplo para iniciar `SimpleHTTPServer` , mas você pode usar qualquer servidor que preferir.  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  Abra uma guia no Microsoft Edge e navegue até a versão hospedada localmente do site.  Você deve ser capaz de acessá-lo usando uma URL como `localhost:8080` ou `http://0.0.0.0:8080` .  O número [exato da porta][WikiPortURLs] pode ser diferente.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="A demonstração" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       A demonstração  
    :::image-end:::  
    
### <a name="set-up-devtools"></a>Configurar o DevTools  

1.  Selecione `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` + `Option` + `J` \(macOS\) para abrir o **painel console** do DevTools.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="O painel Console" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       O **painel Console**  
    :::image-end:::  
    
1.  Navegue até a **ferramenta Sources.**  
1.  No painel **Navegador** (à esquerda), escolha a **guia Sistema de** Arquivos.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="A guia Sistema de Arquivos" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       A **guia Sistema de** Arquivos  
    :::image-end:::  
    
1.  Escolha **Adicionar pasta ao espaço de trabalho**.  
1.  Digite `~/Desktop/app`.  
1.  Escolha **Permitir** para dar permissão ao DevTools para ler e gravar no diretório.  
    Na guia **Sistema de** Arquivos, um ponto verde agora aparece ao lado de , `index.html` e `script.js` `styles.css` .  Um ponto verde indica que o DevTools estabeleceu um mapeamento entre um recurso de rede da página e o arquivo em `~/Desktop/app` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="A guia Sistema de Arquivos agora indica um mapeamento entre os arquivos locais e os de rede" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       A **guia Sistema de** Arquivos agora indica um mapeamento entre os arquivos locais e os de rede  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a>Etapa 2: Salvar uma alteração CSS no disco  

1.  Abra `styles.css` .  
    
    > [!NOTE]
    > A `color` propriedade de elementos é definida como `h1` `fuchsia` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Exibir styles.css em um editor de texto" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Exibir `styles.css` em um editor de texto  
    :::image-end:::  
    
1.  Escolha a **ferramenta Elementos.**  
1.  Altere o valor `color` da propriedade do elemento para sua cor `<h1>` favorita.  
    Lembre-se de que você precisa escolher o elemento na Árvore DOM para exibir as regras CSS aplicadas a `<h1>` ele no painel **Estilos.** ****  O ponto verde ao lado `styles.css:1` significa que qualquer alteração que você fizer será mapeada para `~/Desktop/app/styles.css` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="O indicador verde que o arquivo está vinculado" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       O indicador verde que o arquivo está vinculado  
    :::image-end:::  
    
1.  Abra `styles.css` em um editor de texto novamente.  A `color` propriedade agora está definida como sua cor favorita.  
1.  Atualize a página.  A cor do `<h1>` elemento ainda está definida como sua cor favorita.  A alteração permanece em uma atualização, porque quando você fez a alteração DevTools salvou a alteração no disco.  E, quando você atualizeu a página, seu servidor local atendeu a cópia modificada do arquivo do disco.  
    
## <a name="step-3-save-an-html-change-to-disk"></a>Etapa 3: Salvar uma alteração HTML no disco  

### <a name="change-html-from-the-elements-panel"></a>Alterar HTML do Painel de Elementos  

Você pode fazer alterações no html do Painel de Elementos, mas suas alterações na árvore DOM não são salvas no disco e só efetivam a sessão atual do navegador.  

A árvore DOM não é html.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-tool"></a>Alterar HTML da ferramenta Sources  

Se você quiser salvar uma alteração no HTML da página da Web, use a **ferramenta Sources.**  

1.  Navegue até a **ferramenta Sources.**  
1.  No painel **Navegador** (à esquerda), escolha a **guia** Página.  
1.  Escolha **(índice)**.  O HTML da página é aberto.  
1.  Substitua `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .  Revise a figura a seguir.  
1.  Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.  
1.  Atualize a página.  O `<h1>` elemento continua a exibir o novo texto após a atualização da página.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Alterar HTML da ferramenta Sources" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Alterar HTML da ferramenta **Sources**  
    :::image-end:::  
    
1.  Abra `~/Desktop/app/index.html` .  O `<h1>` elemento contém o novo texto.  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a>Etapa 4: Salvar uma alteração do JavaScript no disco  

O principal local para usar o editor de código do DevTools é a **ferramenta Sources.**  Mas, às vezes, você precisa acessar outras ferramentas, como a **ferramenta Elements** ou o **painel console,** durante a edição de arquivos.  A **ferramenta De origem** Rápida fornece apenas o editor da ferramenta **Fontes,** enquanto qualquer ferramenta está aberta.  

Para abrir o editor de código do DevTools juntamente com outras ferramentas, faça o seguinte:  

1.  Navegue até **a ferramenta Elements.**  
1.  Selecione `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` ou \(macOS\).  O **Menu de Comando** é aberto.  
1.  Digite `Quick Source` e escolha Mostrar Fonte **Rápida**.  Na parte inferior da janela DevTools, a ferramenta **Fonte** Rápida é exibida, exibindo o conteúdo de , que é o último arquivo editado na `index.html` ferramenta **Fontes.**    
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Abra a ferramenta Fonte Rápida usando o Menu de Comando" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Abra a **ferramenta Fonte** Rápida usando o Menu **de Comando**  
    :::image-end:::  
    
1.  Selecione `Control` + `P` \(Windows, Linux\) `Command` + `P` ou \(macOS\) para abrir a **caixa de diálogo Abrir Arquivo.**  Revise a figura a seguir.  
1.  Digite `script` , escolha **aplicativo/script.js**.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Abra script.js usando a caixa de diálogo Abrir Arquivo" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       Abrir `script.js` usando a caixa de diálogo Abrir **Arquivo**  
    :::image-end:::  
    
    > [!NOTE]
    > O `Save Changes To Disk With Workspaces` link na demonstração é estilizado regularmente.  
    
1.  Adicione o código a seguir à parte inferior ** do **script.jsusando a ferramenta **De origem** rápida.  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Selecione `Control` + `S` \(Windows, Linux\) `Command` + `S` ou \(macOS\) para salvar a alteração.  
1.  Atualize a página.  
    
    > [!NOTE]
    > O link na página agora está itálico.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="O link na página agora está itálico" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       O link na página agora está itálico  
    :::image-end:::  
    
## <a name="next-steps"></a>Próximas etapas  

Use o que você aprendeu neste tutorial para configurar espaços de trabalho em seu próprio projeto.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Começar a exibir e alterar o CSS | Microsoft Docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Arquivos de demonstração de espaços de trabalho | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Conteúdo - CSS: Folhas de estilo em cascata | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Como começar com o web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Executando um servidor HTTP local simples | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM - APIs da Web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Uma introdução ao código-fonte Mapas | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Porta \(rede do computador\) - Wikipédia"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
