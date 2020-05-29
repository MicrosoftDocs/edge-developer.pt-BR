---
title: Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento na Web, Ferramentas F12, devtools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601716"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="29c97-103">Localizar código JavaScript e CSS não usados com a guia cobertura no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="29c97-103">Find Unused JavaScript And CSS Code With The Coverage Tab In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="29c97-104">A guia cobertura no Microsoft Edge DevTools ajuda você a localizar código JavaScript e CSS não utilizados.</span><span class="sxs-lookup"><span data-stu-id="29c97-104">The Coverage tab in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="29c97-105">A remoção de um código não usado pode acelerar a carga da página e salvar os dados da rede celular dos seus usuários móveis.</span><span class="sxs-lookup"><span data-stu-id="29c97-105">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

> ##### <span data-ttu-id="29c97-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="29c97-106">Figure 1</span></span>  
> <span data-ttu-id="29c97-107">Analisando cobertura de código</span><span class="sxs-lookup"><span data-stu-id="29c97-107">Analyzing code coverage</span></span>  
> ![Analisando cobertura de código][ImageExample]  

> [!WARNING]
> <span data-ttu-id="29c97-109">Localizar código não usado é relativamente fácil.</span><span class="sxs-lookup"><span data-stu-id="29c97-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="29c97-110">Mas refatorar uma codebase para que cada página só entregue o JavaScript e o CSS necessários, pode ser difícil.</span><span class="sxs-lookup"><span data-stu-id="29c97-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="29c97-111">Este guia não aborda como refatorar uma codebase para evitar código não usado, pois esses refactores dependem muito do seu conjunto de tecnologias.</span><span class="sxs-lookup"><span data-stu-id="29c97-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <span data-ttu-id="29c97-112">Visão geral</span><span class="sxs-lookup"><span data-stu-id="29c97-112">Overview</span></span>   

