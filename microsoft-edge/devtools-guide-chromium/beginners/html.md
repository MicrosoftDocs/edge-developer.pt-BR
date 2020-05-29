---
title: DevTools para iniciantes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581584"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# DevTools para iniciantes: introdução ao HTML e ao DOM   

Esta é a primeira em uma série de tutoriais que ensinam noções básicas sobre o desenvolvimento na Web.  Você também aprenderá sobre um conjunto de ferramentas de desenvolvedor da Web, chamado Microsoft Edge DevTools, que podem aumentar sua produtividade.  

Neste tutorial específico, você aprenderá sobre HTML e DOM.  O HTML é uma das principais tecnologias de desenvolvimento na Web.  É o idioma que controla a estrutura e o conteúdo das páginas da Web.  O DOM também está relacionado à estrutura e ao conteúdo de páginas da Web, mas você aprenderá mais sobre isso mais tarde.  

## Goal   

Você aprenderá a desenvolver na Web Criando seu próprio website.  Quando você concluir todos os tutoriais da série *devtools para iniciantes* , o seu site final terá a aparência da **Figura 1**.  

> ##### Figura 1  
> O site concluído  
> ![O site concluído][ImageHtmlFinished]  

No final deste tutorial, você compreenderá:  

*   Como o HTML e o DOM criam o conteúdo que você vê nas páginas da Web.  
*   Como o Microsoft Edge DevTools pode ajudá-lo a experimentar alterações em HTML e DOM.  
*   A diferença entre HTML e DOM.  

Você também terá um site real!  Você pode usar este site para hospedar seu currículo ou blog.  

## Pré-requisitos   

Antes de tentar este tutorial, complete os seguintes pré-requisitos:  

*   Se você não estiver familiarizado com HTML, leia [introdução ao HTML][MDNGettingStartedHtml].  
*   Baixar o navegador da Web [Microsoft Edge][MicrosoftEdgeInsider] .  Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamado de Microsoft Edge DevTools, incorporado ao Microsoft Edge.  

## Configurar seu código   

Você vai criar seu site em um editor de código online chamado falha.  

1.  Abra o [código-fonte][GlitchAlluringShockIndex].  Esta guia será chamada de **guia Editor** ao longo deste tutorial.  
    > ##### Figura 2  
    > A guia Editor  
    > ![A guia Editor][ImageHtmlSetup1]  

1.  Clique em **alluring-choque**.  O menu opções do projeto é aberto no canto superior esquerdo.  
    
    > #### Figura 3  
    > O menu opções do Project  
    > ![O menu opções do Project][ImageHtmlSetup2]  
    
1.  Clique em **remix projeto**.  Falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.  O conteúdo é o mesmo que antes.  
    
    > ##### Figura 4  
    > O projeto remisturado  
    > ![O projeto remisturado][ImageHtmlSetup3]  
    
1.  Se você planeja concluir o próximo tutorial desta série, clique em **entrar** e entre em falha com sua conta do GitHub ou do Facebook.  Se você não se conectar, perderá a capacidade de editar esse projeto depois de fechar a guia Editar.  
1.  Clique em **Mostrar** e selecione **em uma nova janela**.  Uma nova guia é aberta, mostrando a página ao vivo.  Esta guia será chamada de **guia ao vivo** durante este tutorial.  
    
    > ##### Figura 5  
    > A guia ao vivo  
    > ![A guia ao vivo][ImageHtmlSetup4]  
    
## Adicionar conteúdo   

Seu site está muito vazio.  Siga as etapas abaixo para adicionar conteúdo a ele!  

1.  Na **guia Editor**, substituir `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### Figura 6  
    > O novo código é realçado na guia Editor  
    > ![O novo código é realçado na guia Editor][ImageHtmlAdd1]  
    
1.  Exiba suas alterações na **guia ao vivo**.  O texto `About Me` está visível na página.  É maior do que o restante do texto, porque o `<h1>` elemento representa um título de seção.  O navegador da Web automaticamente dimensiona títulos em tamanhos de fonte maiores.  
    
    > ##### Figura 7  
    > O novo título fica visível na guia ao vivo  
    > ![O novo título fica visível na guia ao vivo][ImageHtmlAdd2]  
    
1.  De volta à **guia Editor**, insira `<p>I am learning HTML.  Recent accomplishments:</p>` na linha abaixo de onde você acabou de colocar `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### Figura 8  
    > O novo código é realçado na guia Editor  
    > ![O novo código é realçado na guia Editor][ImageHtmlAdd3]  
    
