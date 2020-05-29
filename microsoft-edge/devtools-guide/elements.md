---
description: Use o painel elementos para inspecionar o HTML, CSS, DOM e acessibilidade da página.
title: DevTools-elementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, elementos, HTML, CSS, pontos de interrupção do dom, eventos, acessibilidade
ms.custom: seodec18
ms.openlocfilehash: 8948ddb3291bd122521e0b0800c0113a576d49e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562226"
---
# Elementos

O painel **elementos** ajuda você a:

* [Identificar e Editar elementos na árvore HTML](#html-tree-view) da página atual
* [Inspecionar e modificar CSS](./elements/styles.md) na página, incluindo pseudo-estados e pseudoelementos
* [Entender o layout CSS e o estilo em cascata](./elements/computed.md) acontecendo na página
* [Rastrear manipuladores de eventos não autorizados](./elements/events.md) para que você possa depurá-los
* [Definir pontos de interrupção de depuração para alterações visuais inesperadas](./elements/dom-breakpoints.md) para saltar para o código que os causou
* [Obter informações detalhadas sobre as fontes usadas na página](./elements/fonts.md) e onde elas estão sendo carregadas
* [Exibir sua página a partir de um ponto de vista do leitor de tela](./elements/accessibility.md) para verificar e testar a acessibilidade 
* [Revisar uma comparação em execução das alterações de CSS](./elements/changes.md) feitas enquanto você depura a interface do usuário da página

## Modo de exibição de árvore HTML

![O painel elementos DevTools do Microsoft Edge](./media/elements.png)

1. Use a ferramenta **Select Element** ( `Ctrl+B` ) para localizar um elemento no **modo de exibição de árvore HTML** clicando nele na página.

2. Use a ferramenta de **realce de elemento** ( `Ctrl+Shift+L` ) para localizar um elemento na página passando o mouse sobre ele no **modo de exibição de árvore HTML**.

3. Abra a ferramenta **seletor de cores** ( `Ctrl+K` ) para ver uma lista das cores em uso na página atual. Clicar em uma cor na lista fornece mais detalhes (Matiz, saturação, luminosidade, alfa). O *seletor de cores* também é aberto quando você clica no quadrado colorido ao lado de um valor de cor no painel **estilos** , permitindo que você edite a cor de um elemento de página e veja os resultados imediatamente.

4. O botão da **árvore de acessibilidade** ( `Ctrl+Shift+A` ) abrirá o painel de [árvore de acessibilidade](./elements/accessibility.md) mostrando a estrutura da sua página como seria exibido para uma tecnologia assistencial, como o [narrador do Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) leitor.

5. Você também pode **encontrar** ( `Ctrl+F` ) um elemento no modo de exibição de árvore HTML procurando por seu nome de marca, atributos ou conteúdo de texto.

### Editando elementos

Você pode editar um elemento clicando com o botão direito do mouse nele dentro do modo de exibição de árvore HTML e selecionando **Editar como HTML** no menu de contexto. O menu de contexto também fornece opções para excluir, recortar, copiar, colar, definir pseudovariáveis CSS (*: ativo*, *: foco*, *: focalizar*, *: visitado*) e adicionar atributos. Outra maneira de editar um atributo e/ou seu valor é clicar duas vezes nele no modo de exibição de árvore HTML.

![Menu de contexto da exibição em árvore HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> Editar a árvore HTML não afeta a marcação de origem subjacente. Atualizar a página reverterá as alterações e renderizará apenas o layout determinado pela fonte da página. Você pode **copiar** o HTML modificado para a área de transferência clicando com o botão direito do mouse no elemento desejado (ou no `html` elemento global, se você quiser a página inteira) para abrir o menu de contexto. (As opções de**recorte** e **colagem** também estão disponíveis).

No painel [estilos](./elements/styles.md) , você também pode adicionar/excluir/Editar pseudoelementos e pseudoelementos CSS.

## Painéis de ferramentas

Depois de selecionar um elemento de página de interesse, você pode usar os painéis de ferramentas para inspecionar ainda mais seus diferentes estilos e propriedades de acessibilidade, exibir seus ouvintes de eventos e definir pontos de interrupção de mutação DOM.

![Painéis ferramentas no painel elementos](./media/elements_toolpanes.png)

1. [**Estilos**](./elements/styles.md): estilos atualmente aplicados organizados por folha de estilos

2. [**Calculado**](./elements/computed.md): estilos atualmente aplicados organizados por atributos de CSS

3. [**Eventos**](./elements/events.md): ouvintes de eventos registrados no elemento atual e nos elementos ancestrais

4. [**Pontos**](./elements/dom-breakpoints.md)de interrupção dom: pontos de interrupção de mutação dom 

5. [**Fontes**](./elements/fonts.md): fontes aplicadas atualmente para um elemento selecionado

6. [**Acessibilidade**](./elements/accessibility.md): Propriedades de acessibilidade

7. [**Alterações**](./elements/changes.md): alterações de CSS feitas durante a sessão de diagnóstico  

## Teclado

| Ação               | Atalho               |
|:---------------------|:-----------------------|
| Painel elementos       | `Ctrl` + `1`           |
| Realce de elemento | `Ctrl` + `Shift` + `L` |
| Selecionar elemento       | `Ctrl` + `B`           |
| Seletor de cor         | `Ctrl` + `K`           |
| Árvore de acessibilidade   | `Ctrl` + `Shift` + `A` |
