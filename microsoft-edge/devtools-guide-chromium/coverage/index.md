---
description: Como encontrar e analisar o JavaScript e o código CSS nãoutilados no Microsoft Edge DevTools.
title: Encontre JavaScript e Código CSS nãoutilados com o painel Cobertura no Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398760"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a><span data-ttu-id="fd1d5-104">Encontre o JavaScript e o código CSS nãoutilados com o painel Cobertura no Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fd1d5-104">Find unused JavaScript and CSS code with the Coverage panel in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="fd1d5-105">O **painel Cobertura** no Microsoft Edge DevTools ajuda você a encontrar código JavaScript e CSS não-utilado.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-105">The **Coverage** panel in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="fd1d5-106">A remoção de código nãousado pode acelerar a carga da página e salvar os dados celulares dos usuários móveis.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-106">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Analisando a cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   <span data-ttu-id="fd1d5-108">Analisando a cobertura de código</span><span class="sxs-lookup"><span data-stu-id="fd1d5-108">Analyzing code coverage</span></span>  
:::image-end:::  

> [!WARNING]
> <span data-ttu-id="fd1d5-109">Localizar código nãousado é relativamente fácil.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="fd1d5-110">Mas a refactoração de uma base de código para que cada página só envia o JavaScript e CSS necessários pode ser difícil.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="fd1d5-111">Este guia não abrange como refactor uma base de código para evitar o código nãousado, pois esses refatores dependem muito da sua pilha de tecnologia.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <a name="overview"></a><span data-ttu-id="fd1d5-112">Visão geral</span><span class="sxs-lookup"><span data-stu-id="fd1d5-112">Overview</span></span>  

<span data-ttu-id="fd1d5-113">O envio de JavaScript ou CSS nãousado é um problema comum no desenvolvimento da Web.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="fd1d5-114">Por exemplo, suponha que você queira usar o [componente do botão Bootstrap][BootstrapButtons] em sua página.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="fd1d5-115">Para usar o componente de botão, você precisa adicionar um link à folha de estilos Bootstrap em seu HTML, assim:</span><span class="sxs-lookup"><span data-stu-id="fd1d5-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="fd1d5-116">Esta folha de estilos não inclui apenas o código do componente do botão.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="fd1d5-117">Ele contém o CSS para **todos os** componentes Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="fd1d5-118">Mas você não está usando nenhum dos outros componentes Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="fd1d5-119">Portanto, sua página está baixando um monte de CSS que ela não precisa.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="fd1d5-120">Esse CSS extra é um problema pelos seguintes motivos.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="fd1d5-121">O código extra reduz a carga da página.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-121">The extra code slows down your page load.</span></span>  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="fd1d5-122">Se um usuário acessar a página em um dispositivo móvel, o código extra usará seus dados celulares.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a><span data-ttu-id="fd1d5-123">Abra o painel Cobertura</span><span class="sxs-lookup"><span data-stu-id="fd1d5-123">Open the Coverage panel</span></span>  

1.  <span data-ttu-id="fd1d5-124">[Abra o Menu de Comando][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="fd1d5-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="fd1d5-125">Comece a digitar `coverage` , selecione o comando Mostrar **Cobertura** e, em seguida, selecione para executar `Enter` o comando.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-125">Start typing `coverage`, select the **Show Coverage** command, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="fd1d5-126">O **painel Cobertura** é aberto na **Gaveta**.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-126">The **Coverage** panel opens in the **Drawer**.</span></span>  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="O painel Cobertura" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       <span data-ttu-id="fd1d5-128">O **painel Cobertura**</span><span class="sxs-lookup"><span data-stu-id="fd1d5-128">The **Coverage** panel</span></span>  
    :::image-end:::  
    
## <a name="record-code-coverage"></a><span data-ttu-id="fd1d5-129">Cobertura de código de registro</span><span class="sxs-lookup"><span data-stu-id="fd1d5-129">Record code coverage</span></span>  

1.  <span data-ttu-id="fd1d5-130">Escolha um dos seguintes botões no painel **Cobertura.**</span><span class="sxs-lookup"><span data-stu-id="fd1d5-130">Choose one of the following buttons in the **Coverage** panel.</span></span>  
    *   <span data-ttu-id="fd1d5-131">Escolha **Iniciar a Cobertura de Instrumentação** e Recarregar Página \( Iniciar Cobertura de Instrumentação e Recarregar Página \) se quiser revisar qual código é necessário para carregar a ![ ][ImageReloadIcon] página.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-131">Choose **Start Instrumenting Coverage And Reload Page** \(![Start Instrumenting Coverage And Reload Page][ImageReloadIcon]\) if you want to review what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="fd1d5-132">Escolha **Cobertura de** Instrumento \( Cobertura de Instrumento \) se quiser revisar qual código é usado após interagir com a ![ ][ImageRecordIcon] página.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-132">Choose **Instrument Coverage** \(![Instrument Coverage][ImageRecordIcon]\) if you want to review what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="fd1d5-133">Escolha **Parar a cobertura de instrumentação e mostrar resultados** \( Parar a cobertura de instrumentação e mostrar resultados \) quando quiser parar de gravar a cobertura de ![ ][ImageStopIcon] código.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-133">Choose **Stop Instrumenting Coverage And Show Results** \(![Stop Instrumenting Coverage And Show Results][ImageStopIcon]\) when you want to stop recording code coverage.</span></span>  
    
## <a name="analyze-code-coverage"></a><span data-ttu-id="fd1d5-134">Analisar a cobertura de código</span><span class="sxs-lookup"><span data-stu-id="fd1d5-134">Analyze code coverage</span></span>  

<span data-ttu-id="fd1d5-135">A tabela no painel **Cobertura** exibe os recursos que foram analisados e quanto código é usado em cada recurso.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-135">The table in the **Coverage** panel displays the resources that were analyzed, and how much code is used within each resource.</span></span>  <span data-ttu-id="fd1d5-136">Escolha uma linha para abrir esse recurso no painel **Fontes** e revise uma divisão linha por linha do código usado e do código não usado.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-136">Choose a row to open that resource in the **Sources** panel and review a line-by-line breakdown of used code and unused code.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Um relatório de cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   <span data-ttu-id="fd1d5-138">Um relatório de cobertura de código</span><span class="sxs-lookup"><span data-stu-id="fd1d5-138">A code coverage report</span></span>  
:::image-end:::  

*   <span data-ttu-id="fd1d5-139">A **coluna URL** é a URL do recurso que foi analisado.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-139">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="fd1d5-140">A **coluna Type** diz se o recurso contém CSS, JavaScript ou ambos.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-140">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="fd1d5-141">A **coluna Total de Bytes** é o tamanho total do recurso em bytes.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-141">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="fd1d5-142">A **coluna Bytes não utilizados** é o número de bytes que não foram usados.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-142">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="fd1d5-143">A última coluna sem nome é uma visualização das colunas **Bytes Totais** e **Bytes NãoUsados.**</span><span class="sxs-lookup"><span data-stu-id="fd1d5-143">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="fd1d5-144">A seção vermelha da barra é bytes nãousados.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-144">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="fd1d5-145">A seção verde é usada bytes.</span><span class="sxs-lookup"><span data-stu-id="fd1d5-145">The green section is used bytes.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="fd1d5-146">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fd1d5-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Execute comandos com o menu DevTools Command do Microsoft Edge | Microsoft Docs"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botões - Bootstrap"  

> [!NOTE]
> <span data-ttu-id="fd1d5-149">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd1d5-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fd1d5-150">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/coverage/index) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="fd1d5-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fd1d5-152">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd1d5-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
