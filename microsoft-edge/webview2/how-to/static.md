---
description: Saiba como vincular estaticamente a biblioteca do carregador WebView2.
title: Como vincular estaticamente a biblioteca do carregador WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 8f48a4fde9e2960de6156fc14db8c84f87a49868
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535743"
---
# <a name="statically-link-the-webview2-loader-library"></a><span data-ttu-id="6ed15-104">Vincular estaticamente a biblioteca do carregador WebView2</span><span class="sxs-lookup"><span data-stu-id="6ed15-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="6ed15-105">Talvez você queira distribuir seu aplicativo com um único arquivo executável, em vez de um pacote de muitos arquivos.</span><span class="sxs-lookup"><span data-stu-id="6ed15-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="6ed15-106">Para criar um único arquivo executável ou reduzir o tamanho do pacote, você deve vincular estáticamente os arquivos WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="6ed15-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="6ed15-107">O SDK WebView2 contém um arquivo de header `WebView2Loader.dll` e o `IDL` arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ed15-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="6ed15-108">é um pequeno componente que ajuda os aplicativos a localizar o Tempo de Execução webView2 ou canais não estáveis de Microsoft Edge, no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ed15-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="6ed15-109">Para aplicativos que não querem enviar `WebView2Loader.dll` um , conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed15-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="6ed15-110">Abra o arquivo de projeto para seu aplicativo em um editor de `.vcxproj` texto, como Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="6ed15-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6ed15-111">O `.vcproj` arquivo do projeto pode ser um arquivo oculto, o que significa que ele não é exibido Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6ed15-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="6ed15-112">Use a linha de comando para encontrar arquivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="6ed15-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="6ed15-113">Localize a seção no código em que você inclui os arquivos de destino do pacote WebView2 NuGet pacote.</span><span class="sxs-lookup"><span data-stu-id="6ed15-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="6ed15-114">O local no código é realçado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ed15-114">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Project Trecho de código de arquivos" lightbox="./media/insert-here.png":::
       <span data-ttu-id="6ed15-116">Project Trecho de código de arquivos</span><span class="sxs-lookup"><span data-stu-id="6ed15-116">Project Files code snippet</span></span>   
    :::image-end:::  
    
1.  <span data-ttu-id="6ed15-117">Copie o trecho de código a seguir e o colar onde o `Microsoft.Web.WebView2.targets` está incluído.</span><span class="sxs-lookup"><span data-stu-id="6ed15-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Trecho de código inserido" lightbox="./media/static-lib.png":::
       <span data-ttu-id="6ed15-119">Trecho de código inserido</span><span class="sxs-lookup"><span data-stu-id="6ed15-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6ed15-120">Edite as dependências adicionais da configuração de com build para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed15-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="6ed15-121">Para começar, encontre todas as `<AdditionalDependencies>` marcas.</span><span class="sxs-lookup"><span data-stu-id="6ed15-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="6ed15-122">Para cada um deles, `version.lib` adicione como uma dependência adicional a cada configuração de com build diferente no `.vcxproj` arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ed15-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Adicionando version.lib a ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       <span data-ttu-id="6ed15-124">Adicionando `version.lib` ao</span><span class="sxs-lookup"><span data-stu-id="6ed15-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="6ed15-125">A equipe webView2 tem como objetivo automatizar a adição da dependência adicional em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="6ed15-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1.  <span data-ttu-id="6ed15-126">Compile e execute seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ed15-126">Compile and run your app.</span></span>  
    
## <a name="getting-in-touch-with-the-webview2-team"></a><span data-ttu-id="6ed15-127">Entrar em contato com a equipe webView2</span><span class="sxs-lookup"><span data-stu-id="6ed15-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a><span data-ttu-id="6ed15-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6ed15-128">See also</span></span>  

*   <span data-ttu-id="6ed15-129">Para começar a usar WebView2, navegue até [WebView2 Introdução Guias][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="6ed15-129">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="6ed15-130">Para um exemplo abrangente de recursos WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samples] em GitHub.</span><span class="sxs-lookup"><span data-stu-id="6ed15-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="6ed15-131">Para obter informações mais detalhadas sobre APIs WebView2, navegue até [referência de API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="6ed15-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="6ed15-132">Para obter mais informações sobre WebView2, navegue até [Recursos WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="6ed15-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge (Chromium) ferramentas de desenvolvedor | Microsoft Docs"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Referência da API WebView2 | Microsoft Docs"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  
[Webview2MainGetStarted]: ../index.md#get-started "Introdução - Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Novidades? - Depurador JavaScript para Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (Chromium) Aplicativos WebView - Visual Studio Code - Depurador para Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