1.  Exiba sua alteração na **guia ao vivo**.  
1.  De volta à **guia Editor**, adicione uma lista das suas conquistas:  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### Figura 9  
    > O novo código é realçado na guia Editor  
    > ![O novo código é realçado na guia Editor][ImageHtmlAdd4]  
    
1.  Novamente, volte para a **guia ao vivo** para garantir que o novo conteúdo seja exibido corretamente.  
    
    > ##### Figura 10  
    > A nova lista fica visível na guia ao vivo  
    > ![A nova lista fica visível na guia ao vivo][ImageHtmlAdd5]  
    
## Experimentar alterações de conteúdo no Microsoft Edge DevTools   

Se você estivesse desenvolvendo uma página grande com grande parte do HTML, pode imaginar que pode ser um pouco cansativo para voltar e avançar entre a guia Editor e a guia ao vivo centenas de vezes para ver suas alterações, especialmente se você não tiver certeza sobre o que deve ser colocado na página.  O Microsoft Edge DevTools pode ajudá-lo a experimentar alterações de conteúdo sem precisar sair da guia ao vivo.  

### Saiba a diferença entre HTML e DOM   

Antes de começar a editar seu conteúdo do Microsoft Edge DevTools, é útil compreender a diferença entre HTML e DOM.  A melhor maneira de aprender é por exemplo:  

1.  Ir para a **guia ao vivo**.  Na parte inferior da página, você vê o texto `A new element!?!` .  
    
    > ###### Figura 11  
    > Na parte inferior da página, o texto `A new element!?!` pode ser visto  
    > ![Na parte inferior da página, o novo elemento texto um novo!?! pode ser vista][ImageHtmlDom1]  
    
1.  Volte para a **guia Editor** e tente localizar esse texto `index.html` .  Não está lá!  
    
    > ##### Figura 12  
    > O texto mistério `A new element!?!` não está disponível em qualquer lugar do `index.html`  
    > ![O texto mistério um novo elemento!?! está em qualquer lugar para ser localizado em index. html][ImageHtmlDom2]  
    
1.  Volte para a **guia ao vivo**, clique com o botão direito do mouse `A new element!?!` e selecione **inspecionar**.  
    
    > ##### Figura 13  
    > Inspecionar texto  
    > ![Inspecionar texto][ImageHtmlDom3]  
    
    O DevTools é aberto juntamente com sua página.  `<div>A new element!?!</div>` é realçado azul.  Embora essa estrutura em DevTools se pareça com o HTML, ela é na verdade a **árvore DOM**.  
    
    > ##### Figura 14  
    > O DevTools está aberto junto com a página  
    > ![O DevTools está aberto junto com a página][ImageHtmlDom4]  
    
Quando a página é carregada, o navegador leva o HTML para criar o conteúdo *inicial* da página.  O DOM representa o conteúdo *atual* da página, que pode mudar ao longo do tempo.  O `<div>A new element!?!</div>` conteúdo misterioso é adicionado à sua página devido à `<script src="new.js"></script>` marca na parte inferior da sua HTML.  Essa marca faz com que algum código JavaScript seja executado.  Você aprenderá mais sobre JavaScript em um tutorial posterior, mas, por ora, pense nisso como uma linguagem de programação que pode alterar o conteúdo da sua página.  Nesse caso específico, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.  É por isso que esse texto mistério fica visível na sua página ao vivo, mas não no HTML.  

### Editar o DOM   

Se você quiser experimentar rapidamente as alterações de conteúdo sem precisar sair da guia ao vivo, tente DevTools.  

1.  No DevTools, clique com o botão direito do mouse `Your site!` e selecione **Editar como HTML**.  

    > ##### Figura 15  
    > Editando o nó como HTML  
    > ![Editando o nó como HTML][ImageHtmlEdit1]  
    
1.  Substituir `<p>Your site!</p>` pelo código abaixo.  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### Figura 16  
    > Editando o nó como HTML  
    > ![Editando o nó como HTML][ImageHtmlEdit2]  
    
1.  Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para salvar suas alterações ou clique fora da caixa.  Suas alterações aparecem automaticamente na exibição ao vivo da página.  O texto foi `Your site!` substituído pelo novo conteúdo.  
    
    > ##### Figura 17  
    > O novo conteúdo aparece imediatamente na página  
    > ![O novo conteúdo aparece imediatamente na página][ImageHtmlEdit3]  
    
Esse fluxo de trabalho é bom para experimentar alterações de conteúdo.  Se você recarregar a página ou fechar a guia, suas alterações serão feitas para sempre.  Se você estiver usando este fluxo de trabalho e quiser salvar suas alterações, será necessário copiar manualmente essas alterações para o HTML.  As próximas seções mostram algumas outras maneiras de alterar o conteúdo da árvore DOM.  

