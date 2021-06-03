---
description: Tudo sobre o 3D View e como usá-lo.
title: Modo de exibição 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "11203967"
---
# <a name="3d-view"></a>Modo de exibição 3D  

Use o **View 3D** para depurar seu aplicativo Web navegando pelo DOM (Modelo de Objeto de [Documento)][MDNDocumentObjectModel] ou pelo contexto de empilhamento de [índice z.][MDNZIndex]  Com ele, você pode concluir as seguintes tarefas.  

*   [Explorar a página da Web traduzida em uma perspectiva 3D](#3d-dom)  
*   [Depuração com base no contexto de empilhamento de índice z](#z-index)  
*   [Acessar a funcionalidade da ferramenta Layers do 3D View com camadas compostas](#composited-layers)  
*   [Limpar parte da desordem no painel DOM](#changing-your-view) ou no [painel de índice z](#change-the-scope-of-your-exploration)  
*   [Escolha o esquema de cores para melhor depurar seus problemas de DOM](#dom-color-type) ou problemas de índice [z](#z-index-color-type)  

Se você quiser explorar um protótipo inicial do projeto de Exibição 3D e executar o código por conta própria, navegue até Amostra de Exibição [3D][GithubMicrosoftedgeDevtoolssamples3dview].  

No lado esquerdo, há três painéis que você pode usar para sua experiência de depuração.  

*   O [painel de índice Z.](#z-index)  Navegue pelos diferentes elementos no aplicativo Web com o contexto de índice z em mente.  O **painel de índice Z** é o painel padrão.  
*   O [painel DOM 3D.](#3d-dom)  Explore o DOM como um todo com todos os elementos facilmente acessíveis.  Para acessar o painel, escolha o painel **DOM** ao lado do **painel de índice Z.**  
*   O [painel Camadas Compostas.](#composited-layers)  Adicione outro elemento 3D para criar uma experiência mais abrangente de uma perspectiva de camadas.  Para acessar o painel, escolha o painel **Camadas** Compostas ao lado do **painel DOM.**  
    
No lado direito, a tela exibe suas seleções do [índice Z,](#z-index) [DOM 3D](#3d-dom)ou [Camadas Compostas](#composited-layers).  

## <a name="navigating-the-canvas"></a>Navegando na tela  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Tela de exibição 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Tela de exibição 3D  
:::image-end:::  

### <a name="keyboard-shortcuts"></a>Atalhos de teclado  

*   Gire o DOM: para girar horizontalmente, selecione `left-arrow` as `right-arrow` teclas e.  Para girar verticalmente, selecione `up-arrow` as `down-arrow` teclas e.  
*   Navegue pelo DOM: para mover pelos elementos adjacentes, escolha um elemento e selecione `up-arrow` e `down-arrow` teclas.  

### <a name="mouse-controls"></a>Controles de mouse  

*   Gire o DOM: Escolha e arraste em torno do espaço da tela.  
*   Pan ao redor do DOM: Abra o menu contextual \(clique com o botão direito do mouse\) e arraste na direção que você deseja que o DOM mova.  
*   Zoom: arraste dois dedos pelo touchpad ou use a roda de rolagem no mouse.  

### <a name="on-screen-controls"></a>Controles na tela  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Controles na tela" lightbox="../media/3d-view-controls-small.msft.png":::
   Controles na tela  
:::image-end:::  

*   Reset the canvas view to the original view: Choose the **Reset camera** button, or choose the Reset elements in view and **re-center camera** \(sideways refresh icon\) button.  
*   Atualize a tela \(por exemplo, se o navegador for alterado ou você alternado para **** uma exibição do emulador de dispositivo\): Escolha o botão **Retomar** instantâneo ou escolha o botão Tomar novo instantâneo \(ícone de atualização\).  

## <a name="z-index"></a>Índice Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Exibição de índice Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Exibição de índice Z  
:::image-end:::  

Embora o **painel de índice Z** tenha recursos compartilhados com o painel DOM **3D,** os painéis ainda têm elementos exclusivos do painel.  

### <a name="highlight-elements-with-stacking-context"></a>Destacar elementos com contexto de empilhamento  

A **configuração Realçamento** de elementos com contexto de empilhamento permite ativar \(e desativar\) as marcas de índice z para os elementos na tela.  A caixa de seleção é escolhida por padrão.  

### <a name="change-the-scope-of-your-exploration"></a>Alterar o escopo de sua exploração  

O **botão Mostrar todos os** elementos é a maneira mais rápida de exibir todos os elementos do DOM após alterar as configurações abaixo dele.  

O **botão Mostrar somente elementos com contexto de** empilhamento remove elementos sem empilhar contexto e nivela o DOM para facilitar a navegação.  

O **botão Isolar elemento selecionado** é essencialmente três botões em um.  Há duas caixas de **** seleção abaixo do botão Isolar elemento selecionado: a caixa de seleção **Mostrar** todos os pais e Manter somente pais com nova caixa de seleção **de contexto de** empilhamento.  

Por **padrão,** a caixa de seleção Mostrar todos os pais está 100% 100%.  Para exibir o elemento e quaisquer pais na tela, escolha um elemento e escolha **o botão Isolar elemento selecionado.**  

Para exibir o elemento e os pais que têm um novo **** contexto de empilhamento na tela, a opção Manter somente pais com nova configuração de contexto de empilhamento e escolha o botão Isolar elemento **selecionado.**  

Para exibir o elemento escolhido na tela, desligue as configurações e escolha **Isolar botão de elemento** selecionado.  

Na parte inferior do painel **DOM 3D,** localize os elementos Hide com a mesma ordem de tinta **que sua caixa de** seleção pai.  Escolher e desmarcar a caixa de seleção atualiza os elementos com base em sua escolha.  Se escolhido, os elementos que compartilham a ordem de tinta são achatado para o pai.  

As opções são destinadas a limpar parte da desordem que as páginas da Web mais complexas criam em sua tela.  

### <a name="z-index-color-type"></a>Tipo de cor de índice Z  

As são as diferentes visualizações que você pode usar para o DOM em sua tela.  Se você usá-lo para diversão ou porque as visualizações ajudam você a visualizar melhor o DOM, o DevTools tem formas de cores diferentes e uma **opção Usar** cor de plano de fundo.  O **painel de índice Z** compartilha a cor roxo para **branco** e **plano** de fundo com o painel **DOM 3D.**  Dado o elemento visual adicionado dos rótulos de índice z, seus comentários que levaram a uma redução no número de opções de cores.  A nova simplicidade melhora a experiência de depuração de índice z.  Os botões de opção permitem alternar entre as opções e escolher o tipo de cor.  O tipo de cor é mais apropriado para seu projeto ou um que você mais gosta.  

## <a name="3d-dom"></a>DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Exibição DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Exibição DOM  
:::image-end:::  

Se você quiser ter mais de um modo de exibição geral de depuração, em vez da experiência de índice z, o **DOM 3D** fornece uma aparência geral do DOM.  Como o contexto de índice z é removido, o DOM é empilhado de forma mais próxima e limpa.  O **painel DOM 3D** tem uma funcionalidade semelhante, mas há algumas nuances.  

### <a name="changing-your-view"></a>Alterar sua exibição  

No painel **DOM 3D,** o botão Isolar elemento **selecionado** tem As caixas de seleção **Incluir filhos** e **Incluir** pais.  As duas caixas de seleção estão 24h 24h por padrão.  Isso significa que **** se você escolher o botão Isolar elemento selecionado após escolher um elemento, a tela exibirá o elemento escolhido, os pais do elemento e os filhos do elemento.  Desativar a **configuração Incluir filhos** e escolha o botão Isolar elemento **selecionado** novamente para exibir o elemento escolhido e os pais do elemento.  Se você ativar a configuração Incluir **** **filhos** e desativar a configuração Incluir pais e, em seguida, escolher o botão **Isolar** elemento selecionado, a tela exibirá o elemento e quaisquer filhos.  Se você desativar as duas configurações e escolher o botão **Isolar** elemento selecionado, a tela exibirá apenas o elemento escolhido anteriormente.  

Um controle deslizante no painel de controle chamado **Nível de** aninhamento para página com um número ao lado dele.  O número indica o número de camadas do documento.  Arrastar o controle deslizante para a esquerda faz com que as camadas mais externas se descamem até que você seja deixado com um nível de aninhamento definido como , que exibe apenas o elemento back mais distante no `1` DOM.  Para remover parte da desordem, arraste o controle deslizante.  Isso ajuda você a ver mais de perto o que está acontecendo nos níveis inferiores.  

### <a name="dom-color-type"></a>Tipo de cor DOM  

O **painel DOM 3D** exibe as seguintes opções.  

*   Três formas de cores diferentes.  
    *   **Heatmap - Roxo para Branco**  
    *   **Heatmap - Azul para Amarelo**  
    *   **Heatmap - Arco-íris**  
*   **Usar cor de plano de fundo**  
*   **Usar textura de tela**  
    
A **opção Usar textura de** tela adiciona contexto à sua experiência de depuração.  Ele exibe diretamente o conteúdo da página da Web para os elementos.  

## <a name="composited-layers"></a>Camadas compostas

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Painel de camadas compostas" lightbox="../media/experiments-layers.msft.png":::
   Painel de **Camadas Compostas**
:::image-end:::  

O **painel Camadas Compostas** abre os elementos da ferramenta **Layers** sem alterar contextos.  Você ainda pode acessar os detalhes de cada uma das camadas e ter as **rects** de rolagem **lenta**e Paint .

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools  

A Microsoft Edge equipe do Devtools está trabalhando na interface do usuário e adicionando mais funcionalidade ao 3D View com base em seus comentários.  Envie seus comentários para ajudar a melhorar o Microsoft Edge DevTools.  Escolha o **ícone Enviar Comentários** no DevTools ou selecione no Windows/Linux ou no macOS e insira qualquer comentário ou solicitação de recurso que você tenha para `Alt` + `Shift` + `I` `Option` + `Shift` + `I` o DevTools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge Exibição 3D do DevTools - MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objeto de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
