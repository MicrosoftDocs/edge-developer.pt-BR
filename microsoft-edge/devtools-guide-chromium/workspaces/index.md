---
title: Editar arquivos com espaços de trabalho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601843"
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







# Editar arquivos com espaços de trabalho   



> [!NOTE]
> O objetivo deste tutorial é fornecer uma prática prática para configurar e usar espaços de trabalho, para que você possa usar os espaços de trabalho em seus próprios projetos.  Você pode salvar as alterações no código-fonte em seu computador local, que você fez no DevTools depois de habilitar os espaços de trabalho.  

> [!CAUTION]
> **Pré-requisitos**: antes de iniciar este tutorial, você deve saber como:  
> *   [Usar HTML, CSS e JavaScript para criar uma página da Web][MDNWebGettingStarted]  
> *   [Usar o DevTools para fazer alterações básicas em CSS][DevToolsCssIndex]  
> *   [Executar um servidor Web HTTP local][MDNSimpleLocalHTTPServer]  

## Visão geral   

Os espaços de trabalho permitem salvar uma alteração feita no devtools em uma cópia local do mesmo arquivo em seu computador.  Por exemplo, suponha que:  

*   Você tem o código-fonte do seu site na área de trabalho.  
*   Você está executando um servidor Web local do diretório de código-fonte, para que o site possa ser acessado em `localhost:8080` .  
*   Você abriu `localhost:8080` no Microsoft Edge e está usando o devtools para alterar a CSS do site.  

Com os espaços de trabalho habilitados, as alterações de CSS feitas em DevTools são salvas no código-fonte na área de trabalho.  

## Limitações   

Se você estiver usando uma estrutura moderna, ele provavelmente transforma o código-fonte de um formato fácil de manter em um formato otimizado para ser executado o mais rápido possível.  
Em geral, os espaços de trabalho são capazes de mapear o código otimizado de volta ao código-fonte original com a ajuda dos [mapas de origem][TreehouseBlogSourceMaps].  Mas há uma grande quantidade de variações entre estruturas sobre como elas usam mapas de origem.  Devtools simplesmente dá suporte a todas as variações.  

Não se sabe que os espaços de trabalho não funcionam com esses frameworks:  

*   Criar aplicativo reagir  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## Recurso relacionado: substituições locais   

**Substituições locais** é outro recurso de devtools semelhante a espaços de trabalho.  Use substituições locais quando você deseja experimentar alterações em uma página, e você precisa ver essas alterações nas cargas da página, mas não importa o mapeamento das alterações para o código-fonte da página.  

<!--Todo: add section when content is ready  -->  

## Etapa 1: configurar   

Preencha este tutorial para obter experiência prática com espaços de trabalho.  

### Configurar a demonstração   