## Reordenar nós   

Você também pode alterar a ordem dos nós DOM.  Por exemplo, em sua página da Web, o menu de navegação fica próximo à parte inferior.  Para movê-la para a parte superior:  

1.  Localize o `<nav>` nó na **árvore DOM** do devtools.  
    
    > ##### Figura 18  
    > O nó de navegação é em azul realçado no DevTools  
    > ![O nó de navegação é em azul realçado no DevTools][ImageHtmlReorder1]  
    
1.  Arraste o `<nav>` nó para a parte superior, para que seja o primeiro filho abaixo do `<body>` nó.  
    > ##### Figura 19  
    > Arrastando o nó de navegação para a parte superior  
    > ![Arrastando o nó de navegação para a parte superior][ImageHtmlReorder2]  
    
    O `<nav>` nó agora está sendo exibido na parte superior da página.  
    
    > ##### Figura 20  
    > O nó de navegação está na parte superior da página  
    > ![O nó de navegação está na parte superior da página][ImageHtmlReorder3]  
    
### Excluir um nó   

Você também pode remover nós da árvore DOM.  

1.  Na **árvore DOM**, clique em `<div>A new element!?!</div>` .  DevTools realça o nó em azul.  
    
    > ##### Figura 21  
    > Selecionando o nó a ser excluído  
    > ![Selecionando o nó a ser excluído][ImageHtmlDelete1]  
    
1.  Pressione a `Delete` tecla no teclado.  O `<div>A new element!?!</div>` nó é removido da sua árvore DOM.  
    
    > ##### Figura 22  
    > O nó foi excluído  
    > ![O nó foi excluído][ImageHtmlDelete2]  
    
## Copiar as alterações   

Você está quase pronto.  Você fez algumas alterações na sua página no DevTools, mas elas ainda não foram salvas em seu código-fonte.  

1.  Atualize a **guia ao vivo**.  As alterações feitas na árvore DOM desaparecem.  Em particular, o texto `Your site!` retorna à parte superior da página, e o texto `A new element!?!` retorna para a parte inferior.  
    
    > ##### Figura 23  
    > As alterações feitas desapareceram  
    > ![As alterações feitas desapareceram][ImageHtmlCopy1]  

1.  Copie o código abaixo.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  Volte para a **guia Editor** e substitua o conteúdo do seu `index.html` arquivo pelo código que você acabou de copiar.  
    
    > ##### Figura 24  
    > Qual `index.html` deve ser a aparência de seu arquivo  
    > ![Como o arquivo index. html deve ser exibido][ImageHtmlCopy2]  
    
## Próximas etapas   

*   Conclua o próximo tutorial desta série, comece a [usar o CSS][DevToolsBeginnersCss]para aprender a estilizar sua página e experimentar alterações de estilo no Microsoft Edge devtools.  
*   Leia [introdução ao dom][MDNIntroductionDom] para saber mais sobre o dom.  
*   Dê uma olhada em um curso como [introdução ao desenvolvimento na Web][CourseraIntroductionToWebDevelopment] para obter uma experiência de desenvolvimento da Web mais prática.  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Figura 1: o site concluído"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Figura 2: a guia Editor"  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Figura 3: o menu de opções do Project"  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Figura 4: o projeto misturado"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Figura 5: a guia ao vivo"  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Figura 6: o novo código está realçado na guia Editor"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Figura 7: o novo título está visível na guia ao vivo"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Figura 8: o novo código está realçado na guia Editor"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Figura 9: o novo código está realçado na guia Editor"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Figura 10: a nova lista é visível na guia ao vivo"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Figura 11: na parte inferior da página o novo elemento texto um novo!?! pode ser vista"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Figura 12: o texto mistério um novo elemento!?! está em qualquer lugar para ser localizado em index. html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Figura 13: inspecionar algum texto"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Figura 14: o DevTools está aberto junto com a página"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Figura 15: editando o nó como HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Figura 16: editando o nó como HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Figura 17: o novo conteúdo aparece imediatamente na página"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Figura 18: o nó de navegação é em azul realçado no DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Figura 19: arrastando o nó de navegação até o início"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Figura 20: o nó de navegação está na parte superior da página"  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Figura 21: selecionando o nó a ser excluído"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Figura 22: o nó foi excluído"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Figura 23: as alterações feitas desapareceram"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Figura 24: como será a aparência do arquivo index. html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools para iniciantes: introdução ao CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento na Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. html-alluring-choque | Problema"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Introdução ao HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao DOM | MDN"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/html) e é criada pela [Katherine Jackson][KatherineJackson] \ (redatora técnica, Chrome devtools \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
