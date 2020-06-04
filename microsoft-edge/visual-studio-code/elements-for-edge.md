---
description: Como usar os elementos do Microsoft Edge (Chromium) a partir do código VS
title: Elementos do Microsoft Edge (Chromium) de código VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, elementos
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694859"
---
# <span data-ttu-id="b7796-104">Elementos da extensão de código do Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="b7796-104">Elements For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="b7796-105">Com os [elementos para Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] vs extensão de código, use a ferramenta elementos do navegador Microsoft Edge de dentro do [código do Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="b7796-105">With the [Elements for Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS Code extension, use the Elements tool of the Microsoft Edge browser from within [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="b7796-106">Ao iniciar ou anexar, a ferramenta elementos se conecta a uma instância do Microsoft Edge, exibe a estrutura HTML do tempo de execução e permite que você altere o layout ou corrija problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="b7796-106">By either launching or attaching, the Elements tool connects to an instance of Microsoft Edge, displays the runtime HTML structure, and allows you to alter the layout or fix styling issues.</span></span>  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Elementos para Edge VS extensão de código no trabalho":::
   <span data-ttu-id="b7796-108">Elementos para Edge VS extensão de código no trabalho</span><span class="sxs-lookup"><span data-stu-id="b7796-108">Elements for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## <span data-ttu-id="b7796-109">Iniciando o Microsoft Edge da extensão de elementos</span><span class="sxs-lookup"><span data-stu-id="b7796-109">Launching Microsoft Edge From the Elements extension</span></span>  

<span data-ttu-id="b7796-110">Navegue até elementos na **barra de atividades**.</span><span class="sxs-lookup"><span data-stu-id="b7796-110">Navigate to Elements in the **Activity Bar**.</span></span>  <span data-ttu-id="b7796-111">Ao lado de onde ele diz **elementos para Microsoft Edge: targets,** há um sinal de adição que abre o navegador do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7796-111">Next to where it says **Elements for Microsoft Edge: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="b7796-112">Se você tiver selecionado a opção **about: Blank** , você deve navegar para o seu aplicativo Web no navegador para que ele apareça no painel de elementos em vs Code.</span><span class="sxs-lookup"><span data-stu-id="b7796-112">If you selected the **about:blank** option, you must navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>  

## <span data-ttu-id="b7796-113">Iniciando o Microsoft Edge a partir do modo de exibição de depuração</span><span class="sxs-lookup"><span data-stu-id="b7796-113">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="b7796-114">Se você estiver acostumado a usar o modo de exibição de depuração no código do Visual Studio, acesse elementos dessa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="b7796-114">If you are accustomed to using the Debug view in Visual Studio Code, access Elements from that tool.</span></span>  <span data-ttu-id="b7796-115">Navegue até o modo de exibição de depuração \ ( `Ctrl` + `Shift` + `D` no Windows ou `Command` + `Shift` + `D` no MacOS \).</span><span class="sxs-lookup"><span data-stu-id="b7796-115">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\).</span></span>  

<span data-ttu-id="b7796-116">Se você não tiver configurações no código do VS, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="b7796-116">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="b7796-117">Selecione **borda** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="b7796-117">Select **Edge** in the dropdown.</span></span> <span data-ttu-id="b7796-118">Você deve ver um `launch.json` arquivo com a configuração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7796-118">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

<span data-ttu-id="b7796-119">Agora que você carregou a configuração correta, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="b7796-119">Now that you have loaded the correct configuration, either press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="b7796-120">A ferramenta elementos, que é familiar para você, do navegador Microsoft Edge é iniciada no código VS, permitindo que você acesse o screencast do seu navegador e examine os componentes da página.</span><span class="sxs-lookup"><span data-stu-id="b7796-120">The Elements tool, that is familiar to you, from the Microsoft Edge browser launches in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>  

## <span data-ttu-id="b7796-121">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b7796-121">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="b7796-122">Para anexar o código VS a uma instância do Microsoft Edge \ (Chromium \), você deve iniciar o navegador executando o seguinte comando no seu terminal.</span><span class="sxs-lookup"><span data-stu-id="b7796-122">To attach VS Code to an instance of Microsoft Edge\(Chromium\), you must start the browser by running the following command from your terminal.</span></span>  

`start msedge --remote-debugging-port=9222`  

<span data-ttu-id="b7796-123">Depois que o aplicativo for iniciado, adicione a configuração abaixo ao arquivo **. JSON de inicialização** :</span><span class="sxs-lookup"><span data-stu-id="b7796-123">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

<span data-ttu-id="b7796-124">Selecione **anexar ao Microsoft Edge e abra a ferramenta elementos** no menu suspenso depurador.</span><span class="sxs-lookup"><span data-stu-id="b7796-124">Select **Attach to Microsoft Edge and open the Elements tool** from the Debugger drop-down menu.</span></span>  <span data-ttu-id="b7796-125">Em seguida, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="b7796-125">Next, either press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="b7796-126">VS o código inicia a ferramenta elementos, permitindo que você acesse o screencast do seu navegador, inspecione o DOM e o estilo dos componentes na página.</span><span class="sxs-lookup"><span data-stu-id="b7796-126">VS Code launches the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>  

## <span data-ttu-id="b7796-127">Entre em contato com os elementos da equipe de extensão de código do Microsoft Edge versus</span><span class="sxs-lookup"><span data-stu-id="b7796-127">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>  

<span data-ttu-id="b7796-128">Envie seus comentários por meio do [arquivamento de um problema][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] no [repositório GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="b7796-128">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="b7796-129">Se você quiser ajudar a melhorar a extensão de código do Microsoft Edge VS, suas contribuições serão bem-vindos!</span><span class="sxs-lookup"><span data-stu-id="b7796-129">If you want to help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="b7796-130">Encontre tudo o que você precisa para começar a usar o [repositório do GitHub][GithubMicrosoftVscodeEdgeDevtools] da extensão.</span><span class="sxs-lookup"><span data-stu-id="b7796-130">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
<span data-ttu-id="b7796-131">Elementos [ImagePngElementsEdge]:./Media/Elements-for-Edge.png "para Edge VS extensão de código em ação"</span><span class="sxs-lookup"><span data-stu-id="b7796-131">[ImagePngElementsEdge]: ./media/elements-for-edge.png "Elements for Edge VS Code extension in action"</span></span>  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Elementos para Microsoft Edge VS extensão de código | Documentos da Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Novo problema-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Elementos do Microsoft Edge (Chromium) | Visual Studio Marketplace"  
