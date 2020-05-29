---
title: Mapear código pré-processado para código-fonte
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: b48c67584b3f3253ada99e32c5dabfdccb2fa4de
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581793"
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





# <span data-ttu-id="d60f5-103">Mapear código pré-processado para código-fonte</span><span class="sxs-lookup"><span data-stu-id="d60f5-103">Map Preprocessed Code to Source Code</span></span>   




<span data-ttu-id="d60f5-104">Mantenha o código do lado do cliente legível e debuggable, mesmo depois de combinar, Minify ou compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="d60f5-104">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="d60f5-105">Use mapas de origem para mapear o código-fonte para o código compilado.</span><span class="sxs-lookup"><span data-stu-id="d60f5-105">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="d60f5-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="d60f5-106">Summary</span></span>  

*   <span data-ttu-id="d60f5-107">Use mapas de origem para mapear o código minified para o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="d60f5-107">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="d60f5-108">Em seguida, você pode ler e depurar o código compilado na fonte original.</span><span class="sxs-lookup"><span data-stu-id="d60f5-108">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="d60f5-109">Use pré-processadores que sejam capazes de produzir mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="d60f5-109">Only use preprocessors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="d60f5-110">Verifique se o servidor Web é capaz de servir mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="d60f5-110">Verify that your web server is able to serve Source Maps.</span></span>  

<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="d60f5-111">Introdução aos pré-processadores</span><span class="sxs-lookup"><span data-stu-id="d60f5-111">Get started with preprocessors</span></span>  

<span data-ttu-id="d60f5-112">Este artigo explica como interagir com mapas de origem JavaScript no painel DevTools fontes.</span><span class="sxs-lookup"><span data-stu-id="d60f5-112">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="d60f5-113">Usar um pré-processador compatível</span><span class="sxs-lookup"><span data-stu-id="d60f5-113">Use a supported preprocessor</span></span>  

