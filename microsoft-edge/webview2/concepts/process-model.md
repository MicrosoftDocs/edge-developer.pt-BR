---
description: Modelo de processo
title: Modelo de processo | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 95d0c53219114c47a781317ab4b2ee2028fc586f
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535612"
---
# <a name="process-model"></a><span data-ttu-id="05b4e-104">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="05b4e-104">Process model</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="05b4e-105">Plataformas com suporte:</span><span class="sxs-lookup"><span data-stu-id="05b4e-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="05b4e-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="05b4e-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="05b4e-107">O WebView2 usa o mesmo modelo de processo que o Microsoft Edge navegador.</span><span class="sxs-lookup"><span data-stu-id="05b4e-107">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="05b4e-108">Para obter mais informações sobre o modelo de processo do navegador, navegue até Arquitetura do Navegador - Confira o [navegador da Web moderno.][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]</span><span class="sxs-lookup"><span data-stu-id="05b4e-108">For more information about the browser process model, navigate to [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span>  

<span data-ttu-id="05b4e-109">Um processo de navegador está associado aos processos de renderização e outros processos utilitários, conforme descrito neste artigo.</span><span class="sxs-lookup"><span data-stu-id="05b4e-109">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="05b4e-110">Além disso, se WebView2 for especificado, os processos de solicitação do aplicativo host usarão WebView2.</span><span class="sxs-lookup"><span data-stu-id="05b4e-110">Additionally, if WebView2 is specified, the host app requesting processes use WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processo 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="05b4e-112">Processo 1</span><span class="sxs-lookup"><span data-stu-id="05b4e-112">Process 1</span></span>  
:::image-end:::    

<span data-ttu-id="05b4e-113">Um processo de navegador é associado a apenas uma pasta de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="05b4e-113">A browser process is associated with only one user data folder.</span></span>  <span data-ttu-id="05b4e-114">Um processo de solicitação pode especificar mais de uma pasta de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="05b4e-114">A request process may specify more than one user data folder.</span></span>  <span data-ttu-id="05b4e-115">Um processo de solicitação que especifica mais de uma pasta de dados do usuário está associado ao mesmo número de processos do navegador.</span><span class="sxs-lookup"><span data-stu-id="05b4e-115">A request process that specifies more than one user data folder is associated with the same number of browser processes.</span></span>  
<span data-ttu-id="05b4e-116">Por exemplo, um processo de solicitação que solicita acesso a duas pastas de dados do usuário usa dois processos de navegador.</span><span class="sxs-lookup"><span data-stu-id="05b4e-116">For example, a request process that requests access to two user data folders uses two browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processo 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="05b4e-118">Processo 2</span><span class="sxs-lookup"><span data-stu-id="05b4e-118">Process 2</span></span>  
:::image-end:::    

<span data-ttu-id="05b4e-119">Um processo de navegador está associado a vários processos de renderização.</span><span class="sxs-lookup"><span data-stu-id="05b4e-119">A browser process is associated with several renderer processes.</span></span>  <span data-ttu-id="05b4e-120">Uma instância do WebView 2 cria um processo de navegador para quadros de serviço.</span><span class="sxs-lookup"><span data-stu-id="05b4e-120">A WebView 2 instance creates a browser process to service frames.</span></span>  <span data-ttu-id="05b4e-121">Um processo de navegador pode estar associado a vários quadros.</span><span class="sxs-lookup"><span data-stu-id="05b4e-121">A browser process may be associated with multiple frames.</span></span>  <span data-ttu-id="05b4e-122">Um processo de navegador pode ser associado a instâncias diferentes do WebView2.</span><span class="sxs-lookup"><span data-stu-id="05b4e-122">A browser process may be associated with different instances of WebView2.</span></span>  <span data-ttu-id="05b4e-123">O número de processos de renderização varia com base nas seguintes condições.</span><span class="sxs-lookup"><span data-stu-id="05b4e-123">The number of render processes varies based on the following conditions.</span></span>  

*   <span data-ttu-id="05b4e-124">Uso do recurso de isolamento de site no navegador.</span><span class="sxs-lookup"><span data-stu-id="05b4e-124">Use of the website isolation feature in your browser.</span></span>  
*   <span data-ttu-id="05b4e-125">O número de origens desconectadas distintas renderizadas em instâncias associadas de WebView2.</span><span class="sxs-lookup"><span data-stu-id="05b4e-125">The number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  
    
<span data-ttu-id="05b4e-126">O recurso de navegador de isolamento de site é descrito no conteúdo anterior.</span><span class="sxs-lookup"><span data-stu-id="05b4e-126">The website isolation browser feature is described in the previous content.</span></span> 
<!--todo:  which previous content?  -->  

<span data-ttu-id="05b4e-127">Representa `CoreWebView2Environment` uma pasta de dados do usuário e um processo de navegador.</span><span class="sxs-lookup"><span data-stu-id="05b4e-127">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="05b4e-128">O não corresponde diretamente a nenhum conjunto de processos, pois vários processos renderer são usados por um WebView2, dependendo do isolamento do `CoreWebView2` site, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="05b4e-128">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on website isolation as previously described.</span></span>  

<span data-ttu-id="05b4e-129">Para reagir a falhas e travamentos nos processos do navegador e do renderador, use o `ProcessFailed` evento `CoreWebView2` de .</span><span class="sxs-lookup"><span data-stu-id="05b4e-129">To react to crashes and hangs in the browser and renderer processes, use the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="05b4e-130">Para desligar com segurança os processos de renderização e navegador associados, use o `Close` método `CoreWebView2Controller` de .</span><span class="sxs-lookup"><span data-stu-id="05b4e-130">To safely shut down associated browser and renderer processes, use the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="05b4e-131">Para abrir a janela Gerenciador de Tarefas do Navegador na janela **DevTools** de uma instância do WebView2, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="05b4e-131">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, complete on of the following actions.</span></span>  

*   <span data-ttu-id="05b4e-132">Selecione `Shift` + `Escape` .</span><span class="sxs-lookup"><span data-stu-id="05b4e-132">Select `Shift`+`Escape`.</span></span>  
*   <span data-ttu-id="05b4e-133">Passe o mouse na barra de título da janela DevTools, abra o menu contextual \(clique com o botão direito do mouse\) e escolha `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="05b4e-133">Hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  
    
<span data-ttu-id="05b4e-134">Todos os processos associados ao processo de navegador do WebView2 são exibidos, incluindo finalidades associadas.</span><span class="sxs-lookup"><span data-stu-id="05b4e-134">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05b4e-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05b4e-135">See also</span></span>  

*   <span data-ttu-id="05b4e-136">Para Introdução WebView2, navegue até [WebView2 Introdução Guias.][Webview2IndexGetStarted]</span><span class="sxs-lookup"><span data-stu-id="05b4e-136">To Get Started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="05b4e-137">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] em GitHub.</span><span class="sxs-lookup"><span data-stu-id="05b4e-137">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="05b4e-138">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="05b4e-138">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="05b4e-139">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="05b4e-139">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="05b4e-140">Entrar em contato com a equipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="05b4e-140">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "WebView2 Class | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitetura do Navegador - Veja o navegador da Web moderno (parte 1)"  
