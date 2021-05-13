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
# <a name="map-preprocessed-code-to-source-code"></a><span data-ttu-id="8613f-104">Mapear código pré-processador para código-fonte</span><span class="sxs-lookup"><span data-stu-id="8613f-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="8613f-105">Mantenha seu código do lado do cliente acessível e depurável mesmo depois de combiná-lo, minificá-lo ou compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="8613f-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="8613f-106">Use mapas de origem para mapear seu código-fonte para o código compilado.</span><span class="sxs-lookup"><span data-stu-id="8613f-106">Use source maps to map your source code to your compiled code.</span></span>  

### <a name="summary"></a><span data-ttu-id="8613f-107">Resumo</span><span class="sxs-lookup"><span data-stu-id="8613f-107">Summary</span></span>  

*   <span data-ttu-id="8613f-108">Use Source Mapas para mapear o código minificado para o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="8613f-108">Use Source Maps to map minified code to source code.</span></span>  <span data-ttu-id="8613f-109">Em seguida, você pode ler e depurar código compilado na origem original.</span><span class="sxs-lookup"><span data-stu-id="8613f-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="8613f-110">Use somente pré-processadores capazes de produzir o source Mapas.</span><span class="sxs-lookup"><span data-stu-id="8613f-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="8613f-111">Verifique se o servidor Web é capaz de servir o Source Mapas.</span><span class="sxs-lookup"><span data-stu-id="8613f-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a><span data-ttu-id="8613f-112">Começar com pré-processadores</span><span class="sxs-lookup"><span data-stu-id="8613f-112">Get started with preprocessors</span></span>  

