---
description: Comece a usar HTML e o DOM
title: 'DevTools para iniciantes: introdução ao HTML e ao DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: 182885cb97dbd1672d33b257569b0d841466985b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993279"
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

Você aprenderá a desenvolver na Web Criando seu próprio website.  Quando você concluir todos os tutoriais da série *devtools para iniciantes* , o seu site final será exibido na figura a seguir.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-finished.msft.png":::
   O site concluído  
:::image-end:::  

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

Você vai compilar seu site em um editor de código online chamado falha.  

1.  Abra o [código-fonte][GlitchAlluringShockIndex].  Esta guia será chamada de **guia Editor** ao longo deste tutorial.  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="A guia Editor" lightbox="../media/beginners-html-setup1.msft.png":::
       A guia Editor  
    :::image-end:::  
    
1.  Clique em **alluring-choque**.  O menu opções do projeto é aberto no canto superior esquerdo.  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="O menu opções do Project" lightbox="../media/beginners-html-setup2.msft.png":::
       O menu opções do Project  
    :::image-end:::  
    
1.  Clique em **remix projeto**.  Falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.  O conteúdo é o mesmo que antes.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="O projeto remisturado" lightbox="../media/beginners-html-setup3.msft.png":::
       O projeto remisturado  
    :::image-end:::  
    
1.  Se você planeja concluir o próximo tutorial desta série, clique em **entrar** e entre em falha com sua conta do GitHub ou do Facebook.  Se você não se conectar, perderá a capacidade de editar esse projeto depois de fechar a guia Editar.  
1.  Clique em **Mostrar** e selecione **em uma nova janela**.  Uma nova guia é aberta, mostrando a página ao vivo.  Esta guia será chamada de **guia ao vivo** durante este tutorial.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-html-setup4.msft.png":::
       A guia ao vivo  
    :::image-end:::  
    
## Adicionar conteúdo   

Seu site está muito vazio.  Siga as etapas abaixo para adicionar conteúdo a ele!  

1.  Na **guia Editor**, substituir `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="O novo código é realçado na guia Editor" lightbox="../media/beginners-html-add1.msft.png":::
             O novo código é realçado na guia Editor  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Exiba suas alterações na **guia ao vivo**.  O texto `About Me` está visível na página.  É maior do que o restante do texto, porque o `<h1>` elemento representa um título de seção.  O navegador da Web automaticamente dimensiona títulos em tamanhos de fonte maiores.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="O novo título fica visível na guia ao vivo" lightbox="../media/beginners-html-add2.msft.png":::
       O novo título fica visível na guia ao vivo  
    :::image-end:::  
    
1.  De volta à **guia Editor**, insira `<p>I am learning HTML.  Recent accomplishments:</p>` na linha abaixo de onde você acabou de colocar `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="O novo código é realçado na guia Editor" lightbox="../media/beginners-html-add3.msft.png":::
             O novo código é realçado na guia Editor  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Exiba sua alteração na **guia ao vivo**.  
1.  De volta à **guia Editor**, adicione uma lista das suas conquistas:  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="O novo código é realçado na guia Editor" lightbox="../media/beginners-html-add4.msft.png":::
             O novo código é realçado na guia Editor  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Novamente, volte para a **guia ao vivo** para garantir que o novo conteúdo seja exibido corretamente.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="A nova lista fica visível na guia ao vivo" lightbox="../media/beginners-html-add5.msft.png":::
       A nova lista fica visível na guia ao vivo  
    :::image-end:::  
    
## Experimentar alterações de conteúdo no Microsoft Edge DevTools   

Se você estivesse desenvolvendo uma página grande com grande parte do HTML, pode imaginar que pode ser um pouco cansativo para voltar e avançar entre a guia Editor e a guia ao vivo centenas de vezes para ver suas alterações, especialmente se você não tiver certeza sobre o que deve ser colocado na página.  O Microsoft Edge DevTools pode ajudá-lo a experimentar alterações de conteúdo sem precisar sair da guia ao vivo.  

### Saiba a diferença entre HTML e DOM   

Antes de começar a editar seu conteúdo do Microsoft Edge DevTools, é útil compreender a diferença entre HTML e DOM.  A melhor maneira de aprender é por exemplo:  

1.  Ir para a **guia ao vivo**.  Na parte inferior da página, você vê o texto `A new element!?!` .  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Na parte inferior da página, o novo elemento texto um novo!?! pode ser vista" lightbox="../media/beginners-html-dom1.msft.png":::
       Na parte inferior da página, o novo elemento texto um novo!?! pode ser vista  
    :::image-end:::  
    
1.  Volte para a **guia Editor** e tente localizar esse texto `index.html` .  Não está lá!  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="O texto mistério um novo elemento!?! está em qualquer lugar para ser encontrado no index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       O texto mistério `A new element!?!` não está disponível em qualquer lugar do `index.html`  
    :::image-end:::  
    
1.  Volte para a **guia ao vivo**, clique com o botão direito do mouse `A new element!?!` e selecione **inspecionar**.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspecionar texto" lightbox="../media/beginners-html-dom3.msft.png":::
       Inspecionar texto  
    :::image-end:::  
    
    O DevTools é aberto juntamente com sua página.  `<div>A new element!?!</div>` é realçado azul.  Embora essa estrutura em DevTools se pareça com o HTML, ela é na verdade a **árvore DOM**.  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="O DevTools está aberto junto com a página" lightbox="../media/beginners-html-dom4.msft.png":::
       O DevTools está aberto junto com a página  
    :::image-end:::  
    
