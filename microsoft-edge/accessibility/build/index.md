---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Mostre como as práticas recomendadas e os aplicativos sofisticados da Internet (ARIA) acessíveis podem ser juntos para criar um site acessível.
title: Build | Acesso
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: acessibilidade, acessibilidade para desenvolvedores, sites acessíveis, Edge, desenvolvimento da Web, ARIA, desenvolvedor, UIA, automação da interface do usuário
ms.custom: seodec18
ms.openlocfilehash: 40ab1acd0b5356ad4696cde0762f656708a67890
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231399"
---
# <span data-ttu-id="58d3e-104">Criando sites acessíveis</span><span class="sxs-lookup"><span data-stu-id="58d3e-104">Building Accessible Websites</span></span>

<span data-ttu-id="58d3e-105">A Web é preenchida com sites, aplicativos e interfaces do usuário dinâmicos e complexos criados usando uma combinação de HTML, CSS e JavaScript.</span><span class="sxs-lookup"><span data-stu-id="58d3e-105">The web is filled with dynamic and complex websites, applications, and user interfaces built using a combination of HTML, CSS, and JavaScript.</span></span>  <span data-ttu-id="58d3e-106">No entanto, quando projetado e criado sem acessibilidade em mente, esses sites complexos são difíceis de usar por pessoas que dependem de [tecnologias adaptativas](https://webaim.org/articles/motor/assistive) para navegar na Web.</span><span class="sxs-lookup"><span data-stu-id="58d3e-106">However, when designed and built without accessibility in mind, these complex websites are difficult to use by people who rely on [assistive technologies](https://webaim.org/articles/motor/assistive) to browse the web.</span></span> <span data-ttu-id="58d3e-107">A criação de sites acessíveis para pessoas com deficiências exige informações semânticas sobre a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="58d3e-107">Building websites that are accessible to people with disabilities requires semantic information about the user interface.</span></span> <span data-ttu-id="58d3e-108">Isso permite que tecnologias assistenciais, como leitores de tela, transmitam as informações necessárias para ajudar as pessoas com diversas habilidades a usar o site.</span><span class="sxs-lookup"><span data-stu-id="58d3e-108">This allows for assistive technologies, like screen readers, to convey the necessary information to help people with a range of abilities use the website.</span></span>

<span data-ttu-id="58d3e-109">Acesse [HTML5Accessibility](https://html5accessibility.com) para obter informações sobre quais novos recursos do HTML5 são accessibly suportados pelo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="58d3e-109">Visit [HTML5Accessibility](https://html5accessibility.com) for information on which new HTML5 features are accessibly supported by Microsoft Edge.</span></span>

## <span data-ttu-id="58d3e-110">Como funciona a acessibilidade</span><span class="sxs-lookup"><span data-stu-id="58d3e-110">How Accessibility Works</span></span>

<span data-ttu-id="58d3e-111">As tecnologias adaptativas adicionam recursos que os computadores geralmente não têm.</span><span class="sxs-lookup"><span data-stu-id="58d3e-111">Assistive technologies add capabilities that computers don't usually have.</span></span> <span data-ttu-id="58d3e-112">Por exemplo, um usuário com deficiência visual pode usar o teclado em combinação com tecnologia assistencial, como um leitor de tela, em vez de usar o navegador diretamente com o mouse e a tela.</span><span class="sxs-lookup"><span data-stu-id="58d3e-112">For example, a visually impaired user might use their keyboard in combination with assistive technology such as a screen reader, rather than directly using the browser with the mouse and screen.</span></span> <span data-ttu-id="58d3e-113">Para aplicativos em plataformas Microsoft e na Web, a tecnologia assistencial interage com a [automação da interface do usuário](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)da Microsoft, um modelo de objeto específico do aplicativo, como o dom (modelo de objeto de documento) no Microsoft Edge ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="58d3e-113">For applications on Microsoft platforms and on the web, the assistive technology interacts with Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), an application-specific object model such as the Document Object Model (DOM) in Microsoft Edge, or a combination of these.</span></span>

<span data-ttu-id="58d3e-114">Para os desenvolvedores da Web, determinados elementos HTML são mapeados para objetos de automação da interface do usuário, portanto, ao selecionar esses elementos HTML, o desenvolvedor pode usar as propriedades e os eventos de acessibilidade incluídos nesses elementos.</span><span class="sxs-lookup"><span data-stu-id="58d3e-114">For web developers, certain HTML elements are mapped to UI Automation objects, so in selecting those HTML elements, the developer can use the accessibility properties and events built in to those elements.</span></span> <span data-ttu-id="58d3e-115">Ao desenvolver seu site, geralmente você só precisa se preocupar em garantir que a API seja gravada corretamente (ou que o elemento apropriado seja especificado), para que o aplicativo possa ser acessado.</span><span class="sxs-lookup"><span data-stu-id="58d3e-115">While developing your website, you usually only need to be concerned with ensuring that the API is correctly written to (or that the appropriate element is specified), in order for the application to be accessible.</span></span> <span data-ttu-id="58d3e-116">Consulte [o Aria e a automação da interface do usuário no Microsoft Edge](./ARIA-and-UI-Automation.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="58d3e-116">Check out [ARIA and UI Automation in Microsoft Edge](./ARIA-and-UI-Automation.md) for more information.</span></span>  <span data-ttu-id="58d3e-117">Para obter informações sobre aplicativos da plataforma universal do Windows (UWP) acessíveis, consulte o tópico [acessibilidade](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) no centro de desenvolvimento do Windows.</span><span class="sxs-lookup"><span data-stu-id="58d3e-117">For information on accessible Universal Windows Platform (UWP) apps, see the [Accessibility](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) topic in the Windows Dev Center.</span></span>

<span data-ttu-id="58d3e-118">Muitos problemas comuns de acessibilidade com conteúdo dinâmico podem ser resolvidos por uma boa prática de codificação, e a documentação da [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) inclui muitas técnicas e práticas recomendadas para ajudá-lo a criar aplicativos Web dinâmicos mais acessíveis.</span><span class="sxs-lookup"><span data-stu-id="58d3e-118">Many common accessibility issues with dynamic content can be addressed by good coding practice, and the [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) documentation includes many techniques and best practices to help you create more accessible dynamic web applications.</span></span> <span data-ttu-id="58d3e-119">Mesmo quando codificado corretamente, no entanto, o conteúdo dinâmico não está necessariamente acessível.</span><span class="sxs-lookup"><span data-stu-id="58d3e-119">Even when coded properly, however, dynamic content is not necessarily accessible.</span></span> <span data-ttu-id="58d3e-120">[Aplicativos de Internet sofisticados e acessíveis (Aria)](#aria) ajudam a resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="58d3e-120">[Accessible Rich Internet Applications (ARIA)](#aria) helps overcome this issue.</span></span>  

<span data-ttu-id="58d3e-121">Para obter mais informações sobre acessibilidade na Web, confira a [introdução à acessibilidade da Web](https://www.w3.org/WAI/intro/accessibility.php) pela [iniciativa de acessibilidade da Web](https://www.w3.org/WAI/) (WAI).</span><span class="sxs-lookup"><span data-stu-id="58d3e-121">For more information on web accessibility, check out the [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative](https://www.w3.org/WAI/) (WAI).</span></span>

## <span data-ttu-id="58d3e-122">ARIA</span><span class="sxs-lookup"><span data-stu-id="58d3e-122">ARIA</span></span>

<span data-ttu-id="58d3e-123">A especificação do Aria ( [aplicativos sofisticados da Internet) acessível](https://www.w3.org/TR/wai-aria/) pela W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) define como uma sintaxe para tornar conteúdo dinâmico da Web e interfaces do usuário personalizadas acessíveis para todas as pessoas.</span><span class="sxs-lookup"><span data-stu-id="58d3e-123">The [Accessible Rich Internet Applications](https://www.w3.org/TR/wai-aria/) (ARIA) specification by the W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) defines as a syntax for making dynamic web content and custom user interfaces accessible to all people.</span></span> <span data-ttu-id="58d3e-124">O ARIA estende o HTML usando atributos adicionais (funções, propriedades e Estados) projetados para transmitir semântica personalizada.</span><span class="sxs-lookup"><span data-stu-id="58d3e-124">ARIA extends HTML by using additional attributes (roles, properties, and states) that are designed to convey custom semantics.</span></span> <span data-ttu-id="58d3e-125">Esses atributos são usados por navegadores para passar ao longo do estado e da função dos controles para a API de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-125">These attributes are used by browsers to pass along the controls' state and role to the accessibility API.</span></span>

### <span data-ttu-id="58d3e-126">Funções, propriedades e Estados</span><span class="sxs-lookup"><span data-stu-id="58d3e-126">Roles, Properties, and States</span></span>

<span data-ttu-id="58d3e-127">As funções do ARIA são definidas em elementos usando o [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) atributo para fornecer tecnologias adaptativas e informações sobre APIs de acessibilidade sobre o elemento.</span><span class="sxs-lookup"><span data-stu-id="58d3e-127">ARIA roles are set on elements using the [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribute to give assistive technologies and accessibility APIs information about the element.</span></span> <span data-ttu-id="58d3e-128">Por exemplo, o `<li>` elemento abaixo é atribuído `role="menuitem"` para significar que se trata de um item em um menu.</span><span class="sxs-lookup"><span data-stu-id="58d3e-128">For example, the below `<li>` element is assigned `role="menuitem"` to signify it's an item in a menu.</span></span>

```html
<li role="menuitem">Home</li>
```

<span data-ttu-id="58d3e-129">Os Estados e as propriedades do ARIA são atributos prefixados pelo Aria que fornecem informações específicas sobre um objeto para ajudar a formar a definição da natureza das funções.</span><span class="sxs-lookup"><span data-stu-id="58d3e-129">ARIA states and properties are aria-prefixed attributes that provide specific information about an object to help form the definition of the nature of roles.</span></span> <span data-ttu-id="58d3e-130">Propriedades são atributos essenciais para a natureza de um objeto, como [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) e [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="58d3e-130">Properties are attributes that are essential to the nature of an object, like [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) and [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx).</span></span> <span data-ttu-id="58d3e-131">Alterar uma propriedade afeta o significado do objeto.</span><span class="sxs-lookup"><span data-stu-id="58d3e-131">Changing a property affects the meaning of the object.</span></span> <span data-ttu-id="58d3e-132">No exemplo abaixo, a propriedade `aria-haspopup="true"` é definida em um `<li>` item de menu para significar que ele tem um pop-up.</span><span class="sxs-lookup"><span data-stu-id="58d3e-132">In the example below, the property `aria-haspopup="true"` is set on a `<li>` menu item to signify it has a popup.</span></span>

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

<span data-ttu-id="58d3e-133">Os Estados não alteram a natureza do objeto, mas representam informações associadas ao objeto ou à interação do usuário com o objeto, como [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) ou [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="58d3e-133">States do not change the nature of the object, but represent information associated with the object or user interaction with the object, like [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) or [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx).</span></span> <span data-ttu-id="58d3e-134">Por exemplo, o estado `aria-checked="false"` no exemplo abaixo representa que a caixa de seleção não está marcada.</span><span class="sxs-lookup"><span data-stu-id="58d3e-134">For example, the state `aria-checked="false"` in the example below represents that the checkbox is not checked.</span></span>

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

<span data-ttu-id="58d3e-135">Vá para [o modelo de funções](https://www.w3.org/TR/wai-aria-1.1/#roles) pelo W3C para ver uma lista completa de funções, propriedades e Estados.</span><span class="sxs-lookup"><span data-stu-id="58d3e-135">Go to [The Roles Model](https://www.w3.org/TR/wai-aria-1.1/#roles) by the W3C to see a full list of roles, properties, and states.</span></span>

<span data-ttu-id="58d3e-136">Para obter mais informações sobre o ARIA, consulte o ARIA na seção [Resources](#resources) .</span><span class="sxs-lookup"><span data-stu-id="58d3e-136">For more information on ARIA, see the ARIA in the [Resources](#resources) section.</span></span>

## <span data-ttu-id="58d3e-137">Teste de compatibilidade de tecnologia assistencial</span><span class="sxs-lookup"><span data-stu-id="58d3e-137">Assistive Technology Compatibility Testing</span></span>  

<span data-ttu-id="58d3e-138">Verificar se o site que você está criando funciona com tecnologias assistenciais reais é a melhor maneira de garantir uma boa experiência para os usuários com deficiências.</span><span class="sxs-lookup"><span data-stu-id="58d3e-138">Verifying that the website you are building works with real assistive technologies is the best way to ensure a good experience for your users with disabilities.</span></span>  <span data-ttu-id="58d3e-139">Como muitas tecnologias assistenciais usam o teclado, testar a acessibilidade de teclado do seu site é um bom lugar para começar.</span><span class="sxs-lookup"><span data-stu-id="58d3e-139">Since many assistive technologies make use of the keyboard, testing the keyboard accessibility of your website is a good place to start.</span></span>  <span data-ttu-id="58d3e-140">O [teste de compatibilidade de teclado][W3cPerspectiveVideosKeyboard] valida que os usuários têm acesso a todos os controles interativos sem exigir um mouse.</span><span class="sxs-lookup"><span data-stu-id="58d3e-140">[Keyboard compatibility testing][W3cPerspectiveVideosKeyboard] validates that users have access to all interactive controls without requiring a mouse.</span></span>  <span data-ttu-id="58d3e-141">O Microsoft [Accessibility insights para Web][AccessibilityinsightsWebOverview] é uma extensão de navegador para Microsoft Edge e Chrome que o orienta e revela vários problemas comuns.</span><span class="sxs-lookup"><span data-stu-id="58d3e-141">Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] is a browser extension for Microsoft Edge and Chrome that guides you and reveals several common issues.</span></span>  

<span data-ttu-id="58d3e-142">Quando tiver certeza de que seu site funciona bem com um teclado, experimente-o com outras tecnologias assistenciais, como leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="58d3e-142">Once you are confident that your website works well with a keyboard, try it with other assistive technologies, such as screen readers.</span></span>  <span data-ttu-id="58d3e-143">Ele revela problemas no seguinte.</span><span class="sxs-lookup"><span data-stu-id="58d3e-143">It uncover issues in the following.</span></span>

*   <span data-ttu-id="58d3e-144">HTML, ARIA e CSS.</span><span class="sxs-lookup"><span data-stu-id="58d3e-144">Your HTML, ARIA, and CSS.</span></span>  
*   <span data-ttu-id="58d3e-145">O nível de suporte de uma tecnologia assistencial para um recurso ou uma técnica.</span><span class="sxs-lookup"><span data-stu-id="58d3e-145">The level of support of an assistive technology for a feature or technique.</span></span>  
    
<span data-ttu-id="58d3e-146">Diferentes navegadores podem mapear elementos para APIs de acessibilidade de plataforma de forma diferente do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="58d3e-146">Different browsers may map elements to platform accessibility APIs differently than Microsoft Edge.</span></span>  <span data-ttu-id="58d3e-147">Ao criar sua interface, é importante considerar cada diferença.</span><span class="sxs-lookup"><span data-stu-id="58d3e-147">While building your interface, it is important to consider each difference.</span></span>  

<span data-ttu-id="58d3e-148">O WebAIM conduz pesquisas com [leitores de tela][WebaimProjectsScreenreadersurvey8] e usuários com [deficiência visual][WebaimProjectsLowvisionsurvey2] que ajudam você a decidir quais tecnologias adaptativas e navegadores você deseja testar.</span><span class="sxs-lookup"><span data-stu-id="58d3e-148">WebAIM conducts surveys with [screen reader][WebaimProjectsScreenreadersurvey8] and [low vision][WebaimProjectsLowvisionsurvey2] users that help you decide which assistive technologies and browsers you want to test.</span></span>  

### <span data-ttu-id="58d3e-149">Aprendendo a testar</span><span class="sxs-lookup"><span data-stu-id="58d3e-149">Learning How to Test</span></span>  

<span data-ttu-id="58d3e-150">Tecnologias adaptativas são ferramentas sofisticadas.</span><span class="sxs-lookup"><span data-stu-id="58d3e-150">Assistive technologies are sophisticated tools.</span></span>  <span data-ttu-id="58d3e-151">Não presuma que você pode iniciar imediatamente o teste com uma tecnologia assistencial sem primeiro aprender a trabalhar.</span><span class="sxs-lookup"><span data-stu-id="58d3e-151">Do not assume that you are able to immediately start testing with an assistive technology without first learning about how it works.</span></span>  <span data-ttu-id="58d3e-152">Aprender a testar com um leitor de tela tem uma curva de aprendizagem especialmente acentuada.</span><span class="sxs-lookup"><span data-stu-id="58d3e-152">Learning to test with a screen reader has an especially steep learning curve.</span></span>  <span data-ttu-id="58d3e-153">Um usuário do leitor de tela principiante pode supor que um erro de leitor de tela ocorreu enquanto o problema está relacionado ao uso indevido do leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="58d3e-153">A novice screen reader user may assume that a screen reader bug has occurred while the issue is related to misuse of the screen reader.</span></span>  

<span data-ttu-id="58d3e-154">Para obter mais informações sobre como aprender a testar com tecnologias adaptativas, navegue até [testando com leitores de tela][WebaimArticlesScreenreaderTesting] no WebAIM.</span><span class="sxs-lookup"><span data-stu-id="58d3e-154">For more information about learning to test with assistive technologies, navigate to [Testing with Screen Readers][WebaimArticlesScreenreaderTesting] on WebAIM.</span></span>  

### <span data-ttu-id="58d3e-155">Testando localmente</span><span class="sxs-lookup"><span data-stu-id="58d3e-155">Testing Locally</span></span>  

<span data-ttu-id="58d3e-156">A maioria dos dispositivos inclui tecnologia assistencial interna ao sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="58d3e-156">Most devices include assistive technology that is built-in to the OS.</span></span>  <span data-ttu-id="58d3e-157">O Microsoft Windows inclui o leitor de tela do [Windows narrador][MicrosoftSupport22798] e a [lupa do Windows][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].</span><span class="sxs-lookup"><span data-stu-id="58d3e-157">Microsoft Windows includes the [Windows Narrator][MicrosoftSupport22798] screen reader and [Windows Magnifier][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].</span></span>  <span data-ttu-id="58d3e-158">tecnologias assistenciais de terceiros, como o [NVDA][NvaccessAboutNvda], o [FreedomscientificSoftwareJaws]e o [ZoomText][FreedomscientificSoftwareZoomtext] , estão disponíveis para download.</span><span class="sxs-lookup"><span data-stu-id="58d3e-158">3rd party assistive technologies like [NVDA][NvaccessAboutNvda], [FreedomscientificSoftwareJaws], and [ZoomText][FreedomscientificSoftwareZoomtext] are available to download.</span></span>  <span data-ttu-id="58d3e-159">O Apple macOS inclui o leitor de tela [VoiceOver][AppleAccessibilityMacVision] .</span><span class="sxs-lookup"><span data-stu-id="58d3e-159">Apple macOS includes the [VoiceOver][AppleAccessibilityMacVision] screen reader.</span></span>  <span data-ttu-id="58d3e-160">E iOS, Android e Linux dão suporte a uma variedade de tecnologias adaptativas.</span><span class="sxs-lookup"><span data-stu-id="58d3e-160">And iOS, Android, and Linux all support a variety of assistive technologies.</span></span>  

### <span data-ttu-id="58d3e-161">Teste em emuladores e máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="58d3e-161">Testing in Virtual Machines and Emulators</span></span>  

<span data-ttu-id="58d3e-162">Em macOS, se você quiser testar com uma tecnologia assistencial somente disponível para Windows, como o narrador do Windows ou o NVDA, crie um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="58d3e-162">Under macOS, if you want to test with an assistive technology only available for Windows, like Windows Narrator or NVDA, create a Windows virtual machine.</span></span>  <span data-ttu-id="58d3e-163">Máquinas virtuais com o Microsoft Edge \ (EdgeHTML \) e o IE estão disponíveis para VirtualBox e VMWare na [página de download de máquinas virtuais][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="58d3e-163">Virtual machines with Microsoft Edge \(EdgeHTML\) and IE are available for VirtualBox and VMWare on the [Virtual Machines download page][MicrosoftDeveloperEdgeVms].</span></span>  

<span data-ttu-id="58d3e-164">O [Android Studio][AndroidDeveloperSdkInstallingStudioHtml] inclui um emulador que você testará as tecnologias assistenciais no [pacote de acessibilidade do Android][GooglePlayStoreAndroidAccessibilitySuite].</span><span class="sxs-lookup"><span data-stu-id="58d3e-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] includes an emulator that for you to test assistive technologies in the [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite].</span></span>  <span data-ttu-id="58d3e-165">Siga as instruções para [configurar um dispositivo virtual][AndroidDeveloperDevicesManagingAvdsHtml] e [iniciar o emulador][AndroidDeveloperDevicesEmulatorHtml]e, em seguida, instalar o [pacote de acessibilidade Android][GooglePlayStoreAndroidAccessibilitySuite] na GooglePlay Store.</span><span class="sxs-lookup"><span data-stu-id="58d3e-165">Follow the instructions to [set up a virtual device][AndroidDeveloperDevicesManagingAvdsHtml] and [start the emulator][AndroidDeveloperDevicesEmulatorHtml], then install [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] from the GooglePlay store.</span></span>  

> [!NOTE]
> <span data-ttu-id="58d3e-166">No momento, o simulador do iOS não inclui o VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="58d3e-166">The iOS Simulator does not currently include VoiceOver.</span></span>  

### <span data-ttu-id="58d3e-167">Ferramentas de teste baseado em nuvem</span><span class="sxs-lookup"><span data-stu-id="58d3e-167">Cloud-based Testing Tools</span></span>  

<span data-ttu-id="58d3e-168">Se uma tecnologia assistencial não estiver disponível no seu sistema operacional ou se você não puder instalar uma em uma máquina virtual ou emulador, as ferramentas de teste de tecnologia assistencial baseadas em nuvem serão a melhor coisa.</span><span class="sxs-lookup"><span data-stu-id="58d3e-168">If an assistive technology is not available on your OS or you not possible to install one on a virtual machine or emulator, cloud-based assistive technology testing tools are the next best thing.</span></span>  

*   <span data-ttu-id="58d3e-169">O [Assistiv Labs (comercial)][AssistivlabsMain] permite que você teste manualmente com tecnologias adaptativas por meio de qualquer navegador da Web moderno.</span><span class="sxs-lookup"><span data-stu-id="58d3e-169">[Assistiv Labs (commercial)][AssistivlabsMain] enables you to manually test with assistive technologies through any modern web browser.</span></span>  <span data-ttu-id="58d3e-170">Escolha uma tecnologia assistencial e um navegador e conecte você a uma máquina virtual, emulador ou dispositivo real com o qual você pode interagir.</span><span class="sxs-lookup"><span data-stu-id="58d3e-170">Choose an assistive technology and browser and it connects you with a virtual machine, emulator, or real device with which you may interact.</span></span>  

## <span data-ttu-id="58d3e-171">Recursos</span><span class="sxs-lookup"><span data-stu-id="58d3e-171">Resources</span></span>

### <span data-ttu-id="58d3e-172">Noções básicas sobre acessibilidade</span><span class="sxs-lookup"><span data-stu-id="58d3e-172">Accessibility Basics</span></span>

#### [<span data-ttu-id="58d3e-173">O projeto A11Y</span><span class="sxs-lookup"><span data-stu-id="58d3e-173">The A11Y Project</span></span>](http://a11yproject.com/)

<span data-ttu-id="58d3e-174">O projeto A11Y é um esforço orientado à Comunidade para facilitar a acessibilidade na Web.</span><span class="sxs-lookup"><span data-stu-id="58d3e-174">The A11Y Project is a community-driven effort to make web accessibility easier.</span></span> <span data-ttu-id="58d3e-175">Confira [o site de projeto do A11Y](https://a11yproject.com/) para saber mais sobre os princípios básicos de acessibilidade, o padrão acessível e a [biblioteca](https://a11yproject.com/patterns)de widgets e seus [recursos](http://a11yproject.com/resources.html) de acessibilidade software, Blogs, livros e ferramentas.</span><span class="sxs-lookup"><span data-stu-id="58d3e-175">Check out [The A11Y Project](https://a11yproject.com/) site to learn about basic accessibility principles, their accessible pattern and widget [library](https://a11yproject.com/patterns), and their [resources](http://a11yproject.com/resources.html) on accessibility software, blogs, books, and tools.</span></span>

#### [<span data-ttu-id="58d3e-176">Iniciativa de acessibilidade da Web (WAI)</span><span class="sxs-lookup"><span data-stu-id="58d3e-176">Web Accessibility Initiative (WAI)</span></span>](https://w3.org/WAI/)

<span data-ttu-id="58d3e-177">O W3C Web Accessibility Initiative (WAI) é um esforço para ajudar a melhorar a acessibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="58d3e-177">The W3C Web Accessibility Initiative (WAI) is an effort to help improve the accessibility of the web.</span></span> <span data-ttu-id="58d3e-178">O site fornece uma variedade de recursos para [introdução à acessibilidade da Web](https://www.w3.org/WAI/gettingstarted/Overview.html), [design para inclusão](https://www.w3.org/WAI/users/Overview.html), [tutoriais e apresentações](https://www.w3.org/WAI/train.html)e muito mais.</span><span class="sxs-lookup"><span data-stu-id="58d3e-178">Their site provides a variety of resources for [Getting Started with Web Accessibility](https://www.w3.org/WAI/gettingstarted/Overview.html), [Designing for Inclusion](https://www.w3.org/WAI/users/Overview.html), [tutorials and presentations](https://www.w3.org/WAI/train.html), and more.</span></span>

### <span data-ttu-id="58d3e-179">Blogs sobre acessibilidade</span><span class="sxs-lookup"><span data-stu-id="58d3e-179">Accessibility Blogs</span></span>

#### [<span data-ttu-id="58d3e-180">O grupo Paciello Group</span><span class="sxs-lookup"><span data-stu-id="58d3e-180">The Paciello Group</span></span>](https://www.paciellogroup.com/blog/)

<span data-ttu-id="58d3e-181">O grupo Paciello Group fornece soluções de consultoria e tecnologia a organizações em todo o mundo para garantir que seus clientes atinjam todas as audiências de forma eficaz e eficiente, ao mesmo tempo em que atendem aos padrões governamentais e internacionais.</span><span class="sxs-lookup"><span data-stu-id="58d3e-181">The Paciello Group provides consulting and technology solutions to organizations around the world to ensure their clients reach all audiences effectively and efficiently, while meeting governmental and international standards.</span></span> <span data-ttu-id="58d3e-182">O blog aborda os tópicos como práticas recomendadas de acessibilidade na Web, ferramentas de acessibilidade e tendências de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-182">Their blog covers topics like web accessibility best practices, accessibility tools, and accessibility trends.</span></span>

#### [<span data-ttu-id="58d3e-183">Simplesmente acessível</span><span class="sxs-lookup"><span data-stu-id="58d3e-183">Simply Accessible</span></span>](http://simplyaccessible.com/articles/)

<span data-ttu-id="58d3e-184">Simplesmente acessível é uma equipe de especialistas em acessibilidade que fornecem treinamento de acessibilidade, consultoria e muito mais para alterar a percepção da acessibilidade na Web.</span><span class="sxs-lookup"><span data-stu-id="58d3e-184">Simply Accessible is a team of accessibility specialists providing accessibility training, consulting and more to change the perception of accessibility on the web.</span></span> <span data-ttu-id="58d3e-185">A seção de [artigos](http://simplyaccessible.com/articles/) descreve as práticas recomendadas para acessibilidade da Web, design acessível e muito mais.</span><span class="sxs-lookup"><span data-stu-id="58d3e-185">Their [Articles](http://simplyaccessible.com/articles/) section discusses best practices for web accessibility, accessible design, and more.</span></span>

#### [<span data-ttu-id="58d3e-186">Grupo SSB BART (SSB)</span><span class="sxs-lookup"><span data-stu-id="58d3e-186">SSB BART Group (SSB)</span></span>](http://www.ssbbartgroup.com/blog/)

<span data-ttu-id="58d3e-187">SSB BART Group é uma empresa de acessibilidade digital que oferece suporte a seus clientes no desenvolvimento e implantação de produtos e serviços acessíveis.</span><span class="sxs-lookup"><span data-stu-id="58d3e-187">SSB BART Group is a digital accessibility firm supporting their clients in developing and deploying accessible products and services.</span></span> <span data-ttu-id="58d3e-188">Seus tópicos de endereços de blog, como práticas recomendadas do ARIA, tendências de acessibilidade, webinars e muito mais.</span><span class="sxs-lookup"><span data-stu-id="58d3e-188">Their blog addresses topics like ARIA best practices, accessibility trends, webinars, and more.</span></span>

### <span data-ttu-id="58d3e-189">Exemplos acessíveis</span><span class="sxs-lookup"><span data-stu-id="58d3e-189">Accessible Examples</span></span>

#### [<span data-ttu-id="58d3e-190">ally.js-tutoriais</span><span class="sxs-lookup"><span data-stu-id="58d3e-190">ally.js - Tutorials</span></span>](http://allyjs.io/tutorials/)

<span data-ttu-id="58d3e-191">Biblioteca JavaScript para ajudar os aplicativos da Web modernos com preocupações com acessibilidade, facilitando a acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-191">JavaScript library to help modern web applications with accessibility concerns by making accessibility simpler.</span></span>

#### [<span data-ttu-id="58d3e-192">Heydonworks-exemplos de ARIA</span><span class="sxs-lookup"><span data-stu-id="58d3e-192">Heydonworks - ARIA Examples</span></span>](http://heydonworks.com/practical_aria_examples/)

<span data-ttu-id="58d3e-193">Exemplos práticos do ARIA para melhorar a acessibilidade do aplicativo</span><span class="sxs-lookup"><span data-stu-id="58d3e-193">Practical ARIA examples to enhance your application accessibility</span></span>

#### [<span data-ttu-id="58d3e-194">Exemplos de OpenAjax</span><span class="sxs-lookup"><span data-stu-id="58d3e-194">OpenAjax Examples</span></span>](http://oaa-accessibility.org/)

<span data-ttu-id="58d3e-195">O website da Aliança OpenAjax é um recurso excelente para verificar as regras do WAI-ARIA e fornece vários exemplos de implementações do WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="58d3e-195">The OpenAjax Alliance website is an excellent resource for verifying the rules for WAI-ARIA and provides a number of examples of WAI-ARIA implementations.</span></span>

#### [<span data-ttu-id="58d3e-196">Padrões</span><span class="sxs-lookup"><span data-stu-id="58d3e-196">Patterns</span></span>](http://a11yproject.com/patterns.html)

<span data-ttu-id="58d3e-197">[O projeto A11Y](http://a11yproject.com/) oferece uma biblioteca de widgets e padrões acessíveis, como menus, botões, dicas de ferramenta e muito mais.</span><span class="sxs-lookup"><span data-stu-id="58d3e-197">[The A11Y Project](http://a11yproject.com/) offers a library of accessible widgets and patterns like menus, buttons, tooltips, and more.</span></span>

### <span data-ttu-id="58d3e-198">Técnicas de acessibilidade & ferramentas</span><span class="sxs-lookup"><span data-stu-id="58d3e-198">Accessibility Techniques & Tools</span></span>

#### [<span data-ttu-id="58d3e-199">Acessibilidade: criando ícones de extensão acessíveis para o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="58d3e-199">Accessibility: Creating accessible extension icons for Microsoft Edge</span></span>](../../edgehtml/extensions/guides/accessibility.md)

<span data-ttu-id="58d3e-200">Obtenha orientação sobre como criar ícones de extensões acessíveis para o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="58d3e-200">Get guidance on creating accessible extensions icons for Microsoft Edge.</span></span>

#### [<span data-ttu-id="58d3e-201">Nome acessível e descrição: computação e mapeamentos 1,1</span><span class="sxs-lookup"><span data-stu-id="58d3e-201">Accessible Name and Description: Computation and Mappings 1.1</span></span>](https://www.w3.org/TR/accname-1.1/)

<span data-ttu-id="58d3e-202">Este documento de mapeamento W3C explica como os navegadores determinam o nome e as descrições dos objetos acessíveis em linguagens de conteúdo da Web e os expõem em APIs de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-202">This W3C mapping document explains how browsers determine name and descriptions of accessible objects from web content languages and expose them in accessibility APIs.</span></span>

#### [<span data-ttu-id="58d3e-203">Recursos de avaliação de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="58d3e-203">Accessibility Evaluation Resources</span></span>](https://www.w3.org/WAI/eval/Overview.html)

<span data-ttu-id="58d3e-204">Recursos de avaliação de acessibilidade é um recurso de várias páginas pelo W3C que descreve abordagens diferentes para a avaliação de sites para acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-204">Accessibility Evaluation Resources is a multi-page resource by the W3C that outlines different approaches for evaluating websites for accessibility.</span></span>

#### [<span data-ttu-id="58d3e-205">Testes de compatibilidade de tecnologia assistencial</span><span class="sxs-lookup"><span data-stu-id="58d3e-205">Assistive technology compatibility tests</span></span>](http://www.powermapper.com/tests/)

<span data-ttu-id="58d3e-206">Resultados de teste mostrando como diferentes tipos de conteúdo e padrões se comportam em tecnologias assistenciais (AT), como leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="58d3e-206">Test results showing how different content types and standards behave in assistive technologies (AT) like screen readers.</span></span>

#### [<span data-ttu-id="58d3e-207">A criação de sites acessíveis ficou muito mais fácil</span><span class="sxs-lookup"><span data-stu-id="58d3e-207">Building accessible websites just got a lot easier</span></span>](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

<span data-ttu-id="58d3e-208">Esta postagem de blog de ferramentas e desenvolvimento Web .NET descreve o [Verificador de acessibilidade da Web](https://go.microsoft.com/fwlink/p/?linkid=841539)de extensão do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="58d3e-208">This .NET Web Development and Tools blog post describes the Visual Studio extension [Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).</span></span>

#### [<span data-ttu-id="58d3e-209">Principais mapeamentos de API de acessibilidade 1,1</span><span class="sxs-lookup"><span data-stu-id="58d3e-209">Core Accessibility API Mappings 1.1</span></span>](https://www.w3.org/TR/core-aam-1.1/)

<span data-ttu-id="58d3e-210">Este documento de mapeamento W3C explica como a semântica de idiomas de conteúdo da Web é exposta a APIs de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-210">This W3C mapping document explains how the semantics of web content languages are exposed to accessibility APIs.</span></span>  

#### [<span data-ttu-id="58d3e-211">Verificações fáceis – uma primeira revisão da acessibilidade na Web</span><span class="sxs-lookup"><span data-stu-id="58d3e-211">Easy Checks – A First Review of Web Accessibility</span></span>](https://www.w3.org/WAI/eval/preliminary.html)

<span data-ttu-id="58d3e-212">Uma série de verificações rápidas do WAI que ajudam você a Asses a acessibilidade de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="58d3e-212">A series of quick checks by the WAI that help you asses the accessibility of a web page.</span></span>

#### [<span data-ttu-id="58d3e-213">Como se adequar à WCAG 2,0</span><span class="sxs-lookup"><span data-stu-id="58d3e-213">How to Meet WCAG 2.0</span></span>](https://www.w3.org/WAI/WCAG20/quickref/)

<span data-ttu-id="58d3e-214">Uma referência rápida às diretrizes de acessibilidade de conteúdo da Web (WCAG) 2,0 requisitos (critérios de sucesso) e técnicas.</span><span class="sxs-lookup"><span data-stu-id="58d3e-214">A quick reference to Web Content Accessibility Guidelines (WCAG) 2.0 requirements (success criteria) and techniques.</span></span>

#### [<span data-ttu-id="58d3e-215">Mapeamentos de API de acessibilidade em HTML 1,0</span><span class="sxs-lookup"><span data-stu-id="58d3e-215">HTML Accessibility API Mappings 1.0</span></span>](https://www.w3.org/TR/html-aam-1.0/)

<span data-ttu-id="58d3e-216">Este documento de mapeamentos do W3C explica como elementos e atributos do HTML 5.1 são mapeados para APIs de acessibilidade de plataforma.</span><span class="sxs-lookup"><span data-stu-id="58d3e-216">This W3C mappings document explains how HTML5.1 element and attributes map to platform accessibility APIs.</span></span>

#### [<span data-ttu-id="58d3e-217">Dicas rápidas</span><span class="sxs-lookup"><span data-stu-id="58d3e-217">Quick Tips</span></span>](http://a11yproject.com/#Quick-tips)

<span data-ttu-id="58d3e-218">Uma lista de dicas de desenvolvimento rápido na Web para acessibilidade pelo [projeto A11Y](http://a11yproject.com/).</span><span class="sxs-lookup"><span data-stu-id="58d3e-218">A list of quick web development tips for accessibility by [The A11Y Project](http://a11yproject.com/).</span></span>

#### [<span data-ttu-id="58d3e-219">Verificação de site</span><span class="sxs-lookup"><span data-stu-id="58d3e-219">Site Scan</span></span>](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

<span data-ttu-id="58d3e-220">A ferramenta de verificação de site no centro de desenvolvimento do Microsoft Edge verifica se há bibliotecas desatualizadas, problemas de layout e problemas de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-220">The Site Scan tool on Microsoft Edge Dev Center checks for out-of-date libraries, layout issues, and accessibility issues.</span></span>

#### [<span data-ttu-id="58d3e-221">Técnicas para WCAG 2,0</span><span class="sxs-lookup"><span data-stu-id="58d3e-221">Techniques for WCAG 2.0</span></span>](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

<span data-ttu-id="58d3e-222">Técnicas do W3C que fornecem orientação para os desenvolvedores da Web sobre como atender às [diretrizes de acessibilidade do conteúdo da Web (WCAG) 2,0](https://w3.org/TR/WCAG20/) critérios de sucesso.</span><span class="sxs-lookup"><span data-stu-id="58d3e-222">Techniques from the W3C that provide guidance for web developers on meeting [Web Content Accessibility Guidelines (WCAG) 2.0](https://w3.org/TR/WCAG20/) success criteria.</span></span>

#### [<span data-ttu-id="58d3e-223">Dicas sobre o desenvolvimento para acessibilidade pela Web</span><span class="sxs-lookup"><span data-stu-id="58d3e-223">Tips on Developing for Web Accessibility</span></span>](https://w3.org/WAI/gettingstarted/tips/developing.html)

<span data-ttu-id="58d3e-224">Dicas do W3C sobre como desenvolver conteúdo da Web que seja mais acessível a pessoas com deficiências.</span><span class="sxs-lookup"><span data-stu-id="58d3e-224">Tips from the W3C on developing web content that is more accessible to people with disabilities.</span></span>

#### [<span data-ttu-id="58d3e-225">WAI-práticas de criação do ARIA 1,1</span><span class="sxs-lookup"><span data-stu-id="58d3e-225">WAI-ARIA Authoring Practices 1.1</span></span>](http://w3c.github.io/aria-practices/)

<span data-ttu-id="58d3e-226">Um documento pelo W3C que fornece aos leitores noções básicas sobre como usar o WAI-ARIA 1,1 e recomenda abordagens para tornar widgets, navegação e comportamentos acessíveis usando funções, Estados e propriedades do WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="58d3e-226">A document by the W3C that provides readers with an understanding of how to use WAI-ARIA 1.1 and recommends approaches to make widgets, navigation, and behaviors accessible using WAI-ARIA roles, states, and properties.</span></span>

#### [<span data-ttu-id="58d3e-227">Diretrizes e técnicas do WAI</span><span class="sxs-lookup"><span data-stu-id="58d3e-227">WAI Guidelines and Techniques</span></span>](https://w3.org/WAI/guid-tech.html)

<span data-ttu-id="58d3e-228">Uma série de diretrizes e normas de acessibilidade pela Web desenvolvida pela WAI.</span><span class="sxs-lookup"><span data-stu-id="58d3e-228">A series of web accessibility guidelines and standards developed by the WAI.</span></span>  

#### [<span data-ttu-id="58d3e-229">Lista de ferramentas de avaliação da Web Accessibility</span><span class="sxs-lookup"><span data-stu-id="58d3e-229">Web Accessibility Evaluation Tools List</span></span>](https://www.w3.org/WAI/ER/tools/index.html)

<span data-ttu-id="58d3e-230">Uma lista de ferramentas de avaliação de acessibilidade da Web para ajudar a determinar se os sites atendem às diretrizes de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="58d3e-230">A list of web accessibility evaluation tools to help determine if websites meet accessibility guidelines.</span></span>

#### [<span data-ttu-id="58d3e-231">Perspectivas de acessibilidade na Web: explorar o impacto e os benefícios de todos</span><span class="sxs-lookup"><span data-stu-id="58d3e-231">Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone</span></span>](https://w3.org/WAI/perspectives/)

<span data-ttu-id="58d3e-232">Uma série de vídeos de situação curto pelo W3C sobre o impacto da acessibilidade e os benefícios de todos.</span><span class="sxs-lookup"><span data-stu-id="58d3e-232">A series of short situational videos by the W3C about the impact of accessibility and the benefits for everyone.</span></span>

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Máquinas virtuais | Desenvolvedor do Microsoft Edge"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Guia completo do narrador | Suporte da Microsoft"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Use a lupa para facilitar a visualização de itens na tela | Suporte da Microsoft"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Informações sobre acessibilidade para Web | Informações sobre acessibilidade"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Criar e gerenciar dispositivos virtuais | Desenvolvedores Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Executar aplicativos no emulador Android | Desenvolvedores Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Baixar Android Studio | Desenvolvedores Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Acessibilidade de visão-Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Assistiv Labs"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "Jaws® | Freedom científico"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Freedom científico"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Pacote de acessibilidade do Android | GooglePlay Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "Sobre o NVDA | Acesso NV"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Compatibilidade de teclado | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Pesquisa de usuários com deficiência visual \ #2 resultados | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Pesquisa de usuários do leitor de tela \ #8 resultados | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Testes com leitores de tela | WebAIM"  