1.  [Abra a demonstração][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### Figura 1  
    > Um projeto de falha em ![ um projeto de falha][ImageGlitchProject]  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  Crie um `app` diretório na área de trabalho.  Salvar cópias dos arquivos no `workspaces-demo` diretório.  Para o restante deste tutorial, este diretório é conhecido como `~/Desktop/app` .  
1.  Inicie um servidor Web local `~/Desktop/app` .  Veja a seguir um exemplo de código para inicialização `SimpleHTTPServer` , mas você pode usar qualquer servidor de sua preferência.  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  Abra uma guia no Microsoft Edge e vá para a versão hospedada localmente do site.  Você deve ser capaz de acessá-lo usando uma URL como `localhost:8080` ou `http://0.0.0.0:8080` .  O [número de porta][WikiPortURLs] exato pode ser diferente.  
    
    > ##### Figura 2  
    > A demonstração  
    > ! [A demonstração] [ImageDemo]  

### Configurar o DevTools   

1.  Pressione `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o painel do **console** do devtools.  
    
    > ##### Figura 3  
    > Painel do **console**  
    > ! [O painel do console] [ImageConsolePanel]  

1.  Clique na guia **fontes** .  
1.  Clique na guia **FileSystem** .  
    
    > ##### Figura 4  
    > A guia **sistema de arquivos**  
    > ! [Guia sistema de arquivos] [ImageFilesystem]  

1.  Clique em **Adicionar pasta ao espaço de trabalho**.  
1.  Selecione `~/Desktop/app` .  
1.  Clique em **permitir** para conceder ao devtools permissão para ler e gravar no diretório.  
    Na guia **sistema de sistema** , agora há um ponto verde ao lado de `index.html` , `script.js` e `styles.css` .  Esses pontos verdes significam que o DevTools estabeleceu um mapeamento entre os recursos de rede da página e os arquivos `~/Desktop/app` .  
    
    > ##### Figura 5  
    > A guia **sistema de arquivos** agora mostra um mapeamento entre os arquivos locais e os de rede  
    > ! [A guia sistema de arquivos agora mostra um mapeamento entre os arquivos locais e os de rede] [ImageMapping]  

## Etapa 2: salvar uma alteração de CSS em disco   

1.  Abrir `styles.css` .  
    
    > [!NOTE]
    >A `color` propriedade dos `h1` elementos é definida como `fuchsia` .
    
    > ##### Figura 6  
    > Exibir `styles.css` em um editor de texto  
    > ! [Exibindo estilos. CSS em um editor de texto] [ImageStylesFuchsia]  


1.  Clique na guia **elementos** .  
1.  Altere o valor da `color` Propriedade do `<h1>` elemento para sua cor favorita.  
    Lembre-se de que você precisa clicar no `<h1>` elemento na **árvore DOM** para ver as regras CSS aplicadas a ele no painel **estilos** .  O ponto verde ao lado de `styles.css:1` significa que qualquer alteração feita está mapeada `~/Desktop/app/styles.css` .  
    
    > ##### Figura 7  
    > O indicador verde para o qual o arquivo está vinculado  
    > ! [O indicador verde no qual o arquivo está vinculado] [ImageStylesGreen]  

1.  Abra `styles.css` em um editor de texto novamente.  A `color` Propriedade agora está definida como sua cor favorita.  
1.  Recarregar a página.  A cor do `<h1>` elemento ainda está definida para sua cor favorita.  Isso funciona porque quando você fez a alteração, o DevTools salvou a alteração em disco.  Depois, quando você recarregar a página, o servidor local atuou na cópia modificada do disco.  

## Etapa 3: salvar uma alteração de HTML em disco   

### Alterar o HTML do painel elementos  

Você pode fazer alterações no HTML a partir do painel de elementos, mas as alterações na árvore DOM não são salvas em disco e só afetam a sessão atual do navegador.  
A árvore DOM não é HTML.  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### Alterar o HTML no painel fontes   

Se você quiser salvar uma alteração no HTML da página, use o painel **fontes** .  

1.  Clique na guia **fontes** .  
1.  Clique na guia **página** .  
1.  Clique em **(índice)**.  O HTML da página é aberto.  
1.  Substituir `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .  Veja a [Figura 8](#figure-8).  
1.  Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.  
1.  Recarregar a página.  O `<h1>` elemento ainda está exibindo o novo texto.  
    
    > ##### Figura 8  
    > A linha 12 foi definida como `I ❤️  Cake`  
    > ! [Alterando HTML no painel fontes] [ImageSourcesCakeHTML]  

1.  Abrir `~/Desktop/app/index.html` .  O `<h1>` elemento contém o novo texto.  

## Etapa 4: salvar uma alteração de JavaScript em disco   

O painel **fontes** também é o local para fazer alterações em JavaScript.  Mas, às vezes, você precisa acessar outros painéis, como o painel **elementos** ou o painel do **console** , ao fazer alterações em seu site.  Há uma maneira de ter o painel **fontes** aberto junto com outros painéis.  

1.  Clique na guia **elementos** .  
1.  Pressione `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).  O **menu de comando** é aberto.  
1.  Digite `QS` e selecione **Mostrar fonte rápida**.  Na parte inferior da janela do DevTools, agora há uma guia **fonte rápida** .  A guia exibe o conteúdo de `index.html` , que é o último arquivo editado no painel **fontes** .  A guia **fonte rápida** oferece o editor do painel **fontes** , para que você possa editar arquivos enquanto tiver outros painéis abertos.  
    
    > ##### Figura 9  
    > Abrir a guia **fonte rápida** usando o **menu de comandos**  
    > ! [Abrindo a guia fonte rápida usando o menu de comando] [ImageCommandMenuQuickSource]  

1.  Pressione `Control` + `P` \ (Windows \) ou `Command` + `P` \ (MacOS \) para abrir a caixa de diálogo **Abrir arquivo** .  Veja a [Figura 10](#figure-10).  
1.  Digite `script` e, em seguida, selecione **app/script. js**.  
    
    > ##### Figura 10  
    > Abrindo `script.js` usando a caixa de diálogo **Abrir arquivo**  
    > ! [Abrindo script. js usando a caixa de diálogo abrir arquivo] [ImageOpenFileDialog]  
    
    > [!NOTE]
    > O `Save Changes To Disk With Workspaces` link na demonstração tem o estilo regular.  
    
1.  Adicione o código a seguir na parte inferior do **script. js** usando a guia **fonte rápida** .  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Pressione `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.  
1.  Recarregar a página.  
    
    > [!NOTE]
    > O link na página agora está em itálico.
    
    > ##### Figura 11  
    > O link na página agora está em itálico  
    > ! [O link na página agora está em itálico] [ImageScriptItalic]  

## Próximas etapas   

Use o que você aprendeu neste tutorial para configurar espaços de trabalho em seu próprio projeto.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Figura 1: um projeto de falha com um nome gerado aleatoriamente"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo.msft.png "Figura 2: a demonstração"  
[ImageConsolePanel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-console.msft.png "Figura 3: o painel do console"  
[ImageFilesystem]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-FileSystem.msft.png "Figura 4: a guia Filesystem"  
[ImageMapping]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-FileSystem-Folder.msft.png "Figura 5: a guia Filesystem agora mostra um mapeamento entre os arquivos locais e os de rede"  
[ImageStylesFuchsia]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-FileSystem-CSS.msft.png "Figura 6: exibindo estilos. CSS em um editor de texto"  
[ImageStylesGreen]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Elements-Styles-CSS.msft.png "Figura 7: o indicador verde no qual o arquivo está vinculado"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-sources-Page-H1.msft.png "Figura 8: alterando o HTML no painel fontes"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Search-show-Quick-Source.msft.png "Figura 9: abrindo a guia fonte rápida usando o menu de comando"  
[ImageOpenFileDialog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Search-script.msft.png "Figura 10: abrindo script. js usando a caixa de diálogo abrir arquivo"  
[ImageScriptItalic]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo-Elements-Styles-Quick-Source-script.msft.png "Figura 11: o link na página agora está em itálico"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introdução à exibição e alteração de CSS"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Arquivos de demonstração de espaços de trabalho | Problema"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Conteúdo-CSS: folhas de estilos em cascata | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Introdução à Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Executar um servidor HTTP local simples | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução a APIs do DOM-Web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Uma introdução aos mapas de origem | Blog Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Porta \ (rede de computador \)-Wikipédia"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