<span data-ttu-id="8613f-113">Este artigo explica como interagir com o JavaScript Source Mapas na ferramenta DevTools Sources.</span><span class="sxs-lookup"><span data-stu-id="8613f-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources tool.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a><span data-ttu-id="8613f-114">Usar um pré-processador com suporte</span><span class="sxs-lookup"><span data-stu-id="8613f-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="8613f-115">Use um minifier capaz de criar mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="8613f-115">Use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, navigate to preprocessor support section.  -->  <span data-ttu-id="8613f-116">Para uma exibição estendida, navegue até [Mapas de origem: idiomas, ferramentas e outras informações][GitHubWikiSourceMapsLanguagesTools] wiki.</span><span class="sxs-lookup"><span data-stu-id="8613f-116">For an extended view, navigate to [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="8613f-117">Os seguintes tipos de pré-processadores são comumente usados em combinação com o source Mapas:</span><span class="sxs-lookup"><span data-stu-id="8613f-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="8613f-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="8613f-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="8613f-119">Compiladores \([Compilador de Fechamento,][GitHubGoogleClosureCompiler] [TypeScript,][|::ref1::|Main] [CoffeeScript,][|::ref2::|Main] [Dardos][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="8613f-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="8613f-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="8613f-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <a name="source-maps-in-devtools-sources-tool"></a><span data-ttu-id="8613f-121">Fonte Mapas ferramenta Fontes do DevTools</span><span class="sxs-lookup"><span data-stu-id="8613f-121">Source Maps in DevTools Sources tool</span></span>  

<span data-ttu-id="8613f-122">A Mapas de pré-processadores causa a carga dos arquivos originais do DevTools, além dos minificados.</span><span class="sxs-lookup"><span data-stu-id="8613f-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="8613f-123">Em seguida, use os originais para definir pontos de interrupção e passar o código.</span><span class="sxs-lookup"><span data-stu-id="8613f-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="8613f-124">Enquanto isso, Microsoft Edge está executando seu código minificado.</span><span class="sxs-lookup"><span data-stu-id="8613f-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  <span data-ttu-id="8613f-125">A execução do código oferece a ilusão de executar um site de desenvolvimento em produção.</span><span class="sxs-lookup"><span data-stu-id="8613f-125">The running of the code gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="8613f-126">Ao executar o source Mapas no DevTools, você deve observar que o JavaScript não é compilado e todos os arquivos JavaScript individuais que ele faz referência são exibidos.</span><span class="sxs-lookup"><span data-stu-id="8613f-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and all of the individual JavaScript files it references are displayed.</span></span>  <span data-ttu-id="8613f-127">A Mapas de origem no DevTools está usando o mapeamento de origem, mas a funcionalidade subjacente realmente executa o código compilado.</span><span class="sxs-lookup"><span data-stu-id="8613f-127">Source Maps in DevTools is using source mapping, but the underlying functionality actually runs the compiled code.</span></span>  <span data-ttu-id="8613f-128">Quaisquer erros, logs e pontos de interrupção mapeiam para o código de dev para depuração incrível.</span><span class="sxs-lookup"><span data-stu-id="8613f-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging.</span></span>  <span data-ttu-id="8613f-129">Portanto, na verdade, ele dá a você a ilusão de que você está executando um site de dev em produção.</span><span class="sxs-lookup"><span data-stu-id="8613f-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <a name="enable-source-maps-in-settings"></a><span data-ttu-id="8613f-130">Habilitar o Mapas de origem nas configurações</span><span class="sxs-lookup"><span data-stu-id="8613f-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="8613f-131">As Mapas de origem estão habilitadas por padrão</span><span class="sxs-lookup"><span data-stu-id="8613f-131">Source Maps are enabled by default</span></span><!-- \(as of Microsoft Edge 39\)--><span data-ttu-id="8613f-132">, mas se você quiser verificar duas vezes ou habilita-los; primeiro abra DevTools, escolha **Personalizar e controlar o DevTools** \( `...` \) > **Configurações**.</span><span class="sxs-lookup"><span data-stu-id="8613f-132">, but if you want to double-check or enable them; first open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="8613f-133">No painel **Preferências,** em **Fontes**, ative **Habilitar o código-fonte javascript Mapas**.</span><span class="sxs-lookup"><span data-stu-id="8613f-133">On the **Preferences** pane, under **Sources**, turn on **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="8613f-134">Você também pode ativar o **recurso Habilitar o código-fonte CSS Mapas**.</span><span class="sxs-lookup"><span data-stu-id="8613f-134">You may also turn on the **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar o Mapas" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="8613f-136">Habilitar o código-fonte javascript Mapas</span><span class="sxs-lookup"><span data-stu-id="8613f-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a><span data-ttu-id="8613f-137">Depuração com a fonte Mapas</span><span class="sxs-lookup"><span data-stu-id="8613f-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="8613f-138">Ao depurar o código e a Mapas habilitada, o source Mapas mostrar em dois locais:</span><span class="sxs-lookup"><span data-stu-id="8613f-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="8613f-139">No console \(o link para a origem deve ser o arquivo original, não o gerado\)</span><span class="sxs-lookup"><span data-stu-id="8613f-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="8613f-140">Ao passar pelo código \(os links na pilha de chamada devem abrir o arquivo de origem original\)</span><span class="sxs-lookup"><span data-stu-id="8613f-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a><span data-ttu-id="8613f-141">@sourceURL e displayName</span><span class="sxs-lookup"><span data-stu-id="8613f-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="8613f-142">Embora não faça parte da especificação mapa de origem, o permite tornar o desenvolvimento muito mais `@sourceURL` fácil ao trabalhar com evals.</span><span class="sxs-lookup"><span data-stu-id="8613f-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="8613f-143">O auxiliar é exibido de forma semelhante à `//# sourceMappingURL` propriedade e é mencionado nas especificações do Mapa de Origem V3.</span><span class="sxs-lookup"><span data-stu-id="8613f-143">The helper is displayed similar to the `//# sourceMappingURL` property and is mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="8613f-144">Ao incluir o seguinte comentário especial em seu código, que é evadida, você pode nomear evals e scripts e estilos em linha para que cada um apareça como nomes mais lógicos em seu DevTools.</span><span class="sxs-lookup"><span data-stu-id="8613f-144">By including the following special comment in your code, which is evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="8613f-145">Navegue até a página a seguir.</span><span class="sxs-lookup"><span data-stu-id="8613f-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="8613f-146">demonstração</span><span class="sxs-lookup"><span data-stu-id="8613f-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="8613f-147">Conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="8613f-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="8613f-148">Abra DevTools e navegue até a **ferramenta Sources.**</span><span class="sxs-lookup"><span data-stu-id="8613f-148">Open DevTools and navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="8613f-149">Insira um nome de arquivo no **campo Nome do código:** entrada.</span><span class="sxs-lookup"><span data-stu-id="8613f-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="8613f-150">Escolha o **botão compilar.**</span><span class="sxs-lookup"><span data-stu-id="8613f-150">Choose the **compile** button.</span></span>  
1.  <span data-ttu-id="8613f-151">Um alerta é exibido, mostrando a soma avaliada da fonte CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="8613f-151">An alert appears, showing the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="8613f-152">Se você expandir o sub-painel **Fontes,** agora exibirá um novo arquivo com o nome de arquivo personalizado inserido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8613f-152">If you expand the **Sources** sub-panel you now display a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="8613f-153">Se você clicar duas vezes para exibir esse arquivo, ele conterá o JavaScript compilado para a origem original.</span><span class="sxs-lookup"><span data-stu-id="8613f-153">If you double-click to view this file, it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="8613f-154">Na última linha, no entanto, há um `// @sourceURL` comentário indicando o arquivo de origem original.</span><span class="sxs-lookup"><span data-stu-id="8613f-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="8613f-155">Isso pode ajudá-lo com a depuração durante o trabalho com abstrações de idioma.</span><span class="sxs-lookup"><span data-stu-id="8613f-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Trabalhar com sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="8613f-157">Trabalhar com</span><span class="sxs-lookup"><span data-stu-id="8613f-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8613f-158">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8613f-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

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
> <span data-ttu-id="8613f-168">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8613f-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8613f-169">A página original [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) é encontrada aqui e é de autoria de [Meggin Kearney][MegginKearney] \(Tech Writer\) e [Paulo Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation e UX\).</span><span class="sxs-lookup"><span data-stu-id="8613f-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8613f-171">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8613f-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
