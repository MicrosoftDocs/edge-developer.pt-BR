---
description: Saiba como vincular estaticamente a biblioteca WebView2 Loader.
title: Como vincular estaticamente a biblioteca WebView2 Loader
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 880e9ed809dc268ee0b30b6ee3b5996711f54300
ms.sourcegitcommit: 0ded671914aae231493f418dd7645a04361dca1b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120121"
---
# <span data-ttu-id="83e71-104">Vincule estaticamente a biblioteca WebView2 Loader</span><span class="sxs-lookup"><span data-stu-id="83e71-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="83e71-105">Você pode querer distribuir seu aplicativo com um único arquivo executável, em vez de um pacote de muitos arquivos.</span><span class="sxs-lookup"><span data-stu-id="83e71-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="83e71-106">Para criar um único arquivo executável ou reduzir o tamanho do seu pacote, você deve vincular estaticamente os arquivos WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="83e71-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="83e71-107">O SDK do WebView2 contém um arquivo de cabeçalho, `WebView2Loader.dll` e o `IDL` arquivo.</span><span class="sxs-lookup"><span data-stu-id="83e71-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="83e71-108">é um componente pequeno que ajuda os aplicativos a localizar o tempo de execução do WebView2 ou os canais não estáveis do Microsoft Edge, no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="83e71-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="83e71-109">Para os aplicativos que não querem enviar a uma `WebView2Loader.dll` , conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="83e71-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="83e71-110">Abra o `.vcxproj` arquivo de projeto para seu aplicativo em um editor de texto, como código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="83e71-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="83e71-111">O `.vcproj` arquivo de projeto pode ser um arquivo oculto, o que significa que ele não é exibido no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="83e71-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="83e71-112">Use a linha de comando para localizar arquivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="83e71-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="83e71-113">Localize a seção no código em que você inclui os arquivos de destino do pacote NuGet do WebView2.</span><span class="sxs-lookup"><span data-stu-id="83e71-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="83e71-114">O local no código é realçado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="83e71-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/inserthere.png":::
       <span data-ttu-id="83e71-116">Trecho de código de arquivos de projeto</span><span class="sxs-lookup"><span data-stu-id="83e71-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="83e71-117">Copie o trecho de código a seguir e cole-o onde o `Microsoft.Web.WebView2.targets` está incluído.</span><span class="sxs-lookup"><span data-stu-id="83e71-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/staticlib.png":::
       <span data-ttu-id="83e71-119">Trecho de código inserido</span><span class="sxs-lookup"><span data-stu-id="83e71-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="83e71-120">Edite as dependências adicionais da configuração de compilação do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83e71-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="83e71-121">Para começar, localize todas as `<AdditionalDependencies>` marcas.</span><span class="sxs-lookup"><span data-stu-id="83e71-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="83e71-122">Para cada um, adicione `version.lib` como uma dependência adicional a cada configuração de compilação diferente no `.vcxproj` arquivo.</span><span class="sxs-lookup"><span data-stu-id="83e71-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Trecho de código de arquivos de projeto" lightbox="./media/versionlib.png":::
       <span data-ttu-id="83e71-124">Adicionar `version.lib` a</span><span class="sxs-lookup"><span data-stu-id="83e71-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="83e71-125">A equipe do WebView2 tem o objetivo de automatizar a adição da dependência adicional em lançamentos futuros.</span><span class="sxs-lookup"><span data-stu-id="83e71-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="83e71-126">Compile e execute o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83e71-126">Compile and run your app.</span></span>

### <span data-ttu-id="83e71-127">Entrar em contato com a equipe do WebView2</span><span class="sxs-lookup"><span data-stu-id="83e71-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <span data-ttu-id="83e71-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="83e71-128">See also</span></span>  

*   <span data-ttu-id="83e71-129">Para começar a usar o WebView2, navegue até [WebView2 guias de introdução][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="83e71-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="83e71-130">Para obter um exemplo abrangente de recursos do WebView2, navegue até [WebView2Samples][GithubMicrosoftedgeWebview2samples] no github.</span><span class="sxs-lookup"><span data-stu-id="83e71-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="83e71-131">Para obter informações mais detalhadas sobre APIs do WebView2, navegue até [referência da API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="83e71-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="83e71-132">Para obter mais informações sobre o WebView2, navegue até [recursos do WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="83e71-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Referência de API do Microsoft Edge WebView2 | Documentos da Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Próximas etapas-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Ponto de partida-introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quais são as novidades? -Depurador JavaScript para código do Visual Studio-Microsoft/vscode-js-depuração | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Aplicativos WebView do Microsoft Edge (Chromium)-depurador de código do Visual Studio para Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
