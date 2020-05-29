---
description: Tudo sobre o modo de exibição 3D e como usá-lo.
title: Modo de exibição 3D
author: erdraud
ms.author: erdraud
ms.date: 11/27/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: f2ae80426da71797d4bee4060d33965f04047e19
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560873"
---
# Modo de exibição 3D

Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do dom ( [modelo de objeto de documento](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) ) ou do contexto de empilhamento de [índice z](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) . Você pode: 

- [Explorar a página da Web traduzida para um perspevtive 3D](#3d-dom)
- [Depuração baseada no contexto de empilhamento de índice z](#z-index)
- [Remover parte do email secundário no painel dom](#changing-your-view) ou no [painel z-index](#change-the-scope-of-your-exploration)
- [Escolher o esquema de cores para melhor depurar problemas do dom](#dom-color-type) ou [problemas no índice z](#z-index-color-type)

Há dois painéis que você pode usar para a sua experiência de depuração.

1. **Índice Z** Navegue pelos diferentes elementos do aplicativo Web com o contexto z-index em mente. Este é o painel padrão.
2. **dom 3D** Explore o DOM como um todo com todos os elementos ao seu alcance. Para acessar esse painel, clique no painel "DOM" ao lado do painel "Z-index".

![tela do modo de exibição 3D](./media/canvas.png)

## Navegar pela tela

### Atalhos de teclado
- Girar o DOM: Use as teclas de seta para a esquerda e para a direita para girar horizontalmente e use as teclas de direção para cima e para baixo para girar verticalmente.
- Navegar no DOM: se um elemento for selecionado, você pode usar as teclas de direção para cima e para baixo para percorrer os elementos adjacentes

### Controles de mouse
- Gire o DOM: clique com o botão esquerdo e arraste em torno do espaço da tela.
- Movimente-se pelo DOM: clique com o botão direito do mouse e arraste na direção que você deseja que o DOM mova.
- Zoom: arraste dois dedos pelo Touchpad ou use a roda de rolagem do mouse.

![controles na tela](./media/controls-small.png)
### Controles na tela
- Redefinir o modo de exibição de tela de pintura para o modo de exibição original: clique no botão "redefinir câmera" ou clique no ícone que se parece com um botão de atualização lateral e "redefinir elementos no modo de exibição e recentralizar câmera"
- Atualize a tela (por exemplo, se o navegador mudou ou você mudou para um modo de exibição de emulador de dispositivo): clique no botão que diz "refazer instantâneo" ou clique no botão que se parece com um ícone de atualização e tem "tirar novo instantâneo" como texto de foco.

![Modo de exibição de índice Z](./media/z-index-view-box.png)

## Índice Z

Embora o painel Z-index tenha recursos compartilhados com o painel DOM, ele ainda tem elementos que são exclusivos do painel.

### Realçar elementos com contexto de empilhamento

Essa configuração permite que você ative e desative as marcas de índice z dos elementos na tela de pintura. A caixa de seleção estará selecionada por padrão.

### Alterar o escopo da exploração

O botão **Mostrar todos os elementos** é a maneira mais rápida de exibir todos os elementos do Dom após alterar as configurações abaixo.

**Mostrar somente elementos com contexto de empilhamento** remove elementos sem empilhamento de contexto e ACHATA o dom para facilitar a navegação.

O filtro **isolar elemento selecionado** é essencialmente três botões em um. Há duas caixas de seleção abaixo deste botão: uma é "Mostrar todos os pais" e "manter somente os pais com o novo contexto de empilhamento". 

A caixa de seleção "Mostrar todos os pais" será marcada por padrão. Se você selecionar um elemento no painel tela e clicar em **isolar elemento selecionado**, a tela de pintura só exibirá o elemento e seus pais.

Se você selecionar o botão "manter apenas os pais com o novo contexto de empilhamento" e clicar em **isolar elemento selecionado**, a tela de pintura só exibirá o elemento e os pais que têm um novo contexto de empilhamento.

Se você desmarcar as caixas de seleção e clicar em **isolar elemento selecionado**, a tela de pintura só exibirá o elemento escolhido em primeiro lugar.

Na parte inferior do painel de controles, há os **elementos ocultar com a mesma ordem de pintura que seus pais** alternam. Marcar e desmarcar a caixa de seleção recarregará os elementos com base em sua seleção. Se selecionado, os elementos que compartilham a ordem de pintura serão achatados para o pai.

Essas opções são destinadas a limpar alguns dos emails mais complexos criados por páginas da Web mais complexas na tela.

### Tipo de cor do índice Z

Essas são visualizações diferentes que você pode usar para o DOM na tela. Seja para diversão ou porque ajuda você a visualizar o DOM melhor, temos três colorways diferentes, bem como uma configuração de "cor de plano de fundo". Os botões de opção permitem que você alterne entre as opções e escolha o tipo de cor mais apropriado para o seu projeto (ou que você desejar).

![Modo de exibição DOM](./media/dom-purple-box.png)

## DOM 3D

Se você quiser usar mais um modo de exibição de depuração geral, em vez da experiência do z-index, o DOM 3D fornece uma aparência geral do DOM. Como o contexto z-index é removido, o DOM é empilhado mais estreitamente e com clareza. Esse painel tem funcionalidade semelhante, mas há algumas nuances.

### Como alterar o modo de exibição

No painel **dom 3D** , o filtro **isolar elemento selecionado** tem "incluir filhos" e "incluir pais". Por padrão, ambas as caixas de seleção são marcadas, o que significa que clicar no botão **isolar elemento selecionado** após selecionar um elemento na tela de pintura exibiria o elemento escolhido, os pais do elemento e os filhos do elemento. Desmarcar a caixa de seleção "incluir filhos" e clicar no botão **isolar elemento selecionado** novamente exibiria o elemento selecionado e os pais do elemento. Se você marcar a caixa de seleção "incluir filhos" e desmarcar a caixa de seleção "incluir pais" antes de clicar em **isolar elemento selecionado**, a tela de pintura exibirá o elemento e seus filhos. Se você desmarcar ambas as caixas de seleção e clicar em **isolar elemento selecionado**, a tela de pintura só exibirá o elemento selecionado anteriormente.

Você observará um controle deslizante no painel de controle intitulado **nível de aninhamento** com um número ao lado dele. O número indica o número de camadas no documento. Arrastar o controle deslizante para a esquerda fará com que as camadas mais externas se desapareçam até você ficar com um nível de aninhamento de 1, exibindo somente o elemento back-back mais distante do DOM. Isso permite que você remova alguns dos resíduos se estiver tentando obter uma visão mais detalhada do que está acontecendo nos níveis inferiores.

### Tipo de cor DOM

Você notará que, além das opções de *cor de plano de fundo* de *roxo para branco*, *azul para amarelo*, *arco-íris*e uso de plano de fundo, há uma textura de *tela*. A textura de tela adiciona contexto à sua experiência de depuração exibindo o conteúdo da página da Web diretamente nos elementos. Isso ainda é um trabalho em andamento, pois alguns sites têm um tempo mais difícil renderizando a textura da tela no modo de exibição 3D. 

## Próximas etapas

Estamos trabalhando na interface do usuário e adicionando mais funcionalidade ao modo de exibição 3D com base em uma pergunta de usuários como você. Envie-nos seus comentários para que possamos continuar melhorando o Microsoft Edge DevTools para você. Basta clicar no ícone de comentários no devtools ou pressionar o `Alt`  +  `Shift`  +  `I` Windows ( `Option`  +  `Shift`  +  `I` no Mac) e digitar qualquer comentário ou solicitação de recurso que você tenha para o devtools.