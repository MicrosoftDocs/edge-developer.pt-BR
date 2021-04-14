---
description: Se você estiver digitando as mesmas expressões JavaScript no Console repetidamente, experimente Expressões Ao Vivo.
title: Assista aos valores de expressão javascript em tempo real com expressões ao vivo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento na Web, ferramentas F12, devtools
ms.openlocfilehash: 51b7aa5119775f43861a84c1055ac9149a626d8a
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483111"
---
# <a name="monitor-changes-in-javascript-using-live-expressions"></a><span data-ttu-id="39203-104">Monitorar alterações em JavaScript usando expressões ao vivo</span><span class="sxs-lookup"><span data-stu-id="39203-104">Monitor changes in JavaScript using Live Expressions</span></span>  

<span data-ttu-id="39203-105">**Expressões ao vivo** são uma excelente maneira de monitorar expressões JavaScript que mudam muito.</span><span class="sxs-lookup"><span data-stu-id="39203-105">**Live Expressions** are an excellent way to monitor JavaScript expressions that change a lot.</span></span>    <span data-ttu-id="39203-106">Em vez de ter muitas mensagens de Console para ler e navegar, você pode fixar suas expressões JavaScript específicas na parte superior do **Console**.</span><span class="sxs-lookup"><span data-stu-id="39203-106">Instead of having many Console messages to read and navigate, you may pin your specific JavaScript expressions to the top of the **Console**.</span></span>  

## <a name="add-a-new-live-expression"></a><span data-ttu-id="39203-107">Adicionar uma nova expressão ao vivo</span><span class="sxs-lookup"><span data-stu-id="39203-107">Add a new live expression</span></span>  

<span data-ttu-id="39203-108">Para começar, escolha o **botão Criar expressão ao vivo** \(eye\) ao lado da caixa de texto **Filtrar.**</span><span class="sxs-lookup"><span data-stu-id="39203-108">To start, choose the **Create live expression** \(eye\) button next to the **Filter** textbox.</span></span>  <span data-ttu-id="39203-109">Depois de escolher, uma caixa de texto é exibida para que você insira sua nova expressão nele.</span><span class="sxs-lookup"><span data-stu-id="39203-109">After you choose it, a textbox is displayed for you to enter your new expression in it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-new.msft.png" alt-text="Escolha o botão Nova expressão ao vivo para abrir uma caixa de texto para digitar uma expressão" lightbox="../media/console-live-expressions-new.msft.png":::
    <span data-ttu-id="39203-111">Escolha o `New live expression` botão para abrir uma caixa de texto para digitar uma expressão</span><span class="sxs-lookup"><span data-stu-id="39203-111">Choose the `New live expression` button to open a textbox to type an expression</span></span>  
:::image-end:::  

