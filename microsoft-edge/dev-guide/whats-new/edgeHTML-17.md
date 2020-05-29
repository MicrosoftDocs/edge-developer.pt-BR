---
title: Novos recursos e APIs no EdgeHTML 17
description: Este guia fornece uma visão geral dos recursos e padrões do desenvolvedor incluídos no EdgeHTML 17.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 1359464bfb9ec6f2b84536a11b0fb4bfcce2fb1c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560577"
---
# O que há de novo no EdgeHTML 17

Aqui está uma lista dos recursos novos e atualizados fornecidos na [EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/04/30/edgehtml-17-april-2018-update/) na plataforma da Web, como parte da [atualização do Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/27/make-the-most-of-your-time-with-the-new-windows-10-update/) (04/2018, Build 17134). Para alterações em compilações específicas do [Windows Insider](https://insider.windows.com/) Preview, consulte o [changelog do Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) e [o que há de novo no EdgeHTML](../whats-new.md).

Aqui está o link permanente para a seguinte lista de alterações: [https://aka.ms/devguide_edgehtml_17](https://aka.ms/devguide_edgehtml_17) .

## Recursos novos e atualizados 

### Funções, Estados e eventos do ARIA 1,1

O EdgeHTML 17 adiciona suporte a várias funções, Estados e propriedades da [especificação de aplicativos da Internet sofisticados (WAI-ARIA 1,1) disponíveis](https://w3.org/TR/wai-aria-1.1/), incluindo [feed](https://www.w3.org/TR/wai-aria-1.1/#feed), [formulário](https://www.w3.org/TR/wai-aria-1.1/#form), [Aria-haspopup](https://w3.org/TR/wai-aria-1.1/#aria-haspopup), [Aria-PlaceHolder](https://w3.org/TR/wai-aria-1.1/#aria-placeholder)e muito mais; Encontre uma [lista completa de atualizações do Aria no Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299). Com esta atualização, EdgeHTML 17 agora oferece suporte a todas as funções e atributos definidos em WAI-ARIA 1,1. Confira os documentos de [acessibilidade](https://docs.microsoft.com/microsoft-edge/accessibility) para obter mais informações sobre acessibilidade no Microsoft Edge.

### Mascaramento CSS

EdgeHTML 17 inclui suporte experimental ao [mascaramento de CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking). A implementação parcial introduz a máscara de CSS [-imagem](https://developer.mozilla.org/docs/Web/CSS/mask-image) e propriedades [de tamanho da máscara](https://developer.mozilla.org/docs/Web/CSS/mask-size) .  Marque a bandeira "Habilitar mascaramento CSS" em About: flags para estar experimentando!

### As transformações CSS em elementos SVG

EdgeHTML 17 agora oferece suporte a CSS Transforms em elementos SVG e atributos de apresentação. Isso permite que os elementos SVG sejam manipulados visualmente, incluindo rotação, dimensionamento, movimentação, inclinação ou tradução. 

### Extensões 

O Microsoft Edge agora oferece suporte à [API de notificação](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) que exibe notificações de extensões. Os desenvolvedores de extensão agora podem criar diferentes tipos de notificações (básico, lista, imagem etc.) que dão suporte à interação do usuário total. As notificações também são registradas automaticamente na central de ações. Acesse o [exemplo de notificações](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) sobre como usar essa API em sua extensão.

O EdgeHTML 17 agora também oferece suporte ao `Tabs.reload()` método como parte da classe API de guias padrão. Também novidade na atualização do Windows 10 de abril de 2018, os usuários agora podem optar por permitir que as extensões sejam executadas durante a navegação InPrivate.

Para obter mais detalhes sobre as atualizações de extensões nesta versão, vá até a postagem de blog [novos recursos para extensões na atualização de abril de 2018 do Windows 10](https://blogs.windows.com/msedgedev/2018/05/24/new-extension-features-april-2018-update-notifications-inprivate/).

### DevTools
Esta versão do DevTools vem de duas maneiras: como as ferramentas tradicionais no navegador ( `F12` ) para Microsoft Edge e a visualização como um aplicativo autônomo do [Windows 10](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) da Microsoft Store!

![Aplicativo DevTools Microsoft Edge](../../devtools-protocol/media/microsoft-edge-devtools.png) 

As ferramentas também foram atualizadas com vários recursos principais, incluindo suporte básico para [depuração remota](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) (por meio do nosso novo [protocolo devtools](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)), [recursos de depuração do PWA](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging), [Gerenciamento de cache do IndexedDB](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection), [encaixe vertical](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) e muito mais! Também continuamos o [esforço de refatoração](./edgehtml-16.md) geral ter começado o último lançamento como parte de investimentos contínuos em desempenho e confiabilidade.

Acesse [devtools na atualização mais recente do Windows 10 (EdgeHTML 17)](../../devtools-guide/whats-new/edgehtml-17.md) para obter mais detalhes.

### JavaScript

Com o EdgeHTML 17, o mecanismo de JavaScript do Chakra introduz melhorias de desempenho em várias áreas importantes:

**Espaço de memória mais enxuto**

 - (Re-) adiar a análise de [funções de seta](https://github.com/Microsoft/ChakraCore/pull/4105) e [métodos em literais de objeto](https://github.com/Microsoft/ChakraCore/pull/4136)
 - [Refatoração de código de bytes RegExp](https://github.com/Microsoft/ChakraCore/pull/3915)

**Internas de JavaScript mais rápidas**

 - [Digite o compartilhamento de Object. Create](https://github.com/Microsoft/ChakraCore/pull/3901)
 - [Cache embutido polimórfico para Object. Assign](https://github.com/Microsoft/ChakraCore/pull/3792)
 - [Otimizações JSON. Parse/stringify](https://github.com/Microsoft/ChakraCore/pull/4077)
 - [Regravar iteradores de matriz em JavaScript e mais rápido para... de](https://github.com/Microsoft/ChakraCore/pull/4095)

**Assembly da Web**

 - [Suporte Inling](https://github.com/Microsoft/ChakraCore/pull/3681) 

Confira [*desempenho aprimorado de JavaScript e Webassembly no EdgeHTML 17*](https://blogs.windows.com/msedgedev/2018/06/19/improved-javascript-webassembly-performance-edgehtml-17/#I4vzUJK2va54kSWl.97) para obter todos os detalhes.

### Elemento de mídia

EdgeHTML 17 inclui atualizações para o [HTMLMediaElement](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) , incluindo:
* O novo `preload` atributo no [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) elemento indica quais dados devem ser pré-carregados.
* A adição do [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId) método e da [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) propriedade permite que os desenvolvedores selecionem o dispositivo de saída de áudio. (**Observação**: isso ainda não está disponível no RTC)

### API de captura de mídia 
O Microsoft Edge agora oferece suporte à captura de tela no RTC por meio da [API de captura de mídia](https://w3c.github.io/mediacapture-screen-share/). Esse recurso permite que as páginas da Web capturem a saída do dispositivo de exibição de um usuário, geralmente usadas para transmitir uma área de trabalho para reuniões ou apresentações virtuais sem plugin

### Aplicativos Web progressivos
A partir de EdgeHTML 17, os funcionários de serviço e as notificações por push são habilitados por padrão (Saiba mais sobre esses recursos no trabalho do serviço de postagem de blog [: indo além da página](https://blogs.windows.com/msedgedev/2017/12/19/service-workers-going-beyond-page/). Isso conclui o conjunto de tecnologias (incluindo a rede de buscas e as APIs de cache e push) que estabelece a base técnica para aplicativos Web progressivos (PWAs) no Windows 10.

PWAs são simplesmente aplicativos Web que são [aprimorados progressivamente](https://en.wikipedia.org/wiki/Progressive_enhancement) com recursos de semelhantes a aplicativos nativos em plataformas de suporte e mecanismos de navegador, como instalação/inicialização da tela inicial, suporte offline e notificações por push. No Windows 10 com o mecanismo Microsoft Edge (EdgeHTML), PWAs Desfrute da vantagem adicional de ser executado independentemente da janela do navegador como aplicativos da [plataforma universal do Windows](https://docs.microsoft.com/windows/uwp/get-started/whats-a-uwp) .

Além do PWAs, os funcionários do serviço e a API do cache permitem que os desenvolvedores interceptem solicitações de rede e respondam do cache. Um site não precisa sequer ter sido um aplicativo Web de baixa aparência para aproveitar o cache do serviço de trabalho para o desempenho e a confiabilidade da carga de páginas tined, além da capacidade de oferecer uma experiência offline durante períodos sem conexão à Internet ou de baixa qualidade.  

Vá até nossos [aplicativos Web progressivos em documentos do Windows](../../progressive-web-apps-edgehtml/index.md) para saber mais sobre os funcionários do serviço e detalhes sobre o PWAs no Windows 10.

### Segurança da Web
EdgeHTML 17 introduz suporte para a integridade de subrecurso (SRI). A [integridade do subrecurso](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) é um recurso de integridade que permite que os navegadores verifiquem se os recursos buscados (por exemplo, imagens, scripts, fontes etc.) são entregues sem a manipulação inesperada. 

Adicione um `integrity` atributo contendo uma representação de hash criptográfico do recurso que você espera carregar na sua página da Web para um `<script>` `<link>` elemento ou, como o exemplo abaixo. Em seguida, o Microsoft Edge irá comparar o recurso solicitado com o hash definido no `integrity` atributo. Se eles não corresponderem, o Microsoft Edge não executará o recurso e retornará um erro à rede.

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```

Também novidade no EdgeHTML 17, o cabeçalho de solicitação [atualização-inseguro-solicitações](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) permite que os navegadores solicitem uma experiência de navegação segura. Esse cabeçalho informa ao servidor que o navegador dá suporte à atualização de solicitações inseguras e que o usuário deve ser redirecionado para uma versão segura do site, se disponível.

### Fontes variáveis
O suporte completo para fontes variáveis (incluindo [as configurações de variação de fonte](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) CSS e o [dimensionamento de fonte-óptico](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)) está disponível no EdgeHTML 17. As fontes variáveis permitem que os desenvolvedores obtenham a aparência de tipos de letra aparentemente diferentes com uma única fonte ajustando vários eixos – reduzindo a necessidade de vários arquivos de fonte e melhorando o desempenho.

Junte- [se a um expedição para saber mais sobre quais fontes variáveis fornecem desenvolvedores e designers da Web](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts/)e como usá-los em seu site. E leia mais sobre fontes variáveis na postagem de blog, [trazendo uma tipografia expressiva e com o Autoformato para o Microsoft Edge com fontes variáveis](https://blogs.windows.com/msedgedev/2018/03/13/bringing-expressive-performant-typography-to-microsoft-edge-with-variable-fonts/).

<iframe height='456' scrolling='no' title='Exemplos de tíquete de variáveis de onda' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulte os exemplos de tíquete de a variável de caneta <a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'> </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>

## Novas APIs no EdgeHTML 17

Aqui está a lista completa de novas APIs no EdgeHTML 17. Elas são listadas no formato [nome da interface]. [nome da API].

> [!NOTE] 
> Embora as seguintes APIs sejam expostas no DOM, o comportamento de ponta a ponta de alguns ainda pode estar em desenvolvimento. Consulte o [status da plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para obter a palavra oficial sobre o suporte ao recurso.

<iframe height='580' scrolling='no' title='Novas APIs no EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Veja a caneta <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> New APIs no EdgeHTML 17 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) em <a href='https://codepen.io'> CodePen </a> .</iframe>

> [!TIP]
> Fizemos [parcerias](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) com outros navegadores e a Comunidade da Web na adoção de [documentos da Web do MDN](https://developer.mozilla.org/) como local definitivo para a documentação útil, não polarizada e independente de navegador para as tecnologias da Web atuais e emergentes baseados em padrões. Você pode encontrar detalhes sobre o suporte à API do EdgeHTML diretamente em cada página da [biblioteca MDN Web Reference](https://developer.mozilla.org/docs/Web). Visite o status da [plataforma](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) do Microsoft Edge para obter os recursos mais recentes com suporte no Microsoft Edge. 

## Versões anteriores do EdgeHTML

[EdgeHTML 13/Build do Windows 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Build do Windows 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Build do Windows 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

[EdgeHTML 16/Build do Windows 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)
