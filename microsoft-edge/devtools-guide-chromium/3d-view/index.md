---
description: Tudo sobre o modo de exibição 3D e como usá-lo.
title: Modo de exibição 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: ba1125654c46be6ef4da99efc9ba027ba5e40672
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986077"
---
# Modo de exibição 3D  

Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [dom (modelo de objeto de documento)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .  Com ele, você pode executar as seguintes tarefas.  

*   [Explorar a página da Web traduzida para uma perspectiva 3D](#3d-dom)  
*   [Depuração baseada no contexto de empilhamento de índice z](#z-index)  
*   [Remova alguns dos resíduos no painel dom](#changing-your-view) ou no [painel z-index](#change-the-scope-of-your-exploration)  
*   [Escolher o esquema de cores para melhor depurar problemas do dom](#dom-color-type) ou [problemas no índice z](#z-index-color-type)  

Se você quiser explorar um protótipo anterior do projeto do modo de exibição 3D e executar o código por conta própria, consulte [exemplo de modo de exibição 3D][GithubMicrosoftedgeDevtoolssamples3dview].   

No lado esquerdo, há dois painéis que você pode usar para a sua experiência de depuração.  

1.  O painel [Z-index](#z-index) .  Navegue pelos diferentes elementos do aplicativo Web com o contexto z-index em mente.  O painel **Z-index** é o painel padrão.  
1.  O painel [dom 3D](#3d-dom) .  Explore o DOM como um todo com todos os elementos ao seu alcance.  Para acessar o painel, selecione no painel **dom** ao lado do painel **Z-index** .  
    
No lado direito, a tela exibe suas seleções do [índice Z](#z-index) ou do [dom 3D](#3d-dom).  

## Navegar pela tela  

:::image type="complex" source="../media/canvas.png" alt-text="Tela do modo de exibição 3D" lightbox="../media/canvas.png":::
   Tela do modo de exibição 3D  
:::image-end:::  

### Atalhos de teclado  

*   Girar o DOM: para girar horizontalmente, pressione as `left-arrow` `right-arrow` teclas e.  Para girar verticalmente, pressione as `up-arrow` `down-arrow` teclas e.  
*   Navegue pelo DOM: para se mover pelos elementos adjacentes, selecione um elemento e pressione `up-arrow` as `down-arrow` teclas e.  

### Controles de mouse  

*   Gire o DOM: Selecione e arraste ao lado do espaço da tela.  
*   Movimente-se pelo DOM: Abra o menu contextual \ (clique com o botão direito do mouse \) e arraste na direção que você deseja que o DOM mova.  
*   Zoom: arraste dois dedos pelo Touchpad ou use a roda de rolagem do mouse.  

### Controles na tela  

:::image type="complex" source="../media/controls-small.png" alt-text="Controles na tela" lightbox="../media/controls-small.png":::
   Controles na tela  
:::image-end:::  

*   Redefinir o modo de exibição de tela de pintura para o modo de exibição original: selecione o botão **Redefinir câmera** ou selecione o botão **redefinir elementos em Exibir e recentralizar câmera** \ (ícone de atualização para os lados).  
*   Atualize a tela \ (por exemplo, se o navegador mudou ou você mudou para um modo de exibição de emulador de dispositivo \): selecione o botão **retomar instantâneo** ou selecione o botão **criar novo instantâneo** \ (ícone atualizar \).  

## Índice Z  

:::image type="complex" source="../media/z-index-view-box.png" alt-text="Modo de exibição de índice Z" lightbox="../media/z-index-view-box.png":::
   Modo de exibição de índice Z  
:::image-end:::  

Embora o painel **Z-index** tenha recursos compartilhados com o painel **dom 3D** , os painéis ainda têm elementos que são exclusivos do painel.  

### Realçar elementos com contexto de empilhamento  

A configuração **realçar elementos com contexto de empilhamento** permite ativar \ (e desativar \) as marcas z-índice para os elementos na tela.  A caixa de seleção é marcada por padrão.  

### Alterar o escopo da exploração  

O botão **Mostrar todos os elementos** é a maneira mais rápida de exibir todos os elementos do dom depois de alterar as configurações abaixo.  

O botão **Mostrar somente elementos com contexto de empilhamento** remove elementos sem o contexto de empilhamento e ACHATA o dom para facilitar a navegação.  

O botão **isolar elemento selecionado** é essencialmente três botões em um.  Há duas caixas de seleção abaixo do botão **isolar elemento selecionado** : a caixa de seleção **Mostrar todos os pais** e **manter apenas os pais com o novo contexto de empilhamento** .  

A caixa de seleção **Mostrar todos os pais** está marcada por padrão.  Se você selecionar um elemento no painel de tela e selecionar o botão **isolar elemento selecionado** , a tela exibirá somente o elemento e os pais.  

Se você marcar a caixa de seleção **manter apenas os pais com o novo contexto de empilhamento** e selecionar isolar o botão do **elemento selecionado** , a tela exibirá somente o elemento e os pais que têm um novo contexto de empilhamento.  

Se você desmarcar as caixas de seleção e selecionar o botão **isolar elemento selecionado** , a tela exibirá somente o elemento escolhido na primeira vez.  

Na parte inferior do painel **dom 3D** , localize os **elementos ocultar com a mesma ordem de pintura que sua** caixa de seleção pai.  Marcar e desmarcar a caixa de seleção atualiza os elementos com base em sua seleção.  Se selecionado, os elementos que compartilham ordem de pintura são achatados para o pai.  

As opções destinam-se a limpar parte do email secundário que as páginas da Web mais complexas criam na tela.  

### Tipo de cor do índice Z  

As diferentes visualizações que você pode usar para o DOM na tela.  Seja para diversão ou porque as visualizações ajudam a visualizar o DOM melhor, o DevTools tem três colorways diferentes, bem como uma configuração de cor de **plano de fundo** .  Os botões de opção permitem que você alterne entre as opções e escolha o tipo de cor mais apropriado para o projeto \ (ou que você quiser).  

## DOM 3D  

:::image type="complex" source="../media/dom-purple-box.png" alt-text="Modo de exibição DOM" lightbox="../media/dom-purple-box.png":::
   Modo de exibição DOM  
:::image-end:::  

Se você quiser usar mais um modo de exibição de depuração geral, em vez da experiência do z-index, o **dom 3D** fornece uma aparência geral do dom.  Como o contexto z-index é removido, o DOM é empilhado mais estreitamente e com clareza.  O painel **dom 3D** tem funcionalidade semelhante, mas há algumas nuances.  

### Como alterar o modo de exibição  

No painel **dom 3D** , o botão **isolar elemento selecionado** **inclui filhos** e incluir caixas de seleção dos **pais** .  Por padrão, ambas as caixas de seleção são marcadas, o que significa que a seleção do botão **isolar elemento selecionado** após a seleção de um elemento na tela deve exibir o elemento escolhido, os pais do elemento e os filhos do elemento.  Desmarque a caixa de seleção **incluir filhos** e selecione o botão **isolar elemento selecionado** novamente para exibir o elemento selecionado e os pais do elemento.  Se você marcar a caixa de seleção **incluir filhos** e desmarcar a caixa de seleção **incluir pais** antes de selecionar o botão **isolar elemento selecionado** , a tela exibirá o elemento e os filhos.  Se você desmarcar ambas as caixas de seleção e selecionar o botão **isolar elemento selecionado** , a tela exibirá somente o elemento selecionado anteriormente.  

Um controle deslizante no painel de controle intitulado **nível de aninhamento de página** com um número ao lado dele.  O número indica o número de camadas do documento.  Arrastar o controle deslizante para a esquerda faz com que as camadas mais externas se desapareçam até você ficar com um nível de aninhamento definido como 1, que exibe somente o elemento de back-back mais distante do DOM.  Arrastar o controle deslizante permite remover alguns dos resíduos se você estiver tentando obter uma visão mais detalhada do que está acontecendo nos níveis inferiores.  

### Tipo de cor DOM  

Além do **mapa compromissos-roxo para branco**, **mapa compromissos-azul a amarelo**, **mapa compromissos-arco-íris**e **usar** os botões de opção cor da tela de fundo, há a opção **usar textura de tela**.  A textura de tela adiciona contexto à sua experiência de depuração exibindo o conteúdo da página da Web diretamente nos elementos.  No painel **dom 3D** , a configuração de  **tipo de cor** ainda é um trabalho em andamento, pois alguns sites têm uma textura de tela de renderização de tempo mais difícil no modo de exibição 3D.  

## Entrar em contato com a equipe do Microsoft Edge DevTools

A equipe do Microsoft Edge devtools está trabalhando na interface do usuário e adiciona mais funcionalidade ao modo de exibição 3D com base em uma pergunta de usuários como você.  Envie seus comentários para ajudar a melhorar o Microsoft Edge DevTools.  Basta selecionar o ícone de comentários no devtools ou pressionar `Alt` + `Shift` + `I` \ (Windows \) ou pressionar `Option` + `Shift` + `I` \ (MacOS \) e inserir qualquer comentário ou solicitação de recurso que você tenha para o devtools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Modo de exibição 3D do Microsoft Edge DevTools-MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
