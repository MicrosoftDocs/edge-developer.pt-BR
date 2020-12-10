---
description: Tudo sobre o modo de exibição 3D e como usá-lo.
title: Modo de exibição 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203967"
---
# Modo de exibição 3D  

Use o **modo de exibição 3D** para depurar seu aplicativo Web navegando por meio do [dom (modelo de objeto de documento)][MDNDocumentObjectModel] ou do contexto de empilhamento de [índice z][MDNZIndex] .  Com ele, você pode concluir as seguintes tarefas.  

*   [Explorar a página da Web traduzida para uma perspectiva 3D](#3d-dom)  
*   [Depuração baseada no contexto de empilhamento de índice z](#z-index)  
*   [Acessar a funcionalidade da ferramenta camadas do modo de exibição 3D com camadas compostas](#composited-layers)  
*   [Remova alguns dos resíduos no painel dom](#changing-your-view) ou no [painel z-index](#change-the-scope-of-your-exploration)  
*   [Escolher o esquema de cores para melhor depurar problemas do dom](#dom-color-type) ou [problemas no índice z](#z-index-color-type)  

Se você quiser explorar um protótipo anterior do projeto do modo de exibição 3D e executar o código por conta própria, navegue até [exemplo do modo de exibição 3D][GithubMicrosoftedgeDevtoolssamples3dview].  

No lado esquerdo, há três painéis que você pode usar para a sua experiência de depuração.  

*   O painel [Z-index](#z-index) .  Navegue pelos diferentes elementos do aplicativo Web com o contexto z-index em mente.  O painel **Z-index** é o painel padrão.  
*   O painel [dom 3D](#3d-dom) .  Explore o DOM como um todo com todos os elementos facilmente acessíveis.  Para acessar o painel, escolha o painel **dom** ao lado do painel **Z-index** .  
*   O painel de [camadas compostas](#composited-layers) .  Adicione outro elemento 3D para criar uma experiência mais abrangente a partir de uma perspectiva de camadas.  Para acessar o painel, escolha o painel de **camadas compostas** ao lado do painel **dom** .  
    
No lado direito, a tela exibe suas seleções do [índice Z](#z-index), [dom 3D](#3d-dom)ou [camadas compostas](#composited-layers).  

## Navegar pela tela  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Tela do modo de exibição 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Tela do modo de exibição 3D  
:::image-end:::  

### Atalhos de teclado  

*   Girar o DOM: para girar horizontalmente, selecione as `left-arrow` `right-arrow` teclas e.  Para girar verticalmente, selecione as `up-arrow` `down-arrow` teclas e.  
*   Navegue pelo DOM: para se mover pelos elementos adjacentes, escolha um elemento e selecione `up-arrow` as `down-arrow` teclas e.  

### Controles de mouse  

*   Gire o DOM: escolher e arrastar em torno do espaço da tela.  
*   Movimente-se pelo DOM: Abra o menu contextual \ (clique com o botão direito do mouse \) e arraste na direção que você deseja que o DOM mova.  
*   Zoom: arraste dois dedos pelo Touchpad ou use a roda de rolagem do mouse.  

### Controles na tela  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Controles na tela" lightbox="../media/3d-view-controls-small.msft.png":::
   Controles na tela  
:::image-end:::  

*   Redefinir o modo de exibição de tela de pintura para o modo de exibição original: escolha o botão **Redefinir câmera** ou escolha o botão **redefinir elementos em Exibir e recentralizar câmera** \ (ícone de atualização para os lados).  
*   Atualize a tela \ (por exemplo, se o navegador mudou ou você mudou para um modo de exibição do Device Emulator \): escolha o botão **retomar instantâneo** ou escolha o botão **tirar novo instantâneo** \ (ícone atualizar \).  

## Índice Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Modo de exibição de índice Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Modo de exibição de índice Z  
:::image-end:::  

Embora o painel **Z-index** tenha recursos compartilhados com o painel **dom 3D** , os painéis ainda têm elementos que são exclusivos do painel.  

### Realçar elementos com contexto de empilhamento  

A configuração **realçar elementos com contexto de empilhamento** permite ativar \ (e desativar \) as marcas z-índice para os elementos na tela.  A caixa de seleção é selecionada por padrão.  

### Alterar o escopo da exploração  

O botão **Mostrar todos os elementos** é a maneira mais rápida de exibir todos os elementos do dom depois de alterar as configurações abaixo dele.  

O botão **Mostrar somente elementos com contexto de empilhamento** remove elementos sem o contexto de empilhamento e ACHATA o dom para facilitar a navegação.  

O botão **isolar elemento selecionado** é essencialmente três botões em um.  Há duas caixas de seleção abaixo do botão **isolar elemento selecionado** : a caixa de seleção **Mostrar todos os pais** e **manter apenas os pais com o novo contexto de empilhamento** .  

A caixa de seleção **Mostrar todos os pais** está ativada por padrão.  Para exibir o elemento e todos os pais na tela, escolha um elemento e escolha o botão **isolar elemento selecionado** .  

Para exibir o elemento e os pais que têm um novo contexto de empilhamento na tela, ative a configuração **manter somente pais com o novo contexto de empilhamento** e escolha o botão **isolar elemento selecionado** .  

Para exibir o elemento escolhido na tela, desative as configurações e escolha **isolar o botão elemento selecionado** .  

Na parte inferior do painel **dom 3D** , localize os **elementos ocultar com a mesma ordem de pintura que sua** caixa de seleção pai.  Escolher e desmarcar a caixa de seleção atualiza os elementos de acordo com a sua escolha.  Se escolhido, os elementos que compartilham a ordem de pintura são achatados para o pai.  

As opções destinam-se a limpar parte do email secundário que as páginas da Web mais complexas criam na tela.  

### Tipo de cor do índice Z  

As diferentes visualizações que você pode usar para o DOM na tela.  Seja para diversão ou porque as visualizações ajudam a visualizar o DOM melhor, a DevTools tem colorways diferente e uma opção de cor de **plano de fundo** .  O painel **Z-index** compartilha a cor de tela de **fundo** e de **roxo a branco** com o painel **dom 3D** .  Devido ao elemento visual adicionado dos rótulos de índice z, seus comentários levaram a uma redução no número de opções de cores.  A nova simplicidade melhora a experiência de depuração do índice z.  Os botões de opção permitem que você alterne entre as opções e escolha o tipo de cor.  O tipo de cor é o mais apropriado para o seu projeto ou um que você goste mais.  

## DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Modo de exibição DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Modo de exibição DOM  
:::image-end:::  

Se você quiser usar mais um modo de exibição de depuração geral, em vez da experiência do z-index, o **dom 3D** fornece uma aparência geral do dom.  Como o contexto z-index é removido, o DOM é empilhado mais estreitamente e com clareza.  O painel **dom 3D** tem funcionalidade semelhante, mas há algumas nuances.  

### Como alterar o modo de exibição  

No painel **dom 3D** , o botão **isolar elemento selecionado** **inclui filhos** e incluir caixas de seleção dos **pais** .  Ambas as caixas de seleção são ativadas por padrão.  Isso significa que, se você escolher o botão **isolar elemento selecionado** após escolher um elemento, a tela de pintura exibirá o elemento escolhido, os pais do elemento e os filhos do elemento.  Desative a configuração **incluir filhos** e escolha o botão **isolar elemento selecionado** novamente para exibir o elemento escolhido e os pais do elemento.  Se você ativar a configuração **incluir filhos** e desativar a configuração **incluir pais** e, em seguida, escolher o botão **isolar elemento selecionado** , a tela exibirá o elemento e os filhos.  Se você desativar ambas as configurações e escolher o botão **isolar elemento selecionado** , a tela exibirá somente o elemento escolhido anteriormente.  

Um controle deslizante no painel de controle chamado **nível de aninhamento de página** com um número ao lado dele.  O número indica o número de camadas do documento.  Arrastar o controle deslizante para a esquerda faz com que as camadas mais externas se desapareçam até você ficar com um nível de aninhamento definido como `1` , que exibe somente o elemento de back-back mais distante do dom.  Para remover parte do email secundário, arraste o controle deslizante.  Ele ajuda você a ter uma visão mais detalhada do que está acontecendo nos níveis inferiores.  

### Tipo de cor DOM  

O painel **dom 3D** exibe as opções a seguir.  

*   Três colorways diferentes.  
    *   **Mapa compromissos-roxo a branco**  
    *   **Mapa compromissos-azul a amarelo**  
    *   **Mapa compromissos-arco-íris**  
*   **Usar cor de plano de fundo**  
*   **Usar a textura de tela**  
    
A opção **usar textura de tela** adiciona contexto à sua experiência de depuração.  Ele exibe diretamente o conteúdo da página da Web para os elementos.  

## Camadas compostas

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   Painel de **camadas compostas**
:::image-end:::  

O painel de **camadas compostas** abre os elementos da ferramenta **camadas** sem alterar contextos.  Você ainda pode acessar os detalhes de cada uma das camadas e ter os **retângulos de rolagem lentos** e **pintar**.

## Entrar em contato com a equipe Microsoft Edge DevTools  

A equipe do Microsoft Edge devtools está trabalhando na interface do usuário e adiciona mais funcionalidade ao modo de exibição 3D com base nos seus comentários.  Envie seus comentários para ajudar a melhorar o Microsoft Edge DevTools.  Escolha o ícone **enviar comentários** no devtools ou selecione `Alt` + `Shift` + `I` Windows/Linux ou `Option` + `Shift` + `I` no MacOS e insira as solicitações de comentários ou recursos que você tem para o devtools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Modo de exibição 3D do Microsoft Edge DevTools-MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (modelo de objeto de documento) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-índice | MDN"  
