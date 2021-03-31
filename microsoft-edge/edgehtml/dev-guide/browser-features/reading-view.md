---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Veja como o Microsoft Edge fornece um modo de exibição de leitura para páginas da Web para permitir a leitura sem adição.
title: Modo de exibição de leitura-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 30c01d61ff896cca7b0af90b345a8619307f91c0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231796"
---
# <span data-ttu-id="ab700-104">Modo de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="ab700-104">Reading view</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="ab700-105">O Microsoft Edge fornece um modo de exibição de leitura para uma experiência de leitura mais simplificada do que o livro de páginas da Web sem a distração de conteúdo não relacionado ou outro conteúdo secundário na página.</span><span class="sxs-lookup"><span data-stu-id="ab700-105">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="ab700-106">O modo de exibição de leitura pode ser ativado ou desativado no botão **modo de exibição de leitura** \(ícone de livro \) na barra de endereços ou em `Ctrl` + `Shift` + `R` .</span><span class="sxs-lookup"><span data-stu-id="ab700-106">Reading view can be toggled on or off from the **Reading view** \(book icon\) button on the address bar or with `Ctrl`+`Shift`+`R`.</span></span>  <span data-ttu-id="ab700-107">O modo de exibição de leitura extrai os seguintes metadados de uma página:</span><span class="sxs-lookup"><span data-stu-id="ab700-107">Reading view extracts the following metadata from a page:</span></span>  

*   <span data-ttu-id="ab700-108">Title</span><span class="sxs-lookup"><span data-stu-id="ab700-108">Title</span></span>
*   <span data-ttu-id="ab700-109">Autor</span><span class="sxs-lookup"><span data-stu-id="ab700-109">Author</span></span>
*   <span data-ttu-id="ab700-110">Data</span><span class="sxs-lookup"><span data-stu-id="ab700-110">Date</span></span>
*   <span data-ttu-id="ab700-111">Editor</span><span class="sxs-lookup"><span data-stu-id="ab700-111">Publisher</span></span>
*   <span data-ttu-id="ab700-112">Imagem dominante \(s \)</span><span class="sxs-lookup"><span data-stu-id="ab700-112">Dominant image\(s\)</span></span>
*   <span data-ttu-id="ab700-113">Legendas da imagem dominante \(s \)</span><span class="sxs-lookup"><span data-stu-id="ab700-113">Captions of dominant image\(s\)</span></span>
*   <span data-ttu-id="ab700-114">Imagens secundárias</span><span class="sxs-lookup"><span data-stu-id="ab700-114">Secondary images</span></span>
*   <span data-ttu-id="ab700-115">Conteúdo do texto principal da página</span><span class="sxs-lookup"><span data-stu-id="ab700-115">Main text content of the page</span></span>
*   <span data-ttu-id="ab700-116">Direitos autorais</span><span class="sxs-lookup"><span data-stu-id="ab700-116">Copyright</span></span>

<span data-ttu-id="ab700-117">Os usuários podem então ajustar o contraste da página e o tamanho da fonte no painel **configurações** do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab700-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>  

## <span data-ttu-id="ab700-118">Extração de metadados</span><span class="sxs-lookup"><span data-stu-id="ab700-118">Metadata extraction</span></span>  

<span data-ttu-id="ab700-119">Aqui estão detalhes dos metadados de página renderizados pelo modo de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="ab700-119">Here are details of the page metadata rendered by reading view.</span></span>  

### <span data-ttu-id="ab700-120">Title</span><span class="sxs-lookup"><span data-stu-id="ab700-120">Title</span></span>  

<span data-ttu-id="ab700-121">Para garantir que o modo de exibição de leitura renderize o título do artigo:</span><span class="sxs-lookup"><span data-stu-id="ab700-121">To ensure Reading view renders your article's title:</span></span>  