<span data-ttu-id="29c97-113">O envio de JavaScript ou CSS não usado é um problema comum no desenvolvimento na Web.</span><span class="sxs-lookup"><span data-stu-id="29c97-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="29c97-114">Por exemplo, suponha que você queira usar o [componente botão Bootstrap][BootstrapButtons] na página.</span><span class="sxs-lookup"><span data-stu-id="29c97-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="29c97-115">Para usar o componente Button, você precisa adicionar um link para a folha de estilo Bootstrap em seu HTML, assim:</span><span class="sxs-lookup"><span data-stu-id="29c97-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="29c97-116">Essa folha de estilos não inclui apenas o código do componente Button.</span><span class="sxs-lookup"><span data-stu-id="29c97-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="29c97-117">Ele contém a CSS para **todos** os componentes de bootstrap.</span><span class="sxs-lookup"><span data-stu-id="29c97-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="29c97-118">Mas você não está usando nenhum dos outros componentes de inicialização.</span><span class="sxs-lookup"><span data-stu-id="29c97-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="29c97-119">Portanto, sua página está baixando um grupo de CSS que não precisa.</span><span class="sxs-lookup"><span data-stu-id="29c97-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="29c97-120">Essa CSS extra é um problema pelos motivos a seguir.</span><span class="sxs-lookup"><span data-stu-id="29c97-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="29c97-121">O código extra reduz a carga da página.</span><span class="sxs-lookup"><span data-stu-id="29c97-121">The extra code slows down your page load.</span></span>  <!--See [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="29c97-122">Se um usuário acessar a página em um dispositivo móvel, o código adicional usará seus dados da rede celular.</span><span class="sxs-lookup"><span data-stu-id="29c97-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <span data-ttu-id="29c97-123">Abrir a guia cobertura</span><span class="sxs-lookup"><span data-stu-id="29c97-123">Open the Coverage tab</span></span>   

1.  <span data-ttu-id="29c97-124">[Abrir o menu de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="29c97-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="29c97-125">Comece `coverage` a digitar, selecione o comando **Mostrar cobertura** e pressione `Enter` para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="29c97-125">Start typing `coverage`, select the **Show Coverage** command, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="29c97-126">A guia **cobertura** é aberta na **gaveta**.</span><span class="sxs-lookup"><span data-stu-id="29c97-126">The **Coverage** tab opens in the **Drawer**.</span></span>  

    > ##### <span data-ttu-id="29c97-127">Figura 2</span><span class="sxs-lookup"><span data-stu-id="29c97-127">Figure 2</span></span>  
    > <span data-ttu-id="29c97-128">A guia **cobertura**</span><span class="sxs-lookup"><span data-stu-id="29c97-128">The **Coverage** tab</span></span>  
    > ![A guia cobertura][ImageCoverage]  

## <span data-ttu-id="29c97-130">Cobertura de código de registro</span><span class="sxs-lookup"><span data-stu-id="29c97-130">Record code coverage</span></span>   

1.  <span data-ttu-id="29c97-131">Clique em um dos seguintes botões na guia **cobertura** :</span><span class="sxs-lookup"><span data-stu-id="29c97-131">Click one of the following buttons in the **Coverage** tab:</span></span>  
    *   <span data-ttu-id="29c97-132">Clique em **iniciar a cobertura de instrumentação e recarregar** ![ cobertura de instrumentação de início de página e carregar página ][ImageReloadIcon] se desejar ver qual código é necessário para carregar a página.</span><span class="sxs-lookup"><span data-stu-id="29c97-132">Click **Start Instrumenting Coverage And Reload Page** ![Start Instrumenting Coverage And Reload Page][ImageReloadIcon] if you want to see what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="29c97-133">Clique em cobertura do instrumento de **cobertura do instrumento** ![ ][ImageRecordIcon] se você quiser ver qual código será usado depois de interagir com a página.</span><span class="sxs-lookup"><span data-stu-id="29c97-133">Click **Instrument Coverage** ![Instrument Coverage][ImageRecordIcon] if you want to see what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="29c97-134">Clique em **interromper a cobertura de instrumentação e mostrar resultados** ![ interromper cobertura de instrumentação e mostrar resultados ][ImageStopIcon] quando quiser parar de gravar cobertura de código.</span><span class="sxs-lookup"><span data-stu-id="29c97-134">Click **Stop Instrumenting Coverage And Show Results** ![Stop Instrumenting Coverage And Show Results][ImageStopIcon] when you want to stop recording code coverage.</span></span>  

## <span data-ttu-id="29c97-135">Analisar cobertura de código</span><span class="sxs-lookup"><span data-stu-id="29c97-135">Analyze code coverage</span></span>   

<span data-ttu-id="29c97-136">A tabela na guia **cobertura** mostra quais recursos foram analisados e quanto de código é usado dentro de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="29c97-136">The table in the **Coverage** tab shows you what resources were analyzed, and how much code is used within each resource.</span></span> <span data-ttu-id="29c97-137">Clique em uma linha para abrir esse recurso no painel **fontes** e ver uma divisão linha por linha de código usado e código não usado.</span><span class="sxs-lookup"><span data-stu-id="29c97-137">Click a row to open that resource in the **Sources** panel and see a line-by-line breakdown of used code and unused code.</span></span>  

> ##### <span data-ttu-id="29c97-138">Figura 3</span><span class="sxs-lookup"><span data-stu-id="29c97-138">Figure 3</span></span>  
> <span data-ttu-id="29c97-139">Um relatório de cobertura de código</span><span class="sxs-lookup"><span data-stu-id="29c97-139">A code coverage report</span></span>  
> ![Um relatório de cobertura de código][ImageExample]  

*   <span data-ttu-id="29c97-141">A coluna **URL** é a URL do recurso que foi analisado.</span><span class="sxs-lookup"><span data-stu-id="29c97-141">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="29c97-142">A coluna **tipo** indica se o recurso contém CSS, JavaScript ou ambos.</span><span class="sxs-lookup"><span data-stu-id="29c97-142">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="29c97-143">A coluna **total de bytes** é o tamanho total do recurso em bytes.</span><span class="sxs-lookup"><span data-stu-id="29c97-143">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="29c97-144">A coluna **bytes não utilizados** é o número de bytes que não foram usados.</span><span class="sxs-lookup"><span data-stu-id="29c97-144">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="29c97-145">A última coluna sem nome é uma visualização das colunas **total de bytes** e **bytes não utilizados** .</span><span class="sxs-lookup"><span data-stu-id="29c97-145">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="29c97-146">A seção vermelha da barra é bytes não utilizados.</span><span class="sxs-lookup"><span data-stu-id="29c97-146">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="29c97-147">A seção verde é usada bytes.</span><span class="sxs-lookup"><span data-stu-id="29c97-147">The green section is used bytes.</span></span>  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Figura 1: analisando cobertura de código"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Figura 2: a guia cobertura"  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Figura 3: um relatório de cobertura de código"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Executar comandos com o menu de comando do Microsoft Edge DevTools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botões-Bootstrap"  

> [!NOTE]
> <span data-ttu-id="29c97-153">Partes desta página são modificações com base no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usados de acordo com os termos descritos na [licença internacional Creative Commons][CCA4IL]rereference 4,0 International.</span><span class="sxs-lookup"><span data-stu-id="29c97-153">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="29c97-154">A página original é encontrada [aqui](https://developers.google.com/web/tools/chrome-devtools/coverage/index) e é criada por [Kayce Basques][KayceBasques] \ (redator técnico, Chrome devtools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="29c97-154">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="29c97-156">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International (CC BY 4.0) da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="29c97-156">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
