---
description: Introdução html e o DOM
title: 'DevTools para iniciantes: Começar com HTML e o DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564564"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools para iniciantes: Começar com HTML e o DOM  

Este é o primeiro de uma série de tutoriais que lhe ensinarão as noções básicas de desenvolvimento da Web.  Saiba mais sobre um conjunto de ferramentas de desenvolvedor da Web, chamada Microsoft Edge DevTools, que pode aumentar sua produtividade.  

Neste tutorial específico, você aprenderá sobre HTML e DOM.  HTML é uma das principais tecnologias de desenvolvimento da Web.  É o idioma que controla a estrutura e o conteúdo das páginas da Web.  O DOM também está relacionado à estrutura e ao conteúdo das páginas da Web, saiba mais sobre isso mais tarde.  

## <a name="goals"></a>Metas  

Você aprenderá o desenvolvimento da Web criando seu próprio site.  Quando você concluir todos os tutoriais na série **DevTools para Iniciantes,** o site concluído poderá ter a aparência da figura a seguir.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="O site concluído" lightbox="../media/beginners-html-finished.msft.png":::
   O site concluído  
:::image-end:::  

No final deste tutorial, você deve entender os tópicos a seguir.  

*   Como o HTML e o DOM criam o conteúdo exibido em páginas da Web.  
*   Como Microsoft Edge o DevTools pode ajudá-lo a experimentar alterações em HTML e DOM.  
*   A diferença entre HTML e DOM.  

Você também tem um site real.  Você pode usar o site para hospedar seu currículo ou blog.  

## <a name="prerequisites"></a>Pré-requisitos  

Antes de tentar este tutorial, conclua os seguintes pré-requisitos:  

*   Se você não estiver familiarizado com HTML, leia [Getting Started with HTML][MDNGettingStartedHtml].  
*   Baixe o [Microsoft Edge][MicrosoftEdgeInsider] da Web.  Este tutorial usa um conjunto de ferramentas de desenvolvimento da Web, chamada Microsoft Edge DevTools, que são Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurar seu código  

Você vai criar seu site em um editor de código online chamado Glitch.  

1.  Abra o [código-fonte][GlitchAlluringShockIndex].  Essa guia é chamada de **guia editor ao** longo deste tutorial.  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="A guia editor" lightbox="../media/beginners-html-setup1.msft.png":::
       A guia editor  
    :::image-end:::  
    
1.  Escolha **alluring-shock**.  O Project menu Opções é aberto no canto superior esquerdo.  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="O menu Project opções" lightbox="../media/beginners-html-setup2.msft.png":::
       O menu Project opções  
    :::image-end:::  
    
1.  Escolha **Mesclar Project**.  A falha cria uma cópia do projeto que você pode editar e gera aleatoriamente um novo nome para o projeto.  O conteúdo é o mesmo de antes.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="O projeto remixado" lightbox="../media/beginners-html-setup3.msft.png":::
       O projeto remixado  
    :::image-end:::  
    
1.  Se você planeja concluir o próximo tutorial **** desta série, escolha Entrar e entrar em Glitch com sua GitHub ou conta do Facebook.  Se você optar por não entrar em sua conta, perderá a capacidade de editar o projeto depois de fechar a guia de edição.  
1.  Escolha **Mostrar** e escolher **Em uma nova janela**.  Uma nova guia é aberta, mostrando a página ao vivo.  Essa guia é chamada de **guia ao vivo ao** longo deste tutorial.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="A guia ao vivo" lightbox="../media/beginners-html-setup4.msft.png":::
       A guia ao vivo  
    :::image-end:::  
    
## <a name="add-content"></a>Adicionar conteúdo  

Seu site está muito vazio.  Siga as etapas abaixo para adicionar algum conteúdo a ele.  

1.  Na guia **editor,** substitua `<!-- You're "About Me" will go here.  -->` por `<h1>About Me</h1>` .  
    
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
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="O novo código é realçado na guia editor" lightbox="../media/beginners-html-add1.msft.png":::
             O novo código é realçado na guia editor  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Exibir suas alterações na **guia ao vivo**.  O texto `About Me` está visível na página.  O texto maior do que o texto ao redor, porque `<h1>` o elemento representa um título de seção.  O navegador da Web automaticamente estilos de títulos em tamanhos de fonte maiores.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="O novo título está visível na guia ao vivo" lightbox="../media/beginners-html-add2.msft.png":::
       O novo título está visível na guia ao vivo  
    :::image-end:::  
    