<span data-ttu-id="39203-112">**Expressões ao vivo** podem ser qualquer expressão JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="39203-112">**Live Expressions** may be any valid JavaScript expression.</span></span>  <span data-ttu-id="39203-113">Para experimentar, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="39203-113">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="39203-114">Abra a **caixa de texto Expressão Ao** Vivo.</span><span class="sxs-lookup"><span data-stu-id="39203-114">Open the **Live Expression** textbox.</span></span>  
1.  <span data-ttu-id="39203-115">Digite `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="39203-115">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="39203-116">Para salvar a expressão, conclua uma das seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="39203-116">To save the expression, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="39203-117">Selecione `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` ou \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="39203-117">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    *   <span data-ttu-id="39203-118">Escolha fora da **caixa de texto Expressão Ao** Vivo.</span><span class="sxs-lookup"><span data-stu-id="39203-118">Choose outside the **Live Expression** textbox.</span></span>  
        
<span data-ttu-id="39203-119">A expressão agora está ao vivo e `body` é exibida como resultado.</span><span class="sxs-lookup"><span data-stu-id="39203-119">The expression is now live and displays `body` as the result.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element.msft.png" alt-text="Expressão ao vivo para document.activeElement exibe o corpo como o resultado" lightbox="../media/console-live-expressions-document-active-element.msft.png":::
    <span data-ttu-id="39203-121">Expressão ao vivo `document.activeElement` para exibe o corpo como resultado</span><span class="sxs-lookup"><span data-stu-id="39203-121">Live expression for `document.activeElement` displays body as the result</span></span>  
:::image-end:::  

<span data-ttu-id="39203-122">Se você navegar pela página da Web, o valor será alterando.</span><span class="sxs-lookup"><span data-stu-id="39203-122">If you navigate around the webpage, the value changes.</span></span>  <span data-ttu-id="39203-123">Por exemplo, na figura a seguir, você abre o menu de pesquisa na página da Web e a expressão agora é exibida `button.nav-bar-button.focus-visible` como o valor.</span><span class="sxs-lookup"><span data-stu-id="39203-123">For example, in the following figure you open the search menu in the webpage and the expression now displays `button.nav-bar-button.focus-visible` as the value.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-nav-button.msft.png" alt-text="Para alterar o valor da Expressão Ao Vivo, interaja com diferentes elementos na página da Web" lightbox="../media/console-live-expressions-document-active-element-nav-button.msft.png":::
    <span data-ttu-id="39203-125">Para alterar o valor da **Expressão Ao Vivo**, interaja com diferentes elementos na página da Web</span><span class="sxs-lookup"><span data-stu-id="39203-125">To change the value of the **Live Expression**, interact with different elements on the webpage</span></span>  
:::image-end:::  

<span data-ttu-id="39203-126">Para alterar o valor novamente, abra e escolha a caixa de texto Pesquisar na página da Web.</span><span class="sxs-lookup"><span data-stu-id="39203-126">To change the value again, open and choose the Search textbox on the webpage.</span></span>  

:::image type="complex" source="../media/console-live-expressions-document-active-element-search.msft.png" alt-text="Navegue até um elemento diferente na página da Web para atualizar a Expressão Ao Vivo" lightbox="../media/console-live-expressions-document-active-element-search.msft.png":::
    <span data-ttu-id="39203-128">Navegue até um elemento diferente na página da Web para atualizar a **Expressão Ao Vivo**</span><span class="sxs-lookup"><span data-stu-id="39203-128">Navigate to a different element in the webpage to update the **Live Expression**</span></span>  
:::image-end:::  

## <a name="remove-live-expressions"></a><span data-ttu-id="39203-129">Remover expressões ao vivo</span><span class="sxs-lookup"><span data-stu-id="39203-129">Remove Live Expressions</span></span>  

<span data-ttu-id="39203-130">Uma **expressão ao vivo** está disponível desde que você a mantenha ativa.</span><span class="sxs-lookup"><span data-stu-id="39203-130">A **Live Expression** is available as long as you keep it active.</span></span>  <span data-ttu-id="39203-131">Para se livrar de uma **expressão ao vivo,** escolha `x` o próximo a ela.</span><span class="sxs-lookup"><span data-stu-id="39203-131">To get rid of a **Live Expression**, choose the `x` next to it.</span></span>  

:::image type="complex" source="../media/console-live-expressions-remove.msft.png" alt-text="Para remover expressões ao vivo, escolha o x ao lado dele" lightbox="../media/console-live-expressions-remove.msft.png":::
    <span data-ttu-id="39203-133">Para remover **Expressões Ao Vivo,** escolha `x` o próximo a ele</span><span class="sxs-lookup"><span data-stu-id="39203-133">To remove **Live Expressions**, choose the `x` next to it</span></span>  
:::image-end:::  

## <a name="replace-console-logging-with-live-expressions"></a><span data-ttu-id="39203-134">Substituir o registro em log de console por expressões ao vivo</span><span class="sxs-lookup"><span data-stu-id="39203-134">Replace Console logging with Live Expressions</span></span>  

<span data-ttu-id="39203-135">Você pode criar quantas expressões quiser e persistir em todas as sessões do navegador e janelas.</span><span class="sxs-lookup"><span data-stu-id="39203-135">You may create as many expressions as you want and persist each across browser sessions and windows.</span></span>  <span data-ttu-id="39203-136">**Expressões ao vivo** são uma maneira de reduzir o ruído no fluxo de trabalho de depuração.</span><span class="sxs-lookup"><span data-stu-id="39203-136">**Live Expressions** are a way to cut down on noise in your debugging workflow.</span></span>  

<span data-ttu-id="39203-137">Por exemplo, você deseja monitorar o movimento do mouse na página da Web atual.</span><span class="sxs-lookup"><span data-stu-id="39203-137">For example, you want to monitor the mouse movement in the current webpage.</span></span>  <span data-ttu-id="39203-138">Navegue [até Logging Mouse Movement demo][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml], abra o **Console**e mova o mouse para exibir os logs com muitas informações.</span><span class="sxs-lookup"><span data-stu-id="39203-138">Navigate to [Logging Mouse Movement demo][GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml], open the **Console**, and move your mouse around to display the logs with a lot of information.</span></span>  

:::image type="complex" source="../media/console-live-expression-mouse-logging.msft.png" alt-text="Console exibe muitas informações sobre a posição do mouse" lightbox="../media/console-live-expression-mouse-logging.msft.png":::
    <span data-ttu-id="39203-140">**Console** exibe muitas informações sobre a posição do mouse</span><span class="sxs-lookup"><span data-stu-id="39203-140">**Console** displays much information on mouse position</span></span>  
:::image-end:::  

<span data-ttu-id="39203-141">A grande quantidade de informações não só retarda o processo de depuração, como também facilita a falta das alterações que você deseja revisar.</span><span class="sxs-lookup"><span data-stu-id="39203-141">The large amount of information not only slows your debug process, but also makes it easy to miss the changes you want to review.</span></span>  <span data-ttu-id="39203-142">À medida **que o Console** exibe mais mensagens e você move o mouse, os valores que você deseja revisar rolam para fora da tela.</span><span class="sxs-lookup"><span data-stu-id="39203-142">As the **Console** displays more messages and you move your mouse, the values you want to review scroll off the screen.</span></span>  

<span data-ttu-id="39203-143">Para experimentar **Expressões Ao Vivo** como uma alternativa, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="39203-143">To try **Live Expressions** as an alternative, complete the following actions.</span></span>  

1.  <span data-ttu-id="39203-144">Navegue até o [movimento do mouse sem registrar a demonstração][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].</span><span class="sxs-lookup"><span data-stu-id="39203-144">Navigate to the [Mouse movement without logging demo][GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml].</span></span>  
1.  <span data-ttu-id="39203-145">Criar **Expressões Ao Vivo** para e `x` `y` .</span><span class="sxs-lookup"><span data-stu-id="39203-145">Create **Live Expressions** for `x` and `y`.</span></span>  
    
<span data-ttu-id="39203-146">Ao usar **expressões**ao vivo, você sempre obterá as informações na mesma parte da tela e manterá logs de **Console** para valores que não mudam tanto.</span><span class="sxs-lookup"><span data-stu-id="39203-146">When you use **Live Expressions**, you always get the information on the same part of your screen and keep **Console** logs for values that don't change as much.</span></span>

:::image type="complex" source="../media/console-live-expressions-x-and-y.msft.png" alt-text="Exibir a posição x e y do mouse como Expressões Ao Vivo" lightbox="../media/console-live-expressions-x-and-y.msft.png":::
    <span data-ttu-id="39203-148">Exibir a `x` posição e do mouse como `y` **Expressões Ao Vivo**</span><span class="sxs-lookup"><span data-stu-id="39203-148">Display the `x` and `y` position of the mouse as **Live Expressions**</span></span>  
:::image-end:::  

<span data-ttu-id="39203-149">**Expressões ao vivo** são executados exclusivamente no computador e você não precisa alterar nada em seu código para exibição.</span><span class="sxs-lookup"><span data-stu-id="39203-149">**Live Expressions** run exclusively on your computer and you don't need to change anything in your code to display.</span></span>  <span data-ttu-id="39203-150">**Expressões ao vivo** são uma ótima maneira de garantir que você apenas exibe as informações que deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="39203-150">**Live Expressions** are a great way to ensure that you only display the information you want to debug.</span></span>  <span data-ttu-id="39203-151">Além disso, **expressões ao** vivo ajudam a limitar o ruído nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="39203-151">Also, **Live Expressions** help you limit the noise on your users' computers.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="39203-152">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="39203-152">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleMousemoveHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove.html "Exemplos de mensagens de console: usando a tabela | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleMouseNoLogHtml]: https://microsoftedge.github.io/DevToolsSamples/console/mousemove-no-log.html "Movimento do mouse sem registro em log | GitHub"  