<span data-ttu-id="d60f5-114">Você precisa usar um Minifier que seja capaz de criar mapas de origem.</span><span class="sxs-lookup"><span data-stu-id="d60f5-114">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="d60f5-115">Para uma exibição estendida, consulte a página [mapas de origem: idiomas, ferramentas e outras informações][GitHubWikiSourceMapsLanguagesTools] wiki.</span><span class="sxs-lookup"><span data-stu-id="d60f5-115">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="d60f5-116">Os seguintes tipos de pré-processadores geralmente são usados em combinação com mapas de origem:</span><span class="sxs-lookup"><span data-stu-id="d60f5-116">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="d60f5-117">Transcompilers \ ([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="d60f5-117">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="d60f5-118">Compiladores \ ([compilador de fechamento][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="d60f5-118">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="d60f5-119">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="d60f5-119">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  

## <span data-ttu-id="d60f5-120">Mapas de origem no painel fontes do DevTools</span><span class="sxs-lookup"><span data-stu-id="d60f5-120">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="d60f5-121">Mapas de origem de pré-processadors fazem com que o DevTools carregue seus arquivos originais, além de seus minified.</span><span class="sxs-lookup"><span data-stu-id="d60f5-121">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="d60f5-122">Em seguida, use os originais para definir pontos de interrupção e percorrer o código.</span><span class="sxs-lookup"><span data-stu-id="d60f5-122">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="d60f5-123">Enquanto isso, o Microsoft Edge está realmente executando o código minified.</span><span class="sxs-lookup"><span data-stu-id="d60f5-123">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="d60f5-124">Isso lhe dá a ilusão de executar um site de desenvolvimento em produção.</span><span class="sxs-lookup"><span data-stu-id="d60f5-124">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="d60f5-125">Ao executar mapas de origem no DevTools, você deve observar que o JavaScript não é compilado e você pode ver todos os arquivos JavaScript individuais referenciados.</span><span class="sxs-lookup"><span data-stu-id="d60f5-125">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="d60f5-126">Isso é usando o mapeamento de origem, mas, em realidade, os bastidores executam o código compilado.</span><span class="sxs-lookup"><span data-stu-id="d60f5-126">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="d60f5-127">Todos os erros, logs e pontos de interrupção são mapeados para o código de desenvolvimento para a depuração de awesome!</span><span class="sxs-lookup"><span data-stu-id="d60f5-127">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="d60f5-128">Então, em vigor, ele dá a você a ilusão de que você está executando um site de desenvolvimento em produção.</span><span class="sxs-lookup"><span data-stu-id="d60f5-128">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="d60f5-129">Habilitar mapas de origem em configurações</span><span class="sxs-lookup"><span data-stu-id="d60f5-129">Enable Source Maps in settings</span></span>  

<span data-ttu-id="d60f5-130">Os mapas de origem são habilitados por padrão</span><span class="sxs-lookup"><span data-stu-id="d60f5-130">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="d60f5-131">, mas se você quiser verificá-los ou habilitá-los, clique duas vezes. Primeiro, abra o DevTools, clique no botão **Personalizar e controlar devtools** `...` e selecione **configurações**.</span><span class="sxs-lookup"><span data-stu-id="d60f5-131">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** `...` button, and select **Settings**.</span></span>  <span data-ttu-id="d60f5-132">No painel **preferências** , em **fontes**, marque **habilitar mapas de origem JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="d60f5-132">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="d60f5-133">Você também pode marcar **habilitar mapas de código-fonte CSS**.</span><span class="sxs-lookup"><span data-stu-id="d60f5-133">You may also check **Enable CSS Source Maps**.</span></span>  

> ##### <span data-ttu-id="d60f5-134">Figura 1</span><span class="sxs-lookup"><span data-stu-id="d60f5-134">Figure 1</span></span>  
> <span data-ttu-id="d60f5-135">Habilitar mapas de origem</span><span class="sxs-lookup"><span data-stu-id="d60f5-135">Enable Source Maps</span></span>  
> ![Habilitar mapas de origem][ImageSourceMaps]  

### <span data-ttu-id="d60f5-137">Depuração com mapas de origem</span><span class="sxs-lookup"><span data-stu-id="d60f5-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="d60f5-138">Ao depurar seus mapas de código e de origem habilitados, os mapas de origem são exibidos em dois locais:</span><span class="sxs-lookup"><span data-stu-id="d60f5-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="d60f5-139">No console \ (o link para a origem deve ser o arquivo original, não o um \ gerado)</span><span class="sxs-lookup"><span data-stu-id="d60f5-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="d60f5-140">Quando percorrendo o código \ (os links na pilha de chamadas devem abrir o arquivo de origem original \)</span><span class="sxs-lookup"><span data-stu-id="d60f5-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  

<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## <span data-ttu-id="d60f5-141">@sourceURL e displayName</span><span class="sxs-lookup"><span data-stu-id="d60f5-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="d60f5-142">Embora não faça parte da especificação do mapa de origem, o `@sourceURL` permite que você torne o desenvolvimento muito mais fácil ao trabalhar com evals.</span><span class="sxs-lookup"><span data-stu-id="d60f5-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="d60f5-143">Esse auxiliar é muito semelhante à `//# sourceMappingURL` propriedade e, na verdade, é mencionado nas especificações do mapa de fontes v3.</span><span class="sxs-lookup"><span data-stu-id="d60f5-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="d60f5-144">Ao incluir o seguinte comentário especial em seu código, que é proparado, você pode nomear avaliações e scripts e estilos embutidos para que cada um deles seja exibido como mais nomes lógicos em seu DevTools.</span><span class="sxs-lookup"><span data-stu-id="d60f5-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="d60f5-145">Navegue até a página a seguir.</span><span class="sxs-lookup"><span data-stu-id="d60f5-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="d60f5-146">demonstração</span><span class="sxs-lookup"><span data-stu-id="d60f5-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="d60f5-147">Siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="d60f5-147">Follow these steps.</span></span>  

1.  <span data-ttu-id="d60f5-148">Abra o DevTools e vá para o painel **fontes** .</span><span class="sxs-lookup"><span data-stu-id="d60f5-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="d60f5-149">Insira um nome de arquivo no campo **_nome do seu código:_** entrada.</span><span class="sxs-lookup"><span data-stu-id="d60f5-149">Enter in a filename into the **_Name your code:_** input field.</span></span>  
1.  <span data-ttu-id="d60f5-150">Clique no botão **Compilar** .</span><span class="sxs-lookup"><span data-stu-id="d60f5-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="d60f5-151">Um alerta é exibido com a soma avaliada da fonte CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="d60f5-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  

<span data-ttu-id="d60f5-152">Se você expandir o Subpainel **_fontes_** , agora verá um novo arquivo com o nome de arquivo personalizado que você digitou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d60f5-152">If you expand the **_Sources_** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="d60f5-153">Se você clicar duas vezes para exibir esse arquivo, ele contém o JavaScript compilado para a fonte original.</span><span class="sxs-lookup"><span data-stu-id="d60f5-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="d60f5-154">Na última linha, no entanto, é um `// @sourceURL` comentário que indica o arquivo de origem original.</span><span class="sxs-lookup"><span data-stu-id="d60f5-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="d60f5-155">Isso pode ajudá-lo com a depuração enquanto trabalha com abstrações de idioma.</span><span class="sxs-lookup"><span data-stu-id="d60f5-155">This may help you with debugging while working with language abstractions.</span></span>  

> ##### <span data-ttu-id="d60f5-156">Figura 2</span><span class="sxs-lookup"><span data-stu-id="d60f5-156">Figure 2</span></span>
> <span data-ttu-id="d60f5-157">Trabalhando com sourceURL</span><span class="sxs-lookup"><span data-stu-id="d60f5-157">Working with sourceURL</span></span>  
> ![Trabalhando com sourceURL][ImageCoffeeScript]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageSourceMaps]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png "Figura 1: habilitar mapas de origem"  
[ImageCoffeeScript]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-coffeeeeeeee.msft.png "Figura 2: trabalhando com sourceURL"  

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
> <span data-ttu-id="d60f5-170">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="d60f5-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d60f5-171">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) e é criada por [Meggin Kearney][MegginKearney] \ (Tech Writer \) e [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor, Google: ferramentas, desempenho, animação e UX \).</span><span class="sxs-lookup"><span data-stu-id="d60f5-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d60f5-173">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d60f5-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
