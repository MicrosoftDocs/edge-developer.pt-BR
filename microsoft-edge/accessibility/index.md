---
description: Saiba como criar, projetar e testar sites acessíveis em Microsoft Edge.
title: Acessibilidade
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, borda, desenvolvimento da Web, ARIA, desenvolvedor, UIA, Automação da Interface do Usuário
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231398"
---
# <span data-ttu-id="2b7e1-104">Visão geral de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="2b7e1-104">Accessibility overview</span></span>  

> <span data-ttu-id="2b7e1-105">"\[T\]o impacto da deficiência é alterado radicalmente na Web porque a Web remove barreiras à comunicação e à interação que muitas pessoas enfrentam no mundo físico."</span><span class="sxs-lookup"><span data-stu-id="2b7e1-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="2b7e1-106">(Acessibilidade | W3C)</span><span class="sxs-lookup"><span data-stu-id="2b7e1-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="2b7e1-107">A [Organização Mundial de][WHODisabilities] Saúde define a deficiência como "uma incompatibilidade na interação entre os recursos do corpo de uma pessoa e os recursos do ambiente em que ela mora".</span><span class="sxs-lookup"><span data-stu-id="2b7e1-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="2b7e1-108">As deficiências variam de deficiências de situação, como mobilidade limitada ao segurar um bebê ou luz do sol brilhante em um telefone, até outras deficiências físicas, auditivas, visuais ou relacionadas à idade.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="2b7e1-109">Projetar sites e outras tecnologias para inclusão cria uma experiência agradável para cada pessoa.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="2b7e1-110">O design inclusivo e a acessibilidade da Web capacitam e ajudam a todos a usar a Web.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="2b7e1-111">Aqui estão algumas práticas recomendadas, exemplos de código e recursos adicionais para você saber mais sobre [Designing,][AccessibilityDesign] [Building][AccessibilityBuild]e [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="2b7e1-112">Acessibilidade no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2b7e1-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="2b7e1-113">Em Microsoft Edge, introduzimos a MODERNA API de Automação da [Interface do][WindowsWin32AutoEntryui] Usuário \(API UIA\).</span><span class="sxs-lookup"><span data-stu-id="2b7e1-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="2b7e1-114">A alteração para a UIA foi um grande investimento na acessibilidade do navegador e estabelece a base para uma experiência da Web mais inclusiva para usuários que dependem da tecnologia assistida no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="2b7e1-115">Os usuários também se beneficiam da natureza cada vez maior do Chromium mecanismo.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="2b7e1-116">O sistema de acessibilidade no Microsoft Edge oferece suporte inerentemente a padrões web modernos, incluindo ARIA, HTML5 e CSS3.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="2b7e1-117">O diagrama a seguir do pipeline de navegador simplificado segue o conteúdo da página da Web em uma camada de apresentação acessível.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="O conteúdo transformado no modelo de mecanismo é projetado em exibições visuais e de acessibilidade que são apresentadas como apresentação visual ou acessível":::
   <span data-ttu-id="2b7e1-119">O conteúdo transformado no modelo de mecanismo é projetado em exibições visuais e de acessibilidade que são apresentadas como apresentação visual ou acessível</span><span class="sxs-lookup"><span data-stu-id="2b7e1-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="2b7e1-120">A Microsoft Edge trabalha com o W3C e outros fornecedores de navegadores de forma contínua para garantir que os novos recursos da plataforma Web tenham acessibilidade interna suficiente.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="2b7e1-121">Para obter informações sobre quais novos recursos HTML5 têm suporte Microsoft Edge, navegue até [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="2b7e1-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="2b7e1-122">Recursos</span><span class="sxs-lookup"><span data-stu-id="2b7e1-122">Resources</span></span>  

#### <span data-ttu-id="2b7e1-123">Blog Windows automação da interface do usuário da Microsoft</span><span class="sxs-lookup"><span data-stu-id="2b7e1-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="2b7e1-124">O [blog Windows automação da interface][ArchiveBlogsWinuiautomation] do usuário da Microsoft aborda tópicos relacionados à API Windows Automação.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="2b7e1-125">Iniciativa de Acessibilidade da Web (WAI)</span><span class="sxs-lookup"><span data-stu-id="2b7e1-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="2b7e1-126">A [Iniciativa de Acessibilidade da Web (WAI)][W3CWaiHome] fornecida bt o W3C é um esforço para ajudar a melhorar a acessibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="2b7e1-127">O site fornece uma variedade de recursos para Introdução à Acessibilidade da [Web,][W3CWaiGettingstartedOverview] [Design para][W3CWaiFundamentals]Inclusão, tutoriais e [apresentações][W3CWaiTeachAdvocate]e muito mais.</span><span class="sxs-lookup"><span data-stu-id="2b7e1-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Criar sites acessíveis | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Criar sites acessíveis | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Testes de acessibilidade | Microsoft Docs"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Interface do usuário | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog Windows de Automação da Interface do Usuário da Microsoft | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "Acessibilidade HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Acessibilidade | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Introdução à | Iniciativa de Acessibilidade da Web (S) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Iniciando: tornando um site acessível | Iniciativa de Acessibilidade da Web (S) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Iniciativa de Acessibilidade da Web (S) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Visão geral do professor e do advogado | Iniciativa de Acessibilidade da Web (S) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Deficiências | OMS"  