Quando a página é carregada, o navegador leva o HTML para criar o conteúdo *inicial* da página.  O DOM representa o conteúdo *atual* da página, que pode mudar ao longo do tempo.  O `<div>A new element!?!</div>` conteúdo misterioso é adicionado à sua página devido à `<script src="new.js"></script>` marca na parte inferior da sua HTML.  Essa marca faz com que algum código JavaScript seja executado.  Você aprenderá mais sobre JavaScript em um tutorial posterior, mas, por ora, pense nisso como uma linguagem de programação que pode alterar o conteúdo da sua página.  Nesse caso específico, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.  É por isso que esse texto mistério fica visível na sua página ao vivo, mas não no HTML.  

### Editar o DOM   

Se você quiser experimentar rapidamente as alterações de conteúdo sem precisar sair da guia ao vivo, tente DevTools.  

1.  No DevTools, clique com o botão direito do mouse `Your site!` e selecione **Editar como HTML**.  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Editando o nó como HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       Editando o nó como HTML  
    :::image-end:::  
    
1.  Substituir `<p>Your site!</p>` pelo código abaixo.  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Editando o nó como HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             Editando o nó como HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Pressione `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \) para salvar suas alterações ou clique fora da caixa.  Suas alterações aparecem automaticamente na exibição ao vivo da página.  O texto foi `Your site!` substituído pelo novo conteúdo.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="O novo conteúdo aparece imediatamente na página" lightbox="../media/beginners-html-edit3.msft.png":::
       O novo conteúdo aparece imediatamente na página  
    :::image-end:::  
    
Esse fluxo de trabalho é bom para experimentar alterações de conteúdo.  Se você recarregar a página ou fechar a guia, suas alterações serão feitas para sempre.  Se você estiver usando este fluxo de trabalho e quiser salvar suas alterações, será necessário copiar manualmente essas alterações para o HTML.  As próximas seções mostram algumas outras maneiras de alterar o conteúdo da árvore DOM.  

## Reordenar nós   

Você também pode alterar a ordem dos nós DOM.  Por exemplo, em sua página da Web, o menu de navegação fica próximo à parte inferior.  Para movê-la para a parte superior:  

1.  Localize o `<nav>` nó na **árvore DOM** do devtools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="O nó de navegação é em azul realçado no DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       O nó de navegação é em azul realçado no DevTools  
    :::image-end:::  
    
1.  Arraste o `<nav>` nó para a parte superior, para que seja o primeiro filho abaixo do `<body>` nó.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Arrastando o nó de navegação para a parte superior" lightbox="../media/beginners-html-reorder2.msft.png":::
             Arrastando o nó de navegação para a parte superior  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          O `<nav>` nó agora está sendo exibido na parte superior da página.  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="O nó de navegação está na parte superior da página" lightbox="../media/beginners-html-reorder3.msft.png":::
             O nó de navegação está na parte superior da página  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### Excluir um nó   

Você também pode remover nós da árvore DOM.  

1.  Na **árvore DOM**, clique em `<div>A new element!?!</div>` .  DevTools realça o nó em azul.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Selecionando o nó a ser excluído" lightbox="../media/beginners-html-delete1.msft.png":::
       Selecionando o nó a ser excluído  
    :::image-end:::  
    
1.  Pressione a `Delete` tecla no teclado.  O `<div>A new element!?!</div>` nó é removido da sua árvore DOM.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="O nó foi excluído" lightbox="../media/beginners-html-delete2.msft.png":::
       O nó foi excluído  
    :::image-end:::  
    
## Copiar as alterações   

Você está quase pronto.  Você fez algumas alterações na sua página no DevTools, mas elas ainda não foram salvas em seu código-fonte.  

1.  Atualize a **guia ao vivo**.  As alterações feitas na árvore DOM desaparecem.  Em particular, o texto `Your site!` retorna à parte superior da página, e o texto `A new element!?!` retorna para a parte inferior.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="As alterações feitas desapareceram" lightbox="../media/beginners-html-copy1.msft.png":::
       As alterações feitas desapareceram  
    :::image-end:::  
    
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
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Como o arquivo index.html deve ser exibido" lightbox="../media/beginners-html-copy2.msft.png":::
       Qual `index.html` deve ser a aparência de seu arquivo  
    :::image-end:::  
    
## Próximas etapas   

*   Conclua o próximo tutorial desta série, comece a [usar o CSS][DevToolsBeginnersCss]para aprender a estilizar sua página e experimentar alterações de estilo no Microsoft Edge devtools.  
*   Leia [introdução ao dom][MDNIntroductionDom] para saber mais sobre o dom.  
*   Dê uma olhada em um curso como [introdução ao desenvolvimento na Web][CourseraIntroductionToWebDevelopment] para obter uma experiência de desenvolvimento da Web mais prática.  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para iniciantes: introdução ao CSS | Documentos da Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento na Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring-choques | Problema"  

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
