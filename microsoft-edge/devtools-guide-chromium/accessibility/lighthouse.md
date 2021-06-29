---
description: Testando a acessibilidade usando o Farol de dentro do DevTools.
title: Testar a acessibilidade usando o Lighthouse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 822c25240ba30df31416ca783bf48d6d9ba52ed2
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624630"
---
<!-- this article was created on 05/11/2021 by moving a section out from the "Accessibility reference" article (reference.md) -->
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

# <a name="test-accessibility-using-lighthouse"></a><span data-ttu-id="36f0f-104">Testar a acessibilidade usando o Lighthouse</span><span class="sxs-lookup"><span data-stu-id="36f0f-104">Test accessibility using Lighthouse</span></span>

<span data-ttu-id="36f0f-105">Você pode usar o Farol de dentro do DevTools para auditar a acessibilidade de uma página e gerar um relatório.</span><span class="sxs-lookup"><span data-stu-id="36f0f-105">You can use Lighthouse from within DevTools to audit the accessibility of a page and generate a report.</span></span> <span data-ttu-id="36f0f-106">Você pode usar a ferramenta Doleiro para determinar:</span><span class="sxs-lookup"><span data-stu-id="36f0f-106">You can use the Lighthouse tool to determine:</span></span>

*   <span data-ttu-id="36f0f-107">Se uma página está marcada corretamente para leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="36f0f-107">Whether a page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="36f0f-108">Se os elementos de texto em uma página têm taxas de contraste suficientes usando o Selador de Cores.</span><span class="sxs-lookup"><span data-stu-id="36f0f-108">Whether the text elements on a page have sufficient contrast ratios using the Color Picker.</span></span> <span data-ttu-id="36f0f-109">Para obter mais informações, navegue [até Testar contraste de cor de texto usando o Selador de Cores](color-picker.md).</span><span class="sxs-lookup"><span data-stu-id="36f0f-109">For more information, navigate to [Test text-color contrast using the Color Picker](color-picker.md).</span></span>   

> [!NOTE]
> <span data-ttu-id="36f0f-110">A **ferramenta Lighthouse** fornece links para conteúdo hospedado em sites de terceiros.</span><span class="sxs-lookup"><span data-stu-id="36f0f-110">The **Lighthouse** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="36f0f-111">A Microsoft não é responsável e não tem controle sobre o conteúdo desses sites e quaisquer dados que possam ser coletados.</span><span class="sxs-lookup"><span data-stu-id="36f0f-111">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="36f0f-112">Para auditar uma página usando a ferramenta Lighthouse, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="36f0f-112">To audit a page using the Lighthouse tool, perform the following steps.</span></span>

1.  <span data-ttu-id="36f0f-113">Navegue até a URL que você deseja auditar.</span><span class="sxs-lookup"><span data-stu-id="36f0f-113">Navigate to the URL that you want to audit.</span></span>
1.  <span data-ttu-id="36f0f-114">Em DevTools, selecione a **ferramenta DevTools.**</span><span class="sxs-lookup"><span data-stu-id="36f0f-114">In DevTools, select the **Lighthouse** tool.</span></span>  <span data-ttu-id="36f0f-115">As opções de configuração são exibidas.</span><span class="sxs-lookup"><span data-stu-id="36f0f-115">Configuration options are displayed.</span></span>
    
    :::image type="complex" source="../media/accessibility-lighthouse.msft.png" alt-text="Opções de configuração do Farol" lightbox="../media/accessibility-lighthouse.msft.png":::
       <span data-ttu-id="36f0f-117">Opções de configuração do Farol</span><span class="sxs-lookup"><span data-stu-id="36f0f-117">Lighthouse configuration options</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="36f0f-118">Para **Dispositivo**, selecione **Móvel** se quiser simular um dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="36f0f-118">For **Device**, select **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="36f0f-119">Essa opção altera a cadeia de caracteres do agente do usuário e resize o viewport.</span><span class="sxs-lookup"><span data-stu-id="36f0f-119">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="36f0f-120">Essa opção pode afetar os resultados da auditoria.</span><span class="sxs-lookup"><span data-stu-id="36f0f-120">This option can affect the audit results.</span></span>
1.  <span data-ttu-id="36f0f-121">Na seção **Categorias,** selecione **Acessibilidade**.</span><span class="sxs-lookup"><span data-stu-id="36f0f-121">In the **Categories** section, select **Accessibility**.</span></span>
1.  <span data-ttu-id="36f0f-122">Selecione **Gerar relatório**.</span><span class="sxs-lookup"><span data-stu-id="36f0f-122">Select **Generate report**.</span></span> <span data-ttu-id="36f0f-123">Após 10 a 30 segundos, o DevTools exibe um relatório.</span><span class="sxs-lookup"><span data-stu-id="36f0f-123">After 10 to 30 seconds, DevTools displays a report.</span></span>  <span data-ttu-id="36f0f-124">O relatório fornece dicas sobre como melhorar a acessibilidade da página.</span><span class="sxs-lookup"><span data-stu-id="36f0f-124">The report gives tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result.msft.png" alt-text="Um relatório do Farol para a categoria Acessibilidade" lightbox="../media/accessibility-lighthouse-result.msft.png":::
       <span data-ttu-id="36f0f-126">Um relatório do Farol para a **categoria Acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="36f0f-126">A Lighthouse report for the **Accessibility** category</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="36f0f-127">Selecione um item no relatório para saber mais sobre ele.</span><span class="sxs-lookup"><span data-stu-id="36f0f-127">Select an item in the report to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-lighthouse-result-issue-expanded.msft.png" alt-text="Um problema expandido em um relatório do Farol" lightbox="../media/accessibility-lighthouse-result-issue-expanded.msft.png":::
       <span data-ttu-id="36f0f-129">Um problema expandido em um relatório do Farol</span><span class="sxs-lookup"><span data-stu-id="36f0f-129">An expanded issue in a Lighthouse report</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="36f0f-130">Selecione o link **Saber mais** para exibir a documentação do problema.</span><span class="sxs-lookup"><span data-stu-id="36f0f-130">Select the **Learn more** link to view the documentation of the issue.</span></span>
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Exibir a documentação de um problema" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="36f0f-132">Exibir a documentação de um problema</span><span class="sxs-lookup"><span data-stu-id="36f0f-132">View the documentation of an issue</span></span>
    :::image-end:::  

1.  <span data-ttu-id="36f0f-133">Para retornar às opções de configuração, em DevTools, selecione **Executar uma auditoria** ( `+` ).</span><span class="sxs-lookup"><span data-stu-id="36f0f-133">To return to the configuration options, in DevTools, select **Perform an audit** (`+`).</span></span>    


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="36f0f-134">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="36f0f-134">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


> [!NOTE]
> <span data-ttu-id="36f0f-135">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="36f0f-135">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="36f0f-136">A página original é [encontrada](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) aqui e é de autoria de [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="36f0f-136">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="36f0f-138">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="36f0f-138">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- links -->  
[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd "axe - Teste de Acessibilidade da Web - Chrome Web Store"  
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
