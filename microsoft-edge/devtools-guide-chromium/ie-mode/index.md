---
description: Modo IE e o Microsoft Edge (Chromium) DevTools
title: Modo Internet Explorer e o DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, ie11, internet explorer 11, modo ie
ms.openlocfilehash: 070bf970c784b4f2173ebc52e4494fc6807b4a8e
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643232"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="0e927-104">Modo Internet Explorer e o DevTools</span><span class="sxs-lookup"><span data-stu-id="0e927-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="0e927-105">Este artigo descreve como o modo do Internet Explorer \(modo IE\) se integra ao Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="0e927-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="0e927-106">Noções básicas sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="0e927-106">Understanding IE mode</span></span>  

<span data-ttu-id="0e927-107">O modo IE permite que as empresas especifiquem uma lista de sites que funcionam apenas no Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0e927-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="0e927-108">Quando você navega para esses sites em Microsoft Edge \(Chromium\), uma instância do Internet Explorer 11 é executado e renderiza o site em uma guia.  A funcionalidade permite que as empresas gerenciem a compatibilidade com tecnologias que atualmente não são compatíveis com nenhum navegador moderno da Web.</span><span class="sxs-lookup"><span data-stu-id="0e927-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="0e927-109">O suporte para as seguintes tecnologias está incluído no modo IE.</span><span class="sxs-lookup"><span data-stu-id="0e927-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="0e927-110">Modos de documento do IE</span><span class="sxs-lookup"><span data-stu-id="0e927-110">IE document modes</span></span>  
*   <span data-ttu-id="0e927-111">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="0e927-111">ActiveX controls</span></span>  
*   <span data-ttu-id="0e927-112">outros componentes herdados</span><span class="sxs-lookup"><span data-stu-id="0e927-112">other legacy components</span></span>  

