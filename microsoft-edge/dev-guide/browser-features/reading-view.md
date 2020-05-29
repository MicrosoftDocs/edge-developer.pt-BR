---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Veja como o Microsoft Edge fornece um modo de exibição de leitura para páginas da Web para permitir a leitura sem adição.
title: Guia de desenvolvimento-modo de exibição de leitura
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: e84edb5cc29b644939895f2996c50f3b4ec23379
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560565"
---
# Modo de leitura

O Microsoft Edge fornece um *modo de exibição de leitura* para uma experiência de leitura mais simplificada do que o livro de páginas da Web sem a distração de conteúdo não relacionado ou outro conteúdo secundário na página. O modo de exibição de leitura pode ser ativado ou desativado no botão **modo de exibição de leitura** (ícone de livro) na barra de **endereços** (ou com **Ctrl**  +  **Shift**  +  **R**). O modo de exibição de leitura extrai os seguintes metadados de uma página:

* Title
* Autor
* Data
* Editor
* Imagem (s) dominante (s)
* Legendas da (s) imagem (s) dominante (s)
* Imagens secundárias
* Conteúdo do texto principal da página
* Direitos autorais

Os usuários podem então ajustar o contraste da página e o tamanho da fonte no painel **configurações** do Microsoft Edge.

## Extração de metadados


Aqui estão detalhes dos metadados de página renderizados pelo modo de exibição de leitura.

### Title

Para garantir que o modo de exibição de leitura renderize o título do artigo:

* Incluir um elemento **title** no cabeçalho
* Incluir uma meta tag com `name="title"`
* Correspondam ao texto do título no corpo do artigo com a cadeia de caracteres de conteúdo da sua marca meta. Pipes `|` em sua cadeia de caracteres de conteúdo impedem que o modo de exibição leitor se torne ativo, tente usar hypens `-` .

### Autor

O modo de exibição de leitura irá procurar um elemento com `class = "byline-name"` . Prática recomendada é colocar o nome do autor após o título e antes do corpo do artigo.

```html
<div class="byline-name">Author name</div>
```

### Data

O modo de exibição de leitura renderizará as informações do Publicador e de data em conjunto na mesma linha, com estilo adicional para destacar essas informações. A data de publicação do artigo será renderizada exatamente como aparece na cadeia de caracteres. O modo de exibição de leitura não é convertido em um formato de data específico.

Se você tiver uma data no corpo do artigo e quiser que o modo de exibição de leitura o renderize, atribua o elemento que contém a data com a classe `'dateline'` :

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```

Se você não tiver uma data no corpo do artigo, mas quiser que o modo de exibição de leitura renderize a data, use a marca meta `name='displaydate'` :

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```

### Editor

O modo de exibição de leitura procurará o protocolo de *gráfico aberto* `"og:site_name"` para renderizar as informações do Publicador. Ele também procura `source_organization` e `publisher` atributos em qualquer marca HTML como um indicador secundário das informações do Publisher na página. O texto do Publicador será vinculado à URL da página usando o estilo de hiperlink da página modo de exibição de leitura.

```html
<meta content="Name of organization source" property="og:site_name">
```

### Images

O modo de exibição de leitura captura a maioria das imagens brutas com largura >= 400px e taxa de proporção >= 1/3 e =< 3,0. As imagens que não atendem a essas dimensões ainda podem ser extraídas, como imagens menores do que 400px em largura, mas têm legendas. A primeira imagem qualificada torna-se a imagem dominante do artigo. A imagem dominante é renderizada como a primeira parte do conteúdo e recebe toda a largura da coluna. Todas as imagens a seguir são renderizadas como imagens embutidas no artigo.

### Legendas

Prática recomendada é colocar as imagens nas marcas de [Figura](https://msdn.microsoft.com/library/gg593038(v=vs.85).aspx) com, no máximo, duas marcas [figcaption](https://msdn.microsoft.com/library/gg593037(v=vs.85).aspx) aninhadas.

### Body

Para garantir que todo o corpo de texto da sua página seja capturado pelo modo de exibição de leitura, ele ajuda a manter a maior parte do texto do artigo o mesmo tamanho de fonte e a profundidade do DOM. O algoritmo do modo de exibição de leitura permite algum desvio dessa regra para que os editores possam ter liberdade para adicionar ênfase a linhas ou palavras.

### Direitos autorais

O modo de exibição de leitura extrai e exibe as informações de direitos autorais denotadas pelas METAmarcas com `name = "copyright"` , ou se não houver informações de marca meta, um nó de texto que contenha o símbolo de direitos autorais (**©**). O modo de exibição de leitura exibe as informações de direitos autorais no final do corpo principal do artigo, com um estilo de fonte menor do que o corpo do texto principal.

```html
<meta name="copyright" content="Your copyright information">
```

## Recusar o modo de exibição de leitura


Se você acha que seu conteúdo não é uma boa opção para o modo de exibição de leitura, você pode usar a seguinte marca meta para recusar esse recurso:

```html
<meta name="IE_RM_OFF" content="true">
```

Com essa marca, o botão **modo de exibição de leitura** não aparecerá na barra de endereços quando os usuários exibirem sua página.
