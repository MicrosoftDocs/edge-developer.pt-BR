---
description: Mantenha seu código do lado do cliente acessível e depurável mesmo depois de combiná-lo, minificá-lo ou compilá-lo.
title: Mapear código pré-processador para código-fonte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c04d1ec02b188cc7ec8ab2598b395dbeb4431c46
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519412"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="map-preprocessed-code-to-source-code"></a>Mapear código pré-processador para código-fonte  

Mantenha seu código do lado do cliente acessível e depurável mesmo depois de combiná-lo, minificá-lo ou compilá-lo.  Use mapas de origem para mapear seu código-fonte para o código compilado.  

### <a name="summary"></a>Resumo  

*   Use Mapas de origem para mapear código minificado para código-fonte.  Em seguida, você pode ler e depurar código compilado na origem original.  
*   Use somente pré-processadores capazes de produzir Mapas de origem.  
*   Verifique se o servidor Web é capaz de servir Mapas de Origem.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a>Começar com pré-processadores  

Este artigo explica como interagir com mapas de origem javascript na ferramenta DevTools Sources.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a>Usar um pré-processador com suporte  

Use um minifier capaz de criar mapas de origem.  <!--For the most popular options, navigate to preprocessor support section.  -->  Para uma exibição estendida, navegue até [Mapas de origem: idiomas, ferramentas e outras informações][GitHubWikiSourceMapsLanguagesTools] wiki.  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Os seguintes tipos de pré-processadores são comumente usados em combinação com mapas de origem:  

*   Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiladores \([Compilador de Fechamento,][GitHubGoogleClosureCompiler] [TypeScript,][|::ref1::|Main] [CoffeeScript,][|::ref2::|Main] [Dardos][DartMain]\)  
*   Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)  
    
## <a name="source-maps-in-devtools-sources-tool"></a>Mapas de origem na ferramenta DevTools Sources  

Mapas de origem de pré-processadores causam o DevTools carregar seus arquivos originais, além dos seus minificados.  Em seguida, use os originais para definir pontos de interrupção e passar o código.  Enquanto isso, o Microsoft Edge está realmente executando seu código minificado.  A execução do código oferece a ilusão de executar um site de desenvolvimento em produção.  

Ao executar mapas de origem no DevTools, você deve observar que o JavaScript não é compilado e todos os arquivos JavaScript individuais que ele faz referência são exibidos.  Mapas de origem no DevTools está usando mapeamento de origem, mas a funcionalidade subjacente realmente executa o código compilado.  Quaisquer erros, logs e pontos de interrupção mapeiam para o código de dev para depuração incrível.  Portanto, na verdade, ele dá a você a ilusão de que você está executando um site de dev em produção.  

### <a name="enable-source-maps-in-settings"></a>Habilitar mapas de origem nas configurações  

Mapas de origem são habilitados por padrão<!-- \(as of Microsoft Edge 39\)-->, mas se você quiser verificar duas vezes ou habilita-los; primeiro abra DevTools, escolha **Personalizar e controlar DevTools** \( `...` \) > **Configurações**.  No painel **Preferências,** em **Fontes**, ative **Habilitar Mapas de Origem JavaScript.**  Você também pode ativar o **Enable CSS Source Maps**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar mapas de origem" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Habilitar mapas de origem javascript**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a>Depuração com mapas de origem  

Ao depurar seu código e mapas de origem habilitados, os Mapas de Origem mostram em dois locais:  

1.  No console \(o link para a origem deve ser o arquivo original, não o gerado\)  
1.  Ao passar pelo código \(os links na pilha de chamada devem abrir o arquivo de origem original\)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a>@sourceURL e displayName  

Embora não faça parte da especificação mapa de origem, o permite tornar o desenvolvimento muito mais `@sourceURL` fácil ao trabalhar com evals.  O auxiliar é exibido de forma semelhante à `//# sourceMappingURL` propriedade e é mencionado nas especificações do Mapa de Origem V3.  

Ao incluir o seguinte comentário especial em seu código, que é evadida, você pode nomear evals e scripts e estilos em linha para que cada um apareça como nomes mais lógicos em seu DevTools.  

```javascript
//# sourceURL=source.coffee
```  

Navegue até a página a seguir.  

*   [demonstração][CssNinjaDemoSourceMapping]

Conclua as seguintes ações.  

1.  Abra DevTools e navegue até a **ferramenta Sources.**  
1.  Insira um nome de arquivo no **campo Nome do código:** entrada.  
1.  Escolha o **botão compilar.**  
1.  Um alerta é exibido, mostrando a soma avaliada da fonte CoffeeScript.  
    
Se você expandir o sub-painel **Fontes,** agora exibirá um novo arquivo com o nome de arquivo personalizado inserido anteriormente.  Se você clicar duas vezes para exibir esse arquivo, ele conterá o JavaScript compilado para a origem original.  Na última linha, no entanto, há um `// @sourceURL` comentário indicando o arquivo de origem original.  Isso pode ajudá-lo com a depuração durante o trabalho com abstrações de idioma.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Trabalhar com sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Trabalhar com `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Entrar em contato com a equipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "O Babel é um compilador JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Um exemplo simples de nomeação de eval //# sourceURL"  

[DartMain]: https://www.dartlang.org "Linguagem de programação de dardos"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "google/closure-compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Mapas de origem: idiomas, ferramentas e outras informações | Wiki do GitHub"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Getting Started - google/traceur-compiler | Wiki do GitHub"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) é encontrada aqui e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Paulo Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation e UX\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
