---
description: Modo IE e o Microsoft Edge (Chromium) DevTools
title: Modo Internet Explorer e o DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, ie11, Internet Explorer 11, modo IE
ms.openlocfilehash: c88da78e073a75a664561aba899ca5c8ada78477
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231275"
---
# <span data-ttu-id="fc5f1-104">Modo Internet Explorer e o DevTools</span><span class="sxs-lookup"><span data-stu-id="fc5f1-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="fc5f1-105">Este artigo descreve como o modo \ (IE Mode \) do Internet Explorer integra-se com o DevTools Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <span data-ttu-id="fc5f1-106">Noções básicas sobre o modo IE</span><span class="sxs-lookup"><span data-stu-id="fc5f1-106">Understanding IE mode</span></span>  

<span data-ttu-id="fc5f1-107">O modo IE permite que as empresas especifiquem uma lista de sites da Web que só funcionam no Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="fc5f1-108">Quando você navegar para esses sites no Microsoft Edge \ (Chromium \), uma instância do Internet Explorer 11 será executada e renderizará o site em uma guia.  A funcionalidade permite às empresas gerenciar a compatibilidade com tecnologias que atualmente não são compatíveis com qualquer navegador da Web moderno.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="fc5f1-109">O suporte para as seguintes tecnologias está incluído no modo IE.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="fc5f1-110">Modos de documento do IE</span><span class="sxs-lookup"><span data-stu-id="fc5f1-110">IE document modes</span></span>  
*   <span data-ttu-id="fc5f1-111">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="fc5f1-111">ActiveX controls</span></span>  
*   <span data-ttu-id="fc5f1-112">outros componentes herdados</span><span class="sxs-lookup"><span data-stu-id="fc5f1-112">other legacy components</span></span>  

<span data-ttu-id="fc5f1-113">No modo IE, o processo de renderização é baseado no Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="fc5f1-114">O Gerenciador de processos do Microsoft Edge \ (Chromium \) manipula o tempo de vida do processo de renderização.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="fc5f1-115">Ele é restrito ao tempo de vida da guia para um site específico \ (ou app \).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="fc5f1-116">Quando uma guia é renderizada no modo IE, um emblema é exibido na barra de endereços para a guia específica.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Selo do modo do IE na barra de endereços" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="fc5f1-118">Selo do modo do IE na barra de endereços</span><span class="sxs-lookup"><span data-stu-id="fc5f1-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="fc5f1-119">No momento, o modo do IE está disponível no Windows 10 versão 1903 \ (atualização de maio de 2019), mas estará disponível em breve para todas as plataformas do Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <span data-ttu-id="fc5f1-120">Iniciando o DevTools em uma guia no modo IE</span><span class="sxs-lookup"><span data-stu-id="fc5f1-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="fc5f1-121">Se você estiver tentando exibir o modo de documento de um site no modo IE, escolha o selo na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Exibir o modo de documento usando o selo do modo IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="fc5f1-123">Exibir o modo de documento usando o selo do modo IE</span><span class="sxs-lookup"><span data-stu-id="fc5f1-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="fc5f1-124">Se uma guia estiver usando o modo IE, o DevTools não funcionará e as seguintes condições ocorrerão.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="fc5f1-125">Se você selecionar `F12` ou selecionar `Ctrl` + `Shift` + `I` uma instância em branco do Microsoft Edge \ (Chromium \) devtools será inicializada exibirá a mensagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="fc5f1-126">Se você abrir um menu contextual \ (clique com o botão direito do mouse \) e escolher **Exibir fonte**, o bloco de notas será iniciado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="fc5f1-127">Se você abrir um menu contextual \ (clique com o botão direito do mouse \), o **elemento inspecionar** não ficará visível.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="fc5f1-128">O motivo pelo qual um número de ferramentas na DevTools \ (como as ferramentas de **rede** e **desempenho** \) não funciona é o mecanismo de renderização switches do Chromium para o Internet Explorer 11 no modo IE.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="fc5f1-129">Para enviar comentários, navegue até entrar [em contato com a equipe do Microsoft Edge devtools](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools iniciado no modo IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="fc5f1-131">DevTools iniciado no modo IE</span><span class="sxs-lookup"><span data-stu-id="fc5f1-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="fc5f1-132">Para testar seu site baseado no Internet Explorer 11 (ou app \) no Internet Explorer 11 e no modo IE, siga as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="fc5f1-133">Abra o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="fc5f1-134">No Windows 10, localize o atalho para o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="fc5f1-135">**Menu iniciar**  >  **Acessórios**  >  do Windows **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="fc5f1-136">No Windows 7, localize o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="fc5f1-137">**Menu iniciar**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="fc5f1-138">No Internet Explorer 11, abra a mesma página da Web.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="fc5f1-139">Inicie o Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="fc5f1-140">Selecione `F12` .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="fc5f1-141">Passe o mouse em qualquer lugar, abra um menu contextual \ (clique com o botão direito do mouse \) e escolha **inspecionar elemento**.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="fc5f1-142">Para obter mais informações sobre como usar essas ferramentas, navegue até [usando as ferramentas de desenvolvedor F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span><span class="sxs-lookup"><span data-stu-id="fc5f1-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <span data-ttu-id="fc5f1-143">Depuração remota e modo IE</span><span class="sxs-lookup"><span data-stu-id="fc5f1-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="fc5f1-144">Inicie o Microsoft Edge \ (Chromium \) com a depuração remota ativada na interface de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="fc5f1-145">O Visual Studio, o código do Visual Studio e outras ferramentas de desenvolvimento normalmente executam um comando para iniciar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-145">Visual Studio, Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="fc5f1-146">O comando a seguir inicia o Microsoft Edge com a porta de depuração remota definida como `9222` .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="fc5f1-147">Depois de iniciar o Microsoft Edge \ (Chromium \) usando um argumento de linha de comando, o modo IE não está disponível.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="fc5f1-148">Você ainda pode navegar para os sites \ (ou aplicativos \) que, de outra forma, seriam exibidos no modo IE.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-148">You may still navigate to websites \(or apps\) that would otherwise display in IE mode.</span></span>  <span data-ttu-id="fc5f1-149">O conteúdo do site \ (ou app \) é renderizado usando Chromium, não o Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="fc5f1-150">Espere que as partes das páginas da Web que dependem de IE11, como controles ActiveX, não sejam renderizadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-150">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="fc5f1-151">O selo do modo do IE não aparece na barra de endereços.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="fc5f1-152">O modo IE permanecerá indisponível até você fechar completamente e reiniciar o Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="fc5f1-153">Entrar em contato com a equipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fc5f1-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Usar as ferramentas de desenvolvedor F12 | Documentos da Microsoft"  