*   <span data-ttu-id="ab700-122">Incluir um `title` elemento no cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab700-122">Include a `title` element in your header</span></span>  
*   <span data-ttu-id="ab700-123">Incluir uma meta tag com</span><span class="sxs-lookup"><span data-stu-id="ab700-123">Include a meta tag with</span></span> `name="title"`  
*   <span data-ttu-id="ab700-124">Correspondam ao texto do título no corpo do artigo com a cadeia de caracteres de conteúdo da sua marca meta.</span><span class="sxs-lookup"><span data-stu-id="ab700-124">Match the title text in your article body with the content string of your meta tag.</span></span>  <span data-ttu-id="ab700-125">Pipes \( `|` \) na cadeia de caracteres de conteúdo impedem que o modo de exibição do leitor se torne ativo, tente usar hifens \( `-` \) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ab700-125">Pipes \(`|`\) in your content string prevent the reader view from becoming active, try using hyphens \(`-`\) instead.</span></span>  

### <span data-ttu-id="ab700-126">Autor</span><span class="sxs-lookup"><span data-stu-id="ab700-126">Author</span></span>  

<span data-ttu-id="ab700-127">O modo de exibição de leitura irá procurar um elemento com `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="ab700-127">Reading View will look for an element with `class = "byline-name"`.</span></span>  <span data-ttu-id="ab700-128">Prática recomendada é colocar o nome do autor após o título e antes do corpo do artigo.</span><span class="sxs-lookup"><span data-stu-id="ab700-128">Best practice is to place the author name after the title and before the article body.</span></span>  

```html
<div class="byline-name">Author name</div>
```  

### <span data-ttu-id="ab700-129">Data</span><span class="sxs-lookup"><span data-stu-id="ab700-129">Date</span></span>  

<span data-ttu-id="ab700-130">O modo de exibição de leitura renderizará as informações do Publicador e de data em conjunto na mesma linha, com estilo adicional para destacar essas informações.</span><span class="sxs-lookup"><span data-stu-id="ab700-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span>  <span data-ttu-id="ab700-131">A data de publicação do artigo será renderizada exatamente como aparece na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ab700-131">The article's publishing date will render exactly as it appears in the string.</span></span>  <span data-ttu-id="ab700-132">O modo de exibição de leitura não é convertido em um formato de data específico.</span><span class="sxs-lookup"><span data-stu-id="ab700-132">Reading view does not convert to a specific date format.</span></span>  

<span data-ttu-id="ab700-133">Se você tiver uma data no corpo do artigo e quiser que o modo de exibição de leitura o renderize, atribua o elemento que contém a data com a classe `'dateline'` :</span><span class="sxs-lookup"><span data-stu-id="ab700-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

<span data-ttu-id="ab700-134">Se você não tiver uma data no corpo do artigo, mas quiser que o modo de exibição de leitura renderize a data, use a marca meta `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="ab700-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### <span data-ttu-id="ab700-135">Editor</span><span class="sxs-lookup"><span data-stu-id="ab700-135">Publisher</span></span>  

<span data-ttu-id="ab700-136">O modo de exibição de leitura procurará o protocolo de gráfico aberto `"og:site_name"` para renderizar as informações do Publicador.</span><span class="sxs-lookup"><span data-stu-id="ab700-136">Reading view will look for the Open Graph protocol `"og:site_name"` to render the publisher information.</span></span>  <span data-ttu-id="ab700-137">Ele também procura `source_organization` e `publisher` atributos em qualquer marca HTML como um indicador secundário das informações do Publisher na página.</span><span class="sxs-lookup"><span data-stu-id="ab700-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span>  <span data-ttu-id="ab700-138">O texto do Publicador será vinculado à URL da página usando o estilo de hiperlink da página modo de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="ab700-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### <span data-ttu-id="ab700-139">Images</span><span class="sxs-lookup"><span data-stu-id="ab700-139">Images</span></span>  

