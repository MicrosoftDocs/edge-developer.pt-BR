---
description: Saiba como salvar alterações feitas dentro de DevTools em disco.
title: Editar arquivos com espaços de trabalho
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 496bbbb34cdf900d36aa7ebfbf79ad63cdf3e6e7
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125346"
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

> [!IMPORTANT]
> **Pré-requisitos**: antes de iniciar este tutorial, você deve saber como executar as seguintes ações.  
> 
> *   [Usar HTML, CSS e JavaScript para criar uma página da Web][MDNWebGettingStarted]  
> *   [Usar o DevTools para fazer alterações básicas em CSS][DevToolsCssIndex]  
> *   [Executar um servidor Web HTTP local][MDNSimpleLocalHTTPServer]  

## Visão geral  

Os espaços de trabalho permitem salvar uma alteração feita no devtools em uma cópia local do mesmo arquivo em seu computador.  Para este tutorial, você deve ter as seguintes configurações em seu computador.  

*   Você tem o código-fonte do seu site na área de trabalho.  
*   Você está executando um servidor Web local do diretório de código-fonte, para que o site possa ser acessado em `localhost:8080` .  
*   Você abriu `localhost:8080` no Microsoft Edge e está usando o devtools para alterar a CSS do site.  

Com os espaços de trabalho habilitados, as alterações de CSS feitas em DevTools são salvas no código-fonte na área de trabalho.  

## Limitações  

Se você estiver usando uma estrutura moderna, ele provavelmente transforma o código-fonte de um formato fácil de manter em um formato otimizado para ser executado o mais rápido possível.  

Em geral, os espaços de trabalho são capazes de mapear o código otimizado de volta ao código-fonte original com a ajuda dos [mapas de origem][TreehouseBlogSourceMaps].  Mas há uma grande quantidade de variações entre estruturas sobre como cada uma usa mapas de origem.  Devtools simplesmente dá suporte a todas as variações.  

Os espaços de trabalho são conhecidos por não trabalhar com a estrutura a seguir.  

*   Criar aplicativo reagir  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## Recurso relacionado: substituições locais  

**Substituições locais** é outro recurso de devtools semelhante a espaços de trabalho.  Use substituições locais quando você deseja experimentar alterações em uma página e precisa ver as alterações nas cargas da página, mas não importa como mapear as alterações no código-fonte da página.  

<!--Todo: add section when content is ready  -->  

## Etapa 1: configurar  

Conclua as ações a seguir para obter experiência prática com espaços de trabalho.  

### Configurar a demonstração  

