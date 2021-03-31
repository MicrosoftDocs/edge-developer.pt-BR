---
description: Saiba como criar, projetar e testar sites acessíveis dentro do Microsoft Edge.
title: Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, Edge, desenvolvimento da Web, ARIA, desenvolvedor, UIA, automação da interface do usuário
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231398"
---
# <span data-ttu-id="f5a2b-104">Visão geral de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="f5a2b-104">Accessibility overview</span></span>  

> <span data-ttu-id="f5a2b-105">"\ [T \], o impacto da deficiência é alterado radicalmente na Web porque a Web remove barreiras à comunicação e à interação que muitas pessoas enfrentam no mundo físico."</span><span class="sxs-lookup"><span data-stu-id="f5a2b-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="f5a2b-106">(Acessibilidade | W3C</span><span class="sxs-lookup"><span data-stu-id="f5a2b-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="f5a2b-107">A [organização de saúde do mundo][WHODisabilities] define a deficiência como "uma incompatibilidade entre os recursos do corpo de uma pessoa e os recursos do ambiente em que elas residem".</span><span class="sxs-lookup"><span data-stu-id="f5a2b-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="f5a2b-108">As desabilidades vão desde as desabilidades de situação, como mobilidade limitada enquanto mantém um bebê ou um sol brilhante em um telefone, a outros problemas físicos, auditivos, visuais ou relacionados à idade.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="f5a2b-109">A criação de sites e outras tecnologias para inclusão cria uma experiência agradável para cada pessoa.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="f5a2b-110">O design inclusivo e a acessibilidade na Web capacitam e auxiliam todos a usar a Web.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="f5a2b-111">Veja a seguir algumas práticas recomendadas, exemplos de código e outros recursos para obter mais informações sobre como [projetar][AccessibilityDesign], [criar][AccessibilityBuild]e [testar][AccessibilityTest] sites acessíveis no Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="f5a2b-112">Acessibilidade no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5a2b-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="f5a2b-113">No Microsoft Edge, introduzimos a [API de automação da interface do usuário][WindowsWin32AutoEntryui] moderna \(UIA API \).</span><span class="sxs-lookup"><span data-stu-id="f5a2b-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="f5a2b-114">A mudança para UIA foi um grande investimento em acessibilidade do navegador, e ele prepara a base para uma experiência da Web mais inclusiva para os usuários que dependem da tecnologia assistencial no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="f5a2b-115">Os usuários também se beneficiam da natureza verde do mecanismo Chromium.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="f5a2b-116">O sistema de acessibilidade no Microsoft Edge oferece suporte inerentemente a padrões da Web modernos, incluindo ARIA, HTML5 e CSS3.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="f5a2b-117">O diagrama a seguir do pipeline simplificado de navegador segue o conteúdo da página da Web em uma camada de apresentação acessível.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="O conteúdo transformado para o modelo de mecanismo é projetado em modos de exibição visuais e de acessibilidade apresentados como uma apresentação visual ou acessível":::
   <span data-ttu-id="f5a2b-119">O conteúdo transformado para o modelo de mecanismo é projetado em modos de exibição visuais e de acessibilidade apresentados como uma apresentação visual ou acessível</span><span class="sxs-lookup"><span data-stu-id="f5a2b-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="f5a2b-120">A equipe do Microsoft Edge trabalha com o W3C e outros fornecedores de navegador continuamente para garantir que os novos recursos da plataforma da Web tenham acessibilidade interna suficiente.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="f5a2b-121">Para obter informações sobre quais novos recursos do HTML5 são accessibly suportados pelo Microsoft Edge, acesse [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="f5a2b-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="f5a2b-122">Recursos</span><span class="sxs-lookup"><span data-stu-id="f5a2b-122">Resources</span></span>  

#### <span data-ttu-id="f5a2b-123">Blog de automação da interface do usuário do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="f5a2b-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="f5a2b-124">O [blog de automação da interface do usuário do Microsoft Windows][ArchiveBlogsWinuiautomation] aborda tópicos relacionados à API de automação do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="f5a2b-125">Iniciativa de acessibilidade da Web (WAI)</span><span class="sxs-lookup"><span data-stu-id="f5a2b-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="f5a2b-126">A [iniciativa de acessibilidade da Web (WAI)][W3CWaiHome] oferecida BT o W3C é um esforço para ajudar a melhorar a acessibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="f5a2b-127">O site fornece uma variedade de recursos para [introdução à acessibilidade da Web][W3CWaiGettingstartedOverview], [design para inclusão][W3CWaiFundamentals], [tutoriais e apresentações][W3CWaiTeachAdvocate]e muito mais.</span><span class="sxs-lookup"><span data-stu-id="f5a2b-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Criando sites acessíveis | Documento da Microsoft"  
[AccessibilityDesign]: ./design.md "Criando sites acessíveis | Documento da Microsoft"  
[AccessibilityTest]: ./test.md "Teste de acessibilidade | Documentos da Microsoft"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Automação da interface do usuário | Documento da Microsoft"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog de automação da interface do usuário do Microsoft Windows | Documento da Microsoft"  

[HTML5Accessibility]: https://html5accessibility.com "Acessibilidade do HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Acessibilidade | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Introdução à acessibilidade na Web | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Introdução: tornar um site acessível | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Visão geral de ensinar e defensor | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Recursos | QUE"  