<span data-ttu-id="ab700-140">O modo de exibição de leitura captura a maioria das imagens brutas com largura >= 400px e taxa de proporção >= 1/3 e =< 3,0.</span><span class="sxs-lookup"><span data-stu-id="ab700-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span>  <span data-ttu-id="ab700-141">As imagens que não atendem a essas dimensões ainda podem ser extraídas, como imagens menores do que 400px em largura, mas têm legendas.</span><span class="sxs-lookup"><span data-stu-id="ab700-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span>  <span data-ttu-id="ab700-142">A primeira imagem qualificada torna-se a imagem dominante do artigo.</span><span class="sxs-lookup"><span data-stu-id="ab700-142">The first eligible image becomes the dominant image of the article.</span></span>  <span data-ttu-id="ab700-143">A imagem dominante é renderizada como a primeira parte do conteúdo e recebe toda a largura da coluna.</span><span class="sxs-lookup"><span data-stu-id="ab700-143">The dominant image is rendered as the first piece of content and given full column width.</span></span>  <span data-ttu-id="ab700-144">Todas as imagens a seguir são renderizadas como imagens embutidas no artigo.</span><span class="sxs-lookup"><span data-stu-id="ab700-144">All following images are rendered as inline images within the article.</span></span>  

### <span data-ttu-id="ab700-145">Legendas</span><span class="sxs-lookup"><span data-stu-id="ab700-145">Captions</span></span>  

<span data-ttu-id="ab700-146">Prática recomendada é colocar as imagens nas marcas de [Figura](https://developer.mozilla.org/docs/Web/HTML/Element/figure) com, no máximo, duas marcas [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) aninhadas.</span><span class="sxs-lookup"><span data-stu-id="ab700-146">Best practice is to place images in [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) tags with no more than two nested [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) tags.</span></span>  

### <span data-ttu-id="ab700-147">Body</span><span class="sxs-lookup"><span data-stu-id="ab700-147">Body</span></span>  

<span data-ttu-id="ab700-148">Para garantir que todo o corpo de texto da sua página seja capturado pelo modo de exibição de leitura, ele ajuda a manter a maior parte do texto do artigo o mesmo tamanho de fonte e a profundidade do DOM.</span><span class="sxs-lookup"><span data-stu-id="ab700-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span>  <span data-ttu-id="ab700-149">O algoritmo do modo de exibição de leitura permite algum desvio dessa regra para que os editores possam ter liberdade para adicionar ênfase a linhas ou palavras.</span><span class="sxs-lookup"><span data-stu-id="ab700-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>  

### <span data-ttu-id="ab700-150">Direitos autorais</span><span class="sxs-lookup"><span data-stu-id="ab700-150">Copyright</span></span>  

<span data-ttu-id="ab700-151">O modo de exibição de leitura extrai e exibe as informações de direitos autorais denotadas pelas METAmarcas com `name = "copyright"` , ou se não houver informações de marca meta, um nó de texto que contenha o símbolo \( `©` \) Copyright.</span><span class="sxs-lookup"><span data-stu-id="ab700-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright \(`©`\) symbol.</span></span>  <span data-ttu-id="ab700-152">O modo de exibição de leitura exibe as informações de direitos autorais no final do corpo principal do artigo, com um estilo de fonte menor do que o corpo do texto principal.</span><span class="sxs-lookup"><span data-stu-id="ab700-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>  

```html
<meta name="copyright" content="Your copyright information">
```  

## <span data-ttu-id="ab700-153">Recusar o modo de exibição de leitura</span><span class="sxs-lookup"><span data-stu-id="ab700-153">Opting out of Reading View</span></span>  

<span data-ttu-id="ab700-154">Se você acha que seu conteúdo não é uma boa opção para o modo de exibição de leitura, você pode usar a seguinte marca meta para recusar esse recurso:</span><span class="sxs-lookup"><span data-stu-id="ab700-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>  

```html
<meta name="IE_RM_OFF" content="true">
```  

<span data-ttu-id="ab700-155">Com essa marca, o botão **modo de exibição de leitura** não aparecerá na barra de endereços quando os usuários exibirem sua página.</span><span class="sxs-lookup"><span data-stu-id="ab700-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>  