1.  De volta à **guia editor**, insira na linha abaixo onde você acabou de `<p>I am learning HTML.  Recent accomplishments:</p>` colocar `<h1>About Me</h1>` .  
    
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
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="O código atualizado é realçado na guia editor" lightbox="../media/beginners-html-add3.msft.png":::
             O código atualizado é realçado na guia editor  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Exibir sua alteração na **guia ao vivo**.  
1.  De volta à **guia editor**, adicione uma lista de suas conquistas:  
    
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
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="O código atualizado também é realçado na guia editor" lightbox="../media/beginners-html-add4.msft.png":::
             O código atualizado também é realçado na guia editor  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Novamente, volte para a **guia ao** vivo para garantir que o novo conteúdo seja exibido corretamente.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="A nova lista está visível na guia ao vivo" lightbox="../media/beginners-html-add5.msft.png":::
       A nova lista está visível na guia ao vivo  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Experimente alterações de conteúdo no Microsoft Edge DevTools  

Se você estava desenvolvendo uma página grande com muito HTML, é um pouco tedioso ir e voltar entre a guia editor e a guia ao vivo centenas de vezes para exibir suas alterações, especialmente se você não tiver certeza do que exatamente colocar na página.  Microsoft Edge O DevTools ajuda você a experimentar alterações de conteúdo sem sair da **guia ao vivo.**  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Saiba a diferença entre HTML e DOM  

Antes de começar a editar seu conteúdo Microsoft Edge DevTools, você deve entender a diferença entre HTML e DOM.  A melhor maneira de aprender é por exemplo:  

1.  Navegue até **a guia ao vivo**.  Na parte inferior da página, o `A new element!?!` texto é exibido.  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Na parte inferior da página, o texto Um novo elemento!?! é exibido" lightbox="../media/beginners-html-dom1.msft.png":::
       Na parte inferior da página, o `A new element!?!` texto é exibido  
    :::image-end:::  
    
1.  Volte para a **guia editor** e tente encontrar o texto em `index.html` .  O texto não está lá.  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="O texto de mistério Um novo elemento!?! não está em nenhum lugar para ser encontrado index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       O texto de `A new element!?!` mistério não é encontrado em nenhum lugar `index.html`  
    :::image-end:::  
    
1.  Volte para a guia **ao**vivo, passe o mouse sobre , abra o menu contextual \(clique com o botão direito do `A new element!?!` mouse\) e escolha **Inspecionar**.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspecionando algum texto" lightbox="../media/beginners-html-dom3.msft.png":::
       Inspecionando algum texto  
    :::image-end:::  
    
    O DevTools abre junto com sua página.  `<div>A new element!?!</div>` é realçada em azul.  Embora essa estrutura no DevTools se pareça com seu HTML, na verdade é a **árvore DOM**.  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="O DevTools está aberto juntamente com a página" lightbox="../media/beginners-html-dom4.msft.png":::
       O DevTools está aberto juntamente com a página  
    :::image-end:::  
    
Quando sua página é carregada, o navegador pega seu HTML para criar o *conteúdo inicial* da página.  O DOM representa *o conteúdo* atual da página, que pode mudar ao longo do tempo.  O conteúdo `<div>A new element!?!</div>` misterioso é adicionado à sua página devido à marca na parte inferior do `<script src="new.js"></script>` HTML.  Essa marca faz com que algum código JavaScript seja executado.  Saiba mais sobre JavaScript em um tutorial posterior, mas, por enquanto, pense nele como uma linguagem de programação que pode alterar o conteúdo da sua página.  Nesse caso específico, o código JavaScript adiciona `<div>A new element!?!</div>` à sua página.  É por isso que esse texto de mistério é visível em sua página ao vivo, mas não em seu HTML.  

### <a name="edit-the-dom"></a>Editar o DOM  

Se você quiser experimentar rapidamente as alterações de conteúdo sem sair da guia ao vivo, experimente DevTools.  

1.  Em DevTools, passe o mouse sobre , abra o menu contextual \(clique com o botão direito do `Your site!` mouse\) e escolha Editar como **HTML**.  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Editar o nó como HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       Editar o nó como HTML  
    :::image-end:::  
    