<span data-ttu-id="0e927-113">No modo IE, o processo de renderização é baseado no Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0e927-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="0e927-114">O Microsoft Edge do processo \(Chromium\) lida com o tempo de vida do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="0e927-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="0e927-115">Ele é restrito ao tempo de vida da guia para um site específico \(ou app\).</span><span class="sxs-lookup"><span data-stu-id="0e927-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="0e927-116">Quando uma guia é renderiza no modo IE, um selo aparece na barra de endereços da guia específica.</span><span class="sxs-lookup"><span data-stu-id="0e927-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Selo do modo IE na barra de endereços" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="0e927-118">Selo do modo IE na barra de endereços</span><span class="sxs-lookup"><span data-stu-id="0e927-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="0e927-119">O modo IE está disponível no momento no Windows 10 Versão 1903 \(Atualização de maio de 2019\), mas está chegando em breve a todas as plataformas Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="0e927-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="0e927-120">Iniciando o DevTools em uma guia no modo IE</span><span class="sxs-lookup"><span data-stu-id="0e927-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="0e927-121">Se você estiver tentando exibir o modo de documento de um site no modo IE, escolha o selo na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="0e927-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Exibir o modo de documento usando o selo do modo IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="0e927-123">Exibir o modo de documento usando o selo do modo IE</span><span class="sxs-lookup"><span data-stu-id="0e927-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="0e927-124">Se uma guia estiver usando o modo IE, o DevTools não funcionará e as seguintes condições ocorrerão.</span><span class="sxs-lookup"><span data-stu-id="0e927-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="0e927-125">Se você selecionar ou selecionar , uma instância em branco do `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools será lançada exibirá a seguinte mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e927-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="0e927-126">Se você abrir um menu contextual \(clique com o botão direito do mouse\) e escolher **Exibir Fonte**, Bloco de notas será lançado.</span><span class="sxs-lookup"><span data-stu-id="0e927-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="0e927-127">Se você abrir um menu contextual \(clique com o botão direito do mouse\), o **Elemento Inspect** não será visível.</span><span class="sxs-lookup"><span data-stu-id="0e927-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="0e927-128">O motivo pelo qual várias ferramentas dentro do DevTools \*\*\*\* \(como as ferramentas de Rede e Desempenho\) não funcionam é que o mecanismo de renderização alterna do Chromium para o Internet Explorer 11 no modo IE. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0e927-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="0e927-129">Para fornecer comentários, navegue até Entrar em [contato com a equipe Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="0e927-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools lançado no modo IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="0e927-131">DevTools lançado no modo IE</span><span class="sxs-lookup"><span data-stu-id="0e927-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="0e927-132">Para testar seu site baseado no Internet Explorer 11 \(ou app\) no modo Internet Explorer 11 e IE, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e927-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="0e927-133">Abra o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0e927-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="0e927-134">No Windows 10, localize o atalho para o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0e927-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="0e927-135">**Menu Iniciar**  >  **Windows Acessórios**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="0e927-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="0e927-136">No Windows 7, localize o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0e927-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="0e927-137">**Menu Iniciar**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="0e927-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="0e927-138">No Internet Explorer 11, abra a mesma página da Web.</span><span class="sxs-lookup"><span data-stu-id="0e927-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="0e927-139">Iniciar o Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="0e927-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="0e927-140">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="0e927-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="0e927-141">Passe o mouse em qualquer lugar, abra um menu contextual \(clique com o botão direito do mouse\) e escolha **Inspecionar elemento**.</span><span class="sxs-lookup"><span data-stu-id="0e927-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="0e927-142">Para obter mais informações sobre como usar essas ferramentas, navegue até [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="0e927-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

<span data-ttu-id="0e927-143">Se o Internet Explorer 11 não estiver disponível, como no Windows 11, você poderá usar o IEChooser para iniciar o Internet Explorer DevTools para depurar o conteúdo das guias de modo IE.</span><span class="sxs-lookup"><span data-stu-id="0e927-143">If Internet Explorer 11 is not available, such as on Windows 11, you can use IEChooser to launch the Internet Explorer DevTools to debug the content of your IE mode tabs.</span></span> <span data-ttu-id="0e927-144">Para usar o IEChooser, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e927-144">To use IEChooser, perform the following steps.</span></span>

1.  <span data-ttu-id="0e927-145">Abra IEChooser.</span><span class="sxs-lookup"><span data-stu-id="0e927-145">Open IEChooser.</span></span>
    1. <span data-ttu-id="0e927-146">Abra a caixa de diálogo Executar.</span><span class="sxs-lookup"><span data-stu-id="0e927-146">Open the Run dialog box.</span></span> <span data-ttu-id="0e927-147">Por exemplo, pressione `Windows logo key`  +  `R` o .</span><span class="sxs-lookup"><span data-stu-id="0e927-147">For example, press the `Windows logo key` + `R`.</span></span>
    2. <span data-ttu-id="0e927-148">Insira `%systemroot%\system32\f12\IEChooser.exe` e selecione **Ok**.</span><span class="sxs-lookup"><span data-stu-id="0e927-148">Enter `%systemroot%\system32\f12\IEChooser.exe`, and then select **Ok**.</span></span>
2.  <span data-ttu-id="0e927-149">No IEChooser, selecione a entrada para a guia Modo IE.</span><span class="sxs-lookup"><span data-stu-id="0e927-149">In IEChooser, select the entry for the IE mode tab.</span></span>


## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="0e927-150">Modo de depuração remota e IE</span><span class="sxs-lookup"><span data-stu-id="0e927-150">Remote debugging and IE mode</span></span>  

<span data-ttu-id="0e927-151">Iniciar Microsoft Edge \(Chromium\) com a depuração remota acionda a partir da interface de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0e927-151">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="0e927-152">Microsoft Visual Studio, Microsoft Visual Studio Código e outras ferramentas de desenvolvimento normalmente executem um comando para iniciar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0e927-152">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="0e927-153">O comando a seguir inicia Microsoft Edge com a porta de depuração remota definida como `9222` .</span><span class="sxs-lookup"><span data-stu-id="0e927-153">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="0e927-154">Depois de iniciar Microsoft Edge \(Chromium\) usando um argumento de linha de comando, o modo IE fica indisponível.</span><span class="sxs-lookup"><span data-stu-id="0e927-154">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="0e927-155">Você ainda pode navegar para sites \(ou aplicativos\) que são exibidos de outra forma no modo IE.</span><span class="sxs-lookup"><span data-stu-id="0e927-155">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="0e927-156">O conteúdo do site \(ou app\) é render Chromium, não o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="0e927-156">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="0e927-157">Espere que as partes das páginas da Web que dependem do IE11, como controles ActiveX, não renderizar corretamente.</span><span class="sxs-lookup"><span data-stu-id="0e927-157">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="0e927-158">O selo do modo IE não aparece na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="0e927-158">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="0e927-159">O modo IE permanece indisponível até que você feche completamente e reinicie Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="0e927-159">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0e927-160">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0e927-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Usando as ferramentas de desenvolvedor F12 | Microsoft Docs"  
