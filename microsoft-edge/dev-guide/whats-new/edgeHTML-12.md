---
description: Esta página fornece uma visão geral do que há de novo no EdgeHTML 12.
title: Novidades do EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: f16db0551d4bea3d29b974c2a35fff2adf476c75
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560554"
---
# Novidades do EdgeHTML 12

O Microsoft Edge introduz o EdgeHTML, um novo mecanismo "vivo" projetado com interoperabilidade em seu núcleo, para garantir que você esteja sempre obtendo a mais recente e mais alta plataforma da Web do Windows. O Microsoft Edge apresenta uma quebra limpa do passado, grátis do código herdado necessário para dar suporte a controles ActiveX, BHOs (objetos auxiliares do navegador) e outras práticas de desenvolvimento da Web Bygone. Além disso, o Microsoft Edge oferece suporte a PDF nativo. A partir de IE11, os modos de documento herdados foram preteridos e, com o Microsoft Edge, a infraestrutura de navegador para dar suporte a ele não existe. Confira o [IEBlog](https://go.microsoft.com/fwlink/p/?LinkID=519011) para obter mais informações.

Aqui estão as alterações fornecidas com o EdgeHTML 12 na versão inicial do [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) (07/2015, Build 10240). Para obter uma visão geral das alterações no navegador geral do Microsoft Edge, veja [uma pausa do passado: o nascimento do novo mecanismo de renderização da Web da Microsoft](https://blogs.windows.com/msedgedev/2015/02/26/a-break-from-the-past-the-birth-of-microsofts-new-web-rendering-engine/) e [uma pausa do passado, parte 2: dizer adeus a ActiveX, VBScript, AttachEvent...](https://blogs.windows.com/msedgedev/2015/05/06/a-break-from-the-past-part-2-saying-goodbye-to-activex-vbscript-attachevent/)

Aqui está o link permanente para a seguinte lista de alterações: [https://aka.ms/devguide_edgehtml_12](https://aka.ms/devguide_edgehtml_12) .


## Novos recursos

### Política de segurança de conteúdo 1,0
O Microsoft Edge agora implementa o CSP (política de segurança de conteúdo) 1,0. O padrão de segurança do CSP permite que os desenvolvedores da Web controlem os recursos (script, CSS, plugins, imagens, etc.), que uma determinada página pode buscar ou executar com o objetivo de evitar XSS (script entre sites), clickjacking e outros ataques de injeção de código que buscam executar conteúdo mal-intencionado no contexto de uma página da Web confiável. Consulte [política de segurança de conteúdo](https://docs.microsoft.com/microsoft-edge/dev-guide/security/content-security-policy) para obter mais informações sobre o CSP no Microsoft Edge. 

### Filtrar efeitos
O Microsoft Edge oferece uma maneira fácil de adicionar efeitos visuais aos elementos. Usando a `filter` propriedade, você pode adicionar esfumadores, ajustar o brilho, adicionar uma sombra projetada, alterar a opacidade e muito mais para um elemento. Usando essencialmente CSS, você pode aplicar vários efeitos de filtro a um elemento e animar os filtros. Para obter mais informações, consulte [Filtrar efeitos](https://docs.microsoft.com/microsoft-edge/dev-guide/css/filter-effects).

### JavaScript
O suporte a JavaScript varia ligeiramente entre a versão final do Internet Explorer (IE11) e o Microsoft Edge. Os novos recursos do Edge incluem:

| | |
|--|--|
|**Demonstrativos**| [classe](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) (experimental), [para... da](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) |
|**Eles**| [Promessa](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [símbolo](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [fracoset](/scripting/javascript/reference/weakset-object-javascript) |
|**Funções** | [ACOSH](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [IsInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [IsNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [RAW](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw) |
|**Métodos**| [inclui](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [chaves](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) (matriz), [repetir](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) (cadeia), [valores](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) (matriz) |
|**Outros recursos**| [Funções](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) (experimental), [geradores](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [iteradores](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [ `y` sinalizador de expressão regular](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) (experimental), [cadeias](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals)de caracteres de modelo, [caracteres de escape de ponto de código Unicode](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals) |

Para obter uma comparação entre o suporte de JavaScript em aplicativos Internet Explorer, Microsoft Edge e Microsoft Store, consulte [*informações sobre a versão JavaScript*](./javascript-version-information.md).

### Captura e fluxos de mídia
O Microsoft Edge introduz o suporte para as APIs de captura e fluxo de mídia com base na especificação de [captura e fluxo de mídia do W3C](https://go.microsoft.com/fwlink/p/?LinkID=534096) . Essas APIs JavaScript permitem que páginas da Web acessem dispositivos de captura de mídia, como webcams ou microfones, com permissão do usuário. Usando as APIs de captura e fluxo de mídia, você pode criar cenários como capturar uma foto usando uma webcam ou capturar uma mensagem de voz de um microfone. Leia mais sobre a captura de mídia no Microsoft Edge no [blog do desenvolvedor do Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/13/announcing-media-capture-functionality-in-microsoft-edge/). 

### Novo elemento HTML e atributos
* `meter` sub-elemento
* `picture` sub-elemento
* `template` sub-elemento
* `image` elemento: `srcset` e `sizes` atributos ( [postagem do blog](https://blogs.windows.com/msedgedev/2015/06/08/introducing-srcset-responsive-images-in-microsoft-edge/)do desenvolvedor do Microsoft Edge)
* `selectionDirection` atributo
* `input type=time` e `input type=datetime-local`

### API RTC Object 
O objeto de comunicação em tempo real (ORTC) permite que a mídia (áudio e/ou vídeo) seja transmitida (enviada e recebida) em tempo real diretamente entre navegadores da Web, dispositivos móveis e servidores via APIs JavaScript nativas. Confira o objeto de tópico do guia de desenvolvimento do objeto de tópico [RTC API](https://docs.microsoft.com/microsoft-edge/dev-guide/realtime-communication/object-rtc-api) para obter mais informações sobre ORTC no Microsoft Edge. 

### Modo de Leitura
O Microsoft Edge fornece um modo de exibição de leitura para uma experiência de leitura mais simplificada do que o livro de páginas da Web sem a distração de conteúdo não relacionado ou outro conteúdo secundário na página. O modo de exibição de leitura pode ser ativado ou desativado no botão modo de exibição de leitura (ícone de livro) na barra de endereços (ou com CTRL + SHIFT + R). Acesse o [modo de exibição de leitura](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/reading-view) para obter mais informações. 

### Descoberta de provedores de pesquisa
A integração de pesquisa avançada está embutida na barra de endereços do Microsoft Edge, incluindo sugestões de pesquisa, resultados da Web, seu histórico de navegação e favoritos. O Microsoft Edge segue a especificação [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) para descobrir e usar provedores de pesquisa na Web. Se você for um provedor de pesquisa, [Leia mais](https://docs.microsoft.com/microsoft-edge/dev-guide/browser/search-provider-discovery) sobre como garantir que o Microsoft Edge dê suporte ao seu serviço. 

### Suporte para APIs WebKit
Para melhorar a compatibilidade, o Microsoft Edge oferece suporte a uma variedade de APIs prefixadas "-WebKit-". Para obter uma lista completa de APIs "-WebKit-" com suporte, use o [Catálogo de API](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).

### Áudio da Web
O Microsoft Edge introduz o suporte para a especificação de [API de áudio do W3C Web](https://go.microsoft.com/fwlink/p/?LinkID=512167) . Áudio da Web é uma API JavaScript de alto nível para processar e resumir áudio em aplicativos Web para fornecer experiências de áudio e música avançadas. Embora o `audio` elemento HTML5 permita reprodução de áudio de fluxo de áudio básica, a API de áudio da Web fornece uma variedade de APIs que permitem que você reproduza vários sons com sincronização justa e aplique ganhos, fades, transições e efeitos básicos em um áudio misto. Leia mais sobre [áudio da Web](https://docs.microsoft.com/microsoft-edge/dev-guide/multimedia/web-audio) no guia de desenvolvimento e no [blog do desenvolvedor do Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/19/bringing-web-audio-to-microsoft-edge-for-interoperable-gaming-and-enthusiast-media/). 

### Driver da Web 
A [API do W3C WebDriver](https://w3.org/TR/webdriver/) é uma plataforma e uma interface neutra em linguagem e um protocolo de conexão, permitindo que programas ou scripts controlem o comportamento de um navegador da Web. O WebDriver permite que os desenvolvedores criem testes automatizados que simulam a interação do usuário. Isso é diferente dos testes de unidade JavaScript porque o WebDriver tem acesso à funcionalidade e às informações que o JavaScript em execução no navegador não, e ele pode simular de forma mais precisa eventos do usuário ou eventos no nível do sistema operacional. O WebDriver também pode gerenciar o teste em várias janelas, guias e páginas da Web em uma única sessão de teste.  Para saber mais sobre como começar a usar o WebDriver para Microsoft Edge, confira [WebDriver](https://docs.microsoft.com/microsoft-edge/dev-guide/tools/webdriver). 


## Novas APIs no EdgeHTML 12

Aqui está a lista completa de novas APIs no EdgeHTML 12.  Elas são listadas no formato **[nome da interface]. [ nome da API]**.

 > [!NOTE] 
 > Muitas dessas APIs estavam disponíveis no IE11. Os dados a seguir para o EdgeHTML 12 são oferecidos como uma linha de base para comparar a versão inicial do EdgeHTML às versões posteriores.

<iframe height='580' scrolling='no' title='Novas APIs no EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Veja a caneta <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> novas APIs no EdgeHTML 12 </a> por documentos do Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>