1.  Substitua `<p>Your site!</p>` pelo código abaixo.  
    
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
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Atualizando o nó como HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             Atualizando o nó como HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Selecione `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) para salvar suas alterações ou escolher fora da caixa.  Suas alterações aparecem automaticamente na exibição ao vivo da página.  O texto `Your site!` foi substituído pelo novo conteúdo.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="O novo conteúdo aparece imediatamente na página" lightbox="../media/beginners-html-edit3.msft.png":::
       O novo conteúdo aparece imediatamente na página  
    :::image-end:::  
    
Esse fluxo de trabalho só é bom para experimentar alterações de conteúdo.  Se você atualizar a página ou fechar a guia, suas alterações se foram para sempre.  Se você estiver usando esse fluxo de trabalho e quiser salvar suas alterações, será necessário copiar manualmente essas alterações para seu HTML.  As próximas seções mostram mais algumas maneiras de alterar o conteúdo da Árvore DOM.  

## <a name="reorder-nodes"></a>Nós de reordenar  

Você também pode alterar a ordem dos nós DOM.  Por exemplo, em sua página da Web, o menu de navegação está próximo à parte inferior.  Para movê-lo para a parte superior:  

1.  Encontre o `<nav>` nó na Árvore **DOM** de DevTools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="O nó de nav é realçado em azul no DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       O nó de nav é realçado em azul no DevTools  
    :::image-end:::  
    
1.  Arraste o `<nav>` nó até a parte superior, para que o nó seja o primeiro filho do `<body>` nó.  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          O `<nav>` nó agora está sendo exibido na parte superior da página.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Arrastando o nó de nav para a parte superior" lightbox="../media/beginners-html-reorder2.msft.png":::
             Arrastando o nó de nav para a parte superior  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="O nó de nav está na parte superior da página" lightbox="../media/beginners-html-reorder3.msft.png":::
             O nó de nav está na parte superior da página  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a>Excluir um nó  

Você também pode remover nós da Árvore DOM.  

1.  Na Árvore **DOM,** escolha `<div>A new element!?!</div>` .  DevTools realça o nó azul.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Escolha o nó a ser excluído" lightbox="../media/beginners-html-delete1.msft.png":::
       Escolha o nó a ser excluído  
    :::image-end:::  
    
1.  Selecione a `Delete` tecla no teclado.  O `<div>A new element!?!</div>` nó é removido da árvore DOM.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="O nó foi excluído" lightbox="../media/beginners-html-delete2.msft.png":::
       O nó foi excluído  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Copiar suas alterações  

Você está quase terminando.  Você fez algumas alterações em sua página no DevTools, mas elas ainda não foram salvas no código-fonte.  

1.  Atualize sua **guia ao vivo**.  As alterações feitas na Árvore DOM desaparecem.  Em particular, o texto `Your site!` retorna para a parte superior da página e o texto retorna para a parte `A new element!?!` inferior.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="As alterações que você fez foram embora" lightbox="../media/beginners-html-copy1.msft.png":::
       As alterações que você fez foram embora  
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
    
1.  Volte para a **guia editor e** substitua o conteúdo do arquivo pelo código que você `index.html` copiou.  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Como seu arquivo index.html deve ficar" lightbox="../media/beginners-html-copy2.msft.png":::
       Como seu `index.html` arquivo deve ser  
    :::image-end:::  
    
## <a name="next-steps"></a>Próximas etapas  

*   Conclua o próximo tutorial desta série, Introdução [css][DevToolsBeginnersCss], para saber como estilo sua página e experimentar alterações de estilo no Microsoft Edge DevTools.  
*   Leia [Introdução ao DOM][MDNIntroductionDom] para saber mais sobre o DOM.  
*   Confira um curso como Introdução ao [Desenvolvimento da Web][CourseraIntroductionToWebDevelopment] para obter mais experiência de desenvolvimento da Web prática.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools para iniciantes: Introdução com css | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introdução ao desenvolvimento da Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Iniciando com o html | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introdução ao dom | MDN"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original foi encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/beginners/html) e foi criada por [Katherine Jackson][KatherineJackson] \(Technical Writer Intern, Chrome DevTools\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