1.  [Abra a demonstração][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Um projeto de falha  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Crie um `app` diretório na área de trabalho.  Salve cópias dos arquivos do `workspaces-demo` diretório para o `app` diretório.  Para o restante do tutorial, o diretório é conhecido como `~/Desktop/app` .  
1.  Inicie um servidor Web local `~/Desktop/app` .  Veja a seguir um exemplo de código para inicialização `SimpleHTTPServer` , mas você pode usar qualquer servidor de sua preferência.  
    
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
    
1.  Abra uma guia no Microsoft Edge e vá para a versão hospedada localmente do site.  Você deve ser capaz de acessá-lo usando uma URL como `localhost:8080` ou `http://0.0.0.0:8080` .  O [número de porta][WikiPortURLs] exato pode ser diferente.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       A demonstração  
    :::image-end:::  
    
### Configurar o DevTools  

1.  Selecione `Control` + `Shift` + `J` \ (Windows, Linux \) ou `Command` + `Option` + `J` \ (MacOS \) para abrir o painel de **console** do devtools.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       Painel do **console**  
    :::image-end:::  
    
1.  Escolha a guia **fontes** .  
1.  Escolha a guia **sistema de arquivos** .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       A guia **sistema de arquivos**  
    :::image-end:::  
    
1.  Escolha **Adicionar pasta ao espaço de trabalho**.  
1.  Digite `~/Desktop/app`.  
1.  Escolha **permitir para que** o devtools Conceda permissão para ler e gravar no diretório.  
    Na guia **sistema de sistema** , agora há um ponto verde ao lado de `index.html` , `script.js` e `styles.css` .  Esses pontos verdes significam que o DevTools estabeleceu um mapeamento entre os recursos de rede da página e os arquivos `~/Desktop/app` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       A guia **sistema de arquivos** agora mostra um mapeamento entre os arquivos locais e os de rede  
    :::image-end:::  
    
## Etapa 2: salvar uma alteração de CSS em disco  

1.  Abrir `styles.css` .  
    
    > [!NOTE]
    > A `color` propriedade dos `h1` elementos é definida como `fuchsia` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Exibir `styles.css` em um editor de texto  
    :::image-end:::  
    
1.  Escolha a guia **elementos** .  
1.  Altere o valor da `color` Propriedade do `<h1>` elemento para sua cor favorita.  
    Lembre-se de que você precisa escolher o `<h1>` elemento na **árvore DOM** para ver as regras CSS aplicadas a ele no painel **estilos** .  O ponto verde ao lado de `styles.css:1` significa que qualquer alteração feita está mapeada `~/Desktop/app/styles.css` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       O indicador verde para o qual o arquivo está vinculado  
    :::image-end:::  
    
1.  Abra `styles.css` em um editor de texto novamente.  A `color` Propriedade agora está definida como sua cor favorita.  
1.  Atualize a página.  A cor do `<h1>` elemento ainda está definida para sua cor favorita.  A alteração permanece em uma atualização, porque quando você fez a alteração, o DevTools salvou a alteração em disco.  E, em seguida, ao atualizar a página, o servidor local atuou na cópia modificada do disco.  
    
## Etapa 3: salvar uma alteração de HTML em disco  

### Alterar o HTML do painel elementos  

Você pode fazer alterações no HTML a partir do painel de elementos, mas as alterações na árvore DOM não são salvas em disco e só afetam a sessão atual do navegador.  

A árvore DOM não é HTML.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** panel  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### Alterar o HTML no painel fontes  

Se você quiser salvar uma alteração no HTML da página, use o painel **fontes** .  

1.  Escolha a guia **fontes** .  
1.  Escolha a guia **página** .  
1.  Escolha **(índice)**.  O HTML da página é aberto.  
1.  Substituir `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .  Veja a figura a seguir.  
1.  Selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.  
1.  Atualize a página.  O `<h1>` elemento ainda está exibindo o novo texto.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Alterar o HTML no painel **fontes**  
    :::image-end:::  
    
1.  Abrir `~/Desktop/app/index.html` .  O `<h1>` elemento contém o novo texto.  
    
## Etapa 4: salvar uma alteração de JavaScript em disco  

O painel **fontes** também é o local para fazer alterações em JavaScript.  Mas, às vezes, você precisa acessar outros painéis, como o painel **elementos** ou o painel do **console** , ao fazer alterações em seu site.  Há uma maneira de ter o painel **fontes** aberto junto com outros painéis.  

1.  Escolha a guia **elementos** .  
1.  Selecione `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \).  O **menu de comando** é aberto.  
1.  Digite `QS` e escolha **Mostrar fonte rápida**.  Na parte inferior da janela do DevTools, agora há uma guia **fonte rápida** .  A guia exibe o conteúdo de `index.html` , que é o último arquivo editado no painel **fontes** .  A guia **fonte rápida** oferece o editor do painel **fontes** , para que você possa editar arquivos enquanto tiver outros painéis abertos.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Abrir a guia **fonte rápida** usando o **menu de comandos**  
    :::image-end:::  
    
1.  Selecione `Control` + `P` \ (Windows, Linux \) ou `Command` + `P` \ (MacOS \) para abrir a caixa de diálogo **Abrir arquivo** .  Veja a figura a seguir.  
1.  Digite `script` e escolha **app/script.js**.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       Abrir `script.js` usando a caixa de diálogo **Abrir arquivo**  
    :::image-end:::  
    
    > [!NOTE]
    > O `Save Changes To Disk With Workspaces` link na demonstração tem o estilo regular.  
    
1.  Adicione o código a seguir na parte inferior de **script.js** usando a guia **fonte rápida** .  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Selecione `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) para salvar a alteração.  
1.  Atualize a página.  
    
    > [!NOTE]
    > O link na página agora está em itálico.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Um projeto de falha" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       O link na página agora está em itálico  
    :::image-end:::  
    
## Próximas etapas  

Use o que você aprendeu neste tutorial para configurar espaços de trabalho em seu próprio projeto.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Introdução ao visualizar e alterar CSS | Documentos da Microsoft"  

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
