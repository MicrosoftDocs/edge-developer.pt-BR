---
description: Mantenha seu código do lado do cliente acessível e depurável mesmo depois de combiná-lo, minificá-lo ou compilá-lo.
title: Mapear código pré-processador para código-fonte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 3240e437a917dd7074a0584b91dcc6c34576ca24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564046"
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

*   Use Source Mapas para mapear o código minificado para o código-fonte.  Em seguida, você pode ler e depurar código compilado na origem original.  
*   Use somente pré-processadores capazes de produzir o source Mapas.  
*   Verifique se o servidor Web é capaz de servir o Source Mapas.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a>Começar com pré-processadores  

Este artigo explica como interagir com o JavaScript Source Mapas na ferramenta DevTools Sources.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a>Usar um pré-processador com suporte  

Use um minifier capaz de criar mapas de origem.  <!--For the most popular options, navigate to preprocessor support section.  -->  Para uma exibição estendida, navegue até [Mapas de origem: idiomas, ferramentas e outras informações][GitHubWikiSourceMapsLanguagesTools] wiki.  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Os seguintes tipos de pré-processadores são comumente usados em combinação com o source Mapas:  

*   Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiladores \([Compilador de Fechamento,][GitHubGoogleClosureCompiler] [TypeScript,][|::ref1::|Main] [CoffeeScript,][|::ref2::|Main] [Dardos][DartMain]\)  
*   Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)  
    
## <a name="source-maps-in-devtools-sources-tool"></a>Fonte Mapas ferramenta Fontes do DevTools  

A Mapas de pré-processadores causa a carga dos arquivos originais do DevTools, além dos minificados.  Em seguida, use os originais para definir pontos de interrupção e passar o código.  Enquanto isso, Microsoft Edge está executando seu código minificado.  A execução do código oferece a ilusão de executar um site de desenvolvimento em produção.  

Ao executar o source Mapas no DevTools, você deve observar que o JavaScript não é compilado e todos os arquivos JavaScript individuais que ele faz referência são exibidos.  A Mapas de origem no DevTools está usando o mapeamento de origem, mas a funcionalidade subjacente realmente executa o código compilado.  Quaisquer erros, logs e pontos de interrupção mapeiam para o código de dev para depuração incrível.  Portanto, na verdade, ele dá a você a ilusão de que você está executando um site de dev em produção.  

### <a name="enable-source-maps-in-settings"></a>Habilitar o Mapas de origem nas configurações  

As Mapas de origem estão habilitadas por padrão<!-- \(as of Microsoft Edge 39\)-->, mas se você quiser verificar duas vezes ou habilita-los; primeiro abra DevTools, escolha **Personalizar e controlar o DevTools** \( `...` \) > **Configurações**.  No painel **Preferências,** em **Fontes**, ative **Habilitar o código-fonte javascript Mapas**.  Você também pode ativar o **recurso Habilitar o código-fonte CSS Mapas**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar o Mapas" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Habilitar o código-fonte javascript Mapas**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a>Depuração com a fonte Mapas  

Ao depurar o código e a Mapas habilitada, o source Mapas mostrar em dois locais:  

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

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Mapas de origem: idiomas, ferramentas e outras informações | GitHub wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Getting Started - google/traceur-compiler | GitHub wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) é encontrada aqui e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Paulo Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation e UX\).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
