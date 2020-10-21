---
description: Mantenha o código do lado do cliente legível e debuggable, mesmo depois de combinar, Minify ou compilá-lo.
title: Mapear Código em Pré-processamento para Código-fonte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: c16f59658217ab9dfb905bd814f96af21f95130d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124675"
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

# Mapear código pré-processado para código-fonte  

Mantenha o código do lado do cliente legível e debuggable, mesmo depois de combinar, Minify ou compilá-lo.  Use mapas de origem para mapear o código-fonte para o código compilado.  

### Resumo  

*   Use mapas de origem para mapear o código minified para o código-fonte. Em seguida, você pode ler e depurar o código compilado na fonte original.  
*   Use apenas processadores que sejam capazes de produzir mapas de origem.  
*   Verifique se o servidor Web é capaz de servir mapas de origem.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## Introdução aos pré-processadores  

Este artigo explica como interagir com mapas de origem JavaScript no painel DevTools fontes.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## Usar um pré-processador compatível  

Você precisa usar um Minifier que seja capaz de criar mapas de origem.  <!--For the most popular options, navigate to preprocessor support section.  -->  Para um modo de exibição estendido, navegue até [mapas de origem: idiomas, ferramentas e outras informações][GitHubWikiSourceMapsLanguagesTools] wiki.  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Os seguintes tipos de pré-processadores geralmente são usados em combinação com mapas de origem:  

*   Transcompilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiladores \ ([compilador de fechamento][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)  
*   Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)  
    
## Mapas de origem no painel fontes do DevTools  

Mapas de origem de pré-processadors fazem com que o DevTools carregue seus arquivos originais, além de seus minified.  Em seguida, use os originais para definir pontos de interrupção e percorrer o código.  Enquanto isso, o Microsoft Edge está realmente executando o código minified. Isso lhe dá a ilusão de executar um site de desenvolvimento em produção.  

Ao executar mapas de origem no DevTools, você deve observar que o JavaScript não é compilado e você pode ver todos os arquivos JavaScript individuais referenciados.  Isso é usando o mapeamento de origem, mas, em realidade, os bastidores executam o código compilado.  Todos os erros, logs e pontos de interrupção são mapeados para o código de desenvolvimento para a depuração de awesome!  Então, em vigor, ele dá a você a ilusão de que você está executando um site de desenvolvimento em produção.  

### Habilitar mapas de origem em configurações  

Os mapas de origem são habilitados por padrão <!--\(as of Microsoft Edge 39\)-->, mas se você quiser verificá-los ou habilitá-los, clique duas vezes. Primeiro, abra o DevTools, clique no botão **Personalizar e controlar devtools** \ ( `...` \) e escolha **configurações**.  No painel **preferências** , em **fontes**, marque **habilitar mapas de origem JavaScript**.  Você também pode marcar **habilitar mapas de código-fonte CSS**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar mapas de origem" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Habilitar mapas de origem JavaScript**  
:::image-end:::  

### Depuração com mapas de origem  

Ao depurar seus mapas de código e de origem habilitados, os mapas de origem são exibidos em dois locais:  

1.  No console \ (o link para a origem deve ser o arquivo original, não o um \ gerado)  
1.  Quando percorrendo o código \ (os links na pilha de chamadas devem abrir o arquivo de origem original \)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## @sourceURL e displayName  

Embora não faça parte da especificação do mapa de origem, o `@sourceURL` permite que você torne o desenvolvimento muito mais fácil ao trabalhar com evals.  Esse auxiliar é muito semelhante à `//# sourceMappingURL` propriedade e, na verdade, é mencionado nas especificações do mapa de fontes v3.  

Ao incluir o seguinte comentário especial em seu código, que é proparado, você pode nomear avaliações e scripts e estilos embutidos para que cada um deles seja exibido como mais nomes lógicos em seu DevTools.  

```javascript
//# sourceURL=source.coffee
```  

Navegue até a página a seguir.  

*   [demonstração][CssNinjaDemoSourceMapping]

Conclua as ações a seguir.  

1.  Abra o DevTools e vá para o painel **fontes** .  
1.  Insira um nome de arquivo no campo **nome do seu código:** entrada.  
1.  Clique no botão **Compilar** .  
1.  Um alerta é exibido com a soma avaliada da fonte CoffeeScript.  
    
Se você expandir o Subpainel **fontes** , agora verá um novo arquivo com o nome de arquivo personalizado que você digitou anteriormente.  Se você clicar duas vezes para exibir esse arquivo, ele contém o JavaScript compilado para a fonte original.  Na última linha, no entanto, é um `// @sourceURL` comentário que indica o arquivo de origem original.  Isso pode ajudá-lo com a depuração enquanto trabalha com abstrações de idioma.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Habilitar mapas de origem" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Trabalhar com `sourceURL`  
:::image-end:::  

## Entrar em contato com a equipe Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel é um compilador JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Um exemplo simples de nomenclatura de eval//# sourceURL"  

[DartMain]: https://www.dartlang.org "Linguagem de programação DART"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/fechamento-compilador | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Mapas de origem: idiomas, ferramentas e outras informações | Wiki do GitHub"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Introdução-Google/Traceur-Compiler | Wiki do GitHub"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.  
> A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor, Google: ferramentas, desempenho, animação e UX \).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
